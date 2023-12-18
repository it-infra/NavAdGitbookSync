# Trial Balance & Other Reports

## G/L Project P\&L Report <a href="#_toc417565509" id="_toc417565509"></a>

Prerequisite: Before creating a G/L Project P\&L, you must set up one or more G/L Products (see Setup -> G/L Project Setup, and you must link a G/L Project to transactions.

Navigate to Financial Reports -> G/L Project Financial Report

Select G/L Product from the Project Dropdown

Select Financial Statement Report from Report ID Dropdown

Select Report Period from Report Period dropdown (prerequisite: [Calculate and Publish Financial Period](financial-statement-reports/#\_toc121381308))

Report will display, showing transactions tagged with the G/L Project

<figure><img src="../../../.gitbook/assets/image (1612).png" alt=""><figcaption></figcaption></figure>

## Trial Balance Report <a href="#_toc417565509" id="_toc417565509"></a>

Navigate to Financial Reports -> Trial Balance Report

Select desired parameters.

* One of either Company, G/L Code Group or G/L Account are required.
* Select desired Start/End Period range
* Choose yes/no to suppress zero value lines
* Choose yes/no to include detail.

Without Details selected, trial balance summary is displayed

<figure><img src="../../../.gitbook/assets/image (1293).png" alt=""><figcaption></figcaption></figure>

With Details selected, a > sign is displayed in the left column where user can expand to see transactions, and a transaction tab is displayed:

<figure><img src="../../../.gitbook/assets/image (1295).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (500).png" alt=""><figcaption></figcaption></figure>

When user clicks the button download details to excel, many fields not on the screen display will be included with the download. The fields are as follows: G/L ID, G/L Name, Posted Date, Period, Source, Transaction ID, Debit Amount, Credit Amount, Client ID, Client Name, Product ID, Product Name, Comment, Project ID, Project Name, Employee ID, and Employee Name, and many more.

![](<../../../.gitbook/assets/6 (16).png>)

Some of these details are also included one the tab “Transactions”.

![](<../../../.gitbook/assets/7 (16).png>)

This trial balance report, either in summary or detailed format, often form the basis for what gets imported into a 3rd party G/L System. (Alternatively, can use the API to extract G/L details)

## G/L Transactions Report <a href="#_toc121381322" id="_toc121381322"></a>

This is a list of debit/ credit transaction report by financial period and level parameters which user chooses to narrow down the report as applicable.

<figure><img src="../../../.gitbook/assets/image (1026).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1305).png" alt=""><figcaption></figcaption></figure>

## Prepaid Expenses Report <a href="#_toc121381323" id="_toc121381323"></a>

This provides a list of transactions logged against the prepaid expenses GL account for a company by vendor for a period.

<figure><img src="../../../.gitbook/assets/image (676).png" alt=""><figcaption></figcaption></figure>
