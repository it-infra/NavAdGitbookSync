# Group Security (A/P)

#### A/P Security

This section controls the features access in the A/P module’s screen.

For Information on Group Security for other Modules, see the respective module documentation or [System Settings Group Security](../../../system-settings-admin/security/group-security.md)

<figure><img src="../../../../.gitbook/assets/image (1600).png" alt=""><figcaption></figcaption></figure>

## **General Security Settings**

1. Prevent override of check number: If this option is checked, user will not be able to override a check number in the A/P screens. If left blank and unchecked, user will be able to override a check number in the A/P screens.
2. Prevent changes to 1099 amount in invoice detail: If set to yes user will not be able to override an amount in the invoice inquiry screen for the 1099 forms. If left blank, however, user will be able to change the amounts on the 1099 forms in the invoice detail screen in A/P module.\
   ![](<../../../../.gitbook/assets/image (919).png>)
3. Prevent invoice amount to exceed P.O. line amounts: If checked, this option will not allow users to enter invoice amounts in excess of the purchase order line items amounts. The below screenshot is from AP Invoice Entry. The below is $700. If this is set to "yes", and if the below PO was for $700, even if I typed $800 in the amount field, it would revert to $700. It will allow me to enter an amount less than 700, but not more than 700.\
   ![](<../../../../.gitbook/assets/image (880).png>)
4. Require A/P batches to balance before posting: If checked, user cannot post batches of A/P invoices to G/L unless the batch is balanced (see screenshot below). User will have to balance the batch before posting. If the box is unchecked, then user will be able to post any A/P batch of invoices with no restrictions requiring the batch to be balanced.\
   ![](<../../../../.gitbook/assets/image (1627).png>)

## **Vendor Maintenance**

<figure><img src="../../../../.gitbook/assets/image (1647).png" alt=""><figcaption></figcaption></figure>

1. Allowed to view/ change tax id: If checked, this box allows users to view change the tax id for a vendor in the analysis report 1099 vendor listings. If left unchecked, then user will only be able to view the last 4 digits of the tax id. Screen from Vendor Maintenance below, with and without this option set to yes.\
   ![](<../../../../.gitbook/assets/image (364).png>)![](<../../../../.gitbook/assets/image (1269).png>)
2. Allowed to change vendor auto clearing info: If checked, this option allows users in the group to change the auto clearing info for a vendor. If set to no - all these fields will be grayed out:\
   ![](<../../../../.gitbook/assets/image (1607).png>)
3. Prevent changing status from to stop to pay or hold: If the option is checked, the users in this group will be prevented from changing the status of A/P operations on vendors to stop to pay or to hold. If left unchecked, users will be allowed to change the status.

## **Bank Reconciliation**

<figure><img src="../../../../.gitbook/assets/image (1669).png" alt=""><figcaption></figcaption></figure>

1. Allowed to re-open a closed statement: If this option is checked, user can reopen a closed statement for bank reconciliations.

## **Purchase Orders**

<figure><img src="../../../../.gitbook/assets/image (764).png" alt=""><figcaption></figcaption></figure>

This is mostly used by book customers and allows for options regarding purchase orders settings. It may also be used in the Production / Job Costing Module. These settings will affect what the user can do in the A/P Module or Production Module -> Purchase Orders -> Purchase Orders menu.

1. Allowed to Enter Requisitions / Quotes
2. Allowed to Enter Purchase Orders that Require Approval
3. Allowed to Approve Purchase Orders
4. Allowed to Enter Purchase Order Receipts
5. Allowed to reopen Closed Purchase Orders

## **A/P Invoices**

<figure><img src="../../../../.gitbook/assets/image (1664).png" alt=""><figcaption></figcaption></figure>

1. Suppress the Import All P.O. Lines Prompt/ popup when selecting a P.O. line on an A/P Invoice: When this option is checked, when user selects a PO line on an AP invoice, the system will not display the popup prompt to import all P.O. lines. When set to no, the following Pop-up will appear, giving user the option to automatically add all line items from a PO onto the A/P Invoice.\
   ![](<../../../../.gitbook/assets/image (1598).png>)
