# Custom Forms Setup

The purpose of this document is to provide users with description of custom data forms which can be used to organize forms which contain metadata or requirements related to a specific platform where user sells orders for a client. For example, user can utilize one form for all ads sold on You tube and a different form for all ads sold on Instagram and a third form for video ads. Each form would contain various details which would be standard required information to setup the order on a platform.

The original purpose of these forms were for production requirements, and were known as Production Forms, but they have since expanded and now can be tied to opportunities and to Tickets. They can also be shared with a client on the Portal so that the client can provide the needed data rather than the sales person or production controller. Currently, the Ticket-related Custom Data forms are hidden from the portal since tickets are more of an internal construct.

## Custom Form Setup <a href="#_toc115263573" id="_toc115263573"></a>

This is a similar process to the Classified Category metadata setup. This form uses the Merge Codes from the Metadata and the same merge codes from the order confirmation templates, so you can include data from the Order and your custom fields.

Navigate to the menu in the Ad module -> Setup > Custom Forms Setup. Click the “New” button, then enter an ID and description for the form to indicate its usage.

If this form is to be used for Opportunities, select "CRM Opportunites" in the form type field. If this form is to be used on Tickets, select "Campaign Tickets" Currently all forms are available to be selected in product setup or on a campaign line.

At the bottom of the screen, click the + to add 1 or more new lines. Proceed to enter a label for the first item on the form which can be any alphanumeric entry. Choose from the drop-down a prompt type where it can be a single line, multiple lines, number or date and so forth. In the Validation drop-down, you can choose a validation that corresponds with the entry. For example, a phone number formatting which would automatically formats a phone number entered on the form to match the advertiser’s country’s phone format as setup in the Address Setup System Table.

{% hint style="info" %}
For more details about Prompt types, see [Classified Metadata](classified-setup/category-tree-categories.md#category-metadata) setup.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (626).png" alt=""><figcaption></figcaption></figure>

There is a long description box at the top if you want to give your client some instruction related to the form. And below each Label/Question in the above screenshot there is a box where you can be a little more verbose and give some instruction related to the specific form question.

<figure><img src="../../../.gitbook/assets/image (1633).png" alt=""><figcaption></figcaption></figure>

For each label, there is a Merge Tag that you can enter so that you can later use it to associate the field with the tag on the template as described below.

When finished entering the lines, click Save.

Note that you can mark any of these fields as required by checking the corresponding box so that the user performing the entry must fill in these values to these questions. If the user does not complete the required fields, it will still be able to be saved, but on the Production Reports it won't be considered to be "complete."

You can also click the node “Template” and design an HTML template by clicking the “HTML” tab on the bottom of this screen. This requires HTML knowledge. For assistance, please contact your account manager or the Naviga helpdesk.

![](<../../../.gitbook/assets/2 (1).jpeg>)

These fields are the HTML fields used in the Order Confirmation template marked as #\_Fieldname# while fields used from the Form Metadata tab are labeled #Fieldname#.

Here is an example template to get you started. Be sure to change the tags to match the merge tags in your custom form.

{% file src="../../../.gitbook/assets/Custom Form Template.txt" %}

When the form is being used internally, on the form, there is a history so you can see who saved it and when and whether or not the customer submitted the form from the client portal.

<figure><img src="../../../.gitbook/assets/image (690).png" alt=""><figcaption></figcaption></figure>

## Product Setup <a href="#_toc115263574" id="_toc115263574"></a>

Once you have setup a form, you can then set it as a default on Product Setup screen.

<figure><img src="../../../.gitbook/assets/image (645).png" alt=""><figcaption></figcaption></figure>

Choose the form from the drop-down menu for “Default Custom Data Form” field and save. This will allow the system to attach this form to the order by default and save the user entry effort of attaching the form. This value can be overridden to a different form during order entry.

## Ticket Type Setup

Navigate to Setup -> Advertising Setup -> [Ticket Type Setup](advertising-setup/campaign-tickets-and-adjustment-tickets.md#\_toc102043876) to link your custom form to a ticket type.

<figure><img src="../../../.gitbook/assets/image (1054).png" alt=""><figcaption></figcaption></figure>

## Order Entry Line Override <a href="#_toc115263575" id="_toc115263575"></a>

When you create a line item for this product you will see this form default in on the Line under the “Other Options” tab where you can override it by choosing another one in the “Custom Data Form” drop-down.

<figure><img src="../../../.gitbook/assets/image (1369).png" alt=""><figcaption></figcaption></figure>

## Viewing and Editing From Data <a href="#_toc115263576" id="_toc115263576"></a>

In Order Entry there is a new node in the tree at left called “Campaign Custom Data Forms”. This node is where you can view all lines with an attached form.

<figure><img src="../../../.gitbook/assets/image (1533).png" alt=""><figcaption></figcaption></figure>

Click the hyperlink to the Line ID and a pop-up screen displays the order line.

Click on the form name hyperlink to view the form metadata, add data, generate forms (PDF or HTML) and download the data as JSON or XML files.

![](<../../../.gitbook/assets/6 (12).png>)

The form preview displays the data from the Merge tags on the form as well as the confirmation order HTML fields.

![](<../../../.gitbook/assets/7 (11).png>)

Note that you can edit any of these fields in this order in the Metadata tab. The preview is a display only of how the final form appears.

## Production Workflow <a href="#_toc115263577" id="_toc115263577"></a>

You can view or edit the form data in Production Workflow screens. Note several new columns you can add to your report by clicking on them and then use the right facing mouse to click which will then move them to the available side.

<figure><img src="../../../.gitbook/assets/image (596).png" alt=""><figcaption></figcaption></figure>

On the “Selected Campaign Lines” tab, you can then click the hyperlinks to the forms and fill out any missing data. Clicking the form name from here will bring you to the same screen as above when clicking the Form name from the Campaign.

<figure><img src="../../../.gitbook/assets/image (420).png" alt=""><figcaption></figcaption></figure>

The screen indicates the status of the custom data form data.

## Production by Product Custom Data Forms <a href="#_toc115263578" id="_toc115263578"></a>

Production Reports also allow for downloading the custom data forms data for campaigns which have forms connected to them. The custom forms downloaded contain the information from the campaigns.

Navigate to the menu Production -> Production by Product (non-print). Choose the product from the drop-down menu and date range.

Check the box(es) for the campaigns to download and click the drop-down menu for the action items.

![](<../../../.gitbook/assets/11 (3).png>)

Choose the option “Generate Excel File of Custom Data Forms Data”. Once the file has been downloaded, click OK. Then open the excel file.

![](<../../../.gitbook/assets/12 (25).png>)

The file displays all details of the custom forms. If there are multipe forms, each form will get its own tab. If there are multiple orders with the same form, each order will get its own row on the same tab.

## Using forms on Opportunities

Forms which are set up with a Form type of CRM Opportunities will be allowed to be added to any opportunity. in the "Forms" section. Click add a form in the top right and select desired form. The form will pop up and data can be filled in.

<figure><img src="../../../.gitbook/assets/image (1436).png" alt=""><figcaption></figcaption></figure>
