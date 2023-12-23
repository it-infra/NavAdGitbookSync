# Account Approvals

The system has the option to require finance approval for accounts created in the system. This is accomplished in the Account Maintenance or in the A/R module as a stand-alone menu.

{% hint style="info" %}
Note that the approval status for an account does not trickle down from parent to child account. Each account must be approved on its own.
{% endhint %}

## New Client Approval Defaults

User determines the prerequisite setup in the A/R module, **Setup -> Admin -> A/R System Setup.**

Scroll to the section “Client Defaults” and click the box of the field “Auto Approve New Clients” to set the value to “Yes” if you would like the new accounts in the system to be automatically set as approved and their orders can be processed. If you leave the box value as “No”, new clients created in the system will be marked as pending approval and campaign creation (or confirmation) may be prevented (depending upon Group Security).

<figure><img src="../../../.gitbook/assets/image (407).png" alt=""><figcaption></figcaption></figure>

## Group Security Setting for Account Approval Actions

You can determine whether actions may be allowed or not from the **Group Security menu -> Advertising Security**. Scroll to the Client Approval Requirements section.

Check the yes/no boxes for each of the flags to control what is and is not allowed for unapproved accounts:

* Prevent Opportunity Creation if Account is not Approved
* Prevent Order Creation if Account is not Approved
* Prevent Quote Creation if Account is not Approved

These flags affect all users in this security group.

<figure><img src="../../../.gitbook/assets/image (853).png" alt=""><figcaption></figcaption></figure>

## Account Approval Procedure

There are a couple of ways to approve accounts:

### From Advertising Module

**Option 1:** In the Advertising module, navigate to the menu **Customers -> Account Maintenance -> A/R Setup** node.

* Search for the account to be approved and note the field “Account Approval Status” which indicates whether this account has been approved or not yet.
* Click the “Approve Account” button. Click Yes to the confirmation message indicating that this action cannot be undone. The screen then displays the approved status, approver name and date on which this account was approved.

**Option 2:** Navigate to **Customers -> Approve Pending Accounts**. This menu allows for individual or bulk approvals of accounts.

* Search by account creator, date range of when the account was created and approval status. Click on “Get Data”.
* When data displays you can check the box corresponding to the account or check the top box to check all accounts. Then click on “Approve Selected”.

### From the A/R Module

**Option 1** - Click on **Customers -> Name Address Maintenance** and follow same procedure as Option 1 above. The benefit of doing it this way is that you have the whole account edit screen available to you then, so if this customer has a specific credit limit, specific requirements for where to send invoices, etc. You can then manage those settings at the same time as you are approving the account.

**Option 2** - Click on **Customers -> Approve Pending Accounts**. Follow same procedure as Option 2 above.

{% hint style="info" %}
Note the hyperlinks to the accounts which direct you to the account maintenance menu.
{% endhint %}

## CRM Account Approval

In Customer Overview screen under the CRM/ Sales tab, user can change the status of a customer who is not approved by clicking on the “Change” button displayed in the Account Overview pane, next to the field “Source(s)” under the Account Approval Status text.

<figure><img src="../../../.gitbook/assets/image (329).png" alt=""><figcaption></figcaption></figure>

A pop-up with Account Approval Priority displays where user can enter free text to mark the priority of the approval request. Then click the “Save” button.

The status displays with the new request priority.

This allows user who approves accounts to view the priority user entered on approval requests under the A/R menu of **Customers -> Accounts Pending Approval**.

<figure><img src="../../../.gitbook/assets/image (193).png" alt=""><figcaption></figcaption></figure>

User can then check these accounts and approve them in a priority as set by the request.

If user is not allowed to create an order or proposal for an unapproved account based on their group security, and attempts to create an order, the system produces a message to prevent it.
