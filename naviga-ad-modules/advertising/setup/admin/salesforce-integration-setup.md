# Salesforce Integration Setup

## Demo of Salesforce Integration

Here is a little preview of how it all works once connected:

{% embed url="https://dev.navigahub.com/mothership/resources/videos/SalesForceIntegrationDemo.mp4" %}

## Initial connection with SF

1.  In Salesforce, create profile: Naviga\_Admin, based/cloned on the “System Administrator” profile. Use Salesforce license. Setup -> Users -> Profiles-> New\\

    <figure><img src="../../../../.gitbook/assets/0 (43).png" alt=""><figcaption></figcaption></figure>

    ![](<../../../../.gitbook/assets/1 (45).png>)
2. Login to the Salesforce Org you are installing the package on using any System Administrator account.
3. Install the package to the Salesforce Org:

[https://login.salesforce.com/packaging/installPackage.apexp?p0=04t4P000002ifpM](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t4P000002ifpM) (v20200724)

![](<../../../../.gitbook/assets/2 (85).png>)

Give Full Access to System Administrator and Naviga\_Admin Profiles

![](<../../../../.gitbook/assets/3 (78).png>)

![](<../../../../.gitbook/assets/4 (79).png>)

Grant access to these third parties on this prompt, these will be changed later (in this document)

![](<../../../../.gitbook/assets/5 (15).png>)

\\

<figure><img src="../../../../.gitbook/assets/6 (15).png" alt=""><figcaption></figcaption></figure>

1. In Salesforce, go to Setup -> Platform Tools -> Custom Code -> Custom Metadata Types -> Common Settings -> ManageRecords -> Edit “NavigaBaseURL”, update to your naviga ad base url. Will be formatted like this: https://XXX.navigahub.com/EW/XXX/
   1. The XXX will be replaced with your 3-digit site code.
   2. This can also be found in Naviga Ad System settings - Naviga Parameters: ![](<../../../../.gitbook/assets/image (1366).png>)
2. Go to Setup -> Security -> Remote Site Settings, Edit “NavigaAd” Remote Site Name, should be updated from https://devapps.msglcloud.com to https://xxx.navigahub.com
   1. same as above, the xxx can be found in the Naviga Parameters.
   2. Do not use the entire System Base Url. Only use the subdomain.domain.com portion.

![](<../../../../.gitbook/assets/9 (27).png>)

1. For communication (and authentication) between the Salesforce Org and Naviga Ad, we need one integration user account that exists in both places, but it must be a valid, accessible email address (due to later steps in this doc/process). We recommend something that indicates the purpose of the account, i.e. [naviga\_sfdc\_integration@yourdomain.com](mailto:naviga\_sfdc\_integration@yourdomain.com). This email account will need to be in hand and functional before continuing.
   1. Naviga Ad: This account must be created AND have a password set/initialized/validated before continuing.
      1. /general/setup/user\_admin.aspx, click on Create a New User
         1. Suggested: [naviga\_sfdc\_integration@yourdomain.com](mailto:naviga\_sfdc\_integration@yourdomain.com)
      2. An email will be sent to the account in question.
      3. Use the email to set/initialize/validate this account as a valid Naviga Ad User.
         1. This step must be completed before continuing.
   2. Salesforce: User accounts can be created at Setup -> Home -> Administration -> Users -> Users -> New User (button)
      1. The Profile should be a Naviga Admin.
      2. The User License should be Salesforce.
      3. Email: The email address should match EXACTLY (including case sensitive) the Naviga Ad User account created in the last step.
         1. Suggested: [naviga\_sfdc\_integration@yourdomain.com](mailto:naviga\_sfdc\_integration@yourdomain.com)
      4. Username: Can be anything you like as it is only used to log in to this Salesforce Org, which will likely be rare.
      5. You will need to login as this user and request a security token. Hint: to generate the security token, login as the new integration user you just created, from the ![](<../../../../.gitbook/assets/10 (5).png>)icon at top right, click and go to settings. From there, select “reset security token”. It will send the new security token to the email address you used when you created the integration user. Save this security token for later reference (in this document).
2. A note about user administration: Each Salesforce user’s email address must match (exactly, case sensitive) a Naviga Ad User email address, as this is what allows us to determine which Salesforce record and/or Naviga Ad record, or action upon a record, was performed by whom. The Salesforce integration (or communication) will simply not work without matching email address(es) in both places.

| Salesforce                                              | Naviga Ad                                       | Result |
| ------------------------------------------------------- | ----------------------------------------------- | ------ |
| [john@company.com](mailto:john@company.com)             | [john@company.com](mailto:john@company.com)     | Pass   |
| [John@company.com](mailto:John@company.com)             | [john@Company.com](mailto:john@Company.com)     | Fail   |
| [first.last@company.com](mailto:first.last@company.com) | [f.last@company.com](mailto:f.last@company.com) | Fail   |
| [JANE@company.com](mailto:JANE@company.com)             | [jane@company.com](mailto:jane@company.com)     | Fail   |

1.  Create the Naviga\_Integration connected app via Setup -> App Manager -> New Connected App

    1.  NOTE: A full list of settings/instructions are available below these screenshots\\

        <figure><img src="../../../../.gitbook/assets/11 (1).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../../../../.gitbook/assets/image (993).png" alt=""><figcaption></figcaption></figure>

\
**Call Back URL:** https://XXX.navigahub.com/ew/XXX/not\_used.aspx

1. The XXX will be replaced with your 3-digit site code.
2. This can also be found in Naviga Ad System settings -> Naviga Parameters: ![](<../../../../.gitbook/assets/image (1366).png>)

\
**OAuth Scope:** Full Access\
**Canvas:** Checked\
**Canvas App URL:** https://XXX.navigahub.com/ew/XXX/interfaces/salesforce/authentication.aspx\
**Access Method:** Signed Request (POST)\
**Locations:** Chatter Feed, Chatter Tab, Console, Layouts and Mobile Cards, Lightning Component, Visualforce Page\\

Everything else leave as default.

Save

There will be a warning “Allow from 2-10 minutes for your changes to take effect on the server before using the connected app”, it is generally advised to wait the 10 minutes before continuing.

If you receive any other validation errors, be sure that “Naviga\_Integration” is still in the API Name field as below, before saving.

![](<../../../../.gitbook/assets/15 (6).png>)

1.  Once the connected app has been created, modify the OAuth policies/properties:\
    Setup -> App Manager -> NavigaAd10 -> Manage\
    Permitted Users: Admin approved\
    IP Relaxation: Relax Ip Restrictions\
    \\

    ![](<../../../../.gitbook/assets/18 (3).png>)

    <figure><img src="../../../../.gitbook/assets/16 (5).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../../../../.gitbook/assets/17 (10).png" alt=""><figcaption></figcaption></figure>
2. Manage Profiles: Add System Admin, Naviga\_Admin (others as needed)

App Manager -> NavigaAd10 -> Manage -> Profiles (may need to scroll down)

![](<../../../../.gitbook/assets/19 (4).png>)

![](<../../../../.gitbook/assets/20 (10).png>)

1. Log into Naviga Ad and setup the Salesforce integration.
   1. Go to Setup -> Admin -> Salesforce Integration Setup
   2. Detailed settings information follow the screenshot.

<figure><img src="../../../../.gitbook/assets/image (166).png" alt=""><figcaption></figcaption></figure>

Enable Salesforce Integration: Checked/Yes\
Consumer Key: comes from the connected app view (yours will be different)

Setup -> App Manager -> NavigaAd10 -> View

Consumer Secret: Comes from the connected app view

<figure><img src="../../../../.gitbook/assets/image (200).png" alt=""><figcaption></figcaption></figure>

Security Token: Assigned to the Salesforce user after they are created, and the token was requested.\
User Name: Salesforce login for the integration user to use Salesforce APIs on the back end.

Hint: [naviga\_sfdc\_integration@yourcompany.com](mailto:naviga\_sfdc\_integration@yourcompany.com)

Password: Salesforce user password for the integration user

Note: After the user and connection is entered, save the settings, then reload the page. If everything connected, you should see line items in the cross-reference tables under Campaign and Opportunity Contact Roles. If you don’t or you get an error, there is an issue with connecting with that user’s info or managed app configuration.

1.  Assign the Naviga Account Layout and Naviga Opportunity Layout as the default for desired profiles (Naviga\_Admin, ??). The desired profiles will depend entirely upon how your company/organization uses profiles/roles within Salesforce.\
    ![](<../../../../.gitbook/assets/image (433).png>)\
    Setup -> Object Manager -> Account -> Page Layouts -> Page Layout Assignments -> Edit Assignments\
    Set the page layout for Naviga\_Admin, and other profiles used by your company, to Naviga\_Account\_Layout

    Repeat the above for Opportunity: Setup -> Object Manager -> Opportunity -> Page Layouts -> Page Layout Assignments -> Edit Assignments -> Naviga Opportunity Layout -> Save
2.  Assign the Naviga Compact Layout for Account and Opportunity as the default.\
    Setup -> Object Manager -> Account -> Compact Layout -> Compact Layout Assignment -> Edit Assignment

    Set the default compact layout to Naviga\_Compact\_Layout\
    ![](<../../../../.gitbook/assets/image (1180).png>)\
    Repeat the above for Opportunity \[Naviga Opportunity Compact Layout]
3. Add the Search Naviga button to the Account List View.

Switch to Salesforce Classic

![](<../../../../.gitbook/assets/image (1062).png>)\\

Setup -> Build -> Customize -> Accounts -> Search Layouts -> (Edit) Accounts List View\
![](<../../../../.gitbook/assets/image (392).png>)

Add the Search Naviga button to the account list view.\
![](<../../../../.gitbook/assets/image (1107).png>)

1. Switch to Lightning Experience\
   ![](<../../../../.gitbook/assets/image (856).png>)

Add the Naviga Reports visual force page to the default lightning home page.\
Go to Select Sales and select Home\
<img src="../../../../.gitbook/assets/image (1513).png" alt="" data-size="original">\
Click on the <img src="../../../../.gitbook/assets/image (307).png" alt="" data-size="line"> and select Edit Page.\
Drag the Visualforce icon up to the top of the first column then release it. Set the Visualforce Page Name to Naviga\_Reports\_List and the Label to Naviga Reports.\
Save.

Activate the page as the “Org Default”.\\

<figure><img src="../../../../.gitbook/assets/image (1226).png" alt=""><figcaption></figcaption></figure>

1. Add the Naviga Links visual force page to the default Lightning home page.\
   Click on the <img src="../../../../.gitbook/assets/image (1378).png" alt="" data-size="line"> and select Edit Page.\
   Drag the Visualforce icon up to the top of the second column then release it. Set the Visualforce Page Name to Naviga\_Custom Links and the Label to Naviga Links.\
   Save.

Activate the page as the “Org Default”.

![](<../../../../.gitbook/assets/image (1086).png>)\
\\

1. Switch to Salesforce Classic and click Setup (link, upper right)

Search for Home and select Home Page Layouts\
Add the Naviga Default page assignment for the Classic Home Page assignment.\
![](<../../../../.gitbook/assets/image (1401).png>)\
Select Page Layout Assignment and use Naviga\_Default for the desired profiles.

1. Test Canvas connectivity by switching to the Sales app. Select Accounts and list Naviga Account List. From the list, click on the Create Naviga Account link. If everything works, you should see the Naviga Ad Naviga Account Search page with a button to create a new account or link an existing one.

![](<../../../../.gitbook/assets/image (739).png>)

![](<../../../../.gitbook/assets/image (1609).png>)

## Additional Configuration in Naviga:

Under Integration Settings, Salesforce node, you will see several options at the bottom of the screen (settings at the top discussed above)

<figure><img src="../../../../.gitbook/assets/image (768).png" alt=""><figcaption></figcaption></figure>

* **Automatically Create Accounts in Salesforce when created in Naviga** - When an account is created in Naviga, if this is set to yes, the account will be auto-created in Salesforce as well. If your workflow is that accounts are first created in Salesforce, this should be marked as 'no'
* **Allowed to Link Agencies** - When in Salesforce, and you are searching for an account in naviga (generally to link an existing naviga account to a salesforce account), setting this to no, will not allow you to search on ad agencies.
* **User Order Taker as Rep** - When set to yes, the order taken in Salesforce will be used as the order rep for the order, regardless of who the account rep is on the brand in Naviga.
* **Security Group(s) that should NOT have access to standard Naviga Ad menu(s) when in another browser tab** - For most of our clients, sales people spend 100% of their time inside salesforce and do not enter the naviga application at all, except for those pages that are accessed via the Salesforce Canvas integration. For other users, like admins or finance users, they might bounce back and forth between the full naviga application and saleforce. This setting allows you to set which security groups should NOT have access to the main naviga navigation menus if they are logged into both Naviga and Salesforce simultaneously.

On the cross reference tables node, set up the links between Naviga Campaign Statuses and Salesforce Opportunity Stages (Note, your stages in Salesforce will likely differ from the sample below):

<figure><img src="../../../../.gitbook/assets/image (360).png" alt=""><figcaption></figcaption></figure>

The integration will update Stages as needed between the systems. (For example, in the above sample, when an order in Naviga moves from a Quote to R1 status, the Salesforce opportunity will automatically update to Closed Won.

On the Opportunity Contact Roles node select Yes/No as desired on each contact role you have defined in Salesforce. Your roles may differ from the examples below:

<figure><img src="../../../../.gitbook/assets/image (441).png" alt=""><figcaption></figcaption></figure>

The Sync node displays Accounts, Opportunities, Reports and Shortcuts that are sync'd between the systems.

<figure><img src="../../../../.gitbook/assets/image (1594).png" alt=""><figcaption></figcaption></figure>

It is unlikely that you will need to come into this screen regularly, but it can be used to remove a sync if needed.

Here is a short video of the Naviga Ad and Salesforce integration using the Salesforce Canvas framework:

{% embed url="https://dev.navigahub.com/mothership/resources/videos/NavigaAdSalesforceIntegration.mp4" %}
