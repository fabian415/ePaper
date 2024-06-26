# Wake Up & Status Report Period

{% hint style="info" %}
Adjusting the EPD's Wake Up Period can expedite the response time to image transmission commands. However, this comes at the cost of increased power consumption. In other words, the shorter the Wake Up Period, the faster the battery drains.

Similarly, adjusting the EPD's State Report Period affects the frequency of status updates. A longer State Report Period means that information such as RSSI and battery levels is reported less frequently, which conserves battery life. Conversely, a shorter State Report Period provides more frequent updates but increases power consumption.
{% endhint %}

## Key Considerations

**Wake Up Period**

* **Shorter Period**: Faster response to commands, higher power consumption.
* **Longer Period**: Slower response to commands, lower power consumption.

**State Report Period**

* **Shorter Period**: More frequent status updates, higher power consumption.
* **Longer Period**: Less frequent status updates, lower power consumption.

By carefully balancing these settings, you can optimize the performance and battery life of your EPD devices according to your specific application requirements.

## Single Device Setting

Step 1. Navigate to the **EPD Controller** page, choose a target EPD device, and then click the **Period** icon.

<figure><img src="../../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

Step 2. Fill in the **Wake-Up Period** and **State Report Period** values, and then click **OK**.&#x20;

<figure><img src="../../../.gitbook/assets/image (391).png" alt=""><figcaption></figcaption></figure>

## Schedule Setting

If you want to set up the **Wake-up Period** and **State Report Period** for a group of devices, we recommend to proceed the group schedule setting. It allows you to set up these two parameters at specific times.

{% hint style="info" %}
By using the group schedule task, you can set specific working intervals, such as from 8 AM to 6 PM. For example, you can configure the Wake-up Period and State Report Period to be shorter at 7 AM, and then set them to be longer at 6 PM. This configuration allows the ePaper devices to be both power-efficient and highly effective.
{% endhint %}

**Step 1. Access Group Schedule.** Navigate to the **Group Control** settings on the **EPD Controller** page.

<figure><img src="../../../.gitbook/assets/image (392).png" alt=""><figcaption></figcaption></figure>

**Step 2. Add Schedule Task.** Click the **Schedule** button to go to the Schedule setting page. Click **+** button to add a new schedule.

<figure><img src="../../../.gitbook/assets/image (394).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (396).png" alt=""><figcaption></figcaption></figure>

**Step 3. Set Wake-Up Period.** Click the **Schedule** button to go to the Schedule setting page. Click **+** button to add a new schedule.

<figure><img src="../../../.gitbook/assets/image (398).png" alt=""><figcaption></figcaption></figure>

**Parameters**

* **Schedule Name:** Assign a schedule name (cannot be duplicated)
* **Enable:** Enable or disable this schedule
* **Device Task:**&#x20;
  * Transmit
  * Refresh
  * Wake Up
  * State Report
* **Timezone:** Select your timezone area
* **Period:** Once, Hourly, Daily, Weekly, Monthly, Yearly
* **Set Time:** Schedule execution time
* **Select EPD Model:** Choose an EPD model you want to apply this schedule task
*   **Period:** Period time



**Step 4. Schedule Plans.** Here we set up schedule plans according to the following table.&#x20;

Note: You can only set up one action within ONE minute of a specific time, so please shift the time to the next minute.

| Schedule Name   | Time  | Action                       |
| --------------- | ----- | ---------------------------- |
| wakeUp7hr       | 07:00 | Wake Up Period -> 2 s        |
| stateReport7hr  | 07:01 | State Report Period -> 1 min |
| wakeUp18hr      | 18:00 | Wake Up Period -> 20 s       |
| stateReport18hr | 18:01 | State Report Period -> 5 min |

<figure><img src="../../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

