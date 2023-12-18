# Group Security

## Security Group Setup <a href="#_toc79061543" id="_toc79061543"></a>

1. Leave the group ROOT as setup by default with the software. This group is the highest-level user group and comes with no restrictions. This is the group assigned to Naviga Admins
2. Navigate to the System Settings module’s menu Security -> Group Security -> Security Group setup.
3. Create new groups as needed.
   1. User groups can be deleted.
   2. Users can be added to groups.
   3. User groups’ access can be edited

Can select "**Users in Group**" node to see the users that are assigned to each group.

## Group Security Setup Per Module <a href="#_toc79061552" id="_toc79061552"></a>

To setup the access permissions of a security group per module, navigate to the System Settings module -> Security -> Group Security

This same screen can also be accessed from

* Advertising -> Setup -> Admin -> Group Security Setup
* CRM -> Setup -> Group Security Setup
* Exhibitions -> Setup -> Group Security Setup
* A/R -> Setup -> Admin -> Group Security

### Audit Report

Navigate to Group Security from the Setup Menu and select the Audit Report at the top of the screen. Select any desired groups from the left column and move them into the right column using the arrows in the center.

<figure><img src="../../../.gitbook/assets/image (1476).png" alt=""><figcaption></figcaption></figure>

Click Generate report button at the bottom of the screen. Depending upon the number of groups selected, this could take a couple of minutes to run. The following excel report will automatically download.

{% hint style="danger" %}
With over a dozen tabs and each tab having a column for each security group - this isn't a report you should be running for dozens of groups at a time. The process will time out after 90 seconds. If the spinning graphic closes and no file is downloaded, you have requested too much data. Actual number of groups a site can download successfully will vary based on the number of users you have in the system and the data being downloaded, but I would advise against attempting more than a dozen groups at one time.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (555).png" alt=""><figcaption></figcaption></figure>

The selected security groups will be across the top and the modules, menus and permissions that the user group has will be displayed. Note the multiple tabs across the bottom of the report. This separates Module Security, Menu Security and then all of the Group Security nodes (note "Digital Security" is Advertising Security on screen), and then finally after all the Group Security tabs is a list of active and inactive users along with which security group that person is in.

### General/ Company Security <a href="#_toc79061554" id="_toc79061554"></a>

This node allows you to provide access to the various companies.

Choose the group from the drop-down menu to setup.

#### General Security

1. **Disable Grid Export and Screen Selection Features** - Click the box to indicate “Yes” only if you want users to not have access to exporting reports to Excel and PDF. Leave as “No” if you want to allow users to perform the export. The export capability allows users to utilize the data and email it to other user.

#### Company Security

1. **Allow All Companies** - Click the box to “Yes” to allow all users in this group access to all companies you created. Selecting yes here will gray out the option below.
2. **Specific Companies** - highlight one or more companies in the table and click the right arrow to allow users in the group access to this company.

#### Main Menu Shortcuts

When a user logs into the system they are presented with tiles of modules that they can access. To the right of the system modules, the user can also create their own personal shortcut tiles to various screens in the system. This must be created by each individual user for themselves since they are personal shortcuts.\
\
By creating shortcuts here in group security, admins can create some standard shortcuts for those users.

<figure><img src="../../../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure>

These shortcuts are also then accessible from the Main Menu dropdown from the menu bar that is displayed throughout the system. These Shortcuts are labeled with "Group Default:" and the Description from the shortcut setup.

<figure><img src="../../../.gitbook/assets/image (1693).png" alt=""><figcaption></figcaption></figure>

### Name Security <a href="#_toc79061555" id="_toc79061555"></a>

This node’s settings allow users to view, edit or have no access to a particular module. Choose the group from the drop-down menu to setup.

#### Basic Permissions

Select Yes/No to these Name Maintenance options

1.  **Allowed to Access Name Maintenance Screens** - Saying Yes here will allow you to see this Name Maintenance Screen: (Customers -> Advertiser / Agency Maintenance)

    <figure><img src="../../../.gitbook/assets/image (980).png" alt=""><figcaption></figcaption></figure>
2. **Allowed to Create New Names** - In the above screenshot there is a + to the right of the account ID. If this is set to yes, the + will be enabled. If this is set to no it will be grayed out.
3. **Allowed to set/unset the Do not use option** - In the top right of the above screen is a do not use flag. If this is set to Yes the user will be able to set/unset this flag. If this is set to no, the flag will be grayed out and not selectable.
4.  **Allowed to change employer** - If viewing the Name/Maintenance screen of an individual, with this flag set to yes, the user will be able to click the button labeled "Change Empoyer." Otherwise, the button will be grayed out.

    <figure><img src="../../../.gitbook/assets/image (458).png" alt=""><figcaption></figcaption></figure>
5.  **Allowed to change Legacy ID's** - With this set to yes the user will be able to add and delete Legacy ID's on the Name and Address screen. With it set to no, the two boxes below will be hidden:

    <figure><img src="../../../.gitbook/assets/image (782).png" alt=""><figcaption></figcaption></figure>

#### Module Permissions

Still on the Name/Agency Maintenance Screen, each of the below modules can be labeled as View and Edit, View only, or No Access. View only, they will see all the settings, but not be able to change anything. No Access means they will not even see the node on the left side. View Edit means they can make changes.

1. Name / Address
2. Accounts Receivable
3. Advertising
4. Exhibition
5. Alerts

### A/R Security <a href="#_toc79061556" id="_toc79061556"></a>

This node determines the level of details of access for the security group within the accounts receivable module.

[See A/R Documentation for details of these security settings](../../accounts-receivable-credit-control/setup-a-r-system-setup/admin-menu.md#\_toc124065024-1)

### A/P Security <a href="#_toc79061557" id="_toc79061557"></a>

This node determines the security access of the different groups in the module Accounts Payable.

[See A/P Documentation for details of these security settings](../../accounts-payable/setup/admin/group-security-a-p.md)

### G/L Security <a href="#_toc79061558" id="_toc79061558"></a>

This node allows you to setup the General Ledger module security options per group. This includes the journal entries and Cash Entries.

[See G/L Documentation for details of these security settings](../../general-ledger/setup/admin/group-security-g-l.md)

### Production Workflow <a href="#_toc79061559" id="_toc79061559"></a>

This node determines the security of production workflow in the Ad Module which handles the materials on orders as well as the third party preflight settings.

[See Ad Documentation for details of these security settings](../../advertising/setup/admin/group-security-ad.md#production-workflow)

### Advertising Security <a href="#_toc79061561" id="_toc79061561"></a>

This node determines the level of details of access for the security group within the advertising module.

[See Ad Documentation for details of these security settings](../../advertising/setup/admin/group-security-ad.md)

### Exhibition Module Security <a href="#_toc79061562" id="_toc79061562"></a>

This node determines the level of details of access for the security group within the exhibition module.

[See Exhibition Documentation for details of these security settings](../../exhibitions/setup/group-security-exhibitions.md)

### Product Security

These settings control Product Group Access for both Exhibition Product Groups and Advertising Product Groups.

1. **Product Groups:** Choose the allowed product groups by clicking on the name of the group in the left side table and then click the right arrow to move to the right-side table. There is a search filter at the top of the list to assist in finding groups where there are long lists of product groups.
2. **Apply Product Group security to Client Inquiry and When Selecting Cash on Account to Apply to a Campaign:** This option, when checked, applies the setting of product security access here to the user in this group when searching for a client in the client inquiry screen and applying COA to a campaign. So, a user who isn’t setup to view certain groups in this section cannot view these items on a client record either.

{% hint style="info" %}
For example: Assume User 1 has access to only Product Group 1 and User 2 has access to only product Group 2. Customer A has a campaign that is for Product Group 1. If option two is set to yes for both users' groups, then looking at the same customer account, Sales User 1 will see the order, but Sales User 2 two will not.

If option 2 is set to no in the above scenario, both reps will see that the client has placed the order....but only Rep 1 would have been able to book the order since Rep 2 dosen't have access to that product group
{% endhint %}

### CRM Security <a href="#_toc79061565" id="_toc79061565"></a>

This node determines the level of access users in a certain security group have for CRM module.

[See CRM Documentation for details of these security settings](../../crm/setup/group-security-crm.md)

### Copy Group Settings <a href="#_toc79061566" id="_toc79061566"></a>

This node saves the admin time and effort and will copy the settings of one group to another, which the admin can then edit as applicable.
