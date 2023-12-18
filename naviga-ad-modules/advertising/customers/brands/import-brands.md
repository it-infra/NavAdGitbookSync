# Import Brands

## Brand Import <a href="#_toc119329780" id="_toc119329780"></a>

Navigate to the menu Customers -> Brands -> Brand Import.

Click on the menu “Download Template”. Fill in the columns as described below in the Templates section. Save the file to your desktop.

Click on “Select” and upload the template you saved. Click “Test Import File” and the system alerts you to any errors in the template you made.

![](<../../../../.gitbook/assets/1 (46).png>)

Click “Close” and then click “Remove x”. Navigate back to the template on your desktop and correct the errors. Save the template and then re-select the template to upload into Naviga from the import screen. Once all errors are cleared and the system provides you with a success message, click “Import File”.

Note that you can click “Use Legacy ID” button to change it to “Yes”, if the Advertiser ID you enter in the import template is the legacy ID and not the Naviga Advertiser ID.

When the import is complete, you will receive a confirmation message that the import was successful.

![](<../../../../.gitbook/assets/2 (13).png>)

Navigate to the menu Customers -> Brands -> Brand Maintenance. Search for the advertiser you used in the import template and in the brand drop-down, search for the Brand you just imported.

![](<../../../../.gitbook/assets/3 (56).png>)

The brand details included in the import file should display on this screen as well as the Rep Assignments screen displaying the rep you assigned to the imported brand.

The brand is now ready for use in the orders.

![](<../../../../.gitbook/assets/4 (71).png>)

### Import Template <a href="#_toc119329781" id="_toc119329781"></a>

Fill in the import template with the details as described below in the given examples. The table provides you with the source of data which must match Naviga data.

<table data-header-hidden><thead><tr><th width="164"></th><th width="111"></th><th width="330"></th><th></th></tr></thead><tbody><tr><td><strong>Field</strong></td><td><strong>Example</strong></td><td><strong>Source of Data</strong></td><td><strong>Mandatory/ Optional</strong></td></tr><tr><td><strong>Advertiser ID</strong></td><td>244529</td><td>This must match the Advertiser’s ID in Naviga. If you check the “Use Legacy ID” on the import screen, then this is the legacy ID.</td><td>Mandatory</td></tr><tr><td>Brand ID</td><td>B1</td><td>Free form alphanumeric entry of brand ID you’d like to identify the brand with for use in campaigns.</td><td>Optional</td></tr><tr><td>Brand Name</td><td>Brand Import</td><td>Free alphanumeric entry of the description of the brand.</td><td>Optional</td></tr><tr><td><strong>Category ID</strong></td><td>ACCESS</td><td>This value must match the PIB/ Category/ Industry Code in Naviga.</td><td>Mandatory</td></tr><tr><td>Agency ID</td><td>323444</td><td>This must match the Agency ID in Naviga.</td><td>Optional</td></tr><tr><td>Production Controller ID</td><td>SH</td><td>This is the same ID of the production controller from Naviga who is not assigned to this brand.</td><td>Optional</td></tr><tr><td>Default Discount % on Ad Campaigns</td><td>5</td><td>Numeric percentage value which is the default discount applied to orders once the brand is used in the order.</td><td>Optional</td></tr><tr><td>Default Rep to Assign in Order Entry</td><td>Y</td><td>This determines whether you’d like this brand to default to require the user to enter a rep in order entry every time the order is entered. If left blank the system assumes it’s a No. Or enter Y for Yes. If this is set to Yes, you must leave the REP ID1 and all REP ID columns blank.</td><td>Optional</td></tr><tr><td>Product Group ID</td><td>SHNA</td><td>This must match the Product Group ID in Naviga. You can enter Product Group ID here or the Product ID in the next column, but not both. Leave blank if you want the rep to be the default on the brand in any order.</td><td>Optional</td></tr><tr><td>Product ID</td><td></td><td>This must match the Product ID value. Leave blank if you want the rep to be the default on the brand in any order.</td><td>Optional</td></tr><tr><td>Rep ID 1</td><td>SHIGH</td><td>This must match the Salesrep ID in Naviga.</td><td>Optional</td></tr><tr><td>Rep Percent 1</td><td>60.00</td><td>This is a numeric value of the percentage of the rep’s share of the commission.</td><td>Optional</td></tr><tr><td>Rep ID 2</td><td>BOB</td><td>Enter this value if the brand commission is shared among reps. This value must match the Rep ID in Naviga.</td><td>Optional</td></tr><tr><td>Rep Percent 2</td><td>40</td><td>This is a numeric value of the percentage of the rep’s share of the commission.</td><td>Optional</td></tr><tr><td>Rep ID 3</td><td></td><td>Enter this value if the brand commission is shared among reps. This value must match the Rep ID in Naviga.</td><td>Optional</td></tr><tr><td>Rep Percent 3</td><td></td><td>This is a numeric value of the percentage of the rep’s share of the commission.</td><td>Optional</td></tr><tr><td>Rep ID 4</td><td></td><td>Enter this value if the brand commission is shared among reps. This value must match the Rep ID in Naviga.</td><td>Optional</td></tr><tr><td>Rep Percent 4</td><td></td><td>This is a numeric value of the percentage of the rep’s share of the commission.</td><td>Optional</td></tr><tr><td>Notes</td><td>This brand is …</td><td>Free alphanumeric entry for the notes. They will display after the import in the brand maintenance.</td><td>Optional</td></tr><tr><td>Tearsheet Contact ID</td><td>244535</td><td>The ID must match the advertiser individual ID in Naviga. This information is in the Advertiser/ Agency Maintenance screen under Employee ID.</td><td>Optional</td></tr><tr><td>Tearsheet Delivery Method</td><td>E</td><td><p>The value here must be one of the following:</p><p>E = Email, M = Mail, N = None</p></td><td>Optional</td></tr><tr><td>Number of Tearsheets</td><td>3</td><td>Numeric value for the number of tearsheets to provide the advertiser.</td><td>Optional</td></tr></tbody></table>
