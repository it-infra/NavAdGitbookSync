# Financial Statement Reports

## Financial Statement Report <a href="#_toc415150395" id="_toc415150395"></a>

User can view the financial statement report based on the setup previously performed ([instructions below](./#financial-statement-report-setup)), by navigating to the menu Financial Reports -> Financial Statement Report. There are two types of reports available: P\&L Reports and Balance Sheet Reports. The data displayed will differ depending upon the type of report that it is.

User can change the period and view when the report was last calculated and by whom.

User can select to show/hide decimals and/or Zero lines.

User can choose to email the report as a pdf to one or more email addresses.

If the financial period calculations have not yet been performed, the Report Period will not be displayed and selectable. User can navigate to the menu Financial Reports -> [Calculate Financial Statements Reports](./#\_toc121381308) and choose the period desired. Click the calculate button. Only periods set to publish will display on the Financial Statement Report screen.

### P\&L Report

A P\&L Report type of report has these tabs:

* P\&L Report
* 12 Period Report
* Trailing Quarterly Report
* Custom Reports

The P\&L Report will look something like this:

<figure><img src="../../../../.gitbook/assets/image (1482).png" alt=""><figcaption></figcaption></figure>

The columns are defined by the system, but the rows will be defined in your Financial Statement Report Setup.

The 12 Period report will look like this:

<figure><img src="../../../../.gitbook/assets/image (1400).png" alt=""><figcaption></figcaption></figure>

Again, the columns are hard coded in the system, but you can customize the grouping on the rows however you would like. In this report, the number will display actuals for any past periods and budgets for the future periods. The dropdown report type in the top right allows you to change that behavior and select forecasts instead, or all budgets, or all actuals.

![](<../../../../.gitbook/assets/image (637).png>)

Selecting Actuals only for example will show 0's for the future periods:

<figure><img src="../../../../.gitbook/assets/image (1542).png" alt=""><figcaption></figcaption></figure>

User then chooses the report from the menu and note the calculations are listed according to the report design and setup. To see anything on the "Custom Reports" tab, as a prerequisite, user must design the financial statement report template. To do so, please refer to “[Financial Statement Templates](financial-statement-templates.md)."

<figure><img src="../../../../.gitbook/assets/image (643).png" alt=""><figcaption></figcaption></figure>

The Trailing Quarterly Report will show the Current Quarter (Actuals and Budget) on the left most column, and then the three prior quarters to the right.

<figure><img src="../../../../.gitbook/assets/image (1282).png" alt=""><figcaption></figcaption></figure>

Custom Reports will only display data if a Financial Statement Template has been configured.

On all the report bodies, hyperlinks for the details and/or figures per line are provided for further drill downs. Click one of the figures for drill down purpose. A new pop up screen displays with the data.

<figure><img src="../../../../.gitbook/assets/image (1579).png" alt=""><figcaption></figcaption></figure>

Further drill down of the G/L Accounts is also available if user clicks it.

Click on the View Full Page Report to view all Positive and Negative values together on one screen.

<figure><img src="../../../../.gitbook/assets/image (545).png" alt=""><figcaption></figcaption></figure>

### Balance Sheet Report

The balance sheet report has just one tab (the balance sheet), plus any custom reports you wish to create using the Financial Statement Templates.

The data displays for the Balance Sheet Report as follows:

<figure><img src="../../../../.gitbook/assets/image (1166).png" alt=""><figcaption></figcaption></figure>

The rows are designed by the user in the Financial Statement Report Setup. The Columns are system defined and will show the Opening Balance for the year, closing balance of the period, and the change between the two numbers.

Click on any detail row and a popup window will display the details and G/L codes that make up that item.

<figure><img src="../../../../.gitbook/assets/image (988).png" alt=""><figcaption></figcaption></figure>

## Calculate Financial Statement Reports <a href="#_toc121381308" id="_toc121381308"></a>

This allows the user to calculate the numbers for a certain period. Navigate to the menu Financial Statement Report -> Calculate Financial Statement Reports, enter the financial period and then click calculate button. A message indicating the calculation is complete.

![](<../../../../.gitbook/assets/0 (38).png>)

If user unchecks the box to publish Y/N and clicks save publish settings, the user who is viewing the financial reports will not be able to see the financial period blocked here in the financial reports statements screen.

If user checks the box to publish the newly calculated report, the user who is viewing the reports will be able to view this financial period and run the reports.

## Financial Statement Report Setup

Two types of Financial Statement reports can be setup: P\&L Reports and Balance Sheet Reports. To get started, select Financial Reports -> Financial Statement Report Setup.

### Report Details Header

<figure><img src="../../../../.gitbook/assets/image (629).png" alt=""><figcaption></figcaption></figure>

In the **Report No** field, select the + to create a new financial statement report. Enter in the desired Report ID

Enter a **Report Description** and select one or more allowed users. The **allowed users** selection here will affect what reports this person can access on the Financial Reports -> Financial Statement Reports screen.

If needed, enter the **Calculation Sequence** (used if one report builds upon another) - can leave as zero if not needed for your report.

**Default Report Tab** - this will open the report on the desired tab.

**Default Custom Template** - See Financial Statement Templates - If you have multiple custom templates created, this will set the default template to use when opening the report. This can always be changed to a different template by the user.

**Custom Percent Calculation** - This function is used when viewing a Custom Report / Template that contains a Percentage column. By default, the percentage calculation is based on the first line that a line totals into. For example, if a revenue line "Subscription Revenue" totals into a "Total Revenue" line then the calculated amount will be Subscription Revenue expressed as a percentage of the Total Revenue. This feature allows you to override the default behavior by instead basing the percentage calculation on a specific line on a report - defined here.

**Inactive** - Set inactive flag to yes if you no longer plan to use a financial report.

**Show Decimals** - If set to yes, the statement will show decimals. If set to no, the numbers will be rounded up or down to the nearest whole number. This will set the default behavior and the user can change it as needed when viewing the financial report.

**Suppress Zero Lines** - if a row on the report has all zeros, the line will be suppressed if this is set to Yes, otherwise zero lines will be displayed. This will set the default behavior and the user can change it as needed when viewing the financial report.

### Report Details Body

In the body of the report, you can customize the lines (rows) based on desired look and feel of the report. The columns are fixed based on the type of report. If you wish to customize the columns, use the Financial Statement Templates and create a custom report.

At the bottom of the setup screen is a dropdown to select the type of line you with to add:

![](<../../../../.gitbook/assets/image (1144).png>)

Following is a sample report -

<figure><img src="../../../../.gitbook/assets/image (757).png" alt=""><figcaption></figcaption></figure>

* Heading lines: Rows 1 and 11 in the above example are Heading lines
* Detail Lines: Rows 2 - 8 and Rows 12 - 19 are Detail lines
* Total Lines: Tows 9, 20, & 22 are Total Lines
* Math Line: None used in this report, but a math line will add, subtract, multiply, divide or divide as a %, two or more lines.
* Spacer Line: Row 10 & 21 are spacer lines
* PDF Page Break line: None shown in this example, but the purpose of this type of line is to force a page break at a certain position when printing the Financial Statement to PDF format.

Add rows one at a time until all necessary rows are added to the report.

#### Heading Line

<figure><img src="../../../../.gitbook/assets/image (986).png" alt=""><figcaption></figcaption></figure>

When adding/editing a Heading line, the above options are available.

*   **Line ID** - by default this is a sequential numeric ID, but can be overwritten if desired. When hovering over the name, the ID will be displayed.\\

    <figure><img src="../../../../.gitbook/assets/image (1486).png" alt=""><figcaption></figcaption></figure>
* **Description** - This will be the label displayed on screen
* **Internal Comment** - This will be displayed if the user clicks on the description when viewing the report.

<figure><img src="../../../../.gitbook/assets/image (1203).png" alt=""><figcaption></figcaption></figure>

* **Line Style** - The following options are available: none, Single Overline, Single Underline, Single Over/Underline, Double Overline, Double Underline, Double Over/Underline.
* **Bold** - Set to Yes if you would like this line to be displayed in bold font
* **Print Line** - Set to Yes if you would like this line to be displayed when printing / emailing this report or when downloading to Excel.
* **Line Position** - Enter the numerical sort order for where this line belongs on the report.

#### Detail Line

The detail lines will make up the bulk of the report

<figure><img src="../../../../.gitbook/assets/image (543).png" alt=""><figcaption></figcaption></figure>

When adding/editing a Detail line, these options are available:

* **Line ID** - by default this is a sequential numeric ID, but can be overwritten if desired. When hovering over the name, the ID will be displayed.
* **Description** - This will be the label displayed on screen
* **Debit or Credit** - Select from the dropdown if this is expected to be a debit balance or a credit balance.
* **Internal Comment** - This will be displayed if the user clicks on the description when viewing the report.
* **Line Style** - The following options are available: none, Single Overline, Single Underline, Single Over/Underline, Double Overline, Double Underline, Double Over/Underline.
* **Bold** - Set to Yes if you would like this line to be displayed in bold font
* **Print Line** - Set to Yes if you would like this line to be displayed when printing / emailing this report or when downloading to Excel.
* **Statistical Line** - Statistical lines are used to enter numbers that are not tracked in the system e.g. "No. of Employees". These lines are excluded from percentage column calculations and rounding.
* **Line Position** - Enter the numerical sort order for where this line belongs on the report.
* G/L Account Selection Criterial - The G/L's included here will be what gets utilized in the calculation of this line.
  * To select a specific Account, enter the "(From) G/L Account" and leave the "To G/L Account" blank
  * To select a range of Accounts, enter both a "(From) G/L Account" and "To G/L Account". Range selection do not have to be existing Accounts, but must be a valid Account format
  * To enter a wildcard selection, use the ^ character, e.g. 01\*0000\*^ or 01\*0000\*^00^\*1000 or 01\*0000\*^\*1000

**Selected G/L Accounts tab -** read only summary of G/L Accounts that will sum to this Detail Line, based on the G/L Account Selection Criteria entered on the first tab.

<figure><img src="../../../../.gitbook/assets/image (244).png" alt=""><figcaption></figcaption></figure>

**Add to Lines -** This read-only listing shows any other lines on this report, or other reports, that use this line as part of a Total or Math line.

<figure><img src="../../../../.gitbook/assets/image (1163).png" alt=""><figcaption></figcaption></figure>

#### Total Line

The total line will sum two or more detail lines, math lines or other total lines

<figure><img src="../../../../.gitbook/assets/image (558).png" alt=""><figcaption></figcaption></figure>

When adding/editing a Total line, these options are available:

* **Line ID** - by default this is a sequential numeric ID, but can be overwritten if desired. When hovering over the name, the ID will be displayed.
* **Description** - This will be the label displayed on screen
* **Debit or Credit** - Select from the dropdown if this is expected to be a debit balance or a credit balance.
* **Internal Comment** - This will be displayed if the user clicks on the description when viewing the report.
* **Line Style** - The following options are available: none, Single Overline, Single Underline, Single Over/Underline, Double Overline, Double Underline, Double Over/Underline.
* **Bold** - Set to Yes if you would like this line to be displayed in bold font
* **Print Line** - Set to Yes if you would like this line to be displayed when printing / emailing this report or when downloading to Excel.
* **Statistical Line** - Statistical lines are used to enter numbers that are not tracked in the system e.g. "No. of Employees". These lines are excluded from percentage column calculations and rounding.
* **Line Position** - Enter the numerical sort order for where this line belongs on the report.
* **Total Derived From Lines** - select the lines that will be used to create the total of this line. Note - these lines can be taken from this report or other reports. If amounts are taken from other reports, this is where you will utilize the Calculation Sequence in the report header. Ensure that the report this one depends upon is calculated before this report.
* **Add to Lines -** This read-only listing shows any other lines on this report, or other reports, that use this line as part of a Total or Math line.

<figure><img src="../../../../.gitbook/assets/image (1197).png" alt=""><figcaption></figcaption></figure>

#### Math Lines

<figure><img src="../../../../.gitbook/assets/image (1140).png" alt=""><figcaption></figcaption></figure>

When adding/editing a Math line, these options are available:

* **Line ID** - by default this is a sequential numeric ID, but can be overwritten if desired. When hovering over the name, the ID will be displayed.
* **Description** - This will be the label displayed on screen
* **Debit or Credit** - Select from the dropdown if this is expected to be a debit balance or a credit balance.
* **Internal Comment** - This will be displayed if the user clicks on the description when viewing the report.
* **Line Style** - The following options are available: none, Single Overline, Single Underline, Single Over/Underline, Double Overline, Double Underline, Double Over/Underline.
* **Display as a Percent** - Select yes if this number is to be displayed as a percent as opposed to a decimal number.
* **Bold** - Set to Yes if you would like this line to be displayed in bold font
* **Print Line** - Set to Yes if you would like this line to be displayed when printing / emailing this report or when downloading to Excel.
* **Statistical Line** - Statistical lines are used to enter numbers that are not tracked in the system e.g. "No. of Employees". These lines are excluded from percentage column calculations and rounding.
* **Line Position** - Enter the numerical sort order for where this line belongs on the report.
* In the bottom section add the lines from this report or other reports which will be used in the calculation in this line.
* **Selected G/L Accounts -** This read-only listing shows the G/L Accounts that will calculate to this Math Line, based on the G/L Account Selection Criteria entered on the first tab.
* **Add to Lines -** This read-only listing shows any other lines on this report, or other reports, that use this line as part of a Total or Math line.

#### PDF Page Break or Spacer lines

When adding spacers or page breaks, all that is needed is to enter the position where the break/spacer will be added. click Insert when finished.

![](<../../../../.gitbook/assets/image (636).png>)

#### Notes/Comments

Right click on any cell to enter a comment on that cell that the user will then see when reading the report.

<figure><img src="../../../../.gitbook/assets/image (1030).png" alt=""><figcaption></figcaption></figure>

Any notes entered here will be displayed with a yellow highlight when viewing the report on screen

<figure><img src="../../../../.gitbook/assets/image (1573).png" alt=""><figcaption></figcaption></figure>

If you have added notes on one or more reports, you can clear them individually by right clicking and deleting the note and resaving, or you can delete in bulk with the dropdown in the top right. Can delete one report at a time or delete the notes across all the reports

<figure><img src="../../../../.gitbook/assets/image (1289).png" alt=""><figcaption></figcaption></figure>

#### Validate Lines

The validate lines button to the right of the notes dropdown will check over the lines and give the user a heads up if there are any of the following issues present:

* One of the Totals lines (or Math lines) is referencing a totals line which has not yet been calculated at this point in the report
* A Totals line (or Math line) is referencing another line in the report that no longer exists
* A Totals line (or Math line) references a line from an external report that is set to calculate after this report. This will cause the value for this line to be calculated incorrectly. (Revisit the Calculation Sequence in the [Report Header](./#report-details-header) if necessary to re-order the calculation sequence.)

## List of Financial Reports <a href="#_toc121381318" id="_toc121381318"></a>

Navigate to Financial reports -> List Financial Reports to generate a list of financial reports created in the system. User has the option to export the list to excel or PDF.

Filters are available at the top of each column to filter the data.

<figure><img src="../../../../.gitbook/assets/image (1307).png" alt=""><figcaption></figcaption></figure>
