# Installation

{% hint style="info" %}
If you are interested in DeviceOn/ePaper and are used to the Linux platform, we here provide an installer for Ubuntu Linux 20.04 (one of the most popular Linux distributions). This section will guide you on how to install DeviceOn/ePaper on Ubuntu. Note here that:

* The DeviceOn/ePaper Ubuntu Linux installer is named something like “**DeviceOnEPDInstaller\_u2004\_**<mark style="color:red;">**3.x.x**</mark>**.tar.gz**”. To acquire the installer and ensure having the latest version, please go to the [resource page](../../../#download).
* If you are running the installer with an account other than “<mark style="color:blue;">**root**</mark>”, you should use the “<mark style="color:blue;">**sudo**</mark>” command to obtain higher privileges, or the installation may fail at any step.
{% endhint %}

## Steps to Install

**Step 1: Open a terminal**

> The installer runs in CLI (Command Line Interface) mode. As such, open a terminal preferable for you.

**Step 2: Copy the installer to the target host**

> Use the way you like to copy the installer to the target host.

**Step 3: Unwrap the files**

> In the terminal, run “**tar -xvf DeviceOnEPDInstaller\_u2004\_**<mark style="color:red;">**3.x.x**</mark>**.tar.gz**” to unwrap the install files under Ubuntu Linux.

<pre><code><strong>tar -xvf DeviceOnEPDInstaller_u2004_<a data-footnote-ref href="#user-content-fn-1">3.x.x</a>.tar.gz
</strong></code></pre>

**Step 4: Go into the directory**&#x20;

> In the terminal, run “**cd DeviceOnEPDInstaller\_**<mark style="color:red;">**3.x.x**</mark>” to go to the directory.

```
cd DeviceOnEPDInstaller_3.x.x
```

**Step 5: Set the installer as executable**

> In the terminal, run “**sudo chmod +x DeviceOn\_Server\_Ubuntu 20.04\_x64\_**<mark style="color:red;">**3.x.x**</mark>**.run**” so that the installer as an executable file under Ubuntu Linux.

```
sudo chmod +x EPD_Server_Ubuntu-20.04_x64_3.x.x.run
```

**Step 6: Run the installer**

> You may need to run "**sudo ./EPD\_Server\_Ubuntu-20.04\_x64\_3.x.x.run**" to acquire higher privileges if you were logged in as a normal user.

```
sudo ./EPD_Server_Ubuntu-20.04_x64_3.x.x.run
```

**Step 6 (Optional): Run the installer offline**

> You may need to run "**sudo ./run\_install.sh**" to acquire higher privileges if you were logged in as a normal user.

```
sudo ./run_install.sh -o EPD-Dependency-Ubuntu-20.04.iso
```

**Step 7: Answer some questions**

> This installer will guide you through installing DeviceOn/ePaper onto your local machine. All you need to do throughout the installation process is answer some questions as prompted.

<figure><img src="../../../.gitbook/assets/image (225).png" alt=""><figcaption></figcaption></figure>

1. Please read the End-User License Agreement carefully. Press any key when you have finished reading and agree to the terms to continue with the installation.
2. Enter "<mark style="color:blue;">**yes**</mark>" to accept the license agreement.

<figure><img src="../../../.gitbook/assets/image (209).png" alt=""><figcaption></figcaption></figure>

3. Check the running mode  (should run as <mark style="color:red;">**install mode**</mark>) and system dependencies...&#x20;

<figure><img src="../../../.gitbook/assets/image (226).png" alt=""><figcaption></figcaption></figure>

4. DeviceOn/ePaper license is tied to a network interface. The following lists all chooseable network interface information. To install DeviceOn/ePaper, you have to determine which network interface to be tied to.

{% hint style="info" %}
It is strongly recommended to select a <mark style="color:red;">**physical network interface**</mark> instead of a virtual one. Choosing a physical interface avoids any potential issues DeviceOn/ePaper may encounter in the future.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (228).png" alt=""><figcaption></figcaption></figure>

5. Enter a "<mark style="color:blue;">**public static IP**</mark>**"** in this step (Note: It is an important step for key functions such as OTA firmware upgrade, device connection, and image transfer).

<figure><img src="../../../.gitbook/assets/image (230).png" alt=""><figcaption></figcaption></figure>

6. Enter the password for the PostgreSQL database (Note: This is the password for user **postgres** to login the PostgreSQL database).

<figure><img src="../../../.gitbook/assets/image (231).png" alt=""><figcaption></figcaption></figure>

7. Enter the password for the Mongo database (Note: This is the password for user **wisepaas** to login the Mongo database).&#x20;

<figure><img src="../../../.gitbook/assets/image (232).png" alt=""><figcaption></figcaption></figure>

8. Decide whether you want to turn on the Mongo database-capped functionality or not. If you choose yes, please enter "<mark style="color:blue;">**y**</mark>". Then, enter the recommended size: <mark style="color:blue;">**10240**</mark> (MB).

<figure><img src="../../../.gitbook/assets/image (233).png" alt=""><figcaption></figcaption></figure>

> When you run into this step the question shows like above. Just input “**yes**” or “**no**” to enable or disable “capped” functionality. If you answer “yes”, a subsequent question follows to ask you “How much capped size, in MB, to be used? “. Just input the size, in MB, you want to use in the “capped” functionality in the MongoDB database.
>
>
>
> [Capped collections](https://docs.mongodb.com/manual/reference/glossary/#term-capped-collection) are fixed-size collections that support high-throughput operations that insert and retrieve documents based on insertion order. Capped collections work in a way similar to circular buffers: once a collection fills its allocated space, it makes room for new documents by overwriting the oldest documents in the collection.

9. Enter the root email for login DeviceOn/ePaper portal, and type '<mark style="color:blue;">**y**</mark>' to use '<mark style="color:blue;">**root@advantech.com.tw**</mark>'. If you want to use your domain, type '<mark style="color:blue;">**n**</mark>'.
10. The password of user “<mark style="color:blue;">**root@advantech.com.tw**</mark>” to login the DeviceOn/ePaper portal, and the rule should follow the below guideline.

<figure><img src="../../../.gitbook/assets/image (234).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
#### Strong Password Rules:

_Minimum eight characters, at least one number, one lowercase letter, one uppercase letter, and one special character (Blank character, Backslash(\\), Double quotes(") are prohibited)_
{% endhint %}

11. After that, this installer will continue to install EPD Hub, EPD Controller, Service Monitor, and other system settings such as Firewall. Please wait in patience until the overall processes are done. Then, you will see a message like below.

<figure><img src="../../../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>

Finally, a workable DeviceOn/ePaper server should be there as the target host. Open a browser and input **http://{IP-USED-IN-STEP-7.4}**, you should see the DeviceOn/ePaper login page.

<figure><img src="../../../.gitbook/assets/image (219).png" alt=""><figcaption></figcaption></figure>

## Firewall Setting

Check out whether the firewall inbound rules in the following table have been set or not (We have set up the necessary port by default).

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
| 60001-60100 | Enable                                  | FTP Passive Mode       |



[^1]: 
