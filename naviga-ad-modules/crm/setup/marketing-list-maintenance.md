# Marketing List Maintenance

This page describes the CRM marketing lists functionality, including prerequisite setup. Marketing lists allow you to add contacts which exist in Naviga to different mailing lists which can be used for marketing purposes. Naviga allows for adding names to the lists over time or adding names in bulk to one list at a time.

## Create Marketing List <a href="#_toc56441438" id="_toc56441438"></a>

Create a marketing list by navigating to the menu Setup -> Marketing List Maintenance. Click the button “Add a New List”.

![](<../../../.gitbook/assets/1 (30).png>)

Enter a description for the list, and click the “Save” button.

If MailChimp is setup, and if you decide to connect your list to MailChimp, then enter the MailChimp ID to the settings. Click the “Auto Subscribe” and “Auto unsubscribe” to implement the subscription and removal from subscription to MailChimp.

![](<../../../.gitbook/assets/2 (19).png>)

You can also link MailChimp lists together, by clicking the button “Link MailChimp List”. The system will offer you to select the lists you would like to link to.

![](<../../../.gitbook/assets/3 (45).png>)

Click Select and then click the save button, and you will receive an option to import the names to your list or to just save. If you choose to import the names to your list, a status message of importing the names, including the requalified names, added, removed or skipped.

![](<../../../.gitbook/assets/4 (62).png>)

If you do not and click “No, just save”, you will only have your names on the list.

You can check the status of the MailChimp list if you click the icon under “Linked” column which indicates a connection to MailChimp. You will need the MailChimp login and password.

![](<../../../.gitbook/assets/5 (44).png>)

## Attach Names to List <a href="#_toc56441439" id="_toc56441439"></a>

You can add names to the list either individually one at a time or in bulk.

### Individual Names <a href="#_toc56441440" id="_toc56441440"></a>

To add a name at a time, you can do so in many ways using the following:

* Name Maintenance screen
* CRM Contact Details Screen
* Mail-Chimp Interface

For example, to do so using the CRM contact screen, navigate to the Customers menu -> click on any of the customers on the list or perform a customer search, and the system will display the customer overview.

Scroll to the Contacts pane and click the hyperlink to the contact for this customer.

Scroll to the pane “Marketing Lists”.

![](<../../../.gitbook/assets/6 (8).png>)

Click the drop down arrow under “Add a List” and you will view the lists to choose from. Then click the next drop down arrow for the email information for this list and click + sign to add the name to the list.

You will receive a message confirming that the addition of this name to the marketing list has been saved.

An alternative method is to use the name maintenance screen. From the same customers overview screen, click the hyperlink to the name and then click the link “Edit This Contact”. Then click “Go to Full Maintenance”. Click the node “Marketing List”.

![](<../../../.gitbook/assets/7 (35).png>)

Scroll to “Add a List” section and add one using the drop down arrows and click the + sign then click “Save” to store the settings.

### Add Names to List in Bulk <a href="#_toc56441441" id="_toc56441441"></a>

These menus can be used to add more than one name at a time to the marketing lists:

* “Import to Marketing Lists” process
* CRM “My Lists” process.

To use the import process, navigate to the Setup menu -> Marketing Lists menu and then click the node “Import to Marketing Lists”.

![](<../../../.gitbook/assets/8 (24).png>)

Click the button “Download Template”. This will download an Excel sheet which you can fill out with data regarding the names you would like to add to the list. These names must be existing in Naviga.

![](<../../../.gitbook/assets/9 (32).png>)

Fill in the name ID of the contact, the actual name of the contact and their email address. These columns are required and must match existing data in Naviga.

You can fill in as many names as you want and then save the sheet to your desktop.

In the Naviga import screen, click the drop down menu to choose the marketing list you want to add these names to, and then click the “select” button. Browse for the spreadsheet you saved and choose it.

Click “Check Import” button to flush out all errors prior to the import.

In case there is an error, click OK to the message you receive and the system will display the line on which you have the error and the error itself.

In this case, click the “Remove” button to remove the spreadsheet from Naviga selection. Return to the spreadsheet and correct the errors and resave the file. Repeat the select and check import process until you get a success message.

Click the “Import” button and this will add the names to the list you chose.

## View which Lists have been assigned to an Individual <a href="#_toc56441442" id="_toc56441442"></a>

There are several ways to view the lists which have been assigned to a specific individual using:

* Name Maintenance screen
* CRM Contact Screen

## Mailings

### Create Mailings <a href="#_toc56441443" id="_toc56441443"></a>

Now you can create mailings for marketing purposes using the lists you created. You can create mailings as a list at a certain moment in time. Creating a mailing creates an associated CSV file which you can use to bring these contacts into another system, or to print labels, and so forth.

To create the mailings, navigate to the menu Setup -> Marketing Lists. Click the node “Mailings”.

![](<../../../.gitbook/assets/11 (24).png>)

Click the drop down menu from the Marketing List. Then click the button “Create New Mailing”.

A pop up screen displays with the method to use to create the mailings.

![](<../../../.gitbook/assets/12 (22).png>)

Write the mailing description. Click the drop down of the type. Note the list is “Email” and “Snail Mail” for example. Choose the method desired. If you click “Yes” to the “Include Duplicate Emails”, the mailing list will include duplicate emails. If left as “No”, duplicates will be eliminated from the mailings.

Click “Preview List” to get a glimpse at the mailing list. A CSV file will display with the data.

![](<../../../.gitbook/assets/13 (8).png>)

Click “Create” and the list will display in the Naviga mailings screen.

![](<../../../.gitbook/assets/14 (15).png>)

You can then click the CSV link, or export to Excel to Word using the icons available. This list can be used to print labels and used further.

### Mailing Results <a href="#_toc56441444" id="_toc56441444"></a>

You can upload the results of the mailings to include data on the contacts in the list on whether they subscribed, unsubscribed, opened or clicked the mailing. There is a utility to import list results using a template spreadsheet from any other system.

To do so, navigate to the menu Setup – Marketing Lists and click the node “Import Mailing Results”.

![](<../../../.gitbook/assets/15 (15).png>)

Choose the marketing list for which you want to upload the results. Click the Mailing which you have created and for which you want to upload the results.

Click the button “Download Template”, which will display a spreadsheet to be filled with data of the results.

![](<../../../.gitbook/assets/16 (12).png>)

Fill in the ID of the contact as well as their name and email address. Fill in whether the email was bounced as invalid email, or if customer has unsubscribed from the mailing list, the number of times the email was opened and the number of times it was clicked by the customer.

When finished, save the template to your desktop.

On the Naviga import page, click the “Select” button and browse and select the spreadsheet you saved.

Click the button “Check Import”, in order to flush out all import errors before uploading. If there are errors, click “Remove” button to remove the saved template from Naviga import page. Navigate to correct the errors in the imported spreadsheet, and save it again to the same location.

Navigate to the import page and repeat the select and check import process till all errors are gone. Then click “Import”.

![](<../../../.gitbook/assets/17 (8).png>)

Click OK to the success message. This will import the results to Naviga.

Once the upload is complete, you will view the results under the node “Mailings”.

![](<../../../.gitbook/assets/18 (15).png>)

Also, in the contact edit screen, you should be able to view the results as well under the pane “Mailings”.

![](<../../../.gitbook/assets/19 (5).png>)

## MailChimp Integration <a href="#_toc56441445" id="_toc56441445"></a>

A Mailing may be linked to a MailChimp campaign. When this is done, linked mailings can be synced by clicking the Sync button on the Mailing. This process will automatically query MailChimp for Opens, Clicks, Bounces and Unsubscribes and save this information in Naviga.

### MailChimp Setup <a href="#_toc56441446" id="_toc56441446"></a>

Navigate to the menu Setup -> Marketing Lists, and click the node “Settings” under MailChimp Integration. You will need to contact the administrator to get the appropriate data to fill in the setup.

![](<../../../.gitbook/assets/20 (9).png>)

### Working from Naviga <a href="#_toc56441447" id="_toc56441447"></a>

When you create or update a marketing list, you can link to and pull contacts from a MailChimp list.

If you set the Naviga marketing list to auto Un/Subscribe, when you add a name to a List or remove them, they are automatically (un)subscribed in MailChimp.

The same is true when you tag multiple names to a list through CRM My Lists. When you create or update a mailing, you can link to a MailChimp campaign. Also, you can pull statistics from MailChimp on linked Mailing Lists.

### Working from MailChimp <a href="#_toc56441448" id="_toc56441448"></a>

Using WebHooks:

* When subscribers are added or removed, this information gets sent to Naviga automatically.
* When a campaign is sent from MailChimp, it updates the mailing date in Naviga.
* When a subscriber changes their name.
* When a subscriber changes their email address.

### Missing Names from Imports <a href="#_toc56441449" id="_toc56441449"></a>

That node is used to show a list of names that have subscribed to user’s MailChimp list from outside Naviga system, and for which there have not been a match found to tie them to in Naviga. For instance, if a customer is subscribed to your list and forwards it to a friend who subscribes, then the latter’s email is not found in our system, and therefore it would show up here.
