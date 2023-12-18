# Email Integration Monitor

## Email Integration Monitor

### Nylas Integration

For those who are using the Nylas Email Integration, there is visibility into the emails that are / are not matching to accounts within Naviga Ad.

Navigate to **System Settings Module -> Integration -> Email Integration Monitor**

<figure><img src="../../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

A user will be displayed in this list if one or both of these settings is selected on their profile:

<figure><img src="../../../.gitbook/assets/image (61).png" alt="" width="340"><figcaption></figcaption></figure>

If the user enters an email address in the profile email integration tab (above screenshot) and authorizes connection to that email, then the other columns from the first screenshot will be populated as well.

The Nylas Sync State lets an admin know the status of the sync.

Possible options here are:  valid┃invalid┃downloading┃running┃partial┃invalid-credentials┃exception┃sync-error┃stopped┃initializing

The meanings of each status is described below (taken from the [Nylas website](https://developer.nylas.com/docs/developer-guide/manage-accounts/account-sync-status/#monitoring-sync-states-in-the-nylas-dashboard))

<table><thead><tr><th width="148">Sync state</th><th width="109">Simplified</th><th width="111">Detailed</th><th>Description</th></tr></thead><tbody><tr><td>valid</td><td>x</td><td></td><td>All emails for folders, contacts, and calendars are syncing reliably.</td></tr><tr><td>invalid</td><td>x</td><td></td><td>The account has an authorization issue and needs to be re-authenticated.</td></tr><tr><td>downloading</td><td>x</td><td></td><td>All folders are connected and the account is in the process of syncing all historical messages on the account. Depending on the size of the account and the speed of the connection between Nylas and the email server, this can take up to 24 hours or more to complete. During this time, the account is usable for sending messages and receiving new email messages.</td></tr><tr><td>running</td><td></td><td>x</td><td>All emails for folders, contacts, and calendars are syncing reliably.</td></tr><tr><td>partial</td><td></td><td>x</td><td><p>Partial states are typically temporary and may indicate issues with the mail server. Accounts in this state, however, are still running.</p><p>One or more folders in the account may not fully sync currently or not sync mail at all. Typically, accounts recover and return to a full-running state.</p><p>Some reasons an account may be in a partial state:</p><ul><li>It's a new account and hasn't finished its initial sync.</li><li>The account was recently reauthenticated.</li><li>The user deletes, changes, adds, or restricts folders.</li><li>Slow network connections.</li><li>Low bandwidth on the email server.</li><li>A backlog within the Nylas platform.</li><li>A large number of folders in the user's mailbox.</li><li>Syncing historical data</li><li>The user has external integrations that may be slowing down their email server.</li><li>The user’s email server has connection or network issues.</li><li>Microsoft accounts with numerous folders.</li></ul></td></tr><tr><td>invalid-credentials</td><td></td><td>x</td><td>You can only continue to use an account with the Nylas API as long as the &#x3C;ACCESS_TOKEN> is valid. Sometimes, this token is invalidated by the provider when connection settings are changed or by the end-user when their password is changed. When this happens, reauthenticate the account and generate a new &#x3C;ACCESS_TOKEN> for the account.</td></tr><tr><td>exception</td><td></td><td>x</td><td>This can occur if an upstream provider returns an error that Nylas's sync engine doesn't yet understand. Please contact Naviga Support for accounts in this state.</td></tr><tr><td>sync-error</td><td></td><td>x</td><td>An unexpected error was raised while syncing an account. Please contact Naviga Support for accounts in this state.</td></tr><tr><td>stopped</td><td></td><td>x</td><td>An account stops syncing if it repeatedly encounters the same error or is unable to access the email server. In cases where an account has stopped, you can try to restart it using the downgrade and upgrade endpoints. If the account continues to fall into a stopped sync state, please contact Naviga Support.</td></tr><tr><td>initializing</td><td></td><td>x</td><td>The account has been authenticated on the Nylas platform and is in the process of connecting to all the account's folders. Accounts that use email.send as the only scope will always be in an initializing state. Nylas uses folders to determine sync status. email.send doesn't fetch folders.</td></tr></tbody></table>

Under the email to sync column is a link to View Sync History for each user. Click on that link for a popup of all the matched and unmatched emails that have been processed.  During testing and initial implementation of the Nylas email sync feature, users will often be looking for specific emails and asking questions about why something may or may not have shown up as linked to a customer account. This gives admins of the system additional visibility into the processed emails.

<figure><img src="../../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

On the matched emails tab, the subject is displayed as a link and the admin user can click on it to view the text of the email, the same as they would see should they see that email on the customer/contact account record or the managers rep activity screen.  Unmatched emails will not have a link to read the text of the email for individual privacy reasons.

### Email BCC / FWD Sync

In some cases, a media company may prefer to allow users to pick and choose which emails to sync by forwarding or bcc-ing emails to a monitored email address rather than using the Nylas integration, which will automatically scan the users inbox and sent mail (or other designated folder). &#x20;

The plus side of using email BCC/FWD instead of Nylas is that there is more control for the users to pick and choose which emails to send into the system.  The downside of using email BCC/FWD is that there is more control for the users to pick and choose which emails to send into the system.  With the control being on the user, they can cherry-pick the positive emails and not sync if the client is unhappy with them.  Allowing the user to pick the emails does allow them to keep the system more tidy though and eliminate syncing the clutter that might not be relevant to keep.

Navigate to **System Settings Module -> Integration -> Email Forward and/or BCC Configuration**

{% hint style="info" %}
<mark style="background-color:green;">Note - the BCC integration is ready to go.  We are still fixing some remaining issues with the FWD, so don't enable that one in your PROD system just yet.</mark>
{% endhint %}

Select Yes to enable the bcc and/or forward integration. Once the gmail account is configured, it will be selected from the dropdown in step 3, below:

<figure><img src="../../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

Click on the Connection Setup link from screenshot above.

<figure><img src="../../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

Click New and give the connection an ID and a Description.  The Connection Settings section will be filled in after following the steps below to create a gmail account and to get the Client ID and Client Secret from the Google Development Console.

To set up the email BCC/FWD integration, an admin must first setup the account which will be used for forwarding.  We have standardized this using a google email address. If you are using G-Suite as your email system, you can use something like navigasync@yourdomain.com, or you can just create a free gmail account and use that.  The important part is that you are able to get to the Google Developer Console to give your naviga ad instance oauth access to the mailbox to be able to actually sync the emails.

Follow these steps to enable the sync:

1. Create Gmail Account (If needed)
2. Navigate to Google Cloud: [https://console.cloud.google.com/](https://console.cloud.google.com/)
3.  Make sure upper right hand corner of webpage has email account selected – if not select and log into that email account:\


    <figure><img src="../../../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>
4. If this is the first time using Google Cloud, you may have to agree to terms of service:\
   ![](<../../../.gitbook/assets/image (67).png>)\

5. Select a project and choose New Project:\
   ![](<../../../.gitbook/assets/image (68).png>)\

6. Give it any name and choose Create:\
   ![](<../../../.gitbook/assets/image (69).png>)
7. Once the creation is done, choose Select Project:\
   ![](<../../../.gitbook/assets/image (70).png>)
8. Under APIs and Services, choose OAuth consent screen:\
   ![](<../../../.gitbook/assets/image (71).png>)
9. Choose External and then Create:\
   ![](<../../../.gitbook/assets/image (72).png>)
10. Give the application a name (any name) and select your email address from the list:\
    ![](<../../../.gitbook/assets/image (73).png>)
11. Skip the app logo and App domain sections and then use any email address for Developer Contact and click Save and Continue:\
    ![](<../../../.gitbook/assets/image (74).png>)\

12. Click Add or Remove Scopes:\
    ![](<../../../.gitbook/assets/image (75).png>)
13. Under the manually add scopes add these and click Add to Table:\
    [https://www.googleapis.com/auth/gmail.readonly](https://www.googleapis.com/auth/gmail.readonly)[https://www.googleapis.com/auth/gmail.modify](https://www.googleapis.com/auth/gmail.modify)\
    ![](<../../../.gitbook/assets/image (76).png>)
14. Select ../auth/userinfo.email and openid from the top section (in addition to the two you added):\
    ![](<../../../.gitbook/assets/image (77).png>)
15. Click update at the bottom of the window and then Save and Continue. On the Test users screen you can leave it empty and choose Save and Continue:\
    ![](<../../../.gitbook/assets/image (78).png>)
16. Choose Back to Dashboard and then Publish App:\
    ![](<../../../.gitbook/assets/image (79).png>)
17. Once the pop-up is displayed to push to production, click Confirm:\
    ![](<../../../.gitbook/assets/image (80).png>)
18. Next click Library to go to the list of available APIs:\
    ![](<../../../.gitbook/assets/image (81).png>)
19. Type in gmail and hit enter to search for the gmail api:\
    ![](<../../../.gitbook/assets/image (82).png>)
20. Choose Gmail API and then click enable:\
    ![](<../../../.gitbook/assets/image (83).png>)
21. Next choose Credentials from the left menu and then Create Credentials at the top:\
    ![](<../../../.gitbook/assets/image (84).png>)\
    ![](<../../../.gitbook/assets/image (85).png>)\

22. &#x20;Choose OAuth client ID:\
    ![](<../../../.gitbook/assets/image (86).png>)
23. &#x20;Chose Web application for the Application type.\
    ![](<../../../.gitbook/assets/image (87).png>)\

24. &#x20;Chose any name for the Name field.\
    \
    For Authorized JavaScript origins use the first part of the url of the Naviga System. If there are test or dev systems with a different prefix, include them here as well. For example, our dev system the base url is this: [https://dev.navigahub.com](https://dev.navigahub.com/) yours will be your 3-digit site code where we have "dev"\
    \
    For the Authorized redirect URIs, you need to use the full URL or the screen you will be authorizing your connection on. For example, our dev system the full url is this: [https://dev.navigahub.com/ew/devdigital/general/setup/oauth\_connections](https://dev.navigahub.com/ew/devdigital/general/setup/oauth\_connections)\
    \
    NOTE – the url above is case sensitive so be sure it matches what you have in your browser URL. If EW or your 3-digit site code are capitalized, be sure to capitalize in the Authorized redirect URIs\
    ![](<../../../.gitbook/assets/image (88).png>)\

25. &#x20;Once you click Create you will get a pop-up with some important information:\
    ![](<../../../.gitbook/assets/image (89).png>)
26. &#x20;In the Naviga Ad system you will need to go to the URL that you specified in the prior step and create a new connection:\
    ![](<../../../.gitbook/assets/image (90).png>)
27. &#x20;Click save so the connection is saved just in case there is a problem with the authorization. When you are doing the authorize it needs to redirect to Google and then comes back to the Naviga Ad system.\
    \
    Click Authorize and then choose the email address (you may have multiple displayed if you have multiple gmail accounts):\
    ![](<../../../.gitbook/assets/image (91).png>)
28. &#x20;You may recall when setting up the OAuth Consent screen Google gave you a message about the App needing to be verified. Because the application has not been verified you will get a screen that looks like this:\
    ![](<../../../.gitbook/assets/image (92).png>)\
    \
    \
    Choose Advanced and then Go to navigahub.com (unsafe). This doesn’t make you any less safe, it is just google trying to protect your account. In this case you were the one that created the Google Cloud Account.\
    ![](<../../../.gitbook/assets/image (93).png>)
29. &#x20;Next you will get the Google screen asking you for access to read and compose messages in this gmail account. You need to select continue to proceed:\
    ![](<../../../.gitbook/assets/image (94).png>)
30. &#x20;Assuming everything went ok, you should be back on the Naviga Ad screen with a green banner saying the connection was authorized. Just click save to make sure that everything was saved:\
    ![](<../../../.gitbook/assets/image (95).png>)

Once this has been enabled, users can start to BCC the created Gmail sync email account on emails sent to their clients.  They can also forward emails received from their clients to that same email address and, if matched with an email in the system, the email will sync to the customer's account in the same way that the Nylas emails sync.

Back in the Email Integration Monitor, these BCC and FWD events will be displayed in the matched/unmatched tabs in the users sync history. Admins can tell how the email came into the system by looking at the source:\


<figure><img src="../../../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>
