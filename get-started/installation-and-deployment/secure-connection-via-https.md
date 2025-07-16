# Secure Connection via HTTPS

{% hint style="info" %}
In this recipe, we will generate a **Let's Encrypt** certificate using **Certbot**. This certificate will then be deployed for use in the DeviceOn/ePaper server.

* [Let’s Encrypt](https://letsencrypt.org/) is a free, automated, and open-source Certificate Authority.
* [Certbot](https://certbot.eff.org/) is a console-based certificate generation tool for Let's Encrypt.

**Please Note:** For production environments, it is strongly recommended to obtain an SSL/TLS certificate from a trusted and reputable Certificate Authority (CA) based on your organization's security and compliance requirements. Each CA provides its procedures for certificate issuance, validation, and renewal, which should be followed accordingly.

In this guide, we use **Let’s Encrypt**, a free and automated open-source CA, as an example to illustrate the certificate generation and deployment process. While Let’s Encrypt is suitable for development or internal use, organizations requiring extended validation, wildcard domains, or long-term support should consider using a commercial CA.
{% endhint %}

**Requirements:**

1. Port 443 for https needs to be open and available at time of executing certbot.
2. Certbot needs root access while executing because only root is allowed to bind to any port below 1024.

#### Step 1. Access the [Certbot](https://certbot.eff.org/instructions?ws=other\&os=snap) website and select certbot instructions as below

<figure><img src="../../.gitbook/assets/image (454).png" alt=""><figcaption></figcaption></figure>

#### Step 2. SSH into the server and install snapd with sudo privileges

```
sudo apt update
sudo apt install snapd
```

