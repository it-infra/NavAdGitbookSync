# Order/Show Reports

## Performance Comparison Report

Performance Comparison Report will compare shows with their previous year show.

Select a date range from when the shows will start. (for example, select the current year's shows). Choose to filter by Exhibition Group (optional) and choose to include reserved and quoted orders as well (Confirmed Orders will show by default)

<figure><img src="../../../.gitbook/assets/image (1562).png" alt=""><figcaption></figcaption></figure>

In the charts, current year shows in blue and comparison show shows in gray. (Comparison show is set on Exhibition Setup)

User can see the current show in the first section, broken down by Space & Services.

Comparison Show is in the next section, also broken down by Space and Services

Finally, the Difference between the Current and Comparison shows in terms of both Amount and %.

## Orders by Show

The orders by show report will display all the orders for a given show. This includes Spaces, Services and what has been billed and paid so far. There are options in the top right to see the amounts in the local currency (system currency) or in the actual billing currency if you are billing in foreign currencies. This report can also be downloaded to Excel for further calculations if desired.

<figure><img src="../../../.gitbook/assets/image (1043).png" alt=""><figcaption></figcaption></figure>

## Space Reservations by Show

Select desired show from the top right. A list of space reservation orders will be displayed.

<figure><img src="../../../.gitbook/assets/image (917).png" alt=""><figcaption></figcaption></figure>

To group this report, drag and drop a column heading into the light blue bar at the top of the order list. Perhaps you would like to see this list grouped by Hall or Section, or perhaps by the exhibitor's Industry code.

Options at the top right allow for viewing revenue by the billing currency or by the system (local) currency. You can also choose to show or hide shared space.

This list can be downloded to excel or pdf using the icons at the top right of the data.

## Service Orders by Show

Select desired show from the top right and a list of Service orders will be displayed

<figure><img src="../../../.gitbook/assets/image (315).png" alt=""><figcaption></figcaption></figure>

To group this report, drag and drop a column heading into the light blue bar at the top of the order list. Perhaps you would like to see this list grouped by Hall or perhaps by the Service Product itself.

Options at the top right allow for viewing revenue by the billing currency or by the system (local) currency.

This list can be downloded to excel or pdf using the icons at the top right of the data.

## Insurance Report

The insurance report will display a list of orders for the selected show, and will display if there was an insurance charge or not. (see [Services Charge](../setup/ratecards-services-adjustments.md#\_toc9435432) setup. The insurance charge must be flagged as such to display on this report). On the exhibitor maintenance screen for the customer, we also will store infomation on the account if we have received proof of insurance and the expiration date of that insurance.

<figure><img src="../../../.gitbook/assets/image (1554).png" alt=""><figcaption></figcaption></figure>

There is a nightly process that can be setup to run by your Naviga Implementation Specialist or Support where the Insurance charge will be removed if proof of insurance has been received.

## Directory Report / Export

The directory report provides directory information which was gathered in order entry and exports it to excel so that it can be used in creation of the show directory.

<figure><img src="../../../.gitbook/assets/image (726).png" alt=""><figcaption></figcaption></figure>

Select the show in the dropdown at the top right. Select or deselect the button to Include Shared Space Exhibitors depending upon whether or not those exhibitors are included int the directory.

## Fascia / Board Report

Very similar report to the Directory above, but this displays the information for the Fascia Board

<figure><img src="../../../.gitbook/assets/image (842).png" alt=""><figcaption></figcaption></figure>

Select the show in the dropdown at the top right. Select or deselect the button to Include Shared Space Exhibitors depending upon whether or not those exhibitors would have a separate Fascia Board.

## Conflicting Space Reservations

This report is used to warn if there are any conflicts in a show. In group security, there is a setting on whether or not a user is allowed to overbook a space reservation on quotes. If you allow for quoting 2 advertisers for the same space, you will be able to use this report to find and re-quote a different space when one of the exhibitors eventually confirms that space.

<figure><img src="../../../.gitbook/assets/image (843).png" alt=""><figcaption></figcaption></figure>

Run the report for the desired show (top right corner dropdown) and any conflicts will display, along with the conflict reason. Anything that has been oversold will need more immediate attention. Expand the > on the left side of the report and see that this same space has a quote outstanding and also a confirmed line. The user can click on the order id of the quote order and select a different space to quote that customer.

<figure><img src="../../../.gitbook/assets/image (907).png" alt=""><figcaption></figcaption></figure>

The other error of being overbooked simply means that there are two quotes out there for the same space. Eventually you might have an issue when one of the orders get confirmed, but for now it's just a heads up.

## Badge Report

The badge report for any given show will display who is also attending the show among the exhibitors contact people on an order so that you know who needs exhibitor badges. This provides a list which can be downloaded to excel so that you can make and print your badges externally to the naviga ad system. See Order Entry -> [Contacts](../orders/enter-edit-orders.md#contacts) for more info about contacts.

<figure><img src="../../../.gitbook/assets/image (1179).png" alt=""><figcaption></figcaption></figure>

## Renewal Report

See [Renew Orders](../orders/renew-orders.md#renewal-orders-report) for info on this report.

## Exhibition Production Report

The exhibition production report is a comprehensive view of the order details in an exhibition order

<figure><img src="../../../.gitbook/assets/ExhibitionProduction Report.gif" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note: the last several columns in my example report above is showing premium carpeting, Wired Internet, Sponsorship, etc. These are my Service Charges for this show, so your columns there may look different.
{% endhint %}

## Cancelled Space Reservations

For information on deleting and cancelling orders, see [Enter / Edit Orders](../orders/enter-edit-orders.md#deleting-cancelling-an-order)

<figure><img src="../../../.gitbook/assets/image (299).png" alt=""><figcaption></figcaption></figure>

The Cancelled Space report will display all orders which were cancelled for the selected show. (select show from the top right corner)

Click the ID to open the order containing the cancelled space reservation

## Deleted Space Reservations

For information on deleting and cancelling orders, see [Enter / Edit Orders](../orders/enter-edit-orders.md#deleting-cancelling-an-order)

<figure><img src="../../../.gitbook/assets/image (571).png" alt=""><figcaption></figcaption></figure>

Similar to above, the deleted Space report will display all orders which were deleted for the selected show. (select show from the top right corner)

Click the ID to open the order containing the deleted space reservation

## Cancelled and Deleted Space Reservations

For information on deleting and cancelling orders, see [Enter / Edit Orders](../orders/enter-edit-orders.md#deleting-cancelling-an-order)

<figure><img src="../../../.gitbook/assets/image (1565).png" alt=""><figcaption></figcaption></figure>

This report combines the previous two reports and shows all deleted and cancelled lines together. You can tell which is which from the Cancel Type column. Only cancelled lines contain the option to include a cancellation fee, and only the cancelled lines will include the cancel reason code.
