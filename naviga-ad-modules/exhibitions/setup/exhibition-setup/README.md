# Exhibition Setup

This is where you can create a new exhibition and setup all the parameters for the exhibition in preparation for entering orders against it.

## Exhibition Groups <a href="#_toc9435414" id="_toc9435414"></a>

{% hint style="info" %}
Only use Exhibition Groups if you are not using the Advertising Module. If you use both Ad and Exhibition Modules, Exhibitions will be linked to Product Groups in Advertising rather than Exhibition Groups so that you can have a combined Ad/Ex Campaign.
{% endhint %}

Once Exhibition Groups have been set up, you can link each exhibition to a “primary” group via the Group prompt in Exhibition Maintenance. If you linked the same exhibition to more than one group above, this allows selecting one of those as the “main” or “primary” group.

Navigate to the menu Setup -> Exhibition Setup. Click the Exhibition Groups node.

![](<../../../../.gitbook/assets/0 (45).png>)

Click the New button to create a group to add the exhibitions to this group. Enter the exhibition group ID, name and move any exhibitions using the right arrow to the box labeled “Exhibitions in This Group”. Click the save button.

## Exhibition Detail <a href="#_toc9435415" id="_toc9435415"></a>

Click the Exhibition Detail node.

![](<../../../../.gitbook/assets/1 (74).png>)

Click the “New” button and enter an exhibition ID to identify the exhibition, a name for the exhibition, and a description.

Enter the start and end dates of the exhibition, a build and break date of the details of the exhibition.

Enter the address of the exhibition.

<figure><img src="../../../../.gitbook/assets/image (868).png" alt=""><figcaption></figcaption></figure>

Enter an affiliate publisher and commission for this publisher. Please refer the [Affiliate Setup](../../../advertising/setup/affiliates.md) for more information in using this section.

<figure><img src="../../../../.gitbook/assets/image (939).png" alt=""><figcaption></figcaption></figure>

Enter the general settings for the exhibition, such as the company, where the company will validate against Company Security to ensure that the user has security to use this company. Enter the financial period where revenues for this exhibition will be marked, tax code, primary group of the exhibition, a unit of measure being meters, yards or Feet, and enter the number of available units in the exhibition.

<figure><img src="../../../../.gitbook/assets/image (1159).png" alt=""><figcaption></figcaption></figure>

Enter last year’s exhibition if applicable, the organizer’s name and any text you have in the contract for exhibitors who will participate in the exhibition, any comments or notes for internal use, the sort code of where the exhibition will display in the list, and any related conference to this one from the drop down module.

### G/L Account Allocations

When finished, click the tab GL Account Allocations, where the general ledger codes will be used when posting exhibition orders.

![](<../../../../.gitbook/assets/3 (9).png>)

Type the first numbers or description of the GL account for the specified field and a list displays to choose from, and then the description will default accordingly.

Accounts Receivable: For standard billing, this account will be debited for the entire invoice amount. For cancelled orders, this will be credited for the refund amount specified at the time the order was cancelled (the refund amount may include an insurance refund).

Deferred Income: For standard billing, this account will be credited for the entire invoice amount, less the amount posted to Price Adjustments and Insurance Code accounts (if those accounts are different). For cancelled orders, this will be debited for the entire amount posted to this account for this order.

Price Adjustments: For standard billing, this account will be credited for the amount of price adjustments (discounts or extra charges added to the standard rate on the order). For cancelled orders, this will be debited for the entire amount posted to this account for this order.

Non-Refundable Deposits: For cancelled orders, this account will be credited for the amount billed for this order, less the refund amount.

External Charges: For standard billing, this account will be credited for the external charges on the order (comes from the selected ratecard). For cancelled orders, this will be debited for the entire amount posted to this account for this order. If not using external charges, enter the dummy g/l code.

Sponsorships: This account will be used for the exhibition sponsorships.

The click the save button.

### Groups

This will only be relevant if using Exhibition Groups rather than Product Groups.

<figure><img src="../../../../.gitbook/assets/image (1090).png" alt=""><figcaption></figcaption></figure>

## Order Entry Settings <a href="#_toc9435416" id="_toc9435416"></a>

Click the node Order Entry Settings.

These are the default settings and security settings for the order entry screen of orders against exhibitions.

![](<../../../../.gitbook/assets/4 (10).png>)

For example, the option to display halls and areas, prompt user to enter whether the deposit was received or not, whether to require the number of points of space sold, whether to use the exhibitor tax code. If this is set to no, then the order will use the exhibition values. Click “Yes” if you want to require some sides are open, and “Yes” to allow overbooking of spaces on orders’ status “Quotes” or not display the space which is already booked.

Enter the email address for the recipient you want to receive the email when there is a new order entered for this exhibition. This is optional.

Enter “Yes” if you want to require a contact to be entered on forms in the order entry screen. For the “Other Required Contacts”, select the contacts in the not required box and click the right arrow to move this contact to the required contact box. This is only if you require other contacts to be entered on the order. If you do not require contacts then skip this step.

![](<../../../../.gitbook/assets/5 (63).png>)

In the “Allowed Catalog Categories”, move the categories to the “Allowed” box by highlighting the category and clicking the right arrow. These values come from the values entered in the menu Setup -> Directory Category Setup menu.

In the UDFs, choose the UDF you want to add to the order and click the + sign. Repeat and click on the save button. UDF's are set up in the [Exhibition Code Tables](../exhibition-code-tables.md#\_toc9435404)

## Areas/Halls <a href="#_toc9435417" id="_toc9435417"></a>

Click the node “Areas/ Halls”.

![](<../../../../.gitbook/assets/6 (40).png>)

In the section “Enter a New Hall”, enter an ID, description, available number of units, target revenue and budget amounts and click the + sign. This will add the areas and halls to the exhibition to make them available for order entry.

## Sections <a href="#_toc9435418" id="_toc9435418"></a>

Click the node “Sections”.

![](<../../../../.gitbook/assets/7 (44).png>)

As in the Halls node, enter the section’s ID, description and click the + sign to add the different sections for this exhibition.

Halls and Sections are two ways to identify where the booth is located. Depending on the size of an exhibition, you can use either or both of these options, or none. For example, an exhibition may consist of several buildings, where each building is divided into groups of related booths. In this case, halls can be used to identify each building, and sections can be used to identify each group of related booths where each hall contains one or more sections.

The reverse of the previous example may occur. More than one building may contain a section (a group of related booths). This time each section contains one or more halls.

Another example, is if an exhibition may all be in one building, but two different ways to split up the building layout are needed. In this case, halls will identify one layout, and section for another, but both will be for the same space. Halls can be pre-assigned to booths; sections cannot.

Also, Halls can be set as mandatory during order entry; sections cannot.

## Billing Parameters <a href="#_toc9435419" id="_toc9435419"></a>

Click the node “Billing Parameters”.

<figure><img src="../../../../.gitbook/assets/image (1259).png" alt=""><figcaption></figcaption></figure>

#### General Invoice Settings

Enter an invoice prefix which you want to affix to the invoices for the exhibition.

#### Fabsoft Form Settings

This section will only be relevant if you use Fabsoft for Invoice forms in the system. Fabsoft is an older 3rd party tool for creating invoice forms. Most clients today use Naviga Forms, which are the HTML-based form templates in the system. Using Naviga forms gives you the most flexibity over the look and feel of your invoices.

#### Naviga Forms Settings

Select the new invoice form and new credit form from the drop down list. For information on creating invoice forms, please refer to [Exhibition Invoice Forms](../exhibition-invoice-forms.md). Select the [override new form logo](../../../advertising/setup/system-tables-setup-ad/#invoice-form-logos).

Enter the email address in the “Send Invoices from Email Address” field, which is the email address you want the clients to view as the sender of the invoice for the exhibition.

#### Other Settings

<figure><img src="../../../../.gitbook/assets/image (288).png" alt=""><figcaption></figcaption></figure>

If desired, select the Default currency for the show

In the field “Days before Invoice Date to Generate Billing”, enter the number of days before the billing date that you want to be able to generate invoices. This limits how many days before the scheduled billing date you can generate invoices. If left blank you will only be allowed to bill on or after each scheduled billing date. You can override this value in the order billing parameters. Also, the billing days can be changed in the billing screen to allow for earlier billing.

“Allow Adjustment to Invoiced Orders” field if checked to have a value of “Yes” allows user to make adjustments to orders which have been invoiced.

“Credit Full Amount by Default” - when checked as “Yes”, then the system will create a credit of the order amount when an invoiced order is cancelled.

“Use EU Tax Rule”, if checked as “Yes” will apply the EU tax rule for the European clients.

“Remit to Address” is the remit address to use on the invoice.

## Billing Schedule <a href="#_toc9435420" id="_toc9435420"></a>

This screen may be used as an option to set one or more fixed schedules for an exhibition which will apply to all exhibitors for an exhibition.

<figure><img src="../../../../.gitbook/assets/image (921).png" alt=""><figcaption></figcaption></figure>

Click “Create New Schedule” button and enter the date of the billing. You can enter multiple dates for billing stages.

<figure><img src="../../../../.gitbook/assets/image (1417).png" alt=""><figcaption></figcaption></figure>

Enter the value of billing, whether it is an amount, percentage or percentage of remaining balance. This is determined in the field “Type”. Enter any billing comments and click the + sign to add the schedule. Click on the “Save” button when finished.

This billing schedule can also be changed in the order entry screen for the exhibition.

## Budgets/ Forecasts <a href="#_toc9435421" id="_toc9435421"></a>

This is the screen which you can enter with budgets and forecasts of the exhibition.

Target/Services Target/Sponsorship Target is where to enter the target revenue amounts.

Budget/Services Budget/Sponsorship Budget is where to enter the expected revenue amounts.

Signed Contract/Sponsorship Revenue Budget is where you enter the signed contract revenue and sponsorship budgets for this exhibition. Signed Contract/Sponsorship Revenue Forecast is where to enter the signed contract revenue and sponsorship forecasts for this exhibition. Signed Contract Space Budget/Forecast is where to enter the signed contract space budget and forecasts for this exhibition in Units of Measure for this conference.

<figure><img src="../../../../.gitbook/assets/image (1068).png" alt=""><figcaption></figcaption></figure>

Enter the sales rep from the drop down and enter the corresponding budget for this sales rep. You can enter more than one rep

<figure><img src="../../../../.gitbook/assets/image (1663).png" alt=""><figcaption></figcaption></figure>

## Blueprint Integration <a href="#_toc495314844" id="_toc495314844"></a>

Formerly called Showplan, Naviga Ad integrates floorplan designs of trade shows with third party software Blueprint, which uses AutoCAD. The integration facilitates the design and orders’ sales for users. When user has a Blueprint design, it can be integrated with Naviga Ad so that the sales rep/order entry user can view the floorplan from within Naviga ad and see what space is remaining to be sold. Once a booth is reserved, the API passes the booking or cancellation over to Blueprint so that it reflected in the floorplan. See [Setting up Blueprint Integration](setting-up-blueprint-integration.md) for detailed Instructions

## Utilities

### Copy an Exhibition <a href="#_toc9435424" id="_toc9435424"></a>

This option is useful when you have an annual or periodic exhibition which takes place regularly and you can just copy it from one time to another.

![](<../../../../.gitbook/assets/14 (13).png>)

Enter the exhibition to copy from, from the drop down menu. Enter the new Exhibition ID and name, as well as date range and financial period for the new exhibition.

Click “Yes” to copy any of the options available such as the sections, area/halls, spaces, and other parameters. You can also copy the billing schedule and just add number of days to each of the schedule dates to accommodate the date change.

### Copy a Floorplan <a href="#_toc9435425" id="_toc9435425"></a>

This option allows you to copy the floor plan from one exhibition to a new exhibition.

![](<../../../../.gitbook/assets/15 (3).png>)

Choose the exhibition to copy from in the drop down menu and choose the new one to copy to. Click on the save button. If the new exhibition already has a floorplan, the system will not allow for copying over the floor plan and will alert you to that fact.
