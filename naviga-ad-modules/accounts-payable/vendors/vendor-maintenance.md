# Vendor Maintenance

## Vendor Maintnance Header

Navigate to the menu Vendor -> Vendor Maintenance.

<figure><img src="../../../.gitbook/assets/image (1388).png" alt=""><figcaption></figcaption></figure>

If you have opened an existing vendor, the header section of vendor maintenance shows high level information about the account, which can be edited if needed. To search for a vendor, click the magnifying glass icon to the right of the vendor ID field, or simply start typing the name into the VendorID field and the system will display a dropdown with matching vendors to select.

If entering a new vendor into the system, click the “New” button.

Minimum information required to save - Vendor ID, Vendor Name, Vendor Type, and Tax Code, so be sure that you have completed the [Vendor Type](../setup/vendor-type-setup.md) and [Tax Code](../setup/system-tables-setup/tax-setup.md) setup prior to creating vendors. Payment terms and Payment status are also required, but will likely be pre-filled based on A/P System Settings.

Enter the first line on the name of the vendor, and then enter the second line on the name of the vendor, if there is a need. This is typically used when you have a vendor with multiple departments, for example, Con Edison as line 1 and the gas department on the second line. You can then have another vendor as Con Edison, but with the electric bill on the second line. Note that this is a line which may be printed on the invoice and check to the vendor if so activated in the setup.

Click the button “Edit Address” to enter the address of the vendor. Fill in the address details on the pop up screen with all the address lines and phone numbers.

<figure><img src="../../../.gitbook/assets/image (1110).png" alt=""><figcaption></figcaption></figure>

You have the option to validate the address, to ensure that it indeed exists. The system will then provide a confirmation of the address, or say that the address is invalid.

<figure><img src="../../../.gitbook/assets/image (1408).png" alt=""><figcaption></figcaption></figure>

Enter the website URL for the vendor if any exists.

**Our Account No. w/ Vendor** is a field which allows you to enter your account number with the vendor. This number will print at the top of the check along with the batch id and bank, so long as the vendor is not MSC type and Fabsoft is used. For user to print the account on the Check or Remittance portion, user must have their Fabsoft form set up to read from that location and place it in the desired location

On the vendor setup screen, enter the sort field as the characters on which you would like the system to sort in reports and screens where a display of vendors’ names is listed. This is beneficial when you have vendors names which start with a determiner, such as the words “the”, “this”, “some”, and so forth, for example, “The New York Times” should have the sort field as “New” in order to sort on the word “New” instead of the word “The”.

Enter the legacy ID for the vendor if one exists. This is in case of users converting from another system or importing vendors where the system will have a legacy ID tied to the new vendor ID assigned by Naviga, to allow a correct importing of information to the correct vendor. Note that you can enter more than one legacy ID if applicable, separated by pressing the enter button on the computer.

## Payment Settings

<figure><img src="../../../.gitbook/assets/image (1072).png" alt=""><figcaption></figcaption></figure>

**Payment Terms:** Scroll to the payment settings section and choose the payment terms from the drop-down list which defines the terms by which to pay the invoices. Terms must be set up in advance of creating vendors and are a shared resource with other parts of the system. Terms for vendors will default in from the A/P System Setup.

**Grade Days:** Choose the grace days if any, which will be added to the payment terms as the total number of days during which the vendor payment has to be processed. For example, if you enter payment terms as net 30 days, and grace days as 5, then the total of the allowed time to pay the vendor is 35 days. The grace days can be any number from zero and higher.

**Tax Code:** Choose the tax code from the drop-down menu. This is the percentage of tax which the vendor collects in addition to the invoice amount.

**Posting Approval Required:** Check the box to be “yes”, if there is a requirement to approve the posting of this invoice to accounts payable. If this is the case, choose the system user which needs to approve the posting. If there is no need to approve postings, mark the “Posting Approval Required” as “No”, and leave the user name blank. Note that if approval is required, user must manually approve every invoice for approval.

**VAT ID:** If applicable, enter the VAT ID, which is value add tax ID. This is typically applicable to users in Canada and Europe.

**Accepts Credit Card Payments:** Mark as Yes if the vendor accepts credit card payments. Later vendor invoices can be marked as Paid by Credit Card. This doesn’t process through the system but is only an indication that the invoice is paid by credit card. User must manually pay the invoice by credit card and enter the payment in the A/P module independent of this flag.

**AP Check Legal Line Language:** Select language from the list of available languages.

**Payment Status:** Enter the payment status for the vendor. This could be “pay”, “hold”, “stop”, or "none". The default value is according to the setup, but you can change this value here. These are three hard coded values in the system to choose from and are setup by Naviga software.

* **Pay:** If this option is chosen, then users, processing the vendor invoices, can create the vendor invoice, generate the payment, and post to the G/L.
* **Hold:** If this option is chosen, then the users processing the vendor invoices will be able to create the invoice, but will not be able to generate payment for the vendor.
* **Stop:** This option is to stop the creating of an invoice for this vendor.
* **None:** This is not an option to allow for saving the vendor. User has to choose a value.

**Payment Priority:** Enter the payment priority. This is free form field in which you can decide what to enter. For example, you can choose to enter “High”, “Medium”, or “Low” for the new vendor. You can instead use a code, for example, “1” for high, or “2” for medium, and so forth. This can then be optionally be utilized when Selecting invoices for which to process payments, so best to decide on a naming convention and stick to it or the priority dropdown in payment processing will get quite long.

**Payment Type:** Choose the payment type to be either a “Separate Payments per Invoice” for generating one check per invoice, or “Consolidate Invoices per Payment” for generating one check for multiple invoices.

**Pay from Bank:** Enter the bank from which these checks will be generated.

**Payee Vendor:** Enter the ID for the payee vendor, or search for one using the magnifying glass. Occasionally, you would want to make the payment for this vendor, to another vendor, for example, a contractor handling multiple vendors.

**Pay by Wire Transfer:** Check the box “Pay by Wire Transfer” as “Yes” if you want to allow wire transfers to be made to the vendor’s bank account. When selecting invoices for payment, the Payment method field is available as a filter so that you can find only wire transfer payments if desired.

**Auto Clearing:** Check the box for “Auto Clearing” as a “yes” if the vendor will be paid by ACH. If this is set to yes, the remaining Auto Clearing fields in this section will become required to save the vendor. Similar to Wire Transfers above, the payment method field when selecting invoices for payment allows the user to search for only ACH transactions.

Enter the account name which is at the bank chosen above. Enter the account number which allows for the electronic payment. Enter the type of account whether it is a checking or savings. Enter a routing number, and a branch name from which the electronic check will be sent out. Each Bank should either provide their specifications in full, which will state exactly what needs to go in that field.

Enter an email of the user to be notified once an electronic payment is made.

## Tax Withholdings

Scroll to the Tax Withholdings section.

**Federal Withholding Tax Code:** Choose the appropriate withholding tax code, which is the amount you withhold from the vendor when paying the invoice. For example, if the withholding tax code is for 25%, when you pay this vendor a $100 invoice, the check generated to the vendor will be for $75, and you then submit $25 to the IRS, when you file your 1099 report.

**Tax Payer ID:** Enter the tax payer ID, which is the vendor’s tax ID or social security number. This information is always needed for later tax purposes, when the user files taxes. (Note: There is group security controlling whether or not a user can see/edit the Tax ID on a vendor once it has been saved.)

Choose the tax form requirement from the drop-down list. This is the form appropriate to the payment which the user and the vendor submit to the IRS. These are US, Canada and Europe clients.

1099 has multiple uses, for example, royalties, legal fees, non-employee compensation. Any payments you make to an individual get reported on a 1099 and may or may not have taxes withheld.

A 1042 is basically the same, but for foreign vendors that do not file US tax Returns. This is designed to comply with revised regulations. The Canadian and Irish forms are similar. Depending on the type of Tax Form selected, the fields below it will change.

**W9/W8 Received:** Check the box as “yes” for the W9/W8 form, if the Form has been received. Use this form to provide your correct TIN to the person who is required to file an information return with the IRS to report, for example, income paid to you, real estate transactions, mortgage interest you paid, acquisition or abandonment of secured property, cancellation of debt, or contributions you made to an IRA.

**Withholding Limit** - Read only field. This will populate from the "Exempt Amount" field on the Tax Setup (Vendor Payment Withholding Information section)

The Read-only **Tax Percent** field will display the % Tax Rate from tax setup of the tax code selected in the "Federal Withholding Tax Code" field

Note that the bottom section of Tax Withholdings section is blank if this is a new vendor. But when this vendor has been paid over time, a listings of all taxes withheld per year will display.

The display will be sorted by year of taxes, taxable payments, taxes withheld, and total payments.

## Contacts

Scroll to the section for contacts

Enter a contact name, title, phone and email address. Click the + sign. Repeat as many times as you need.

## Attachments and Linked Documents

For a linked document, enter a description and url link to a document and click the + sign.

To upload a physical document, use the Attachments section. This can be used to attach the contract with the vendor, or any other document as desired. Enter a description and click the white box or select file to browse for the file on your computer. Click the + to add the document. It will be displayed as a link with the Description entered. If you do not enter a description, the filename will be used instead.

## Vendor Notes

Scroll to the vendor notes and add notes for yourself or other users to view on the vendor overview screen or to view/edit on the vendor maintenance screen.

<figure><img src="../../../.gitbook/assets/image (1390).png" alt=""><figcaption></figcaption></figure>

## Invoice Defaults

<figure><img src="../../../.gitbook/assets/image (1374).png" alt=""><figcaption></figcaption></figure>

Enter a comment in the default invoice comment to be placed on all invoices for this vendor.

Enter the G/L account to which payments to this vendor will be posted. Enter the percentage to which you want to attach the payment to this G/L account, for example, 100%, or 50% and then click the + sign. Add another account as needed to add up to 100%.

These are just defaults to save time in manual entry for repetitive invoices. The defaults can always be modified when actually entering an A/P Invoice.

## User Defined Fields

Scroll to the User Defined Fields and enter values for any of the predefined fields. See Setup -> [Vendor User Defined Fields Setup](../setup/vendor-user-defined-fields-setup.md) for help on setting up User Defined Fields

## Purchase Orders

<figure><img src="../../../.gitbook/assets/image (1383).png" alt=""><figcaption></figcaption></figure>

There is a section for purchase orders which is used primarily by the book module users. When you send the vendor a purchase order, and get the invoice for the services or goods, you enter the invoice using the PO lines rather than the G/L lines. This also relates with Production / Job Cost Module. They also need to do a PO Receipt against the PO as part of the process.

Enter the contact name as the default for the purchase orders, and his email address if the box “Email P.O.s” is checked as “yes”.

When finished, click the “save” button, in order to store the vendor information. You may now use this vendor to generate invoices and payments.
