# Contracts

Customer Contracts screens available to allow user the ability to track customers’ expenditures against contracts’ committed amounts and setup frequency discounts for digital products and volume discount percentage which can apply to print products and all other types of non-frequency based products.

## Client Contract Setup <a href="#_toc115447996" id="_toc115447996"></a>

#### Create Contract <a href="#_toc115447997" id="_toc115447997"></a>

This screen allows you to setup a contract with all details for a customer. Navigate to the menu Customers -> Client Contract Setup.

Choose the advertiser account ID from the drop-down menu. Click the + sign next to the Contract ID to create a new contract. Enter a contract ID which is alphanumeric free format entry, or click Auto Assign to have the system assign an ID. Enter a description for the contract. Enter the start and end dates for the contract and the commitment $ amount.

If desired enter a Sales Rep and a Contact Person for the Contract. These fields are informational.

Note the volume discount field where you can enter a numerical value for the discount the customer gets based on volume of advertisement. In the field “**Multiple Discount Rule**”, there are two options:

* Do NOT Apply Volume Discount if a Frequency Discount is Applied: This option if chosen, the system will not apply the volume discount if the frequency discount is entered.
* Apply Frequency and Volume Discount if Applicable: If chosen, the system applies both frequency and volume discounts where available.

Frequency Rate: Enter the numeric frequency discount for the contract. (See [Frequency Discount Schedules](../setup/advertising-setup/frequency-discount-schedule.md) for Setup). For example if the client is due to get the 6x Frequency Discount, enter a 6 here. Frequencies only apply to Print ads and they are not required. You can just do a volume based discount by putting a percentage discount in the Volume Discount field.

Volume Discount: Enter the volume discount rate you wish to apply to the order when this contract is used.

Volume Discount Rounding: Choose to round the volume discount above to the nearest 1, 5 or 10. This discount is applied in the order per line item and marked as an adjustment.

### Product Override <a href="#_toc115447998" id="_toc115447998"></a>

Choose a product from the drop-down menu and enter the discount for this product which would override the overall discount on the contract. You can enter more than one product.

![](<../../../.gitbook/assets/1 (61).png>)

You can enter a frequency commitment and volume discount which will override the volume discount in the main contract.

### Notes

Enter any notes on this contract and click "Save"

### Revenue Summary

This section offers a summary of the revenue for this advertiser.

![](<../../../.gitbook/assets/3 (74).png>)

### Refresh Summaries <a href="#_toc115447999" id="_toc115447999"></a>

Once the contract is saved and used, click the button “Refresh Summaries” and click the “Include Reserved or Quotes” to view the existing orders in the system which this advertiser has.

![](<../../../.gitbook/assets/2 (86).png>)

Note that the data can be filtered and ordered. Also, if you click the various tabs such as “Summary by Format”, the screen displays the data by the product format in which advertiser purchased an order.

Click the “Summary by Product” to view orders by product. Click the “Summary by Ad Type” and the screen displays the summary by the type of Ad being flat fee or cost per measurement which you already have setup in the system.

The details include net, gross, ratecard amounts discount amounts, and Insertion Counts (note insertion counts only apply to print orders).

### Sales Order Detail

The “Sales Order Detail” provides a full list per line ID and Campaign ID for each of the order for this advertiser.

Note that all lines of data have a hyperlink so that you can drill down into the details.

![](<../../../.gitbook/assets/4 (40).png>)

## List of Client Contracts <a href="#_toc115448000" id="_toc115448000"></a>

This screen shows all contracts that are current where the current period falls within the contract periods.

Navigate to the menu Customers -> List of Client Contracts.

![](<../../../.gitbook/assets/5 (12).png>)

The screen displays the client ID, name, contract information and amounts. Click the hyperlink to each client ID for further drill down and use the excel and PDF to export the data for further use.

## Seeing Contracts in Action <a href="#_toc12277660" id="_toc12277660"></a>

#### Ratecards <a href="#_toc12277661" id="_toc12277661"></a>

Navigate to the menu Setup -> Product Setup -> Ratecards node. Choose the product from the drop-down menu, and then choose the ratecard to which to apply the frequency discount. Choose the schedule from the drop-down menu which you want to apply for frequent orders.

Click the button “Preview Frequency Discount Schedule” and the pop-up screen displays the frequency discount calculation from the base rate in your ratecard and where the system used the discount schedule you chose.

![](<../../../.gitbook/assets/10 (1) (1).png>)

You can then apply the frequency to client contracts where on a Client Contract you can specify what frequency rate to use on print orders.

### Campaign Entry <a href="#_toc115448004" id="_toc115448004"></a>

Navigate to the menu Campaigns -> Enter a New Campaign. Choose the advertiser from the drop-down and the contract displays in the “Default Contract” field.

![](<../../../.gitbook/assets/11 (20).png>)

Save the campaign and click the line item node to enter a new one. Choose a product which is not part of the override list on the contract for this advertiser and use the full line entry.

Note that the field “Contract” contains the client’s contract by default from the campaign header. You can choose the blank field to remove the contract from the list or keep it. If you keep the contract, and enter the line details, note that the Adjustments field automatically calculates the discount this client is entitled based on the contract details.

Click the node “Adjustments” to view all the details of the contract discounts.

Note that the campaign discount value from the discount field on the campaign header is applied in addition to the contract percentage if the campaign has a header default discount.

### Apply Both Frequency and Volume Discounts <a href="#_toc115448006" id="_toc115448006"></a>

Navigate to the Client Contract and set it to apply both frequency and volume discounts with a rounding option for example to the nearest 5, and save the settings.

![](<../../../.gitbook/assets/16 (18).png>)

Create a line item for this advertiser using this contract, and note that the frequency discount is applied first, then the volume discount and rounding are applied separately on the Ratecard amount. Because the Volume discount has a rounding rule to round to the nearest 5, the discount is rounded down to $20.

![](<../../../.gitbook/assets/17 (18).png>)

These amounts are then added up to makeup the adjustment on the line. That adjustment is then subtracted from the ratecard price and multiplied over the number of issues on the order..

### Frequency Discount W/O Contract <a href="#_toc115448007" id="_toc115448007"></a>

You can apply a frequency discount schedule to a Ratecard without a contract. This applies to a campaign with multiple lines that match the frequency on the schedule.

Navigate to display the Ratecard menu for a product from the Setup menu -> Product Setup -> Ratecard.

![](<../../../.gitbook/assets/18 (10).png>)

Check the box corresponding to the field “Apply Frequency Discounts without Contract”.

Choose a schedule in the drop-down field “Default Frequency Rate Discount Schedule field.” You can click the button “Preview Frequency Discount Schedule”. The screen displays what the discount looks like with the frequency in the schedule.

![](<../../../.gitbook/assets/19 (3).png>)

Enter a campaign for the print product using this Ratecard. Choose multiple issues to match or exceed the frequency of the schedule. The lines reflect the discount on the schedule.

![](<../../../.gitbook/assets/20 (4).png>)

This doesn’t apply when you create one-line items on multiple campaigns. It only applies when creating multiple issues on one line.
