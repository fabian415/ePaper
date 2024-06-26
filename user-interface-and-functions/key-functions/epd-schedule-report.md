# EPD Schedule Report

{% hint style="info" %}
The EPD schedule report provides a regular report on EPD usage, primarily sent to users regarding EPD anomalies. It includes statistical reports on weak signals of electronic paper devices, device disconnections, and image refresh failures. This report helps users clarify the usage conditions of the wireless environment on-site, continuously track changes in the electronic paper signal, and ultimately assist users in building a stable and properly functioning EPD usage scenario.
{% endhint %}

> This function is only available in the v1905 or higher.

## Google Mail Service

You can follow the instructions below to get one for free.

Step 1. Open a browser and enter the Google url: [https://www.google.com](https://www.google.com). Create a Google account if you do not have one.

<figure><img src="../../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

Step 2. Sign in your Google account, and then go to manage your Google account.

<figure><img src="../../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>

&#x20;

Step 3. Open the two-step validation in the security section.

<figure><img src="../../.gitbook/assets/image (111).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="../../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure>

You will see the following message inform you a success.

<figure><img src="../../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>

Step 4. Then, get an App password for Mail Service usage.

<figure><img src="../../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>

Then you will see the following dialog. Please save this password and this password will be used in the later section.

<figure><img src="../../.gitbook/assets/image (306).png" alt=""><figcaption></figcaption></figure>

## Email Service Setting

Step 1. Open a browser and enter the DeviceOn/ePaper url: http://\[Your\_Server\_IP]. Sign in with **root** account.

<figure><img src="../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

Step 2. Navigate to the **Setting–System** page, and click the **Email Service Setting**.

<figure><img src="../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

Step 3. Please fill in the following information:

* **On/Off:** On
* **Email Server:** smtp.gmail.com
* **Port:** 465 SSL
* **Email Account:** \[Your google mail]
* **Email Password:** \[Your two-step validation password]
* **Sender Email:** \[Your google mail]
* **Email Subject:** EPD

<figure><img src="../../.gitbook/assets/image (106).png" alt=""><figcaption></figcaption></figure>

Step 4 (Optional). You can test whether this mail service works or not. Click the test button and fill in the following information.

<figure><img src="../../.gitbook/assets/image (107).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

If this mail service works, you should receive a mail like this.

<figure><img src="../../.gitbook/assets/image (307).png" alt=""><figcaption></figcaption></figure>

## EPD Schedule Report Setting

Step 1. Navigate to the **Setting–System** page, and click the **EPD Schedule Report**.

<figure><img src="../../.gitbook/assets/image (102).png" alt=""><figcaption></figcaption></figure>

Step 2. Fill in the following information.

* **Activation:** ON
* **Recipients:** \[Recipients’email] Multiple recipients should be separated by semicolon (;).
* **Interval:** 1 day / 1 week / 1 month
* **Report Time:** When users will receive the report.
* **Rules (Recommended):**
  * **Low Battery Report:** Battery <= Bad
  * **Device Offline Report:** Device Offline for 4 days
  * **Low Signal Report:** RSSI <= -75 for 3 times per day
  * &#x20;**Refresh Error Report:** Image Failed for 1 times per day

<figure><img src="../../.gitbook/assets/image (308).png" alt=""><figcaption></figcaption></figure>

If this mail service works, you should receive a mail like this.

<figure><img src="../../.gitbook/assets/image (309).png" alt=""><figcaption></figcaption></figure>
