# Classified Self Service Portal

The Self-Service Classified ad entry is designed for your advertisers to create and generate their own advertisements with no login required and with pre-designed templates which simplify the process. The ads still must be reviewed and approved internally by you before publication and must be prepaid by the customer.

The software is responsive and runs on a desktop or a mobile device.

Clients who use this feature tend to be transient clients or one-time clients, and the Naviga system will not store their information so as not to crowd the database with non-repeat clients. Based on the client email address, if the client becomes a repeat client with repeat ads, the system no longer considers him a transient customer and you can connect his ads to one account as the ads are requested and are connected to a client ID.

Alternately, the user CAN create an account for himself through the portal. Once they have establised an account, the client can log in and see past self service orders and copy the order to repeat the ad.

## Prerequisites <a href="#_toc117696645" id="_toc117696645"></a>

1. This service must be enabled in the admin screen by the Naviga team. This is a flag set to Yes in the Windows Service Setup admin menu to enable the feature under the section “Classified Self Service”. If this flag is not set, email confirmations will not properly send to your clients.\
   ![](<../.gitbook/assets/image (189).png>)
2. Your Naviga Account must be licensed to use the classified portal. Navigate to Security -> License Information and confirm you are licensed properly. Note: prior to 2023.1, we didn't have a license flag in the database. So if you have the Self Service Portal in your contract and you upgrade to 23.1 and don't see the flag enabled, please notify support and we can get you sorted quickly.\
   ![](<../.gitbook/assets/image (1597).png>)

## Classified Self-Service Portal Setup <a href="#_toc117696646" id="_toc117696646"></a>

Navigate to the Advertising Module Campaigns -> Classified Self Service -> Self Service Setup. In this screen you can setup the portal layout where the user can see the general setup and look and feel of the screen where they place their self-serve ad.

The Classified Self-Service system can be run under one or more profiles. A profile is a setup of rules that can represent different websites or properties. For instance, if you have Website A and Website B, and want to offer a different Self-Service portal for each, you could create a Profile A and B.

This screen also allows you to copy from an existing profile and tweak the copied profile to avoid repetitive manual entry.

Each profile has its ID and description and the steps which user will view while entering the ad. Once created, under the Profile Description will be a link to navigate to the Classified Portal. Anytime you make changes in here, go to the portal screen by clicking the link. In your browser, add ?reset=true to the end of that URL to clear the cache and read in your recent changes. If you don't do this step, your configuration changes will not be visible until after your next nightly maintenance process.

<figure><img src="../.gitbook/assets/image (597).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note - the URL link above is formed based on what Naviga personnel has set up as your Base System URL. In the above example, my Base System url is https://sandbox.navigaglobal.com/ew/dem/

To form the URL, the "ew" is replaced with "portal/classified" and the profile ID is added to the end.\
If the Base system URL was created without the slash at the end, your URL shortcut might be missing the slash between your 3-digit site code and the profile ID. That can be added manually after you click the link (in the short term) - or for a permanent fix, ask your Implementation Specialist or Naviga Support to add that extra slash for you in the system admin setup screen.
{% endhint %}

### Testing Options

During setup and testing it might be desirable to send the confirmation emails to one or more email addresses instead of the email address entered online. Enter the email addresses here. This should be blank in a production environment to allow the emails to go to the client placing the order.

### Configuration Options

Enter the text which prompts the user to make choices of entries for the ad. Save the profile.

<figure><img src="../.gitbook/assets/image (564).png" alt=""><figcaption></figcaption></figure>

The above text corresponds to the instructional text that the client sees when booking their ad:

<figure><img src="../.gitbook/assets/image (1442).png" alt=""><figcaption></figcaption></figure>

### Site Logo

Upload desired logo to be placed at the top left of the screen. An ideal logo file will be less than 100kb in size, and in PNG format. Other supported formats include JPG and GIF.

<figure><img src="../.gitbook/assets/image (267).png" alt=""><figcaption></figcaption></figure>

Online it appears like this:

<figure><img src="../.gitbook/assets/image (776).png" alt=""><figcaption></figcaption></figure>

### Color Configuration

The UI is based on a Material.io theme consisting of two primary colors. You can change the primary, secondary, and/or Application Bar colors to adjust the site to more closely match your corporate colors. Select a color from the "web" tab by clicking on the desired color box. Select RGB, HSB, or HSV tabs to manually enter a specific color code

<figure><img src="../.gitbook/assets/image (524).png" alt=""><figcaption></figcaption></figure>

### Other Configuration

When your client has succesfully entered an ad, they will be prompted with a confirmation screen, and two action buttons. The first action is to enter another order. The second action is to return to your main website. The text and URL below will determine the appearance and functionality of the second option.

1. **Completed Next Action Button Text:** Once the user has completed the process they are presented with 2 buttons. One will return them to the start to book another ad, and the second is customizable. Enter what you want the button to say here.
2. **Completed Next Action Button URL:** For the above button, enter the URL where the customer will be directed here. Generally this is your main website or marketplace page.
3. **Allow PDF Download of creative in steps 3 & 4:** Generally it is desirable to require the client to pay for the ad before being able to download a pdf. If you wish to allow them to download the pdf earlier in the process, select "yes" here.
4. **Minimum order lead time:** This is the number of days you need as approval lead time. For instance enter a 2 here would mean that the earliest issue or run date a user can select will be two days in the future.
5. **Prompt for location data:** Yes/No field. When enabled, your end users will be prompted to share their location data. If they accept, we will record Latitude and Longitude coordinates on the order when it is submitted.

<figure><img src="../.gitbook/assets/image (251).png" alt=""><figcaption></figcaption></figure>

### Order Defaults

When orders are created, the following default data is used to complete the data records.

1. Advertiser: If a client opts to not log into the portal, but instead book the order anonymously, this is the account that the order will be attached to. To create a Transient account, the "Transient Record" flag must be set in [Name Maintenance](../naviga-ad-modules/advertising/customers/advertiser-maintenance.md#advertising-details).\
   **\*\*\* It is very important to set a default client here. There isn't a mechanism to force the client to log in, so you do need to have a transient client set up here. If the client doesn't link the order to their account, the person approving the orders internally can link it to an account prior to approving the order.**
2. Sales Rep: This will be the sales rep associated with the self service users. (A generic "web" rep can be created in Sales Rep Setup if you do not with to link to a regular rep.)

<figure><img src="../.gitbook/assets/image (277).png" alt=""><figcaption></figcaption></figure>

### Terms and Conditions

If desired, the advertiser can be required to approve some terms and conditions prior to creating the order and/or before creating their account.

1. Enter text in this box if you would like to display some terms to the user in Step 1 of order placement.
2. Set to yes to have a box there user must indicate that they agree to the above terms and conditions.

<figure><img src="../.gitbook/assets/image (1527).png" alt=""><figcaption></figcaption></figure>

If 1 and 2 are set above, this is what it looks like to the user:

<figure><img src="../.gitbook/assets/image (603).png" alt=""><figcaption></figcaption></figure>

Note that the "Next" button is grayed out. Since #2 is set to yes, the advertiser must click I Accept to proceed. If #2 was No, the Attention box with the terms would still be displayed, but they would not be required to indicate acceptance.

3. This next option pertains to creating a user account. Enter text here to provide some terms and conditions to the user before they can create an account
4. Indicate Yes here is the client is required to indicate that they have read and agree to the terms prior to creating an account.

This is what it will look like to the client when they create an account. If #4 was set to "No" but there was text in box #3, then the terms and conditions link would be there, but there wouldn't be a requirement to check the I accept box. If #3 is blank and #4 is no, then that entire line would disappear and the user could create their account with just email, first name, last name, phone number and password.

<figure><img src="../.gitbook/assets/image (600).png" alt=""><figcaption></figcaption></figure>

### Email Notifications

#### Initial Confirmation that their order was received

1. Order Confirmation Email - Subject line - Enter the text of the email's subject line. Basic order tags can be used. (For Example, Campaign ID)
2. Order Confirmation Email - Body Text - Enter desired body text for the confirmation email that is sent to the customer.

<figure><img src="../.gitbook/assets/image (163).png" alt=""><figcaption></figcaption></figure>

Here is some sample text to get you started. Click on the "click here" link after #2 to see all available merge tags for the confirmation email.

{% code overflow="wrap" %}
```
<div style="margin:10px;  width: 700px; font: 14px arial, sans-serif;line-height:150%">
<div style="background-color: #B8B7B5; width: 100%; padding: 10px; box-sizing: border-box;">
<img alt="" src="https://pages.navigaglobal.com/rs/531-ETU-453/images/NavigaColorLogo.png" style="height: 40px; display: inline-block; outline: none; border-width: 0px;">
</div>
<div style="background-color: #411CB5; width: 100%; padding: 10px; box-sizing: border-box; height: 20px;">
</div>
<br>
<span style="font-size: 150%">Thank you for your order!</span>
<br>
<br>
Order No.: #CAMPAIGN_ID#
<br>
Order Date: #TODAY#
<br>
First Run Date: #START_DATE#</div>
<div style="margin:10px;  width: 700px; font: 14px arial, sans-serif;line-height:150%">Order Total:&nbsp;#TOTAL_AMOUNT#<br>
<br>
Dear #FIRST#,
<br>
<br>
We have received your ad and will review it for approval ASAP. If we have any questions or concerns we will reach out to you via phone and/or email. Each ad submitted online is reviewed by our team of advertising experts.
<br>
<br>
<img style="max-width: 400px" src="#PREVIEW_IMAGE#">
<br>
<br>
Approvals typically happen in less than 24 hours. We will notify you via email when you ad is approved!
<br>
<br>
<br>
If you have any questions, please contact us at (555)-567-8900,
<br>
or via email at we_care@someplace.com.
<br>
<br>
<br>
</div>
```
{% endcode %}

#### Order Approval Email

Steps 3 -> 5 pertain to the email that gets sent when the order has been approved by an internal user.

3. Order Approval Email - Subject Line: Enter the text of the email's subject line. Basic order tags can be used. (For Example, #CAMPAIGN\_ID#)
4. Order Approved Email - Body Text: Enter desired body text for the approval email that is sent to the customer.
5. Order Approval Email - Attachment template. For the dropdown to populate here, you must create a template in Campaigns -> Classified Self Service -> [Email Templates](classified-self-service-portal.md#self-serve-approval-rejection-templates)

<figure><img src="../.gitbook/assets/image (506).png" alt=""><figcaption></figcaption></figure>

#### Order Rejected Email

6. Order Rejected Email - Subject Line: Enter the text of the email's subject line. Basic order tags can be used. (For Example, #CAMPAIGN\_ID#)
7. Order Rejected Email - Body Text: Enter desired body text for the confirmation email that is sent to the customer.
8. Order Rejected Email - Attachment template. For the dropdown to populate here, you must create a template in Campaigns -> Classified Self Service -> [Email Templates](classified-self-service-portal.md#self-serve-approval-rejection-templates)

<figure><img src="../.gitbook/assets/image (1161).png" alt=""><figcaption></figcaption></figure>

### Bank Selection

From the dropdown select the desired bank that the payment should be attached to. Spreedly or NavigaPay banks are accepted.

<figure><img src="../.gitbook/assets/image (1067).png" alt=""><figcaption></figcaption></figure>

### Payment Configuration (Spreedly Only)

If using Spreedly, the screen details that the client sees can be modified here.

For example, in the example below "Naviga" is displayed - This will be the Company Name in Step 1. Where you see "Self Service" below, this will be whatever you set in step 2, and so on. This section changes the labels from what is there by default. Be sure to enter the Currency code in Step 10 if using Spreedly. This entire section can be skipped if using a NavigaPay bank

<figure><img src="../.gitbook/assets/image (1485).png" alt=""><figcaption></figcaption></figure>

### Moderation

Set the language to be used in the moderation set up for this profile. This works in conjunction with the Moderation setup above in Prerequisites.

<figure><img src="../.gitbook/assets/image (162).png" alt=""><figcaption></figcaption></figure>

### Profile Restrictions

Once the profile is saved, then you can go back and limit the profile to certain packages to be available to clients using this website profile only. This can be done by highlighting the package and click the right facing arrow to move them to the right pane.

You can do the same to limit the profile to category trees.

![](<../.gitbook/assets/3 (63).png>)

These limit the user entering the self-classified order to these options.

If you are using the self-service for just a single category, you may wish to have the category pre-selected for the client. OR, if from a particular page on your website, you wish to direct the client to the portal and have a relevant category pre-set, you can do that by adding ?t=TREEID or ?t=TREEID\&c=CATEGORYID to the URL. (The IDs should be in all caps) For example:

https://sandbox.navigahub.com/portal/classified/dem/demo/entry?t=LEGAL -- This will pre-select my Public Notice Tree\
https://sandbox.navigahub.com/portal/classified/dem/demo/entry?t=LEGAL\&c=BIDS -- This will pre-select my Public Notice Tree and my Bids & Proposals Sub-Category

NOTE: Please don't book ads in my demo system - the URLs above were just provided as examples.

### Package Restrictions

For any given profile, you can restrict which packages are displayed in the portal. Select which packages display by moving those packages to the right column (shown in screenshot above). If none are selected, that means all are available. See [Package setup](../naviga-ad-modules/advertising/setup/classified-setup/classified-packages.md#for-use-in-classified-self-service-portal) for assistance in creating the packages.

## Self Serve Approval/Rejection Templates

Navigate to Campaigns -> Classified Self-Service -> Email templates to configure the attachments for approval and rejection emails.

Click "Create New" in the document explorer on the left side. Enter a template name and, if desired, a description. Select "yes" to the active flag to make this template available for use. Use the Design and/or HTML tabs at the bottom to create your template. Example templates are provided below and can be copy and pasted onto the HTML tab and then modified to suit your needs.

<figure><img src="../.gitbook/assets/image (1324).png" alt=""><figcaption></figcaption></figure>

Below is a sample approved order template to get you started. Click on the "click here" link under step #5 in self service email notification section to see all available merge tags.

{% file src="../.gitbook/assets/SelfServiceApprovalSample.txt" %}

Below is a sample rejection template to get you started. Click on the "click here" link under step #8 in self service email notification section to see all available merge tags.

{% file src="../.gitbook/assets/SelfServiceRejectionSample.txt" %}

## Advertiser’s View <a href="#_toc117696647" id="_toc117696647"></a>

Your advertiser can navigate to the classified portal. Typically a site will have a link to this portal from your main website or classified marketplace.

If enabled in setup, the client is asked whether to allow or block location tracking. These preferences are stored in their browser, so they are only asked once, unless they clear their cache.

The client can choose a category and a sub-category for the ad he would like to enter.

![](<../.gitbook/assets/4 (27).png>)

The client can then choose one of the many [packages ](../naviga-ad-modules/advertising/setup/classified-setup/classified-packages.md#for-use-in-classified-self-service-portal)designed for them in the Naviga Ad system.

![](<../.gitbook/assets/5 (30).png>)

Client has the options to include print, digital, mobile and so forth according to the availability of your publications’ packages offered.

When the client clicks next, the screen allows him to enter his ad information according to the metadata as per the setup in the Naviga Ad system.

![](<../.gitbook/assets/6 (11).png>)

The system displays the ad as the client is creating it. The client can upload an image and enter all the data relevant optional and mandatory fields according to the setup on Naviga Ad. The client can also choose from existing images in the system which are designed as generic but attention-grabbing images which are uploaded in the Naviga system.

Once the client clicks next, the system allows him to choose the date for the advertisement to be placed.

![](<../.gitbook/assets/7 (28).png>)

The package setup gives you flexibility to offer promotions which the client can see on this screen such as free offers with certain purchases. Once the dates are selected, the client can then enter his contact information. If the client opted to set up an account and has signed in, this contact information will be pre-filled.

![](<../.gitbook/assets/8 (5).png>)

Once the client clicks “Approve and Pay”, the payment screen displays allowing him to use a credit card. The design of the payment window will be dependent on the payment processor.

The processing screen displays to confirm the payment. The client then receives an email confirmation the the order was received. Note that at this point the system only authorizes the credit card it will not be settled until the order has been approved by you.

## Approval Queue and Approval <a href="#_toc117696648" id="_toc117696648"></a>

In Naviga Ad, you can view all ads entered by the clients through the Self-Service portal and which are pending your review and approval.

Navigate to Campaigns -> Classified Self-Serve -> Orders Pending Approval.

![](<../.gitbook/assets/9 (18).png>)

If desired, select the product group which contains products in which clients place orders and click “Select Data”. This can be left blank to see all. The data displays the Campaign ID with a hyperlink to drill down into the details of the ad, the date the ad was entered, the client contact information and the approval status of the order.

Click the hyperlink to the ad and you can review and, if necessary, edit the details.

<figure><img src="../.gitbook/assets/image (1064).png" alt=""><figcaption></figcaption></figure>

Once you complete the edits, you can then click the Approved, or Rejected or Pending status on the order from this screen or from the Queue screen and save the settings. You can also click Reject and Next or Approve and Next to keep this window open and review all orders one by one.

![](<../.gitbook/assets/11 (25).png>)

When editing the order, you can also change the dates if there is a change needed.

You can also click the email address of the client to view matching emails in the system.

![](<../.gitbook/assets/12 (12).png>)

If this is a repeat client, you can check the matching email account and click Apply, which would tie the orders for this client together, and the client is no longer considered a transient client aka one-time advertiser.

If the client logged into the portal and this order was already linked to an account the email box would indicate "Logged in Account" and display the account number.

Once you approve or reject the order, the client receives an email with approval information or with the rejection email.

At this point, once the order is approved, the credit card is settled. If the order is rejected, the credit card will not be charged.

## Create Account <a href="#_toc117696649" id="_toc117696649"></a>

The advertiser can click the login button and create an account for himself by filling the form with name, email and password. The account can be as an individual or Company.

![](<../.gitbook/assets/13 (10).png>)

Click “Sign Up”.

Once you login, under the account name you can enter an new order and view past orders.

The user can create their account up front, or they can also be prompted to create an account at the end after their order was booked.

## Moderation <a href="#_toc117696650" id="_toc117696650"></a>

On the order there is a button called View Moderation Detail. The system uses a tool which can highlight and interpret content which can be considered inappropriate and when you click this button, the system provides details of questionable text and images that the client may have entered.

![](<../.gitbook/assets/14 (2).png>)

The system provides a rating of the text and images.

Moderation supports multiple languages in many countries based on Microsoft Azure service.

### Moderation Setup <a href="#_toc117696651" id="_toc117696651"></a>

The moderation process goes through four steps:

1. The text used in the ad is processed by Microsoft's Content Moderator, a machine-assisted content moderation system which identifies text that could be deemed inappropriate.
2. The images are then processed through an image recognition and filter process to identify any images that could be deemed inappropriate.
3. English terms are then run through a preset list of English terms that Google uses to filter online search content to block words and phrases that could be deemed inappropriate.
4. The Naviga system then applies the rules set below in this screen for additional terms that could be deemed inappropriate.

This screen is an added optional step.

![](<../.gitbook/assets/15 (18).png>)

Add any words or phrases that you may want to allow even if found by Microsoft moderator on the OK Words side. Likewise, add any words or phrases to the list of unacceptable words and phrases, even if Mocrosoft deems them to be ok.

## Abandoned Orders <a href="#_toc117696652" id="_toc117696652"></a>

When a client starts to enter an order but never completes the order in full, the order is marked in the report Campaigns -> Self-Service Classified -> Abandoned Orders.

![](<../.gitbook/assets/16 (19).png>)

The screen provides details of the step where the order was abandoned, the device the client was using at the time, the IP address and Operating System. It also lists the package chosen, time and date of starting the order.

The abandoned orders provide a tool to analyze the where usage is dropping off and this can assist in better business decisions or improvements.

## Self-Service Orders Dashboards <a href="#_toc117696653" id="_toc117696653"></a>

These screens allows for a high-level analysis of the orders entered.

The analysis is by days of the week, categories, value of the ads for the days as well as locations on the map from where the ads are coming. The screen also provides a record list of the orders.

### Approved Orders Dashboard <a href="#_toc117696654" id="_toc117696654"></a>

Navigate to the menu Campaigns -> Self-Service Classified -> Approved Orders Dashboard.

![](<../.gitbook/assets/18 (16).png>)

The approved orders graphic and record analysis display by category, day of the week, map and revenue. The list provides hyperlinks to the orders for more details. If you are not asking the client for their location data in Self-Service Setup, the map will not be displayed

Navigate to the menu Campaigns -> Self-Service Classified -> Approved Orders to see a list of approved orders without the charts at the top

<figure><img src="../.gitbook/assets/image (559).png" alt=""><figcaption></figcaption></figure>

### Rejected Orders Dashboard <a href="#_toc117696655" id="_toc117696655"></a>

The menu Campaigns -> Self-Service Classified -> Rejected Orders provide details on the orders which were rejected such as the order number, who rejected the order and when.

![](<../.gitbook/assets/19 (13).png>)

The screen lists also the packages, the start and end dates, the group, and value of the rejected order.

## Billing <a href="#_toc117696658" id="_toc117696658"></a>

The payment which is processed on Naviga Ad is treated the same as an internal order where the invoice is generated in Naviga and is posted to A/R. This is completed at the time of approval, so the order will not go through the standard Billing Process. Upon approval it is considered to be immediately billed and posted.

The tax is calculated on the portal and added to the credit card payment at the time the client submits the order.
