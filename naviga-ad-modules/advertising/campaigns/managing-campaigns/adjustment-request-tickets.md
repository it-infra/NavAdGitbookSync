# Adjustment Request Tickets

Campaign Adjustment Tickets are similar to Campaign Tickets, but just different enough to require their own setup and dashboard. The workflow for Adjustment Tickets has hard coded workflow statuses, but customizable structure of ticket types and adjustment levels so that different users / teams can be assigned based on the value of the adjustment and the ticket type. Additionally, you may have different routings assigned for different Product Groups and/or different ticket teams.

{% hint style="info" %}
**Prerequisite:** complete [Campaign Adjustment Tickets](../../setup/advertising-setup/campaign-tickets-and-adjustment-tickets.md#campaign-adjustment-tickets) setup. Navigate to Setup -> Advertising Setup -> Ticket Type Setup
{% endhint %}

## Creating an Adjustment Ticket

Adjustment tickets are created on the campaign that is being adjusted. The lines being adjusted must have already been Invoiced. These are post-billing adjustments. Select the “Tickets” tab on the screen and then click the New Adjustment Request button:

![](<../../../../.gitbook/assets/4 (21).png>)

The New ticket form will open. For those already using regular tickets this form will look familiar. There are some differences though between a regular ticket and an adjustment ticket.

![](<../../../../.gitbook/assets/5 (73).png>)

1. The ticket type dropdown will only show the Adjustment ticket types.
2. The priority field has the same options as a regular ticket.
3. The status field is not selectable in this workflow, since the status is action driven. A new ticket will always be “pending approval.” Statuses are as follows:
   1. **Pending Approval** - new, pending approval, can still change the value of the request and the lines you selected.
   2. **Partially Approved** - one or more approvals have been received, but more are needed.
   3. **More Info Required** - an approver has requested more information; this ticket is assigned back to the "owner."
   4. **Approved**
   5. **Denied**
4. The assigned team and user is blank at the moment, b/c this will be automatically determined by the value of the adjustment requested.
5. If a custom data form was selected on the adjustment type, it will be pre-filled here, otherwise a user can select to manually add a form.
6. The user owner and team owner will be auto filled based on the creating user and their team. This can be changed (if the user is creating the ticket on behalf of someone else)
7. Enter a short description (required) and long description, if desired. This will assist the approving user in knowing what the adjustment is for.
8. Click the “Select Lines to Adjust” button. A popup will open and display all the invoiced insertions on the campaign.

![](<../../../../.gitbook/assets/6 (52).png>)

By default, the adjustment type will be credit. Can select debit if the adjustment isn’t a credit. The amounts will be forced to negative if they are credits, positive if they are debits. If some lines are positive and some are negative, the user can change from credit to debit before applying and some lines will get a positive adjustment (when debit was selected) and others will get a negative adjustment (when credit is selected).

Select the lines you wish to adjust or start typing the value in the adjustment amount and the line will be selected for you. If you select the line, it will default to full adjustment on that line, but the user can override that and type in a lesser amount.

The system will keep a tally of the total amount of the adjustment.

1. Click Apply
2. The Assigned Team and/or Assigned user will adjust based on the amount of the adjustment.
3. Click Save and the user is returned to the campaign screen and the Adjustment request is sent to the appropriate user (along with an email alerting the assigned user that they have an adjustment to approve).

## Approving/Managing the Adjustment Ticket

The approving user will receive an email with a link to open the ticket. Alternatively, the ticket can also be found on the Adjustment Request Dashboard. (Advertising Module -> Campaigns Menu -> Adjustment Request Dashboard)

Only the approving user (or a member of the assigned team) will be able to approve the ticket.

![](<../../../../.gitbook/assets/7 (42).png>)

Other users may be able to open the ticket, but the Action Options button will only be displayed to the assigned user.

While the ticket is in “Pending” status, the adjustment details tab can still be modified, or the entire ticket could be deleted.

When the assigned user clicks the Action Options button, the actions dialog opens with several choices:

![](<../../../../.gitbook/assets/8 (47).png>)

* To only make a comment, enter the comment and select “Just Save my Changes” this will leave the ticket in pending status and assigned to me
* Select “Approve this Request” to record my approval and create the adjustment (if I am the only approver) or update the status to Partially Approved and move the ticket to the next person in the workflow. Now, the next user in the workflow will get an email directing them to the Adjustment Request Dashboard.
  *   When the ticket is past the “pending” status, the delete button will no longer be available nor will the option to edit the adjustment details

      <figure><img src="../../../../.gitbook/assets/9 (14).png" alt=""><figcaption></figcaption></figure>
* If the user selects the option “Request More Information” the ticket will go back to the Ticket Originator and will be placed in the More Info Required status until the user enters additional information and re-saves the ticket. Upon save, the user will be prompted if they would like the ticket to re-enter the workflow. It will be reassigned back the manager who requested the information and doesn’t have to go back to the manager who already approved it (if there are any).
* If the ticket request is denied, the originating user will receive an email informing them that the request was denied.

## Adjustment Requests Dashboard

The Adjustment request Dashboard is visually similar to the Tickets Dashboard. There are several filters across the top and a count of how many tickets are in each of the hardcoded statuses. User can select to view closed tickets or not. If include closed is set to yes, the closed date range must be filled in to return closed item data. If left blank, only open tickets matching remaining criteria will be displayed.

![](<../../../../.gitbook/assets/10 (16).png>)

The configure output tab allows each user to customize their dashboard to show the columns they wish to see.

![](<../../../../.gitbook/assets/11 (6).png>)

When a user who is assigned an adjustment receives an email about a ticket, the email will include a link to the Adjustments dashboard and will open that specific ticket. The referenced ticket will be listed at the top of the tickets list, regardless of the search criteria.
