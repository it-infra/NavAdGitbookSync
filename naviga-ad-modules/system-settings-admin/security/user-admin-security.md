# User Admin / Security

## User Setup / Administration <a href="#_toc79061544" id="_toc79061544"></a>

The User Administration screen displays license metrics at the top of the screen so you can see how many users you are licensed for, how many are in use, and how many are available. For most installations the first column is the only one in use, but there are some special limited use licenses available for certain timesheet and A/P approval functions.

Be sure to mark inactive users as inactive to free up licenses as needed.

<figure><img src="../../../.gitbook/assets/image (935).png" alt=""><figcaption></figcaption></figure>

#### Setup and inactivate Users

1. Create a new user by navigating to Systems Settings module and one of the following menu options:\
   Setup -> User Administration\
   Security -> User Administration
2. Click on Create a New User
3. Enter user name (might be first initial last name, first name dot last name, email address, etc, according to your chosen naming convention, but it must contain no spaces and will be forced to all lowercase)
4. Enter First name, last name, and email address - email address will be used to send user a link to setup their password - so double check for typos before saving)

<figure><img src="../../../.gitbook/assets/image (1328).png" alt=""><figcaption></figcaption></figure>

4. Security Group - User can be assigned to the different security groups based on their role and will therefore inherit the security access of their group. (see [Group Security](group-security.md) for more information)
5. If the user is an administrator, select yes. Only administrators will be permitted to create new users, access group security, menu security and module security.
6. License Type will typically be left blank for a regular system user. A user with permissions limited to A/P approvals or timesheet approvals will only be able to access those functions. This user is defined as someone who can only approve invoices and payments. Note that she doesn't have access to any modules at all, but does have custom shortcuts to Invoice Payment Approval and Invoice Approval:\
   ![](<../../../.gitbook/assets/image (945).png>)\
   \
   Similarly, a user that has a license type which only allows timesheets, will be limited to only entering in Timesheets (timesheets are part of the Production/Job Costing Module):\
   ![](<../../../.gitbook/assets/image (1156).png>)\
   \
   The above shortcuts were created automatically for these users. No other shortcuts can be created.
7. Once the data is entered, the system sends the password information to the email in this pop-up to allow user to login.

![](<../../../.gitbook/assets/image (1336).png>) User can be edited from this screen as well. Click the pencil icon to edit the user.

![](<../../../.gitbook/assets/image (468).png>) This option will send password recovery information to this user via email. It will not invalidate their current password until it is changed. If a user did not receive the initial password setup email when their user was created, click this icon to re-send it.

![](<../../../.gitbook/assets/image (289).png>) This option will force the user to set a new password on next login. Do not use this option if the user has forgotten their password, instead us the Password Recovery Option (the yellow key).

## User Security <a href="#_toc79061550" id="_toc79061550"></a>

Users’ security is setup from System Settings module -> Security -> User Security, or from the Setup menu in each of the different modules.

### General Settings

#### User Settings

The user settings node allows for the user’s security group and ID display.

**Contact Information:**

Personal contact info can be entered in here. The From name may be different from how the user's name was setup in system setup. This allows the user to customize how their name appears in outgoing corresponsence. Phone and profile picture can be added if desired. This Profile Picture will appear with the Rep's performance information in the CRM.

**General Settings:**

In the General Settings section , the “Time Zone” is a mandatory field for the user to be able to operate the system. Greenwich Mean Time is the default, but it should be edited to be the correct time zone. Desired main menu behavior is also set here. One can either use the CRM main menu or the default. If the user is set to "Use the CRM Main Menu" then they will see these tiles at the top of the screen throughout the CRM Module:

A CRM Sales Manager will see these tiles:

<figure><img src="../../../.gitbook/assets/image (969).png" alt=""><figcaption></figcaption></figure>

A CRM Sales Rep will see these tiles:

<figure><img src="../../../.gitbook/assets/image (707).png" alt=""><figcaption></figcaption></figure>

If the user is setup to "Use the Default Main Menu" then these tiles will not be displayed at all.

If the the User was setup as an administrator with the Administrator flag in User Administration, the user will be able to edit these User Security screens. Without the Admin Flag, only some of these fields will be editable.

#### Rep/ User Integration

In the Proposals setting section of this node, the following settings can be set:

<figure><img src="../../../.gitbook/assets/image (58) (1).png" alt=""><figcaption></figcaption></figure>

1. The email address(es) set here will determine who is notified if a proposal is signed by the client in the portal. Depending on your organization structure the rep themself may be notified, it it might be a sales ops person who will take it from there
2. Items 2 - 5 on this list control who gets notified if the selected user is the rep on the campaign, and the status changes to R1, R2, R3 or CO. The email will be sent from the person who made the change to the person(s) listed here.

This node shows the data which determines the Sales Rep groups which this user has access to by highlighting the group on the left side table and clicking the arrow pointing right to allow the group. At least one group is required to access reports such as the Orders by Product Report.

Ad Rep <--> User ID Associations associates the user ID to a sales rep ID. The sales reps are set up separately in the system because 1-not all users are a sales person and 2-not all sales people are users of the system. If you are a rep, and you are a licensed user of the system, this will link your user ID with your rep ID. In some rare cases there is more than one rep associated with a user ID, but in most scenarios this is a 1:1 relationship. If you are not a rep, this will be blank.

#### Account Activation History

This will track if a user was marked as inactive / active. It will display who made the change and when.

### CRM

The CRM Access Control node determines the user’s type of CRM access:

* The user can be setup as a sales rep or a sales manager. This will determine the rep’s access to other reps information. In conjunction with the [General settings](user-admin-security.md#general-settings) "main menu" choice to It will also determine which set of tiles get shown at the top of the screen, if you choose to "Use the CRM Main Menu".
* Default State / Region ID will set the default state on new clients. This can be left blank if you do not wish to set a default.
* The default Opp. Type field value will default in selected Opportunity type when user creates a new opportunity. This is designed to save the rep time during entering opportunities if the rep specializes in selling only one type.
* One or more of the Sales Order Entry Access fields can be set to Yes or No to allow the user to enter new orders for Exhibition or Advertising. If these both say no, in the CRM you will not see the menu for Advertising and/or Exhibition
* The user can also have access to specific reps, a specific rep group, or to all reps, as decided by the field “Access to Other Reps”. One or more or all reps can be selected from the drop down menu.

#### Managers Home Page

* CRM Home Page / Menu - If a user's security is set that they use the CRM Main Menu, this will control which tiles are displayed to the Manager when they first log into the system. If the option is set to rep home screen the rep tiles will be displayed\
  <img src="../../../.gitbook/assets/image (70) (1).png" alt="" data-size="original">\
  \
  If the option is set to use the manager home screen the manager tiles will be displayed:\
  ![](<../../../.gitbook/assets/image (71) (1).png>)\
  \
  Managers can always use the far right tile to toggle to the alternate view.
* Default Product Group - Will only display if user is set to allow Ad Sales. This controls what the default product group is on the manager's Rep Activity screen. Dropdown includes only the Product groups that the user has access to through group security.
* Default Exhib. Group - Will only display if user is set to allow Exhibition Sales. This controls what the default product group is on the manager's Rep Activity screen. Dropdown includes only the Product groups that the user has access to through group security. If the user has access to both Ad and Exhibitions, the Ad setting will trump whatever is in the Exhibition Group field.
* Reps To Display - This controls which reps display on the Rep Activity screen. One or more reps can be assigned to the sales manager from the “Reps to Display” field by using the arrows to move reps to the Display or the Do Not Display box. Only reps that were allowed in the Access Control settings will be displayed here

#### Rep Home Page

* **Campaign Delivery:** Delivery stats can be displayed on the Reps home page or not depending on what is set here
* Show all To Do's by default: If set to no, only To Do's for today and past days will be displayed on the Home Page. If set to yes, future to do's will also display

#### Rep summary Page

* Whether the user is a sales manager or a rep, his summary page defaults can be defined in the “Rep summary Page” node. This is the page which will display when user navigates to the CRM module on System and clicks on the Rep Summary menu. The page will display the list of products figures and charts for all orders, opportunities and proposals for this rep. User can move the assigned products below at any time to the unassigned box and vice versa.

#### Email and Calendar Integration

* Email and Calendar Integration enables the user to view the emails they sent or received to and from a client. Only contacts that are labeled "My Contacts" will sync. This utilizes a 3rd party called Nylas and must be set up by Naviga Hosting before it can be used in your system. Discuss with your Implementation Specialist or Naviga Support if you wish to enable this function. Only Google Suite and Outlook emails are supported.
* Once enabled, users can view the emails on the customer record inside Naviga Ad according to the settings below and can also “Force Sync” the emails to display in System CRM module.
  1. The “Connection Details” settings include the user’s email address and password. To authorize connection, the user must click Authorize Connection and be re-directed to their email login prompt to authorize Naviga to sync their emails.
  2. The Enable Email Sync and Enable Calendar Sync are set to Yes to start the synchronization process.
  3. The Email Folders field if left blank will synchronize the Inbox and Sent email folders. User can choose other folders separated by a semi colon.
  4. The synchronization range of days for the calendar is determined by the numeric values entered in “Sync Days Before Today” and “Sync Days After Today”. This is only used for the initial sync.
  5. More setup is performed from the menu “Integration” under the Setup/Admin module in System. Please refer to the heading “Integration” below.

### Advertising

* The “Advertising User Settings” node determines the settings for the advertising module for this user.
  1. The “Default Product Group” field will pre-fill the selected Product Group onto the Campaign Header in order entry.
  2. The “Production Controller” field is set to Yes if the user is the controller and left No if he is not. If set to Yes, the user’s name will display in the Production Controller dropdown field throughout the system.
  3. I Can Approve Campaigns: Set to yes if the user is permitted to approve campaigns from the Campaigns -> Campaign Approvals screen. Those who are set to yes will display on the "Approval Users" dropdown on that screen if user has Campaign Approval Scope set to I Can approve for anyone. Otherwise user will see a filtered list of approvers based on if the used can only approve for themself or those in their security group.
  4. “Default Home Page” is the default home page displaying for the user when he logs into the advertising module. It could be:
     * Ad Home Page displaying the reports, and history of user’s activities.
     * Production Home Page displaying the products and production statuses for both print and digital orders.
     * Executive Homepage & navigation - will display the same as the ad home page plus navigation icons to various executive reports and summary ofconfirmed orders in the last week, month, quarter, etc.\
       \
       The Ad Home and Production screens can also be viewed if user navigates to the Advertising module and clicks on Ad Home menu, and chooses the Ad Home Page or the Production Home Page.
  5. Products listed at the bottom of the screen determines the products displaying on the user’s Production Home Page.

### Accounts Receivable

This node determines the settings for the user’s Accounts Receivable module.

1. If “User Type” is set to Default A/R User, then the user will be able to perform all accounts receivable functions from that module as determined by the group security and module security. For instance, apply check or credit card payment, create batches, apply credit and so forth.
2. If “User Type” is set to “Credit Controller”, then the user will be able to be assigned as a Credit Controller on a client and be able to view his activities for every account. For example, calls or emails for each client and drill down into each action item. User will also be able to view the Customer Overview screen and apply credit or make payments as allowed by the group security access. The same screen can be viewed as the home screen when user logs into the Account Receivable module. Also it can be viewed when user clicks the menu Credit Control and then choose “Controller Home”.
3. If “User Type” is set to “Credit Manager”, then user will be able to do the same as in item 2, but for all of his subordinate credit reps who are assigned to him. If a user is a credit manager the Team of Credit Controllers will be displayed on screen and a manager can be limited to only certain controllers.

The same screen can be viewed as the home screen when user logs into the Account Receivable module. Also it can be viewed when user clicks the menu Credit Control and then choose “Manager Home”.
