# Change/Import Sales Rep Assignments

## Change Sales Rep Assignment in Bulk <a href="#_toc98514799" id="_toc98514799"></a>

Navigate to the Customers menu -> Brands -> Change Salesrep Assignments.

![](<../../../../.gitbook/assets/9 (26).png>)

Choose the current Salesrep from the drop-down menu and click “Get Data”. Select desired brands or select all using the check boxes.

At the bottom, choose the new Salesrep who you’d like to replace the current one.

Check the flag “Re-assign Future Commissions” to “Yes” if you’d like all future unbilled orders to change the Salesrep and assign these orders’ commissions to the new Salesrep.

Check the flag “Replace Order Reps” to “Yes” if you’d like to change the Salesrep on all actively running and future orders. Click “Apply Change”. This will perform these functions.

{% hint style="info" %}
Note - to change the rep for one customer / Brand see [Customers -> Brands -> Brand Maintenance](./#\_toc115259173)
{% endhint %}

## Import Rep Assignments for Campaign Sales <a href="#_toc41990731" id="_toc41990731"></a>

User can import sales reps’ assignment to a brand/product group combination using a provided template. The template allows user to enter multiple sales reps’ assignments to the respective brand/product group, so when user enters orders the system will automatically assign the order to the rep as imported. The template includes an effective date field for when this takes effect as well as financial period to use instead of the effective date, the rep ID and the percentage commission. The template allows for up to four reps and split of commissions among them.

Navigate to the menu Customers -> Brands -> Import Sales Rep Assignments -> Campaign Sales Rep Assignments node -> Import Rep Assignments.

Click on “Download Template” and an excel template displays with the following fields to fill out as in the template section.

Check the box “Update Unbilled Orders” to have the value “Yes”, if you’d like the orders that haven’t been billed yet to be updated with the sales rep information for the brand.

Check the box “Update Unprocessed Commissions Records” to “Yes” if you’d like to update any commissions allocations that have not been processed yet with the new information.

Check the box "Use Legacy ID" if the Advertiser ID in the import file is the Legacy ID rather than the Naviga Advertiser ID

Once you fill out the template, save it to the desktop and then return to the import screen and click “Select” button to browse for the file you saved. Then click on the button “Test Import” and the system will let you know if you have any errors to correct, resave the template and re-browse for the template to replace the existing one.

<figure><img src="../../../../.gitbook/assets/image (648).png" alt=""><figcaption></figcaption></figure>

Click on the button “Import File” and the data will be imported successfully. Click on the node “List of Imported Rep Assignments” and look for the import ID. The data for the rep will display.

![](<../../../../.gitbook/assets/2 (63).png>)

Proceed to enter an order which will reflect that information for this rep and his commission.

### Import Template <a href="#_toc41990732" id="_toc41990732"></a>

<table data-header-hidden><thead><tr><th width="179"></th><th width="111"></th><th width="314"></th><th></th></tr></thead><tbody><tr><td><strong>Field Name</strong></td><td><strong>Example</strong></td><td><strong>Conditions</strong></td><td><strong>Mandatory (Yes/No)</strong></td></tr><tr><td>Advertiser ID</td><td>244534</td><td>Must match the System Advertiser ID, unless the box was checked above to use Legacy ID, in which case the ID would need to match the Legacy ID</td><td>Y</td></tr><tr><td>Brand ID</td><td>A1</td><td>Must match the System Brand ID</td><td>Y</td></tr><tr><td>Product Group ID</td><td>BF</td><td>Must match the System Product Group ID if the reps are to be imported into the Sales Rep Overrides by Product Group section</td><td>Y/N</td></tr><tr><td>Product ID</td><td>DEMO10</td><td>Must match the System Product ID if the reps are to be imported into the Sales Rep Overrides by Product section. If neither Product Group ID nor Product ID are provided then the Reps below will be placed in the "Default Sales Rep Assignments" section</td><td>Y/N</td></tr><tr><td>Rep ID 1</td><td>GLB</td><td>This is the rep ID which must match the value in System.</td><td>Y</td></tr><tr><td>Rep Percent 1</td><td>100</td><td>Numeric percentage.</td><td>N</td></tr><tr><td>Rep ID 2</td><td>DLG</td><td>Same as Rep 1 if more than one rep is assigned to the brand.</td><td>N</td></tr><tr><td>Rep Percent 2</td><td>100</td><td>Numeric Percentage</td><td>N</td></tr><tr><td>Rep ID 3</td><td>DLG</td><td>Same as Rep 1 if more than one rep is assigned to the brand.</td><td>N</td></tr><tr><td>Rep Percent 3</td><td>100</td><td>Numeric Percentage</td><td>N</td></tr><tr><td>Rep ID 4</td><td>DLG</td><td>Same as Rep 1 if more than one rep is assigned to the brand.</td><td>N</td></tr><tr><td>Rep Percent 4</td><td>100</td><td>Numeric Percentage</td><td>N</td></tr></tbody></table>

## Import Rep Assignments for Exhibition Sales <a href="#_toc41990733" id="_toc41990733"></a>

User can import sales reps’ assignments using the same screen as in the advertising module.

Navigate to the menu Customers -> Brands -> Import Sales Reps Assignments -> Import Reps Assignments node under the section "Exhibition Sales Rep Assignments".

Click the box “Update Unbilled Orders” to change the value to a “Yes” if you want these values you are importing to override the existing values in System.

Click the box for “Update Unprocessed Commission Records” as “Yes” if you want to update the commission records which have not been processed with the values in the imported template.

Click the button “Download Template” and the spreadsheet template displays on the screen.

![](<../../../../.gitbook/assets/5 (7).png>)

Enter the values in the sheet according to the template section below. Save the sheet to your desktop.

On the System, click the “Select” button to upload the template sheet.

On the System screen, click the button “Test Import File” which prompts the system to check for errors in your sheet. If there are errors, click the x remove button on System screen. Fix the errors on the sheet and re-save the sheet to your desktop. Repeat the upload and the test steps till the system indicates with a message that the template is free of errors. Then click on the button “Import File”.

The system provides an import ID. Click OK then click the node on the tree “List of Imported Rep Assignments”.

Enter the ID in the drop-down menu and the system provides you with a listing of all the assignments you imported.

### Import Template <a href="#_toc41990734" id="_toc41990734"></a>

<table data-header-hidden><thead><tr><th width="208"></th><th width="108"></th><th width="287"></th><th></th></tr></thead><tbody><tr><td>Field Name</td><td>Example</td><td>Data Source</td><td>Mandatory or Optional</td></tr><tr><td><strong>Exhibitor ID</strong></td><td>14009</td><td>This must be the same ID of the exhibitor in System</td><td>Mandatory</td></tr><tr><td><strong>Division ID</strong></td><td>A3</td><td>This must be the same ID as the division in System.</td><td>Mandatory</td></tr><tr><td><strong>Group ID</strong></td><td>SH</td><td>The must be the same as the exhibition group ID in the system which can be found in the Exhibition Maintenance.</td><td>Mandatory</td></tr><tr><td><strong>Rep ID 1</strong></td><td>SH2</td><td>This must match the sales rep ID in System. This is the rep to which you are assigning the brand.</td><td>Mandatory</td></tr><tr><td>Rep Percent 1</td><td>75</td><td>This is a numeric value of the percentage commission which this rep is assigned.</td><td>Optional</td></tr><tr><td>Rep ID 2</td><td></td><td>This must match the second sales rep ID in System if this rep is splitting the commission with the first rep.</td><td>Optional</td></tr><tr><td>Rep Percent 2</td><td>25</td><td>This is a numeric percentage value of the commission shared with the first rep.</td><td>Optional</td></tr><tr><td>Rep ID 3</td><td></td><td>This must match the second sales rep ID in System if this rep is splitting the commission with the first rep.</td><td>Optional</td></tr><tr><td>Rep Percent 3</td><td></td><td>This is a numeric percentage value of the commission shared with the first rep.</td><td>Optional</td></tr><tr><td>Rep ID 4</td><td></td><td>This must match the second sales rep ID in System if this rep is splitting the commission with the first rep.</td><td>Optional</td></tr><tr><td>Rep Percent 4</td><td></td><td>This is a numeric percentage value of the commission shared with the first rep.</td><td>Optional</td></tr></tbody></table>
