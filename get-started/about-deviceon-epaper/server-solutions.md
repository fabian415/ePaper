# 🖥️ Server Solutions

DeviceOn/ePaper is a software platform developed by Advantech, which comprises an IoT Hub (RabbitMQ), database (PostgreSQL and MongoDB), web service (Tomcat), storage (Apache FTP), and DeviceOn/ePaper core services. Here we provide three ways to help customers fast deploy their ePaper solutions - standalone installer, on-premise ARK, and subscription from Azure marketplace.&#x20;

## Standalone Installer

The standalone version provides all packages of the DeviceOn/ePaper software in one installer package, including RabbitMQ as a message broker, MongoDB, PostgreSQL as databases, Apache FTP for image storage, Tomcat for web services, and a watchdog service that protects DeviceOn/ePaper core components from crashing or becoming unresponsive.

This section specifies the minimum hardware requirements for DeviceOn/ePaper Cloud (Standalone) and the operating systems on which DeviceOn/ePaper is supported. In general, the better the hardware configuration of your computer, the better your experience with DeviceOn/ePaper will be. To achieve a more satisfying experience with DeviceOn/ePaper, particularly in terms of the client software, it is highly recommended that your system be substantially better than the minimum requirements specified in the following sections. This is particularly true if running server software locally on the same system as the client software.

Attention to the following areas can make a significant improvement to your overall user experience and enjoyment of the software:

* <mark style="color:blue;">Memory - at least 16 GB or more.</mark>
* <mark style="color:blue;">CPU - Intel Core i7 6600U (CPU Benchmark: 3446) or more.</mark>
* <mark style="color:blue;">Hard Drive - 128 GB SSD or 1TB HDD.</mark>

General Operation Systems and Recommendations:

* <mark style="color:blue;">Ubuntu-20.04 64-bit</mark>

## **On-premise ARK**

The On-premise ARK solution for DeviceOn/ePaper involves integrating the DeviceOn/ePaper software into Advantech's ARK machines, such as the ARK-2250A2 and ARK-1123HA2. This approach bundles the ePaper management software with robust hardware, providing a comprehensive, self-contained solution. It's particularly suited for environments where on-site management and data handling are preferred, offering enhanced control and security. This solution is ideal for users who seek a reliable, integrated system for managing ePaper devices without the need for external cloud services.

Order Information:

| Model Name    | Part Number     | Description                                                                                          |
| ------------- | --------------- | ---------------------------------------------------------------------------------------------------- |
| EPD-ARK-1123H | ARK-1123H-EP2A2 | Ubuntu 18.04 64-bit / 8G RAM / 128 GB SSD machine built in DeviceOn/ePaper with a 500-device license |
| EPD-ARK-2250L | ARK-2250L-EP1A2 | Ubuntu 18.04 64-bit / 16G RAM / 1TB HDD machine built in DeviceOn/ePaper with a 500-device license   |

## &#x20;Subscription from Azure Marketplace

The DeviceOn/ePaper VM (Virtual Machine) can be initiated directly from the Azure Marketplace. This enables users to easily deploy and manage the DeviceOn/ePaper service in a cloud environment, leveraging the scalability and flexibility of Azure's cloud infrastructure. By starting the VM from the Azure Marketplace, users benefit from a streamlined setup process and can quickly integrate the DeviceOn/ePaper service with their existing Azure-based systems and services, making it a convenient and efficient solution for cloud-based ePaper device management.

Current Version of DeviceOn/ePaper on Azure Marketplace:

* <mark style="color:blue;">v1907 (Ubuntu-20.04 64-bit)</mark>

Please follow the instructions below to guide you to start this feature.&#x20;

{% embed url="http://ess-wiki.advantech.com.tw/view/DeviceOn_ePaper_Azure_Marketplace" %}

