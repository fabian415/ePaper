# Upgrade

{% hint style="info" %}
**Prerequisite**

1. Your system MUST have installed DeviceOn/ePaper software.
2. Upgrade version MUST be higher than the installed version.
{% endhint %}

## Steps to Upgrade

**Step 1: Open a terminal**

> The installer runs in CLI (Command Line Interface) mode. As such, open a terminal preferable for you.

**Step 2: Copy the installer to the target host**

> Use the way you like to copy the installer to the target host.

**Step 3: Unwrap the files**

> In the terminal, run “**tar -xvf DeviceOnEPDInstaller\_u2004\_**<mark style="color:red;">**3.x.x**</mark>**.tar.gz**” to unwrap the install files under Ubuntu Linux.

```
tar -xvf DeviceOnEPDInstaller_u2004_3.x.x.tar.gz
```

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

<figure><img src="../../../.gitbook/assets/image (201).png" alt=""><figcaption></figcaption></figure>

1. Please read the End-User License Agreement carefully. Press any key when you have finished reading and agree to the terms to continue with the installation.
2. Enter "<mark style="color:blue;">**yes**</mark>" to accept the license agreement.

<figure><img src="../../../.gitbook/assets/image (220).png" alt=""><figcaption></figcaption></figure>

3. Check the running mode (should run as <mark style="color:red;">**upgrade mode**</mark>) and system dependencies...&#x20;

<figure><img src="../../../.gitbook/assets/image (221).png" alt=""><figcaption></figcaption></figure>

4. After upgrading the DeviceOn/ePaper, this installer will continue to install EPD Hub, EPD Controller, Service Monitor, and other system settings such as Firewall. Please wait in patience until the overall processes are done. Then, you will see a message like below.

<figure><img src="../../../.gitbook/assets/image (222).png" alt=""><figcaption></figcaption></figure>
