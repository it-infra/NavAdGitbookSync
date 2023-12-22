# Group Security (Ad)

There are some very complex controls around who can do what in the Advertising module. This section covers both the "Advertising Security" and "Production Workflow" nodes on the Group Security Screen.

For easier navigating, the Advertising Security node has sub-groups under it and each item is numbered. Choose the group ID from the drop-down menu and view the description matching it.

For Information on Group Security for other Modules, see the respective module documentation or [System Settings Group Security](../../../system-settings-admin/security/group-security.md)

## Advertising Security

### Status Codes

1. **Default Status on New Campaigns:** Choose the default status on a new campaign when the user creates one in the campaign entry screen. Or leave option blank to allow user to choose any status during entering an order.
2. **Default Status on New Campaigns when Pre-Payment is Required**: If prepayment is required as a setup option on the Advertiser Maintenance screen, then the Confirmed status is not immediately available when creating a new campaign. Campaign Entry status will default to the first available Status Code. Setting this option will override the default in security flag above by selecting this status code when prepayment is required and Confirmed status is not yet allowed.
3. **Auto Pay Cash on Account when Confirming Campaigns**: If checked, the system applies Cash on Account automatically when confirming campaigns using Bulk Campaign Update utility. This is when the client is NOT set to require Prepayment in advertiser maintenance screen. Clients who are set to require Pre-payments, Cash on Account will be automatically be applied in the Bulk Campaign Update utility. This setting can be used if you often have customers where prepayment is entered as cash on account prior to any campaign or invoice being created.
4. **Disallow Confirmed Status when renewing a campaign** - This flag will prevent certain users from being able to select "confirmed" status during campaign renewal. The reason you might want to set this status to "yes" is that the renewal process simply copies the lines on the campaign for future dates. It doesn't do all the sophisticated inventory checking that would normally be done in Full line entry or quick line entry. So preventing the user from setting the status as confirmed will allow the inventory checking to be done separately before then manually updating (or via bulk update status screen) the status to confirmed.
5. **Restrict Status Codes:** Click on the code you want available and move to the right side by clicking the right arrow into the allowed table. This will restrict the user not only from Creating a campaign in that status, but also prevent them from editing a campaign in that status.

### Reports

1. **Available Ad Reports:** Click on any number of the reports to move to the allowed table on the right side where the user can view these reports in the home page.

{% hint style="info" %}
This setting will only remove reports from the advertising home screen shortcut. Full restriction report access should be disabled via menu security. The reason for this is that one may choose to remove reports so as to provide a cleaner shortcut list on the home screen, which still allowing access to the report thru the menu system.

This list of reports is also offered to CRM users who are using the CRM Main Menu system using the Reports navigation icon.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/image (568).png" alt=""><figcaption></figcaption></figure>

### Client Approval Requirements

1. **Prevent Opportunity Creation if Account is not Approved**: If set to “Yes”, this setting would disallow these users from creating Opportunities for unapproved clients
2. **Prevent Order Creation If Account is Not Approved**: If set to “Yes”, this setting would disallow these users from creating confirmed orders for unapproved clients.
3. **Prevent Quote Creation If Account is Not Approved:** This setting if “Yes” would prevent this group’s users from creating quotes / proposals for unapproved clients.
4. **Prepayment Required on New Customers**: If set to “Yes”, then users in this group would not be allowed to confirm orders for newly created customers without first applying a prepayment. This doesn’t apply to existing customers. This may be useful if you do not wish to set a customer as requiring prepayment for all lines of business.
5. **Allow Account Approval In Campaign Entry**: If checked, system will redirect user from campaign confirmation screen to approve account before being able to confirm the campaign.

### Discounting & Campaign Approvals

1. **Proposals Require Approval by Manager Before Sending:** This option when checked would prevent order entry user from generating a PDF confirmation of the campaign to the client. Once approved by the manager, the system displays the node for user to generate the confirmation. This flag is related to the next three items (#2 - 4. if this is set to No the next items will be grayed out.)
2. **Only Proposals Over this Value Require Approval:** Enter a $ amount as a threshold above which proposals of this amount would require approval by a manager. Proposals with less than this amount will not need approval. 0.00 in this field means ALL proposals will need approval. A blank in this field will mean there is no value that would cause the proposal to require approval.
3. **Proposals must be Approved if this Percent Discount on any Line Exceeds a certain amount**: This restriction is on the line item if there is a discount exceeding this amount you enter which will trigger an approval required status of the campaign.
4. **Proposals must be Approved if this Average Discount Percent is Exceeded on a Campaign:** This restriction is a restriction on a discount you place on the campaign in total, which then requires approval.
5. **Maximum Total Discount:** Enter a percentage discount value for the maximum allowed. This regardless of approval settings, restricts maximum total discount user can enter per line. Note: leave blank to allow any discount, including the ability to enter negative lines.
6. **Auto Adjust Over Applied Incentives:** When updating or deleting lines, this option will insure that applied incentives still qualify - and if not will remove them. Note: This cannot remove applied incentives to billed orders.
7. **Auto Adjust Over Applied Incentives only for these status codes:** If you would like to auto adjust incentives, but only for certain status codes, select those status codes here.

### Campaign Header Security

1. **Allowed to Create New Campaigns** - If set to no, users will be allowed to view or edit campaigns but disallowed from creating new campaigns.
2. **Allowed to Edit Campaigns** - If set to no, this setting would provide view only access to campaigns and prevent all editing.
3. **Allowed to Cancel Campaigns** - if set to no it restricts ability to cancel existing campaigns.
4. **Default Campaign Type:** Default Performance or Flexible. Users can overwrite default in campaign entry.
5. **Allowed to Change Advertiser on Campaign -** Option will allow or prevent a user from changing the advertiser on a campaign.
6. **Allowed to Change Original Reps** - The system tracks the original rep assigned to the order at the time of order entry. It would be unusual to change the original rep unless it was entered in error.
7. **Allowed to Change Current Reps** - The original and current rep would be the same at the time of campaign entry. If allowed to edit this field one could change the rep currently responsible for the campaign (without necessarily changing the original rep).
8. **Allowed to Change Agency on Campaign:** The agency defaults into campaign entry from the brand, this setting would allow for an overwrite for the selected campaign only. The percentage commission should also be updated on the pricing as a result of changes to the agency.
9. **Allowed to Change Terms on a Campaign:** These are the payment terms on the campaign.
10. **Allowed to Change the Billing Contact on a Campaign:** This provides the ability to overwrite billing contact/billing address at the campaign level.
11. **Allowed to Create New Advertiser in Campaign Entry:** This restricts ability to create advertisers directly from campaign entry screen. Users restricted on this screen may be able to create advertisers elsewhere. (User also must be setup as Sales rep with assigned reps to enable this option).
12. **Allowed to Create New Brand from Campaign Entry:** Restricts ability to create a new brand on the campaign entry screen. Inability to create a brand would prevent users from entering campaigns for customers that had not been set up for advertising.
13. **Allowed to Set/Change Default Campaign Discount Percent on Brand Maintenance:** If this option is set, then user can set or change the existing default campaign discount percentage from the brands maintenance screen for a brand. Users may be allowed to create/edit other brand information without being allowed to set a default discount that would automatically apply to all campaigns for the brand.
14. **Allowed to select digital product groups that do not have Rep Assignments setup on the selected Brand:** If set to “No”, the user would not be able to enter campaigns for first time advertisers. If set to “Yes”, then in the campaign entry screen, user will be able to select a digital product group which does not have a rep assigned to it in the Customers menu -> Brands -> Brand Maintenance -> Rep assignment node.
15. **Set New Brands to Assign Reps in Order Entry:** If you do not have default Salesreps, select this setting and the system will require that the campaign entry person select a rep every time they enter a campaign.
16. **Save New Rep Assignments Made in Order Entry to the Brand:** If this option is checked, then the system will save this rep assignment to the new brand which was created in the campaign entry screen. If the option is not checked, then this rep assignment to this brand will not be saved in the system, and moving forward, user will have to re-assign a rep to this brand in every campaign entry order. This option will save the selected Rep Assignments made in Order Entry back to the Brand as the Product Group override, if either:

    i. The selected Brand was created either through Brand Maintenance or through an import, and the brand has no Default Rep Assignment and no matching Override Assignment for the Web Group

    ii. Or if the "Allowed to select Product Groups that do not have Rep Assignments setup on the selected Brand" is selected, and you select a Product Group that does not have a Rep Assignment, and the Brand has no default Rep Assignment.
17. **Allow Entry of Campaigns with Start Dates Before Today:** These campaigns can’t be sent to Google Ad Manager and can’t be sent to NavigaPlan. This option is designed as an alternative, for billing purposes, to fixing errors for campaigns that have started but have not been created in the system.
18. **Allow Confirming of Campaigns with Line Items in the Past**: If set to “Yes”, then user has the ability to confirm campaigns if any line items on the campaign have a start date prior to today.
19. **Prevent Campaign Confirmation if Credit Checks Fails:** When confirming a campaign this setting would validate customer credit limit or customer past due invoices or as per the Advertiser Maintenance -> A/R Settings screen settings for either fields: “Credit Limit” and “Credit Stop Days (Ad)”. The system checks also for the balance plus the confirmed unbilled balance. The order of checks if the “Bill-To” has an overdue balance as follows:

    a. If the Bill-To has a credit limit then,

    b. it checks if the Bill-To A/R balance exceeds the credit limit,

    c. it checks if the Bill-To (A/R balance + unbilled confirmed campaign balance) exceeds the credit limit.

    Note that the system checks for item b. if it passed the check in a. The system provides a warning message and won’t show the Confirm option for the campaign.
20. **Allowed to Change the Campaign Type on an Unbilled Campaign**: This setting determines if users can change an unbilled performance campaign to flexible, or an unconfirmed flexible campaign to performance. Once invoices or journal entries have been created the campaign type can’t be changed.
21. **Allowed to Enter Pre-Payment:** If checked to “Yes”, users in this group are allowed to assign pre-payments to orders on the campaign entry screen.
22. **Allowed Payment Types:** Credit Card, New Check, Cash on Account, Trade and so forth. You can choose one or more payment types. If left blank, all methods of payment are allowed.
23. **Allow Overpayment when paying by check** - will allow for overpayment on campaign pre-payments- where the overage will be left as Cash on Account. (The use case for this is when someone mails in their ad along with their check and the check amount is too much).
24. **Allowed to Override Currency on a New Campaign:** When a customer is set to bill in a certain currency, the currency will default on to the campaign header. If set to “Yes”, user can edit the currency on a campaign header.
25. **Require Order Contact:** If set to “Yes”, then user must select an order contact on the campaign header. The billing contact will default from brand set up.
26. **Allowed to Change I/O Flag on campaign:** If set to “Yes”, then users can change no/yes setting on campaign header that indicates if insertion order has been received.
27. **Default Billing Schedule:** Billing schedules can be set to the following options but user can still override these options on the campaign entry screen:

    \--> Dynamic to auto-calculate the amount for each billing based on campaign total, number of billings and frequency of billings. If campaign totals change after billing is set, then system will automatically re-calculate.

    \--> Manual billing schedules allow the user to enter amounts for each billing. This selection requires user to adjust billing if campaign total changes.

    \--> Bill on First Insertion Date: Billing is set to be on the date of the first line’s date.

    \--> Bill on Last insertion Date: Billing is set to be on the date of the last line item’s date.
28. **Allowed to Recognize Revenue in a Single Period on Flexible Campaigns:** To follow GAP accounting rules, we do not recommend setting this to yes. If checked this option will allow users to post the revenue on one financial period for revenue recognition during that period, and not have to be spread across financial periods that match the billing cycle.
29. **Disable Text Editing on Order Confirmation Form Emails:** If set to “Yes”, then user cannot edit the text of the confirmation form being emailed to the client when generating the confirmation. If set to “No”, then user will be able to edit the text.
30. **Restrict "Pay Now" and "Pay Later" Options:** depending upon your selection, user will see the Pay Later option on payment window in the invoices & payments node of a campaign, meaning that the payment will be processed at the time of billing. OR they will have the Pay now option displayed, meaning the payment is processed immediately upon entering the payment information OR they will have both options available and can choose based on the clients wishes.
31. **Allow Auto Payment Option on Campaign Header:** This is the “Auto Payment Method” which allows user to choose from the drop-down menu the credit card payment on file for example. This allows the card to be charged when prepayment and billing take place.
32. **Allow Rep Commissions Greater than 100%:** If set to “Yes” user can allocate more than 100% for a Salesrep. This same security is also used on Brand Setup to determine if the sales rep split % is allowed to be > 100%.
33. **Require Campaign Description:** If set to “Yes”, then the campaign header must have a value entered in it.
34. **Allowed to Ignore/ Override Prepayment Requirements:** When this is checked to Yes, the system allows user to confirm a campaign even if prepayment is mandatory and no confirmation is allowed unless campaign is prepaid.
35. **Allowed to Add Attachments even if you are not allowed to update the campaign:** Set this option to YES will allow users in this group to add attachments to a Campaign even if they are not allowed to edit/update the Campaign

### Campaign Line Security

1. **Require Ratecard Selection for Pricing:** If set to “No”, then users in this group will be able to select size from price table, G/L type from dropdown and enter any pricing without a Ratecard in the line item. If set to “Yes”, then a line item must have a Ratecard to select the pricing.
2. **Disable G/L Type Selection/ Override in Line Entry:** If set to “No”, then users in this group will be able to change G/L codes on line items in campaign entry. Otherwise, the G/L selections default from the product setup.
3. **Allowed to Override Tax Code on a Campaign Line:** This can be set to “Yes”, if some line items are taxed at a different rate than others, user may need to manually adjust taxes at the line item level in campaign entry.
4. **Do Not Allow Changes to Past Month Allocations on Flexible Campaigns:** If set to “Yes”, users in this group will not be able to edit line detail for past months. This is to restrict changes to revenue allocations that occur in the past.
5.  **→ Default Proportion By:**

    a. The system default recognizes revenue proportionally by day.

    b. Default by monthly would use same amount each month even if campaign runs limited number of days in any month.

    c. Custom setting requires user to select proportioning. For example, this may be used for an accelerated online campaign. For performance campaigns these choices will set billing and revenue recognition. For flexible campaigns these choices govern revenue recognition as billing is controlled by the billing schedule.
6. **Disable Custom Allocations on Line Entry:** User can disable the “Custom Proportion By” option in Line Entry. This prevents users from selecting this option to put all the revenue on one line versus another to manipulate the system to generate commissions at a certain time.
7. **Disable Amount Changes to Custom Allocations -** This only applies to Digital lines using Ad Types where a Qty is specified on each month container. This option will effectively only allow the user to change Quantities with the Custom Allocation option.
8. **Allowed to Enter Orders in Closed Issues:** Print product setup allows for entering closed date and time of issues. If this is set to “No”, these users won’t be able to enter orders after close date/time (deadline) is set.
9. **Require Audience Selection on Date-Based Product Lines:** For e-newsletters the system allows you to select an audience. This can be used to default in CPM and to control the number of emails subscribers receive. This setting if set to “Yes” makes audience selection mandatory.
10. **Do Not Allow Section and Position Changes If They are Set from a Ratecard Selection:** Sections and/or positions can be set on Ratecard lines for each line. IF this is set to “Yes”, then users won’t be able to change the position and section tied to a particular size/price on the line item. The values will be defaulted in the line item.
11. **Display Warning Message When Entering Duplicate Issue Date in Full Line Entry:** If checked, user will receive an alert if duplicate issue is selected on an order for the same line item, by mistake. During line item entry, the system will prompt user to click OK to continue or cancel. If user continues then a duplicate line item is created.
12. **Allow Removal of Auto Adjustments** – Even if The Rule is to Disallow Removal: If set to “No”, then the user’s ability to remove Auto Adjustments is determined based on the rule set on the Auto Adjustment in Product Setup.
13. **Disable Discount Percent on Quick Line Entry:** When checked, this will disable the Discount Percent field at the top of the grid in Quick Line Entry where user can edit the discount on this line. If a discount is defaulted into this field as a result of the campaign header default discount, it will still be reflected here and used, but the user will not be able to edit or change it.
14. **Lock Ratecard and Extended Rate textboxes in Quick Line Entry:** When checked, this option will disable the Ratecard Rate and Extended Rate textboxes in Quick Line Entry so user cannot edit the rate amount on a line.
15. **Prevent Changes to Past Dates and Issues on Line Edit** - When this option is set to YES, users in this security group will not be allowed to change Start/End dates where either date is in the past, or delete issue lines with past dates. This applies only to Confirmed and Reserved orders.
16. Prevent Changes to Material Records and Material Assignments in Line Entry - When this option is set to YES, the user will not be able to Add, Attach or Edit material records on a line item in Campaign entry.
17. Display a Warning before Saving a line edit that results in a price change - If set to yes, in Full Line Entry or Booking Wizard, if the price has changed since you opened the line, you will be warned.
18. Disallow the following options in the booking wizard: If you would like to prevent certain user groups from choosing one or more of the booking wizard options, select the ones to disallow here:

    <figure><img src="../../../../.gitbook/assets/image (1519).png" alt=""><figcaption></figcaption></figure>

    * If there are two or more selected, the user will be prompted to pick which method to use
    * If there is only one allowed option, then the window will simply open into that option
    * If you disallow all three booking wizard options, then the booking wizard button in order entry will disappear completely.
19. Prevent Changes on Material attached to Past Order Lines - By default, this will be set to no. For any user groups you set this as "yes" - the user will not be able to change material assignments for insertions with publishing dates before today. Similarly, they will not be able to edit a material record if there are past issue dates on it. To make edits for future runs, users will need to make a copy of the older material for the future dates. Then they will be able to make changes to the new material.

### Campaign Billing Security

1. **Only Allow Invoice Generation of Campaigns If Prepared by the Same User:** If multiple users will prepare billing and generate invoices this setting prevents a user from billing campaigns prepared by someone else.
2. **Allow Posting to A/R:** After invoicing, invoice batches should be posted to A/R. This setting when set to “No” would allow users to bill but prevent them from posting invoice batches. If set to “Yes”, then the users can also post batches to A/R from the billing menu.

### Naviga Inventory

1.  **Validate Sponsorship Inventory:** This option allows the users in the group to validate the available sponsorships in 3 ways:

    a. Allow Overselling of sponsorships and leave it up to the user to handle the overselling.

    b. Allow the Overselling but at the same time alert the user by displaying a warning that the inventory is being oversold and is exceeding the allowed amount.

    c. Do Not Allow Overselling by preventing the user from saving the order.
2.  **Validate Impression Inventory:** This option allows the users in the group to validate impressions by comparing to the available inventory in 3 ways:

    a. Allow Overselling of impressions and leave it up to the user to handle the overselling.

    b. Allow the Overselling but at the same time alert the user by displaying a warning that the impression exceeds the available allowed amount and is being oversold.

    c. Do Not Allow Overselling by preventing the user from selling the impression.
3. **Allow Impression Oversell by %:** This option allows the user to drag the blue bar to determine the overselling cap percentage allowed. This percentage can be anywhere from 0% to 100%.

### Google Ad Manager Inventory

1.  **Validate Google AD Manager Inventory When Using a Template or a Rate Line with Google Targeting:**

    a. Allow Overselling of sponsorships and leave it up to the user to handle the overselling.

    b. Allow the Overselling but at the same time alert the user by displaying a warning that the inventory is being oversold and is exceeding the allowed amount.

    c. Do Not Allow Overselling by preventing the user from selling the order.
2.  **Use which number for validation:**

    a. Available Units: The total available units are used to validate the numbers.

    b. Possible Units: The total units that could possibly be used would be used to validate the numbers.
3. **Allow Impression Oversell by %:** Decide the percentage by which to allow the overselling of impressions for a digital product.
4. **Default Digital Delivery View Option:** View Timeframe: Choose the value which would default the view timeframe in CRM and campaign delivery screen. These can be: This Month or Full Length of Lines.
5. **Check Inventory on Line Update:** If this is set to Yes, it will check inventory when user updates lines in addition to when adding new lines.
6. **Disable GAM Options:** If set to Yes, this will prevent editing on the GAM targeting and Expected sizes tabs in Campaign Full Line Entry.

### Other Settings

1. **Allowed to Access Setup Screens:** If this is set to “Yes”, then users are allowed menu access to setup screens. If set to “No”, users will have view only access to some setup screens and others will not display at all.
2.  **Currency Tracking Display Options:** For systems using multiple currency displays, this controls which currencies the users can see. These can be:

    a. **Display all Tracking Currency Options:** This will display all foreign currency tracking options with no limitations including amounts in current exchange rate, in budget exchange rate and in exchange rate on the order.

    b. **Display Only Budget Currency Options:** This will show the option in reports to view the amounts in the exchange rate which is set for a foreign currency in the currency maintenance screen.

    c. **Do Not Display Currency Tracking Options**: This will remove any ability to track the currency on any screen if the user has no use for tracking foreign currency.
3. **Only Create Campaigns Inside Salesforce Workflow:** This feature will restrict campaign add/edit access to only work via the Salesforce.com Canvas integration. This may be used in cases where Salesreps have access to the full Naviga Ad system directly and through Salesforce.com and it is desired that they only manage orders through the Salesforce integration.
4. **Require Client Type on New Accounts:** When checked user cannot save a new advertiser without entering a new Client Type.

## Production Workflow

This node determines the security of production workflow in the Ad Module which handles the materials on orders as well as the third party preflight settings.

Choose the group from the drop-down menu to setup.

### Material Settings

1.  **Suppress Prompt to Create New Material Record when Saving Changes** - When changing a material record, the system can prompt if these changes should result in a new material ID being created or if the system should update the existing Material ID. Selecting "yes" here will suppress that message and the system will simply save the existing material. This is what the prompt looks like (will only see the second two questions if you answer yes to the first):

    <figure><img src="../../../../.gitbook/assets/image (295).png" alt=""><figcaption></figcaption></figure>
2.  **Require Material Description** - On the material record there is a Material Description. Setting this to yes will require the user to fill in this field before saving

    <figure><img src="../../../../.gitbook/assets/image (1095).png" alt=""><figcaption></figcaption></figure>
3. **Require Ad Headline** - See above screenshot. The Ad Headline will be required if set to yes.
4.  **Require Creative Type** - This is for a digital creative. When sending campaigns to Google, a Creative type is required, so you can choose in Naviga ad to also make it required if you are sending materials to GAM. This is a Group Security setting, so you might choose to require it of a Production type user but not Sales if production will always be doing a final check of the creatives prior to the order being send to Google.

    <figure><img src="../../../../.gitbook/assets/image (852).png" alt=""><figcaption></figcaption></figure>
5. **Require Click URL** - See screenshot above. Same is true with Click through URL

### Preflight Settings

**Preflight Status Restrictions** - In the Material Trafficking report (Production -> Material Trafficking) there is a filter at the top where you can search for materials by Preflight Status.

<figure><img src="../../../../.gitbook/assets/image (228).png" alt=""><figcaption></figcaption></figure>

The settings that you set here in group security will dictate which Statuses you DO NOT see in that report.

<figure><img src="../../../../.gitbook/assets/image (787).png" alt=""><figcaption></figcaption></figure>

### &#x20;<a href="#_toc79061561" id="_toc79061561"></a>
