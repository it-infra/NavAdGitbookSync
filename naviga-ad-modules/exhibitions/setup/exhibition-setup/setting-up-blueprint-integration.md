# Setting up Blueprint Integration

1.  Under Exhibitions module, select Setup > Blueprint Integration Setup\\

    <figure><img src="../../../../.gitbook/assets/1 (31).png" alt=""><figcaption></figcaption></figure>
2. Open your show under Setup > Exhibition Setup
3. Select Blueprint Integration from the left Navigation tree

![](<../../../../.gitbook/assets/2 (83).png>)

4. The fields on the right will be filled in with data retrieved from the show setup in Blueprint.
5. Select the “use Blueprint” yes/no toggle and ensure it says “YES”
6. In your browser navigate to [https://blueprint.freeman.com/app/](https://blueprint.freeman.com/app/)
7.  Inside the Blueprint application the left panel looks like this:

    <figure><img src="../../../../.gitbook/assets/3 (8).png" alt=""><figcaption></figcaption></figure>
8. Select “show” at the top of the menu
9.  With nothing in the Custom URL field, the URL below it will contain the Plan ID. Copy only what is at the end of the URL…

    <figure><img src="../../../../.gitbook/assets/4 (44).png" alt=""><figcaption></figcaption></figure>
10. Paste the above code from YOUR show (not the example show above) and paste into Naviga Ad in the “Plan ID from Blueprint” field
11. Select “API and Webhooks” from the Blueprint navigation
    * Enter in a client ID and select “Add New API Client”
    *   Select “Add New API client”

        <figure><img src="../../../../.gitbook/assets/5 (47).png" alt=""><figcaption></figcaption></figure>
    * The system will create a “secret”
    * Copy and paste both the Client ID and the Secret into Naviga Ad’s API Client ID and API secret fields.
    * In the Webhooks section select the options in the screenshot to the right:
    * In the URL section copy the URL from Naviga Ad in “Webhooks Endpoint” and paste into the above URL
    * Click Add
12. The final field to copy and paste in is the Floorplan iFrame URL. This will be retrieved in one of two places, depending on in you want to see the 2D floorplan or the 3D floorplan.
    *   Retrieve the 2D floorplan URL from the “show” menu. Scroll to the bottom of the screen and select select desired options in the coloring/properties/layers area and then select just the URL from the iframe Embed Code (just what is inside the quotes below):

        <figure><img src="../../../../.gitbook/assets/6 (30).png" alt=""><figcaption></figcaption></figure>
    *   Retrieve the 3D floorplan from the “Connect” menu option. The URL will be a hyperlink at the top of the page:

        <figure><img src="../../../../.gitbook/assets/7 (47).png" alt=""><figcaption></figcaption></figure>
13. At the bottom of the Navgia Ad Setup screen select which Status ID in Naviga should be sent to Blueprint, and whether that Naviga Ad Status translates to Reserved, Booked, or Available in Blueprint. (Blueprint only has these three statuses)

![](<../../../../.gitbook/assets/8 (23).png>)

14. Click Save

## View 3D Floorplan in Order Entry

The setup above in the Floorplan iFrame URL will display the Blueprint floorplan in order entry when the “view floorplan in Blueprint” option is selected:

![](<../../../../.gitbook/assets/9 (2).png>)

![](<../../../../.gitbook/assets/10 (30).png>)

This is currently NOT selectable to book a booth. To make that happen, Blueprint needs to make a modification on their side to pass us the selected Booth ID.

## Import 2D Selectable Floor Plan

If you want to click on a booth in the Floorplan to book orders, you can still do so, but you will need to import the Blueprint floorplan into Naviga in the Floorplan setup. Steps to do that are below. This will be a 2D rendering of the floorplan.

1. Navigate to Floorplan setup from Setup > Space Setup > Exhibition Space Setup
2.  Select your show in the top right

    <figure><img src="../../../../.gitbook/assets/11 (2).png" alt=""><figcaption></figcaption></figure>
3. Click “Import from Blueprint”

{% hint style="info" %}
Note: you will only see this option on shows that have Blueprint Integration enabled
{% endhint %}

4. You will see a popup with Sellable space and Non-Sellable Space

![](<../../../../.gitbook/assets/12 (15).png>)

5. The options you see above may be different, depending on your Blueprint show configuration and the spaces that are setup for that show. Select or De-select based on what spaces you wish to import into Naviga Ad. And click Import Selected Items at the bottom left.
6. Once they are imported in, you can review in Naviga and be sure to scroll down and save the floorplan.

## Booking an Order and sending to Blueprint.

When booking an order for Exhibitions there are a couple ways to select a booth

1. Enter ID into the Space ID field
2. Click the search to find from a list of Booths
3. Select from the Naviga Floorplan (circled in red below)

![](<../../../../.gitbook/assets/13 (11).png>)

If you select the “View Floorplan in Blueprint” option (highlighted in yellow above), you will see the blueprint floorplan, but it isn’t selectable, so you will see the Booth ID there, but will need to type it into the Space ID field.

(See [Enter / Edit Orders](../../orders/enter-edit-orders.md) for more details on booking the order)

## Blueprint Sync Queue

After you save the order, IF the order is in a status that indicates that it should send to Blueprint, then Naviga Ad will place it in the Blueprint queue (on your menu navigate to Orders > Blueprint Queue):

![](<../../../../.gitbook/assets/14 (8).png>)

Your windows service, running on our servers will sync this to Blueprint automatically on the interval set up in the service. If the windows service happens to not be running, you can force the sync by adding _?a=1_ to the end of the URL. This will add a “Process Pending Records” button at the top right and clicking on it will force the order over to Blueprint.

_Note to Naviga Implementors:_

_Be sure you set this setting in Admin > Windows Service Setup –_

![](<../../../../.gitbook/assets/15 (11).png>)

_Choose desired service interval. This will determine how often the Window service will push order and changes over to Blueprint_

## Blueprint Webhooks Log

Probably more of a technical log view than a screen that would be interesting to end users, but this will log the data transfer between the systems.

Enter a desired date range at the top and click Get Data.

If it has processed you will see the checkbox marked in the processed column. If it hasn't been, you will see the exception reason in the next column. The actual JSON file can be seen in th link to View Data.

<figure><img src="../../../../.gitbook/assets/image (624).png" alt=""><figcaption></figcaption></figure>
