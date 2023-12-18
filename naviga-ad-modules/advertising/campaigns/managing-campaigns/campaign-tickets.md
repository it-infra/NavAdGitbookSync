---
description: >-
  Tickets allow users to request assistance from others to move a campaign
  forward. Think if it like a task that is attached to a campaign and/or
  campaign line item.
---

# Campaign Tickets

Tickets are created on campaigns and can be linked to specific line items, or it can remain general for the whole campaign. Creating User can choose Ticket Type, optionally choose who to assign it to, Priority and Status. There is also a free-format text area to describe what is needed, or an attachments area if attachments are needed, and a custom data form can be linked if form data needs to be filled in. There is also a history of the changes tab to track its history.

Here is a short recording showing the setup and use of Campaign Tickets.

{% embed url="https://dev.navigahub.com/mothership/resources/videos/TicketsWebinar.mp4" %}

{% hint style="info" %}
Since the poduction of the video we make some minor label changes to make is easier to understand. What the video shows as "Master Ticket Status Codes" and "Ticket Status Code Groups" we now call "Master Ticket Workflow" and "Ticket Type Workflows"
{% endhint %}

Tickets can be set to be routed to individuals and/or to teams according to your needs. If a team is selected, depending on your workflow, an email might be sent to all members of that team. If an individual is selected then only that user will be emailed, even if a team is also selected. Emails are sent when a ticket is created or changed.

The tickets workflow is flexible enough to allow you to create a ticket type and attach it to a team with minimum restrictions and include individuals to be assigned the tickets in the workflow. You can then choose the ticket type and assign to various individuals in a line item without restrictions of a complex workflow.

See also Setup -> Advertising Setup -> [Tickets Setup](../../setup/advertising-setup/campaign-tickets-and-adjustment-tickets.md#ticket-setup)

## Using Tickets <a href="#_toc102043879" id="_toc102043879"></a>

### Create Ticket <a href="#_toc102043879" id="_toc102043879"></a>

Navigate to any campaign's line items node. Then click the Tickets tab and click “Add Ticket”. Choose the Type from the dropdown menu. This sets the workflow in the following fields according to the setup. Once the ticket is saved, it’s not possible to edit the Ticket Type. Choose the Priority from the drop-down as setup above. Choose the Status from the drop-down. The Status selected will set the Assigned Team and Assigned User, but that can be changed if needed.

Enter the short description for the ticket. The Team and User Owners will be set based on the logged in User's ID and Team. This can be overwritted if necessary.

If there is a custom data form tied to the ticket type, the Custom Data Form will be pre-filled and will not be allowed to be changed. Click the edit link above the form to enter the details required on the form. If there isn't a form tied to the ticket type, the form field will be blank but a form can be selected to assign it to the ticket. The form types displayed in here will be the "Campaign Ticket" types. (Note if you have been using forms for a while - tickets didn't used to have a type, so if your ticket type is blank, you will also see those types here)

<figure><img src="../../../../.gitbook/assets/image (1276).png" alt=""><figcaption></figcaption></figure>

The Long Description field allows for text or images which can be copied and pasted. If you’d like to make the window bigger, click the drag the bottom frame of the box.

Check the line items to apply the ticket to in the “Other Line Items” tab. Write additional notes in the Notes tab. (Notes can only be added once the ticket has been initially saved)

Click the Attachments tab, where you can add a single file using the “Select File” button and browse for it, then click “Add”.

![](<../../../../.gitbook/assets/5 (68).png>)

You can also use “Bulk Upload” and load up to 10 files of 30MB each. Once finished, click Save.

Once a user is assigned the ticket, this user will be notified by email of the assignment and any changes made to the ticket.

### Tickets Dashboard <a href="#_toc102043880" id="_toc102043880"></a>

You can view all tickets in the system attached to campaigns in their different workflow stages and assignees, including closed tickets. You can click the Ticket ID and edit the ticket and the updates display on the screen. The colors displayed are the ones reflected from the ticket type workflow or the Master Ticket workflow.

Navigate to the menu Campaigns -> Tickets Dashboard.

![](<../../../../.gitbook/assets/6 (5).png>)

Choose the Ticket Type(s) you’ve setup and any other criteria necessary to find what you are looking for and click Select Data. The tickets display.

Click the “Configure Output” tab on the Dashboard screen.

<figure><img src="../../../../.gitbook/assets/image (702).png" alt=""><figcaption></figcaption></figure>

You can highlight a field on the left side in the Available Grid Columns and click the right facing arrow to move it to the Selected Grid Columns and then click Save Configuration. You can do this for both On Screen and Excel Export columns. Make sure you save configuration for each separately. When you click “Selected Tickets” you will view the selected columns.

<figure><img src="../../../../.gitbook/assets/image (348).png" alt=""><figcaption></figcaption></figure>
