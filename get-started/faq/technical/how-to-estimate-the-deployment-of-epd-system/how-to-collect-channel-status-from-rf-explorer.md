# How to collect channel status from RF Explorer?

## RF Explorer

1. You can buy the RF Explorer in the following URL:

[https://shop.nutsaboutnets.com/collections/rf-explorer-handheld-spectrum-analyzers/products/rf-explorer-handheld-spectrum-analyzer-worldwide-distributors?variant=32166366871692](https://shop.nutsaboutnets.com/collections/rf-explorer-handheld-spectrum-analyzers/products/rf-explorer-handheld-spectrum-analyzer-worldwide-distributors?variant=32166366871692)

2. Install RF Explorer utility for Windows PC Client

Download URL:

[http://j3.rf-explorer.com/download/sw/win/RFExplorerWindowsSetup\_v2\_02\_2009\_5.zip](http://j3.rf-explorer.com/download/sw/win/RFExplorerWindowsSetup\_v2\_02\_2009\_5.zip)

3. Power on RF Explorer

<figure><img src="../../../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

4. Connect RF Explorer and Laptop through USB cable

<figure><img src="../../../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

5. Execute (No OpenGL) RF Explorer utility

<figure><img src="../../../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

6. Modify the field separator of CSV to ”Comma(,)”

<figure><img src="../../../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

7. Pre-Configure the Center Frequency to 2442.5 and the field of SPAN to 85

<figure><img src="../../../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

8. After collecting a period of time (20\~30 minutes), export the CSV data and save it

<figure><img src="../../../../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

## Discovery Better Channel

1. Mouse double-click the “Channel\_Select.xlsx” file
2. Erase whole content in RAW\_Data session
3. Import channel data to RAW\_Data sheet

Data->Text file

<figure><img src="../../../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

Select your collecting channel data and import file by “RF Explore For Windows”

<figure><img src="../../../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

Choose delimiter option

<figure><img src="../../../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

Check “Comma” symbol only and click “Next” button

<figure><img src="../../../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

Check the data format to “Text” and finish

<figure><img src="../../../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

Note: the data must start at the initial upper left of field

4. Switch to “Result” session
   1.  Check the result of the data format is PASS or FAIL.

       (If the result is FAIL, please confirm whether previous instructions are correct or not)
   2. Check if the result of Configuration is PASS or FAIL. (If the result is FAIL, please confirm the parameters of RF Explorer is correct or not)
   3. Confirm the Data Start Time is as same as the start time of RF Explorer
   4. Adjust the threshold level if needed
   5. Based on rank values to select a suitable channel in your operating environment (the lowest value is our suggested channel which means idle time is long at your site)

<figure><img src="../../../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

Appendix:

In the below picture, there are five parameters that we need to explain.

![](<../../../../.gitbook/assets/image (57).png>)\


**Channel:** Zigbee channel in 2.4G and each channel is mapping to different frequencies.

<figure><img src="../../../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

**Start Step、End Step:** Start and end frequency mapping table and the mapping table is as below:

&#x20;![](<../../../../.gitbook/assets/image (59).png>)

**Below -70 dBm:** Proportion of signal strength less than -70 dBm in one minute

**Rank:** The result of the analysis tool processing, green refers to the channel recommended subordinate.
