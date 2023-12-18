---
description: >-
  The purpose of this document is to explain how user can mark an invoice in
  accounts payable as paid by credit card.
---

# Mark A/P Invoices as Paid by Credit Card

It is common these days for companies to pay for some invoices with a company credit card rather than paying with a check. Not only does it delay the actual cash payment that needs to go out from your bank account, it also can provide benefits like earning points to fund travel budgets and other items which make paying with credit cards an attractive option for companies.

For reporting purposes though, for some purchases it might be undesirable to have "Amex" for example as the only Vendor involved. You would want a record of who ultimately you are doing business with. For small purchases, like getting gas on a business trip or having a dinner with a client, that might be fine, but if you are making larger purchases with the corporate card, you may wish to allocate that charge to the actual vendor.

The basic workflow and G/L implications are as follows. In this example we are recording the purchase of an item at the apple store for $4700 with a credit card.

<pre data-overflow="wrap"><code><strong>1. Invoice is Entered in A/P Invoice Entry with Apple as the Vendor and G/L looks like this:
</strong>                       Debit    Credit
Equipment              4700.00
Accounts Payable                4700.00

<strong>2. Once Posted, Invoice is flagged as having been paid with a credit card (meaning it is no longer  payable to the A/P vendor, but does still need to be paid off via the credit card company.)  The G/L credited here will depend upon the prerequisite setup in Setup -> Admin -> A/P System Setup (details on this in prerequisite section below)
</strong>                       Debit    Credit
Accounts Payable       4700.00
Clearing Account                4700.00

3. Next month, the bill comes in from Credit Card company, which I must pay off.  There are likely to also be smaller items on there that I don't necessarily care to record a separate invoice for and will just charge that directly against an expense account - Perhaps the card was also used to take a client to lunch or some miscellaneous travel costs that are one time in nature for which I don't really need a separate invoice. Suppose that the bill is $5,000 that I must pay
                       Debit    Credit
Clearing Account       4700.00
Other Expense G/Ls      300.00 
Accounts Payable                5000.00

Then of course when the Payment actually goes out to the credit card company:
                       Debit    Credit
Accounts Payable       5000.00
Cash                            5000.00
</code></pre>

## Prerequisite - Setup <a href="#_toc465670614" id="_toc465670614"></a>

Navigate to A/P Module, **Setup -> Admin -> A/P System Setup**.

Scroll to the credit card section.

<figure><img src="../../../../.gitbook/assets/image (33) (1).png" alt=""><figcaption></figcaption></figure>

Enter the credit card description, the G/L account related to the card and click the + sign. Save the data.

It is recommended that you do **NOT** enter actual credit card numbers in this screen, because the system is not transacting your credit card to pay for the vendor bills. This is for tracking purposes only and the system will display all numbers. There is no encrypting on this description, so enter just a description like the last four digits and name of the card only.

## Create A/P Invoice for Purchase <a href="#_toc465670612" id="_toc465670612"></a>

See [**A/P Invoice Entry**](../a-p-invoice-entry.md) for details on how to enter an A/P Invoice. This will be done initially for the Asset (or large expense) purchased with the credit card (step 1 above) and then another A/P invoice later when actually paying the credit card (step 3 above). The initial A/P Invoice entered will be to the real Vendor it was purchased from, and then the latter will be to the Credit Card company Vendor to pay the credit card statement.

## Invoices Paid by Credit Card <a href="#_toc465670612" id="_toc465670612"></a>

This can only be done once the above invoice batch with the real Vendor has been Posted to the A/P Module. User will navigate to the invoice detail and using this menu option flags the invoices which have been paid by a credit card, meaning that you have already paid for them on your credit card, so we are telling the system not to pay again with a check to this vendor. Note that the system will not actually charge any credit card.

<figure><img src="../../../../.gitbook/assets/image (34) (1).png" alt=""><figcaption></figcaption></figure>

This will prompt a popup window asking the user for the Payment date and period as well as which credit card was used (this credit card comes from the above Prerequisite setup)

<figure><img src="../../../../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>

This will move the amount of this invoice from Accounts Payable G/L account into the G/L Account that was tied to this credit card. (This is Step 2 in the above overview)

## Display of Invoices <a href="#_toc465670613" id="_toc465670613"></a>

When you get your credit card statement, you will need to pay it with an A/P invoice for the total amount to be paid. The detailed line items on the A/P Invoice will be made up of smaller items which did not warrant a separate invoice as well as the items that are now in the Credit Card Clearing account. Smaller line items will be added and allocated to their appropriate expense or asset G/L account. Items that were already invoiced separately will be added (either individually or in summary depending on preference) and will be charged against the clearing G/L account.

If you want to search on any Invoices already entered and flagged as having been paid with Credit Card , navigate to the menu **Invoices -> List of Invoices -> List of Invoices Paid by Credit Card node**. Enter the date range to search on and click “Get Invoices”.

Once the invoices display, you can click the invoice ID hyperlink for more details on any invoices. Can use the filter at the top of the Paid w/Credit Card column to focus on one Statement at a time if there are multiple cards.

<figure><img src="../../../../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>

For any invoices found on the current statement, select the checkbox in the far right column to mark as reconciled, and then click “Save Reconciled.” This doesn't affect the G/L at all, but allows you to acknowledge that it was found on the credit card statement and paid for. Then in subsequent months this item can be filtered out when running this same report. Note at the top of the report, along with the date filters, there is a filter to show All transactions flagged as paid with CC, or only those that are reconciled or only those unreconciled.

If desired, user can expand the details of the invoice by clicking the expansion arrow next to the invoice ID. this shows the initial G/L's used to record the A/P Invoice.

<figure><img src="../../../../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>

## Pay the Credit Card Vendor Statement

The final step will be to Pay the credit card vendor for all purchases made on the statement. (Again see [**A/P Invoice Entry**](../a-p-invoice-entry.md) for instructions for entering an A/P Invoice.) For anything that was already recorded as a separate A/P invoice, user can enter a single line with the total from the Reconciled Invoices report. This will be applied to the G/L account from the above Prerequisite setup for the card being paid. Any transactions that did not warrant a separate A/P invoice will also be added as line items on the invoice with the appropriate expense account for the purchase.

After the A/P invoice for the credit card company is entered and posted, the check will be cut. For that navigate to **Payments -> Pay A/P invoices** and follow the normal procedure for paying invoices when they become due.
