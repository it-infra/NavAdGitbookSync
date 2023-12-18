# Reporting

This menu provides a variety of reports for user, including aging reports, client ranking reports by spending amounts, A/R Statements and more.

## Aging Reports <a href="#_toc124065027" id="_toc124065027"></a>

See [Aging Reports](aging-reports.md) Section

## A/R Statements <a href="#_toc124065029" id="_toc124065029"></a>

See [Statements ](../statements.md)section.

Statements can be accessed from the Statements menu or from the Reporting Menu.

## Client Ranking Reports <a href="#_toc124065029" id="_toc124065029"></a>

Click on the Reporting menu and then any of the 3 ranking reports available. These reports provide a summary of advertisers by spending amounts, or over the 12 financial periods, or a spending trend over 5 years span.

### Client Ranking Report

![](<../../../.gitbook/assets/2 (7)>)

#### Revenue Category (Recommended Prerequisite)

This report will run without setting up Revenue Categories and you can subtotal by GL Accounts, but setting up Revenue Categories might make it more meaningful for you. For example, you might want to have categories like "Print Revenue" and "Digital Revenue" to allow for easier to read summaries rather than having lots of actual G/L Codes being displayed.

To create a revenue category, navigate to the menu **Setup -> Revenue Categories.**

<figure><img src="../../../.gitbook/assets/image (1475).png" alt=""><figcaption></figcaption></figure>

Add the category ID which must be unique, description, and sort order in which you would like the revenue category to appear.

Click the + sign to add the category. Create more as needed. Click the save button to store the settings.

These revenue categories can be attached to one or more G/L accounts by navigating to the G/L module and navigate to the menu **Accounts -> G/L Account Maintenance**. Search using the magnifying glass of the G/L account you would like attached to the newly created revenue categories.

Scroll to the field revenue category and choose the newly created revenue category. Store the settings by clicking the “save” button.

<figure><img src="../../../.gitbook/assets/image (1518).png" alt=""><figcaption></figcaption></figure>

Back in A/R Module, run the Client Ranking Report with the option to subtotal by Revenue Category in the top right and the details under the client name will be subtotaled by Revenue Category. Any G/L's that were not linked to a category will display at the bottom of the list with \*\* as the Category ID and Description.

<figure><img src="../../../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>

Note that the results can be exported to excel or pfd. Also, red and yellow symbols indicate a decrease or leveling of amounts respectively from the previous year to current year. The yellow triangle means that the revenue was within 2% of last year. The red diamond means the revenue was less than 2% of last year. The green circle means that the revenue is more than 2% higher than last year.

When subtotaling by Revenue Category, you can also choose to filter on one or more revenue categories

If you have the clients split into specific groups, you can also filter the list for Client Group. To perform this setup, navigate to the menu **Setup -> Client Groups Setup**. Client can belong to more than one client group.

Note that each client can be expanded to view more details using the expansion arrow.

### Client Ranking - 12 Period Report

The 12 Period Ranking report has similar setup requirements as above Client Ranking Report, but the display is a little more detailed with separate columns for each of the 12 periods starting with the desired "Start Period" at the top. Default is 12 months prior to "last month" to be sure to show full periods.

<figure><img src="../../../.gitbook/assets/image (1024).png" alt=""><figcaption></figcaption></figure>

### Client Spending Trend Report: Last 5 Years

This report shows totals by year (Calendar year or Financial Year) for the last 5 years. This can be filtered by Client Group or by one or more Revenue Categories. Additional filters are available at the top of each column if you are searching for a particular account or amount (Perhaps all advertisers with a total spend greater than or equal to $x

<figure><img src="../../../.gitbook/assets/image (696).png" alt=""><figcaption></figcaption></figure>

## Client Budget Reports

#### Prerequisite Setup

Users can view the client budget reports only if they enter budget amounts for the advertisers for the year in question. To do so, navigate to the menu **Customers -> Client Budget Setup**. Choose a client from the drop-down menu as well as a year for which to enter the budgets.

Either use the auto-fill feature to enter budget and/or any or all the 3 forecasts and save, or manually enter the figures. The autofill feature allows you to enter numbers in each cell starting a certain period or spread evenly the total figure among the different period. This can be done for each forecast and budget year.

You can also import the budgets using the node “import budgets”. Use the template provided to fill in the data and then perform the import.

#### Client Budget Summary Report

User can view the budget summary report which reflects the budget compared to the actual advertising revenue amounts. To do so, navigate to the menu **Reporting -> Client Budget Summary Analysis**.

Choose the client group from the drop-down menu to filter by client group (otherwise can be left blank to see all client groups).

{% hint style="info" %}
Create Client Groups under [**Setup -> Client Group Setup**](../setup-a-r-system-setup/other-a-r-setup-menu-items.md#client-group-setup)
{% endhint %}

Choose whether to see the numbers in gross or net values. Also enter the period through which you want to see the actuals. The report will always show the full year of whatever the actuals through period is in. (for example if you select actuals thru 2022-10, the report will show all of 2022, with actuals up until October and then Budget numbers for the remainder of the year)

After the data displays, you can choose from the drop down to view budget or by forecast.

By Default, the data is displayed with actuals for the Current Period and Prior months. For future months, the numbers will be the budget (or forecast) amount.

<figure><img src="../../../.gitbook/assets/image (1025).png" alt=""><figcaption></figcaption></figure>

## List of Transferred Transactions

This provides the user with a list of transactions which were transferred from one client to another over a date range.

## Credit Controller Cash Report

This is also available on the [Credit Control Manager's](../credit-control/credit-controller-cash-report.md) navigation icons.

## Payment Processing Fees <a href="#_toc11740794" id="_toc11740794"></a>

Introduced with the 2023.4 version of Naviga Ad, charging a processing fee (sometimes called cash discount) requires an add on license to use. If your site uses this function a report is available to track the fees that have been collected for payment processing

<figure><img src="../../../.gitbook/assets/image (1750).png" alt=""><figcaption></figcaption></figure>

The top portion of the report shows a graph of the fees collected in the last 13 months

For detailed transactions, select desired date range and click select data and the report will display with the columns selected in Configure output tab.

## Revenue by Class Reports <a href="#_toc11740794" id="_toc11740794"></a>

Two Reports for Revenue by Class Code by financial period range, as well as the same report by year to date are available providing revenue by the class code, class description, client name, YTD revenue, YTD profit and totals.

Navigate to the menu **Reporting -> Revenue by Class Report**. Enter the financial period for which the report displays the class code revenue for 12 periods starting your selection.

<figure><img src="../../../.gitbook/assets/image (352).png" alt=""><figcaption></figcaption></figure>

The columns display the Class Type ID, Name, Class ID, Name, Client Name and ID, Revenue in each period. You can also choose the numbers displayed to reflect the Profit or Profit percentage instead and click “Run Report”.

Navigate to the menu **Reporting -> Revenue by Class YTD Report**. The data is similar to the report above except that this data is for a particular period and YTD data in comparison to the period’s data.

<figure><img src="../../../.gitbook/assets/image (165).png" alt=""><figcaption></figcaption></figure>

## Deferred A/R Report

In the A/R Module, navigate to Reporting > Deferred A/R Report

This reports shows, for a given financial period, the orders (and Exhibitions if using the Exhibition module) that have had deferred activity in that period, or that has a deferred revenue balance in that period. The numbers are shown in both the billing currency and in the local currency (the system default currency).

<figure><img src="../../../.gitbook/assets/image (920).png" alt=""><figcaption></figcaption></figure>

## Informer Dashboards

In the A/R Module, navigate to **Reporting -> Informer Dashboards**. In the Advertising Module, navigate to **Analysis -> Informer Dashboards.**

This report is only usable by Naviga clients who have purchased a license to Informer Reports.

What is displayed under the selected widget dropdown is configurable by user

<figure><img src="../../../.gitbook/assets/image (771).png" alt=""><figcaption></figcaption></figure>

Within Informer reports, on any report a user can select "Action" and "Generate external link." External links allow you to share reports with someone who does not have a login to Informer.

From the Configuration tab, create as many Name and External link URL's as you would like, and click save:

<figure><img src="../../../.gitbook/assets/image (898).png" alt=""><figcaption></figcaption></figure>

These reports will now be available to you on the Widget tab. This allows the user to see Informer Reports as well and drill down on the data, export them, change columns and filters, etc, all without having to leave the Naviga Ad application.
