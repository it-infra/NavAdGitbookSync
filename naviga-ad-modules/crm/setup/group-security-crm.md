# Group Security (CRM)

There are some complex controls around who can do what in the CRM module. For easier navigating, this node has sub-groups under it and each item is numbered.

For Information on Group Security for other Modules, see the respective module documentation or [System Settings Group Security](../../system-settings-admin/security/group-security.md)

## Group Selection

1. Choose the group ID from the drop-down menu and view the description matching it.

## **User Defined Fields**

1. Restrict User Defined Fields to Only the Following: This is a list of UDFs allowed and not allowed to display and be used by moving them from one list to the other using the arrows.

## **Complimentary Subscriptions**

1. Restrict Complimentary Subscription Products: This is a list of complimentary subscriptions allowed and not allowed for use and display by moving them from one list to the other using the arrows.

## **Category Groups**

1. Restrict Category Groups: This is a list of allowed and not allowed category groups for this user group by moving them from one list to the other using the arrows.

{% hint style="info" %}
Note: Categories are displayed in the "interests" box on both an advertiser and on a contact person. You must have categories in the "allowed" column to be able to see them displayed on the contact person record.\
![](<../../../.gitbook/assets/image (405).png>)
{% endhint %}

## **Allowed Removal Reason**

1. Allowed Removal Reasons: List of allowed reasons of removing a client can be defined here.

## **Name Record Security**

1.  Access to Full Name Maintenance: If you set this, user has the option to bypass the CRM specific Add/Edit screens by going to the Full Name Maintenance system. Name Maintenance Security is set in the Name Security Node at left - and will not use the security options set on this screen. If set to yes, the below box "Go to Full Name Maintenance" will be displayed when you are in Edit this Account window. If set to No, you will not see this option

    <figure><img src="../../../.gitbook/assets/image (708).png" alt=""><figcaption></figcaption></figure>
2. **Require Source When Creating New Customer Accounts from CRM:** When checked, this option obligates a user entering a new account to specify the source this account came into Naviga CRM.

## **Company Record Rules**

These are the company records maintenance rules:

1. **Allowed to Add a New Company:** “Yes” when checked to allow the user to add a new company in CRM.
2. **Allowed to Edit Company Address:** When checked to “Yes” it allows users in this group to edit a company address.
3. **Allowed to Add a Company Address:** When checked as “Yes”, then system allows users in this group to add a new address to an existing company.
4. **Allowed to Change Company Name:** When checked as “Yes”, users in this group can change a company name.
5. **Allowed to Change Parent Company:** When checked to “Yes”, users in this group are allowed to change a parent company of an existing company.
6. **Allowed to Change Company’s Website Address:** When checked to “Yes”, users in this group can change the website address of an existing company.
7. **Allowed to Add Credit Control Notes:** When checked as “Yes”, users in this group are allowed to add new credit control notes.

## **Contact Record Rules**

These settings control a contact record. When set to “Yes” this allows users in this group to perform this function.

1. Allowed to Add a New Contact
2. Allowed to Change Contact Address
3. Allowed to Add Contact Address
4. Allowed to Change Contact Name
5. Allowed to Change Contact Employer
6. Allowed to Change Contact Phone
7. Allowed to Change Contact Email
8. Allowed to Change Contact Job Title
9. Allowed to Change Social Media Links
10. Allow to Change Contact Type
11. Allowed to Change Contact Privacy Preference

## **Actions and To-Dos**

1. **Allowed to Change Notes on Closed Actions:** This will allow users in this group to change notes even if the action is closed. If left un-checked, then users in this group cannot change or edit the notes after the action item has been closed.

## **Opportunities**

These settings control the allowed options for opportunities for the users in this group.

1. **Warn user to save if stage of opportunity has not been saved**: If the opportunity is edited, and this box is checked, then user will receive a warning that he did not change the stage of the opportunity but will be allowed to proceed to save the opportunity.
2. **Require Close Date:** If this box is checked, then user will be required to enter a close date on opportunities.
3. **Disable Probability Percentage Overrides:** If checked, this option prevents users from overriding the probability percentage in an opportunity once user chooses the specific stage.
4.  Allow rep and/or rep group selection on opportunity quick update and taskboard: If set to yes, this security group will see the Sales Rep filter on the Opportunity Pipeline, quick update & Taskboard view screens. If set to no, they will not see it.

    <figure><img src="../../../.gitbook/assets/image (1172).png" alt=""><figcaption></figcaption></figure>

## **Other Settings**

1. **Allowed to Access CRM Setup Screens:** If set to “Yes”, then the users in this group can access all setup screens in CRM.
2. **Only Show Opportunities in the Pipeline:** If this option is checked, then the system will display, in the Pipeline Review screen, only opportunities with stages tied to the setting defining them to be in the pipeline. This definition is found under the menu Setup -> CRM Settings -> Opportunity Stages, where each stage can be set to be considered as “In Pipeline” or not.
3. **CRM Call Lists -> Link Prompt Option:** This has 3 options regarding opening a new screen for the CRM Call Lists:\
   \- Always Prompt whether to open Links in Same or New Tab.\
   \- Always Open Links in New Tab\
   \- Always Open Links in Same Tab
4. **Include Only Confirmed Future Orders on CRM Client Overview Screen (Top Right Panel)**: When checked to “Yes”, the CRM Sales tab on the Customer Overview screen shows the Sales with current year and future confirmed orders only and not any other statuses. When left unchecked, the screen displays Confirmed orders only, except for the current year, which includes future non-confirmed orders.
