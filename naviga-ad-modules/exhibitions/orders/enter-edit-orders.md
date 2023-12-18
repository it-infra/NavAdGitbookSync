# Enter / Edit Orders

Under the Orders menu select either Enter New order or View/Edit an order. Both options take you to the same screen but the Enter a new order will assume that you want to create a new order and so the search will be disabled. Selecting the View Edit an Order will allow you to click the magnifying glass to search for an existing order (or enter the ID in the Order ID field) or click the + button if you don't find what you are looking for and need to create a new order.

## Search for an existing order

Enter some search criteria based on the information available such as the who the exhibitor is, the exhibition, date range, etc.

<figure><img src="../../../.gitbook/assets/image (1185).png" alt=""><figcaption></figcaption></figure>

Click the search button to find exhibition orders matching the given criteria.

Click on the order id in the results to open the order. Make any desired edits to the order and save the changes. See Enter a new order below for a full description of the order entry screens.

## Enter a new order

By navigating to Orders -> Enter a new order, or clicking the + when in view/edit mode you can begin the process to create a new order

<figure><img src="../../../.gitbook/assets/image (230).png" alt=""><figcaption></figcaption></figure>

### Exhibitor Information

Enter a short description in the appropriate fields. This may be displayed on invoices and on order reports, so it is good to be descriptive here.

Select a recent account from the Exhibitor dropdown or search for an exhibitor using the magnifying glass button. Click the + on this row to create a new exhibitor if your user permissions allow you to do so.

Select the division for the order if this advertiser has multiple divisions. Click the + to create a new division if your user permissions allow you to do so.

Billing information will be populated based on the account setup, but it can be overwritten here if needed.

The Order amounts in the top right will be calculated based on information soon to be provided on the Line Items

{% hint style="info" %}
Note: Currency cannot be changed after there are line items on the order. If you need to change the currency once lines are added, you will need to cancel and re-book.
{% endhint %}

Select the Order Status from the available statuses in the dropdown.

If this is related to a marketing campaign, start typing in the Marketing Campaign ID or description and the list will populate with available currently running Marketing campaigns.

Enter a PO Number and Tax ID Override if applicable

Sales rep information will be populated from Division Setup, but can be overwritten here if your user has permission to do so. Rep information is required to save the order header.

Click Save to continue

### Line Items

On the line items screen you can create or edit Space Reservations and/or Service Orders.

In either Section click the appropriate button to add a new line.

<figure><img src="../../../.gitbook/assets/image (309).png" alt=""><figcaption></figcaption></figure>

#### Space Reservations

When creating a space order, the first thing you will want to do is enter the space ID

<figure><img src="../../../.gitbook/assets/image (1575).png" alt=""><figcaption></figcaption></figure>

There are a couple of different ways this can be done and it will be contingent upon how the show has been setup:

*   If there is no floorplan in the system, the + will be activated and a new space can be created.\
    \
    When creating a new booth in order entry the Booth number can be autoassigned (sequential number) or you can type in a unique ID. Select the shape and enter the dimensions. If there is a space adjustment needed (for a pillar or some other object) enter the adjustment item and the size and click create booth.

    <figure><img src="../../../.gitbook/assets/image (1051).png" alt=""><figcaption></figcaption></figure>
* If there is a floorplan in the system, the following options apply:
  1. Floorplan can be previewed with the ![](<../../../.gitbook/assets/image (987).png>) icon and desired booth can be selected from the image (select an available space)\
     ![](<../../../.gitbook/assets/image (1242).png>)
  2. The Space ID can be entered in the Space ID field\
     ![](<../../../.gitbook/assets/image (1249).png>)
  3. The space ID can be searched on with the magnifying glass and selected from a list. Enter information in the top row filter to narrow the list down based on Size, Hall, Shape, etc\
     ![](<../../../.gitbook/assets/image (225).png>)

Once the Space ID has been selected, the Section (if applicable) can be selected

The Order Type, Industry Codes, and Exhibitor Type will be defaulted in, but can be overwritted if necessary

Select the ratecard from the dropdown, following by Rate type and price if there are multiple options (see [ratecard setup](../setup/ratecards-services-adjustments.md#ratecard-setup))

Enter any applicable Price adjustments and click save, unless you have a need to enter more details on the other tabs.

<figure><img src="../../../.gitbook/assets/image (698).png" alt=""><figcaption></figcaption></figure>

#### User Defined Fields

User defined fields can be created in Setup -> [Exhibition Code Tables](../setup/exhibition-code-tables.md)

If any UDFs are marked as being required, you will not be able to save the order until the required UDFs are completed.

#### Directory Information

At most shows a directory of some sort will be published. The information entered here will be what is used for the directory. Default information will be set in here based on the client's setup, but it can be overwritten if needed. For example, what YOU call the client in your setup may differ from how they want to be displayed in the directory.

<figure><img src="../../../.gitbook/assets/image (229).png" alt=""><figcaption></figcaption></figure>

#### Shared Space

If this space is to be shared with another exhibitor, that information can be entered here.

<figure><img src="../../../.gitbook/assets/image (490).png" alt=""><figcaption></figcaption></figure>

Click on Add an Exhibitor in the top right and a screen pops up to add exhibitor information for the shared space, including that exhibitor's preferred directory information

<figure><img src="../../../.gitbook/assets/image (445).png" alt=""><figcaption></figcaption></figure>

#### Service Orders & Other Adjustments

Click the button "Add/Edit Services"

Select deom the list of available service orders. Can add additional lines here if needed.

<figure><img src="../../../.gitbook/assets/image (662).png" alt=""><figcaption></figcaption></figure>

The available items on this list and the rules on whether or not the user can override the price will depend upon the setup in [Services Setup](../setup/ratecards-services-adjustments.md#\_toc9435432)

#### Renew order

If you have opened the order from last year's show, you can click the botton in the bottom left to renew the order for the current year's show.

<figure><img src="../../../.gitbook/assets/image (1189).png" alt=""><figcaption></figcaption></figure>

Select the new show and the new ratecard from the prompt and click Validate Renewal (or cancel to cancel renewal)

If there are any errors, the user will be presented with information about why the order cannot be renewed.

![](<../../../.gitbook/assets/image (1571).png>)

If everything checks out ok and the order can be renewed, the user will be presented with some options on what to copy and what status and billing schedule to use, then click renew order:

![](<../../../.gitbook/assets/image (1041).png>)

### Contacts

On this node you can setup the various contacts related to this order. The contacts may or may not be employees of the company that is ordering the booth and receiving the invoice.

<figure><img src="../../../.gitbook/assets/image (388).png" alt=""><figcaption></figcaption></figure>

Select the contact role(s)

Select the company and the contact person for the role. You can create a new contact from this screen if one doesn't already exist.

Click the yes/no to issue badge for this person, because again, you might be contacting them for something related to the show, but they may or may not actually be attending the show.

When you save this information onto the order you will be prompted to answer if this contact is to be used just for this order, for the order and the future default for orders in this exhibition, or for this order and the default for future orders on this Exhibition Group (product group)

<figure><img src="../../../.gitbook/assets/image (968).png" alt=""><figcaption></figcaption></figure>

### Billing Schedule

If this order is part of a Flexible Ad Campaign, this node will not be displayed on the Exhibition order since the billing will be done from advertising. If this order is a standalone exhibition order or if it is part of a Performance Campaign, then the billing for it, and therefore the schedule, will be done in the Exhibition Module.

<figure><img src="../../../.gitbook/assets/image (444).png" alt=""><figcaption></figcaption></figure>

The schedule will default in here from the Exhibition Setup. Whether or not a user can delete or change these lines will be dependent upon their Group Security

### Forms

The necessary forms for a show will default into here based on [setup](../exhibitions/forms-tracking.md). here you can select your forms contact and (if security allows) mark the date sent and received.

<figure><img src="../../../.gitbook/assets/image (365).png" alt=""><figcaption></figcaption></figure>

### Notes/Comments

Confirmation comments will be displayed on order confirmations if the confirmation form includes the appropriate tag

Invoice comments will be displayed on invoices if the invoice form includes the appropriate tag

Internal comments are just for internal use and wouldn't be included on any externally facing documents

See [Forms and Templates](../setup/forms-and-templates.md) for information on setting up Exhibition forms

<figure><img src="../../../.gitbook/assets/image (814).png" alt=""><figcaption></figcaption></figure>

### Order Confirmations

Click on Send Order Confirmation button from the ORder Confirmation node and you will get a pop up to select to whom the confirmation should be send. The HTML template is selected at the top of the screen and the default confirmation contact (if there is one) will be preselected. This can be overwritten as needed.

<figure><img src="../../../.gitbook/assets/image (409).png" alt=""><figcaption></figcaption></figure>

Select options at the bottom of the screen to download or send the confirmation to the client.

### Attachments

Files can be manually attached to the order if applicable.

### Invoices and Prepayments

If this order was created as part of a Flexible Billing Campaign, this node will not be displayed as it will be controlled in Advertising module. If the order is a standalone Exhibition order or is part of a Performance campaign, then the order can be prepaid here.

<figure><img src="../../../.gitbook/assets/image (1078).png" alt=""><figcaption></figcaption></figure>

To enter a prepayment, select the prepayment type, bank, and payment details. Click the + to add the prepayment to the order.

### G/L Summary

If this order was created as part of an Advertising Module Flexible Billing Campaign, this node will not be displayed as it will be controlled in Advertising module. If the order was standalone in Exhibitions or part of a Performance Ad Campaign, the GL Summary for the Exhibition portion of the order will be displayed in here.

<figure><img src="../../../.gitbook/assets/image (689).png" alt=""><figcaption></figcaption></figure>

### History of Changes

The history of changes will store changes to the Exhibition order and line items

<figure><img src="../../../.gitbook/assets/image (1132).png" alt=""><figcaption></figcaption></figure>

## Deleting/Cancelling an order

When in an order's space reservation line, you will see two options at the bottom - Delete this Reservation and Cancel this Reservation. There is a slight difference between them. Also, if the order has already been billed, the Delete option will go away and only the Cancel will remain.

<figure><img src="../../../.gitbook/assets/image (511).png" alt=""><figcaption></figcaption></figure>

### Delete and order

Delete this reservation will delete it and when you look at the order, you won't see anything in the line items (unless you add a new reservation in its place.

Here is an example order where the Reservation order and Service Orders were deleted.

<figure><img src="../../../.gitbook/assets/image (1541).png" alt=""><figcaption></figcaption></figure>

On the history of changes node and also on the Deleted Space Reservations report, you will be able to see that there once was a reservation on this order.

### Cancel an order

When you choose to cancel an order, there will be a line added to the Space Reservation and the Services Order line (if applicable) that a space reservation was there and it was cancelled.

When a user cancels and order, there will be a prompt and a chance to charge a cancellation fee as well.

<figure><img src="../../../.gitbook/assets/image (888).png" alt=""><figcaption></figcaption></figure>

User can select a reason code for the cancellation, and add a cancellation fee as well.

at the bottom there is a linked service orders section as well, so if there are any services that should also be cancelled along with the space cancellation, that can be done by checking the checkbox on that line.

Once the reservation is cancelled, the order will look like this:

<figure><img src="../../../.gitbook/assets/image (831).png" alt=""><figcaption></figcaption></figure>
