# Azure Marketplace

## Deploy DeviceOn/ePaper from Azure Marketplace

Step 1: Please enter [Azure Marketplace](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/advantech.deviceon\_epaper\_on\_ubuntu\_vm\_v1?tab=Overview) and click “GET IT NOW”

<figure><img src="../../.gitbook/assets/image (235).png" alt=""><figcaption></figcaption></figure>

Step 2. Sign in with your Azure account.

<figure><img src="../../.gitbook/assets/image (236).png" alt=""><figcaption></figcaption></figure>

Step 3. You will enter to Azure portal and please click on Start with pre-set configuration to be quick deployment

<figure><img src="../../.gitbook/assets/image (237).png" alt=""><figcaption></figcaption></figure>

Step 4. This page includes our recommended configuration for DeviceOn/ePaper Server, you can click on Continue to create VM, following the default setting.

<figure><img src="../../.gitbook/assets/image (238).png" alt=""><figcaption></figcaption></figure>

Step 5. On this page, please fill in the following information. Please note that the red-star items are required.

* 5-1. Select your Azure subscription
* 5-2. Create a new resource group or pick an existed one
* 5-3. Decide on your virtual machine name
* 5-4. Select the region of the virtual machine. You can pick one which is the nearest one to your location
* 5-5. Select DeviceOn ePaper - Gen2 as default image
* 5-6. Create an administrator account with username and password. Please note that you must remember them for remote access your virtual machine (with SSH connection).
* 5-7. Then click Next to continue to set-up the advanced setting, or click the Review + create to remain to default instead (skip to Step 9).

<figure><img src="../../.gitbook/assets/image (239).png" alt=""><figcaption></figcaption></figure>

Step 6. On this page, you can choose the disk type on the virtual machine, or use the disk **Standard SSD** instead. Then click Next to move on.

<figure><img src="../../.gitbook/assets/image (240).png" alt=""><figcaption></figcaption></figure>

Step 7. On this page, you can configure the network interface, or use the default setting instead. Then click **Next** to move on.

<figure><img src="../../.gitbook/assets/image (241).png" alt=""><figcaption></figcaption></figure>

Step 8. On this page, you can schedule the power management of the virtual machine to reduce unnecessary costs, or use the default setting instead. Then click Review + Create to move on.

<figure><img src="../../.gitbook/assets/image (242).png" alt=""><figcaption></figcaption></figure>

Step 9. On this page, Azure will validate your virtual machine (within 5 minutes) and summarize your product details including the prices and legal terms. Please click Create to move on.

<figure><img src="../../.gitbook/assets/image (243).png" alt=""><figcaption></figcaption></figure>

Step 10. A few minutes later, you can see below the picture that your virtual machine has been created.

<figure><img src="../../.gitbook/assets/image (244).png" alt=""><figcaption></figcaption></figure>

## Sign In DeviceOn/ePaper

Step 1: Go to the **Overview** blade and find the server IP for your virtual machine

<figure><img src="../../.gitbook/assets/image (191).png" alt=""><figcaption></figcaption></figure>

Step 2. Open a browser and enter the URL with the server IP to access the DeviceOn/ePaper server. Please enter your default account and password (Please get in touch with Advantech provider to get one) and click the Sign In button to sign in.

<figure><img src="../../.gitbook/assets/image (192).png" alt=""><figcaption></figcaption></figure>

## Setup Firewall Rules on Azure VM

{% hint style="info" %}
There is no need to configure firewall settings on Azure VM because this subscription will automatically set up all necessary inbound port rules.&#x20;
{% endhint %}

Step 1. Please go to the **Networking** blade under the Settings.

<figure><img src="../../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure>

Step 2. Check out whether the firewall inbound rules in the following table have been set or not (We have set up the needed port by default).

| Port        | Inbound rule                            | Service                |
| ----------- | --------------------------------------- | ---------------------- |
| 22          | <mark style="color:red;">Disable</mark> | SSH\*                  |
| 80          | Enable                                  | HTTP                   |
| 443         | Enable                                  | HTTPS                  |
| 8090        | <mark style="color:red;">Disable</mark> | Service Monitor        |
| 1883        | Enable                                  | MQTT                   |
| 8883        | Enable                                  | TLS/SSL encrypted MQTT |
| 5672        | Enable                                  | AMQP                   |
| 5671        | Enable                                  | TLS/SSL encrypted AMQP |
| 2121        | Enable                                  | FTP                    |
| 60001-60085 | Enable                                  | FTP Passive Mode       |

Step 3. We recommend closing SSH connection port 22 (Enable it if you want to access VM via SSH connection for debugging purposes).

<figure><img src="../../.gitbook/assets/image (189).png" alt=""><figcaption></figcaption></figure>

Step 4. We recommend closing Service Monitor port 8090 (Enable it if you want to monitor each service for debugging purposes).

<figure><img src="../../.gitbook/assets/image (190).png" alt=""><figcaption></figcaption></figure>
