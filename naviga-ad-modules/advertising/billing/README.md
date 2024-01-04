# Billing

## Prerequisites <a href="#_toc110515823" id="_toc110515823"></a>

#### Reconcile Actuals

Prior to running the billing for digital lines on Performance Campaigns, you will need to do the [Reconcile Campaign Actuals](../campaigns/ad-server-syncing-reconciliation.md#\_toc105408229) step under the Campaigns menu in the Advertising module. This might be done by operations or it might be done by the finance person doing the billing. This process will release those digital lines for billing.

To confirm that this process has been completed, navigate to Billing -> Campaign Billing -> Campaign Billing and select the Missing Actuals node. You want this report to be blank, which will indicate that there a no campaign lines that are missing their actuals.

![](<../../../.gitbook/assets/image (607).png>)

#### [Check for other Problem Campaigns](./#\_toc110515830-1)

#### Confirmed Campaigns

Only Confirmed campaigns will be invoiced. Whether flexible or performance types, the campaign must be in the CO Confirmed status. In most cases only Confirmed orders will run as well, though in some cases, sites to allow certain Reserved statuses to go to Plan and/or to GAM, so if you are one of those sites, ensure that all running orders are updated to CO status prior to billing so that the bills will go out. Can use the [Bulk update campaign status](../campaigns/managing-campaigns/bulk-update-campaign-status.md) for this function or can update status on the campaign as well.

#### Billing Schedule for Flexible Campaigns <a href="#_toc110515830" id="_toc110515830"></a>

On your campaign, various billing schedule options are available to accommodate user’s needs in the generation, and optionally, the automatic update of the Billing Schedule:

* Bill on First Insertion / Date: This option uses the first month or insertion / issue date as the date to bill all values. If line items are altered, affecting the total billing amount, the schedule is automatically updated based on these settings.
* Bill on Last Insertion / Date: This option uses the last month or insertion / issue date as the date to bill all values. If line items are altered, affecting the total billing amount, the schedule is automatically updated based on these settings.
* Manual: This option allows you to define a custom Billing Schedule. You can use the First Billing Date, Billing Interval and Total Billings to generate a schedule. You can also manually add and remove lines as needed. This schedule type will require that you manually adjust the billing schedule any time you make changes to the campaign that affect the total billing amount. The "Build from Lines" option is only available when using this Schedule Type, and only while there are no invoiced lines.
* Dynamic: This option uses the First billing Date, Billing Interval and Total Billings to generate the Billing Schedule. If line items are altered, affecting the total billing amount, the schedule is automatically updated based on these settings.

Enter a flexible campaign with multiple lines with different issues’ dates. For example, January and February 2021. Navigate then to the Billing Schedule node. Choose the option “Bill on First Insertion / Date”.

Note that the date immediately changes to the first issue’s date.

![](<../../../.gitbook/assets/1 (83).png>)

Choose the option “Bill on Insertion / Date”. The date automatically changes to the last issue’s date on the order.

![](<../../../.gitbook/assets/2 (87).png>)

If you add another issue, then the go to the billing schedule. Choose another option then again the option “Bill on Last Insertion/ Date” and the billing date automatically is updated to the last issue on the order as well as the total amount.

#### Invoice Templates

User must also have all [invoice html forms](../setup/advertising-setup/advertising-invoice-forms-templates-line-groups.md) setup.

## Prepare Billing Invoice <a href="#_toc110515824" id="_toc110515824"></a>

Navigate to the menu Billing -> Campaign Billing -> Campaign Billing. This will direct you to the node “Prepare Performance Billing”. If the campaign you are billing is a performance campaign, then this is the correct node. If the campaign to be billed is a flexible campaign, then click on the node below this one titled “Prepare Flexible Billing”. Both screens have the same function but slightly different search options and details in the results grid.

Click on the Configure Output tab.  Similar to other reports in the system with configurable columns, each user with access to the billing screen can choose their own preferred columns for both onscreen viewing and for export. After changes are made, click Save Configuration and click back to the selected campaigns tab to see onscreen changes.

<figure><img src="../../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (287).png" alt=""><figcaption><p>Prepare Flexible Campaign</p></figcaption></figure>

Some of these fields you can choose to search for a campaign are:

**Billing Group**, if you have setup a [billing group](../../accounts-receivable-credit-control/setup-a-r-system-setup/other-a-r-setup-menu-items.md#billing-groups) in the Setup menu in Accounts Receivable module and linked those groups to Advertisers.

**Product Group**, if you want to run the billing for all orders in a product group.

**Specific Product** , if you’d like to search within a product.

**Ad Type** to search by AD Type.

**Specific Campaign IDs**, if you know the campaign number. You can enter more than one, press return between each Campaign ID. You can also use the magnifying glass to search for the campaign instead.

Enter the date range desired. The Date Range selection works different for Performance and Flexible Campaigns.

* Performance Campaigns - Select Campaign Lines that are running within this date range.
* Flexible Campaigns - Select Campaigns that have a billing stage that falls within this date range.

You can then narrow down the search if applicable by choosing “Return Only Prepared Campaigns” or “Return Only Campaigns that are not Prepared”. This allows you to view the campaigns which you have previously run through this process but have not generated an invoice for them. This is also used when a different person prepares the billing than who runs the billing. that is why you will also see a menu item Billing -> Prepare Performance Billing and Billing -> Prepare Flexible Billing. Menu security can be such that someone only has access to prepare and someone else has permission to the full Campaign Billing menu options.

In the Pre-Payment field, you can choose to return the campaigns which are prepaid, not prepaid, all campaigns or only campaigns with a credit card to charge. Click on “Get Campaigns”.

Once the campaigns display, check the box or boxes for the invoices and then click on “Prepare for Billing”.

Do the above steps for both Performance Billing and Flexible Billing

### Edit Billing Parameters <a href="#_toc44011796" id="_toc44011796"></a>

User can edit the billing parameters in the prepare billing screen to change to any of the three available types: Print, Email or Print & Email. User can also enter the details of the invoice recipients. The changes override the settings for this advertiser only for this campaign and affect all lines billed at that time. Other lines are not affected and revert to the advertiser setup.

Click the pencil icon at the end of the line to edit the delivery options.

<figure><img src="../../../.gitbook/assets/image (1353).png" alt=""><figcaption></figcaption></figure>

Choose a different option and the system prompts you to enter the corresponding contact. For Print it is a drop-down of the billing contacts available for the advertiser and for the Email option, enter a valid email address. If you choose the option Print & Email, you can enter both. Click the Save button.

Note the change takes effect on all the lines pertaining to this campaign. This change overrides the settings for the billed lines. This is intended for a temporary change for a specific campaign. To permanantly change the Delivery information, change it in Advertiser Maintenance.

## Generate Invoice <a href="#_toc110515825" id="_toc110515825"></a>

Click on the node “Generate Invoice(s)”. Click on the magnifying glass and the prepared campaign(s) displays.

<figure><img src="../../../.gitbook/assets/image (389).png" alt=""><figcaption></figcaption></figure>

There are other fields to use to search for the prepared campaigns, some of which are:

Specific Campaign IDs - click the magnifying glass to select only certain prepared campaigns. Can leave blank to bill all prepared campaigns

Product Group for all prepared campaigns in the group.

Ad Type for a specific AD Type.

Date to Appear on Invoice: This is the date you’d like to display on the invoice for the client.

Financial Period to Post to: This is the financial period for posting, which depending on the Group Security Advertising setup generally must match the date of the invoice.

Comment to Print on Invoice(s): This comment you can type here as free text and it’ll display on the invoice for the client. (as long as the comment tag was included on your invoice template)

Live or Trial Run : The Trial Run is a test batch internal to you only and isn’t sent to the clients. The Live is the final one which is mailed to the client. You can always create a trial batch to see how the invoice looks and check for accuracy of numbers before you run a live batch. This allows you to correct any issues before the final printing. After you make the corrections, you can return to the Prepare Billing Invoice Step first before you run a trial or live batch to apply changes you’ve made.

Documents to Generate : Generate Both Invoices and Credits: You can choose to generate both invoices and credits, or invoices only or credits only.

Invoice Sort Order: This option allows you to choose how to sort the invoices, alphabetically by advertiser name, or by Bill-To Name from the campaign header or by Campaign number ascendingly.

Suppress Zero Value Invoices: IF this flag is checked, then the invoices of $0 values due to adjustments will not be included in the final printout of the batches. You can still access the PDFs of the invoices from the batch in the next screen.

Include Pre-paid Campaigns with Zero Balance: Once you check the above flag, this flag appears which allows you to also suppress the campaigns that have zero values due to full prepayment on the campaign in a similar manner to the above invoices.

Click on “Generate Invoices”. Click on View/ Print All Invoices field. A PDF invoice displays with the data in the respective fields as designed in the Invoice Forms menu. If this is a trial invoice, the system will not save it. Generate the same invoice but choose live invoice type to view the invoice, post it, and email it.

## Print Invoices and Post to AR <a href="#_toc110515826" id="_toc110515826"></a>

When the live invoice is generated, click on the node “Print Invoices” on the tree or click on the pop up screen button “Go to List of Invoice Batches”.

The screen displays the batch PDF link to the invoices with the green arrow in the “Post to AR” column.

<figure><img src="../../../.gitbook/assets/image (1042).png" alt=""><figcaption></figcaption></figure>

Click on the PDF hyperlink to view the invoice and then click on the green arrow to post to AR.

Once the invoice is posted, the green arrow changes to a black check box.

To see individual invoices instead of the batch, click the Batch number hyperlink.

<figure><img src="../../../.gitbook/assets/image (448).png" alt=""><figcaption></figcaption></figure>

### Reprocess Batches <a href="#_toc45176471" id="_toc45176471"></a>

New option on “Print Invoices” screen to reprocess batch allows user to regenerate the PDFs for the invoices and re-email any that are set to email delivery option. The option will not reset the batch or affect the invoice in anyway. It can be used if there is some interruption in the sending of the emails during the billing run.

{% hint style="info" %}
Note that if there are any changes done to the order after you generate the invoices, and if you’d like these changes to be reflected on the invoices, you must use the feature “[Regenerate Invoices](./#\_toc110515827)” for these changes to display on the invoice. **The reprocessing feature re-prints the PDFs in their prior format and with the original data without any changes made to the campaigns if invoices had been already generated.**
{% endhint %}

Once the batch is generated, navigate to the Print Invoices node, and note the batches are listed with the reprocess circular arrows available to resend the emails and generate the PDFs.

<figure><img src="../../../.gitbook/assets/image (385).png" alt=""><figcaption></figcaption></figure>

The system produces a confirmation message. Click OK.

The emails are resent, and the PDFs are regenerated.

The new billing process uses a background windows service to process the PDFs and send the emails. The process time varies depending on the number of resources. For example, it may take up to 45 minutes to process 450 invoices.

If you hover the mouse over the Batch PDF hour glass icon corresponding to the batch, the new tooltip will keep track of the number of PDFs processed.

<figure><img src="../../../.gitbook/assets/image (755).png" alt=""><figcaption></figcaption></figure>

When you refresh the screen, note that the number of invoices processed increase every few minutes.

## Generate/Download Order Data File

When Naviga Clients don't use our A/R for collections but instead do the collections in a 3rd party A/R system, they typically still do the above AR process, but then send the invoices to the 3rd party A/R System.

Occasionally, the invoices are not created in Naviga ad at all, but instead we generate an Order Data File after the Prepare Billing Steps.

<figure><img src="../../../.gitbook/assets/image (401).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Typically a site will see Generate Invoices and Print Invoices OR they would see Generate Order Data File and Download Order data file, but not both as i have in my screen. See Naviga Support if you are not seeing what you expect to see. Only Naviga personnel can switch the setting for you.
{% endhint %}

## Regenerate Invoice <a href="#_toc110515827" id="_toc110515827"></a>

The system allows you to regenerate the invoice if there is a need to do so, due to a change in the order or the advertiser’s settings.

The Regenerate Invoice function reprocesses the existing "Invoice printing data" through the current HTML Template (of matching Form ID). Therefore, it does not create a new Batch, it only creates a new result when the PDF is opened in the viewer.

Note that there is no built-in method to change the Form ID that was used for each Invoice. The Form ID is saved in the "Invoice printing data" record so the same Form ID will be used with every Regenerate. It can be changed behind the scenes, though, in case an incorrect Form is selected in the future.

Also note that there is some data that is not directly stored in the "Invoice printing data" record and so could change if the external data is changed, even if the HTML Template has not changed. For example, the saved file has an Address ID, but if the connected Address is edited then a Regenerate will pick up the new Address. In general, Regenerate is intended to be used for HTML Template changes and not data changes.

Before you regenerate the invoice, you can change the invoice template used on the Product Group. The newly regenerated invoice uses this latest template. You can change multiple fields on the order to be reflected on the regenerated invoice.

* Comments to Print on the Invoice
* Page number for print products
* PO Number
* Tearsheet if applicable
* Hard coded text in the template, for example instructions or remit address or disclaimers
* Order Contact Name

Click the node “Regenerate Invoice”, and enter the invoice ID. You may enter more than one ID.

Choose the regeneration option to use either Fabsoft, if the original invoice was generated using Fabsoft, or choose Naviga HTML forms even if the original was generated using Fabsoft.

Then click on “Get Invoices”. The invoice displays. Check the corresponding box and click on “Regenerate Selected Invoices”.

Choose the address to print on the invoice, to be the original or the current address. Click on the button to change it to “Yes” to display the watermark “Reprint” on the invoice. Or leave it as “No” to not have it displayed.

Enter a comment which will display on the invoice. Click the “Regenerate Invoices” button. The invoice is available to be viewed and printed if you search again on the invoice ID and click the PDF link.

## Reverse Campaign Billing <a href="#_toc110515828" id="_toc110515828"></a>

This process allows you to reverse all invoicing that has been done against a partially or fully billed campaign, producing a reversing credit. This will not cancel the campaign, nor will it affect any Ad Server integration. The most likely use of this function is when the wrong party was billed and now needs to be credited. After the campaign invoicing has been reversed, you can change the bill-to on the campaign entry screen and then re-bill the campaign.

## Tax Calculation Hierarchy <a href="#_toc110515829" id="_toc110515829"></a>

The system calculates taxes based on the following order. If there is no value in a step, the system proceeds to search for tax setup in the following step.

1\) Line Item Tax Override

2\) Product Tax Override

3\) Customer Default Tax Code – AD

4\) Customer Default Tax Code – AR

The flexible campaign Billing Schedule itself has an effect on how taxes are calculated. It only sets the Stage percentages based on pre-tax amounts.

## Campaigns with Problems <a href="#_toc110515830" id="_toc110515830"></a>

### Billing Schedule Issues

Flexible campaigns require that a billing schedule be completed so that the system knows when to bill the campaign and for how much. When things change with on a campaign after the billing schedule has been set up, the user making the change may need to revisit the Billing Schedule and update the billing information (especially if the schedule type was "Manual").

![](<../../../.gitbook/assets/image (593).png>)

The system prompts the user to visit the Billing Schedule and make updates, and if there is a balance that hasn't been scheduled, the balance will be displayed in red in the campaign....but if the user ignores all that, then the campaign will be listed on this screen so that the person doing the billing is aware that there is an issue.

<figure><img src="../../../.gitbook/assets/image (1006).png" alt=""><figcaption></figcaption></figure>

### Credit Issues

When a campaign is confirmed, it is checked for credit issues and the system will not allow approval if the advertiser is overdue on invoices beyond the allowed number of days, or if they are over their credit limit, if prepayment is required and hasn't been received, etc. (Certain users may be permitted in Group Security to confirm a campaign even with those issues.)

BUT - once the campaign has been confirmed, especially if the campaign is a long running campaign, issues might come up later. This report aims to bring attention to issues so that a user may proactively decide to cancel future issues if credit problems are not remedied.

![](<../../../.gitbook/assets/image (1075).png>)

### Credit Card Issues

This report will display any issues with credit cards that need to be remedied.

### Campaigns Awaiting Credits.

This report will highlight any campaigns that were cancelled and the credit has not yet been processed.
