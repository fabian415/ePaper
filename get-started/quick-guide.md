# ⚓ Quick Guide

This Quick Guide provides a 12-steps to help users quickly install and start using DeviceOn/ePaper.

## Installation and Setup

Step 1. Prepare an Ubuntu 20.04 machine

Step 2. Download and Install the DeviceOn/ePaper Software. You can access the DeviceOn/ePaper download page below, and download the latest version of the software.

{% content-ref url="../" %}
[..](../)
{% endcontent-ref %}

## Initial Configuration

Step 3. Open the DeviceOn/ePaper website and log in using your credentials.

Step 4. Activate DeviceOn/ePaper product with license key or license file. Please follow the instructions below.

{% content-ref url="installation-and-deployment/product-activation.md" %}
[product-activation.md](installation-and-deployment/product-activation.md)
{% endcontent-ref %}

## EPD Routers and zigbee-based EPD Onboard

Step 5. Configure your network settings to ensure connectivity between the server and EPD routers.

Step 6. Connect EPD routers and set up their whitelists to allow for EPD device connection. Please follow the instructions below.

{% content-ref url="../user-interface-and-functions/web-user-interface/device-onboarding/epd-devices/zigbee-based.md" %}
[zigbee-based.md](../user-interface-and-functions/web-user-interface/device-onboarding/epd-devices/zigbee-based.md)
{% endcontent-ref %}

## WiFi-based EPD Onboard

Step 5. Configure your network settings to ensure connectivity between the server and WiFi APs.

Step 6. Use Android or iOS mobile to connect WiFi-based EPDs. Please follow the instructions below.

{% content-ref url="../user-interface-and-functions/web-user-interface/device-onboarding/epd-devices/wifi-based.md" %}
[wifi-based.md](../user-interface-and-functions/web-user-interface/device-onboarding/epd-devices/wifi-based.md)
{% endcontent-ref %}

## Import Application Data

Step 7. Gather all necessary business data that will be displayed on the ePaper devices. This might include item numbers, stock levels, and other pertinent details. Ensure the data is in a structured format, such as a CSV file, for easy import.

Step 8. Navigate to the Data Import Section, create a data source, select the prepared CSV file, and upload it to the platform.

{% content-ref url="../user-interface-and-functions/web-user-interface/data-management/import-data.md" %}
[import-data.md](../user-interface-and-functions/web-user-interface/data-management/import-data.md)
{% endcontent-ref %}

## Design Template

Step 9. Access the template page, and choose the imported data as the data source for the template. Drag and drop elements such as text, images, and data fields onto the template. Ensure that the design is aligned with your business requirements.

Step 10. Once the design is complete, save the template for future use.

{% content-ref url="../user-interface-and-functions/web-user-interface/template-designer/" %}
[template-designer](../user-interface-and-functions/web-user-interface/template-designer/)
{% endcontent-ref %}

## Bind Devices & Test

Step 11. Bind Data and Template to EPD Devices. Navigate to the EPD Controller page, and choose the specific ePaper devices you want to bind the data and template. Please follow the instructions below.

{% content-ref url="../user-interface-and-functions/web-user-interface/epd-controller/bind-data.md" %}
[bind-data.md](../user-interface-and-functions/web-user-interface/epd-controller/bind-data.md)
{% endcontent-ref %}

Step 12. Issue Image Update Commands. Go to the control panel on the EPD Controller page, and issue the **Transmit** command to the selected devices. This will trigger the devices to fetch the latest data and update the display accordingly.

{% content-ref url="../user-interface-and-functions/web-user-interface/epd-controller/transmit-image.md" %}
[transmit-image.md](../user-interface-and-functions/web-user-interface/epd-controller/transmit-image.md)
{% endcontent-ref %}
