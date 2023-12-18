# Finding Invoices / Invoice Details

## A/P Invoice Search

Find a simple search screen for finding invoices by Invoice number, Date, Vendor, Amount, Reference or PO Number by navigating to **Invoices -> A/P Invoice Search**

<figure><img src="../../../../.gitbook/assets/image (1751).png" alt=""><figcaption></figcaption></figure>

Enter information available and click search

<figure><img src="../../../../.gitbook/assets/image (1753).png" alt=""><figcaption></figcaption></figure>

Click the desired Invoice ID to open Invoice detail screen.

## Invoice Details Screen

This screen displays the details of the invoice in several collapsible and movable shutters. Click the ![](<../../../../.gitbook/assets/image (14) (1).png>) in the top right corner of any section below the header to collapse it. Click on the blue part of the section to drag and drop to another area of the screen to display the details in your own desired order.

<figure><img src="../../../../.gitbook/assets/image (13) (1).png" alt=""><figcaption></figcaption></figure>

### Edit Options

<figure><img src="../../../../.gitbook/assets/image (15) (1).png" alt=""><figcaption></figcaption></figure>

The options enabled will vary. For example, If the invoice has already been paid via check or ACH in the "Generate Checks" option then you will no longer have the option to Mark it as being paid by Credit Card and you will no longer be able to Reverse the invoice (unless you go into **Payments -> Pay A/P Invoices** and select "Void a Check" first).

Similarly, you will not be allowed to change Tax Form Information if the vendor was not subject to taxes or if your user [group security](../../setup/admin/group-security-a-p.md#general-security-settings) doesn't allow for "Changes to 1099 Amount in Invoice Inquiry."

Assuming the option is enabled, this is what each option will do:

*   **Add/Remove Attachments:** This will open a popup window where you can select a file to upload and enter a description for the attachment. This can be used to add a copy of an invoice perhaps. That can also be done during Invoice Entry, but if it isn't available at the time, it can be attached later here.

    <figure><img src="../../../../.gitbook/assets/image (16) (1).png" alt=""><figcaption></figcaption></figure>
*   **Change Tax Form Information:** If Applicable, this will open a popup allowing for change to the Tax form type and amount\\

    <figure><img src="../../../../.gitbook/assets/image (17) (1).png" alt=""><figcaption></figcaption></figure>
*   **Change Invoice Details:** What can be changed in here will depend upon whether or not the invoice has already been paid. Unpaid invoices are fully editable in this window. If it has already been paid, only the Invoice Description and Reference can be modified: \\

    <figure><img src="../../../../.gitbook/assets/image (18) (1).png" alt=""><figcaption></figcaption></figure>
* **Go to Vendor Setup:** This will open the current vendor in the [**Vendor Maintenance**](../../vendors/vendor-maintenance.md) screen
* **Go to Vendor Overview:** This will open the current vendor in the [**Vendor Overview**](../../vendors/vendor-overview.md) screen
* **Mark as Paid by credit card:** This will open a popup where you can mark an invoice as being paid via credit card. See "[**Mark Invoices as Paid by credit card**](mark-a-p-invoices-as-paid-by-credit-card.md)" for more details on this workflow\
  ![](<../../../../.gitbook/assets/image (19) (1).png>)
* **Reverse this Invoice:** This will open a window where you can select the date and period for the reversal\
  ![](<../../../../.gitbook/assets/image (20) (1).png>)
* **Assign Job to Lines**: This will open a dialog window allowing user to apply certain lines on this invoice to a Production Job and Class Code\
  ![](<../../../../.gitbook/assets/image (21) (1).png>)

### Header / Financial Summary

The header includes Vendor Name (ID), the invoice description and reference, Invoice ID, Invoice Date, Entry Date, Batch, Financial Period and G/L Posting Date. It will say unposted if it hasn't yet been posted to the G/L module. The financial summary will show the amount, tax and balance due. If it was paid in Foreign currency, that information will be displayed to the right of the system currency.

<figure><img src="../../../../.gitbook/assets/image (22) (1).png" alt=""><figcaption></figcaption></figure>

### Payment / Other Detail

The following details are available in the Payment/Other Detail section. If the Balance in the Financial Summary is not zero, and the invoice has been scheduled to be paid, the scheduled date and amount will be displayed in here. If the Invoice was paid with credit card, the card name/description will be displayed here. If there is Tax withheld, that will also be displayed in here. Payment status will either be Pay, Hold, or Stop

<figure><img src="../../../../.gitbook/assets/image (23) (1).png" alt=""><figcaption></figcaption></figure>

### Attachments

If there are any attachments available for the Invoice, they will be displayed here

### Payment Details

Will be blank if the invoice hasn't been paid yet, if it has been paid, the check number will be displayed. If the function was used to mark as paid by credit card, the check number field will display the invoice number dot CC - example 4324578.CC.

<figure><img src="../../../../.gitbook/assets/image (24) (1).png" alt=""><figcaption></figcaption></figure>

Click on the check number link to drill down to details on the payment

<figure><img src="../../../../.gitbook/assets/image (25) (1).png" alt=""><figcaption></figcaption></figure>

### G/L Details

G/L details section will display the breakdown of charges (credits and debits) to each G/L for the invoice

<figure><img src="../../../../.gitbook/assets/image (26) (1).png" alt=""><figcaption></figcaption></figure>

Click the Vendor ID to open the Vendor Overview screen. See [**Vendor Overview**](../../vendors/vendor-overview.md) for more information on Vendors.

## List of A/P Invoices

The List of Invoices provides a very similar concept to the above A/P Invoice Search but some different search options

### List of Invoices

The List of Invoices allows for searching for invoices by a period or date range. Option to group by G/L account is available

<figure><img src="../../../../.gitbook/assets/image (27) (1).png" alt=""><figcaption></figcaption></figure>

### List of Open Invoices

Same search criteria as the above list of Invoices, but this one will only return invoices which have yet to be paid:

<figure><img src="../../../../.gitbook/assets/image (28) (1).png" alt=""><figcaption></figcaption></figure>

### List of Invoices by Currency

In addition to the options above, this allows the user to filter on a foreign currency to only display that currency.

<figure><img src="../../../../.gitbook/assets/image (29) (1).png" alt=""><figcaption></figcaption></figure>

### List of Invoices Paid by Credit Card

If an invoice has been flagged as being paid with a credit card, this report will allow user to filter on only those invoices. User can search on Period or Date Ranges. There is also a filter to show ALL transactions, only the reconciled or only the unreconciled invoices. See[ **Mark A/P Invoices as Paid by Credit Card**](mark-a-p-invoices-as-paid-by-credit-card.md) for full workflow on this topic

<figure><img src="../../../../.gitbook/assets/image (30) (1).png" alt=""><figcaption></figcaption></figure>

### Custom List of Invoices

<figure><img src="../../../../.gitbook/assets/image (31) (1).png" alt=""><figcaption></figcaption></figure>
