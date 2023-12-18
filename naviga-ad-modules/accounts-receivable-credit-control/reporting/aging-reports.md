# Aging Reports

There are different aging reports available in the accounts receivable module under the Reporting menu:

## Current A/R aging report by customer.

This provides real time aging balances by due date or invoice date arranges them in buckets of days. It also provides the total balance due as well as the cash on account for each customer. Click on the customer ID to open the customer account screen and get additional details.

<figure><img src="../../../.gitbook/assets/image (1357).png" alt=""><figcaption></figcaption></figure>

## A/R Aging Detail Report

Provides the aging as of a certain period or date. It also provides the number of transactions per client as well as the ability to download the summary to Excel. User can also expand using the arrow for each item and click download details to excel to export this data to a spreadsheet. The client summary report includes the address details, contact information and credit limit of the client. Click on the customer ID to open the customer account screen and get additional details. When expanded to show the transaction details click on the Transaction ID to open the invoice or payment details screen.

<figure><img src="../../../.gitbook/assets/image (781).png" alt=""><figcaption></figcaption></figure>

## The Big A/R Aging report

This report allows user to create a template and save the template to continue to use it as well as modify it and create variations of it to generate the report. Prior to first use, user should set up the parameters for the template from the node “Default A/R Aging Parameters”. This will define the parameters for the report and the formatting of the report. The Default A/R Aging Parameters are set for the system, so all users will share the same Default Aging Parameters.

### Default Settings for the A/R Aging Report for all Users

User can setup the default values for all users of the A/R Aging Report by navigating to the **A/R Module -> Reporting -> The BIG A/R Aging Report -> Default A/R Aging Parameters**.

Click all the fields to Yes or No to display or not respectively. Click Save Defaults and click OK to the confirmation message. Then click the node Run A/R Aging Report and the defaults will already be setup as in the defaults node.

<figure><img src="../../../.gitbook/assets/image (167).png" alt=""><figcaption></figcaption></figure>

The First column in the Default Parameters displays what will be shown in the columns on the report. Some of these columns are optional, some are standard. The optional columns have a check box to the left and user can decide if they want that column hidden or not.

* **Transaction Type** - This will be a code depicting what sort of transaction is being displayed. This is only relevant when the report is running in detail mode. Examples are I for Invoice, P for Payment, COA for Cash on Account, etc.
* **Invoice Number / Invoice Date** - (obviously these are the invoice number and date of the invoice)
* **Original Amount** - This is the Original amount of the invoice. Again, only relevant when running in detail mode. It may be helpful for the user viewing the report to know for example, if they are looking at an invoice with $100 in 120 Days bucket if that is an invoice that was originally $100 or if that is just the balance remaining of a much larger invoice.
* **Buckets** - If running the report by the default is to view the aging report as "age by days" this section will define the increments. Typically, aging is done 0-30, 30-60, 60-90, etc, but this allows user to deviate from that standard and have more or fewer aging buckets with different ranges of days in it. If running as Age by Period, then these groupings are not relevant.
* **Unallocated** - This is an optional column and will display payment/prepayment amounts which are unallocated.
* **Balance Due** - This column will display the balance due, either on the customer if run in summary more, or on each individual invoice and the customer if run in detail mode.
* **Not Yet Due** - Optional Column - will display the amounts that are not yet due. For example, one might run the report with aging method 'Age from Invoice Date' and an invoice might fall into the bucket of 30-60 days, but if that invoice is not due until 60 days, it may be helpful for the user reading the report to understand that that invoice isn't yet due.
* **Prepaid** - For Payment transaction types this will indicate if the amount is a prepayment for an order which has yet to be billed.
* **Product** - For this to really be relevant, billing must be run by product, so that each invoice represents a single product. Otherwise, selecting this option will only display the first product found on the invoice, so it may not be desirable to display if invoices typically include many products.
* **Sales Rep** - This will display the sales person ID on the order.

The middle column in the Default A/R Aging Parameters Sets the Selection Options and the Formatting Options. Some of these are fairly obvious what they include / exclude, while other may need some explanation:

#### Selection Options

* **Include Prepaids in Unallocated Column**
* **Include Service Charges**
* **Include Application Summary Comments** - On payments, this will include the "comment" field entered when applying a payment.
* **Suppress Credit Balance Accounts / Select Only Credit Balance Accounts** - These two options are mutually exclusive. Select one and the other will be grayed out. You cannot say "yes" to both of these
* **Exclude Cash on Account for Pre-Payments**
* **Exclude Cash on Account with No Invoice type**
* **Suppress Headings After First Page**
* **Suppress Cash on Account**

#### Formatting Options

* Date Format - Options here are for Month/Day/Year or Day/Month/Year. Day Month Year has short and long format options\
  ![](<../../../.gitbook/assets/image (1732).png>)
* Number Format - Options here allow for commas or no commas, decimals or no decimals:\
  ![](<../../../.gitbook/assets/image (1733).png>)
* Zero Fields - For data in the columns, user can decide if they wish to see zeros in columns without data, or have it be blank (use spaces).\
  ![](<../../../.gitbook/assets/image (1734).png>)

The last column in the defaults will set what is displayed in the Summary and details. Summary Display options are displayed once for each customer and is shown before the detailed invoices. These options are only relevant when running in Detail mode.

#### Summary Options:

* **Print the Bill-to Address** - Prints the client's address below their name on the Detail Report
* **Print the Bill-to's Telephone Number** - Prints the client's phone number below their name on the Detail Report
* **Print the Last Payment** - Prints the client's last payment date and amount on the Detail Report
* **Print the Credit Rating -** If selected, this will display on the report. It comes from the Client Info section in Name Maintenance (A/R Setup node)
* **Print Credit Limit** - This comes from the same place as credit rating above. If set to yes, this field will display on the report.

#### **Detail Options**

* **Print the Brand Address** - If selected, the Brand's address will be displayed. For this to work, the brand must be included in the sort options
* **Print the Brand's Telephone Number** - If selected, the Brand's phone number will be displayed. For this to work, the brand must be included in the sort options
* **Print Ad Confirmation Contact** - This will display at the top of the report and will show the default confirmation contact from Advertising setup in Name Maintenance.
* **Print Issue ID -** Only relevant to Classic systems. Disregard for Digital First
* **Print Issue Date -** Only relevant to Classic systems. Disregard for Digital First
* **Print Invoice Due Days** - if selected, this will show the exact days of this invoices aging
* **Print Credit Control Notes** - this will display the most recent credit control note related to the invoice.
* **Print P.O. Number** - for an advertising invoice, this will display the PO number beneath the invoice. For a Misc. A/R Invoice this will display the Invoice Description
* **Age Cash on Account -** If selected, COA will be assigned to a bucket based on age.

### Sort Codes

User can create a new sort option for the BIG A/R Aging Report from this node. Click the Sort Codes node then click the new button.

<figure><img src="../../../.gitbook/assets/image (644).png" alt=""><figcaption></figcaption></figure>

**Sort Option:** Choose Auto Assign for the new ID which will prompt the system to generate an ID for this sort option. User has the option to unclick this auto assign option and enter a sort ID of user’s choice.

**Description:** Enter a description or click Auto so the system can generate a description.

**Invoice Sort Option:** Choose to sort by oldest invoice, newest invoice date, invoice number or current balance.

**Bill to Sort Option:** Choose to sort the bill to either by bill to name, ID or current value. This will determine the sort order in the end report.

The next 3 options will only become enabled after the Column Sort Order is defined at the bottom of the screen:

* **Sort the advertiser or exhibitor by name:** By default, the system will sort advertiser / exhibitor by their IDs. This option allows you to instead sort by their names. _**You must include the advertiser or exhibitor name in the sort columns to use this option.**_
* **Repeat Invoice for Each Split Rep:** If user chooses "sales person" as a sort column on this screen, the system will unlock this option to be available for user. If this is chosen, each sales person will see the same invoice in their list of invoices.
* **Email Sales Rep:** If user chooses **sub-total and page break** check boxes for this option, then this option will also be allowed to be used.

User will then run the report using this sort code in the sort option on the Run Aging Report node and view the sort options chosen.

Note that invoices or credit invoices which don’t have a sales rep on them will not display in the aging report which is sorted by sales rep.

User can edit or delete sort codes at any time.

### Run A/R Aging Report

Navigate to the A/R menu Reporting -> The BIG A/R Aging Report and enter all the criteria as desired.

#### A/R Aging Report Parameters Section

<figure><img src="../../../.gitbook/assets/image (44) (1).png" alt=""><figcaption></figcaption></figure>

In the top right corner of the screen is a saved template dropdown. The first time this report is run there won't be any templates yet. When you run the report you are presented with an option to save the criteria as a template for subsequent runs. Your templates belong to you as a user, so creating a new template or saving over an existing template will not affect any other users.

<figure><img src="../../../.gitbook/assets/image (590).png" alt=""><figcaption></figcaption></figure>

**Age by Date or Period** - the options in the first column will vary depending if you choose to age by date or by period:

<figure><img src="../../../.gitbook/assets/image (48) (1).png" alt=""><figcaption></figcaption></figure>

If the option chosen is age by period, the following options will be available:

**Age As of Period** - Enter the desired period here and the report will be run as of that period.

**Aging Column Option** - options here are Use Period or Use Days. If Period is chosen the column headings will display periods. The first period will be the "as of period" from above, and then the remaining columns will be the periods prior to that period.

<figure><img src="../../../.gitbook/assets/image (49) (1).png" alt=""><figcaption></figcaption></figure>

If use days is selected the day groupings set up in the aging parameters will be displayed

<figure><img src="../../../.gitbook/assets/image (50) (1).png" alt=""><figcaption></figcaption></figure>

**Min. Invoice Balance:** Enter a balance here if you wish to exclude certain balances (for Example ignore anything with $5.00 or less balance, enter 5.00 in this field. Leave blank to include all balances.

**Ignore Transactions before this Date:** Enter a date in here to exclude transactions before that date.

If the option chosen is age by date, the following options will be available:

**Aging Method:** Options include age by invoice date or age by due date

**Date to Use:** Options include use check date or use applied date

**Aging as of Date:** Enter date in this field to age as of this date. For example, if you put today's date in this field, the aging buckets will be calculated from today. If an earlier date is used, perhaps the last day of the prior month, then the aging buckets will be calculated as of that date.

**Days Past Due:** Enter # of days past due here if you wish to limit the output to only items more than a certain # of days past due. For example, if I were running this by sales person with the idea that they would help to collect on things that are quite old, I may enter 90 or 120 here, and the report will only show things that are older. This can be left blank to include all open invoices.

**Min. Invoice Balance:** Enter a balance here if you wish to exclude certain balances (for Example ignore anything with $5.00 or less balance, enter 5.00 in this field. Leave blank to include all balances.

**Ignore Transactions before this Date:** Enter a date in here to exclude transactions before that date.

In the second column the following options are available:

**Report Detail** - The chosen option will affect how the report will display and also whether or not an excel download will be available The choices are as follows:

*   **Detail** - This will include detailed invoices for each customer on the report. Below is an example, though yours may differ based on other chosen parameters. This option will include an excel download of the data.\\

    <figure><img src="../../../.gitbook/assets/image (1737).png" alt=""><figcaption></figcaption></figure>
*   **Summary** - This will not include invoice level details like the above report. For each customer, there will just be a single line showing the totals by aging bucket. This will include a download of the data to Excel, as long as the Bill-to / Agency is subtotaled as part of the "Sort Codes" setup for the selected Sort Option.\\

    <figure><img src="../../../.gitbook/assets/image (1738).png" alt=""><figcaption></figcaption></figure>
*   **Totals Only** - As the name suggests, this is a report which only shows the report totals. As such, there is no detailed data to include in an excel download, so the download button will just give you a message that there are none available. Example report might look like this (again, based on other settings, your view might differ slightly):\\

    <figure><img src="../../../.gitbook/assets/image (1739).png" alt=""><figcaption></figcaption></figure>
*   **Custom** - This one is similar to the totals only in the data that is displayed, but it is a custom display of that data. It is essentially disregarding the settings for columns and what to display and is using a set of pre-defined and hard coded aging buckets and options. It is displayed in rows rather than columns like the other reports. There is no excel download available for this report.\\

    <figure><img src="../../../.gitbook/assets/image (1740).png" alt=""><figcaption></figcaption></figure>
*   **Summary on First Break Field** - this will look at the sort selected and the first page break that is available on that sort will be what the report is summarized on. This is an example where the bill to was the sort field and there was a page break on the bill-to, so instead of showing all the details for this client on the page, it only shows a summary. There is no excel download for this option.\\

    <figure><img src="../../../.gitbook/assets/image (1742).png" alt=""><figcaption></figcaption></figure>

**Show Invoice Payments** - This option only relevant on "Detail" Report Detail Option. This option will show a detail line for payments against open invoices if set to yes.

**Suppress Zero Lines** - If set to yes, a line will not be shown if it is zero value. May not want to run this with a "no" for a "Detail" report, or you will see all advertisers, even if they have a zero balance and will see all invoices, even if they are paid. - will make for a pretty long report. Here are some examples of a summary report with this set to no: (first one is sorted by name and the second by open balance:

<figure><img src="../../../.gitbook/assets/image (1743).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1744).png" alt=""><figcaption></figcaption></figure>

**Sort Option** - See Discussion above around [Sort Codes](aging-reports.md#sort-codes)

**Companies** - This is a filter to include invoices from one or more system companies.

**Currencies** - This option will filter the report to only show a particular currency. Leave blank to show all currencies

**Modules** - When creating Miscellaneous invoices in A/R the Module is selected during invoice entry. This will filter for those modules. Leave blank to include all.

#### Customer Selection Criteria

<figure><img src="../../../.gitbook/assets/image (1745).png" alt=""><figcaption></figcaption></figure>

* **Clients** - to filter by client(s) select a client from the dropdown or using the search and then click plus to add to be box above. Repeat until you have selected all the clients you wish to see in the report.
* **Credit Controller** - Select a credit controller to filter the report to show only accounts belonging to that credit controller. Leave blank to include all.
* **Client Group** - Select one or more client groups. These are the A/R Client Groups created in **Setup ->** [**Client Group Setup**](../setup-a-r-system-setup/other-a-r-setup-menu-items.md#client-group-setup)
* **Collection Agencies** - Options here allow users to NOT include Collection Agencies at all, Include ONLY Collection Agencies, or to Include them, but only at the End of the Report.
* **Zip Code Ranges** - Can filter by zip codes by adding one or more ranges
* **Min/Max Account Balance** - Enter numbers here to include only clients that have a certain balance on their account.
* **Client type** - This is an internal Client Type. Valid options are AD (for Advertiser), AG (For Agency), or CC (for Collection Agencies).

#### Advertising Specific Selection Criteria

![](<../../../.gitbook/assets/image (1746).png>)

Filter by Product Groups or Ad types by making one or more selections in these dropdowns.

#### Other Module-Specific Selection Criteria

![](<../../../.gitbook/assets/image (1747).png>)

**Sales Reps** - Select one or more sales reps in this field to filter the report to only those reps

**Exhibitions** - Select one or more shows from the dropdown and click the plus sign to only include those shows in this report.

#### Aging Parameters

Most of these fields were already discussed above in [**Default A/R Aging Parameters**](aging-reports.md#default-settings-for-the-a-r-aging-report-for-all-users)**.**

Note that the stationary field is mandatory and is not one of the defaults already discussed. If the users does not select a stationary, they will be not be able to view the report. Choose any of the options which fit the screen best. The field just above stationary displays the calculated report width based on the selection options in the left column.

{% hint style="info" %}
The stationary options that are selectable will vary with the amount of information you have elected to see. For example, if you override the aging days defaults and need to use up all 8 buckets, plus you want to see the unallocated broken out, plus prepays, etc...well, that just isn't going to fit on a portrait pdf with a larger font, so those stationary options will be grayed out.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (428).png" alt=""><figcaption></figcaption></figure>

Click “Generate Report”. The pop up screen to save the report as a template or save over another template pops up. Enter desired information and click OK. (you can leave those fields blank if you are testing out some new options and don't wish to overwrite your existing template.)

{% hint style="info" %}
Note there is no option to delete or rename a template, so name it something meaningful.
{% endhint %}

Once the report popup message appears with the report number, user can click the node View Reports and when the report is complete, user will be able to view the pdf link to the report or download the details to excel. (See notes above on Report Detail to see what types of reports include/exclude data in the excel download)
