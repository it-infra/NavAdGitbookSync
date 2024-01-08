# Credit Stop

## Credit Limits and Credit Stop <a href="#bookmark29" id="bookmark29"></a>

**Credit Hold:** Users can effectively place an advertiser on credit hold with a credit limit. This will not prevent new quotes from being entered for this advertiser, but user will not be able to confirm the order without approval.

**Credit Stop:** To cut off the advertiser after no payments are submitted, user can place this advertiser on credit stop. This will prevent new order entry for this advertiser. If the advertiser submits a payment to the user, in the Accounts Receivable menu, the advertiser will display in red and the credit status for the client will display as credit stop. When user saves a payment in the A/R system for the advertiser, user will be prompted to whether to remove the credit stop status. If user chooses yes, then advertiser will display in green and in good standing status and user will be able to enter new orders for this advertiser. If user chooses no, then the advertiser will still display in red with credit stop status and user will not be able to enter new orders into the system for this advertiser.

As a summary, there are a few options that will impact order entry as it relates to credit: When you create a campaign header (where you set the status) the order has a $0 value as you have not added any line items. The system checks security and if applicable:

1. Stop you if the customer is on credit stop.
2. Allow you to create a proposal, but not allow you to confirm if any of these conditions exist:
   1. Customer exceeds their days past due
   2. Outstanding balance already exceeds their credit limit
   3. Customer requires prepayment
3. If the order is already confirmed, and additional lines are added, which puts the client over the credit limit, the system cannot unconfirm the order (it may already be running). There are reports to help catch these scenarios; there are permissions around who can edit a confirmed order; and there are notifications that can be sent out alerting others when a confirmed campaign is edited.

## Add / Remove Customers from Credit Stop

To place the advertiser on credit stop, navigate to the menu **Credit Control -> Add/Remove Customers from Credit Stop,** or if your role is Credit Manager in A/R User Security, then you also have a tile at the top of the screen to jump directly to this page.

Search for customers using the available search criteria at the top and mark the box of customer(s) and save to change the credit stop for each customer. Client type was added to make it easier to find accounts that need to be put on credit stop. For example, a local advertiser might be subject to credit stop sooner than someone who is a national advertiser. It is also available in the search results grid.

Grid Filters are also in place on this screen, so if you use any of the filters at the top of columns to reduce the list and then click the select all checkbox in the last column (credit stop), only the filtered accounts will be selected.

<figure><img src="../../../.gitbook/assets/image (252).png" alt=""><figcaption></figcaption></figure>

To remove a client from credit stop, use this same screen, but use the Client Selection criteria "Only Clients on Credit Stop"

<figure><img src="../../../.gitbook/assets/image (253).png" alt=""><figcaption></figcaption></figure>

De-select any clients who should be removed from credit stop and save the changes.

You will be prompted to optionally enter a credit rating comment

<figure><img src="../../../.gitbook/assets/image (453).png" alt=""><figcaption></figcaption></figure>

If clients were placed on credit stop, put a comment in the first box, if desired

If client is being removed from credit stop and you wish to put a credit rating comment in on those accounts (perhaps as a reminder to be cautious or keep an eye on them), put the comment in the second box.

Based on settings in Setup -> Admin -> A/R System Setup one or more users may receive an email notification when a client is added or removed from Credit Stop.

## List of Customers on Credit Stop

Navigate to **Credit Control -> List of customers on credit stop**. This is a real time listing of all customers currently on credit stop.

<figure><img src="../../../.gitbook/assets/image (582).png" alt=""><figcaption></figcaption></figure>

Click on the name or the ID to be directed to the customer account screen to see more details about the account. See [**Customer -> Customer Account Overview**](../customers-a-r/#\_toc124065030)
