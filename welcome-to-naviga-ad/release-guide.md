---
description: >-
  This document provides instructions for how to use the new features in the
  2023.6 release, grouped by module. Remember to install & test in your test
  system before Production.
---

# 🎯 Release Guide

<figure><img src="../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

**These are the most important takeaways / impactful changes that you **_**need**_** to pay attention to:**

* There is a new workflow option for Inserts / Preprints.  The older workflow will still be supported, to ease the transition, but we think many of you will want to take advantage of this new workflow. [**See below for details**](release-guide.md#new-workflow-option-for-inserts-preprints)
* There are a couple new Group Security Changes in both [**Advertising** ](release-guide.md#group-security-change)and [**CRM** ](release-guide.md#group-security-change-1)modules

## Advertising Module

### New workflow option for Inserts/Preprints

In 2023.6 there is a new option for setting up, pricing, and managing preprints, which allows for varying page types with page counts, weights and spoilage.  It isn't required that you implement this workflow - if you do not set up the following you will still be able to use preprints the old way, though we do think this way will be appealing to many of you.

#### Prerequisite Setup

#### Size Codes

**Setup -> Advertising Setup -> Size Setup.**  Size Codes are not a new concept for this release, but there is a new field on the size code setup. For any sizes that are to be used in the new Inserts workflow, the flag "For Preprints" should be set to yes.  In addition, only dimension types of Inches, Millimeters, Centimeters, or Points should be used on these, since the digital dimensions wouldn't be relevant.&#x20;

<figure><img src="../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure>

#### Page Types

Navigate to Setup -> Advertising Setup -> Page Types.  Setup one or more page types as needed for the types of inserts/preprints that you offer.  Page types will set defaults for weight and spoilage %. You may also have certain metadata questions that need to be answered and possibly passed on to the printer to allow them to print the insert properly.

<figure><img src="../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

1. Click New to create a new Page Type
2. Enter a desired ID and Description for the Page Type
3. Optionally, select a default size code.  This can also be manually added / changed on an order
4. External ID - Optional - This doesn't have a function inside of Naviga Ad, but may be included on a feed to the printer.
5. Is Inactive - set this flag to yes if you no longer wish to use a Page Type

**Page Options** - Add as many lines as needed for the given page type.  Enter the page count for each line.  These will be the valid page counts allowed when booking an order.  For each number of pages, set the default weight and default spoilage percent.  These two can be overwritten in order entry if a given insert differs from the default.  Each line can also have an override External ID, or this can be left blank it is shares the same External ID as the Page Type itself.  This is optional and only used in external feeds.

**Custom Fields** - much like the metadata in classified order entry and custom forms setup elsewhere in the system, the custom fields tab on Page Type setup allows the system admin to set up certain questions that the order entry user can (or must) answer before saving the order.

<figure><img src="../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>

* Enter a Label / Question &#x20;
* Select the prompt type from the dropdown
* If appropriate for the prompt type, enter validation information (used with single line text, multi-line text, and dropdown list)
* If available, based on the prompt type, select formatting from the dropdown (used on dates, date ranges, number and number ranges)
* check the required flag if the user is required to answer the question before saving the order.&#x20;

#### Ad Type (Preprint Types)

Navigate to **Setup -> Advertising Setup -> Ad Types**. Like Size Codes, Ad Types are not new, but there are some new settings related to the new Inserts workflow.

<figure><img src="../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

Click Ad New at the top of the Ad Type screen, or select an existing Ad Type to edit with the pencil icon.  Each ad type for the new workflow should include the following:

* Ad Type ID
* Ad Type Description
* G/L Type
* Line Type (not actually relevant to these, since the rate type will be defined elsewhere. Cost per Thousand is the default new line type - can leave it at that if desired)
* Is for Preprints flag - set this to Yes.  This is important as it is the trigger to open the new preprint workflow screen rather than Full Line entry.
* Linked Products - Select the products which allow this Ad Type. Only required if you restrict certain ad types to certain products.  Can also select ad types during product setup if desired.
* Page Types (Preprints/Inserts) tab - _**Optional**_ - can set allowed Page Types for this Ad Type. If none are selected, all page types will be available in order entry for this Ad Type.

#### Insert Rating Schedules

**Navigate to Setup -> Advertising -> Insert Rating Schedules**

The new inserts workflow does not use the standard rate cards that other kinds of ads use.  This uses a rule-based engine that determines which price to use based on how closely it matches one of these definitions.

Click New to create a new schedule and give it an ID and a Description.  There is an inactive flag as well in case you wish to no longer use it at some point in the future.

#### In the Basic Settings section:

<figure><img src="../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>

* select the Price Type to be used.  Options include Quantity based CPM, Quantity Based, or Flat Rate. &#x20;
* Optional - Enter a Start Date and Valid through date to limit when this rate can be used.
* Priority Code - The appropriate schedule is chosen by the system based on the number of matching qualifiers.  For example, there might be multiple schedules that could potentially be used in order entry.  One schedule might match on just one qualifier, and another one might match several qualifiers. In the event that two rate schedules match on the same number of qualifiers, the priority code will determine which schedule to use.

#### Qualifiers

<figure><img src="../.gitbook/assets/image (145).png" alt=""><figcaption></figcaption></figure>

There are currently 7 attributes or qualifiers that can be checked to determine which rate schedule to use.

1. Specific Advertiser - Select a specific advertiser if the advertiser has negotiated a custom price
2. Page Types - Select one or more relevant page types for this rating schedule
3. Product Group - If applicable select a product group that this rating schedule is valid for
4. Product(s) - Select one or more allowed products for this rating schedule
5. Client Type - Select a client type that is allowed to use this rate schedule
6. Ad Type(s) - Select one or more ad types that can use this rate schedule (Note these ad types are filtered to only ad types flagged with the "Is for Preprints" flag
7. Matching Days of the week - Select one or more days of the week which can use this rating schedule.

#### Price Escalations&#x20;

<figure><img src="../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>

For each Rate Schedule, you can have one or more sets of prices that can be used, based on the number of pages (which also links to weight based on Page Type Setup) and number if inserts.  These prices can be flat prices, per insert prices, or per thousand prices based on the Price Type selected in the Basic Settings section. &#x20;

* Select Add New Escalation or click the pencil icon to edit an existing one
* Alternatively, Click copy escalations from another schedule to save some time and copy and edit from a similar schedule.

<figure><img src="../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>

#### End User Experience

An end user booking an order with this new workflow will begin on the Line Items tab and select a Product and an AdType, as they normally would for a full line entry order.  The Ad Type, if it is one that is flagged in setup as being for Preprints, will trigger the new workflow rather than traditional full line entry

<figure><img src="../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

The Insert / Preprint Booking workflow window will open and several tabs can be seen across the top, similar to the Booking Wizard for Classified:

<figure><img src="../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>

#### Product Selection

Product and Ad Type are filled in based on what was selected in the prior screen, though it can be changed here if desired.

Page Type must be filled in as it is what drives page counts, weights, spoilage, metadata questions and possible the rates on later screens.

Sections and positions are optional, and section could potentially drive rate selection later if setup as such.

First / Primary Issue Date is when the printing and billing will be done, and all pricing will be based on that date.

Additional (perpetual) Issue dates are not going be relevant for all inserts.  If it is a flyer for instance where the insert itself changes each week, those would only have a single issue date.  If a campaign for flyers needed multiple dates, there can be multiple lines on a campaign, each with their own issue date. You can also copy the original line and modify the date.  The Perpetual Issue dates are used when the printing of the insert is all done up front for the first drop, but then extra copies are saved for future drop dates when the insert will be delivered.  The important thing to understand here is that all the printing and billing happens on the first date.

#### Zone Selection

From there the user clicks "next" to select Zones.

<figure><img src="../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure>

Several different methods are available for selecting Zones

* User Selects Zones from Grid
* User imports the desired Zones.
* User Selects Zones from Map

#### Selecting Zones from the Grid

This will be familiar if you are already booking inserts using Zones in the other workflow.  There is a breadcrumb trail at the top to jump up to higher levels once the user begins drilling down.  This is a view from the highest level grouping (Philadelphia Metro in my system)

<figure><img src="../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>

Based on the blue squares, user can see that some HD routes were selected (HD=Home Delivery in my system, these names are configurable in Zone Dimension Setup), some SC routes were selected, and All of the Retail Outlets were selected in the Zone Group "Outer Suburbs"  In the Philly City Group, nothing was selected for this order.

Drilling down into Outer Suburbs additional Zones and/or Zone Groups can be seen

<figure><img src="../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>

Once all selections are made, the user can click apply to save and close the window, or for additional selections in higher groups, user can select desired group in the breadcrumb trail at the top.

After clicking apply, the user returns to the Zone Selection tab and can see the selected Zones, and their counts for each date selected on the Product Selection tab.

#### Importing Zones

Using the same grid view from above, instead of selecting zones from the boxes as shown from example 1, the user can also import the selections.  Select "Import Selections" button at the bottom of the screen

<figure><img src="../.gitbook/assets/image (119).png" alt=""><figcaption></figcaption></figure>

User can copy and paste from excel, text file, or just manually type in Zone ID's.  These can be a list, like shown in the screenshot above, or it could be comma separated.  I would use the select, to select only certain zone ID's, and select one or more dimensions to select.  To use the deselect, I might select an entire Zone group in the previous screen, but then list just a handful of exceptions in this list to exclude only a few from the overall group.

Click Apply to save the selections and only the selected Zones will be displayed

<figure><img src="../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>

Click apply again to return to the Zone Selection tab

#### Use Map to select Zones

The final option is to select zones from a map with a radius of available zones from the customer's address.  On the Zone tab, the user selects the button "Use Map to Select Zones" and a google map will appear

<figure><img src="../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure>

The customer's address will be displayed, though user can override that with a different address.

The default radius is 5 miles, but that can also be overridden by the user to have a larger or smaller area.

User selects Get postal codes to get all the postal codes in the radius area.  Any postal codes which match a defined Zone in the Product Setup will be pre-selected in the list. (this uses geo-coding, so on product setup one must get lat/long coding for the zones).

Finally, user selects the yes/no flags for the desired Zone Dimensions (HD, SC, and Retail in my sample system setup)

User clicks Use Selected Zones to save selection and return to the Zone Selection screen with the selected Zones displayed.

<figure><img src="../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>

Click next to proceed to the Inset Details

#### Insert Details

<figure><img src="../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure>

* Pages - select desired number of pages for the insert.  Available numbers here will be based on the Page Type setup
* Total Weight - this will default based on the pages selected and the page type setup.  Can be overridden by the user
* Spoilage Percent - again will default from the Page Type and # of Pages selected, but can be overridden by the user.
* Total Distribution - not editable - this is the quantity from the Zone selection on the previous step
* Size Code - Default based on the Page Type Setup.  Can be overridden by the user to another size code.  Only Size Codes flagged as being Insert/Preprint Size codes will be in the dropdown.  May be further filtered by Size Codes allowed on the product.
* Spoilage Qty -  Calculated field equal to the Total Distribution \* Default Spoilage % - can be overridden
* Base Print Qty - Equal to the Total distribution plus the Spoilage
* Optional Metadata fields - if custom fields were configured on the page setup, they will be displayed here, and the user can answer the questions

Click next to continue to overruns

#### Overruns

This optional tab is used if there are any overruns requested on on the order.  These overruns may or may not be charged to the client, but will affect the total quantity needed from the printer

<figure><img src="../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>

There is no rate setup in the background for this.  The user simply types in the information based on the agreed upon price with the client.  Overruns will create additional line items on the order, so Ad Type is important, to properly charge for it and have it map to the correct G/L.  the Ad Type drop down will only display CPM, FF, or CPU line types.

A CPU ad type will calculate the Price by multiplying Qty \* Rate

A CPM ad type will calculate the Price as Qty \* Rate / 1000

A FF Ad type will disregard the Qty in the price calculation and the Price will equal the rate

Click ok and select next to enter adjustments (if applicable)

#### Adjustments

<figure><img src="../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>

Enter one or more adjustment codes as necessary (optional) and click next

<figure><img src="../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>

#### Price and Book

Most of the fields on this final screen are read only.  Only the Billing Quantity can be edited here. There is a "Price it out" button at the top to re-calculate the price.  Generally this isn't needed, but is there in case there is a price change that didn't automatically calculate upon opening this screen.  There is a "Show Rate Selection" button as well which will display which rate was chosen and why (See [Insert Rating Schedules](release-guide.md#insert-rating-schedules) for info on how we determine what rate to charge).

<figure><img src="../.gitbook/assets/image (129).png" alt=""><figcaption></figcaption></figure>

Click Finish to save the order,

One order line will be created for the Primary Issue and any Perpetual Issue dates set on the Product Selection tab (again with all the revenue being tied to that Primary issue date), and one order line will be created for EACH Overrun line.

#### Post Billing user experience

Once the line has been invoiced, the user experience will differ slightly.  The order will still open up in this wizard-like workflow, but the user will see that the order has already been billed and limited information will be editable at this point.  Nothing that affects pricing will be editable.

**Product Selection Tab -** nothing on this page is editable after billing has started.  User can click on the link in the red bar at the top to view the associated invoice. (or it is also available on the campaign Invoices and Payments node, as always)

<figure><img src="../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

**Zone Selection Tab -** nothing on this page is editable after billing has started. &#x20;

<figure><img src="../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

**Insert Details Tab -** This page allows editing of the weight and the metadata. &#x20;

<figure><img src="../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>

Overruns Tab - on the overruns tab, no new overruns can be added and within an overrun, only the description and delivery address can be edited after billing.

<figure><img src="../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>

**Adjustments Tab** - Nothing on the adjustments tab can be edited post-billing.  If adjustments are needed after billing, Post-Billing adjustment tickets should be the workflow used to request an adjustment.

**Price and book Tab -** Nothing on this tab is editable after billing. User can click on the Show Rate Selection button to see what rate was selected (and if there were other possible matching rates that were not selected.)

<figure><img src="../.gitbook/assets/image (107).png" alt=""><figcaption></figcaption></figure>

### <img src="../.gitbook/assets/image (106).png" alt="" data-size="line">  Filter for easier GAM GeoTarget searching

There is a new dropdown field in the geotargeting field on campaign entry

<figure><img src="../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

Selecting what you are searching on in the dropdown will filter the list to better match what you are looking for and cut out some extra matches

<figure><img src="../.gitbook/assets/image (103).png" alt=""><figcaption></figcaption></figure>

Options include filtering on City, State, Province, Country and more

<figure><img src="../.gitbook/assets/image (102).png" alt=""><figcaption></figcaption></figure>

### G/L Override by Client Type

A new column has been added in the G/L Overrides node in Product Setup

<figure><img src="../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>

Now the G/L selected for each G/L Override can vary based on the client type of the advertiser.  To create a new GL Override, click the button "Add an Override" and a popup window will open:

<figure><img src="../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

G/L Type, Revenue G/L Code and Agency Commission G/L code are all required fields.&#x20;

Client Type is only necessary if you choose to use this feature.

Cost G/L and Cost A/P G/L Code are only required if you choose to put cost information on the campaign lines and have them affect G/L mapping. (This was a new feature in [**2023.1**](https://docs.navigaglobal.com/navigaad/v/advertising/welcome-to-naviga-ad/release-guide#\_toc124253160))

### Import option for Price Adjustment Setup

Navigate to **Setup -> Product Setup** and select the new "**Price Adjustments Import**" option to import Adjustment codes for products.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

1. Click the button to Download Template to get the excel file needed to import adjustment codes.  Fill in adjustment codes according to the following template:

<table><thead><tr><th>Field</th><th>Example</th><th width="311">Description</th><th>Required?</th></tr></thead><tbody><tr><td>Product ID</td><td>DEMO123</td><td>Alpha-Numeric field representing the ID for the Product</td><td>Yes</td></tr><tr><td>Description</td><td>Premium Surcharge</td><td>Alpha-Numeric field used to describe the adjustment. This is what the user will see when selecting an adjustment in order entry and what the customer may see on the invoice/order confirmation</td><td>Yes</td></tr><tr><td>External ID</td><td>ABC123</td><td>Alpha-numeric field which may be used in interfaces to external systems</td><td>Optional</td></tr><tr><td>Allow Description Override</td><td>Y</td><td>This is a Y/N field to indicate if the Description can be overwritten by a user in order entry screen.</td><td>Optional.  If left blank and answer of No (unchecked) will be applied.</td></tr><tr><td>Plus/Minus</td><td>-</td><td>+/- field which indicates if the adjustment should be positive (surcharge) or negative (discount).  If left blank, the user will be able to select a positive or a negative adjustment in order entry</td><td>Optional</td></tr><tr><td>Type</td><td>GROSS</td><td>These are hard coded options in the system.  Use the following to indicate the correct option:<br>GROSS = Percent of Gross<br>NET = Percent of Net<br>AMOUNT = AMOUNT</td><td>Yes</td></tr><tr><td>Prompt for Value</td><td>Y</td><td>If set to Yes (Y) the user will be allowed to enter in a value for the discount during order entry.  If set to No (blank or N), the value will need to be set in the "Value" field</td><td>Optional</td></tr><tr><td>Prompt for Qty</td><td>Y</td><td>Only valid if the Type is set to AMOUNT.<br>If type is AMOUNT, this can be set to Y for Yes or it can be blank or N for No.<br>If Type is GROSS or NET, this should be left blank.</td><td>Optional</td></tr><tr><td>Value</td><td>-50</td><td>If the plus/minus field is negative, this must also be negative. If Prompt for Value field is Y, this should be left blank.</td><td>Optional, but if Prompt for Value is No, this should be filled in with a value</td></tr><tr><td>Hide on Forms</td><td>Y</td><td>Y for Yes, N or blank for No</td><td>Optional</td></tr><tr><td>Currency</td><td>POUND</td><td>Only use this for <strong>foreign</strong> currencies.  For amounts in the system's default currency, this should be left blank.  </td><td>Optional, but if used the currency ID from currency setup is what is expected here.</td></tr><tr><td>Ad Type(s)</td><td>CPCI,DCI</td><td>This will allow the adjustment to only be available for certain ad types.  Leave blank to allow for all ad types. Multiple ad types can be entered and comma separated</td><td>Optional, but if used, the values entered here must match the Ad Type ID's in Ad Type setup</td></tr><tr><td>Plan Position Code</td><td>FIRST</td><td>Used for Sorting in Naviga Plan. See <a href="../naviga-ad-modules/advertising/setup/product-setup/products/pricing-rules/price-adjustments.md#plan-position-code">Price adjustment Setup</a> for details</td><td>Optional. Leave blank if not using Naviga Plan</td></tr><tr><td>Section(s)</td><td>NEWS,LOCAL</td><td>This will allow the adjustment to only be available for certain sections.  Leave blank to allow for all sections. Multiples can be entered and comma separated</td><td>Optional, but if used, the values entered here must match the section ID in Product Setup</td></tr><tr><td>Position(s)</td><td>BP</td><td>This will allow the adjustment to only be available for certain sections.  Leave blank to allow for all sections. Multiples can be entered and comma separated.  If Positions are defined within a section according to product setup, then the section must also be entered on the template for position to be accepted.</td><td>Optional, but if used, the values entered here must match the Position ID in Product Setup.</td></tr><tr><td>Override G/L Account</td><td>01*002*123*1234</td><td>This will allow the Adjustment to be applied to a different G/L than the revenue for the order line.  See <a href="../naviga-ad-modules/advertising/setup/product-setup/products/pricing-rules/price-adjustments.md#override-g-l">Price Adjustment setup</a> for details on using this optional field.</td><td>Optional, but if used it must match a G/L code defined in the G/L setup</td></tr><tr><td>Application Rule</td><td>LAST</td><td>This is only used in Booking Wizard order Entry and allows for the adjustment to be applied only to the First insertion, Last Insertion, or All insertions.  Valid options here are FIRST, LAST, and ALL.  A Blank will assume all insertions.</td><td>Optional</td></tr><tr><td>Inactive</td><td>Y</td><td>Leave blank for No.  This sets the Adjustment code to Inactive if set to Yes.</td><td>Optional</td></tr></tbody></table>

2. Once the spreadsheet is filled in with your data, save the file to your computer or desired network location.
3. Click the Select button and navigate to the file location&#x20;
4. Click test import file.  The system will do a test import and will notify the user if there are any errors in importing.  If there are no errors, skip to step 8
5. Open saved spreadsheet and correct any errors, and resave
6. Remove the original uploaded file by clicking the X remove\
   ![](<../.gitbook/assets/image (1) (1).png>)
7. repeat steps 3 - 6 until all errors are resolved
8. Click Import File to run the actual import process.

### Group Security Change

#### Disallow campaign status change from R back to Q

New flag added to disallow campaign status change from R back to Q.  If you set this option to Yes, it will prevent users in this security group from reverting campaigns in any Reserved status to Quote status manually or through the Bulk Update Process.  You might want to consider setting this to yes if you have integrations with downstream systems that send the ad somewhere else when the order becomes reserved.

<figure><img src="../.gitbook/assets/image (226).png" alt=""><figcaption></figcaption></figure>

#### Restrict G/L Type in line override to codes on product

<figure><img src="../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

In product setup, G/L Overrides can be assigned to the product which then get used in ratecards and ultimately on line items so that the system knows what G/L to assign during billing.  Group Security dictates if this G/L Type can be overwritten at the line item level.  This new group security controls if ALL G/L Types or only G/L Types used on the product are available to be selected (assuming the user is allowed to override the G/L type assigned by the ratecard line).  If this is set to 'no' AND users are allowed to override the G/L Type on a line, then all G/L Types will be displayed in the dropdown.

### Fields added to several screens

Advertising Client Type and Prepay Required added to the Client overview screen:

<figure><img src="../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

Client Type added to the Invoices & Payments node on a campaign:

<figure><img src="../.gitbook/assets/image (175).png" alt=""><figcaption></figcaption></figure>

Client Type added to popup when changing the advertiser on a campaign (on a campaign, select edit -> change Advertiser to see this popup):

<figure><img src="../.gitbook/assets/image (178).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If you don't see the option to change the advertiser, remember in [**2023.4**](https://docs.navigaglobal.com/navigaad/v/2023.4/welcome-to-naviga-ad/2023.4-release-guide#a-dvertising-security-greater-than-campaign-header-security) this was added to group security so a user must have permission to be able to change the advertiser on a campaign.
{% endhint %}

Client type (ID and Description) added to the Report **Customers -> Advertiser Listing**

<figure><img src="../.gitbook/assets/image (186).png" alt=""><figcaption></figcaption></figure>

Prepayment Required Flag added to the Account Approval Screen:

<figure><img src="../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

Two new columns has been added to the Payments tab on the Accounting screen of the Customer account overview. This will display the Cash on Account reason and any comment entered when applying payments.

<figure><img src="../.gitbook/assets/image (171).png" alt=""><figcaption></figcaption></figure>

Advertising Home screen - Campaign Tab - added Campaign Description to the grid here:

<figure><img src="../.gitbook/assets/image (218).png" alt=""><figcaption></figcaption></figure>

Client Type added to the Agency field dropdown on Brand Detail screen (**Customers -> Brand -> Brand Maintenance**):

<figure><img src="../.gitbook/assets/image (220).png" alt=""><figcaption></figcaption></figure>

<img src="../.gitbook/assets/image (7) (2).png" alt="" data-size="line"> Fields added to Orders by Product Report: Material Description, Campaign Entry Date (click on Configure output tab to choose which columns to display):

<figure><img src="../.gitbook/assets/image (221).png" alt=""><figcaption></figcaption></figure>

### Orders by Entry Date Report Changes

Several great changes on the Orders by Entry Date Report:\


<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

1. Users (multi-select) added to the search criteria at the top of the report
2. Product list uses intuitive typing to filter the dropdown, making selection easier
3. Grouping added to the report so that user can drag and drop column headers to the light blue bar to group data by various fields
4. Several additional columns added to the configure output tab
   * Campaign Entry Date
   * Existing field "Entry Date" relabeled ad "Line Entry Date"
   * Campaign Description

### Sort order for Classified Categories

In previous releases, user could drag and drop category metadata questions in setup to set the sort order, but parent level questions were always displayed at the top (in whatever sort order was set for the parent), and child questions would be displayed after the parent, in whatever sort was set for the children, and they could not be intermingled at all, and the child questions could not be asked before the parent questions.  That has now been modified and setup users can enter sort codes at the parent (for the parent metadata) and at the child (for child metadata) and when in use these codes will allow the metadata to flow in a logical order to the end user, and parents and children may be intermingled together.  The sort is an alpha-numeric sort, so if you are using numbers, if you have more than 9 questions, be sure to pad the numbers with zeros in front. For example, if you have 15 questions, you would list them 01, 02, 03...10, 11, 12, etc.

In this example, Employment is the parent, and Full Time Help is the child.  Only a single question is asked at the child level, but the desire was to present it to the user, right after the headline and main body text:

<figure><img src="../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

When presented to the end user, this then looks like this:

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note: only internal users currently will see this new sort.  Not currently in use for Classified Self-Service Portal.
{% endhint %}

### New Interval option for Classified Packages

When setting up a classified package, there has always an option to restrict to certain days of the week and to put a quantity on the number of issues, but the quantity would always select consecutive issues, unless issue days were restricted, so it was difficult to do a weekly package that would run once a week on any day, but always the same day from week to week.  Now, there is an interval option on package setup.  The default upon upgrading will set this to "days" on existing packages, since that will be the behavior it has always been, but the setup user can select Week(s) or Month(s) instead:

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

In the above example, if weeks was selected, without any issue day restriction set, the behavior will be to run the ad for 6 consecutive weeks (one issue per week) starting from the start date of the package. The default will be the start date of the campaign, but prior to selecting the package, the user can select a different start date in the booking wizard.  The result will be to schedule 6 insertions on the same day of week as the start date.

<figure><img src="../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

If 6 months was selected in the package setup, the behavior would be to run one issue per month on the same day of month as the start date, so in the below example it is the 14th day of the month, each month, for 6 months.

<figure><img src="../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## CRM Module

### Group Security Change

New Flag in Opportunities which will allow for a single opportunity to cross multiple product groups, and when the proposal is auto-generated, there will be multiple proposals/campaigns created - split by the primary product group on product setup.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

To use this feature, set the above to "yes" and then create an opportunity and link products from different product groups:

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

From there, click the button to auto-create a new proposal

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Quick entry screen will open and allow for any modifications to dates, prices, etc before checking inventory and booking:

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Two proposals will be auto-generated for this campaign, one for each product group:

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

With the new group security flag set to "no", the opportunity would behave like it did in older versions and all products would need to be in the same product group and they would be booked onto a single campaign.  The default behavior upon upgrade will be for this flag to NOT be set and the system will continue to behave as it did in prior releases.

## Accounts Receivable Module

### List of Imported Payments

Minor makeover on the List of Imported Payments.  Navigate to Payments -> List of Payments -> List of Imported Payments. Note that the Company ID has been added as a new column and there is now a row of filters at the top of the columns.

<figure><img src="../.gitbook/assets/image (173).png" alt=""><figcaption></figcaption></figure>

### Option to require an address to approve accounts

There is a new setting on the A/R header (**A/R Module -> Setup -> Admin -> A/R System Setup**, then navigate to Client Defaults Section. If the following is set to yes, the account will not be allowed to be approved if the address or phone number missing on the account.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note - based on CRM System Settings (**CRM Module -> Setup -> CRM System Settings**) it may or may not be required for the CRM user to enter in the address at the time of account creation.

Based on Address Settings on Country Setup (**Ad and A/R Modules -> Setup -> Shared Tables Setup -> Address Setup**), an address may or may not require State and/or Post Codes
{% endhint %}

If the address and/or phone number is missing, on the Approve Pending Accounts screen the approving user will be stopped from approving accounts if the address is missing:

<figure><img src="../.gitbook/assets/image (232).png" alt=""><figcaption></figcaption></figure>

### Logo for Receipt

Receipt templates can now be setup to include the logo from the bank. &#x20;

To Setup:

1. Add the bank's logo to the Advertising invoice logos
   * Navigate to **Setup -> System Tables Setup -> Invoice Form Logos**
   * Enter ID, Description, and upload file
   * Click + to add to logos and click save.
2. Link the new logo to the bank setup
   * Navigate to Setup -> System Tables Setup -> Bank Setup
   * Select the desired bank
   * Select the new logo from the logo dropdown\
     ![](<../.gitbook/assets/image (191).png>)
3. Add tag #BANK\_LOGO\_URL# (image) and/or #BANK\_NAME# (Name of the Bank) to the receipt template in desired location.\
   In my sample, I have placed them here:\
   ![](<../.gitbook/assets/image (210).png>)

Logo will be displayed on the Receipt:\


<figure><img src="../.gitbook/assets/image (217).png" alt=""><figcaption></figcaption></figure>

### <img src="../.gitbook/assets/image (240).png" alt="" data-size="line">Credit Stop Report - Credit Rating added

The screen for Adding/Removing Clients from Credit Stop will now also display the customer's credit rating:

<figure><img src="../.gitbook/assets/image (256).png" alt=""><figcaption></figcaption></figure>

Navigate to **Credit Control or Accounts Receivable Module -> Credit Control -> Add/Remove customers from Credit Stop** or a user who is an A/R Manager can also access this report by clicking the Add/Remove Clients from Credit Stop button from the navigation bar in the credit control module

## Advertiser Portal

### Mark Inactive/Delete Profiles

Two new functions are now available in the Advertiser Portal setup.  For any profile that you no longer wish to use you may mark it as inactive:

<figure><img src="../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

&#x20;If the Profile perhaps was created in error, or you are certain you no longer wish to use it, the profile can also be deleted by scrolling to the bottom of the page and clicking delete:

<figure><img src="../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>



***

{% hint style="info" %}
<img src="../.gitbook/assets/image (7) (2).png" alt="" data-size="line"> In 2022 we introduced the idea of a Customer Enhancement Portal, where you all get to add feature requests, look at feature requests submitted by others, add comments, and vote on things you would like to see us implement in the system. Items that were voted up in the Enhancement Portal will have this check mark next to the feature in the release guide.

<img src="../.gitbook/assets/image (7) (2) (1).png" alt="" data-size="line">  Click on the Video Icon in the heading to be directed to the release video page.  Topics that were included in the release video will display this icon.

<img src="../.gitbook/assets/image (97).png" alt="" data-size="line"> In 2023 we introduced a new learning subscription program called NavigaYou. Part of that program are some custom development hours. Any new features that were part of someone's NavigaYou will be highlighted as such with this icon. See [WEBINAR ](../videos/naviga-ad-video-library/conferences-and-webinars.md#navigayou)for more info on NavigaYou
{% endhint %}

