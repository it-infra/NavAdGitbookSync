# A/P System Setup

The A/P System Setup screen sets defaults and other settings for the A/P module.

<figure><img src="../../../../.gitbook/assets/image (940).png" alt=""><figcaption></figcaption></figure>

## General Settings

**Default Company:** If desired, set a default company for use in the A/P Module. This will be used as the default setting for items such as creating a new invoice batch and entering a manual check.

**Approval Required on Purchase Orders:** Select Yes to Require approval step on any purchase orders created.

## Vendor Defaults

In the Payment Settings Section of a vendor's vendor maintenance screen are several settings. What is set here will affect those settings

<figure><img src="../../../../.gitbook/assets/image (1358).png" alt=""><figcaption></figcaption></figure>

**Default Terms:** See screenshot above - what is selected here will pre-fill the Payment Terms option. Can manually select something different.

**Default new vendors to hold or pay:** see screenshot above - what is seleted here will pre-fill the Payment Status option on a new vendor setup. Can manually select something different.

**Manual payments invoice selection:**

## **Other Vendor Settings**

**Vendor Audit Field Dictionaries:** This field relates to the Vendors -> Vendor Change History report. In your setup you can choose which fields to track in the Change history log. Common options include:

<table data-header-hidden><thead><tr><th width="182"></th><th width="165"></th><th width="166"></th><th width="168"></th></tr></thead><tbody><tr><td>VENDOR.NAME</td><td>ADDR1</td><td>ADDR2</td><td>ADDR3</td></tr><tr><td>CITY</td><td>STATE</td><td>ZIP</td><td>1099.CODE</td></tr></tbody></table>

There are many additional options available besides what is listed above. Start typing in this field and additional items will populate. It is case sensitive though, so be sure to use CAPS. For example:

<figure><img src="../../../../.gitbook/assets/image (1246).png" alt=""><figcaption></figcaption></figure>

## Check Defaults

**Print Second Name Line on Checks:** Vendor maintenance includes 2 lines for a vendor's name. Set this option to Yes if you would like to display the 2nd line on printed checks

**Generate Overflow Remittance at End of Each Check Run:** This option is activated when checked as Yes to print the remittance information which exceeds the available space on the check stub.

## Invoice Entry

The following settings affect the display of these boxes in A/P Invoice Entry:

<figure><img src="../../../../.gitbook/assets/image (1337).png" alt=""><figcaption></figcaption></figure>

**Disable Billable Job Line Entry:** Set to yes to show the Billable Job Costs section in the above screenshot

**Disable Inventory Job Line Entry:** (not shown) set to yes to show the section for Inventory Jobs. Inventory Jobs are only relevant to the Naviga Book system.

**Disable Purchase Order Line Entry:** Set to yes to show the P.O. Line Items section in the above screenshot

<figure><img src="../../../../.gitbook/assets/image (1497).png" alt=""><figcaption></figcaption></figure>

## Payment Approvals

**Approval Process Active:** Select yes to turn on approval process for payments

**Person who has to approve payments:** This person will be required to approve the payments. Email address defaults from user setup, but it can be modified here.

**Person who will be notified when approvals have been made:** This person will be notified one the person above approves the payments. Email address defaults from user setup, but it can be modified here.

**Minimum approval amount:** enter an amount in this field.

## Automated Clearing Payments

**Send Remittance Advice Emails From Address:** enter an email address here. This will be used as the from address on remittance advice emails.

**Auto Clearing Vendor Mandatory Fields:** similar to the Audit Field setting above, enter partial data here and then select from the dropdown of available fields. If the Auto Clearing Flag is set to yes on Vendor maintenance, then any fields listed here will be required. Likely fields you will want to set are as follows:\
![](<../../../../.gitbook/assets/image (579).png>)

## Email Notifications

**If G/L cash is entered, email:** Enter an email address here. This email address will receive notification if GL Cash is entered in A/P.

## Purchase Order Forms Using Fabsoft

Fabsoft has been depricated. If not already using it, leave this section blank. If you are already using it, you will be notified and scheduled to be migrated to Naviga Forms

## Purchase Order Forms Using Naviga Forms

<figure><img src="../../../../.gitbook/assets/image (540).png" alt=""><figcaption></figcaption></figure>

**Use Naviga P.O. Forms** - set this to yes if you intend to use purchase order functionality

**Override Email from Address:** By default Purchase Orders are emailed from the user who generates the PO. This setting allows you to set a different from address.

**Default PO Form:** Select a form from the drop down. Forms are setup in advance under Purchase Orders -> Purchase Order Templates. This sets the default form for the system. It can be overwritted in A/P Company Setup if forms differ by system company

**Email P.O. Subject Line:** Enter a subject line for the emailed purchase order.

**Email P.O. Body:** Enter body text in plain text or in HTML

## Tax Forms

<figure><img src="../../../../.gitbook/assets/image (1538).png" alt=""><figcaption></figcaption></figure>

Select appropriate form for each 1099 type and 1042. 1099 Forms are setup in advance under Setup -> 1099 Copy B Form Templates. 1042 Forms are currently still using Fabsoft. See Naviga Support for assistance with a 1042 form.

These forms will need to be revisited annually to ensure the correct information is displayed for the tax year being processed. Sample forms can be retreived from Naviga Support.

## Credit Cards: Used for Paying A/P Invoices

<figure><img src="../../../../.gitbook/assets/image (956).png" alt=""><figcaption></figcaption></figure>

Enter desired payment methods for use when paying vendors with a credit card. Don't enter actual credit card numbers here - just a description and perhaps the last 4-digits for reference. See [**Mark A/P Invoices as Paid by Credit Card**](../../invoices/finding-invoices-invoice-details/mark-a-p-invoices-as-paid-by-credit-card.md) for more details on using this function.
