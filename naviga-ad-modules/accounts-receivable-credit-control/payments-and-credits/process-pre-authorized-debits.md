# Process Pre-authorized Debits

### Direct Debits

For many years we have had a process called SEPA Direct Debits that was used by the European market. We now have an additional process that produces a payment batch and output file that will be used by some Canadian media companies. The functionality is similar, but the output from each process is different and created according to the standard formatting from those countries.

#### Prerequisites

1. At the company level, you need to set up your bank details. Navigate to System Settings -> Setup -> Company Setup. Scroll down to Electronic Payments section and enter these three fields

<figure><img src="../../../.gitbook/assets/image (174).png" alt=""><figcaption></figcaption></figure>

2. On your client accounts, on the A/R Node, scroll down to the Electronic Payments section. These 4 fields are relevant to the Direct Debits.

* The first field indicated that yes, this client will use electronic Payments
* The IBAN is the Individual's Bank Account Number
* In the Swift field, enter the Bank's Identifying number (Routing number)
* If desired, can enter the Date of Signature as the date the client authorized the direct debit.

<figure><img src="../../../.gitbook/assets/image (1077).png" alt=""><figcaption></figcaption></figure>

#### Processing the Transactions

Under the Payments menu in A/R, select the Process Pre-authorized Debits option. For those familiar with the credit card "use for balance clear" option, this screen will look familiar. The difference here is that the Company field is required (since that is where we entered the bank info) and each company will need to be run separately.

<figure><img src="../../../.gitbook/assets/image (297).png" alt=""><figcaption></figcaption></figure>

Enter other search filters as desired. and click "Get Clients"

List of clients will be displayed. Click the checkboxes at the end of each row (or at the last header) to select single accounts or select all.

Once selected the payment amount will default to the total balance on the account, but it can be adjusted if you wish to pay a partial amount.

Click the button at the bottom and it will create the payment batch.

![](<../../../.gitbook/assets/image (323).png>)

Click the batch ID to open the batch and download the file

<figure><img src="../../../.gitbook/assets/image (1033).png" alt=""><figcaption></figcaption></figure>

Not an easy reading document, but it is output in the format the banks require.

<figure><img src="../../../.gitbook/assets/image (835).png" alt=""><figcaption></figcaption></figure>

Note that this produced the payment batch and these invoices are marked as paid in the system.

If there are any payments that fail to process when you send the file to the bank, then those payments will need to be manually reversed in Naviga ad.

Easiest way to reverse the check would be to select the payment ID from the batch (or search for it in the payments report) and then in the top right either Void the check (if it hasn't posted to the G/L) or Return the check if void is no longer an option.

#### Find a previous batch

Navigate to Payments -> SEPA Direct Debit Processing

The Direct Debit Batches for Pre-authorized Direct Debits are in the same location as those for the SEPA Payments. Click on the Direct Debit Batchs node.

Select a From Date, and click on Get Batches. All batches for the selected date will be displayed. If it was a SEPA batch, the downloadable file will be in the SEPA column, otherwise it will be in the Preauthorized Debit File column. Click the file icon to download.

<figure><img src="../../../.gitbook/assets/image (1564).png" alt=""><figcaption></figcaption></figure>
