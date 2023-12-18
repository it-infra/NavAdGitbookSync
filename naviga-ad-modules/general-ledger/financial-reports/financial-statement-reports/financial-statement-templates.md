# Financial Statement Templates

This document explains how users can design a custom template to produce a financial statement report.

User may create custom sets of columns to be used with the rows of data in Financial Statement Reports. See [Financial Statement Reports](./#financial-statement-report-setup) for details on setting up the rows of data. Once a Template is designed, it may be used for any Report. A saved Template may be set as the default for a Report or may be selected during viewing to see a different set of columns than the default Report.

Columns selected here from top to bottom will print on the report from left to right. New columns are added to a template by selecting the column ID and then clicking the plus-icon “Add” button. Other than the Description, columns are removed from a template using the red-X “Delete” button. The sequence may be changed using click-and-drag, moving the selected column to a new position in the list.

There are three types of columns available for use in a Template:

1. Pre-defined columns – Financial Period-based data
2. Math Calculation columns – using data from other columns in the same row
3. Percent of Total columns – displaying a % based on the Total row of a reference column

### Pre-defined Columns <a href="#_toc24524620" id="_toc24524620"></a>

The pre-defined columns will have a Column ID, a default Description (Line 1 and Line 2), a Category, and a Type. Line 2 of the Description can always be edited by user, but Line 1 will be overwritten by a system definition in the cases noted below. The Type will indicate whether the data comes from posted Actuals, Budgets, Forecast 1, or Forecast 2 of the source GL Codes, or “Calculated” for conditional data.

* The first Category of pre-defined columns is Annual data. There are 19 different columns available...

<div data-full-width="true">

<figure><img src="../../../../.gitbook/assets/image (985).png" alt=""><figcaption></figcaption></figure>

</div>

Columns that refer to “Last Year” (43, 44, 144; 31, 39, 40, 140), “This Year” (41, 42, 142; 27, 28, 128), or “Next Year” (33, 34, 134) in Description Line 1 will always display the system definition of that year and will not recognize an Override Description for Line 1.

The “Predicted Total” columns will calculate an annual amount using Actuals up to the current month and then either Budgets, Forecast 1, or Forecast 2 for the remaining months of the year.

* The next Category of pre-defined columns is Balance Sheet data. There are 3 different columns available.

![](<../../../../.gitbook/assets/2 (35).png>)

The Description Line 1 for these items do not use a system definition.

*   The next Category of pre-defined columns is Current Period data. There are 11 different columns available.\\

    <figure><img src="../../../../.gitbook/assets/image (510).png" alt=""><figcaption></figcaption></figure>

Columns that refer to “Last Year” (5, 13, 21, 121) or “Period” (1, 9, 17, 117) in Description Line 1 will always display the system definition of that Period and will not recognize an Override Description for Line 1.

*   The next Category of pre-defined columns is Previous Period data. There are 11 different columns available.\\

    <figure><img src="../../../../.gitbook/assets/image (1283).png" alt=""><figcaption></figcaption></figure>

The Description Line 1 for these items do not use a system definition.

*   The next Category of pre-defined columns is Quarter-To-Date data. There are 11 different columns available.\\

    <figure><img src="../../../../.gitbook/assets/image (1141).png" alt=""><figcaption></figcaption></figure>

The Description Line 1 for these items do not use a system definition.

*   The last Category of pre-defined columns is Year-To-Date data. There are 11 different columns available.\\

    <figure><img src="../../../../.gitbook/assets/image (1143).png" alt=""><figcaption></figcaption></figure>

Columns that refer to “Last Year” (8, 16, 24, 124) or “This Year” (4, 12, 20, 120) in Description Line 1 will always display the system definition of that year and will not recognize an Override Description.

### Math Calculation Columns <a href="#_toc24524621" id="_toc24524621"></a>

Math Calculation columns will display the results of the calculation defined in the column setup. User must manually enter the Description Line 1 and Description Line 2 for display as the Column title. Optionally, user may override the Column Position here instead of adding the Math Calculation to the end of the list and then moving it to the desired position using click-and-drag.

![](<../../../../.gitbook/assets/7 (14).png>)

Basic math functions may be applied to the pre-defined Column IDs, or to Constants. After selecting the Math Function and a Column ID (or Constant), clicking the plus-icon “Add” button will insert that as one of the terms of the calculation.

For example, to display the change from Last Period to This Period, user would add(+) Column 1, Period Actual, and subtract(-) Column 2, Previous Period Actual.

<figure><img src="../../../../.gitbook/assets/image (350).png" alt=""><figcaption></figcaption></figure>

### Percent of Total Columns <a href="#_toc24524622" id="_toc24524622"></a>

A Percent column will display percentages for each Report row based on the values of another column. User must manually enter the Description Line 1 and Description Line 2 for display as the Column title.

![](<../../../../.gitbook/assets/8 (39).png>)

By default, the percentage calculation is based on the first row which a row totals into. For example, if a revenue line "Subscription Revenue" totals into a "Total Revenue" line then the calculated amount will be Subscription Revenue expressed as a percentage of the Total Revenue.

This default behavior can be overridden to instead calculate the percentage based on a specific line by setting the “Use Custom Calculation” option to YES. The "Custom Percent Calculation" setup is defined on the Financial Report Setup screen.
