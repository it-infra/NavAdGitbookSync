# Affidavits

The purpose of this document is to provide users with detailed steps of the affidavit process in the Advertising module. Newspapers may need to produce affidavits that prove the publication of a legal ad.&#x20;

The newspaper will either print or email the affidavit using the templates Naviga Ad provides.  If printed, the newspaper can then sign and notarize the document making it legal proof that the ad ran and mail that back to the advertiser business owner so that he has a legal record that he met the advertising requirements. If emailed, the notary signature will need to be added as an image to the template.  Please check with your state to determine if emailed affidavits are allowed.&#x20;

The setup involves creating the fields needed, creating the affidavit form templates and attaching them to the appropriate products and advertising categories.  If emailing, setup will need to be completed for the system to know which form to send and when.

## Setup <a href="#_toc106020199" id="_toc106020199"></a>

### Affidavit Template <a href="#_toc106020200" id="_toc106020200"></a>

Navigate to the option under the Billing menu item for Affidavits -> Affidavit Form Template to create the templates that are used when an affidavit is required on a line item.

The Affidavit Template forms are like other HTML templates in the system. The example provided includes merge fields that pull in details from the campaign, including a preview image from the ad itself. Click on "View Merge Fields Documentation" to see all available merge fields

![](<../../../.gitbook/assets/1 (9).png>)

{% hint style="info" %}
Note: if the legal ad was a press-ready pdf, you will still need a jpg preview image to be added to the material record. It is the jpg preview that is used in the affidavit.
{% endhint %}

Metadata from Order entry can also be added to the template for display on an Affidavit.

In this example, it was desired to add County to the affidavit, but that was something that could change order to order, so the user was asked to supply that information during order entry:

<figure><img src="../../../.gitbook/assets/image (1689).png" alt=""><figcaption></figcaption></figure>

Note that the Merge tag is COUNTY. To then utilize that tag in the affidavit template, place an underscore in front of the Merge Tag. (This is used to identify that it is a metadata tag in the event that someone uses the same merge tag name as one of the standard tags)

<figure><img src="../../../.gitbook/assets/image (1690).png" alt=""><figcaption></figcaption></figure>

### System Parameters Setup

Navigate to **Advertising -> Setup -> Admin -> System Parameters** to configure the email body and subject to be used in sending the emails to the client.

<figure><img src="../../../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

Use HTML or the design tab to configure desired message to the client.  The affidavit itself will be sent as an attachment, similar to invoices and statements.

Use Affidavit Template merge tags to personalize the email to insert data like the Product, Contact Person, etc. These can be found by navigating to **Billing -> Affidavits -> Affidavit Form Templates**

### Affidavit Form Routing

#### **Manual Entry -**&#x20;

Click the +Add New button at the top of the screen for a new routing rule

<figure><img src="../../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

1. Select a Product Group
2. Select one or more Products, or leave blank to use rule for all products in this group.
3. Select a Category Tree
4. Select one or more Categories, or leave blank to use rule for all products in this group.
5. Select Delivery type (print, email, or both)
6. Select form to use for this rule

The system will loop though all the rules and will select the rule that has the most exact matches for a given affidavit.  This means, if a given order could apply to two rules, but one rule it matches 2 criteria and on another rule it matches on only one, then it will use the form with 2 matches.  For example, suppose I have a rule that says for Product ABC, Legal Ads Category Tree, and "All Categories" use template #1.  And I have another rule that says for "Product ABC, Legal Category Tree, Bankruptcy Notice Category, use template #2.  When I book an order for Bankruptcy notice, both of these templates could technically apply, but the system will select template #2 because it has more exact matches than #1.&#x20;

#### **Import -**&#x20;

For more complex routing rules, it may be preferable to import rather than manually entering all the rules.  To import, click the Import Data button in the top right corner of the screen

The following popup will appear:

<figure><img src="../../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

1. Click Download Empty Template button to get a copy of a blank template
2. If you already have data in the grid, click Download Template with Current Routes to download a copy of the existing setup to modify.
3. Fill in all fields based on Template information below.
4. Save spreadsheet to your desktop or other preferred location on your computer
5. In the above popup, click select button to select the saved import file
6. If replacing all the current settings, click "yes" to Clear out and replace current form rules on import.  If adding to the existing routings, leave that option set to "no"
7. Click Import.

Template Details

| Field            | Example      | Infomation                                                                                     | Required?                                                                                                                                              |
| ---------------- | ------------ | ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Group ID         | NAVIGA       | Alpha-numeric ID from the Product Group Setup                                                  | Yes.                                                                                                                                                   |
| Product IDs      | DEMO1        | Alpha-numeric ID for the Product                                                               | No, but if left blank, rule will apply to all Products in the Product Group, which might not be desirable if different forms are using different logos |
| Category Tree ID | LEGALS       | Alpha-numeric ID for the Category Tree                                                         | No, but if left blank, rule will apply to all  the trees, which might not be desirable.                                                                |
| Category IDs     | PUBLICNOTICE | Alpha-numeric ID for the Classified Category / Sub-category. Use comma delimiter for multiples | No, but if left blank, rule will apply to all categories in the tree                                                                                   |
| Delivery Type    | E            | <p>Code for Print, Email or Both.  <br>P=Print<br>E=Email<br>B=Both</p>                        | Yes                                                                                                                                                    |
| Form ID          | 123          | Use the Template ID from setup for Affidavit Form Templates                                    | Yes, and must match the ID of an existing Form                                                                                                         |

### Affidavit Automation

Multiple automation batches can be created so that different users are notified upon completion of different runs.

Click the + Add New button

<figure><img src="../../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

1. Enter description
2. Select to run by product or by product group
3. Select an individual Product or Group or leave blank to use for all.
4. Select Category Tree
5. Select Batch Type (Email, Print, or both)
6. Select Date Selection Type as Running between dates or Running between dates.  Generally this will be set based on end dates.
7. Select Day offset for first run and end date - leave as zero for processing orders ending "today"
8. Select task status as active or paused
9. In the notifications section, enter email addresses for whom to notify on Run Start, upon Successful completion, and upon failure\
   <mark style="background-color:green;">NOTE - this item is still in progress with Dev, so no batch notifications are going out just yet. (AD2-5799)</mark>
10. Click save and new to save and create an additional rule, or click Save and Close to save and return to the Automation task list.  Click cancel to close without saving.

Once the automation task has begun running, reopen the task with the pencil icon to see the logging information.  This will give the time and date it ran, as well as the number of items processed. For detailed logging of the exact affidavits in the batch, see the list of batches in **Billing -> Affidavits -> Affidavit Processing -> Print Batches**

<figure><img src="../../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

The Other tab at the bottom will display who created the automation rule, and who last updated it:

<figure><img src="../../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

This process will run nightly when the server maintenance is done.

### Product Setup <a href="#_toc106020201" id="_toc106020201"></a>

Navigate to the menu Setup -> Product Setup -> Product Details to associate an Affidavit Template Form to the product.  In versions prior to 2023.5, this was how the system knew which products received affidavits and which form to use during manual affidavit processing.  In 2023.5 and beyond, this will be used only as a default template if it isn't otherwise defined in the Form Routing setup.

![](<../../../.gitbook/assets/2 (46).png>)

Navigate to the menu Setup -> Classified Category Tree Setup.

![](<../../../.gitbook/assets/3 (12).png>)

Double click on the parent level of for example, Legal Ads. In the Edit Category window, check the box to Allow Affidavits. The selection affects this level and the children below it.

![](<../../../.gitbook/assets/4 (65).png>)

### Workflow <a href="#_toc106020202" id="_toc106020202"></a>

In order to have an affidavit available for a campaign, there should be an address and number of copies on the order (see note below\*\*\*). This can be added directly to the order if it is a one-time need, or for an advertiser who frequently runs and always uses the same address, you can set it as the Default Affidavit Contacts entered on the advertiser. You can enter up to 10 Affidavit Contacts. For each contact, you can specify the number of Affidavits they will receive. Note: this number can be overridden at the campaign level, but each new campaign will default back to the quantity listed here.

If the affidavit is being mailed, be sure to enter the address how you would like it to appear on the affidavit. If you are using this address in a window envelope, for example, you will want to format it here in the correct way for the postal service to deliver it.&#x20;

If the affidavit is being emailed, the email addess must be entered into the email address field.  Multiple emails are allowed and shoule be separated by a comma.

<figure><img src="../../../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note: When setting up the Affidavit Form Template, there are three different address tags available:

![](<../../../.gitbook/assets/image (520).png>)\
The #CONTACT\_ADDRESS# is the tag specific to the affidavit. If you use this tag, you will need to instruct your users to be sure to fill in the affidavit address on the order and/or the account. If you use one of the other tags, the main address for the advertiser or agency will be what gets used and therefore you will not need to enter the affidavit address.

The system does NOT require the affidavit address to be filled in, since many of our clients use main customer address for affidavits. Please be sure to advise users if you wish for them to enter the address in.

The "copies" column is important though - if that is left blank then the system will not print an affidavit.
{% endhint %}

Navigate to create a campaign and note on the line item entry, there is a tab “Affidavits.” This is prefilled with the Default Affidavit Contacts from the Advertiser. Once the batch for this Affidavit has been processed, you will see entries in the “Affidavit Generated On” and “Affidavit Generated By” columns.  The last column will have a pdf icon of the affidavit that was sent in case the system user needs to access it.  It is also accessible in the batch processing screen.

<figure><img src="../../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

The Booking Wizard Entry screen displays the Affidavit screen on the first page of all three booking wizard workflow options. Click the affidavit button and enter the details. The system saves the information on the line item.

<figure><img src="../../../.gitbook/assets/image (823).png" alt=""><figcaption></figcaption></figure>

Note that Affidavits are generated by line / issue and cannot be reconciled backwards to the Booking Wizard once generated.

## Affidavit Processing (Manual Processing) <a href="#_toc106020203" id="_toc106020203"></a>

There is a process for collecting the Affidavits into a batch and printing them. Navigate to the menu Billing -> Affidavits -> Affidavit Processing.

![](<../../../.gitbook/assets/7 (1) (1).png>)

Fill in the parameters at the top of the screen to select campaigns to include in the batch. For each Campaign and Line ID, you can see the Advertiser, Brand, Issue Count, Issue Date(s) and number of Affidavits to be generated. This information can also be viewed if you expand the line.

Click Generate Affidavit Batch to prepare the items for Printing.

![](<../../../.gitbook/assets/8 (36).png>)

Note that on generating the Affidavit, the system prompts you if you’d like to choose an override Affidavit form.

![](<../../../.gitbook/assets/9 (17).png>)

You can leave the option blank to default to the system setup form for this product or choose a new value in the drop-down.

The Print Batches screen displays the queue. Here you can fill in the date ranges at the top of the screen to see a list of batches that match the criteria of any dates you ran.

![](<../../../.gitbook/assets/10 (8).png>)

If you click on a batch number, you will see the details about that batch and be able to view a PDF of each individual Affidavit.

![](<../../../.gitbook/assets/11 (7).png>)

### Sample Affidavit PDF <a href="#_toc106020204" id="_toc106020204"></a>

![](<../../../.gitbook/assets/12 (11).png>)

Below is the HTML for the above Sample:

{% file src="../../../.gitbook/assets/Affidavit Sample 1.txt" %}

Here is another example (with the HTML below). This one is a 2-page (or more for longer ads) with some more advanced image scalling added.

<figure><img src="../../../.gitbook/assets/image (206).png" alt=""><figcaption></figcaption></figure>

{% file src="../../../.gitbook/assets/Affidavit Sample 2_withNewImageScaling.txt" %}

### Additional Notes <a href="#_toc106020205" id="_toc106020205"></a>

The affidavit rules vary from state to state on legal advertising. Some of the rules are:

* First insertion, last insertion or every insertion must have the affidavit.
* The Affidavit processing is generated in a consolidated group for matching orders; to match if for the same Campaign, product, order group, category tree, description and dimensions. This way if one insertion only per line with multiple issues is required, then user doesn’t have to generate an affidavit for all issues on the line.
* Whether a replica copy is acceptable where some advertisers can cut out and paste the actual ad from the newspaper onto the paper after they run the affidavit batch.
* There is a limit in some states as to how much can be charged for both the ad and for the affidavit.
* Some sites only do one copy and others do multiple and to different addresses.

These Web sites show the law in different states. The New York site shows an example:

[https://www.llcuniversity.com/arizona-llc/publication-requirements/](https://www.llcuniversity.com/arizona-llc/publication-requirements/)

[https://app.leg.wa.gov/rcw/default.aspx?cite=65.16.030](https://app.leg.wa.gov/rcw/default.aspx?cite=65.16.030)

[https://www.dos.ny.gov/corps/news06012006b.html](https://www.dos.ny.gov/corps/news06012006b.html)
