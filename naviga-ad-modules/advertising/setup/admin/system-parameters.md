# System Parameters

Navigate to the menu Setup -> Advertising Setup -> System Parameters.

## General Settings

1. **Default Agency Commission Percent:** Enter the commission default value which would be defaulted into the agency when a new one is created.
2. **Set New Advertisers to Not Use Multiple Brands:** If set to "Yes", then when you create a new advertiser, the default for using multiple brands is set to No and a single brand will be created for the advertiser which is the advertiser’s name as a default.\
   ![](<../../../../.gitbook/assets/image (91) (1).png>)\
   If set to no, the customers will default to using multiple brands on creating new accounts and the user will be able to set here what the first brand is\
   ![](<../../../../.gitbook/assets/image (92) (1).png>)\
   Regardless of the default, this can be changed manually when creating the advertiser.\
   \
   (NOTE: See [Advertiser/Agency Import](advertiser-agency-import.md) for how this setting affects importing PIB/Industry Code)
3.  **Assign Reps at Order Entry:** When checked, on any new account, the brand sales rep will look like the screenshot below. This means that every time an order is placed, the user will be prompted to fill in the rep. An Admin or someone with access to the Brand Maintenance Screen can later assign a rep, but until that is done, the user will be prompted. If this is unchecked, at the time the account is created, there will be nothing under the Rep 1 field. At the time of first order, the user will be prompted to fill in the rep and that Rep's name will then get filled into the rep 1 field and also will be assigned as the rep on the product group of that order. Any subsequent orders will default to that rep and the user will not be prompted again.

    <figure><img src="../../../../.gitbook/assets/image (912).png" alt=""><figcaption></figcaption></figure>
4. **Revenue Recognition:** _Use Product G/L Settings_ or _Use Product Group G/L Settings._ This will determine if the revenue G/L will be set based on the Product or Product Group's settings.
5. **Tax Code to Use When a Campaign is Multi Company:** If a campaign involves more than one company within the system, choose the tax code to apply to the campaign.
6. **Line Item Sort on Forms:** The **default sort** is when the system uses the order of line item entry on a campaign to list the lines on the confirmation templates and the production reminders. **Sort by Start Date, Earliest First** sorts the lines by the start date in an ascending order starting with the lines which start on an earlier date than other lines.
7. **Automatically Match Credits to Original Invoices:** If checked to “Yes”, then when you cancel a billed campaign, the system will automatically apply the credit to the original invoice(s) when posting the invoices to A/R. If left as “No”, a credit memo invoice will be created and the credit can be manually applied to other invoices or refunded.
8. **Only Allow Selection of Production Contacts on a Campaign where the contact has an email address:** If “Yes”, then the contacts under the production contacts node of a campaign which have no email address saved in the system will not be able to be selected in a campaign. User will receive an error that an email address is required. There is an edit button to edit the contact and add an email if desired.
9. **Use the Breeze Interface:** If checked to “Yes”, then the system allows for integration between Breeze and Naviga. For more details on how to perform the integration, contact your account manager or the help desk.
10. **Naviga Forms:** If checked, it allows you to use the HTML templates in the system. This should be checked for all accounts not using the older "fabsoft forms" 3rd party forms option.
11. **Override Email from Address:** Enter the email address which appears as the sender when emailing invoices to clients. By default Invoices are emailed from the user who generates the invoices. This setting allows you to set a different from address.
12. **Flexible Campaign Deferred Period:** Use the campaign start or confirmed period allows the deferred period to be the period when the campaign starts or when the campaign is confirmed. Here is an example campaign Journal Entries node. Campaign was created in February (period 2023-02) and was confirmed in that same period. The campaign Starts in April (period 2023-04). First screenshot is with this setting set to Use Campaign Start Period. Second Screenshot is set to use Campaign Confimed Period. In both cases the first Journal Entry in the on that sets the Deferred Revenue and Deferred/Unbilled A/R

    <figure><img src="../../../../.gitbook/assets/image (1056).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../../../../.gitbook/assets/image (1032).png" alt=""><figcaption></figcaption></figure>
13. **Campaign Expense Codes:** You can choose one of two options for expenses: “Expense Codes” which are the Expense Types as defined in the Setup -> Advertising Setup -> Expense Type Setup menu. Or you can choose the Class Type as defined in the A/P or A/R module Setup -> System Tables Setup -> [Class type](../../../accounts-receivable-credit-control/invoices/#\_toc65155656). These are the expense codes added to a campaign in the Campaign Budget. If you are using the Job Costing / Production Module to set up Production Jobs and linking them to the campaign for the expenses, you might want to choose Class Type here. If you are not using the Production module, you might prefer the Expense type option.
14. **Allow Partial Pre-Payments When Pre-Payment is Required:** Setting this option to YES will allow orders with pre-payment required to accept any pre-payment value. Setting this option to NO will require that orders requiring pre-payment receive pre-payment in full before the campaign can be confirmed.
15. **Booking Wizard Status Cut-off:** When line items are created through the Booking Wizard, the recipe used to create those lines is saved, and subsequently editing any related lines will be done again through the Booking Wizard, until the order has started to bill. Once billing has started the lines must be edited individually in full line entry. Leaving this blank or selecting "Invoicing Started" as the cut-off will continue this default behavior. Selecting a different status here will allow you to adjust at what point in the campaign lifecycle a line is no longer edited through the Booking Wizard, but instead in full line entry.
16. **Allow Email Invoice Delivery Method Without Billing Contact on Customer Setup:** This flag when checked the system allows you to choose an email invoice delivery method to be set on the advertiser account maintenance screen even if there is no billing contact on record for that advertiser.

## Font Size Restrictions

1. If you check the flag “Allow Only Custom Fonts”, then your uploaded custom fonts will be used and not the default fonts. Naviga Support or your implementation specialist can assist with uploading your custom fonts.
2. This section determines the font size to use on Classified Liner Ads in order entry. Move the desired fonts from left to right to create the restrictions or leave all in the left column to make them all available.
3. Default Font Size: The default font size is 10pt. If you would like to set it to something other than 10, select it from the dropdown here.

## Renewal Settings

These apply when renewing an expiring campaign.

1. Override Email Address: If this field is filled in with a recipient, then the system will use the email address(es) entered to replace the customer email address(es) for renewal emails. This should only be populated during testing. In a normal production environment you would send renewals to the customers.

## Invoice Settings

1. **Override Email to Address:** If this field is filled in, then the system will use the email address(es) entered to replace the customer email address(es) during live billing runs on Invoices with Delivery method set to Email or Print and Email in Campaign Billing. This should only be populated during testing. In a normal production environment you would send invoices to the customers.
2.  **Replacement Text on Invoices:** Only campaign lines marked to use this option apply the text entered here to the price on an invoice for this line. Screenshots below show sample invoices with and without the replacement text, as well as the field on the campaign to trigger this behavior.

    <figure><img src="../../../../.gitbook/assets/image (860).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../../../../.gitbook/assets/image (1186).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../../../../.gitbook/assets/image (1411).png" alt=""><figcaption></figcaption></figure>
3. **Email Invoice Subject Line:** Enter text as well as some HTML tags in the subject line which the bill recipient sees in the email sent regarding their invoice. For example: Your Order: #INVOICE\_ID#
4. **Email Invoice Body:** This is a template which can contain text and the invoice mapped fields which your client views displayed in the body of the email when you send them invoices.
5.  **Create a separate Invoice Batch for each Product Group:** Check flag to activate this option to separate product groups in batches when billing. If set to yes, there will be an extra column for product group on the Print Invoices screen:

    <figure><img src="../../../../.gitbook/assets/image (283).png" alt=""><figcaption></figcaption></figure>
6. **Separate G/L Posting for each issue/month billed on an invoice:** Check the flag to activate this to separate the posting to the General Ledger for each issue or month being billed. For example, if you have multiple issues in a campaign in a single invoicing run, when you run the billing, if this is set to "No" you will get one G/L Entry for the line. If this is set to Yes, you will get multiple G/L Entries.\
   Example with "yes" :\
   ![](<../../../../.gitbook/assets/image (682).png>)\
   Same order as above, but with "no" :\
   ![](<../../../../.gitbook/assets/image (1495).png>)
7. **Derive Period from End Date:** Check the flag to derive the period to post the invoice from the line item end date. For example, if a Line Item is 11/01/22 through 11/30/22, then a NO setting on this flag will look up “11/01/22” on the Financial Period Setup table and a YES setting on this flag will look up “11/30/22” on the table.
8. **Use Separate Counter for Credits:** Check this option to create separate counters for credits issued.
9. **Calculate early pay discount before taxes:** When checked as “Yes” then the system calculates the taxes on the discounted amounts paid early.
10. **Use G/L Type Override First:** When this flag is unchecked, and its value is “No”, the Product Setup G/L Overrides work in this order:
    1. Industry Code Overrides, then
    2. G/L Type Overrides, then
    3. G/L Defaults and then
    4. The Product’s G/L Defaults in the Product Details screen.\
       When this flag is checked and its value is “Yes”, the Product Setup G/L Overrides work in this order instead:
    5. G/L Type Overrides, then
    6. Industry Code Overrides, then
    7. G/L Defaults and then
    8. The Product’s G/L Defaults in the Product Details screen.
11. **Validate Registered Company Number:** If this flag is checked, the system validates the “Registered Company No.” against the ELMA Registry. The Electronic Recipient Address Register is a Norwegian register recording the recipients of the various EHF formats.

## Material Settings

1. **Option to Create Copy of Material when Attaching to Order:** When checked, this prompts the user in campaign entry when attaching materials to the line item to make a copy of the existing material and use a new ID or attach the existing material with the existing ID. If this is not checked then the system attaches the existing material and its ID to the order. User can proceed to edit the material in either case in the line item entry screen.
2. **Consolidate New Material Records by Size:** If checked, then for Ads with the same size, will all use the same Material Id. This applies to the Quick Line entry when the product is set to auto-create material and also set to split lines.

## Salesrep Settings

The rep settings allow you to choose settings for the rep commissions:

1. **Rep. Commissions - Post Zero Amounts:** If checked then when the system updates the Sales Rep commission file, do you want to include any lines that have zero amounts? Examples of zero lines – make goods, production charges.
2. **Rep. Commissions - Show Rep Amounts:** When checked, the Rep Commission screen, do you want to include the columns that show the Rep’s commission percentage and calculated commission amount? If you do not calculate commission based on a straight percentage then these may not be useful to you.

## Inventory Settings

The inventory settings apply to impressions inventory on a cost per ad type:

1.  Quoted % Counted Against Available Impressions: Move the marker to apply the amount you’d like to count against the orders in Quote status.

    <figure><img src="../../../../.gitbook/assets/image (305).png" alt=""><figcaption></figcaption></figure>
2. Reserved % Counted Against Available Impressions: Move the marker to apply the inventory amount against orders in the Reserved status.

Both of the above settings determine how much inventory is displayed when booking orders against that inventory. For example, assume that my inventory for a given item in a given month is 100,000 impressions. If i have the above settings selected and i book a campaign in _**Quote status**_ for 100,000 impressions, the next time i book an order for that same inventory, it will appear as if half are gone and I have 50,000 impressions left to sell. Note that orders with inventory booked in the confirmed status always have the inventory counted against the available inventory at 100%.

3. Newsletter Inventory Status: This is similar to the website products where it allows you to count inventory if the order is in the Reserved or Confirmed Orders Hold Inventory.
4. Print Inventory Status: You have the option here to hold the inventory only when an order is confirmed or when an order is Reserved or Confirmed.

## Sponsorship Inventory Colors

Choose the colors which display on the Sponsorship Inventory Report for background and text color.
