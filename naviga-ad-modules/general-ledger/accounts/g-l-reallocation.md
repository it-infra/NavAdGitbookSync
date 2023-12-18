# G/L Reallocation

This document describes the process of setup and implementation of G/L Reallocation. The basic concept is to take monthly expense account balances and re-arrange them in a different grouping. For example, a home office pays rent, utilities, and insurance. Reallocation can assign a portion of each expense to different departments, such as Ad, Subs, and Events.

In the process, the original expense accounts are not reduced. Instead, the “Clearing Account” acts as an offset to the expense showing how much was reallocated to the departments. Then the end target G/L accounts each show how much of the home office expenses have been assigned to each department.

## Setup G/L Reallocations <a href="#_toc87274932" id="_toc87274932"></a>

Before using G/L Allocations, user must set up Clearing Account G/L Codes with the box marked “Yes” for them to appear on the drop-down menus in G/L Reallocation Setup. To do so, navigate to the menu Accounts -> G/L Account Maintenance. Choose the G/L Account ID using the magnifying glass to search for the account or directly enter the account ID if available.

Click on the box “This is a Clearing Account” to change the value to “Yes” and click on the “Save” button.

![](<../../../.gitbook/assets/1 (84).png>)

Navigate to the G/L Module menu Accounts -> Setup G/L Allocations.

Click on the “Define Clearing Accounts” node and the screen will display two tabs, “Allocations to Clearing Accounts” and “Reallocations from Clearing Accounts.” Both parts must be completed before a “Save” button is effective.

![](<../../../.gitbook/assets/2 (14).png>)

On the “Allocations to Clearing Accounts” tab, the left side has the original expense G/L codes and the right side has the clearing account G/L codes. Only G/L codes which have clearing account set to “Yes” will appear in the “Clearing Account” drop-down menu.

The “Percent” column allows one expense account to be allocated to multiple clearing accounts which will appear on multiple lines, or to reallocate only a portion of the full expense account. This does not have to equal 100% per source expense account.

![](<../../../.gitbook/assets/3 (52).png>)

On the “Reallocations from Clearing Accounts” tab, each clearing account has a list of end target G/L codes and the percent share of the reallocated amount that will be assigned to each G/L code. On this tab, these percentages must add up to 100%.

The Allocations TO Clearing Account tab accumulates the amounts from all the listed source Expense (for example) accounts and puts them into the mapped Clearing Account. A reallocation will pull 100% of the source amounts so no percent would be needed.

The Reallocations FROM Clearing Account takes the accumulated amount in the Clearing Account and distributes it to the listed destination accounts, the set percentage to each. The Journal Entry that is produced by Reallocations has only G/L Lines from this part of the process.

The Clearing Account is not a G/L Account that would be used in normal day-to-day transactions. It is specifically created for this Reallocation process. Financial Statements should show the Clearing Account as a contra to the source accounts so that the total expenses (for example) are not overstated.

Rent Expense 5000

Insurance Expense 500

Postage Expense 50

Reallocated Expenses -5550

Dept A Expense (40%) 2220

Dept B Expense (40%) 2220

Dept C Expense (20%) 1110

If you’re not combining multiple source expenses (for example) before reallocating them then this two-step setup is a bit more cumbersome. However, users should still not use a real expense (for example) G/L Account as the Clearing Account because the Journal Entry will actually reduce the balance of that original account, which is technically not accurate (a Reclassification rather than a Reallocation). An example of a bad result on Financial Statement:

Postage Expense 0

Reallocated Expenses 0

Dept A Postage 20

Dept B Postage 20

Dept C Postage 10

## Run Reallocations <a href="#_toc87274933" id="_toc87274933"></a>

Click on the next node “Run Allocations”. This will pull G/L amounts from the set up source expense accounts into the clearing accounts, and then reallocate the accumulated total from the clearing accounts into the end target G/L codes.

![](<../../../.gitbook/assets/4 (41).png>)

Only amounts for the specific period that is run will be reallocated. If new journal entries change the balance in a source expense account for a period, then that period must be run again to recalculate according to the new monthly total. Likewise, if the reallocation percentages are changed, then running a reallocation for a Period will recalculate according to the new monthly total.

A journal entry will be created and automatically posted to G/L, with a credit to the clearing account and a debit to each end target G/L code. These journal entries, prefixed with “RR”, are listed and can be reviewed on the fourth node “List of Reallocation Journal Entries”. This is also available from the “Journal Entries” menu in G/L module.

![](<../../../.gitbook/assets/5 (42).png>)

In a revision situation, i.e. new source expenses or revised percentages as described above, the new journal entry will reflect the difference between the prior journal entry and the current reallocation. In other words, the sum of all RR journal entries for a Period will equal the current reallocation calculated for that period.

## Budgets and Forecasts <a href="#_toc87274934" id="_toc87274934"></a>

The node “Run Budget/Forecast Allocations” will reallocate the budget or forecast amounts of a source expense G/L Code rather than the actual amounts posted to G/L. This uses the same percentages and mapping, but is run for the full year instead of per Period.

![](<../../../.gitbook/assets/6 (53).png>)

No journal entries are created, but the budget or forecast amounts stored on the clearing account and end target G/L codes will be overwritten.

## List of Reallocation Journal Entries

The last node on the tree will display a list of completed Reallocation entries.

The selection types and Start/End dates/periods allow user to select the date range filter for the reallocations. Enter desired dates and click "Get Journals" to run the search

<figure><img src="../../../.gitbook/assets/image (989).png" alt=""><figcaption></figcaption></figure>

The list of journal reallocations will be displayed. Click the excel icon or pdf icon to export the results

Click the > on the left column to expand and see details, or click on the Journal ID hyperlink to open the Journal Entry detail screen

<figure><img src="../../../.gitbook/assets/image (628).png" alt=""><figcaption></figcaption></figure>

Once posted, the Journal Entry cannot be modified, but it can be reversed (button at the bottom of the Journal Entry screen.
