# Journal Entries

### Import Journal Entries <a href="#_toc79080424" id="_toc79080424"></a>

As a pre-requisite, some of the values in the template (such as the G/L code against which to import the entry) must have already been set up in the system. Fields that must match an existing entry in the system are highlighted in yellow. G/L Code and Financial Period are both require and must be configured in advance.

Navigate to the General Ledger module and click on the menu Journal Entries -> Journal Entries -> Import Journal Entries.

![](<../../../.gitbook/assets/1 (32).png>)

Click on “Download Template” button which will open an excel sheet containing the necessary columns for you to fill.

Fill out the columns with the data. The guidelines on the template fields are listed below in the section titled “Template Fields”. Note that the bold columns are required and are mandatory to fill out. You can enter multiple lines for more than one journal entry import.

![](<../../../.gitbook/assets/2 (5).png>)

Once finished, save the excel sheet to your desktop. You can include many journals on separate lines.

In the Naviga import screen, click the “Select” button and browse for the file you saved. Choose the file to be imported and it displays in the import screen as a filename.

Enter the status of the journal from the drop-down menu to be approved or pending, which will be the status of the imported journals.

The Reassign Journal IDs box can be checked to be “Yes” for the system to assign a system generated ID for the journals you enter. Leave as “No” if you want the system to use the journal IDs you have in the excel sheet template.

Click on the button “Test Import File”. This allows the system to verify the data before the import takes place to remove any errors in the file.

If there are errors, click on the OK button and the system will specify the template lines containing the errors and provide a reason for the error.

![](<../../../.gitbook/assets/3 (46).png>)

Close the screen. Click on the “x Remove” button by the template file name. Re-open the template on your desktop and perform the changes necessary. Re-save the file.

Repeat the upload process to the import screen till you receive no error messages. When finished, click on the “Import File”. You will receive a confirmation message of the import success.

![](<../../../.gitbook/assets/4 (26).png>)

Note the Import ID so you can search for the journals you imported into the system.

Click OK.

To view the imported journals, click the node on the page “List of Imported Journals” and choose the import ID from the drop-down menu.

![](<../../../.gitbook/assets/5 (41).png>)

### Template Fields <a href="#_toc79080425" id="_toc79080425"></a>

<table data-header-hidden><thead><tr><th width="157"></th><th width="146"></th><th width="334"></th><th></th></tr></thead><tbody><tr><td><strong>Column Name</strong></td><td><strong>Example</strong></td><td><strong>Data Source</strong></td><td><strong>Mandatory (Yes/No)</strong></td></tr><tr><td><strong>Journal ID</strong></td><td>SH3422</td><td>Any alphanumeric values for the journal IDs.</td><td>Yes</td></tr><tr><td><strong>Description</strong></td><td>Publication JE234</td><td>Alphanumeric values for the description of the journal</td><td>Yes</td></tr><tr><td><strong>Type</strong></td><td>GI</td><td>GJ is the standard General Journal Entry. Or GA is an Accrual Journal Entry.</td><td>Yes</td></tr><tr><td><strong>Period</strong></td><td>2018-09</td><td>This is the financial period against which the journal entry is imported. It must match the value in Naviga.</td><td>Yes</td></tr><tr><td>Reversal Period</td><td>2018-07</td><td>This is the reversal period of journal entries if applicable.</td><td>No</td></tr><tr><td><strong>G/L Account</strong></td><td>01*0001*0102</td><td>This is the GL account number against which this journal entries are imported. The value must match the Naviga GL account.</td><td>Yes</td></tr><tr><td><strong>Debits</strong></td><td>100</td><td>Numeric value of the debits attached to the journal entry.</td><td>Yes</td></tr><tr><td><strong>Credits</strong></td><td>100</td><td>Numeric value of the credits attached to the journal entry.</td><td>Yes</td></tr><tr><td>Publication ID</td><td>RT</td><td>Alphanumeric ID of the publication attached to this journal. This value is the same as Naviga.</td><td>No</td></tr><tr><td>Issue ID</td><td>AUG2018</td><td>Alphanumeric ID of the publication’s issue. This value must match the Naviga value of the issue.</td><td>No</td></tr><tr><td>Edition ID</td><td>HOL2018</td><td>Alphanumeric ID of the edition and must match the edition ID value in Naviga.</td><td>No</td></tr><tr><td>Section ID</td><td>FR</td><td>Alphanumeric ID of the edition and must match the section ID value in Naviga.</td><td>No</td></tr><tr><td>Employee ID</td><td>32444</td><td>This is the employee ID attached to this journal and must match a value in Naviga.</td><td>No</td></tr><tr><td>Comment</td><td>Imported 12/2017</td><td>Alphanumeric text which can be anything and displays for the journal after import is complete.</td><td>No</td></tr><tr><td>Project ID</td><td>344</td><td>This is the ID of the project to which this journal entry is attached and must match the value in Naviga.</td><td>No</td></tr><tr><td>Job ID</td><td>12</td><td>Alphanumeric value of the Job ID which will be attached to the import of journal entries.</td><td>No</td></tr><tr><td>Product ID</td><td>NAM</td><td>Alphanumeric value of the product ID and should match the value in Naviga.</td><td>No</td></tr><tr><td>Impression No</td><td>100</td><td>Numeric value of the number of impressions attached to the journal entry.</td><td>No</td></tr><tr><td>Units</td><td>2</td><td>Numeric value of the units attached to this journal entry.</td><td>No</td></tr></tbody></table>
