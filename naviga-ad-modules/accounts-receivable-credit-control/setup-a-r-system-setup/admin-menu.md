# Admin Menu

## A/R System Setup <a href="#_toc124065024" id="_toc124065024"></a>

See [Setup ](./)for A/R System Setup

## Group Security Setup (A/R Security) <a href="#_toc124065024" id="_toc124065024"></a>

System administrators can setup different groups with different rights to A/R Function by navigating to in A/R -> Admin -> Group Security. Other non-administrative users will be able to view their group security from this screen, but not make edits.

For Information on Group Security for other Modules, see the respective module documentation or [System Settings Group Security](../../system-settings-admin/security/group-security.md)

### Security Group Selection

Delect the desired Security Group for which to apply the following settings.

### **A/R Account Screen Permissions**

#### Screen Feature Security

1. Allowed to Create Credit Control Contacted Notes: If this box is checked, user can create notes regarding the clients’ communications under Credit Control.
2. Allowed to Create Credit Control Internal Notes: If this box is checked, user will be able to create internal notes under credit control section in A/R screens.
3. Allowed to Create New Contacts: Only when this box is checked, user will be able to create new contacts from various screens regarding the A/R module for a client.
4. Allowed to Edit Contacts: If the box is checked, user will be able to edit existing contacts even if created by another user.
5. Allowed to Email: If this box is checked, user will be allowed to use email to contact clients or internal users from the A/R module.

#### Account Summary Screen

1. Sort open invoices oldest first: This option, if checked, will list the invoices on the account summary screen from oldest to newest.
2. Default Aging Display: Select which aging view type will be the default. Options are to display by due date or by invoice date.

### **Cash Entry**

These are the options that control the A/R Cash Entry into the system.

#### Basic Features

1. Allowed to Enter/Apply Checks: If checked users can enter new checks and apply the checks to payments to advertiser orders. Please note that user can enter checks and not apply them to payments of invoices.
2. Allowed to Enter Credit Card Payment: If checked users can process credit card payments. For this function to be effective, system administrator configures users for ECP payments on the Main Menu backend. If user is not setup for ECP, user will not be able to enter or process credit card payments. Users will also be allowed to enter new credit card numbers into the payment screens.
3. Allowed to Enter G/L Cash: If checked, users will be allowed to enter G/L Cash when they click this sub menu in the A/R module Payments menu. If this is disabled, user should receive an error message: “You do not have the Security for this option.” In either case, user will be allowed to perform G/L Cash Inquiry.
4. Prompt for Receipt: This option if checked will prompt users to generate a PDF receipt when entering a payment or prepayment for an order from the respective pop up screen.
5. Sort Oldest Invoices First: This option if checked will display the cash entry invoices from oldest to newest.

#### Cash on Account (COA)

1. Allowed to Apply COA that is flagged as Pre-Payment: If checked, in A/R Payments of invoices, if advertiser has cash on account in the system that is flagged as a prepayment, user can apply this amount to pay for an invoice. User will receive a warning that he has selected a payment that is currently attached to orders with prepayments. User can click OK and proceed and can also view the details for the payment in a separate tab. If the option is unchecked, user will receive a message that user does not have the security to allow them to use the COA that is a prepayment for the order.
2. Default Module for COA: Administrator can choose any option from the drop-down menu for the default module to which to apply the COA. When user is entering the COA in the A/R payments screen, a confirmation screen with a field to Allocate to Module. This value will have the default module which administrator set up in A/R security screen. This will also be reflected in the Aging Report.
3. Cash on Account must be assigned to a Product: If checked, user will receive a message that this field is mandatory to choose from the drop-down menu in the confirmation screen after user chooses COA for payment for user to proceed with payment. This also will be reflected in the Aging Report and will determine the A/R code used for payment. If unchecked, user can proceed through the confirmation screen without errors.

#### Discounts based on Payment Terms

1. Allowed to Apply Discounts After Discount Has Expired: Administrator checks this box and enters the next one.
2. Number of grace days after discount date expires. This is to allow the user to apply expired discounts within the grace days’ period. Please note that the expiration date of a discount is still setup on the Main Menu in the back; otherwise this option is invalid. If left unchecked, user will not be allowed to apply any discounts past the expiration date.

#### Operator discounts

1. Allowed to Enter Manual Discounts: If the administrator checks this box; then he can enter the next field.
2. Maximum percent discount allowed for the user to apply to payments. The user cannot exceed this percentage when applying payments to an invoice. If user exceeds the % defined here in the payment screen, user receives an error that user exceeded the maximum amount allowed in his security settings and the user will not be allowed to proceed with the payment.

#### Invoice Write offs in Payment Application

This section affects the write offs specifically in the Payments screens for individual invoices by credit card or check.

1. Administrator checks this box to give a free hand to apply write offs to users for any amounts on the invoice. Administrators can uncheck this box and the next box displays.
2. Maximum write off amount allowed to the user to apply to the payment of invoices. If user can write off a certain amount and user checks the write off box on an invoice which exceeds this amount, then user receives the error message: “The remaining balance exceeds your permitted Write-off amount”. And user will not be permitted to proceed with payment unless they uncheck the write off box on the payment screen.

#### COA Write-Offs in Payment Application

1. Maximum Amount can be entered to limit the cash on account write-offs.

#### Pay for Others

1. Allowed to use “Also Pays For”: This option allows to display other advertisers for which this customer can pay. This is only valid if the administrator sets up an advertiser to pay for another advertiser as in the case with parent and child companies on Main Menu in the backend.
2. Allowed to Pay Invoices for Other Customers: If checked then user can view an extra field where they can select other customers’ invoices/ orders and pay for them. If user is not setup with this option, even if the advertiser is set on the back menu to “Also Pay For”, user will receive the message: “This invoice is for a different customer and your security does not allow you to apply payments from one customer to another’s invoices.”

#### Batch Control

User should note that when some of these options are unchecked, they automatically will disable other options which logically correspond to them. For example, when the option

“Require batch on checks” is disabled, “Allowed to Create New Batches” is also automatically disabled. When “Allowed to Delete Batches” is unchecked, “allowed to Close Unbalanced Batches” is also automatically disabled. When “Allowed to Override Bank Name from Batch” is unchecked, “allowed to Override Period from Batch” becomes disabled.

1. Require Batch on Checks: If checked this option will not allow user to enter a check without attaching the check to a batch. This does not apply to credit card payments.
2. Allowed to Create New Batches: If checked, user can create new batches when entering checks or from the Batch Review sub menu.
3. Allowed to Delete Batches: If checked user can delete any existing batches.
4. Allowed to Close Unbalanced Batches: If checked, user can close a batch even if the entered number of checks and amounts do not match the expected number and amounts. User will receive a warning message that batch is unbalanced but user will be allowed to close the batch.
5. Allowed to Override Bank from Batch: If checked, user can change the bank name on the batch which they chose to attach a check to and proceed with the payment. If the box is unchecked, user will view the bank name as a greyed-out option which user cannot modify.
6. Allowed to Override Period from batch: If checked, user can change the financial period on the batch. If the box is unchecked, user will view the financial period as a greyed-out option which user cannot modify.

#### Other

1. Allowed to Un-allocate Previously Paid Invoices: When administrator checks this box, users in this group will be able to unallocated paid invoices. When the box is unchecked, user will view the option to unallocated paid invoices, but user will not be able to select the option.
2. Allowed to Create Debit/Credit Notes: If administrator checks this box, user will see a button on the invoice payments screen which they can click to create credit or debit notes. If the box is unchecked, user will not be able to see this option on the payments screen.
3. Default Create Reversing Debits Option to YES: If checked the user will have this option default to yes when the user creates a credit memo in the A/R module payment by check screen. This option is typically used for book module users, where the customer deducts an amount from his payments for the returns which he has not yet sent. This creates an automatic reversal when the amounts are received.
4. Allowed Overpay Invoices: If checked, user will be able to apply a check with an amount that exceeds the invoice amount. This is especially applied to Book users. If unchecked, user will receive an error message that the amount of the check exceeds the amount of the invoice and user will not be able to proceed with the payment.

### **Other Cash functions**

1. Allowed to Apply Payments to Orders: If checked, user will be able to click Pay and Apply payments to invoices. If unchecked, user receives a message that their security option is not setup to allow them to apply payments to orders.
2. Allowed to Enter Returned Checks: If administrator checks this option, user will be able search payments and use the option to return checks. If this option is unchecked, user will be able to see the option greyed out but will not be able to select it.
3. Allowed to Delete (Void) Checks: If this option is checked, user will be able to search for a payment and void/delete the check. If this option is unchecked, user will be able to see the greyed-out option but will not able to select delete/void the check.
4. Allowed to Transfer Checks: If this option is checked, user will be able to search for a payment and choose the option to transfer the check to another payment. If this option is unchecked for user, he will not be able to select this option.
5. Allowed to Apply Credit Notes: If this option is checked by the administrator, user will be able to navigate to the Payments menu in A/R and select “Apply a Credit” sub menu, search on the payment and apply that credit to an invoice.
6. Allowed to Reverse an Applied Credit: If this option is checked, user can reverse a credit which user applied to an invoice. Otherwise, user will not be able to view the option from the drop- down menu when user searches for payments.
7. Allowed to Change COA Reason Description: If this option is checked, user can edit the cash on account reason description while performing the COA operations. IF the option is not checked, user will not be able to overwrite the description, but will still be able to perform COA operations.

### **Write-offs and Refunds**

This section affects the A/R invoice write offs and refunds under the invoicing menu to process invoices in bulk.

1. Maximum Write-off Amount: User enters the maximum amount users in this group can mark as refund or write off on invoices. This operation is performed from the A/R module invoicing menu to allow users to write off outstanding amounts or issue refunds for clients for amounts due to the client because of cancelling an order. User will not be able to exceed this amount because the amount will be defaulted in the appropriate field.
2. Allowed to Issue Refunds via Credit Card: If this option is checked, users in the security group will be able to mark refund amounts on invoices to be refunded back to the user on the advertiser’s credit card directly.
3. Allowed to Issue Refunds via Check: If this option is checked, users in the security group will be able to mark refund amounts on invoices to be refunded back to the user by issuing a check to the advertiser.

### **Other Settings**

1. Allowed to Turn Credit Hold On/Off on Customer Maintenance: This option allows the group and its users to have the ability to change the credit hold on any advertiser or agency. If this option is not checked, then this group is not allowed and will not be able to change any credit hold option for the advertiser or agency. This capability is performed from the Advertiser Maintenance screen.
2. Allowed to Transfer Invoices to Another Client: If this option is checked, user can perform a bulk transfer of one or more invoices from one advertiser to another.
3. Allowed to Transfer Invoices to a Collections agency: If this option is checked, user can perform bulk transfer for one or more invoices from an advertiser to a collection agency.
4. Display Cash In/Out Summary on A/R Home Page: If checked, this option will allow user to view the amount of cash in and out whenever user opens the A/R module home page. The amounts will display for today, yesterday, last 7 days and last 30 days.
5. Allow Changes to Misc. Invoice Descriptions after Posted to A/R: This option if checked will allow user to make changes to a miscellaneous invoice description even if the invoice has been posted to A/R. If unchecked, user will not be allowed to make the changes to the description after it has been posted.
6. Allow Change of Sales Rep Adjustment from Invoice Detail Screen: If checked, this option allows user to make changes to the sales rep adjustment from the invoice detail screen.
7. Only allow selection of Banks for Companies this Group has access to: If checked, this group is allowed access to only the banks where in the Bank Maintenance screen they have a Bank G/L Code with the first 2 digits matching the company digits to which this group has access according to the group settings in Company/ General Security node.
8. Force Currency on New Accounts to Country Setting: If this flag is set to “Yes”, then in the various places where you create a new account, if this flag is set, it will select the Currency from the Country settings for this advertiser account. Also, in Full Name Maintenance the Currency Option will be disabled if this new security flag is set.
9. Prevent Misc. Invoice Entry for Clients on Credit Stop: If set to yes, a user in this security group will not be able to enter any entries in Miscellaneous Invoice entry in A/R Module if the client selected is on Credit Stop.  This includes Misc. Invoices, Credit Invoices and Recurring Invoices.

## Email Duplicates

Best practices in Naviga Ad dictates that you should never have two accounts with the same email address and there are controls to prevent that from happening. Naviga Support and Implementation personnel have the ability to turn off that control if you have a reason for really needing to allow duplicate emails.

This report will display accounts that have duplicate email addresses. It is grouped by email address to easily visualize the accounts where the duplicates exist. Links to the Contact record and the account record are provided for easy navigation

<figure><img src="../../../.gitbook/assets/image (1356).png" alt=""><figcaption></figcaption></figure>
