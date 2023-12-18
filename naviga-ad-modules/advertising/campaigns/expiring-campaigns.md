# Expiring Campaigns

There are two primary ways of renewing or copying ads in the system. One way utilizes the Quick Line Entry campaign screen and **can only be used for Display and Digital type ads** and the other way is the "Renew this Campaign" function in the edit menu on the Campaign header, which can be used for any type of ad, including liner ads.

## Run Until Cancel <a href="#_toc51353214" id="_toc51353214"></a>

User can mark a campaign as “[Run Until Cancel](creating-campaigns/#run-until-cancel)” to allow user to include this campaign in the expiring campaigns list so that user can have a chance to renew it as needed. These campaigns are also sometimes referred to as “TFN” and “Till Forbid”. This Run until Cancel flag will not automatically renew the ads, but rather make it easy to find so that when needed, someone might come in and renew these ads. They might check, say monthly, to see if anything is expiring next month that needs to be renewed. Each campaign can run for up to two years, so any one TFN campaign will not need to be renewed very often.

Navigate to create a new campaign and note the button “Run Until Cancel”. Click it to include this campaign in the list of campaigns that are eligible to expire in the Expiring Campaigns screen.

![](<../../../.gitbook/assets/1 (56).png>)

Save the campaign. Navigate to the menu Campaigns -> Expiring Campaigns.

## Renew Expiring Campaign <a href="#_toc61858165" id="_toc61858165"></a>

Navigate to the menu Campaigns -> Expiring Campaigns.

Enter the Product Group in the drop-down menu and enter the start and end date range during which the campaigns expire. Check the boxes to exclude campaigns in the Quote status by setting this flag to “Yes”. This eliminates campaigns that are still in Q status from displaying in the list. If you leave the flag as “No”, then the data set will include campaigns in the Quote status. Check the box “Unbilled Only” so that if the flag is set to “Yes”, then the data set will include campaigns which haven’t been billed. If you leave the flag set as “No”, the data set will include both billed and unbilled campaigns that fall in the previous criteria.

Click the button “Only Run Until Cancel” in the query if you’d like to include the campaigns marked as such. Click on “Get Data”.

<figure><img src="../../../.gitbook/assets/image (728).png" alt=""><figcaption></figcaption></figure>

The results shows are ALL CAMPAIGNS matching this criteria. So this includes both Display/Digital campaigns as well as liner type campaigns. Before renewing, it is important to click on the Campaign ID to open it up and look at the lines you are about to renew.

If your campaign is a Display type ad and or a Digital type ad, you can now click the “Renew” button on the campaign and the renewal pop-up screen displays for you to set the conditions and details of the renewed campaign. This opens the Quick Line Entry screen with the line items displayed. Edit the Start/End dates or rates as needed and then renew the ad.

If your campaign contains a liner type ad, do **NOT** renew from this screen. Select the campaign ID to open the campaign in a new tab and then Renew with the "Renew this Campaign" option on the campaign header.

The results display the campaign ID, description, advertiser information, order status, and the date range of each campaign.

Click the expansion arrow to reveal additional future campaigns for this advertiser. This is meant to show you what else the advertiser has upcoming so you can see if perhaps they already renewed this campaign. This would typically be more helpful for our magazine clients where an advertiser isn't typically running multiple different campaigns in the same publication. For our newspaper clients, an advertiser like a Real Estate company is very likely to be running different ads regularly and seeing the future ads wouldn't be quite as relevant.

![](<../../../.gitbook/assets/3 (34).png>)

### Renew Display/Digital Ads <a href="#_toc61858166" id="_toc61858166"></a>

The renew button from the Expiring Campaign Screen provides you with the line items on the old campaign with dates modeled after the existing dates. For example, if the campaign runs for 10 months, the renewal dates default to start the day after expiration with 10 months duration. But the system allows you to edit the dates, delete lines you don’t want to renew and edit details of the line item based on available inventory. If the date expired is in the past, the new default start date is today’s date. If the product is a date-based issues product, the system allows you to multi-select issues as applicable for renewal.

Click “Renew” on one of the campaigns.

{% hint style="info" %}
IMPORTANT: Only use this method for Display and Digital type ads
{% endhint %}

![](<../../../.gitbook/assets/4 (16).png>)

A pop-up screen with the renewal start date based on the end date of the expiring campaign displays. You can edit the start date as you please. Click OK.

The line item appears for you to edit all its details.

![](<../../../.gitbook/assets/5 (3).png>)

Click “Create Renewal” when finished. Then continue to enter more details in the new pop-up screen.

![](<../../../.gitbook/assets/6 (29).png>)

Enter the description, new status and check the flag to copy the targeting, material and line details. You can also leave the flag unchecked and edit the line as applicable. Click “Create Renewal”.

![](<../../../.gitbook/assets/7 (12).png>)

The screen refreshes back to the expiring campaigns screen and displays the expired campaign as well as the renewal campaign. Note that the number of renewals column is now incremented by 1.

### Renew any ad type

The second option is what you must do for Liner type ads, but this second method is ok to use for any ad type.

If you are doing outbound calls to inquire if an advertiser would like to renew, or if you are renewing the TFN type ads, then start with the Expiring Campaign reports, but instead of clicking on the renew button described above, click on the Campaign ID and in the top right corner of the Campaign header, select "Renew this Campaign"

<figure><img src="../../../.gitbook/assets/image (1595).png" alt=""><figcaption></figcaption></figure>

You will be prompted for a renewal start date and a Status for the New Campaign.

<figure><img src="../../../.gitbook/assets/image (1397).png" alt=""><figcaption></figcaption></figure>

In the above example, the original campaign had an end date of 11/1/2023, therefore the default renewal start date is the following day Nov 2, 2023. The system will attempt to be clever with the dates for the campaign lines. For example, if the campaign started on the 1st, but one of the lines started 10 days later, the renewal for that line will also start 10 days after the campaign start. So be sure to keep that in mind when creating the renewals. You might need to tweak the lines if you want a different pattern for the renewals.

## Sending out renewal notices

For our clients who are using the Client Portal, you can generate email notices for expiring campaigns in bulk, and in turn your customers can choose which campaigns to renew. If the user is a Portal user, they will receive an email with the link and sign the contracts from the Naviga Advertiser Portal. If your client is not yet a portal user, you can either filter out those users and not send them a link, or you can provide instructions in this notice for how to setup access to the portal.

Here is a brief demo highlightling the feature in use:

{% embed url="https://dev.navigahub.com/mothership/resources/videos/RenewalNotices.mp4" %}

### Ad Renewal Forms <a href="#_toc82534383" id="_toc82534383"></a>

Before you can send the notices, you will need to create one or more HTML forms to be used as the renewal notification to your clients.

Navigate to the menu Campaigns -> Renewals -> AD Renewal Forms.

![](<../../../.gitbook/assets/0 (53).png>)

Click the “View Merge Fields Documentation” button to view all available HTML fields.

Click “Create New” and design in the HTML tab the renewal form. You can create multiple ones for the different times you’d like to chase the renewal effort with the client. This step requires HTML knowledge.

Save the forms and link them in the renewal Efforts Forms secton of the product group setup so that the system knows which form to send out for each product group.

### Product Group Setup <a href="#_toc82534384" id="_toc82534384"></a>

On the product group you specify the renewal efforts to be used for the products in this group.

Navigate to the menu Setup -> Product Group Setup. Choose the product group from the drop-down menu.

![](<../../../.gitbook/assets/1 (57).png>)

Scroll to the section “Renewal Effort Forms”. Click the + to Add 1 New Line.

Choose the form from the drop-down menu. Repeat for different lines and different templates. You can use the same template for all attempts, and you can use as many attempts to renew as needed. Save the settings.

### Generate Renewal Notice <a href="#_toc82534385" id="_toc82534385"></a>

Navigate to the menu Campaign -> Renewals -> Generate Renewal Notices.

![](<../../../.gitbook/assets/2 (34).png>)

Choose the criteria to search on the campaigns, using the product group, client type, dates of expiration, whether to include/excluge Quotes, and whether to incluede/exclude orders which have no contact information. Click “Select Campaigns”. (The contact information that it is looking for is the "Order Contact" from the campaign header.)

You can also narrow down the results by typing text or partial text of the different columns’ filter under the header.

Note that the orders without a valid contact have a red exclamation mark by them and a renewal notice cannot be sent unless you correct the contact infomation. You can click the hyperlink to the campaign and view/edit the details.

You can also override the contact name on the order using the pencil icon and the renewal notice will be sent to this contact instead.

![](<../../../.gitbook/assets/3 (75).png>)

There’s a flag for each contact to indicate whether the user is also a Portal user or not. If the contact email address is configured to use the portal, this email address receives the renewal request with a link to the campaign on the portal and can renew it and sign the contract from there.

The Renewal Offset Date field contains the numeric value of the offset number of days in the renewed campaign. This is calculated and added to the column of Renewal Start Date displayed. If left blank, the renewal start date is the following day or according to the portal setup parameters of renewal date.

You can then enter the renewal start date for each campaign line to override the above Offset Date.

The Renewal Effort No. column displays the renewal attempt performed on the campaign the previous time you generated a renewal notice. This matches the template effort marked as first or higher as in the product group setup.

Choose the template to use from the Form Template drop-down for each campaign.

Click “Generate Renewals Batch” and then OK to be taken to the batch screen. Or click the node on the tree “View Batches”.

![](<../../../.gitbook/assets/4 (5).png>)

Click the hyperlink to the batch number to view the details. When the batch is processing you will see an hourglass icon in the Batch PDF column. Once it is finished you will see the black checkmark. Naviga personnel can check the progress of the logs and messages from the Windows Server log in the Admin screens if you have a concern about the status of the messages.

Navigate back to the renewal query screen for expiring campaigns and note that the renewal efforts counter has increased and displays the last renewal effort.

### Test Email Account <a href="#_toc82534386" id="_toc82534386"></a>

You can setup a test email account and use it as a test email address to view renewal notifications. This will override the client email address and send notices to this email instead. So this is just for testing purposes and should be removed when ready to run this in Production.

Navigate to the menu Setup -> Advertising Setup -> System Parameters.

![](<../../../.gitbook/assets/5 (36).png>)

Scroll to the “Renewal Settings” and enter the test email address in the field “Override Email to Address” and save. You can enter multiple addresses who will receive the renewal notifications.

Once you confirm that the notifications are good to go to clients, delete this email address and save the settings. Then repeat the renewal generation process so that the clients can receive the renewal notifications.

### Renew from the Portal <a href="#_toc82534388" id="_toc82534388"></a>

The client receives the above email to notify them of the renewal notice.

The client then clicks the link in the email and the system directs him to login to the portal.

Once the client logs into the Portal, the campaign due to be renewed is visible.

![](<../../../.gitbook/assets/6 (61).png>)

The renewals are listed under a separate node on the Proposals tree. Note that the campaign initially doesn’t have an ID because it hasn’t been renewed yet.

The client can then change the start date by entering the new date in the slot above the order using the calendar icon and click “Change Start Date”.

The order then adjusts the dates by refreshing and displaying the start date. It adjusts the end date to match the expired campaign length. The order also applies the line items to the available issues from the new start date to match the expired campaign.

The client can then scroll to the bottom and sign the contract.

Note that the future print issue dates must be preset in Naviga Ad in Product Setup and the renewed order uses the same rates as the expired campaign.

Once the client signs and approves the contract, the campaign disappears from the Renewal list and displays in the signed contract tab with a new campaign ID.
