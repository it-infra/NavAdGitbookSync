# Campaign Reports

This section discusses this reports, which are accessible under the Campaigns menu in the Advertising Module

<table data-column-title-hidden data-view="cards"><thead><tr><th></th></tr></thead><tbody><tr><td><a href="campaign-reports.md#orders-by-product">Orders by Product</a></td></tr><tr><td><a href="campaign-reports.md#orders-by-entry-date">Orders by Entry Date</a></td></tr><tr><td><a href="campaign-reports.md#campaign-budget-analysis">Campaign Budget Analysis</a></td></tr><tr><td><a href="campaign-reports.md#campaign-delivery-pacing">Campaign Delivery / Pacing</a></td></tr><tr><td><a href="campaign-reports.md#campaigns-from-the-portal">Campaigns from the Portal</a></td></tr><tr><td><a href="campaign-reports.md#accepted-proposals">Accepted Proposals</a></td></tr><tr><td><a href="campaign-reports.md#confirmed-contracts">Confirmed Contracts</a></td></tr><tr><td><a href="campaign-reports.md#campaign-changes">Campaign Changes</a></td></tr></tbody></table>

## Orders by Product

The orders by product report allows for selection of orders in a group of products or selected product(s) in a selected date range. It can optionally be filtered or highlighted using other order criteria.

![](<../../../.gitbook/assets/0 (51).png>)

The report allows users to determine what fields to display in the results. The configure output tab allows selection of what fields to display when the report is run to screen, and what fields to display when the report is exported to Excel. Fields can be selected one by one or by highlighting multiple lines, the single arrow tool moves highlighted fields on or off the report, the double arrows move all fields. Once the configuration is saved the user will see their selected columns in the report output.

![](<../../../.gitbook/assets/1 (62).png>)

If multiple configurations are needed, or if configurations are to be distributed to other users one may choose to create configuration templates to save the query and output selections.

![](<../../../.gitbook/assets/2 (64).png>)

Clicking on “new” in the report template area allows one to name a template and to select who can view/use the template, who can edit the template, and who can delete the template. For example, I may create a template often used by all users, I would allow permissions for any system user. But I may restrict the ability to edit or delete to myself.

![](<../../../.gitbook/assets/3 (19).png>)

Each template and each permission type can be assigned either to all system users, template creator only or everyone in your security group. Save the report.

Then you can run the report to see the data. You can create multiple reports in this manner and save them.

Also, once you run the report, you can choose more filter criteria from the screen. For example, the size and then click highlight matches. Once the data is highlighted on the screen, you can then click Edit in the Report Template section. The system prompts you if you’d like to save these changes to the report.

Click the tab “Link”. This provides you with a URL to this report which you can send or embed elsewhere. Click Copy and this copies the link to the clipboard.

You can change the screen configuration fields and create as many report templates as you need in the same way.

When running the report, the users can select any of the templates for which they have permission and the system will adjust the output to match the selected template.

{% hint style="info" %}
The Campaign External ID on the report reflects the campaign external ID field on the campaign header, while the Line External ID reflects the GAM external ID if the line is connected to GAM.
{% endhint %}

### Page Equivalency (Page Eq.) Calculation

The Page Equivalency field for print orders is calculated as follows:

1. If there is a Line Equivalency on the Ratecard Line and a Lines Per Page on the Product, then the Page Equivalency = Ratecard Line Equivalency / Product Lines.
2. Otherwise if there are values on the Ad Size for Height and Width, then Page Equivalency = (H x W)/ Page Area setting on product setup.

There are several reports in this section which show the size of each print advertisement and provide a total number of advertising pages such as Orders by Product report and similar reports.

Print orders can be entered using modular sizes, column x height sizes or by entering the text of the ad. Because of the variety of ways in which ads are sized, the system performs different calculations on each type of order to total size.

How the system determines the size of an ad:

1. For modular ads the system determines the dimensions using the size code table. The size code is most often stored on the Ratecard, in some cases one may select a size code during campaign entry. If you are seeing inaccurate information for modular ads, check the dimensions on the size table, and the dimensions set up on the product. The unit of measure on the size code is used to convert the width to points for the page total.
2. For Cost Per Column ads where the user enters the number of columns and inches or centimeters or millimeters or agates, the width is determined from the column layout. The system checks the number of columns order line, checks the column layout from the product (possibly overwritten by section or classified category) and matches the number of columns on the order to the column layout. The system checks the number of units (inches, centimeters, millimeters or agates) to calculate the height of the ad. If you are seeing inaccurate information for these ads check the column layout for the product or section or classified category. The system converts the column with points for the page total.
3. If this is a listing type ad (determined by the listing checkbox on the ad type). The system measures the material that was created/entered via the listing entry screen for the height. The width is calculated in the same way and validated against the column setup for that classified category. Verify that the column setup is accurate and that the dimensions on the ad are correct. The system again converts the width to points before calculating the total.

## Orders by Entry Date

This report can be run by product or by product group for a date range of when user entered campaigns into the system. The data displayed will show the entry date for the order, the product name, the campaign ID, the line item ID and all the campaign details such as the ad type and size and various amounts.

<figure><img src="../../../.gitbook/assets/image (1093).png" alt=""><figcaption></figcaption></figure>

Click on the Configure Output tab to select the fields you would like to see displayed on the display grid and/or in the Excel Output when downloading the results

<figure><img src="../../../.gitbook/assets/image (978).png" alt=""><figcaption></figcaption></figure>

## Campaign Budget Analysis

Campaign Budget Analysis Report is a screen which provides graphical and numerical analysis of the revenue vs. expense report for campaigns. Click the tile “Campaign Budget Analysis” or navigate to Campaigns -> Campaign Budget Analysis and run the query by any of the available criteria. For example, the date range during which the campaign is running, the order status, the sales rep or the product group.

<figure><img src="../../../.gitbook/assets/image (1147).png" alt=""><figcaption></figcaption></figure>

The results provide a summary of the Actuals versus the Budgets. You can also limit the criteria to campaigns in which you entered a campaign budget other than the campaign order amounts, using the campaign budget node.

You can also view the B/W information for actual vs. budget revenue and expense. This is the Better/Worse than budgeted by amount and percentage. . In Revenue, Actual > Budget = Better; in Expenses Actual < Budget = Better. This is used vs. showing the strict variance “Actual less Budget” because negative numbers in expenses imply not good when it is actually good.

## Campaign Delivery/Pacing

This report displays the GAM serving details per campaign.

The criteria are the timeframe of viewing to be full length of the campaigns or only this current month. User can choose to view the impressions served or viewable impressions. User can choose the digital product group to view the group’s pacing details and for which line type, such as CPC, or Flat Fee and so forth.

The data displays the campaign ID, advertiser, brand, line item ID, the digital product name, description of size, line type, start and end dates of the campaign. The data also includes totals estimated, viewable, served, projected, days passed, impressions should have served, and actual performance data and percentages.

<figure><img src="../../../.gitbook/assets/Pacing Report.gif" alt=""><figcaption></figcaption></figure>

## Campaigns from the Portal

This screen provides a list of campaigns which have been created on the Advertiser Portal by product group and date range.

<figure><img src="../../../.gitbook/assets/image (799).png" alt=""><figcaption></figcaption></figure>

## Accepted Proposals

Navigate to the menu Campaigns -> Accepted Proposals to view the proposals which are accepted. Search using the criteria provided and data reflects all campaigns in the status: Reserved, Confirmed, Billed, but **they only include orders that started in Quote status.** The report also reflects Approved (Accepted) Date and not Confirmed date. The orders which status changed from Quote to Reserved have the stamp of the Approved Date. If the order is changed back to Quote status, the Approved date is removed.

There is a filter where you can choose to see all accepted proposals or only the ones that were approved via the Advertiser Portal.

<figure><img src="../../../.gitbook/assets/image (909).png" alt=""><figcaption></figcaption></figure>

The report **Accepted Proposals pending Confirmation** is very similar to above, but it filters out the orders that have already been confirmed

<figure><img src="../../../.gitbook/assets/image (537).png" alt=""><figcaption></figcaption></figure>

## Confirmed Contracts

This report displays campaigns in Confirmed or IS (Billed) status regardless of their origin.

<figure><img src="../../../.gitbook/assets/image (1602).png" alt=""><figcaption></figcaption></figure>

## Campaign Changes

A report in the digital first platform displays changes on campaigns within a date range. These are the same changes which display in the audit trail change history of a campaign all combined in the generation of this report.

Navigate to the menu Campaigns -> Campaign Changes Report. Enter the date range of the campaign and you may choose the optional search on the product group name. You can also choose to include Confirmed, Reserved and/or Quoted orders, in addition to including/excluding Imported Campaigns. Click on “Get Data”.

Note that the data is grouped by Campaign ID. Drag any of the column headings to the group bar next to the “Campaign ID” group and the data is rearranged by this column after the Campaign ID. You can also sort by column when you click the column heading. You can also search on each column by typing partial text of the data you would like to see.

You can also click on the Excel or PDF icons to export the data for further use.

<figure><img src="../../../.gitbook/assets/image (317).png" alt=""><figcaption></figcaption></figure>
