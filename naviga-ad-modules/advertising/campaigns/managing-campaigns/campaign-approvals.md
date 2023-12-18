# Campaign Approvals

Campaign approvals are for approving a PROPOSAL (Quote campaign) so that it can be sent to the client. These are approvals that triggered either based on the price of the campaign or based on the % of discounts that have been applied to the campaign.

It is a separate proces where someone (perhaps Finance) moved the campaign to Confirmed Status thereby allowing it to run and bill. This final confirmation might be held up based on the client's credit limit being exceeded or the number of days past due being exceeded. See Bulk Update Campaign Status for that process.

The campaign approval process allows for managers to Approve or Reject a sales rep’s campaign proposal before the proposal can be sent to a customer. Once the sales rep enters a campaign proposal, a notification is sent to the manager - defined in the system security menus - requesting approval. The manager can Approve or Reject the campaign proposal. The salesperson cannot generate a campaign proposal until the proposal has been approved. Further settings on the portal prevent customers from being able to see the proposal until the manager approves the proposal.

## Group Security Settings <a href="#_toc94782479" id="_toc94782479"></a>

In Advertising Group Security, you can switch on or off the Approvals functionality. You can also make the approvals be based on a minimum proposal amount. For instance, approvals can be required for proposals more than a set value. Since this is based on group security, these settings can be different for different security groups. Perhaps a classified rep needs approval for a campaign greater than $500, but a retail rep doesn't need approval until the campaign reaches $10,000.

There are security flags in the system which determine approval status if the dollar amount or percentage are exceeded as follows:

1. The total amount of the campaign proposal where approval is required above the total amount.
2. Proposals must be Approved if this Percent Discount on any Line Exceeds a certain amount.
3. Proposals must be Approved if this Average Discount Percent is Exceeded on a Campaign

![](<../../../../.gitbook/assets/2 (44).png>)

{% hint style="info" %}
In the above screenshot the Value approval setting is 0.00. This essentially means ALL campaigns will require approval. If you want the approval to only be based on the discount percentages and not trigger based on total amount, leave that value field empty.
{% endhint %}

## Sales Rep Maintenance Settings <a href="#_toc94782480" id="_toc94782480"></a>

On the Rep. Maintenance screen, you can specify who will be notified when a Campaign requires approval.

Navigate to the menu Setup -> Salesrep Setup. Search for the sales rep name in the drop-down menu.

Scroll to the section labeled “Alert via Email when Campaign Approval is Required”.

![](<../../../../.gitbook/assets/3 (27).png>)

Select one or more managers who will then be notified to approve the campaign up to this discount percent placed on the campaign. This is a slight change from the pre-2022.2 version of Naviga ad where a simple email address was placed in this notification field rather than a user.

This serves the purposes of:

* If an alert which contained a hyperlink to the campaign approval screen was sent to an email address of an individual that did not have access to the system, this individual would not be able to do anything with the information provided.
* This now allows you to add a security level on the Campaign Approval screen as to which campaigns you are allowed to approve.

The system recognizes the names to allow for selection within the Salesrep maintenance window. This information is derived from a new field on the User Maintenance window within the User Settings for Advertising that is titled _**I Can Approve Campaigns**_. If this is set to Yes, this allows the user to be linked as an approver on the Salesrep Maintenance screen.

![](<../../../../.gitbook/assets/4 (43).png>)

Please be sure that an email address exists for this user, otherwise, the system will not know where to distribute the email notification. The email address can be added per user within the User Administration screen where you can add, edit and inactive users.

![](<../../../../.gitbook/assets/5 (35).png>)

So how do these changes impact how campaigns are approved? In our older releases, if you had access to the Campaign Approval screen, you would have access to approving any campaigns awaiting approval whether the notification went out to you or someone else.

Now, within the User Security screen, there is another new field entitled _**Campaign Approval Scope**_. This setting determines what the user can see and have access to when launching the Campaign Approval screen.

![](<../../../../.gitbook/assets/6 (7).png>)

Once this access is established, this will control what Approved Users that you will have access to and what campaigns you can approve.

![](<../../../../.gitbook/assets/7 (9).png>)

{% hint style="info" %}
If you are just upgrading from a pre-2022.2 version....and already have this feature with email addresses already established?

Naviga has written a conversation routine that will read the email address setup against the Salesrep Maintenance screen as the approver and search for a matching email address associated with a user ID. If found, the email address on the Salesrep Maintenance screen will be replaced with that user ID. If not found, the email address will be removed from the Salesrep Maintenance screen. We will also default all users to the _**I Can Approve for Anyone**_ option as this was the current design of the Campaign Approval screen if one had access to it and would cause no disruption as to how it is currently designed.
{% endhint %}

## Campaign Entry and Status <a href="#_toc94782481" id="_toc94782481"></a>

If a Campaign (with a Quote status) is entered or changed then the salesperson’s manager will be emailed with an Approval request.

![](<../../../../.gitbook/assets/8 (40).png>)

A status bar (in bright red) will inform the user that a Campaign is Pending Approval.

![](<../../../../.gitbook/assets/9 (5).png>)

If a Campaign has not been approved, then the user will not be able to generate the Proposal. The “Send a Proposal” button will be disabled.

![](<../../../../.gitbook/assets/10 (25).png>)

## Campaign Approval by Manager <a href="#_toc94782482" id="_toc94782482"></a>

The manager navigates to the Orders menu -> Campaigns -> Campaign Approvals. The campaigns which require approval or rejection are listed once manager searches on the "Approval Users" and “Product Group” fields and clicks on “Get Data”. The users shown in the "Approval Users" will reflect the logged in Users security. They may only see themselves there, or they may see additional users that they can approve for.

<figure><img src="../../../../.gitbook/assets/image (1035).png" alt=""><figcaption></figcaption></figure>

Choose the correct status from the “Approval Status” drop-down corresponding to each campaign.

Note that if the campaign is changed post approval, but pre-confirmed status, it will require another approval from the manager.
