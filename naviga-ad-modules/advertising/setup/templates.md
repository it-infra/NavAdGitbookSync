# Templates

## Order Confirmation Email Templates

When creating a campaign, you will likely want to send the client a proposal (if it is a Quote campaign) or an order confirmation (if it is a reservation or confirmed campaign). To do that, you will first need one or more Confirmation templates. To create a new template, follow these steps

<figure><img src="../../../.gitbook/assets/image (1601).png" alt=""><figcaption></figcaption></figure>

1. Navigate to Setup -> Templates -> Confirmation email templates
2. In section "Campaign Email Templates" click on "Create New" and a new template will be started
3. Enter the confirmation type that the template will be used for (you will want at least one template for Performance Campaigns and at least one for Flexible Campaigns)
4. Give your template a name and if desired, a description
5. Select the orientation as Portrait or Landscape
6. Select a default Logo. (Logos are defined in Setup -> System Tables Setup -> Invoice Form Logos)
7. Select the Product Group(s) that are eligible to use this template.
8.  Using the Design or HTML tabs at the bottom, create your Order Confirmation Template.

    <figure><img src="../../../.gitbook/assets/image (1460).png" alt=""><figcaption></figcaption></figure>
9. If you are contracted to use the Advertiser Portal, you may add a link in here to "click here to approve this proposal online." Sample html is provided below to get you started. There are examples for Flexible Campaigns, with and without the Portal as well as Performance Campaigns, with and without the Portal.

{% file src="../../../.gitbook/assets/Performance Campaign with Portal (2).txt" %}

{% file src="../../../.gitbook/assets/Performance Campaign without Portal.txt" %}

{% file src="../../../.gitbook/assets/Flexible Campaign without Portal.txt" %}

{% file src="../../../.gitbook/assets/Flexible Campaign with Portal (2).txt" %}

In 2023.3, support was added to group line items by package. Below are sample templates which group lines by package (these samples also include the link to sign propsal in the Portal):

{% file src="../../../.gitbook/assets/PackageGroupingConfirmation_performance.txt" %}

{% file src="../../../.gitbook/assets/PackageGroupingConfirmation_flexible.txt" %}

## Production Reminder Email Templates

Production Reminder Email templates are linked to a [Production Reminder Stage](../production-ad/#production-reminders)

<figure><img src="../../../.gitbook/assets/image (374).png" alt=""><figcaption></figcaption></figure>

1. Select Create New and give your Production reminder a name and if desired, a description.
2. Select which product(s) will use this template
3. Mark the Active flag as "yes" to indicate that it can be used.
4.  Switch to the Editor window and using the design or html tabs at the bottom, enter your production reminder email text.

    <figure><img src="../../../.gitbook/assets/image (952).png" alt=""><figcaption></figcaption></figure>
5. Click the View Merge Fields Documentation button at the top to see which field tags are available to be used in the email. A sample starter template is included below

{% file src="../../../.gitbook/assets/Production Email Reminders.txt" %}

## Marketing Content Templates

Custom Marketing templates can be used as part of an order confirmation template. Typically once a site goes live, their order confirmation template doesn't change very frequently. However, they might want to have different promotional messages that get swapped out from time to time. If there are several Order Confirmation templates it can be cumbersome to update the promotional message in each template when the marketing message changes.

This is where marketing content templates comes into play. There is a single tag called #CONTENT# which gets called inside a broader tag of CONTENT\_START and CONTENT\_END that will call the appropriate Marketing Content Template based on the template selected on the Campaign Header. Here is some sample code for calling the template. This would be placed somewhere in the Order Confirmation/Proposal Template

{% code overflow="wrap" lineNumbers="true" %}
```
<!-- #CONTENT_START# -->
<div style="text-align: left; font-family: arial; background-color: #008DA5; color: #fff; box-sizing: border-box; width: 100%; padding: 5px; font-size: 16px; line-height: 16px;">
audience breakdown
</div>
<div style="width:100%; padding: 10px; border:1px solid #ccc; border-top-color: #f1f1f1; box-sizing:border-box; overflow-x: hidden;">
#CONTENT#
</div>
<br />
<!-- #CONTENT_END# -->
```
{% endcode %}

To create a Marketing Content Template follow these steps:

<figure><img src="../../../.gitbook/assets/image (1469).png" alt=""><figcaption></figcaption></figure>

1. Navigate to Setup -> Templates -> Marketing Content Templates OR Setup -> Advertising Setup -> Marketing Content Templates.
2. Select "Create New"
3. Give your template a Name and if desired, a description
4. Select "Active" as true to enable it to be used.
5. Use the design or html tabs at the bottom, enter your marketing text and/or images
6. Click Save

## Customer Service / CRM Email Templates

Similar to the other templates, these templates are configured here and then used in emails to the customers. The Customer Service emails are used in sending reminder notices our to clients in the A/R module and also when sending extra invoice copies to customers via the Customer screen or from the Credit Control Module on the My Collections page

<figure><img src="../../../.gitbook/assets/image (459).png" alt=""><figcaption></figcaption></figure>

The CRM - Templates section is used in the CRM module when sending emails to clients from the customer screen, My Contacts area ("Send Template Email")

<figure><img src="../../../.gitbook/assets/image (1155).png" alt=""><figcaption></figcaption></figure>

1. Navigate to Setup -> Templates -> Customer Service/CRM Email Templates
2. Select "Create New" in the desired section
3. Give your template a Name, Subject Line for the email, and if desired, a description
4. If there are any attachments being used, select it from the attachments list (set up in advance on the "Attachments Storage" node on this screen)
5. Select "Active" as true to enable it to be used.
6. Click on "View Merge Fields Documentation" to open a window to see all available merge tags
7. Click on the Editor tab and use the design or html tabs at the bottom, enter your text. (examples provided below)
8. Click Save

{% file src="../../../.gitbook/assets/CRM Template.txt" %}

{% file src="../../../.gitbook/assets/CustomerServiceTemplate with Open Invoices.txt" %}
