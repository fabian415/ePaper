# Dynamic Images & Dithering

{% hint style="info" %}
In retail applications, it is often necessary to update images dynamically by changing advertisements. This requires using the "Dynamic Image" feature, which allows you to dynamically replace the images you want to update by uploading them to the **Gallery**. Additionally, due to the nature of ePaper displays, which present images using a limited color palette, there may be a limitation in the display of full-color advertisements. To address this, techniques such as "Dithering Treatment" and "Brightness Enhancement" are used to represent subtle colors through pixel processing, enhancing the visual quality of the images.
{% endhint %}

## Dynamic Images

**Step 1. Navigate to the Item Data Page**: Access the **Item Data** page in your DeviceOn/ePaper platform.

**Step 2. Create a Data Source**: Click on the option to create a new data source.

**Step 3. Create data**: Open a text editor, and create data like below.

{% file src="../../../.gitbook/assets/ChipOrder.csv" %}

**Step 4. Upload Item Data**: Upload your item data file. Ensure this file contains a column named “**file**” with data entries that are strings of _file names_. These file names should match exactly with the names of images stored in the **Gallery**. This will link the item data with the corresponding images for display.

<figure><img src="../../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

**Step 5. Navigate to the Gallery Page**: Access the **Gallery** page in your DeviceOn/ePaper platform.

**Step 6. Select the Data Source**: Choose the data source you created in the previous step.

<figure><img src="../../../.gitbook/assets/image (348).png" alt=""><figcaption></figcaption></figure>

**Step 7. Upload Images**: Upload the images to the FTP storage. Ensure that the file names of these images match the file names specified in the "file" column of your item data. This allows the images to be displayed or changed dynamically based on the item data.

<figure><img src="../../../.gitbook/assets/image (349).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (350).png" alt=""><figcaption></figcaption></figure>

Sometimes, an image might exceed the 2MB size limit. When this happens, the system will automatically prompt you, asking whether you want to compress and convert the image. If you select "OK," the system will resize and convert the image format. It is recommended to select "OK" because the system will perform lossless scaling based on the largest ePaper size, ensuring that the image remains distortion-free on the ePaper display.

<figure><img src="../../../.gitbook/assets/image (351).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (352).png" alt=""><figcaption></figcaption></figure>

Upload Images successfully.

<figure><img src="../../../.gitbook/assets/image (353).png" alt=""><figcaption></figcaption></figure>

**Step 8. Navigate to the Template Page**: Access the **Template** page in your DeviceOn/ePaper platform.

**Step 9. Select the Template**: Choose the template you created in the previous steps.

**Step 10. Add an Image Component**: Drag and drop an **image** component into the template layout.

<figure><img src="../../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

**Step 11. Set Image Value**: Set the value of the image component to “file,” which corresponds to the "file" column in your item data containing the image file names.

**Step 12. Enable Dithering Mode**: Since it is a colorful image, enable the dithering mode if available. This will often result in better display quality on the ePaper device.

**Step 13. Save the Template**: Save the template with the changes.

<figure><img src="../../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

**Step 14. Navigate to the EPD Controller Page**: Access the **EPD controller** page in your DeviceOn/ePaper platform.

**Step 15. Change Binding Data**: Select the binding data that corresponds to your item group and template.

**Step 16 (Optional). Edit the File Name in Data**: Modify the file name entries in your item data to link to different images, if needed.

**Step 17. Preview Changes**: Use the preview function to see how the changes in the file names or data affect the display on the ePaper device.

By following these steps, your ePaper device will be able to dynamically display the images based on the item data, ensuring high-quality visuals even for colorful images.

<figure><img src="../../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

## Dithering

**Step 1. Navigate to the Template Page**: Access the **Template** page in your DeviceOn/ePaper platform.

**Step 2. Select an Image Component**: Drag and drop an **image** component into the template layout. Select it by left-clicking on the mouse. Enable both the **Brightness Enhancement** and **Dithering Treatment** options.

<figure><img src="../../../.gitbook/assets/image (450).png" alt=""><figcaption></figcaption></figure>

* **Brightness Enhancement:** Adjust image colors according to E-ink recommendation.&#x20;
* **Dithering Treatment:** Apply the [Floyd–Steinberg dithering](https://en.wikipedia.org/wiki/Floyd%E2%80%93Steinberg\_dithering) method to process the image.

Step 3. **Save this template and preview.** You will see the output differences between dithering and no-dithering.

* Dithering + Brightness enhancement:

<figure><img src="../../../.gitbook/assets/image (451).png" alt=""><figcaption></figcaption></figure>

* Dithering:

<figure><img src="../../../.gitbook/assets/image (452).png" alt=""><figcaption></figcaption></figure>

* No Treatment:

<figure><img src="../../../.gitbook/assets/image (453).png" alt=""><figcaption></figcaption></figure>
