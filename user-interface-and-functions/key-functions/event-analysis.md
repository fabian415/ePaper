# Event Analysis

{% hint style="info" %}
The event logs from DeviceOn/ePaper record detail information relevant to EPD devices. Through event analysis, we can obtain the following details:

1. The timing of initiating transmitting tasks.
2. The duration required for each transmitting task.
3. The frequency of transmitting tasks. (For example, for a single device)
4. The online and offline status of  EPD devices. (Possibly due to unstable wireless environment or other reasons)
5. The occurrence of abnormal system reboots.
{% endhint %}

## DeviceOn/ePaper Events

Step 1. Navigate to **Setting - Event** page, choose the time range, and then download DeviceOn/ePaper events.

> Before DeviceOn/ePaper Build 1701, the maximum number of event records was 10,000. After Build 1702, the maximum number of event records increased to 50,000.

<figure><img src="../../.gitbook/assets/image (310).png" alt=""><figcaption></figcaption></figure>

A CSV file will be generated. Decide where to save it.

<figure><img src="../../.gitbook/assets/image (311).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (312).png" alt=""><figcaption></figcaption></figure>

## Events Analysis

#### Basic introduction to the event fields.

<figure><img src="../../.gitbook/assets/image (313).png" alt=""><figcaption></figcaption></figure>

#### Timeline of a transmit task

<figure><img src="../../.gitbook/assets/image (314).png" alt=""><figcaption></figcaption></figure>

#### How long does each EPD transmitting task take?

Step 1. Utilize Excel's filtering function to select a specific device name.

Step 2. Locate the "**Transmit tag image**", "**Transmit tag image command accepted**" and "**Transmit tag image successfully**" events.

Step 3. Upon inspecting the events, it is observed that within a span of 1 minute, 19 tasks were initiated for the same device.

<figure><img src="../../.gitbook/assets/image (315).png" alt=""><figcaption></figcaption></figure>

#### Frequency for single device tasks

Step 1. Utilize Excel's filtering function to select a specific device name.

Step 2. Locate the "**Transmit tag image**" or "**Batch tag transmit**" event.

Step 3. Upon inspecting the events, it is observed that within a span of 1 minute, 19 tasks were initiated for the same device.

<figure><img src="../../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>

> In typical scenarios, an EPD device can usually handle only 1 to 3 tasks per minute. Therefore, this situation would be considered excessive usage of the EPD device, potentially leading to rapid battery drainage.

#### EPD Online and Offline Status

Step 1. Utilize Excel's filtering function to filter devices.

Step 2. Locate the "**Device disconnect**" and "**Device connected**" events.

Step 3. Upon inspecting the events, it is highly abnormal for some devices, such as EPD-Tag-32f6c8, to repeatedly go online and offline within a span of approximately two hours, from 4:50 PM to 7:08 PM on February 18, 2023. This behavior suggests potential issues with connectivity or device instability that require further investigation.

<figure><img src="../../.gitbook/assets/image (316).png" alt=""><figcaption></figcaption></figure>

> The online and offline status of EPD devices can be influenced by various factors, such as unstable wireless environments or other reasons.

#### Unstable Situations for EPD\_Hub or EPD Routers

Step 1. Utilize Excel's filtering function to select a specific device name.

Step 2. Locate the "**EPD\_Hub**" or "**EPD-Router-xxxxxx**" devices.

Step 3. Upon inspecting the events, it is observed that EPD\_Hub has connected, which means that this system may encounter a unexpected reboot.

<figure><img src="../../.gitbook/assets/image (317).png" alt=""><figcaption></figcaption></figure>

## System Log Analysis

#### System Unexpected Shutdown

<figure><img src="../../.gitbook/assets/image (318).png" alt=""><figcaption></figcaption></figure>

#### System Normal Shutdown

<figure><img src="../../.gitbook/assets/image (319).png" alt=""><figcaption></figcaption></figure>
