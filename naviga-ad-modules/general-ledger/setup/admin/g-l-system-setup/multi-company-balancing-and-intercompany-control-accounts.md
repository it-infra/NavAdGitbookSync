# Multi Company Balancing and Intercompany Control Accounts

### Setup <a href="#_toc9433267" id="_toc9433267"></a>

The basic setting is at G/L Module -> Setup -> Admin -> G/L System Setup. The section title refers to “A/P Invoice Entry” and “Journal Entry” only, but the Multi-Company Balancing setting also applies to most A/R functions, including some external billing, like from the Ad Module.

<figure><img src="../../../../../.gitbook/assets/image (997).png" alt=""><figcaption></figcaption></figure>

There are three levels of Multi-Company Balancing (from least to most restrictive), and is set with Parameter #6 in the Default Settings section:

1. “Allow lines for more than one Company, **do not require** each Company’s lines to balance”
2. “Allow lines for more than one Company, but each Company’s lines **must balance**”
3. “Require all lines to be for a **single Company**”

Level one could be used in cases where Trial Balance is always run for all Companies, or balancing of GL accounts is not required within Naviga Ad at all. Level three could be used in cases where each Company must be kept separate, such as when following certain commingling rules. The remaining discussion will be about level two.

“Lines” in this context refers to GL Allocation lines and “balance” refers to having Debits equal to Credits. Every transaction is already required to balance overall; Multi-Company Balancing also checks the balancing for GL Codes belonging to each Company separately.

In addition to the basic setting, each of the three core Accounting Modules (G/L, A/R, and A/P) has its own table of Control Accounts to be used when the system is required to automatically adjust a transaction to be balanced. These are located in the G/L System Setup, A/P **Company** Setup, and A/R System Setup screens.

![](<../../../../../.gitbook/assets/2 (9)>)

A complete setup between two Companies requires **two Control Account lines**, for example, “From Company 01” / “To Company 02” and “From Company 02” / “To Company 01.” This is because the Debit/Credit imbalance on a transaction will determine which Company needs the “From” account and the system must be able to look up that Company in the first column of the table.

These G/L Accounts do not need to be specific to each pair, but each Company must have at least one balancing account to use for all pairings. In the above example, Company 01 does not need to have GL Code 01\*0000\*5002 for its Company 02 pair and GL Code 01\*0000\*5003 for its Company 03 pair. There could instead be one GL Code 01\*0000\*5000 that applies to all pairings with other Companies.

### Usage – G/L Module <a href="#_toc9433268" id="_toc9433268"></a>

In the G/L Module, when using \<Enter/Edit Journal Entries>, if the G/L Allocation Lines are not balanced for each Company separately, then upon \<Save>, a warning message will pop-up, informing user that the system will be creating Inter-Company GL Lines to meet the balancing requirement.

![](<../../../../../.gitbook/assets/3 (9)>)

System-generated Journal Entries, such as from Ad Deferrals or SC Entries (change to A/R Payment Allocations), will also follow the balancing rules whenever GL Codes from two or more different Companies are on one transaction.

{% hint style="warning" %}
WARNING: If Multi-Company Balancing is set as “required” (level two), but the appropriate pair of G/L Control Accounts are missing, then the system **will** create the transaction **without** those balancing entries. This may result in at least two Companies being out-of-balance in that time frame. Such a setup allows for using the balancing control only between two specific Companies, while others effectively default to level one (unrestricted).
{% endhint %}

### Usage – A/P Module <a href="#_toc9433269" id="_toc9433269"></a>

In the A/P Module, when using \<Post Batches>, if the G/L Allocation Lines (expenses) are not already balanced for each Company separately, including the Accounts Payable GL Code used, then the system will automatically create Inter-Company GL Lines to meet the balancing requirement.

![](<../../../../../.gitbook/assets/4 (7)>)

Note that unlike Journal Entries, there is no warning message during \<A/P Invoice **Entry**> that balancing lines will be used. Instead, the Multi-Company Balancing check is performed during posting to A/P – this is when the Accounts Payable GL Code is finally determined. Also different, the A/P Module will not post/create an Invoice if the A/P Control Accounts are required, but missing from the setup table.

![](<../../../../../.gitbook/assets/5 (1)>)

Also in the A/P Module, when using \<Generate **Checks**>, if the Cash Account of the Bank uses a different Company than the Accounts Payable GL Code, then the system will automatically create Inter-Company GL Lines to meet the balancing requirement.

However, if the required A/P Control Accounts are missing, then the system **will** create the Payment transaction **without** those balancing entries. As with Journal Entries, this may result in at least two Companies being out-of-balance in that time frame.

### Usage – A/R Module <a href="#_toc9433270" id="_toc9433270"></a>

In A/R Module, when using the posting part of \<Print Invoices / Post to A/R>, if the G/L Allocation Lines are not balanced for each Company, then the system will automatically create Inter-Company GL Lines to meet the balancing requirement.

![](<../../../../../.gitbook/assets/6 (1)>)

Similar to A/P Invoices, there is no warning message during \<A/R Invoicing>/<**Enter**/Edit Invoices> that balancing lines will be used. Instead, the Multi-Company Balancing check is performed during posting to A/R. Also, the A/R Module will not post/create an Invoice if the A/R Control Accounts are required, but missing from the setup table.

![](<../../../../../.gitbook/assets/7 (6)>)

Further, when using \<Pay Invoices with a **Check**>, if the Cash Account of the Bank uses a different Company than the Accounts Receivable GL Code, then the system will automatically create Inter-Company GL Lines to meet the balancing requirement. As with A/P Payments, if the required A/R Control Accounts are missing, then the system **will** create the Cash Receipt transaction **without** those balancing entries.
