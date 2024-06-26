# 🔐 Security Architecture

System Security is about not only installing and onboarding devices and networks securely but also managing their ongoing operations throughout their lifecycle and identifying and isolating any threats. Industries everywhere are digitizing, which is creating a multitude of new security requirements for the Internet of Things (IoT). End-to-end (E2E) security management will be essential to ensuring security and privacy in the IoT, while simultaneously building strong identities and maintaining trust. As the diversity of IoT services and the number of connected devices continue to increase, the threats to IoT systems are changing and growing even faster.

A comprehensive model of IoT device security, as shown below structure, the comprehensive IoT module security in an IoT system has three main parts:

<figure><img src="../../.gitbook/assets/image (212).png" alt=""><figcaption><p>Security Architecture on DeviceOn/ePaper solutions</p></figcaption></figure>

## Device Security

DeviceOn/ePaper Server leverages McAfee Embedded Security software to prevent unauthorized changes and will lock a system down to a known application is an industry, that’s an industrial first solution to secure embedded devices. For disaster recovery, Acronis provides users with a quick and easy-operated solution to protect data and recover the entire system even when OS crashes, effectively reducing down-time cost and lowering the risk of data loss. In the Zigbee solution at the edge, during the EPD device joining the network, the EPD router uses EPID (Extended PAN ID) to create a private network to filter non-EPD devices. EPD device is a wireless microcontroller unit (MCU). It has a built-in hardware accelerator for the Advanced Encryption Standard (AES) algorithm, which is commonly used for secure data communication over wireless networks. The encryption protocol of the Wi-Fi solution is WPA2 (Wi-Fi Protected Access 2), which provides encryption to protect data from being intercepted or tampered with during transmission.

## Secure Transporty

The server distributed SSL certificates to use TLS (v-1.3) as an encrypted and secure data transmission channel, and the device default enabled MQTT-SSL for communication.

* Topics Isolation and Unique Device IoT Key

Topics are specially handled in RabbitMQ. Topics are not public. Access control isolates an activated device from publishing/subscribing only to that device’s topics even though multiple devices will have subscriptions to identically named topics. A device is not allowed to subscribe/publish to another device’s topics. Second, in IoT applications, command topics are used to control a device remotely and to acknowledge successful command executions. Unlike telemetry, command topics are not read-only. Commands are a back-and-forth workflow that can occur **between the cloud and devices**. Because commands are actionable messages, **isolate the MQTT topic for command messages from telemetry topics**.

* Use x.509 Certificates to Authenticate Edge Device

DeviceOn/ePaper supports x.509 certificate authentication for use with a secure TLS/SSL connection. The x.509 edge device authentication **allows devices to authenticate to servers with certificates rather than with a username and password**.

* ~~Use TPM + x.509 Certificates to Provide Higher Security~~

~~The solution that we integrate on DeviceOn/ePaper for Azure (Enterprise Edition), leverages Azure IoT Edge and TPM 2.0 to offer secure authentication and private key protection. TPM, also known as ISO/IEC 11889, is a standard for securely generating and storing cryptographic keys. TPM also refers to a virtual or physical I/O device that interacts with modules that implement the standard. A TPM device can exist as discrete hardware, integrated hardware, a firmware-based module, or a software-based module.~~

## Secure Cloud Service

The cloud service components include Tomcat as a web server that provides an HTTPS protocol and backend API services, each connection between the backend and database adopts SSL encryption and enforces password policies. Second, for an advanced attack, such as SQL injection, XXC, or local and remote file vulnerabilities, the Nginx+Naxsi to achieve Web Application Firewall (WAF) protection. All DeviceOn/ePaper services pass through famous vulnerability tools to ensure security for your it IoT solutions, and the binary uses ProGuard code obfuscation protection. The API authentication uses JWT (JSON Web Tokens) to hide/encrypt sensitive data for security.

## Role-based Access Control (RBAC)

DeviceOn/ePaper supports three different user [roles](http://ess-wiki.advantech.com.tw/view/File:Role\_Permission.xlsx) - “Root”, “System Admin” and “Device Admin”. There is only one single “Root” account per system, which has the highest permission level and can create “System Admin” or “Device Admin” accounts. The intermediate user level “System Admin” can be used to create “Device Admin” accounts. “Device Admin” accounts have the lowest permission level.

## SSL Encryption

* _HTTPS on DeviceOn/ePaper Web Server_

The principal motivations for HTTPS are authentication of the accessed website, and protection of the privacy and integrity of the exchanged data while in transit. It protects against man-in-the-middle attacks. The bidirectional encryption of communications between a client and server protects against eavesdropping and tampering of the communication.

* _SSL Connection on Database (PostgreSQL, MongoDB)_

PostgreSQL and MongoDB have native support for using SSL connections to encrypt client/server communications for increased security.

* _Create Security Credentials on Database_

Databases are by default protected by secure credentials and require explicit authentication for connections. This avoids accidentally deploying platforms with unprotected access.

* _Device Connectivity via MQTT SSL_

RabbitMQ supports multiple protocols including MQTT, which is the most popular IoT (Internet of Things) protocol. By default, SSL is used to encrypt all MQTT traffic for device connectivity.

* _Enforce Password Policies_

While DeviceOn/ePaper allows you to set some of your passwords, please make sure those meet the minimum complexity requirements established by your specific organization.

## Vulnerability Scanning Tools

The DeviceOn/ePaper server pass through below famous vulnerability tools to ensure security for your AIoT solutions. Furthermore, all the testing including anti-malware (Trend Micro and Kaspersky)

* _Web Application Assessment Report (Micro Focus)_

WebInspect is an automated dynamic testing tool that mimics real-world hacking techniques and attacks, and provides comprehensive dynamic analysis of complex web applications and services.

* _OpenVAS (Open Vulnerability Assessment System)_

OpenVAS is a full-featured vulnerability scanner. Its capabilities include unauthenticated testing, authenticated testing, various high level and low-level Internet and industrial protocols, performance tuning for large-scale scans and a powerful internal programming language to implement any type of vulnerability test.The scanner is accompanied by a vulnerability tests feed with a long history and daily updates. This Greenbone Community Feed includes more than 50,000 vulnerability tests.

* _Nessus_

Nessus is the de-facto industry standard vulnerability assessment solution for security practitioners. The latest intelligence, rapid updates, an easy-to-use interface.

1. Covers an industry-leading 47,000+ vulnerabilities
2. Unlimited scans at no extra cost
3. Compliant with PCI, HIPPA, GLBA, CIS, NIST, and more

* _OWASP ZAP_

The OWASP Zed Attack Proxy (ZAP) is one of the world’s most popular free security tools and is actively maintained by hundreds of international volunteers\*. It can help you automatically find security vulnerabilities in your web applications while you are developing and testing your applications. It’s also a great tool for experienced pentesters to use for manual security testing.

* _Skipfish_

Skipfish is an active web application security reconnaissance tool. It prepares an interactive sitemap for the targeted site by carrying out a recursive crawl and dictionary-based probes. The resulting map is then annotated with the output from a number of active (but hopefully non-disruptive) security checks. The final report generated by the tool is meant to serve as a foundation for professional web application security assessments.Key features:

1. High speed: pure C code, highly optimized HTTP handling, minimal CPU footprint – easily achieving 2000 requests per second with responsive targets.
2. Ease of use: heuristics to support a variety of quirky web frameworks and mixed-technology sites, with automatic learning capabilities, on-the-fly wordlist creation, and form autocompletion.
3. Cutting-edge security logic: high quality, low false positive, differential security checks, capable of spotting a range of subtle flaws, including blind injection vectors.

* _Nikto_

Nikto is an Open Source (GPL) web server scanner which performs comprehensive tests against web servers for multiple items, including over 6700 potentially dangerous files/programs, checks for outdated versions of over 1250 servers, and version specific problems on over 270 servers. It also checks for server configuration items such as the presence of multiple index files, HTTP server options, and will attempt to identify installed web servers and software. Scan items and plugins are frequently updated and can be automatically updated.

* _W3af_

w3af is a Web Application Attack and Audit Framework. The project’s goal is to create a framework to help you secure your web applications by finding and exploiting all web application vulnerabilities.

* _Arachni_

Arachni is a fully featured web security scanning tool, it is based on ruby framework.It is an open source, modular and high performance tool. It comes with both command line interface as well as web based gui interface, it is highly versatile tool for security scanning purpose. It supports almost all of the popular web application such as HTML5, Java Script and AJAX etc, Additionally it is enables with multi user-multi platform collaboration.It allows you to generate reports in desired format (.txt, XML, HTML).

## Third-Party Vulnerability Fixed and Updates

* OpenJRE (v-1.8.0\_292-1)

CVE-2021-42340, CVE-2022-23181, CVE-2022-29885

* Tomcat (v-9.0.63)

CVE-2021-33037, CVE-2021-30640, CVE-2021-30639, CVE-2020-9484, CVE-2021-25329, CVE-2021-25122

* RabbitMQ (v-3.11.6), Erlang 25

CVE-2022-37026

* PostgreSQL (v-14.2)

CVE-2021-23214, CVE-2021-23222

* MongoDB (v-4.4.14)
