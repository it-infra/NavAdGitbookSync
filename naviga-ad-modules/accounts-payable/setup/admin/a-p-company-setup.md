# A/P Company Setup

In A/P Company Setup screen has various settings which can be unique per system company. Select desired company at the top of the screen. See [Company Setup](../../../general-ledger/setup/admin/company-setup.md) in G/L Setup for details on setting up Companies in the system

<figure><img src="../../../../.gitbook/assets/image (526).png" alt=""><figcaption></figcaption></figure>

## General Settings

In the A/P module, it is possible to close periods by company rather than for the entire system. In A/R and in G/L periods are set for all companies.

**First Open Period** - enter the desired starting open period here.

**Last Open Period** - Enter the desired ending open period here. This may be the same as the first open period if only one period is open. At the beginning of the month, it may be desirable to open the current month before you are ready to close the prior month.

## Defaults

**Default Bank** - Bank selected here will set the default bank for the company when creating a new invoice batch in A/P Invoice Entry or in A/P Batch Entry

**Auto Schedule Credits** - Setting this option will automatically schedule Vendor Credits for Payment. If not set then you will need to schedule the Credits manually.

**Auto Schedule Invoices** - Setting this option to "Yes" will automatically schedule Vendor Invoices for Payment based on their due date. If not set then you will need to schedule the Payments manually on the Payments -> Pay A/P Invoices screen.

**Withhold Taxes** - Check this prompt ONLY if using withholding taxes and/or withholding from foreign vendors.

**Derive G/L Accounts from A/P Setup** - Typically this will be UNCHECKED.\
When entering all payables into each company and indicating they are to be paid from company 01s bank account, if this prompt is UNCHECKED the system will take the Accounts Payable general ledger from the Bank record, this means that intercompany transactions will be created as soon as the invoice is posted.\
\
If this prompt is CHECKED the due to/from will not be populated until after the invoices are paid (unless there are multiple companies on the expense side). By checking this prompt the general ledger account will come from the Accounts Payable Header for that company and the system will only create the due to/from at the time of payment when the Bank general ledger and the Accounts Payable general ledger differ. The user will get a warning when they select a different Bank code than the company's bank, this is okay, enter through that message.\
\
This means that for A/P Invoices, if the Expected Bank Payable is different than the A/P Company Payable, then it will use the Bank Payable as the first G/L Line and include other G/L Lines on the Invoice to reclass it to the A/P Company Payable (and Multi-Co Balancing as well if ON). Typically, an Invoice has just the one Accounts Payable G/L Line which corresponds to the CHECKED option. Then the Multi-Co balancing will happen on the A/P Payment transaction (still assuming there is a Company difference).

<figure><img src="../../../../.gitbook/assets/image (333).png" alt=""><figcaption></figcaption></figure>

## G/L Allocations

A/P G/L Account - Enter the G/L Code to be used when entering A/P invoices for this company

Tax G/L Account - Enter the Tax G/L account to be used when entering A/P Invoices for this company

Tax G/L Account 2 - If Applicable, Enter an additional Tax G/L account to be used when entering A/P Invoices for this company

## IRS 1099 Minimum Reporting Amounts

The above settings allow you to control, by company, what minimum amounts are required before a 1099 will need to be created for various kinds of 1099 vendors. These minimums may change over time, so the system allows for configurable settings by company.

Irish 46G reporting amount is also included in this section

<figure><img src="../../../../.gitbook/assets/image (1327).png" alt=""><figcaption></figcaption></figure>

## Automatic Inter-Company G/L Allocations

If the G/L system Setup [Multi-Company Balancing](../../../general-ledger/setup/admin/g-l-system-setup/multi-company-balancing-and-intercompany-control-accounts.md) setting is set to allow lines for more than one company, but each company's lines must balance, then this section needs to be filled in so that the system can create balancing adjustments for these invoices.

<figure><img src="../../../../.gitbook/assets/image (1480).png" alt=""><figcaption></figcaption></figure>

## Purchase Order Settings

See also Purchase Order Settings on [A/P System Setup](a-p-system-setup.md#purchase-order-forms-using-naviga-forms). What is set here on the Company will override what is set for the system.
