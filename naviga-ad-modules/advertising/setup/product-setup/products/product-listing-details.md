# Product Listing / Details

## Product Listing

<figure><img src="../../../../../.gitbook/assets/image (892).png" alt=""><figcaption></figcaption></figure>

The Product Listing view is simply a list of all the products defined in the system. It can be useful when searching for information about the products. The filters and sorting options at the top are useful is you need to gather a list of all your Digital products, or all you products in a certain format, or all inactive products. This list can be downloaded to excel and/or pdf format.

## Product Details - Product Settings

### Prerequisites to setting up your products

* [Product Formats](../../product-formats-setup.md) - All Products are linked to a Product Format so you will need to be sure to have some setup or you won't be able to save your new product.
* G/L Codes - Products need to be linked to a G/L code for Revenue, Deferred Revenue and A/R before it can be saved, so you will want to be sure that is set up before trying to create your products.
* [Company Setup](https://github.com/it-infra/NavigaAdGitbookSync/blob/NavigaAd2023.4/naviga-ad-modules/advertising/setup/product-setup/products/broken-reference/README.md) - All Products need to be linked to a company, so that will need to be set up in advance of setting up products.
* [Product Groups](../product-groups.md) - All Products belong to at least one Product Group. The Primary Product Group must be selected when the product is created.

### General Settings

**Product ID / Name** - The product ID and Name are defined when creating a new product. The product name can be modified, but the product ID cannot. When creating new products, to save setup time, you can copy the settings from one product to another.

[Format ](../../product-formats-setup.md)- This dropdown is set in Advertising Setup. Select the desired format for this product.

**Inactive** - Set this flag as inactive if it is desired to no longer be able to book orders for this product. The product will still be available in product dropdowns for reporting, but will no longer be available in order entry

**Product Type** - These are naviga defined product types. What is selected here will determine what other settings need to be filled in for this product. (For example, the system won't ask for GAM settings on a print product, and won't ask for page size metrics or bleed settings for a digital product). Options include:

* Print Product
* Standard Product (website/mobile app)
* Group Product (This is a network product that is made up of multiple Standard Products)
* Date/Issue based Products - these are digital products, but ones that are booked for specific issue date(s) rather than a date range like a website would be, such as an eNewsletter.

Default Custom Data Form - In some cases it is desirable to fill in additional data about certain products. Custom Data Forms are visible in Order Entry (either for additional production related details or on Campign Tickets that might require a form), in Production Reports and also in the Advertiser Portal. The forms are set up in Setup -> Custom Forms Setup

[Ad Serving Platform](../../advertising-setup/ad-serving-platforms.md) - This is the advertising platform such as any social advertising media platform. This is not for the standard Google Ad Manager (GAM) integration.

[Invoice Line Group](../../advertising-setup/advertising-invoice-forms-templates-line-groups.md#invoice-line-groups) - When creating invoices it is often desirable to group similar products together into its own group. It isn't required, but if you display different information on a print line than you would on a digital line it is often helpful to group them separately.

Hide Zero Value Lines - When set to YES, lines with a zero value will not display on invoices nor confirmations.

[Affidavit ](../../../billing/affidavits.md#\_toc106020200)Template Form - only displayed on Print Product types. This is the default template used on Affidavits for this product. This default can be overwritten during affidavit creation.

Product URL -

[Company](https://github.com/it-infra/NavigaAdGitbookSync/blob/NavigaAd2023.4/naviga-ad-modules/advertising/setup/product-setup/products/broken-reference/README.md) - The URL of the product if one exists

[Primary Group](../product-groups.md) - This sets the primary product group for this product. in Product Group Setup this product can be linked to additional product groups. The group is used in reports across the system and is commonly used to analyze sales and accounting data

[Holiday Calendar(s)](../../advertising-setup/holiday-calendars.md) - Holidays are used to stop entry of issue/date-based orders and creation of issue dates on holidays

Default Artist Assignment - This is the default artist who’s assigned to the material designs on an order in this product. These names are pre-setup in the system in the Setup menu -> [Artist Workflow Setup](../../artwork-workflow-setup.md#artist-setup)

Consolidate Lines on Forms - If set to yes, this option will consolidate lines for this product on Order Confirmations, Proposal and Invoices - so long as the Size and Rates match. For digital products the consolidation is by Line.

No Agency Commission Allowed - If checked “Yes” then no agency commission is allowed on the order line. If left unchecked “No” then the order will have agency commission

Charge Tax - If checked “Yes”, then a tax will be added to the campaign based on the settings for tax overrides.

[Allow Edition Splits ](../../advertising-setup/material-edition-splits-setup.md)- Only displayed on Print Product types. Edition splits are available to be used in print products. Edition splits allow user to have the same priced ad with different materials in an edition which is sent to different regions and different demographics. When you click Yes, this allows you to use this in an order

→ Flexible / Free Format Date Selection - only shown on the digital Date/Issue based Products - This sets whether actual issue dates will be set up in the [Published Dates](issue-based-setup/) section, or if the user will be able to select any issue date.

Time Display Option - only shown on the digital Date/Issue based Products - Options here include:

* Hide Time Selection Option - Only date selection is allowed for this product and not a specific time.
* Free Format Selection of Time - User can select any time
* Audience Controlled Time Selection - this look look at the audience on the booking and the [Audience Setup](../../audience-setup.md) to determine if this time is allowed based on other orders that are also targeting the same audience.

→ Default Audience - only shown on the digital Date/Issue based Products - This will be the default audience for a given product. It can be overwritten during order entry,

### Material Lead / Closing Settings

This will look slightly different for Print vs Digital. We only see the Default Closing days/times settings on Print Products.

<figure><img src="../../../../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

Material Lead Time: This field is the number of days which precede the closing date of the product. This is also a prerequisite for the production workflow setup where the material lead time will be the material due date for the product by which the reminders will display for user to email the production contact on each order.

Material Lead Time of Day: This will be used in conjunction with the above setting to determine the time and date of when the is material due.

Default Issue Closing Days: When new issues are created, this is the default number of days before the issue date when the issue will be closed. Unless allowed in Group Security, users won't be allowed to book an order past the closing date/time.

Default Issue Closing Time: When new issues are created, this is the default time when the issue will be closed on the close date.

#### **Material Lead / Closing Settings - Overrides by Artwork Type, Ad Type, Category Tree**

In Group Security -> Advertising Security option to “ALLOWED TO ENTER ORDERS IN CLOSED ISSUE” must be set to “No” for these settings to apply.

Artwork Type, Ad Type, and Category Tree are controls for close dates settings on an issue of a product. Close and material date on print product may be defined by Ad Type, and Category as a combination where the Close Date for issues will be applied by the system as it checks the settings in this order:

i. Combination of Material Type/Ad Type/ Section/ Category, then if not set,

ii. Category or Section only, then if not set,

iii. Ad Type only, then

iv. Issue Date, then

v. Product default setting.

Select the Ad Type in the drop-down and Category Tree valid combination. You may choose only the Ad Type and no Category Tree and vice versa. If you’re setup in the system to not allow for entry of orders in closed issues, and you try to create a line in an issue past these settings, the system displays a message preventing you from saving the line item, and the reason why the system prevents you from doing so.

Note that the Material Close Date being set doesn’t affect your ability to enter the line item or attach materials but will impact other areas as per the production workflow reminder setup.

### Affiliate Publisher

<figure><img src="../../../../../.gitbook/assets/image (238).png" alt=""><figcaption></figcaption></figure>

See [Affiliate Setup](../../affiliates.md)

### Publication Specs

These will only be displayed on print Products

<figure><img src="../../../../../.gitbook/assets/image (1160).png" alt=""><figcaption></figcaption></figure>

#### Publication Page Size Specifications

Default Column Layout - See [Column Layout Maintenance](../../advertising-setup/column-layout-maintenance.md)

Unit of Measure - Select Inches/CM/MM. This lets the system understand the size of the Page Size below.

Page Size - the physical size of the paper (width x depth) in the measurement selected above. It is important for this to be accurate in [Page Eq Calculations](../../advertising-setup/ad-sizes.md#page-equivalency-for-print-ads)

Lines per Page - This is used when calculating the page eq for modular ads. With modular ads, when the size is setup the line eq is set as a fraction of this number. For example, if the Product is set as 420 lines per Page and the ad type is a half page ad, then the Line Eq on the ad size should be 210 (or 420 x .5).

#### Default Bleeds and Margins

These settings are all used by Naviga Plan to understand the margins and bleed settings of ads being sent over:

* Top / Bottom / Left / Right Bleed
* Top / Bottom / Left / Right Margin

### Digital Product Settings

These settings are only displayed on non-print products (Group Product, Standard Product & Date-Based Products)

#### Ad Server Settings

<figure><img src="../../../../../.gitbook/assets/image (1468).png" alt=""><figcaption></figcaption></figure>

This sets the Ad Server and Profile to be used for this product

If there is a desired Default Ad Unit or Placement for the product, you may set it here as well

#### Ad Units allowed for this Product

<figure><img src="../../../../../.gitbook/assets/image (547).png" alt=""><figcaption></figcaption></figure>

Along the left column are all the ad units for the Ad server select in the settings above. If this product only uses a subset of the Ad Units on the ad server, they can be selected here. This reduces the available options for the end user when booking a digital order line.

To select an allowed ad unit, click the checkmark icon on the left side and that unit will be moved to the right side. uncheck selected units on the left, and it will be removed from the right. OR select one or more ad units on the right and click the X to the right and those will be removed.

#### Key Target Filters

<figure><img src="../../../../../.gitbook/assets/image (694).png" alt=""><figcaption></figcaption></figure>

To limit the allowed Key-Value pairs for this product, select the desired Key Targets from the left column and click the single arrow to move them to the right. If you wish to allow all, you may simple not select any and they will all be allowed.

#### Actuals Reconciliation Override

<figure><img src="../../../../../.gitbook/assets/image (242).png" alt=""><figcaption></figcaption></figure>

The default option here will be to use the setting on the client and or the line item. The setting on the client is the default, and the line item will override the client setting.

Selecting "When using Ad Server Impressions, always use Viewable" will override the client/line setting _**on this product**_ to always use Viewable impressions, even if the client would otherwise use Ad Server Impressions for other products.

## Product Details - G/L Defaults

Enter the appropriate G/L codes for this product. This is especially important if you selected on the Product Group Settings to derive the G/L codes from the Product. The Deferred A/R and Revenue will be set automatically based on the G/L Setup for those G/L's. These are only the Default G/L's for the product. The G/L Overrides will handle most of the details where you want different G/Ls for different kinds of ads within the product.

<figure><img src="../../../../../.gitbook/assets/image (1420).png" alt=""><figcaption></figcaption></figure>

Remit-to Commission Settings are only required if that is something you do. Not commonly used these days, but this is used when the Client is billed directly for the Gross amount of the order and the agency is paid its commission only after the client has paid. This allows the Remit-to Commissions to be tracked in a separate G/L than regular agency commissions.

## Product Details - Campaign Parameters

The “Campaign Parameters” tab provides order entry restrictions on the orders for this product.

<figure><img src="../../../../../.gitbook/assets/image (1615).png" alt=""><figcaption></figcaption></figure>

If you choose a **default production controller** from the drop-down, this will be used in the _Production By Controller_ and _Production Reminders by Controller_ reports when selecting to run the report with the controller assignment as set From Product. It is set on the product, but not visible on the order entry screen.

Enter Sections/Positions/Sizes - Select Yes/No/Mandatory for each of these.

* Yes - You will see the field in Order Entry and you can choose to fill this in, or not.
* No - This field will be hidden from view in order entry as it is not used
* Mandatory - The user will no be able to save the order without selecting something in this field

The field “Position by Section” determines whether you want to create the positions within sections or not. “Positions are Defined Independent of Sections” option allows you to create positions and not sections.

{% hint style="info" %}
\*\*\*Note for sites using Naviga Plan\*\*\* When creating Sections and Positions, if you have some Print products that use the setting “Positions are Defined independently of Sections” please let your Naviga Plan Implementation Specialist know which products use that setting. These are handled differently and require different setup by the implementation specialist.
{% endhint %}

**Split New Lines:** If “Yes”, any new line for a date-based product will split the lines one for each issue. If it’s a date range, then each month will be split into a new line. When creating a new Date-Based or Issue-Based Product line with multiple event dates, each event will be broken out into a separate line on the Campaign. When creating a Date-Range line each month will be broken out into a separate line on the campaign. _**If you want to allocate Price Adjustments to their own G/L codes, then this option must be set to "Yes."**_

**Ratecards mandatory** - set to yes if a rate card is required for this product. Users will not be able to save the order if they have not selected a ratecard and rateline.

Auto Create Material - Set the value to “Yes” if you want a material record to be automatically created when you create a new order. The physical material may be added at a later time, but this will automatically create a blank material record when the order is saved if one wasn't already added.

**Must use Quick Line Entry for this Product:** If set to yes, this product won’t appear in the full line entry but only in the quick line entry method.

### Additional settings for Print Products only:

**When Attaching First Material:** This option determines what happens when you attach the first material to an order. The options are:

* Link to any Issue(s) that do not have material: This links the material to all issues which have no material attached.
* Link to only the first issue without material: This links the material to the first issue in the lines which doesn’t have the material.
* Do not automatically associate with any issues: This allows you to choose in order entry which line to attach the material.

**Clear Material Associations on Renewal or Campaign Copy:** On Campaign Renewal or Campaign Copy, when copying material associations, by default the most recent material record used on the old line item is associated with the new line item. Setting this option to yes will instead clear out any material associations from the line you are copying and follow the same rules you have set for standard line entry.

### Additional settings for Digital Products only:

Auto Create Missing Digital Sizes - this option only applies to Full Line Entry and only applies when the order is first saved.

### Notification settings for Order Line Events

Each of the following offers the ability to select a user to notify via email and/or a slack channel to notify. Slack Channels must be set up in advance in Setup -> Admin -> [Other Integrations](../../admin/other-integrations/slack-channel-setup.md).

* Quick Starting Campaigns / Line Items - If a new campaign or line item is set to start within the defined number of days, alert the following person(s). This includes the number of days before start that would be considered "quick starting." For example, a digital website product might be quick starting if it was booked 2 days before start, while a print magazine product might be considered quick starting several weeks before publishing.
* Changes After Issue Close - If changes are made to a confirmed order after the issue close date, alert the following person(s)\*\*
* Confirmed Campaign Line Item is Added - If a line item is added on a Campaign in Confirmed (CO) status, alert the following person(s)
* Confirmed Campaign Line Item is Changed - If a line item is changed on a Campaign in Confirmed (CO) status, alert the following person(s)\*\*
* Confirmed Line Item is Deleted - If a line item is deleted on a Campaign in Confirmed (CO) status, alert the following person(s)

{% hint style="info" %}
\*\* Any of the following events would constitute a "Change" to the order:

* Section change
* Position change
* Rate change
* Change to Estimated Qty or Amount
* Change to Line Description
* Change to dimensions/size
* Ad Unit Change
* Start Date/End Date Change
* Issue Date Change
* Change to Contract ID
* Price Adjustment
* Change to Original/Order Rep
{% endhint %}

### Ad Type Restrictions

All Ad Types will be listed on the left column. Use the single or double arrows in the center to move a few, or all ad types to the available column. This will restrict the ad type options in order entry to only what is available for the product. This can also be set in Ad Type Setup if creating a new ad type and the product has already been created.

<figure><img src="../../../../../.gitbook/assets/image (1167).png" alt=""><figcaption></figcaption></figure>

### Size Restrictions

All sizes will be listed on the left column. Move desired sizes to the right column using the arrows in the center. Digital Products will display digital sizes and Print Products will display only print sizes. (this is determined by the "For Print" yes/no flag on the size setup.

<figure><img src="../../../../../.gitbook/assets/image (1175).png" alt=""><figcaption></figcaption></figure>

### Editions (Print Only)

Editions can be configured for Print Products. Editions are then selected in order entry and will flow through to Naviga Plan so that we know which Edition/Zone to place the ad into.

The Edition is selected first in Full Line Entry and if ratecards are setup by Editions, only the selected Edition's Ratecards will be displayed.

Child editions can optionally be created as a shortcut in Order Entry. Using the below example, if a customer wished to run the same material in both the East Zone and the West Zone, the user could simply book for "All Zones" in order entry. The integration between Naviga Ad and Naviga Plan will understand this booking to be for both East and West and will pass 2 order lines to Plan - one for each Edition.

<figure><img src="../../../../../.gitbook/assets/image (665).png" alt=""><figcaption></figcaption></figure>

## Product Details - Order UDF's

If Order-level UDF's have been created in Advertising Setup, select one or more UDFs desired for this product. Select the Checkbox for "Required" if the user is required to fill in the field prior to saving the order in Full Line Entry or the Booking Wizard.

<figure><img src="../../../../../.gitbook/assets/image (1089).png" alt=""><figcaption></figcaption></figure>

## Product Details - Grouped Products

This is only displayed on Grouped or Network type Digital Product types, like a Run of Network product.

<figure><img src="../../../../../.gitbook/assets/image (895).png" alt=""><figcaption></figcaption></figure>

The actual billing and revenue recognition will typically be based on what websites the ad actually ran on (reconciled in the Reconcile Campaign Actuals process) - but what is set here is used for any estimates reporting.

In the dropdown list select the products that are included in this network product and click the + to add to the list. Enter the % distribution based on what typically would be the spread across these products (for example if one website gets double the traffic compared to another website, then the estimate percent should reflect that).
