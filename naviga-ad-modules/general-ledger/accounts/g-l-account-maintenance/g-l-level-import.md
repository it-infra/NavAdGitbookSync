# G/L Level Import

User has the ability to import G/L Level using an import spreadsheet provided in the software. Navigate to the menu Accounts -> G/L Account Maintenance -> G/L Level Import.

<figure><img src="../../../../.gitbook/assets/image (1236).png" alt=""><figcaption></figcaption></figure>

## Template <a href="#_toc10012383" id="_toc10012383"></a>

Click on the button “Download Template”. The excel sheet will open and you can fill out the fields as follows:

<table data-header-hidden><thead><tr><th width="139"></th><th width="109"></th><th width="382"></th><th></th></tr></thead><tbody><tr><td><strong>Field Name</strong></td><td><strong>Example</strong></td><td><strong>Description</strong></td><td><strong>Mandatory (Yes/ No)</strong></td></tr><tr><td><strong>Level Number</strong></td><td>2</td><td>You can only import Level Number between 2 and before the last level which exists. So if there are 3 levels you can only import level 2, and if there are 5 levels you can only import level 2, 3, 4, and so forth.</td><td>Yes</td></tr><tr><td><strong>Level Code</strong></td><td>022</td><td>The Level Code must follow the format and length as defined. So if defined in the system as 3N then it must be 3 characters and all should be numeric.</td><td>Yes</td></tr><tr><td><strong>Description</strong></td><td>Prepaid Expense Account</td><td>Alphanumeric description of the code level</td><td>Yes</td></tr><tr><td><strong>Inactive</strong></td><td>N</td><td>Y for yes and will set the field to be inactive and not visible to users. N for No will enable the level for users to see and use.</td><td>Yes</td></tr></tbody></table>

Save the spreadsheet to your desktop. Then click on “Select” on the import page and browse for the file you just saved. Select the file to be uploaded. Click on “Test Import File”. This is necessary to correct any errors in the imported spreadsheet prior to importing.

If you have errors, the system will alert you to them. Click on OK to view the error details.

![](<../../../../.gitbook/assets/2 (78).png>)

The system will display the reason for the errors. Click on “Close”, and then click on “Remove” to remove the file from being imported. Reopen the template you saved to your desktop and correct the errors and save it again to the same location. Select the file to upload and repeat the test import process until you receive a success message indicating that your import is accurate.

![](<../../../../.gitbook/assets/3 (28).png>)

Note that if you want to overwrite existing levels, click the corresponding button to change it from “No” to “Yes”.

Click on the button “Import”. The import will be successful. If you click the node on this screen for the level you imported, you should be able to view the newly imported level with its description.

![](<../../../../.gitbook/assets/4 (37).png>)

If you’d like to create accounts based on this ID, then you can click on the last node for "Accounts” and click on “New”. (this might be level 3, 4 or 5 depending on how many segments you are using in your full G/L Code) Enter the level 1 from the drop down menu which is usually the company code. Then choose level 2 which you imported from the drop down list. Then enter the third level of account ID and enter the account description.

![](<../../../../.gitbook/assets/5 (11).png>)

Click on OK. The account is now started.

![](<../../../../.gitbook/assets/6 (59).png>)

Enter the remaining fields as needed and click on “Save”. The account will be ready for use in the system.

You can also import the G/L Accounts once the levels are created. See [G/L Account Import](g-l-account-import.md).
