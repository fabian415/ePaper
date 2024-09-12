# Remote Backup

{% hint style="info" %}
Remote backup for a DeviceOn/ePaper server is a crucial part for protecting against data loss from hardware failures, accidental deletions, software issues, natural disasters, and cyber threats. They ensure business continuity by enabling quick data restoration in case of disasters, provide an extra layer of data redundancy and integrity and help meet regulatory compliance requirements by securing data offsite. This minimizes downtime and disruption, safeguarding critical information and maintaining operational resilience.
{% endhint %}

## Overview

<figure><img src="../../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>

## Backup setting

Step 1. Sign in DeviceOn/ePaper with a super admin role (root).

<figure><img src="../../.gitbook/assets/image (119).png" alt=""><figcaption></figcaption></figure>

Step 2. Select the **Setting - System** option, and then click the **System Backup** button.

<figure><img src="../../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>

Step 3. Choose an external FTP storage as a backup storage.

<figure><img src="../../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure>

Step 4. After midnight, this server will back up all necessary materials (Databases, OTA packages, images, scripts, etc) to this remote repository.&#x20;

File location: /SYSTEM\_BK/{Server MAC}/Backup\_{date}.zip

## &#x20;![](<../../.gitbook/assets/image (127).png>)

## Recovery procedure

Step 1. Install **the same version** of DeviceOn/ePaper on the new machine

Step 2. Copy Backup\_xxxxxxxx.zip file to the new machine

Step 3. `unzip` Backup\_xxxxxxxx.zip

Step 4. Use the `cd` command to navigate to the directory where `run.sh` is located

Step 5. Use the `chmod` command to make `run.sh` script executable

Step 6. Run `run.sh`

<figure><img src="../../.gitbook/assets/image (285).png" alt=""><figcaption></figcaption></figure>

**Note:** If you want to migrate DeviceOn/ePaer from Ubuntu 18.04 (Acronis) to Ubuntu 20.04 (Installer), you can change an internal parameter within the `run.sh` script to set **`IS_UBUNTU_INSTALLER=true`**
