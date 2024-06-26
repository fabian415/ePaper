# Abnormal Alert

> As continuous monitoring of service status may not be feasible, setting up email notifications becomes crucial for promptly alerting any service anomalies. This process will guide users on configuring email settings for reporting such issues.

1. Open a browser and input **http://{YOUR\_SERVER\_IP}:8090**, you should see the Server Monitor login page.

> Sign into Service Monitor with the default account credentials.

<figure><img src="../../../.gitbook/assets/image (184).png" alt=""><figcaption></figcaption></figure>

2. Click on the **Alarm Setting** tab on the left-side menu, and then fill in necessary information about mail server and recipients. You can click "Try it" button to test whether the setting is correct or not.

* On/Off: On
* Host: smtp.gmail.com
* Port: 465
* Method: SSL
* Account: Your Gmail Account
* Password: Application-specific password
* Service: Which service you want to monitor?&#x20;
* Interval: 10 Minutes&#x20;
* Recipient Emails: Recipient (If there are multiple recipients, separate them with semicolons) &#x20;

<figure><img src="../../../.gitbook/assets/image (165).png" alt=""><figcaption></figcaption></figure>

You can use your Gmail SMTP server to send emails.

{% embed url="https://www.youtube.com/watch?v=FZfneLNyE4o" %}

2. Click Yes to confirm to send the e-mails.

<figure><img src="../../../.gitbook/assets/image (166).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (167).png" alt=""><figcaption></figcaption></figure>

3. Then you will receive the test email.

<figure><img src="../../../.gitbook/assets/image (168).png" alt=""><figcaption></figcaption></figure>
