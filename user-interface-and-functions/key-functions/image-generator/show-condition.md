# Show Condition

{% hint style="info" %}
In some application scenarios, ePaper displays often change based on certain values. For example, in a meeting room booking system, users might want the meeting room panel to display a full-screen red color when the room is booked, indicating it is in use. Conversely, when the room is not booked, it should display a full-screen white color, allowing users to observe the room's availability from a distance.

Another example is that some device screens might display a full-screen red or yellow color to alert users to an abnormal condition, prompting them to take immediate action to resolve the issue. These applications can effectively use the "Show Condition" feature to achieve the desired display effects.
{% endhint %}

**Step 1. Create a data source.** Navigate to the **Item Data** page, create a data source named MeetingRoom, and then upload an item data containing a column “status” that has two kinds of conditions, which are BOOKED and FREE, as shown below.&#x20;

> Note: This text or number can vary according to the application settings.

<figure><img src="../../../.gitbook/assets/image (341).png" alt=""><figcaption></figcaption></figure>

**Step 2. Design a template.** Go to the **Template** page, and design a template that contains two backgrounds – red and white, which have \[Show Condition] as \[status == BOOKED] and \[status != BOOKED], respectively.

As you can see, we have two backgrounds - red and white. Click the red background first.

<figure><img src="../../../.gitbook/assets/image (342).png" alt=""><figcaption></figcaption></figure>

Under the \[Show Condition] panel, choose the \[Option] radio button and then click the button below.

<figure><img src="../../../.gitbook/assets/image (343).png" alt=""><figcaption></figcaption></figure>

In this dialog, you can select the item and set condition rules. For example, you can set status == BOOKED, means that if status = BOOKED, this component will be displayed accordingly.

<figure><img src="../../../.gitbook/assets/image (344).png" alt=""><figcaption></figcaption></figure>

**Step 3. Preview the image.** By changing the item data (or bind different item data), and you can observe the display differences (e.g., from "BOOKED" to "FREE").

<figure><img src="../../../.gitbook/assets/image (345).png" alt=""><figcaption></figcaption></figure>
