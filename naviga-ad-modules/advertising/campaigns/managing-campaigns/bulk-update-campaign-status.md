# Bulk Update Campaign Status

The purpose of this screen is to move campaigns from one status to another in bulk. This is most often used to move a campaign from a reserved status to the final confirmed status to release it for billing and production, however the status codes are selectable so you can use it to move from any status to another status. (contingent on the user's permission to use that status of course)

## Update Status

At the top of the screen, select the relevant Product Groups, Sales rep (leave blank for any rep), status codes and dates.

Bulk Status Update screen has configurable fields to reflect what the logged in user would like to see.

Navigate to the menu Campaigns -> Bulk Update Campaign Status and query on campaigns.

Click the tab “Configure Output” and then in the left side under Available Grid Columns click the fields desired and then click the right facing arrow. Then click Save Configuration. On the right side, select the desired export columns. This is what will be included in the spreadsheet if the user chooses to download the report.

<figure><img src="../../../../.gitbook/assets/image (180).png" alt=""><figcaption></figcaption></figure>

Click the tab “Campaigns”.

Click the expansion arrow on one or more of the records.

<figure><img src="../../../../.gitbook/assets/image (516).png" alt=""><figcaption></figcaption></figure>

The records show a notification if it’s marked as such. Other records marked with a red mark when expanded display the reason for the mark such as prepayment required but cash on account unavailable.

The red X will display on any line that cannot be confirmed unless action is first taken. For example, the customer is over their credit limit. Group Security can allow or prevent the user from approving Campaigns which have issues.

This is the view logged in as the Accounting Manager who has permission to approve an order with credit exceptions:

<figure><img src="../../../../.gitbook/assets/image (627).png" alt=""><figcaption></figcaption></figure>

This is the same view as a user without those permissions. Note the red X at the end of the line. This user can move the status from Say R1 to R3, but he cannot make that final approval unless the exception is dealt with. For example, he would be able to approve the invoices if the client paid for the invoices which were past due.

<figure><img src="../../../../.gitbook/assets/image (620).png" alt=""><figcaption></figcaption></figure>

## Credit Checks <a href="#_toc77617309" id="_toc77617309"></a>

The Security Option to Prevent Campaign Confirmation if Credit Checks Fails: When confirming a campaign this setting would validate customer credit limit or customer past due invoices or as per the **Advertiser Maintenance -> A/R Settings screen** settings for either fields: “Credit Limit” and “Credit Stop Days (Ad).” The system checks also for the balance plus the confirmed unbilled balance. The order of checks if the “Bill-To” has an overdue balance as follows:

1. If the Bill-To has a credit limit then,
2. it checks if the Bill-To A/R balance exceeds the credit limit,
3. it checks if the Bill-To (A/R balance + unbilled confirmed campaign balance) exceeds the credit limit.

Note that the system checks for item 2. if it passed the check in 1. The system provides a warning message and won’t show the Confirm option for the campaign. Also note that in step 3, the system checks if the unconfirmed campaign would exceed the credit limit if confirmed and will stop user from confirming the campaign if this is the case.

Navigate to the menu **Setup -> Admin -> Group security -> Advertising Security**. Check the flag for the field “Prevent Campaign Confirmation if Credit Checks Fails”. Save the settings.

For testing this function, navigate to the menu **Customers -> Advertiser/ Agency Maintenance -> A/R Setup** and choose an advertiser from the drop-down menu with confirmed orders in the system. Scroll to the field “Credit Limit” in the Credit Info section and enter a numerical amount which is less than the total of the confirmed campaigns. Save the settings.

Create a new campaign for this advertiser in the Quote or Reserved status with line items that have amounts against them. Edit the campaign to change its status to Confirmed.

The system will give you a message to indicate that you cannot confirm the campaign because of the security limitation.

![](<../../../../.gitbook/assets/1 (8).png>)

Note that the system displays the credit limit amounts you have set and the current account balance. The balance amount equals the AR Balance of unpaid invoices plus the Confirmed campaigns total.
