# Product Groups

## Using Product Groups

Multiple products can be assigned to one group for organizational, reporting and even billing purposes. The group can be organized however you wish, such as product type as in print publications, and digital products, or by publication theme/brand, or in a multi-company organization it might be your internal companies.

There are security settings by product group in the menu Setup -> Admin -> Group Security -> [Product Group Security](../../../system-settings-admin/security/group-security.md#product-security) which allow you to control the groups per the security group of users.

In the Campaign Billing menus, you can run the billing by product group, if desired, as well as by date range or other fields.

Product Group has a G/L Override menu which when filled out, will override the Product G/L Settings.

It also has Email Notifications settings where chosen email recipients would receive an email notification under certain conditions, such as client credit limits exceeded or confirmed campaigns changing and so forth.

## Product Group Details

### Product Group Settings

<figure><img src="../../../../.gitbook/assets/image (1587).png" alt=""><figcaption></figcaption></figure>

* Product Group ID / Name - When creating your Product Group, you will assign a unique ID code and Name to the Group
* Company - Product Groups belong to a company - Select the Company from the Drop down
* Reporting Group Only - sometimes it is desired to report on products in different groupings than the groups that you book the ads for. Mark any such Product Groups as Reporting Group only. (For example - I have a product group for all my Print Naviga Plan Products and for all my eNewsletters so that I can view those reports easily, even if the rep booked them under different Product Groups.
* Charge Tax - Set to Yes if this product group charges taxes (there are also other places throughout the system which will influence taxes such as the Product and the Customer account.
* Override Tax Code - Select a tax code, if desired, as an override for this product group
* Derive G/L Codes From - There are a few places where G/L codes for Revenue and A/R can be set. This tell the system where to look for the rule.
  * Use Values in System Setup - In Setup -> Advertising Setup -> System Parameters, there is a Revenue Recognition Setting (Item #4). The choices there are Use Product Settings or Use Product Group Settings. So choosing this on the Product Group is saying, for this Product Group, I want to follow the rules I set for the entire system, and not override them.
  * Use Values on Product - I might choose this for a Product Group if I had chosen for the system to use values on the Product Group. In other words, I am able to set an override for this Product Group that is different than what i set on the System.
  * Use Values on Group - Similar to above. If i had set on the System header that i wanted to use the Values on the Product for G/L, I could override that on this product group to do something else.
  * Use Values on Product, but A/R Code from the Group - This one says to look to the Product for the Revenue G/L's but use the the Product Group for the Receivable G/L code. This one is good to select if you have multiple A/R's and frequently sell packages that cross companies. If you sell a campaign that has Product A (from one Company) and Product B (from another company) and they have different A/R's on the product - for this campaign, you are likely sending the client one invoice. So which A/R should it get? If you use the option Use Values on the Product, the user will have to be prompted to choose the correct A/R for the campaign. By selecting Use Values on the Product, but the A/R code from the Group, the system will know which A/R to use, because there is only one product group on a campaign.

#### Invoicing

<figure><img src="../../../../.gitbook/assets/image (1550).png" alt=""><figcaption></figcaption></figure>

Invoice Prefix - It is desirable for some to have a prefix on the invoice that represents the product group. That way users can tell at a glance what product group(s) the client might be referring to when they call about an invoice.

Credit Prefix - Same as above, but can be different for credits vs invoices

Override Invoice Email From Address - this will set the email address that invoices are coming from. In Setup -> Advertising Setup -> System Parameters, this is set at the system level (Item #11). If it is set here, it will override that email from address for this product group.

Remit to Address - On the invoice form template there is a field called #REMITTO\_ADDRESS# which can be placed on the form and will pull in the address from this field and place it on the invoice. When you have different remit-to addresses, this saves you from needing to have a separate form for each product group.

Performance Invoice Form - this is the invoice template which will be used when running invoices for this product group for Performance type campaigns

Flexible Invoice Form - this is the invoice template which will be used when running invoices for this product group for Flexible type campaigns

Override New Form Logo - similar to the remit to address concept, this will put this logo onto the invoice for the #LOGO\_URL# tag. Logos should be set up prior to setting up your product group (or you can add it later. This isn't required to save the product group.

BPAY Biller ID / BPAY Default Bank ID - This is used in the Australia market - Some users have different needs such as different BPay numbers for different groups of products. The BP ID is an Australian system that allows anyone to pay a bill from any device using just the vendor ID. If the two BPay fields are populated on the product group settings **and** invoicing is run by product group, then the fields populate on the invoices. AR Statements follow the same logic, so that if statements are run by product group and the statements have the two BPay fields populated, then the statement will display the info.

#### Other Form Defaults

<figure><img src="../../../../.gitbook/assets/image (733).png" alt=""><figcaption></figcaption></figure>

The above are the default forms for the Portal Signature templates and for the Proposal/Confirmation templates during order entry. There are separate forms for Performance Campaigns vs Flexible campaigns for both forms.

There is also a logo override. Similar to the invoice template above, you can share templates across different product groups and just swap out the logo at the top of the form by using the #LOGO\_URL# tag on the form rather than inserting the actual image on the form.

#### Form Overrides by Language

<figure><img src="../../../../.gitbook/assets/image (1318).png" alt=""><figcaption></figcaption></figure>

Some of our clients do business in other countries where different languages are spoken other than their default language. This section allows you to set overrides for Invoice, Confirmation and Portal Signatures for both Performance campaigns and Flexible Campaigns.

{% hint style="info" %}
The preferred forms language is ultimately set on the Client record under Advertiser/Agency Maintance screen (A/R Node), but it can default in for that client when the client is created (either from the import template of from the Country setup in Setup -> System Tables Setup -> Address Setup)
{% endhint %}

#### Renewal Effort Forms

<figure><img src="../../../../.gitbook/assets/image (1023).png" alt=""><figcaption></figcaption></figure>

See [Expiring Campaigns](../../campaigns/expiring-campaigns.md#sending-out-renewal-notices) for details on using Renewal Forms

#### Product Selection

This can be used to add products to this product group. select one or more products from the left column and use the arrows in the center to move them to the right column.

<figure><img src="../../../../.gitbook/assets/image (706).png" alt=""><figcaption></figcaption></figure>

If you have certain products that are commonly booked for a product group and you would like them sorted at the top of the list, or products that are frequently booked together, the products in the right column can be dragged and dropped to sort in a non-alphabetic order. This will only affect order entry product drop downs.

#### User Defined Fields

If you have set up Campaign level user defined fields, they will be displayed in here and you can select which ones you want to use for this product group, and move them to the right column.

#### Security Groups

<figure><img src="../../../../.gitbook/assets/image (604).png" alt=""><figcaption></figcaption></figure>

This is ONLY Displayed when you are creating a new product group. Once you save it, this section will disappear. Be sure to at least set your own security group as being allowed to access this product group, otherwise you won't be able to see it to select it once it is saved. (if you forget, you will need to go to Group Security -> Product Security and add it)

#### Default Ad Server Team(s)

Default Ad Server Team(s): The choice of the teams here is the default value which will display in the Campaign Entry “Other Information” tab. This will override the team value setup in the Ad Server Setup screen associated with the server.

In this section, you can also set a Prefix or Suffix to use for the Advertiser Name when auto creating a new Advertiser or Agency through the GAM Integration.

* Advertiser Prefix: When automatically creating a new Advertiser or Agency, this option will use this field to prefix the name used in GAM. Anything entered here on the Product Group will OVERRIDE the same setting in [GAM Connection Setup](../admin/ad-server-integration.md#\_toc105408190).
* Advertiser Suffix: When automatically creating a new Advertiser or Agency, this option will use this field as a suffix to the name used in GAM. To append the Account ID from Naviga to the Customer Account Name in GAM, add {NAME\_ID} here. Anything entered here on the Product Group will OVERRIDE the same setting in [GAM Connection Setup](../admin/ad-server-integration.md#\_toc105408190).

<figure><img src="../../../../.gitbook/assets/image (446).png" alt=""><figcaption></figcaption></figure>

### G/L Defaults

<figure><img src="../../../../.gitbook/assets/image (581).png" alt=""><figcaption></figcaption></figure>

Enter the appropriate G/L codes for this product group. Especially important if you selected on the Product Group Settings to derive the G/L codes from the Product Group. The Deferred A/R and Revenue will be set automatically based on the G/L Setup for those G/L's

Remit-to Commission Settings are only required if that is something you do. Not commonly used these days, but this is used when the Client is billed directly for the Gross amount of the order and the agency is paid its commission only after the client has paid. This allows the Remit-to Commissions to be tracked in a separate G/L than regular agency commissions.

### Campaign Parameters

<figure><img src="../../../../.gitbook/assets/image (376).png" alt=""><figcaption></figcaption></figure>

There are several campaign parameters which can be set at the Product Group level:

<table data-header-hidden><thead><tr><th width="278"></th><th></th></tr></thead><tbody><tr><td>Is the P.O. Number Required on Confirmed Campaigns</td><td>Set to yes if this product group always requires a purchase order number on the campaign</td></tr><tr><td>Require Entry of External Order ID</td><td>Set to yes if this product group always requires an External Order ID (might be set on campaigns that are coming in from a 3rd party)</td></tr><tr><td>Exclude from Use on Flexible Campaigns</td><td>If you do not want this product group to be allowed on Flexible campaign types, select Yes here</td></tr><tr><td>Is a Production Controller Required on Confirmed Orders</td><td>This will require a production controller to be set on the campaign before it can be confirmed</td></tr><tr><td>Is a Production Contact Required on Confirmed Orders</td><td>If set to yes, a production contact will be required on the campaign before you can confirm the campaign</td></tr><tr><td>Default Production Controller</td><td>This will set a default production controller for the Product Group. This can be overwritten by the Brand Setup for the customer or manually overwritten on a campaign</td></tr></tbody></table>

### Refunds

Settings on this screen will set a default Refund G/L code for the Payable and also a default vendor in our A/P module.

<figure><img src="../../../../.gitbook/assets/image (522).png" alt=""><figcaption></figcaption></figure>

## G/L Overrides

<figure><img src="../../../../.gitbook/assets/image (802).png" alt=""><figcaption></figcaption></figure>

If you have selected to Derive the G/L from Product Groups, this is where you will set your overrides by [G/L Type](../advertising-setup/g-l-types.md#\_toc17126063).

This section is used to link G/L Types to their respective G/L code.

## Email Notifications

There are several events in the system that might trigger an email to go out to one or more people. This section will set who gets notified. For each of these items, select a system user from the dropdown and click the + to add them to the list. These are the events that migth trigger an email:

* Credit Limit Exceeded - If a new campaign is entered for a customer who is over their credit limit, alert the following person(s) via email.
* High Value Campaign Entered - If a new campaign is entered over the assigned total value, alert the following person(s) via email.
* Quick Starting Campaigns / Line Items - If a new campaign or line item is set to start within the defined number of days, alert the following person(s) via email.
* Pre-Payments - If a Pre-Payment is applied, alert the following person(s) via email.
* Billing - When Billing occurs for this Group, alert the following person(s) via email.
* Confirmed Campaign Line Item is Changed - If a line item is changed on a Campaign in Confirmed (CO) status, alert the following person(s) via email.
* Confirmed Line Item is Deleted - If a line item is deleted on a Campaign in Confirmed (CO) status, alert the following person(s) via email.

#### Campaign Notifications by Status

<figure><img src="../../../../.gitbook/assets/image (219).png" alt=""><figcaption></figcaption></figure>

Enter an email address in this field if you want a notification to go to that email when a campaign is set to this status for this Product Group.

## Endemic Industry Codes

Setup the Endemic PIB / Categories for each product group, if desired. (Not commonly used these days). You may enter a list of PIB / Categories that are Endemic to your products. Orders entered against these Categories will then be flagged as endemic orders. This flag is only used for reporting. The values in the PIB to add drop down menu should be setup by navigating to the Setup -> System Tables Setup -> PIB/ Industry Setup.

## Fabsoft Invoice Forms

Not commonly used in Digital First environments. Fabsoft is a 3rd party form provider that we used before we offered the HTML based forms. This setup allows you to choose the Fabsoft template for Mailed and Emailed Invoices as well as set a prefix for invoices generated by the fabsoft forms.

<figure><img src="../../../../.gitbook/assets/image (1323).png" alt=""><figcaption></figcaption></figure>

## Group Sections and Positions

Group Sections and Positions are used in the Booking Wizard order entry method when you are using the 3rd option "Book a Display Ad." The idea in this booking method is that you want to book a group of products together using a Group Rate Card and a Group Section/Position. So for instance, you want to book section A, back page across a dozen products as a group buy. In Product setup, Section A might have been called 'A Section' in one product and 'Main News' in another product. A third product might not even have individual sections and all just fall under ROP as the section. Without this mapping of Group Sections of positions it would be difficult to book that efficiently in order entry.

In this setup, you can create sections and positions as a hierarchy, or positions without being tied to sections. You will tie this group section and position to the corresponding section/ position in individual products.

Navigate to the node “Group Sections” and search for the product group. Choose either independent positions of sections or positions within sections.

Add ID and description in the first new line. At this point, you can also edit the line using the pencil edit to connect this section to a product's defined section.

<figure><img src="../../../../.gitbook/assets/image (1217).png" alt=""><figcaption></figcaption></figure>

Click previous/next to move within the defined sections to set up all group sections.

Click ok when complete. Now this product group section is connected to the corresponding product(s) sections. Don't forget to scroll to the bottom and Save the settings.

Click the expansion icon on the left to see all the products and sections linked to the group.

<figure><img src="../../../../.gitbook/assets/image (1635).png" alt=""><figcaption></figcaption></figure>

Repeat for the node Group Positions. Only difference here is that you will select "section" at the top and then do the mapping to desired positions within that Group Section

<figure><img src="../../../../.gitbook/assets/image (1243).png" alt=""><figcaption></figcaption></figure>

## Product Group Ratecards <a href="#_toc98250957" id="_toc98250957"></a>

Ratecards are designed for Product Groups to cover Print, Digital and Classified Ad Types. Group Rate Cards _**can**_ be used in all order entry methods (Full Line, Quick Line and Booking Wizard). They are _**required**_ to be used in Booking Wizard option 3 (Book a Display Ad).

Navigate to the menu Setup -> Product Group Setup -> Group Ratecards.

<figure><img src="../../../../.gitbook/assets/image (1196).png" alt=""><figcaption></figcaption></figure>

Click New and choose the Ratecard Type. Add the line similar to entering any product [Ratecard](products/pricing-rules/). Save the Ratecard. Note that the “Only Allow this Ratecard on Packages” flag is ineffective at this point. Group Ratecards do not support packages.

Click the node “Price Adjustments” to add a price adjustments.

<figure><img src="../../../../.gitbook/assets/image (692).png" alt=""><figcaption></figcaption></figure>

Enter the details on the line and save the price adjustments.

Click the node Auto Adjustments to tie the adjustment to be automatically applied with a Group Ratecard Line.

Save the settings.

For more details on Price Adjustments and Auto Adjustments, see[ Product Ratecard Setup ](products/pricing-rules/#price-adjustments)they work similarly.
