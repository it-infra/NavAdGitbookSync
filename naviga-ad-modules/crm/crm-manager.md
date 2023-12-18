# CRM Manager

The menu for CRM Manager is controlled by [menu security](../system-settings-admin/security/module-menu-security.md#\_toc79061546) and typically will only be accessible by managers

## Action Items by Rep

This is a screen which allows a Manager to search for To Do activities by rep and by various date ranges.

<figure><img src="../../.gitbook/assets/image (777).png" alt=""><figcaption></figcaption></figure>

In addition to navigating to this report from the CRM Manager menu, it can also be accessed from the sub-menu under the "Rep Activity" navigation tile.

### Sales Activity by Product Group

Next to the Action Details is another report called Sales Activity by Product Group. It displays confirmed orders in the last week, month, 60 days, Qtr and Year. Similar to the report on the Rep Activity Manager Home screen, but this is by product/product group rather than rep. You can expand each product and see the reps underneath.

<figure><img src="../../.gitbook/assets/image (1101).png" alt=""><figcaption></figcaption></figure>

## Transfer / Change Reps

This is used only to transfer reps on the CRM side. It is used for prospecting and not for any orders or rep assignments in the Advertising module. For changing reps in the ad module, please see Brands -> [Change Sales Rep Assignments](../advertising/customers/brands/change-import-sales-rep-assignments.md#\_toc98514799) or [Import Sales Rep Assignments](../advertising/customers/brands/change-import-sales-rep-assignments.md#\_toc41990731)

<figure><img src="../../.gitbook/assets/image (765).png" alt=""><figcaption></figcaption></figure>

On the above screen CRM Reps can be moved to another rep based on a "My List" list of accounts, or by individual account ID's.

Then select the rep this list should be assigned to and answer the following questions with a yes/no

* Should the prospects be removed from the original rep?
* Should the original rep's Actions be reassigned to the new rep?
* Should the original rep's Complementary subs be moved to the new Rep?
* Should the Opps be moved?
* Should any proposals be moved?
* And finally do you wish to keep the list of prospects

## Contacts Flagged as "Do Not Use"

This is a list of contact people that have been flagged as do not use, but who are still attached to the CRM account for a given sales rep and for a given time period.

<figure><img src="../../.gitbook/assets/image (1085).png" alt=""><figcaption></figcaption></figure>

## Proposals Approved Via the Portal

See [Campain Reports](../advertising/campaigns/campaign-reports.md#accepted-proposals) as this report is also available from the Advertising Module

## Call Lists

The concept of call lists is so that Reps can see the list of accounts they are due to call on. From the CRM -> Customers -> Call Lists, a rep can see the calls that they are due to make as part of a Marketing Campaign.

<figure><img src="../../.gitbook/assets/image (625).png" alt=""><figcaption></figcaption></figure>

The rep selects a call list form the call list ID dropdown. They see the Short and Long Description as set by the Manager in Setup. They also see the Marketing Camapign it is related to and the effective dates.

Along the top right, they can log the time spent on the call list. Multiple entries can be added here over time and the manager will be able to see a report of time spent in the [Call List time Spent Report](crm-manager.md#call-list-time-spent-report)

There are then some metrics to see how it's going. Count of Conversions to orders and the total order value sold. As well as the status of the calls made. The statuses are defined in the setup.

In the bottom secton of the page are the names (accounts) that i need to call on. There may be additional reps calling on other names, but these are the ones assigned to them as a rep. The status can be updated, internal notes entered and next action date entered if they need to call back. At the end of the row, is an action button

<figure><img src="../../.gitbook/assets/image (849).png" alt=""><figcaption></figcaption></figure>

The following actions can be taken by the rep:

* Add a CRM Note - This will add a note to the customer account. It can optionally be linked to a contact person, product, and/or Marketing Campaign\
  ![](<../../.gitbook/assets/image (851).png>)
* Send an email - This will open a email screen with the contact person pre-filled. User can select a pre-set template email or free-format a message to the customer. Perhaps as a followup to the phone call.\
  ![](<../../.gitbook/assets/image (1171).png>)
* Create an Opportunity - This will take you to the Opportunity screen pre-filled with the Marketing Campaign and the Call list in the Opportunity details
* Create a Proposal - This will take you to the Campaign Entry screen and will pre-fill the Marketing Campaign in the appropriate field.
* Go to CRM Summary - This will take you to the CRM view of the customer account screen

### Call List Status Setup

The statuses that the rep can select on the call list is configured in Setup -> CRM System Settings and the Call List Status Codes node on the left of the screen. OR they can navigate to Setup -> Call List Setup -> Call List Status Setup

<figure><img src="../../.gitbook/assets/image (1195).png" alt=""><figcaption></figcaption></figure>

Enter a Desired ID and Description at the bottom and click the + to add to the list of codes. If desired, a default email Template can be added to the status so that it is pre-selected when the reps selects the action to Email the client from the call list.

### Call List Setup

This is the screen where the manager creates the call list and assigns it to one or more reps to execute the calls to the clients or prospects.

Navigate to this screen from CRM Manager -> Call List Setup\
or Setup -> Call List Setup -> Call List Setup

<figure><img src="../../.gitbook/assets/image (598).png" alt=""><figcaption></figcaption></figure>

The manager creates the call list with an id and a short description. And if desired, a long description. Link a Marketing Campaign and an Effective Date range.

Then in the top right, names can be imported in a variety of ways. They can be imported from a Spreadsheet, Imported from a CRM List (in My Lists), copied from another Call List or Manually add names.

#### Import Names from a Spreadsheet <a href="#_toc77938631" id="_toc77938631"></a>

Click the button “Import Names from a Spreadsheet”. A pop up screen displays where you can click “Select” button to import an already filled in spreadsheet with accounts. All that is needed in the spreadsheet is a column with the heading “Name ID” and IDs filled in below the column heading.

![](<../../.gitbook/assets/5 (31).png>)

If you have already existing names on your list which are already in the spreadsheet, the system will ignore them and import only Name IDs which are not already on your list.

Click “Select” to browse and upload the spreadsheet.

Note that if you click the button “Delete Current Lines” to be a “Yes”, then the existing lines on your list will be deleted when the import is completed and only the imported names will appear on your list. Leave the button as “No” value in order to leave the names already existing on the list and import the names on the spreadsheet into the list.

Click the button “Import Names” and the system will display a success message with the number of imports.

![](<../../.gitbook/assets/6 (64).png>)

Click on the “OK” button and you will see the names of the list.

![](<../../.gitbook/assets/7 (52).png>)

The names appear and now you can choose the status, next action date and assigned rep from the drop down menus. Once finished, click on the button “Save” to save the new names and choices on the list.

#### Import Names from CRM List <a href="#_toc77938632" id="_toc77938632"></a>

This option allows you to import names from the existing CRM list.

![](<../../.gitbook/assets/8 (16).png>)

Choose the list from the drop down menu and click “Apply”. Note the list has to be a CRM type list; otherwise the import will not be successful.

Note that again you can click “Yes” for “Delete Current Lines” if you want to erase lines already on the list and import only names in the CRM list.

You will receive a success message of import.

![](<../../.gitbook/assets/9 (20).png>)

Note that the system again will only import names which are not already on your list.

Click OK and edit the status, date and reps for each line. Click the “Save” button to save the changes in the list.

#### Copy from another Call List <a href="#_toc77938633" id="_toc77938633"></a>

This allows you to copy names from an already existing call list. Click the button “Copy from Another Call List”.

![](<../../.gitbook/assets/10 (14).png>)

Choose the list name from the “Copy from” drop down. You have the option to copy the list with the same rep assignments if you click “Yes” for “Copy Rep Assignments”. If left as “No”, then the rep assignments will not be copied over and after the import, you can select each rep for each account.

Click the “Yes” to delete current lines if you want to limit the names on the new list to the copied list removing existing names from this list.

Click the “Apply” button to perform the operation.

When all the names have been copied and you receive the success message, click the “Save” button to save the names on the list.

To cancel the operation before clicking on the save button, click the reset w/o save button or cancel button.

#### Manually Add Names <a href="#_toc77938630" id="_toc77938630"></a>

Click the button “Manually Add Names”.

![](<../../.gitbook/assets/3 (6).png>)

Enter an existing account ID and press tab. The account name is automatically filled in. Or you can enter any ID you like and the system will add it in when click “Add Name”.

![](<../../.gitbook/assets/4 (31).png>)

You can then click the down arrow on the status and next action date and assigned rep to choose the respective values.

The add name pop up screen remains on the screen and allows you to keep on adding names. When finished click the “Close” button.

Then click on the “Save” button to save the list.

#### Assign Sales Rep <a href="#_toc77938634" id="_toc77938634"></a>

Click the button “Assign Sales Rep” to perform any bulk change to sales rep on the list. You can choose the sales rep to change from and the one to change to. You can also leave the “from” field blank in order to include all blank sales rep fields to change to the new value.

![](<../../.gitbook/assets/11 (5).png>)

Click “Apply” to perform the sales rep change operation.

![](<../../.gitbook/assets/12 (20).png>)

The other accounts with different sales reps other than blank will remain the same.

#### Bulk Status Change <a href="#_toc77938635" id="_toc77938635"></a>

This button allows you to change any status including blank to anther status.

![](<../../.gitbook/assets/13 (16).png>)

Click Apply and then save the list when finished.

#### Bulk Next Action Date Change <a href="#_toc77938636" id="_toc77938636"></a>

Similarly you can change the next action date to any date you want by clicking the button “Bulk Next Action Date Change”.

![](<../../.gitbook/assets/14 (19).png>)

Enter the “to” and “from” dates to change them to the date in the “from” field. Click Apply and save.

### Call List Time Spent Report

The CRM manager can review the time report spent by each rep on their lists by navigating to the menu CRM Manager -> Call List Time Report.

Enter the date range during which you want to view the lists, and click the button “Get Data”.

![](<../../.gitbook/assets/20 (3).png>)

You can filter the data under the columns Date and Time using the cone filter icon and entering the filter criteria. For example, 11/1/2016 and click the cone filter and choose equal to in order to see the activity on a list on a certain date.

You can also enter partial data in each of the other column blank headings box to see the results matching this search. For example a partial rep name and the system will display only these items matching the name of the rep.

### Call List Performance Report

This report shows a summary of the opportunities per sales rep as well as time spent.

At the top, select a call list from the dropdown menu. Optionally, can also select a rep.

<figure><img src="../../.gitbook/assets/image (1052).png" alt=""><figcaption></figcaption></figure>

The order details in this report refer to the book module in Naviga ad and will be removed in a future version.

## Marketing Campaign 12 Period Analysis

See [Marketing Campaign 12 Period Analysis](../advertising/analysis/marketing-campaign-12-period-analysis.md) in Advertising Module

## Informer Dashboards

See [Informer Dashboards](../advertising/analysis/informer-dashboards.md) in Advetising Module
