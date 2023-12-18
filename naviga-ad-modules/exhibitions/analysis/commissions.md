# Commissions

## Exhibition Commissions

Users can view the commissions from the menu Analysis -> Commissions -> Exhibition Commissions in the Exhibition module. Note that user can also access these reports from the CRM module Rep Summary menu -> My Commissions

Choose the rep name and financial period from the drop down, and include the view for:

* **All Commissions:** This includes all the rep’s commissions in this period you choose whether the commission has been processed or not.
* **Processed Commissions in This Period:** This will provide a list of all commissions which have been already processed for the period chosen.
* **Commissions Not Processed in This Period:** This is the list of commissions for this rep in this period which have not been processed yet.
* **Commissions Not Processed Up to This Period:** This is the list of commissions for this rep which have not been processed in the system for all periods up to this period chosen.

<figure><img src="../../../.gitbook/assets/image (1240).png" alt=""><figcaption></figcaption></figure>

Check the “processed” box corresponding to the commission you’d like to process and click Save. This operation cannot be undone. Once the commission is processed, the order will display with the check in the processed box and will display under the Commissions Processed criteria. User can expedite the process by clicking “Select All” to process all commissions for the rep in one step.

## Processed Exhibition Commissions Report

This is a report of all processed commissions on exhibition sales for a rep during a start and end date which user chooses from the calendar pop ups.

<figure><img src="../../../.gitbook/assets/image (1404).png" alt=""><figcaption></figcaption></figure>

The data displayed includes the financial period to which the commission applies, the exhibitor name, division, the exhibition name, show date, any other reps sharing the commission on the order, the rep’s percentage share of the commission if applicable, the rep’s commission amount, commission amount, the commission percentage which the rep receives, the invoice ID, the payment status of the invoice, the commission processing date and the user ID of the person who processed the commission.

## Rep Commission Summary

This is a report which provides commissions per rep between a start and end financial period. The report displays any sales, adjustments, net sales and totals for a commission per product and the totals. This report includes both Advertising commissions and Exhibitions Commissions in one report.

<figure><img src="../../../.gitbook/assets/image (224).png" alt=""><figcaption></figcaption></figure>

User can group by sales rep or by any other column by dragging the column heading to the bar indicating so. User can also order descending or ascendingly any of the columns.

## This Year vs Last Year Commission Report

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

## Rep Commission Adjustments

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

## Commission Reconciliation Import

It is common for sites to calculate commissions externally and then import them back in. The Reconciliation import allows for that workflow. The report above is downloaded to Excel, modified and imported back in. Please follow these important notes:

* This routine is designed to re-import the Spreadsheet download of Rep Commissions
* You MUST save the modified Excel Download file in XLSX format in order to re-import it here
* You may import any Spreadsheet that contains the 3 required columns for this import: ID, Commission % and Processed
* The ID column is commission file record key provided when the data is downloaded
* Only lines with the "Processed" column marked as True (or Y) will be imported
