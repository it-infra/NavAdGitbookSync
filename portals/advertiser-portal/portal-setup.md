# Portal Setup

This document is a guide to the Advertiser Portal, which is designed for the use by the your clients. The clients can view their own invoices and manage their data directly.

Note that the portal is mobile device friendly, so all screens will fit on the cell phones and iPad screens.

## Setup Menus <a href="#_toc116940147" id="_toc116940147"></a>

The setup menus below can be accessed from the **System Settings Module -> Client Access** menu. It can also be accessed from the **Advertising module -> Setup -> Admin -> Portal Setup**. There are slight differences in what is available in the different menus. Only the System Settings module allows for Portal User Import. Only the Ad Module allows for Emailing portal Users, Setting up Individual Access to multiple Portal Clients, and Setting up the Display templates for Print orders. The remaining items are available in both menus.

These menus, like all menus in Naviga Ad are controlled by Menu Security, so you may have access to some, none, or all of the items below.

<figure><img src="../../.gitbook/assets/image (1424).png" alt=""><figcaption></figcaption></figure>

### Client Access Setup <a href="#_toc116940148" id="_toc116940148"></a>

Allowed users can setup clients with access to the portal by navigating to the menu “Client Access Setup”.

Choose the customer ID from the drop-down menu and click the button “get data”.

To **allow remnant orders**, click “Yes.” These are [packages ](../../naviga-ad-modules/advertising/setup/package-setup.md#using-package-on-the-advertiser-portal)setup on the Ad system side to appear in the portal for customers to buy ad space (generally at a discount). In the Portal, these packages show up under the "Specials" section. Click no, and the available packages will not be shown to this advertiser.

**This is a Creative Agency**: If client is setup as a creative agency, he can see the orders and manage materials for the orders but not view the amounts nor invoices.

{% hint style="info" %}
Creative Agencies are linked to a client through their Brand setup (Billing Overrides section)
{% endhint %}

**Show Performance on Digital Orders:** This will display (or not display) the gauge for fulfillment on a digital order line for the customer to see. Options are Use System Default, Yes, or No. The System Default is set up in Portal Setup, Order View Template, option #5.

![](<../../.gitbook/assets/image (862).png>)

Note, the Single Copy Sales Settings are used in conjunction with our Newsstand module, which was more commonly used in the Classic Naviga Ad system. Most new clients can disregard this section. This section allows you to setup the single copy sales, for example, to allow draws, returns, short shipments, miscellaneous orders and transactions, and to set the minimum and maximum amounts to the respective invoices which would be available for your clients to manage.

Scroll to the section “Employee Access”, and add a username (their email address), enter a password for the user, which they can then change later, enter their title, and phone number, and click the + sign to add a user. Enter more users for this customer ID as needed.

### Setup Individual Portal Access <a href="#_toc116940159" id="_toc116940159"></a>

An individual can now access multiple client Portal accounts to facilitate the approval of proposals or payment of invoices for these clients.

Navigate to **Setup -> Admin -> Portal setup -> Setup Individual Portal Access**.

![](<../../.gitbook/assets/3 (51).png>)

Enter the name or individual ID which is created in the menu **Customers -> Advertiser Agency Maintenance** screen or through the Customer Account Screen, New Contact.

Check the flag “Active” to change its value to “Yes”.

Add the advertisers in the drop-down menu under Linked Portal Accounts. This the list of advertisers which this individual can now access on the Portal. Enter a password which this individual will use to login to the Portal. They can change the password later. Save the settings.

Navigate to login to the Portal using this individual’s email address and password. In the Proposals tab, this individual can see all the proposals from all various clients who are sent proposals from Naviga Ad. Note the advertiser filter just above the date in the below screenshot. The user can use that to filter the orders/invoices to a single account.

![](<../../.gitbook/assets/4 (61).png>)

Click the Invoices tab.

{% hint style="warning" %}
IMPORTANT - if you are using the "Individuals with Portal Access" functionality (set up via Setup -> Portal Setup -> Individuals with Portal Access) - we have temporarily turned off the ability to pay in the portal. This functionality will be brought back in 2024, but it needed to be re-worked to support all the new payment features and wasn't working as expected in 2023 software so it is disabled for the time being to avoid customer confusion. They will still be able to see their invoices and download copies, but they will not be able to pay in the portal.
{% endhint %}

![](<../../.gitbook/assets/5 (32).png>)

This individual can now manage the invoices for all the various clients.

Once you have linked an individual to an account through this screen, this person will also be listed in the "Employee Access" list when viewing the account settings on the **Setup -> Admin -> Portal Setup -> Client Access Setup** screen. If you remove access from either screen, it will be updated in both places.

If you have added access from the Client Access Setup screen, it will NOT automatically be added to the Setup Individual Portal Access screen though. This is because on the Client Access Setup screen you are simply adding an email address that is allowed to access - that email address doesn't necessarily need to correspond to a contact person in the system, where as on the individual setup you ARE selecting a contact person.

### Clients with Portal Access <a href="#_toc116940149" id="_toc116940149"></a>

To view a list of your clients who have access to the portal, navigate to the menu “clients with portal access”, and you can also see and manage which ones are allowed remnant orders.

<figure><img src="../../.gitbook/assets/image (291).png" alt=""><figcaption></figcaption></figure>

Note that when a client who has access to the Portal is marked as a “Do Not Use” in the account maintenance screen in Naviga Ad, the client’s Portal login will be disabled as well, and the system will prevent the client from accessing the Portal.

### Portal Setup <a href="#_toc116940150" id="_toc116940150"></a>

Navigate to the menu Portal Setup in the setup menu. This menu is to setup the portal for clients’ use including orders, materials and invoices.

{% hint style="warning" %}
After making changes in here, you must refresh the system to pull in the new settings. To do this, log into the portal and then by append the following to the URL: _**?reset=true**_

This refreshes the settings for all users.

For example, when you login, this will typically be the URL you land on (where XXX is your site code and YOURPROFILEID is your Portal Profile ID):\
<mark style="color:blue;">https://XXX.navigahub.com/Portal/Client/XXX/YOURPROFILEID/Messages</mark>\
edit that url to instead be: <mark style="color:blue;">https://XXX.navigahub.com/Portal/Client/XXX/YOURPROFILEID/Messages?reset=true</mark>
{% endhint %}

**Profile Selection**

The Client Portal system can be run under one or more profiles. A profile is a setup of rules that can represent different websites or properties. For instance, if you have Website A and Website B, and want to offer a different Self-Service portal for each, you could create a Profile A and B. The profiles are created for a product group where it will filter Orders, Invoices, and Specials to only display those in the selected product group(s) set here. It’s also by company where for orders and invoices the system uses the company assignment on the Group. For AR and other systems, the system uses the Company code related to the product or statement run.

Create a profile ID and profile description and set the defaults and save it.

**Renewals**

Renewals can be configured to allow portal users to quickly and easily renew existing campaigns using the portal. For more information, please refer to [Expiring Campaigns](../../naviga-ad-modules/advertising/campaigns/expiring-campaigns.md#\_toc82534388).

1. **Renewal Start Minimum Days**: Enter the minimum lead time for a campaign renewal and the system adjusts the calendar in the portal to allow for the number of days entered here as a lead time before renewing the campaign.
2. **Renewal Start Maximum Days:** Enter the maximum number of days in the future you will allow a renewal to start. For example, if the campaign expired today, once this maximum number days passed, the client won’t be allowed to renew the campaign from the portal.

The above settings will affect what is selectable in here:

<figure><img src="../../.gitbook/assets/image (292).png" alt=""><figcaption></figcaption></figure>

3. **Auto Renew Past Selection Days:** When listing proposals and renewals, this flag determines how far back the system displays expiring campaigns.
4. **Auto Renew Selection Future Days:** When listing proposals and renewals, this flag determines how far forward the system displays expiring campaigns.

The above settings will affect the campaigns that are displayed here:

<figure><img src="../../.gitbook/assets/image (732).png" alt=""><figcaption></figcaption></figure>

5. **Campaign Status Codes the Qualify for Auto-Renew Generation:** Most often we think of renewing orders that already ran, so you might choose to only allow CO and IS status orders. However, by making this setting flexible, it makes it possible to also renew expired proposals.

**Proposal Signature Settings**

This section is to determine what happens to campaigns when they are pending approval by a manager in the system.

1. **Upon Signatiure Set Campaign Status to:** Choose the desired campaign status in this drop-down. Accepting a proposal in the portal will change the status from a Quote to a Reserved campaign. Any of the 3 Reserved Statuses are available for selection
2. **Upon Pre-Payment, set the campaign Status to:** Choose the Desired campaign status in the dropdown. Prepaying the campaign after signature can further update the status to a different reserved status or it can confirm the order.
3. **Only change status on pre-pay if at least this % is paid:** If the client approves the campaign but only pays a portion of it, should we still change the status to what was selected in #2? Set the desired percent prepayment here. For example, perhaps 50% is acceptable, or perhaps it needs to be 100% prepayed to have the status auto-updated.
4. **Hide Proposals where Account is Pending Approval:** Yes/No value. This is when the advertiser account is pending a manager or finance approval and can be set to Yes to hide the proposal from the client on the Portal. When the advertising client’s account is approved in Naviga Ad, then the client can view their proposals on the Portal.
5. **Hide Proposals that are Pending Approval:** Yes/No value. This is when the proposal has not been yet approved and if set to Yes will hide the proposal from client on the Portal until it is approved by a manager in Naviga Ad. Once approved, client can view and accept the proposal on the Portal.

<details>

<summary>Direct View Settings (No Login Required)</summary>

Some of our clients choose not to utilize the entire portal, but instead only use the portal for the direct view proposal signature process. These settings are for those sites to offer other options besides the default behavior on some screens

1. Insert Billing Contact Details - When set to YES, billing contact information will be defaulted into the signature form when no login is required. When set to NO, billing contact information must be entered by the signer, unless they are logged in, where their login information is defaulted in this area. The recommended setting is No for this field.
2. Hide "Download and Sign Later" Option - If you are not setting up users and passwords for your client to log into the entire portal, and only using the direct view link, it might make sense to hide the option to sign later.
3. **Strip Portal Link when signing** - If set to YES, the Signature Link area in the template will be extracted from the document that is displayed for signature when on the portal.
4. After Approval, Hide "Approve another document" option - If you are not setting up users and passwords for your client to log into the entire portal, and only using the direct view link, there won't be another document to approve, so you will probably want to set this to yes in that scenario
5. "Continue" URL to use after approval - If you are not setting up users and passwords for your client to log into the entire portal, and only using the direct view link, the default behavior to continue to the login screen might not be desirable. You can enter an alternative URL here....perhaps your company website.
6. Email a pdf copy of the signed document to the billing contact on the campaign - select yes/no based on desired behavior
7. Email a pdf copy of the signed document to the signer, if different from the billing contact on the campaign - select yes/no based on desired behavior. This will use the email address that the user fills in while signing the document.
8. Email Subject Line - This relates to the email sent out for #5 and #6 above
9. Email Body - This relates to the email sent out for #5 and #6 above. Merge fields from the order confirmation may be utilized in this email.

</details>

**Order View Templates**

Choose the templates to view for the payment receipt, print, digital and exhibition orders. This will set the way the order information will be viewed on the screen for each order.

The Print Order template comes from **Setup -> Templates -> Order Confirmation Email Templates**, in the section at the top of the screen called "Print Order Portal Display Templates." The Digital Order Templates are chosen from the same list of templates that are used for Campaign Order Confirmations, so the dropdown list will display from the "Campaign Email Templates" section of Order Confirmation Templates. For more information, refer to [Email Templates Setup](client-portal-access.md#\_toc116940185) for the print, digital and exhibition portal order views.

The Receipt Template dropdown comes from **A/R Module -> Setup -> Receipt Template Setup**

You can also choose to show the performance on delivery of digital orders by checking the flag for this option.

<figure><img src="../../.gitbook/assets/image (51) (1).png" alt=""><figcaption></figcaption></figure>

**Credit Card Setup**

<figure><img src="../../.gitbook/assets/image (97) (1).png" alt=""><figcaption></figcaption></figure>

1. Credit card setup can be also set to **allow pre-payments** if the option is checked as “yes”. If the option is set as “no”, orders cannot be paid using credit cards.
2. Choose to **settle the prepayments immediately** as of charging the card, rather than wait, by changing this value to “yes”. If left as “No”, the charging will not take place till an invoice is generated.
3. **Credit Card Currency ISO Code** is a code which the bank can provide.
4. **Default Credit Card Bank:** This is the default bank to use for credit card payments of invoices if you have only one. These settings are required to process payments through the portal, whether that payment comes from a logged in customer or someone paying via Pay Link sent by an internal user.
5. **Bank Overrides by Company & Currency:** Corresponding to each company and currency, there is a drop-down option of bank to charge credit cards in case you have more than one company and/or currency in use. When multiple companies/currencies are in use, the portal will group invoices by company and currency. When your client chooses the invoice to pay, the system will automatically tie this to the company and to the bank listed in this screen and will be charged in the corresponding currency. Use the boxes at the bottom to select the company and the currency and click the add button to move them to the top grid, then select the corresponding bank.\
   **NOTE: If you use overrides for some companies/currencies, you must use them for ALL companies/currencies that you will potentially accept payment in. Use the default in #4 only if you do not need any overrides.**

#### Quick Pay Setup

This section allows you to set an override email (Subject & Body text) and time limit settings when sending a Quick Pay link to an advertiser. When sending the quick pay link, the sending user must select the desired profile from the dropdown.

{% hint style="info" %}
See [A/R Setup](../../naviga-ad-modules/accounts-receivable-credit-control/setup-a-r-system-setup/#\_toc124065024) for information on setting up payment links
{% endhint %}

**Other Settings**

1. **Paid Invoice Cutoff:** Paid Invoices before this date will not be displayed in the portal. For example, if you don't have PDFs from a conversion, you would set this date to eliminate those invoices that were converted.
2. **Default Sales Rep:** Enter the default sales rep for these orders on the portal where a sales rep isn’t defined.
3. **Enable Auto Account Creation:** When enabled, this option allows a user to login to the portal using their email address and Naviga Account ID, if they are not already setup for Portal access. This is valid only if the client has a valid email address in the system. Once validation to an existing portal user fails, the software checks to see if the password provided matches a valid Naviga Account ID, and if so checks to see if there is a contact on that account with the email address they submitted. If that all checks out, an account will be setup for them, they will be logged in and will be prompted to change their password.
4. Display Cash on Account Total in Aging by Currency - in the grid showing the aging to the customer, set this to yes, if you would like to show Cash on Account
5. Display Prepayment total in Aging by Currency - in the grid showing the aging to the customer, set this to yes, if you would like to show Prepayments on Account
6.  Display Balance in Aging by Currency - in the grid showing the aging to the customer, set this to yes, if you would like to show the total balance including Cash on Account and Prepays\
    Below screenshot shows fields 4, 5, & 6 if set to yes:\\

    <figure><img src="../../.gitbook/assets/image (72) (1).png" alt=""><figcaption></figcaption></figure>
7.  Show custom reporting link in Menu Navigation - this option allows for adding a custom link of your choice to the navigation. This will display on the portal here:\\

    <figure><img src="../../.gitbook/assets/image (74) (1).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../../.gitbook/assets/image (73) (1).png" alt=""><figcaption></figcaption></figure>

**Material Upload Configuration**

This section determines the way material is uploaded in the Portal. For details on these paths, please contact support.

They will provide you with the details of the SFTP, and paths for material submission and print-ready details.

In 2023.1, set these settings on the DEFAULT profile if you have multiple profiles. In 2023.2, we will remove this from portal setup and only have a single place to configure it where it will be used in both the Portal and also for internal preflight routing to Twist or Asura. This does not affect preflight if you are preflighting through Interface Link.

**Material Approval**

These settings are used for Material Approval/Rejection using the Portal.

1. **Hide Materials Pending Approval:** If checked to reflect “Yes”, then the materials that are awaiting client approval are not visible. Set to yes if you do not intend to use material approvals in the portal and the entire approval section will disappear.
2. **Status on Approval:** The desired material status can be selected for when the client approves the material for the order.
3. **Status on Rejection:** Any of these options can be selected for the material if the client rejects the materials.
4. **Material rejected Artwork Stage:** This updates the artwork stage upon rejection so that the material will come back into the artist queue for editing.

**Disable Navigation**

In the “Disable Navigation” section, you can click any of these boxes to a value of “Yes” to hide the button.

<figure><img src="../../.gitbook/assets/image (1491).png" alt=""><figcaption></figcaption></figure>

The navigation and page will be removed completely if you choose to disable certain items.

<figure><img src="../../.gitbook/assets/image (556).png" alt=""><figcaption></figcaption></figure>

This is using a grid layout of 12-units. When you display all 6 available navigation options, each navigation button will take up 2 units. When you disable all but 4 buttons or 3 buttons, those are easily divisible and will display evenly

<figure><img src="../../.gitbook/assets/image (1341).png" alt=""><figcaption></figcaption></figure>

If you display 5 buttons, the first three will be smaller than the last two...

<figure><img src="../../.gitbook/assets/image (542).png" alt=""><figcaption></figcaption></figure>

If you disable all but one or two, the navigation boxes will disappear completely, and only the text-based navigation will be available. For example, if invoices is the only item to be shown, you won't see the blue box that says invoices, you will only see the word "invoices" that is currently in the space above the big boxes on the above screenshot. (Otherwise it would look pretty silly to have a giant box saying "invoices" the spans the entire page.)

#### **Account Setup Requests**

This option, when enabled, allows portal users to request and internal user to set up accounts to allow users to login to the portal. Click the “Enable Account Setup Requests” to change its value to “Yes”. If left at “No”, then portal users will not see this option to request to create an account. If enabled (and at least someone is being notified) then the client will see a link "Request an account" that will let the client request a new account.

Enter the username from the drop list which you want notified when a request of an account is sent by a client. Enter the emails of one or more users who will be notified via email of this request.

#### **Message Routing**

This section contains an ability to enter email addresses for users who will be notified for an action. in some cases, this is the default, which will often get overridden by something else. In other cases, it is the only notification option. See message types below for full description of each item:

<figure><img src="../../.gitbook/assets/image (95) (1).png" alt=""><figcaption></figcaption></figure>

**Message types and routing of emails/assignments**

**Invoices –** For Invoices, the message routing from portal setup is just the back-up in case the customer isn’t assigned to a credit controller.

* if the client has a credit controller – the message will be assigned to the credit controller and the email notification also goes to the credit controller - regardless of what is in the message routing setup.
* If no credit controller –
  * It will email notification to whomever is the portal email user in portal setup.
  * The message will be “assigned” to whoever is the assigned to user in the portal setup

**Advertising Campaign (Digital/Print order) –** Regardless of what is set on the message routing –

* Email goes to the sales rep (if there are multiple reps, it will send to both)
* Email also goes to production controller on the order
* Message will be assigned to the production controller if there is one. If no controller, it is assigned to the first rep on the order.
* The notify user column is not generally used here b/c you cannot have an order without a salesperson...but this will be the fall-back if for some reason the system cannot determine who the controller or rep is.

**Exhibition Orders –** email will go to the Portal Setup email users and the message will be assigned to the assign to. This one does not look at the sales rep on the exhibition order at all.

**Proposal / Contract -** These can only be accessed by the client via the messages area in the portal. Client optionally selects the proposal id that this is in reference to, but they may leave it blank. The message will be assigned to the person in the notify user dropdown with email being sent to the user in the email users column. The Assigned User (Notify User) will also get a CRM alert on the CRM home screen. The Alert type on the CRM home will say "Client Note"

**New order inquiry message –** This will add an alert on the rep homepage in CRM to the notify user and an email to the listed email user. The Alert type on the CRM home will say "Request for Quote"

**Material questions –** email will go to the Portal Setup email users and the message will be assigned to the assign to.

**General Messages –** This is what routing and emails get used if the customer is on the Portal Messages screen and generates a new message without putting anything in the “regarding” dropdown. We don’t force them to pick something there.

**Payment Made** - On the invoices tab in the portal if the customer _**pays for an invoice in full**_ the user selected in the notify user dropdown will be assigned this message, and they will get an email notifying them about the message. Emails will be sent to the users listed in the email to column. If the advertiser has a credit controller assigned to them, they will also receive an email about the payment.

**Partial Payment Made** - On the invoices tab in the portal if the customer _**partially pays for an invoice**_ the user selected in the notify user dropdown will be assigned this message, and they will get an email notifying them about the message. Emails will be sent to the users listed in the email to column. If the advertiser has a credit controller assigned to them, they will also receive an email about the payment.

**Pre-Payment Made** - On the proposals tab (either immediately after signing or from the signed contracts screen) in the portal if the customer _**prepays for a campaign in full**_ the following will happen:

* Message will be assigned to the campaign's production controller (if there is one). If there isn't a production controller, it will be assigned to the sales rep. If for any reason, the system cannot determine who the controller or rep is, then the message will assign to the user listed on the portal setup in the message routing.
* Emails will be sent to both the rep and the production controller as well as any user(s) in the email users column.

**Partial Pre-payment made** - On the proposals tab in the portal (either immediately after signing or from the signed contracts screen), if the customer _**partially prepays for a campaign**_ the following will happen:

* Message will be assigned to the campaign's production controller (if there is one). If there isn't a production controller, it will be assigned to the sales rep. If for any reason, the system cannot determine who the controller or rep is, then the message will assign to the user listed on the portal setup in the message routing.
* Emails will be sent to both the rep and the production controller as well as any user(s) in the email users column.

#### Company Logo Image <a href="#_toc116940153" id="_toc116940153"></a>

Choose a logo image for the portal. This could be your company’s logo. You can upload the logo, by clicking the “select” button and choose the logo file. This can be a JPG, JPEG, PNG or GIF file.

#### Custom CSS Override <a href="#_toc116940154" id="_toc116940154"></a>

This is the section where a technically knowledgeable user can enter styles which will override the ones which exist already on the portal. Here is some sample code that I used to change the demo system from the standard colorful tiles to Naviga purple and aqua (Marketing would be so proud...)

{% code overflow="wrap" %}
```
.color1, .color2, .color3, .color4, .color5, .color6 { background-color: #1f0744 !important; border: 1px solid #fff !important; } .color1:hover, .color2:hover, .color3:hover, .color4:hover, .color5:hover, .color6:hover, .color1 .footer, .color2 .footer, .color3 .footer, .color4 .footer, .color5 .footer, .color6 .footer, .defaultColor1, .defaultColor1Alt, .defaultColor2, .defaultColor3, .defaultColor4, .defaultColor5, .defaultColor6, .breadcrumb, .selected, .paymentDetails th { background-color: #14b0bc !important; } #iCompanyLogo {max-height: 70px !important; } .mainFooter { background-color: #1f0744!important; } .footerPanel, .footerPanel a { color: #fff !important; } .footerPanel a:hover { text-decoration: underline !important; }
```
{% endcode %}

#### Default Footer Area <a href="#_toc116940155" id="_toc116940155"></a>

This is the HTML that will be used to render the footer area by default. You can change this code - or completely override it by using the Override Footer Area as explained below.\
Current valid Merge Codes:

**#VERSION# - The current release version of the portal software (e.g. 2023.1 Build 230225.0922)**

**#USERFULLNAME# - The user's full name**

**#USERLOGINID# - The user's login username**

**#COMPANYNAME# - The user's associated company / employer's account name**

**#COMPANYID# - The user's associated company / employer's account ID**

Each responsive column can contain any of the above fields. To keep the 4 responsive footer columns, but override the settings in one or more of them, configure that here.

![](<../../.gitbook/assets/2 (77).png>)

#### Override Footer Area <a href="#_toc116940156" id="_toc116940156"></a>

The footer area is blank and to clear the entire existing footer, user should add in the Footer Area the following: \<br/> or \&nbsp.

Note that the portal caches the Portal Setup options so if user makes changes and returns to the portal web page, they will not see the changes take effect immediately. The cache must be reset. As explained above, to reset the cache user can add the syntax: ?reset=true to the end of any page URL in the portal. This will refresh the setup for all users.

#### Remnant Orders Terms and Conditions <a href="#_toc116940157" id="_toc116940157"></a>

This section can be used to design an HTML message which the client sees when purchasing remnant orders (Specials) from the portal. The client must agree to these terms and conditions at the checkout time to proceed with the purchase.

#### Material Upload Instructions <a href="#_toc116940158" id="_toc116940158"></a>

This section displays the instructions when client is uploading new material in the portal. This is HTML based.

## System Parameters Setup <a href="#_toc116940160" id="_toc116940160"></a>

In the Systems Settings module, navigate to the menu **Setup -> Advertising -> System Parameters.** In the A/R Portal Settings, under the A/R Portal Server Address enter the portal address. This is typically set up by your Implementation Specialist when setting up the system, but if you are seeing any strange behavior, check here to ensure the URL is what is expected.

Typically you will see the below, with your site code in place of the xxx

<figure><img src="../../.gitbook/assets/image (275).png" alt=""><figcaption></figcaption></figure>

Click on the “Save” button to store the settings.

## Client Login Report <a href="#_toc116940161" id="_toc116940161"></a>

You can view who has logged in when they last logged in by navigating to the menu “Client Login Report”. This information can be exported to excel or pdf.

## Client Usage Detail Report <a href="#_toc116940162" id="_toc116940162"></a>

This menu allows you to view the usage of the portal by the different clients you have given access to the portal.

Navigate to the menu “client usage detail report" and choose the date range from the menu calendar popups.

<figure><img src="../../.gitbook/assets/image (1567).png" alt=""><figcaption></figcaption></figure>

You can also filter by function. The functions can be anywhere from login, to viewing orders, to invoices management.

You can also type partial characters to narrow down the list of results, in any of the blank boxes under the columns.

## Inactive Client Report <a href="#_toc116940163" id="_toc116940163"></a>

You can view a list of clients who have been inactive on the portal and are not using it for the last XX days. Navigate to the menu “inactive client report” and select desired number of days from the top right corner.

![](<../../.gitbook/assets/8 (41).png>)

## Email Promotional Items to Your Clients <a href="#_toc116940164" id="_toc116940164"></a>

You as a Naviga user can setup your clients with access to the portal to receive promotional emails regarding new announcements or package promotions. The system provides an email HTML template which you can setup. The template also includes an unsubscribe field so that clients can unsubscribe from these emails if they wish. You can also unsubscribe your clients from the emails through Naviga Ad.

### Email Templates Setup <a href="#_toc116940165" id="_toc116940165"></a>

Navigate to the menu **Setup -> Admin -> Portal Setup -> Portal Email Templates**.

![](<../../.gitbook/assets/9 (11).png>)

Click the button “View Merge Field Documentation” to view all HTML fields available to use in your email. To create the template, you must know HTML.

Click the “Create New” button and design your HTML template. Save the template. Here is some simple sample code to get you started

{% code overflow="wrap" %}
```
<!DOCTYPE html>
<html>
    <head>
        <title>Demo Portal Email</title>
        <style type="text/css">
            body, p, td
            {
            font-family: arial;
            font-size: 1em;
            line-height: 150%;
            }
            #page
            {
            margin: 10px auto;
            width: 85%;
            max-width: 800px;
            min-width: 600px;
            }
        </style>
    </head>
    <body>
        <div id="page">
        <div>#USER_FULLNAME#:</div>
        If you have not checked recently - we have added more buying options for you on the portal.
        <a href="https://xxx.navigahub.com/Portal/Client/xxx/packages/available" target="_blank">Login today</a> and check it out.
        <br />
        <br />
        <div>Account ID: #ACCOUNT_ID#</div>
        <div>Account Name: #ACCOUNT_NAME#</div>
        <div>Your Full Name: #USER_FULLNAME#</div>
        <div>Uour Email Address: #USER_EMAIL#</div>
        <div>Comment: #COMMENT#</div>
        <br />
        <br />
        You are receiving this email because you are a client who is setup with access to our online client portal.
        If you would like to unsubscribe from all future emails like this <a href="#UNSUBSCRIBE#">click here</a>
        </div>
    </body>
</html>
```
{% endcode %}

Navigate to the menu **Setup -> Admin -> Portal Setup -> Send Emails to Portal Users**.

![](<../../.gitbook/assets/10 (10).png>)

Choose by Client Type in the drop-down by checking the box for each client type or leave blank for all clients to receive the emails. The Client Type is the field setup on the Advertiser/ Agency Maintenance screen in the Advertising Setup node. This is meant to classify your clients in groups for organizational purposes.

Once you’ve checked the box(es) for clients, click on “Email Selected Users”.

![](<../../.gitbook/assets/11 (21).png>)

The pop-up screen produces your choice of email template to use. You can enter a subject line and enter comments in the Comment Merge Tag, which also allows for use of the HTML fields available in the template.

Click “Send Email” and the system sends out the promotional emails to your clients. The messages appear from you and contain the template fields and your message.

![](<../../.gitbook/assets/12 (17).png>)

The message also includes a link to unsubscribe from these emails if your client wishes to do so. This removes them from the email list on the system and they can no longer receive the messages you send.

Navigate back to the screen to email portal users.

![](<../../.gitbook/assets/13 (21).png>)

If you choose all clients and select data, you will see when and who was sent the last email, and which template this user sent.

### Unsubscribe Clients from Emails <a href="#_toc116940166" id="_toc116940166"></a>

You can unsubscribe the clients by navigating to the menu **Setup -> Admin -> Portal Setup -> Client Access Setup**. Retrieve the client from the drop-down menu and scroll to the section “Employee Access”.

![](<../../.gitbook/assets/14 (18).png>)

Check the box “Remove from Email Lists” and click Save.

Navigate back to the menu **Setup -> Admin -> Portal Setup -> Email Portal Users**. Select Data and note that this client has been removed from your list of email recipients.

## Portal User Accounts Import <a href="#_toc79079625" id="_toc79079625"></a>

The system allows system users to import names of their clients who they wish to give access to the Portal. This document explains how you as a user can import clients’ IDs and names in large numbers using a system provided template to give access to your clients to the Advertiser Portal. You can use the same import template to update existing accounts.

Navigate to the System Settings module and click on the menu **Client Access -> Portal User Account Import**. This process can be performed using the provided template.

<figure><img src="../../.gitbook/assets/image (1472).png" alt=""><figcaption></figcaption></figure>

Download the template from this screen by clicking on the button “Download Template”, which opens an excel spreadsheet. Fill out the sheet and save to your desktop. For the template details, please see section below titled Template Fields.

![](<../../.gitbook/assets/2 (12).png>)

Click on the “Select” button to browse for the saved spreadsheet and select it which then uploads it to the portal user import screen.

To flush out all errors in the spreadsheet, click on “Test Import” and then click OK if you get an error. The system displays the line number which has the erroneous data and the cause of error so that you can manually fix the errors in the template spreadsheet.

After error correction, resave the template to your desktop. Click the red x remove button to clear the erroneous upload and then click the select button again and browse for the corrected template, then select it to upload it again to the import screen. Once the system displays the message indicating that the import template data is all accurate and no further errors remain, click the “Import File” button to finalize the import process.

To view the imported names, navigate to the menu **Client Access -> Client Access Setup**. Enter the client ID and the imported data is reflected in the screen fields. You can complete any missing information or change any field value on this screen.

<figure><img src="../../.gitbook/assets/image (273).png" alt=""><figcaption></figcaption></figure>

When finished, click on the “Save” button. Now, the client is ready to login to the Advertiser Portal with their provided login emails and passwords according to the values in the import template.

### Template Fields <a href="#_toc79079626" id="_toc79079626"></a>

Click the button “Download Template”.

This will open the excel spreadsheet for you to fill out. The fields are as follows:

<table data-header-hidden><thead><tr><th width="149"></th><th width="156"></th><th width="326"></th><th></th></tr></thead><tbody><tr><td><strong>Field Name</strong></td><td><strong>Sample</strong></td><td><strong>Source and Format</strong></td><td><strong>Optional/ Mandatory</strong></td></tr><tr><td><strong>Client ID</strong></td><td>14009</td><td>This is a numeric value of the client ID which must match the value of the client’s ID in Naviga</td><td>Mandatory</td></tr><tr><td><strong>Email</strong></td><td>abc@xyz.com</td><td>Email address of the client in the form of a valid email address. This is the client’s login ID to the Portal.</td><td>Mandatory</td></tr><tr><td>Password</td><td>Blank with no value; or any value to which the same rules of the portal password apply.</td><td><p>For a client ID who is a current Portal user, and this field is left blank, the client’s password will not change. If the client already has access to the portal and you enter a password in this field, this password in the template replaces the existing client password.</p><p>For a client ID who is new to the Portal and does not have access to the portal, if left blank, the password is automatically the same as the Client ID. If you enter a value in this field, then the client’s password is this value. The client can later reset their own password. Note that the Auto Account Creation must be activated in Portal Setup for this login to work.</p></td><td>Optional.</td></tr><tr><td><strong>Full Name</strong></td><td>Susan Constantine</td><td>Alphanumeric value of the client name.</td><td>Mandatory</td></tr><tr><td>Title</td><td>Marketing Manager</td><td>Alphanumeric value of the client job title.</td><td>Optional</td></tr><tr><td>Allow Remnants</td><td>Y</td><td><p>This is a Y or N field for yes or no which allows the user to purchase remnant orders if available as per the Naviga setup.</p><p>This can be left blank if the client already has access to the portal and the remnant orders value is already set. This value if entered in this field, as Y or N, replaces the value in Naviga for this client.</p></td><td>Optional</td></tr><tr><td>Creative Agency</td><td>N</td><td><p>This is a Y or N field for yes or no which marks this client as a creative agency if applicable.</p><p>This can be left blank if the client already has access to the portal and the creative agency value is already set. This value if entered, as Y or N, replaces the value in Naviga for this client.</p></td><td>Optional</td></tr></tbody></table>
