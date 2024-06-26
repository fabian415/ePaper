# How to estimate the deployment of EPD system?

Because of the wireless signal is invisible, we have to do a site survey before deploying the EPD system. Many factors affect wireless signals. The major effect is in the different fields the occupy frequency is different. All objects made of metal in the field will affect the direction of radio wave reflection. This document will tell you what you need to do in the site survey.

## Hardware Requirement

1\.      WISE-3240

2\.      ARK-2250 or ARK-1123

3\.      More than 6 EPD-230

4\.      Spectrum Analysis tool

## WISE-3240 Field Estimate

When you want to deploy WISE-3240 in the field, you have to know the below information.

<figure><img src="../../../../.gitbook/assets/image (360).png" alt=""><figcaption></figcaption></figure>

Three dimensional radiation pattern of the antenna

<figure><img src="../../../../.gitbook/assets/image (362).png" alt=""><figcaption></figcaption></figure>

Following I will demo how to estimate the WISE-3240 and EPD-230 deployment position.

### **Step 1. Check 2.4GHz RF environment**

{% content-ref url="how-to-collect-channel-status-from-rf-explorer.md" %}
[how-to-collect-channel-status-from-rf-explorer.md](how-to-collect-channel-status-from-rf-explorer.md)
{% endcontent-ref %}

{% file src="../../../../.gitbook/assets/Channel_Select.xlsx" %}

Open “**How to Collect Channel Status from RF Explorer?**” and follow the steps to do the configuration. By using the RF Explorer tool, you will know which channel is suitable for deployment.&#x20;

Example:&#x20;

After you finish the configuration, you will see the analysis result as below. Please select the channel which the “Rank” is green. You can select channel 11,24,25 or 26. Normally a clean channel can deploy two GWs.&#x20;

<figure><img src="../../../../.gitbook/assets/image (363).png" alt=""><figcaption></figcaption></figure>

You can change GW transmit frequency by using DeviceOn/ePaper. Please follow below steps.&#x20;

Step 1.1:&#x20;

<figure><img src="../../../../.gitbook/assets/image (364).png" alt=""><figcaption></figcaption></figure>

Step 1.2:&#x20;

<figure><img src="../../../../.gitbook/assets/image (365).png" alt=""><figcaption></figcaption></figure>

Step 1.3:

<figure><img src="../../../../.gitbook/assets/image (366).png" alt=""><figcaption></figcaption></figure>

Step 1.4: Change the channel value

<figure><img src="../../../../.gitbook/assets/image (367).png" alt=""><figcaption></figcaption></figure>

### **Step 2. Deploy EPD-230 in the Field.**&#x20;

Normally, you can place the EPD device anywhere. But how to make all EPD devices online stable? This is our main consideration. Some people think that the stronger the signal, the better, but we have to evaluate that all EPD devices in the field are online. Therefore, the RSSI of all EPD devices needs to be greater than -70 dBm. If the RSSI of an electronic paper is lower than -70 dBm, then that device will easily offline.&#x20;

Before you deploy the EPD device in the field, you should have a floor plan. It will help you to know how many WISE-3240 should be in the deployment field.

### **Step 3. Choose WISE-3240 deploy position.**&#x20;

After EPD devices location is decided, you have to choose the WISE-3240 deploy position.&#x20;

In the different fields, the WISE-3240 position will affect the tag receiving the wireless signal. This document will show some samples below.&#x20;

#### **Case 1: Smart warehouse application.**

In the small warehouse, all EPD devices will be in the small region (Ex. More than 400 EPD devices within a radius of 20 meters). The Shelf material is metal and it will cause serious interference. In the field, we recommend all EPD devices are deployed around GW. Please reference the below picture. In this example, a GW connects around 400 EPD devices.

<figure><img src="../../../../.gitbook/assets/image (368).png" alt=""><figcaption></figcaption></figure>

The following picture is in the real field deployment (Floor plan).

<figure><img src="../../../../.gitbook/assets/image (369).png" alt=""><figcaption></figcaption></figure>

#### **Cas**[**e**](#user-content-fn-1)[^1] **2: Wide Warehouse Application.**

If the warehouse is wide, we have to estimate the number of connection EPD devices and avoid across metal or cement shelters. In the following picture, I will show how to deploy in the wide warehouse.&#x20;

First, we must determine the area that includes the least shadow deployment and calculate how many tags will be in that area.&#x20;

In the following picture, I separate three regions and I will estimate how many GWs will deploy in each area.&#x20;

<figure><img src="../../../../.gitbook/assets/image (370).png" alt=""><figcaption></figcaption></figure>

A WISE-3240 supports 400 EPD devices. If there are less than 400 EPD devices in a field, please deploy WISE-3240 near the center of the field. You can reference the yellow and the orange region. In the green region, there are 700 EPD devices in the field so we have to deploy two WISE-3240. Because of there are many metal shelters, the GW in the field will be slightly away from the metal shield. If you deploy GW between shelves, the wireless signal will have interference. Please reference the below picture.

<figure><img src="../../../../.gitbook/assets/image (371).png" alt=""><figcaption></figcaption></figure>

#### **Case 3. Meeting Room Application**&#x20;

In meeting room applications, since the number of tags is mostly less than 400, only the communication distance of the router needs to be considered. The evaluation method is the maximum number of tags that can be included in the transmission distance. In addition, there will be steel beams indoors, which should be avoided when deploying WISE-3240.

<figure><img src="../../../../.gitbook/assets/image (372).png" alt=""><figcaption></figcaption></figure>

### Step 4. Check the EPD device RSSIs and test transmitting image.

&#x20;If the transition image is successful, we can know the interference is weak. If the transition image fails, we have to change the WISE-3240 deployment position or modify the direction of WISE-3240 antenna.

<figure><img src="../../../../.gitbook/assets/image (373).png" alt=""><figcaption></figcaption></figure>

### Step 5. Check WISE-3240 antenna direction.&#x20;

Position 1. WISE-3240 is on the ceiling.

<figure><img src="../../../../.gitbook/assets/image (374).png" alt=""><figcaption></figcaption></figure>

If the signal RSSI is still not good, please modify the antenna as below.

<figure><img src="../../../../.gitbook/assets/image (375).png" alt=""><figcaption></figcaption></figure>

Position 2. WISE-3240 is on the high platform

<figure><img src="../../../../.gitbook/assets/image (376).png" alt=""><figcaption></figcaption></figure>

If the signal RSSI is still not good, please modify the antenna as below.

<figure><img src="../../../../.gitbook/assets/image (377).png" alt=""><figcaption></figcaption></figure>

## Appendix

**Item Data design**

In the DeviceOn/ePaper, item data has some rules. When you design the item data, the first column has to be unique in every table.&#x20;

Normally, the customer only puts the data that shows on the EPD device. We recommend the customer can add more information to the table. For example, the customer can add the tag mac and location in the table. It will be much easier to find the EPD device location.

<figure><img src="../../../../.gitbook/assets/image (378).png" alt=""><figcaption></figcaption></figure>

[^1]: 
