# EPD Roaming

In automated warehouse management applications, when an EPD device on a cargo connects to the wireless network, the system can dispatch tasks to the EPD device. The EPD device monitors cargo movements in and out of the warehouse in real-time end records the picking status, which can achieve automated management. However, EPD devices sometimes move along with the attached cargo, requiring roaming between different routers to maintain connectivity. DeviceOn/ePaper provides a solution that allows EPD devices to roam across routers while ensuring that tasks continue to transfer to the new router, enabling continuous screen updates.

## Overview

<figure><img src="../../.gitbook/assets/image (354).png" alt=""><figcaption></figcaption></figure>

## Limitation

A single WISE-3240 device can connect to a maximum of 400 EPD devices simultaneously. If this number is exceeded, there is a risk that additional EPD devices may not be able to connect to DeviceOn/ePaper.

## Steps

According to the EPD Router settings, DeviceOn/ePaper has a default whitelist mechanism. Only EPD devices listed in the whitelist can connect to the EPD Router. To enable the EPD roaming feature, you must disable the whitelist function on the EPD Router. This allows EPD devices to roam and transfer tasks seamlessly between multiple EPD Routers.

Here are the steps:

**Step 1. Access Whitelist Setting**. Go to the EPD Router’s whitelist setting interface, then click the **setting** icon.

<figure><img src="../../.gitbook/assets/image (355).png" alt=""><figcaption></figcaption></figure>

**Step 2. Disable Whitelist Function**: Navigate to the whitelist settings and disable the whitelist feature. This change allows any EPD device to connect to the EPD Router, not just those listed in the whitelist.

**Master switch**

> Once this master switch is turned off, DeviceOn/ePaper will automatically disable the whitelist settings for all connected Routers as well as any new Routers that are added to the network.

<figure><img src="../../.gitbook/assets/image (358).png" alt=""><figcaption></figcaption></figure>

**Individual switch**

<figure><img src="../../.gitbook/assets/image (359).png" alt=""><figcaption></figcaption></figure>

By following these steps, you can facilitate seamless roaming and task continuation for EPD devices in a dynamic and large-scale warehouse environment, enhancing operational efficiency and flexibility.
