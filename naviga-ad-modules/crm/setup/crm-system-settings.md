# CRM System Settings

These settings are for various dropdowns and other fields throughout CRM where the values and defaults are setup here and then used across other menus. They can be edited at any time.

Navigate to the CRM screen Setup -> CRM System settings.

## CRM Global Parameters <a href="#_toc120632507" id="_toc120632507"></a>

<figure><img src="../../../.gitbook/assets/image (1432).png" alt=""><figcaption></figcaption></figure>

### General Settings <a href="#_toc120632508" id="_toc120632508"></a>

1. Allow Companies to be Created without an Address: When checked as Yes, system allows you to create an advertiser without an address. If left as No, you are allowed to create an advertiser without an address.
2. Notification Method for Expiring Complimentary Subscriptions: Send an Email or Use CRM Alerts. These options are to notify the internal user with complimentary subscriptions which are expiring.
3. Default [Source Code](crm-system-settings.md#\_toc120632512): These are the options where you can choose the default code for how the newly created advertiser has been reached and acquired.
4. Automatically set Opportunity to WON status when a linked Proposal is Confirmed: When enabled, this feature will automatically set the Opportunity Stage to the first Stage with a Type of "Won" when a linked Proposal is confirmed.\
   (This means when the linked campaign status is set to "CO" - not when the client accepts the proposal in the portal, which would only set it to one of the "Reserved" statuses)

### Marketing Campaign Settings <a href="#_toc120632509" id="_toc120632509"></a>

[Also see Marketing Campaign Setup](marketing-campaign-setup.md)

1. Marketing Campaign Override Description: Entering a term here will override the display of the label of "Marketing Campaigns" throughout the menus in the system. For example, if your organization calls them "Projects", enter Project in this field. If left blank, the default Marketing Campaign description will be used.
2. Display on Production Jobs: If checked as Yes, then the marketing campaign name is displayed on production jobs.
3. Display on Non-chargeable Timesheet Entries: If checked then marketing campaigns display on the non-chargeable timesheet entry.

### Custom Links <a href="#_toc120632510" id="_toc120632510"></a>

1. These appear on the Company Screen: Custom links are built using tokens to insert values into a URL. This allows you to hand database values from Naviga to another system or website. As an example, https://www.google.com/search?q=\[CLIENT NAME] inserts the prospect’s (or Customer) name in a google search.
2. View Legend of Tokens: This link when clicked displays a list of existing ones. As an example, the above screenshots shows sample links from one of our internal systems. At the end of the URL String for Hoovers (off-screen), google and YouTube is the \[CLIENT NAME] parameter. At the end of Twitter and Facebook are User Defined Fields defined below...\
   ![](<../../../.gitbook/assets/image (998).png>)\
   You can build as many custom links as is desired.

## Name Related Tables <a href="#_toc120632511" id="_toc120632511"></a>

### Name Source <a href="#_toc120632512" id="_toc120632512"></a>

Codes can be added to Companies and Contacts to indicate how this record came in to the system, such as Web Search, Call in, Referral, Trade Show, and so forth. These Sources can also be used to filter Companies and Contacts in 'My Lists'.

<figure><img src="../../../.gitbook/assets/image (501).png" alt=""><figcaption></figcaption></figure>

1. Name Source ID : Click New to create a new ID for a source.
2. Description: Enter the description of the source.
3. Is Inactive: When checked as “Yes” this source is inactive.

When finished, click Save to save the list.

### Job Titles <a href="#_toc120632513" id="_toc120632513"></a>

Job Titles are added to contacts to help target marketing materials based on the role people play in an organization. This can be used as an exact title but is more often used to define a role/category for use in list generation / data selection such as Owner, Executive, Sales, Marketing, and so forth.

![](<../../../.gitbook/assets/image (916).png>)

1. Job Title ID: Click New and enter the ID.
2. Job Title Description: Enter the description.

When done, click Save.

### Job Titles Import <a href="#_toc120632514" id="_toc120632514"></a>

This screen provides a template by which you can import a list of job titles in bulk. The fields in the template are simply the ID and Description, like the Job Titles manual entry screen above.

<figure><img src="../../../.gitbook/assets/image (563).png" alt=""><figcaption></figcaption></figure>

### Name Titles <a href="#_toc120632515" id="_toc120632515"></a>

Name Titles are added to contacts to help pre-define a title such as list of standard military officer ranks.

1. Name Title ID: Click New to create the title ID.
2. Description: Enter a description for the name title.
3. Gender: Select the gender from the list.

Save the settings.

<figure><img src="../../../.gitbook/assets/image (1618).png" alt=""><figcaption></figcaption></figure>

### Name Removal Reasons <a href="#_toc120632516" id="_toc120632516"></a>

Name Removal Reasons are used to track why a contact was removed from a Salesrep’s list.

<figure><img src="../../../.gitbook/assets/image (633).png" alt=""><figcaption></figcaption></figure>

1. Name Removal Reason ID: Click New and add the ID.
2. Description: Enter a description of the name removal ID.
3. Sort Order: Id Desired, enter a sort for this reason to list it in a specific order in the list in menus throughout the system.
4. Remove Name for All Reps: When checked as “Yes” then when the name is removed, it will be gone from all Salesreps’ lists. If “No” then the name is removed only for the Salesrep performing the removal. (For example if the person has left the company, it is likely it should be removed as a contact person for all users. If they are simply not someone I talk to anymore at the company, It might be appropriate to only remove them as "my" contact person.
5. Suspend Comp. Subs.: When checked as “Yes” then the removed name will be removed from complimentary subscriptions lists and they will no longer be sent to this contact.
6. Set Name as "Do Not Use": This reason can be checked to be a Do Not Use rather than removed and deleted from the system.
7. "Do Not Use" Reason: This field displays only when the field above is set to “Yes” to choose from it the reason to mark the name as Do Not Use.

Save the settings when finished with the entries.

### Contact Types <a href="#_toc120632517" id="_toc120632517"></a>

Contact Types are added to contacts to help target-market based on contact role. This is only used in CRM for example, Decision Maker, Assistant and so forth.

1. Contact Type ID : Click New to add a new ID.
2. Description: Enter the description of the contact type.
3. Transfer to Campaigns: If set to yes, when this contact type is used on an Opportunity Contact, the contact person will be added as a campaign production contact if a proposal is created from the Opportunity.

Click the Save to save the settings.

<figure><img src="../../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

### Privacy Defaults <a href="#_toc120632518" id="_toc120632518"></a>

Privacy Defaults are used throughout the application to define customer privacy requests. These defaults are used when creating a new Contact and may be overridden at that time or any time thereafter.

1. Are you allowed to contact this person via Email: If checked as “Yes” then the person is allowed to be contacted by email.
2. Are you allowed to contact this person via Telephone: If checked as “Yes” then the person is allowed to be contacted by phone.
3. Are you allowed to contact this person via Fax: If checked as “Yes” then the person is allowed to be contacted by fax.
4. Are you allowed to include this person in List Rentals: If checked as “Yes” then the person is included in the List Rentals.
5. Are you allowed to contact this person via Mail/Post: If checked as “Yes” then the person is allowed to be contacted by mail.

Save the settings.

### Social Media Links <a href="#_toc120632519" id="_toc120632519"></a>

Social Media Links are used to define social media links on a Contact.

<figure><img src="../../../.gitbook/assets/image (572).png" alt=""><figcaption></figcaption></figure>

1. Social Media Site ID: Click New to create a new social media ID.
2. Description: Enter the description.

Save the settings.

### Employee Tiers

These are for accounts to indicate employee count of the account. This is to allow for categorizing clients within tiers for reporting purposes in Informer.

Click on the node Employee Tier and add an ID, description and lowest and highest value of the range of # of employees of this account. Click + to add the new tier and repeat as needed then click save.

<figure><img src="../../../.gitbook/assets/image (1116).png" alt=""><figcaption></figcaption></figure>

### Revenue Tiers

These are for accounts to indicate Annual Revenue of the account. This is to allow for categorizing clients within tiers for reporting purposes in Informer.

Click on the node Revenue Tier and add an ID, description and lowest and highest value of the revenue of this account. Click + to add the new tier and repeat as needed then click save.

<figure><img src="../../../.gitbook/assets/image (1477).png" alt=""><figcaption></figcaption></figure>

### Departments <a href="#_toc120632522" id="_toc120632522"></a>

This screen allows you to enter various IDs and descriptions of departments.

### Opportunity Tags <a href="#_toc120632523" id="_toc120632523"></a>

This screen allows you to create tags for values to attach opportunities to it where you can use these tags to search for the various opportunities.

### Primary/Secondary Industries

Primary and Secondary Industries are code tables used to set additional data on the client record about the industry they are in. This is then displayed on the "Other" tab on the customer details screen. This was done for a client who needed some additional details beyond the PIB Code/Industry code that is required on the account and order creation. If you do not need the additional fields they can be left blank.

<figure><img src="../../../.gitbook/assets/image (138).png" alt=""><figcaption></figcaption></figure>

## Other Tables <a href="#_toc120632524" id="_toc120632524"></a>

This is a list of various tables which you can use to create set values to be used throughout the system. On several of the screens there’s a capability to import large number of values for the node instead of manually entering each value on the screen. A template is provided for this purpose. Once you click the Import button, download the template, fill it out and import it.

### Required Fields on New Records

CRM Settings include a list of fields which in creating new accounts, new contacts, new notes and new to-do items from CRM module can be made mandatory for user to enter or marked with \*\*\* as important due to requirements in third party applications integrating with CRM, but not necessarily required to save.

Click the Node “Required Fields on New Records”.

<figure><img src="../../../.gitbook/assets/image (588).png" alt=""><figcaption></figcaption></figure>

In the first section, set the New Contact Fields on the list as:

* Blank, leaving them as optional, or
* Required, making the field required where the record will not be saved when creating the contact if this field isn’t entered, or
* Not Required, but Display \*\*\* next to Label, where the field is not mandatory, but the field has a label \*\*\* by it. This alerts the user to enter them because the fields are important for third party integrations, but not so important that the record shouldn't be saved without it.

Repeat this in the next section for New Account where it applies to new advertisers created in CRM.

Repeat for the third section “Action/ To-Do” fields. Also, for the “Notes” fields.

Any fields that are marked as required and the dropdown cannot be changed, are required by the system and cannot be made optional.

### Lead Status Code

The screen allows you to create the codes which provide tracking of each lead’s status to indicate their stage in the sales life cycle.

Navigate to the menu Leads -> Lead Status Codes Setup. This is the same menu as in Setup -> CRM System Settings -> Other Tables -> Lead Status Codes.

<figure><img src="../../../.gitbook/assets/image (1393).png" alt=""><figcaption></figcaption></figure>

Enter an ID, Description for the status to indicate the state of the lead. For example, New, In Progress, Cancelled and so forth.

Choose the Stage Type, to match the description of the status. The Stage Types are hard coded values in the system of “Open” which means the lead is being introduced into the system, “Qualified” meaning the appropriate departments of sales and/or marketing deemed the lead valid and viable, and “Disqualified” meaning the marketing department deemed the lead invalid to proceed.

Check applicable flags for In Pipeline, meaning display it in the Pipeline for follow-up purposes or not, and same for the flag Create Opportunity meaning to allow for creating an opportunity based on this status. Repeat adding various status as applicable and then click the + to add. When finished, click the Save to store the codes.

### Marketing Efforts

Marketing Effort is another field on a lead that can be selected and/or impored in with the lead. This is a more tactical description of where the lead came from. A lead might be related to a marketing campaign, but that Marketing Campaign could include any or all of these efforts, so it gives an additional layer of information beyond linking a Marketing Campaign.

<figure><img src="../../../.gitbook/assets/image (1539).png" alt=""><figcaption></figcaption></figure>

### Business Category Groups <a href="#_toc120632525" id="_toc120632525"></a>

These category groups are used to help manage long lists of Business Categories. A single category may be included in one or more Category Groups. For convenience, Category Groups may be assigned to CRM Security Groups, to only offer relevant groups to various rep groups.

<figure><img src="../../../.gitbook/assets/image (438).png" alt=""><figcaption></figcaption></figure>

1. Group ID: Click New to create a new group ID.
2. Description: Enter the group description.
3. Assigned Categories: This provides the business categories list attached to this group. This comes from the next node “Business Categories”.

Click the Import button at the bottom of the screen to import these rather than enter them manually.

### Business Categories <a href="#_toc120632526" id="_toc120632526"></a>

Business Categories are added to companies and contacts to help target-market based on lines of business such as Manufacturer, Healthcare and so forth.

<figure><img src="../../../.gitbook/assets/image (422).png" alt=""><figcaption></figcaption></figure>

1. Category ID: Click New and create an ID for the business category.
2. Description: Enter the description for the category.
3. Assigned Groups: Choose the group from the drop-down menu to attach to it this category and save the settings.

Click the Import button at the bottom of the screen to import these rather than enter them manually.

### Action Priorities <a href="#_toc120632527" id="_toc120632527"></a>

Action Priorities allow reps to prioritize to-do-list items both in the system and in Google/Outlook calendars.

<figure><img src="../../../.gitbook/assets/image (279).png" alt=""><figcaption></figcaption></figure>

1. Priority ID: Click New to create a new priority ID. For example, H for High, L for low, and so forth.
2. Description: Enter the description for the action priority.
3. Sort Order: Enter an alphanumeric value to order this item in a list where it shows as a drop-down.
4. External Calendar Priority: Choose from the drop-down menu to attach this priority to the external calendar priority.

Click the Import button at the bottom of the screen to import these rather than enter them manually.

### Action Types <a href="#_toc120632528" id="_toc120632528"></a>

Action Types are used to categorize to-do-list items, such as Setup Call, Appointment, and so forth.\\

<figure><img src="../../../.gitbook/assets/image (429).png" alt=""><figcaption></figcaption></figure>

1. Action ID: Click New to create a new action ID.
2. Description: Enter a matching description to the action ID.
3. Sort Order: Enter a value to determine the sort order of this item on lists in the system.
4. Short Description: Enter a short description if you need more details to be displayed for users when using this option.
5. Sync w/ External Calendar: If yes then this action type will sync with the user’s external calendar. (requires [Nylas Integration.](../../system-settings-admin/integration/nylas-email-calendar-integration.md))
6. Auto Close: If “Yes”, then when created the action type is automatically closed.

Click the Import button at the bottom of the screen to import these rather than enter them manually.

### Comp. Types <a href="#_toc120632530" id="_toc120632530"></a>

Complimentary Subscriptions Codes are values to choose when adding a complimentary subscription to a contact. See [My Comp Subscriptions ](../customers/#my-comp-subscriptions-comp-subscriptions-serve-an-issue)for additional details

1. ID: Enter the ID for the complimentary code.
2. Description: Enter the code description.
3. Max Issues: Enter the maximum number of issues to be sent to the contact.
4. Max Copies: Enter the number of maximum copies to be sent to the contact of the same issue.
5. Inactive: If checked then this code is not going to be visible to users to choose.

### Call Lists Status Codes <a href="#_toc120632531" id="_toc120632531"></a>

This table provides values you enter for the status codes of call lists whether the clients on this list are New Lead or a Cold Call.

1. Status ID: Enter a Status ID of the call list.
2. Description: This is a description of the status.
3. Default Email Template: Choose from the drop-down list a template which you can use in contacting clients on this call list.

### User Defined Fields <a href="#_toc120632532" id="_toc120632532"></a>

User Defined Fields allow you to add custom fields on Account Screens when these fields aren’t readily available as part of Naviga screens, for example, budget range, annual marketing budget, and so forth. These can be text, numeric, dropdowns, or multi-select lists. See [Opportunity User Defined fields](../opportunities.md#\_toc122615685) setup for more details around how to set up each type of UDF.
