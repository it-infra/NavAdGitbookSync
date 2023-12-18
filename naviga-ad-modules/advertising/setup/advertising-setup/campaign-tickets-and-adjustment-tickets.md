# Campaign Tickets & Adjustment Tickets

This document provides a description of tickets on a campaign: a feature on one or more line items allowing users to enter a ticket and assign to another user for changes on the campaigns that the creating user does not have permission to perform on his own. User can choose Ticket Type, optionally choose who to assign it to, Priority and Status. There is also an area to describe why the credit is needed. This can be applied to all lines in a campaign or selected lines. There is also a history of the changes tab to track its history.

See also Campaigns -> [Campaign Tickets Dashboard](../../campaigns/managing-campaigns/campaign-tickets.md) for information on using tickets and also a video on the setup and use.

For Adjustment Tickets see setup below and also Campaigns -> [Adjustment Ticket Requests](../../campaigns/managing-campaigns/adjustment-request-tickets.md)

## Campaign Ticket Setup

### Ticket Teams <a href="#_toc102043872" id="_toc102043872"></a>

A user can belong to only one team. Many teams can then be assigned to ticket types and workflows as needed. For example, a financial team can handle financial issues on a campaign, or a production group can be assigned tickets to handle some production aspects of a campaign and so forth.

Navigate to the menu Setup -> Advertising Setup -> Ticket Type Setup, and then click on Ticket Teams node.

<figure><img src="../../../../.gitbook/assets/image (75) (1).png" alt=""><figcaption></figcaption></figure>

Click the “New” to create a Ticket Team. Enter the Team Name and add a member from the drop-down menu and click +. Add as many users as needed to the group. Note that once a user is added to one group, this same user cannot be added to another group. These groups can be specialized in functions, for example operations team versus financial teams vs. production teams and so forth. Save the teams.

Click Yes, if emails should be sent to the entire team rather than just the individual when a ticket is assigned to both a person and a team.

{% hint style="info" %}
If you are thinking to yourself "This person needs to be on two teams though" - perhaps what you really need is a third team....
{% endhint %}

### Master Ticket Workflows <a href="#_toc102043874" id="_toc102043874"></a>

As a prerequisite, the Master Ticket Workflows must be created in the system to indicate the status of a ticket. For example, New, Open, Under Review, Completed and so forth. The master ticket workflow is created so that multipe ticket types can be viewed simultaneously on the Campaign Tickets Dashboard. When viewing a single ticket type, you will see the worflow steps for that ticket type. When viewing multiple ticket types at once, you will see the master workflow stages instead.

<figure><img src="../../../../.gitbook/assets/image (76) (1).png" alt=""><figcaption></figcaption></figure>

This is an example of what I might see when viewing a single Production Ticket Type:

<figure><img src="../../../../.gitbook/assets/image (1662).png" alt=""><figcaption></figcaption></figure>

This is an example of what I see when viewing a Financial Ticket Type:

<figure><img src="../../../../.gitbook/assets/image (539).png" alt=""><figcaption></figcaption></figure>

And this is what I see when looking at both together:

<figure><img src="../../../../.gitbook/assets/image (828).png" alt=""><figcaption></figcaption></figure>

### Ticket Type Workflows <a href="#_toc102043875" id="_toc102043875"></a>

Click the node “Ticket Type Workflows”.

<figure><img src="../../../../.gitbook/assets/image (77) (1).png" alt=""><figcaption></figcaption></figure>

Click the New button to create a new Ticket Workflow. Enter an ID, description and choose a Master Status from the drop-down. Add as many status lines as needed and mark “Completed”, and color code as needed. These statuses are then displayed in the Ticket Dashboard for reporting purposes. Save the settings.

### Ticket Type <a href="#_toc102043876" id="_toc102043876"></a>

Click “Ticket Type” node on the tree. This is to create a type of ticket that would be matched with a Workflow from the above node. Enter an ID, description and select a Status Code Group from the drop-down menu. Create as many ticket types as needed and save. You can attach a workflow to many ticket types as needed. If any or all of these require a custom data form, select that from the dropdown. (Setup for the Custom Data Forms is found in Setup -> [Custom Forms Setup](../custom-forms-setup.md))

<figure><img src="../../../../.gitbook/assets/image (304).png" alt=""><figcaption></figcaption></figure>

### Ticket Priorities <a href="#_toc102043877" id="_toc102043877"></a>

Click the “Ticket Priorities” node to setup the level of criticality of a ticket to be addressed by the group or individual assignee. Save the settings.

<figure><img src="../../../../.gitbook/assets/image (518).png" alt=""><figcaption></figcaption></figure>

### Ticket Workflow Routing <a href="#_toc102043878" id="_toc102043878"></a>

Click the “Ticket Workflow Routing” node on the tree. Only the Ticket Type is required to be chosen and not the Product Group and the Ticket Team. If the Product Group and Team are left blank, then all values in the system for these two fields apply and will be included in this workflow. Click the <img src="../../../../.gitbook/assets/image (341).png" alt="" data-size="line"> icon to load the workflow for the ticket type.

<figure><img src="../../../../.gitbook/assets/image (704).png" alt=""><figcaption></figcaption></figure>

If you check the box “User Selected” the system allows the users of the selected ticket team to choose that option in the ticket entry screen. The Route to Type defines if this workflow stage is selected if it will route to an individual or a team (must select here which individual or team) or route back to the ticket owner and/or team.

## Adjustment Tickets

Adjustment Tickets are similar to Campaign Tickets, but just different enough to require their own setup and dashboard. The workflow for Adjustment Tickets has hard coded workflow statuses, but customizable structure of ticket types and adjustment levels so that different users / teams can be assigned based on the value of the adjustment and the ticket type. Additionally, you may have different routings assigned for different Product Groups and/or different ticket teams.

### Adjustment Ticket Type Setup

Navigate to Setup -> Advertising Setup -> Ticket Type Setup. Notice there is a section here for Adjustment Tickets Setup.

Adjustment tickets use the same teams as Campaign Tickets, so if customizing routing by sales user, be sure to setup Ticket Teams prior to creating the Workflow Routing here.

![](<../../../../.gitbook/assets/0 (107).png>)

Enter an ID, Description, and an ad type. The Custom Data form is optional. If you have additional form data you wish to have the user fill in related to the ticket, you can assign a form to the ticket type.

The Ad type dropdown will only display flat fee ad types that are not flagged with the Listing ad flag. The Ad type selected here will be the ad type on the adjustment line created once the adjustment is approved. You may wish to have ad types specific to these adjustments. Whether or not the ad type is flagged as commissionable to the rep will determine whether or not the rep’s commission is adjusted based on the credit/debit adjustment.

{% hint style="info" %}
Note: The G/L Type on the line will be determined by the G/L Type on the original order line.
{% endhint %}

### Ticket Workflow Routing

Next, Select the Ticket Workflow Routing node.

<figure><img src="../../../../.gitbook/assets/image (324).png" alt=""><figcaption></figcaption></figure>

Select a Ticket type in the drop down.

If this same workflow routing will be used for all product groups and ticket teams, the product group and/or Ticket Team fields can be left blank and then click the circular arrow. ![](<../../../../.gitbook/assets/2 (45).png>) If you will be setting up different routing for different product groups or ticket teams, then select the one or both of those fields, and then click the button.

**When making assignments for approvals, the "Ticket Team" for routing purposes will be determined by:**

1. The first Order Rep’s User ID on the Campaign
2. If the rep isn't a system user or if they aren't on a team, then the Logged in user’s Team
3. If logged in user isn't on a team, then the team manually selected on the ticket

Once the team is derived, then we follow this logic to find a matching approvals workflow:

1. Ticket Type, Team and Product Group all match
2. Ticket Type and Team match
3. Ticket Type and Product Group match
4. Ticket Type matches

Use the “Add New Lines” drop down to select the desired number of lines – one for each number band you wish to set up. In the example above, I have 3 number ranges, each with a different workflow for who must approve the adjustment. Within each band, you can have up to 4 approvers defined.

Using the screenshot above as a reference, I have these rules in place for my “Adjustment for Printer Error” Ticket Type (click on the pencil icon next to the band to set up the following):

1. Up to $250 – the ticket doesn’t need approval; the adjustment will be automatically created upon save.
2. From $250-5000 – there is only a single approval required. According to my setup, this can be done by either the user “Sherri ABC” or by anyone on the Super Powers team. You don’t have to select both a user and a team. It can be one or the other or both. Having a team assigned also is handy if Sherri is out of the office, someone else can step in and approve on her behalf.
3. From $5000+ – Sherri ABC is the first approver, but it also needs to go to Dan and then Kelly. Once the final approver approved the ticket, the adjustment lines are automatically created.

<figure><img src="../../../../.gitbook/assets/image (312).png" alt=""><figcaption></figcaption></figure>
