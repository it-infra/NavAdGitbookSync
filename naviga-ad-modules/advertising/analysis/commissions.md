# Commissions

## Commissions Reports <a href="#_toc121381221" id="_toc121381221"></a>

Users can view the commissions from the menu Analysis -> Commissions -> Commissions in the advertising module. Note that user can also access these reports from the CRM module Rep Summary menu.

Choose the rep name and financial period from the drop down, and include the view for:

* **All Commissions:** This includes all the rep’s commissions in this period you choose whether the commission has been processed or not.
* **Processed Commissions in This Period:** This will provide a list of all commissions which have been already processed for the period chosen.
* **Commissions Not Processed in This Period:** This is the list of commissions for this rep in this period which have not been processed yet.
* **Commissions Not Processed Up to This Period:** This is the list of commissions for this rep which have not been processed in the system for all periods up to this period chosen.

<figure><img src="../../../.gitbook/assets/image (1616).png" alt=""><figcaption></figcaption></figure>

Check the “processed” box corresponding to the commission you’d like to process and click Save. This operation cannot be undone. Once the commission is processed, the order will display with the check in the processed box and will display under the Commissions Processed criteria. User can expedite the process by clicking “Select All” to process all commissions for the rep in one step.

## Commission Reconciliation Import <a href="#_toc121381222" id="_toc121381222"></a>

It is common for sites to calculate commissions externally and then import them back in. The Reconciliation import allows for that workflow. The report above is downloaded to Excel, modified and imported back in. Please follow these important notes:

* This routine is designed to re-import the Spreadsheet download of Rep Commissions
* You MUST save the modified Excel Download file in XLSX format in order to re-import it here
* You may import any Spreadsheet that contains the 3 required columns for this import: ID, Commission % and Processed
* The ID column is commission file record key provided when the data is downloaded
* Only lines with the "Processed" column marked as True (or Y) will be imported

<figure><img src="../../../.gitbook/assets/image (1430).png" alt=""><figcaption></figcaption></figure>

## Rep Commissions Adjustments <a href="#_toc121381222" id="_toc121381222"></a>

This screen allows the user to create and view the adjustments performed for the commissions on a sales rep. When you choose the sales rep from the drop-down menu, and enter the financial period for which you want to enter or view adjustments to the commission for the rep, and then choose the option:

* **All Adjustments:** This will display all adjustments made already for this rep in this period.
* **Adjustments Processed:** This will display all adjustments which were processed already for this rep in this period.
* **Adjustments Not Processed:** This will display all adjustments for this rep in this period which have not been processed yet.

If you want to create a new adjustment for the rep in this period, click on “New Adjustment”. Enter a reason, which can be any alphanumeric entry, for example, previous error. Click on the magnifying glass to search for the invoice ID against which you’d like to make an adjustment. You can enter the invoice ID if you already know it. Then enter the amount of adjustment which needs to be added or subtracted from the existing commission on this invoice.

![](<../../../.gitbook/assets/1 (21).png>)

Click on the “Save” button and this will create the adjustment.

Now it’s time to process the adjustment, which will display in the screen under “All Adjustments” or “Adjustments Not Processed” for this same period and same rep.

![](<../../../.gitbook/assets/2 (9).png>)

Check the box for the adjustment under the column “Processed” and click on “Save Processed”. This will process the commission adjustment for this rep under this period.

### Commission Adjustment Import

User can import multiple adjustments for multiple sales reps on invoices. Navigate to the advertising module’s menu Analysis -> Commissions -> Commission Adjustments Import. This process can be performed using the provided template.

Click on the button “Download Template”. This step opens a spreadsheet. Fill out the sheet and save to your desktop. For the template details, please see section below titled Template Fields.

![](<../../../.gitbook/assets/1 (96).png>)

Then click the “Select” button to choose the spreadsheet and upload to the system. To flush out any errors on the spreadsheet, click the button “Test Import” and click OK if you get an error because the system will display the line and cause of error.

After correcting any errors, resave the template to your desktop. Then click the x remove button to clear the upload then re-click the select button to upload the corrected sheet. Then click the “Import File” to complete the import file. The system will provide an ID for the import and the adjustments are now imported into the system.

To view the imported adjustments, navigate to the menu Analysis -> Commissions -> Rep Commission Adjustments. Select the reps from the drop-down menu as well as the period for the adjustments. Select the option “All Commissions”, and the system provides a view of all commissions’ adjustments for the selected reps, including the ones you imported above.

![](<../../../.gitbook/assets/2 (75).png>)

#### Template Fields <a href="#_toc79079427" id="_toc79079427"></a>

Click the button “Download Template”.

This will open the excel spreadsheet for you to fill out. The fields are as follows:

<table><thead><tr><th width="160">Field Name</th><th width="162">Sample</th><th width="258">Source</th><th>Optional/ Mandatory</th></tr></thead><tbody><tr><td><strong>Rep ID</strong></td><td>SHIGH</td><td>Naviga Sales Rep ID and must match the value in the system.</td><td>Mandatory</td></tr><tr><td>Rep Name</td><td>Shirley High</td><td>Could be any name, but preferably a match to the name in the system.</td><td>Optional</td></tr><tr><td><strong>Period</strong></td><td>2018-06</td><td>Period where adjustment is to be applied; must match the value in Naviga of periods.</td><td>Mandatory</td></tr><tr><td><strong>Date</strong></td><td>6/20/2018</td><td>The date on which adjustment is entered in the system.</td><td>Mandatory</td></tr><tr><td><strong>Adjustment Amount</strong></td><td>-50.89</td><td>Amount of adjustment; numeric and could be positive or negative.</td><td>Mandatory</td></tr><tr><td><strong>Reason</strong></td><td>User entry error</td><td>Alphanumeric text explaining why the adjustment is needed.</td><td>Mandatory</td></tr><tr><td>Invoice Reference</td><td>MM765</td><td>Invoice ID in reference to the rep’s adjustment in commission.</td><td>Optional</td></tr><tr><td><strong>Processed Y/N</strong></td><td>Y</td><td>Y or N for Yes or No on whether the adjustment is entered in the system, marked as already been processed or still needs processing within Naviga.</td><td>Mandatory</td></tr></tbody></table>

## Rep Commissions Summary <a href="#_toc121381223" id="_toc121381223"></a>

This is a report which provides commissions per rep between a start and end financial period. The report displays any sales, adjustments, net sales and totals for a commission per product and the totals

<figure><img src="../../../.gitbook/assets/image (224).png" alt=""><figcaption></figcaption></figure>

User can group by sales rep or by any other column by dragging the column heading to the bar indicating so. User can also order descending or ascendingly any of the columns.

## Processed Commissions Report <a href="#_toc121381224" id="_toc121381224"></a>

This is a report of all processed commissions on the order sales for a rep during a start and end date which user chooses from the calendar pop ups.

The data displayed includes the financial period to which the commission applies, the campaign and line IDs, the campaign type, advertiser name, brand, the website name, the line description, the line start and end dates, any other reps sharing the commission on the order, the rep’s percentage share of the commission if applicable, the rep’s commission amount, commission amount, the commission percentage which the rep receives, the invoice ID on the campaign, the payment status of the invoice, the commission processing date and the user ID of the person who processed the commission.

<figure><img src="../../../.gitbook/assets/image (1275).png" alt=""><figcaption></figcaption></figure>

## This Year V. Last Year Commission Report <a href="#_toc121381225" id="_toc121381225"></a>

This report provides a comparison between the actual rep’s commissions for this current year versus last year’s commissions. The data can be limited by product group as well.

Enter the financial period for which you want the commissions per rep to display and choose Advertising or Exhibitions as the type order to show. Choose the product group from the drop-down menu, if desired.

Note that you can leave the amounts to show in local currency or choose the different currency you want to the amounts to display based on the currency tracking setup previously done in the setup menu.

<figure><img src="../../../.gitbook/assets/image (905).png" alt=""><figcaption></figcaption></figure>

Click on the arrow to retrieve the data. The data displays by sales rep grouped together. The rep group, and product name will display being the digital or print products. The actual amounts will display for the chosen period and the corresponding period from last year. Also, the year to date actuals for each year will display. The total commissions for last year will display per line.

Note that the products display the amounts based on the billed orders for performance campaigns and based on the confirmed orders for flexible campaigns.

The data can be exported to excel by clicking on the excel icon.

You can also group the data by additional columns. To do so, click on the name of the column you want to group the data by and drag it to the top next to the “Sales Rep” column by which the data is already grouped.

This will display the data by rep and then by product or any column you chose for this rep.

To remove any of the columns’ grouping the data, click on the x next to the name of the column.

Click on any of the columns to sort in an ascending order and click again to sort in a descending order.

## Commissions Report Based on Applied or Received Payment <a href="#_toc121381226" id="_toc121381226"></a>

Commissions report displays data based on payments for orders based on Received Date vs. Applied Period according to the billing period.

The report produces more details about the installment payment for the billing stage as well as invoice details.

Navigate to the menu Analysis -> Commissions -> Commissions Based on Payments.

The report displays the stage paid for the flexible campaign and the line paid for the performance campaigns.

<figure><img src="../../../.gitbook/assets/image (1317).png" alt=""><figcaption></figcaption></figure>
