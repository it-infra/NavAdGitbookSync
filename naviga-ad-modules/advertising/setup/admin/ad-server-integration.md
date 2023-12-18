# Ad Server Integration

## Overview <a href="#_toc105408175" id="_toc105408175"></a>

Once configured, an Ad campaign's digital order lines will be connected with Google Ad Manager (GAM). The order is booked in Naviga Ad and passed through the integration for serving. Certain Material Types can be uploaded into Naviga Ad, others will need to be uploaded directly into GAM. Or, if preferred, traffickers can upload all materials in GAM. GAM then counts the actual impressions and clicks and sends them back to the Ad system for accounting and billing purposes.

This document provides an overview and detailed explanation of Google Ad Manager setup and how the following features function:

1. Setup of Google Ad Manager Integration in the Ad system. (Advertising Module -> Setup -> Admin -> Ad Server Integration Setup)
2. Qualifying campaigns created in the Ad system are automatically created in GAM.
3. Campaigns that have a GAM external ID in the Ad system will save updates to the campaign back to GAM (as configured in the Setup).
4. Real-time inventory forecast provided from the Ad system campaign line entry.
5. Actuals are pulled from GAM to their respective campaign lines in the Ad system campaign that have external IDs matching the GAM IDs.
6. Additionally, actuals may be imported from GAM or any other ad server using the import facility. (See [Campaigns -> Import Actuals from a File](../../campaigns/ad-server-syncing-reconciliation.md#\_toc105408230))

## Upgrading from a Release prior to 2021.2 <a href="#_toc105408176" id="_toc105408176"></a>

If you are one of the handful of clients still on an older release, this section is for you. This upgrade required data conversion and so will require a test upgrade in your test environment prior to a live upgrade.

#### Data Conversions on Upgrade <a href="#_toc105408177" id="_toc105408177"></a>

This upgrade requires data conversion. It’s important to confirm the data has converted properly and that all the new features and setup in 2021.2 are reviewed before upgrading the PROD environment. Failure to confirm could result in interruptions to the GAM interface.

All Ad Server settings must be reviewed and saved after the upgrade. The “Settings” node is particularly important as this is a new screen that defines data sync options.

We recommend all Cross Reference Tables and Other targeting tables be resaved after the upgrade. Targeting tables should also be updated when adding new values in GAM.

![](<../../../../.gitbook/assets/1 (50).png>)

Please check the setup fields and existing line items post conversion, especially that sizes are reflected in the Native Styles.

#### Sizes

* All lines serving to GAM will get updated to move the Sizes, Master/Companion Sizes and Native styles into Expected Creative Containers
* All Ratecard lines for products that are linked to a GAM server will get updated to move the Sizes, Master/Companion Sizes and Native styles into Expected Creative Containers
* All Native Styles previously imported and used will be converted to Size codes and associated to the line as an Expected Creatives size.

#### Ad Units

* Previously Selected Ad Units (parents and children) were stored against a Line item, Rate line etc. This data is being converted to store a list of included and excluded Ad Units
* This is on both Rate lines and Campaign Lines

## Prerequisites <a href="#_toc105408178" id="_toc105408178"></a>

1. You must be using a current version of the Ad system due to Google restrictions. Google deprecates older versions of their software regularly, so you will need to keep somewhat current with Naviga ad to prevent interruption with GAM
2. You must be using GAM, and not the older DART.
3. For Naviga Ad to properly support the GAM interface, setup a user account called [dfpadmins@msgl.com](mailto:dfpadmins@msgl.com) on your GAM instance and assign it admin rights. This is the user that will be referenced in the GAM setup screen.
4. GAM Integration Setup must be completed in the Ad system, including:
   * Connection Setup: The GAM Integration uses a single authorized user account in GAM to connect and process data. This part will be completed by Naviga Personnel once you have created the above dfpadmins account on your GAM instance and provided us your network code.
   * Settings:
     * Profile must be created
     * Workflow settings must be set
   * Cross Reference Tables
     * Advertisers
     * Agencies
     * Ad Units
     * Sales Reps
     * Traffickers
     * Ad Types
     * Ad Units

## Group Security Settings related to GAM <a href="#_toc105408179" id="_toc105408179"></a>

<figure><img src="../../../../.gitbook/assets/image (975).png" alt=""><figcaption></figcaption></figure>

A security flag in the Digital Group Security allows admin to set it so that it requires a validation of inventory on GAM. The field is #1 above - "Validate GAM Inventory when using GAM Template or a Ratelink with Google Targeting." The options are:

* No, Allow Overselling - This will allow overselling without warning
* Allow, but Warn on Overselling - this will Warn on oversell
* Do NOT allow Overselling - this will Stop entry on oversell

Setting #2 above - You must also choose which GAM Inventory Number to use Available Units or Possible Units.

Setting #3 - IF the user is allowed to Oversell, there is a field to indicate how much they can oversell by.

Setting #4 - There is a Digital Campaign Delivery Report available in the system. This setting will determine if the default is to view how the campagin is performing overall, or how they are performing in the current month. This just sets the default view. It can easily be changed by the user when viewing the report.

Setting #5 - Set to yes, Inventory will be re-checked if the line is updated. If set to No, inventory will not be rechecked on updates.

Keep in mind that the above are GROUP SECURITY settings, so what you set for one group of users may be different than another group. For example, you might now Sales to oversell, but if Traffic is making the change, they might have additional information and therefore be allowed to oversell or only oversell by X%.

## Automatic Order Creation in GAM <a href="#_toc105408180" id="_toc105408180"></a>

Qualifying campaigns and campaign lines created in the Naviga Ad system are automatically created in GAM.

#### Campaign qualification works as follows:

*   The Campaign Status must be set to whatever status is configured in the "CAMPAIGN STATUS TO TRIGGER ORDER CREATION IN GAM" field in Ad Server Integration Setup "Settings" Node.

    <figure><img src="../../../../.gitbook/assets/image (716).png" alt=""><figcaption></figcaption></figure>
* The Campaign must be assigned a Production Controller who is cross-referenced to a GAM Trafficker.
* The sales rep must be setup in GAM.
* The Campaign must start on or after today.
*   Advertiser and Agency (if applicable) must either exist in the AdServer already and be linked to the account in Naviga, or there is also a create missing advertisers and agencies checkbox to have the system create the missing advertisers or agencies as needed

    <figure><img src="../../../../.gitbook/assets/image (169).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If the advertiser/brand does not exist in GAM, and the _Create Missing Advertisers in GAM_ option is set to no, the Campaign will not be sent to GAM.
{% endhint %}

#### Campaign line item qualification works as follows:

* The line must have one or more valid GAM Ad Units\_.\_
  * If this is a Run of Network Line, each digital product must have a valid GAM Ad Unit.
*   The Line’s ad type must be setup with GAM cross-reference definitions for _Line Type_ and _Cost Type. (See Setup -> Advertising Setup -> Ad Types)_

    <figure><img src="../../../../.gitbook/assets/image (176).png" alt=""><figcaption></figcaption></figure>
* Optional: The Line Size should be set:
  * Line Size must be Numeric, in Width X Height format, e.g. 300x250
  * If a valid line size is not set, a default value of 300x250 is used; this is a required field in GAM.
  * If there are no qualifying lines, but the campaign qualifies, it will be created in GAM with no lines

#### When a Campaign is created in GAM the following fields are written:

**From the Campaign**

1. Advertiser / Brand
2. Agency
3. Trafficker
4. Sales Rep(s)
5. Start Date / End Date & Time (time will be midnight unless overwritten on the line)
6. Internal Order Notes
7. Ad Order ID
8. Campaign Description/Name
   1. Format default is: Campaign\_Description - (Naviga Ad: Campaign ID)
   2. Option to instead use Advertiser Name - Campaign Description - Start Date - Campaign ID - Product Group
9. PO Number
10. Currency ID

**From the Line Item**

1. Start Date / Time
   1. Start Time is set to Midnight unless overwritten
   2. Unless the Start Date is today – in which case the Start Time is set to 5 minutes in the future
2. End Date / Time
   1. End Time is set to 11:59:59pm unless overwritten
3. Line Description
   1. Default Format is: Line\_Description (AD\_Line\_ID)
   2. Alternative option: Ad Unit - Line ID
4. Cost Per Unit
5. Units requested
6. Ad Line ID
7. Ad Unit(s)
8. Creative Type
   1. If Creative Type is set to M (Master/Companion): Road blocking Type is set to Creative Set
   2. If Creative Type is set to V (Video VAST): Environment Type is set to Video Player
9. Creative Placeholder
   1. If using a Standard Creative Type, the Dimension(s) selected will be applied (if none is sent in then a default Dimension of 300x250 is used)
   2. Uses Master and Companion Sizes for M or V Creative Types
10. Targeting – if set to send to GAM; Geo Targeting, Day Part Targeting, Tech Targeting, Custom Targeting, etc.
11. Allow Overbook is set to TRUE
12. Cost Type (CPC, CPD or CPM)
13. Line Item Type (STANDARD, NETWORK, ETC)
14. Roadblocking = One or More (unless already set to As Many as Possible). Roadblocking is a form of homepage takeover where advertiser ad must be viewed by site visitor before the visitor can continue onto the site.
15. Delivery Rate = Evenly
16. Creating Rotation Type = Even. Rotation is when the ads are in the form of a slide show of materials from the advertiser.

## Automatically Creating Advertisers and Agencies in GAM <a href="#_toc105408181" id="_toc105408181"></a>

The Ad system may be configured to create missing advertisers and/or agencies in GAM while creating new orders. This process works as follows:

**For Advertisers:**

* GAM does not support the concept of brands. Instead GAM expects each Advertiser Brand combination to be represented as a separate advertiser record in GAM.
* When creating a new order in GAM, the Ad system first searches GAM looking for an Ad advertiser ID in the external ID field on the advertiser record in GAM.
* The advertiser ID is determined as follows:
  * If the advertiser does not use brands, or if the selected brand ID is XX, the Ad advertiser ID is the NAME.ID from the Ad database.
  * If the advertiser does use brands, and the selected brand ID is not XX, the Ad advertiser ID is NAME.ID|BRAND.ID.
* If an exact match is not found searching the external ID of all advertiser records in GAM, the Ad system determines that the advertiser does not exist, and if setup, GAM will create a new advertiser record.

**For Agencies:**

* If setup, the Ad system will create a new agency record in GAM if an existing match is not found.
* The Ad system attempts to find an existing agency in GAM by searching the external ID field for a matching the Ad name ID.

New advertiser and agency records in GAM include the following fields from the Ad system:

* _Company Name_ or _Company Name – Brand Name_, if this is an advertiser with a brand (saved in the Name field).
* Ad Name ID (saved to External ID)

## Updating Existing Campaigns <a href="#_toc105408182" id="_toc105408182"></a>

When Campaigns are updated in the Ad system, the corresponding campaign and line items are also updated in GAM. Deleting a campaign will also trigger an update. If we are deleting a campaign or a line, we first attempt a delete. If the status has progressed too far for a delete, we then attempt to do an archive.

The following actions trigger an update to GAM:

* New qualifying campaign or line saved.
* Certain field IDs updated on the campaign details (header) screen.
  1. Production Controller
  2. Sales Rep(s)
  3. Start / End Dates
  4. Advertiser Name or ID
  5. Agency
  6. Description
  7. Changing Status
  8. Canceling a Campaign
  9. External Order
  10. P.O. Number
  11. Applied Team
  12. Notes
* Certain items on a line item.
  1. Start / End Date
  2. Rate
  3. Quantity
  4. Line Description
  5. Ad Unit(s)
  6. Dimensions
  7. External ID
  8. Notes
  9. Delivery Rate Type
  10. Priority
  11. Allow Overbook setting
  12. Targeting
  13. Creative ID
  14. Creative Size
  15. Creative Preview URL
* Deleting a line item.
* Selecting the resynchronization to GAM option on the campaign.

Note the following:

* Deleted line items that had previously been linked to GAM are set to _Archived_ status in GAM, if allowed.
* Cancelled campaigns are set to _Archived_ status in GAM, along with all their line items, if allowed.
* When updating an existing campaign, it is possible that it did not qualify to be saved to GAM before the changes, and now does. In this case the campaign and line items will be created in GAM upon Saving.

For more detailed technical information on the objects and fields affected as a result of a trigger please refer to these links:

* Order: [https://developers.google.com/ad-manager/api/reference/v202008/OrderService.Order](https://developers.google.com/ad-manager/api/reference/v202008/OrderService.Order)
* Line Item: [https://developers.google.com/ad-manager/api/reference/v202008/LineItemService.LineItem](https://developers.google.com/ad-manager/api/reference/v202008/LineItemService.LineItem)
* Creative: [https://developers.google.com/ad-manager/api/reference/v202008/CreativeService.Creative](https://developers.google.com/ad-manager/api/reference/v202008/CreativeService.Creative)
* Creative Line-line Association: [https://developers.google.com/ad-manager/api/reference/v202008/LineItemCreativeAssociationService.LineItemCreativeAssociation](https://developers.google.com/ad-manager/api/reference/v202008/LineItemCreativeAssociationService.LineItemCreativeAssociation)

## Real time Inventory Forecasting <a href="#_toc105408183" id="_toc105408183"></a>

A Check Inventory button is available when creating new line items on a campaign in the Ad system. You can define an oversell percentage. It will either prevent saving the line and give you a warning message that there is not enough inventory.

This feature requires that the following information be filled out on the Line Item:

* Ad Type – Must be an Ad Type with GAM Cross References setup
* Start Date
* End Date
* Size
* Estimated Quantity
* GAM Ad Unit(s)
* The Rateline must also be set that it is using GAM Inventory

Clicking this button calls GAM’s forecast service with the line information and returns:

* Available Units: The number of units that can be booked without affecting the delivery of any reserved line items. Exceeding this value will not cause an overbooking, but lower-priority line items may not run.
* Delivered Units: The number of units that have already been served if the reservation is already running.
* Matched Units: The number of units that match the specified targeting and delivery settings.
* Possible Units: The maximum number of units that could be booked by taking inventory away from lower-priority line items. (Please note: booking this number may cause lower-priority line items to under deliver.)
* Reserved Units: The number of reserved units requested. This can be an absolute or percentage value.

Either Available Units or Possible Units (depending on Group Security) is what is use to determine availability. The additional data is for informational purposes in the Ad system. It is not used to validate a new Line Item.

## Changing Delivery Priority <a href="#_toc105408184" id="_toc105408184"></a>

GAM has some rules on which priority is set based on line types and Naviga can’t break them in the API. User can go login to GAM and break these rules there, but the API doesn’t allow it until GAM changes the API.

Here is a good chart to show what is available:\
[**Line item types and priorities - Google Ad Manager Help**](https://support.google.com/admanager/answer/177279?hl=en)

How line items are selected for delivery based on type and priority. Line-item type and priority are a starting point to determine how a line item competes with other line items, yield groups, and Ad Ex.

![](<../../../../.gitbook/assets/image (1614).png>)

In Naviga Ad Line Item Entry, we follow the rules set by GAM, so if you are booking a CPM Line, which would be linked to the STANDARD type, we allow you to change the priority, but only within the 6-10 Range:

<figure><img src="../../../../.gitbook/assets/image (894).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note to previous Adbase Users: We have confirmed that AdBase allowed this on the screen, but then the line kicked out in GAM. The same error is confirmed to happen on Premium / GAM 360 using the latest APIs.

<img src="../../../../.gitbook/assets/image (672).png" alt="" data-size="original">
{% endhint %}

## Actuals from GAM to the Ad Campaign Line <a href="#_toc105408185" id="_toc105408185"></a>

At a defined interval, default is once every 30 minutes, the Ad system gathers all the campaigns lines that are currently running or have recently finished and submits a query to the GAM reporting service to return actuals’ clicks and impressions by ad unit. This data is placed in the _Current Impressions/Quantity_ field. The _Updated as of_ field is set to today.

## Setup Sequence (Admin) <a href="#_toc105408187" id="_toc105408187"></a>

For the process to work accurately for GAM and Ad system to exchange information, user must follow the steps below in the following order:

1. Site creates the dfpadmins user in your GAM instance per the [Prerequisites ](ad-server-integration.md#\_toc105408178)above
2. Naviga personnel connects your Naviga Ad instance to your GAM instance
3. Administrative User configures Ad interface based on the setup instructions below.
4. User starts using GAM in campaigns or links existing campaigns to GAM external IDs.

## Configuring Naviga Ad <a href="#_toc105408189" id="_toc105408189"></a>

In the Ad system, navigate to the advertising menu Setup -> Admin -> Ad Server Integration Setup.

### Connection Setup <a href="#_toc105408190" id="_toc105408190"></a>

Click the connection setup node. Note that more than one GAM Server could be set up. Choose the server from the drop-down menu.

Click the “Yes” button to the field “Interface Enabled”.

* The interface enabled is set to yes to allow for the GAM and Naviga Ad system to communicate.
* The connection settings will be set up by Naviga Personnel.
* Authorization status must be green for GAM and the Ad system to communicate. If this field is red and indicating that authorization is not correct, the Ad system and GAM will not communicate the campaigns’ necessary information. Contact Naviga Support if your Authorization status is not green.
* The Ad Interface Premium Account: If set to yes, administrator must ensure that indeed the account is a premium account, otherwise the campaign lines and GAM communication will produce errors. A premium account in GAM allows for more capabilities than a regular account. For example, more capabilities in the materials and creative assistance. For more information, refer to the GAM help in Google system.

#### Connection Setup > Other Settings

<figure><img src="../../../../.gitbook/assets/image (714).png" alt=""><figcaption></figcaption></figure>

1. Do not use Brands when creating Advertisers: When checked, this box provides an option to ignore Brands when synching queue.
2. Advertiser / Agency Append Field: When creating/updating advertisers/agencies, use this field to store the Naviga ID. Options are Use External ID or Use Comments
3. Ad Unit Usage: This field has 4 options listed below. When we import in Ad Units from GAM we can bring in All Levels, just the top, etc for user selection when booking. The more levels we bring in, the more potential for slowness there will be, though there have been performance improvements and filtering that can be set up on the products, so that every order might not need to display all ad units.
   * Use all Ad Unit Levels
   * Top-Level Ad Units align with Products
   * 2nd Level Ad Units align with Products
   * 3rd Level Ad Units align with Products
4. Create missing advertisers in GAM: If set to yes, if the advertisers are not connected already in GAM, or if user is entering a new advertiser in Ad, this will allow the integration to create this advertiser in the format of AdvertiserID|BrandID in GAM. If this is set to No, the campaign information will fail to send to GAM if the Advertiser is new.
5. Create missing agencies in GAM: Like the advertiser’s field, this will allow the integration to create new agencies in GAM in the format of AgencyID|BrandID and communicate the impressions for the campaign line.
6. Default Campaign Team: The selection here will set the team on the campaign to what is selected here. For details on how to setup these values, please refer to the section below in Cross Reference Tables -> Teams.
7. Advertiser Prefix: When automatically creating a new Advertiser or Agency, this option will use this field to prefix the name used in GAM.
8. Advertiser Suffix: When automatically creating a new Advertiser or Agency, this option will use this field as a suffix to the name used in GAM. To append the Account ID from Naviga to the Customer Account Name in GAM, add {NAME\_ID} here.
9. Team Override: Some of our clients exist in a large, shared GAM instance where not ALL Ad Units are relevant to the products that are in their Naviga Ad system. To eliminate the clutter and system lag that bringing in unnecessary Ad Units would create, we allow this as a filter. The Team Override is a multi-select field which will limit the Advertisers and AdUnits that we import into the system. It will be limited to only those that these teams have access to.
10. Audience Segment Type(s): Options here are First and Select 3rd Party, first party only, or Select Third Party only
11. This allows you to list the select 3rd party Audience Segment ID's referenced above. The Data here must be in CSV format.
12. Campaign Name format: The default is \[Campaign Description] - (Naviga Ad: \[Campaign ID]), but there is now an additional option of \[Advertiser Name] - \[Campaign Description] - \[Start Date] - \[Campaign ID] - \[Product Group]. **Important Note** - GAM restricts this field to a 255 Character limit. Especially if you use the optional fields, there could be truncation.
13. Campaign Line Name Format - Default is \[Description] - (\[Line ID]), but you can override to \[Ad Unit] - \[Line ID]. Note: This field is subject to a 255 character limit, which may result in truncation
14. Date Format - The date format chosen will be applied to any dates that may be used in one of the name formats above (#12 or #13). Options are MM-dd-yyyy or yyyy-MM-dd

#### Workflow Settings / Status Code Settings <a href="#_toc105408196" id="_toc105408196"></a>

In versions Prior to 2023.1, this section was called Status Code Cross Reference, was in the "settings" node, and looked like this:

![](<../../../../.gitbook/assets/image (1170).png>)

In this section, Admins would determine if a given Campaign Status should Sync to GAM and what the GAM status should be for any given Naviga Ad Campagin Status.

Beginning in 2023.1, this section has been Re-labled "Workflow Settings," moved to the Connection Setup node, and looks like this:

<figure><img src="../../../../.gitbook/assets/image (111).png" alt=""><figcaption></figcaption></figure>

1. CAMPAIGN STATUS TO TRIGGER ORDER CREATION IN GAM: This is the minimum Campaign Status that will trigger Order (and Line Items) creation in GAM. Orders are created in a **DRAFT** status in GAM.
2. CAMPAIGN STATUS TO TRIGGER SUBMIT FOR APPROVAL IN GAM: This is the minimum Campaign Status that will trigger a **SUBMIT FOR APPROVAL** request to GAM. \***Note**\* When something is submitted for approval in GAM, it needs to be approved or disapproved in GAM before the API will allow us to make any additional updates, so be sure to test this in your test environment and understand how it works and if it will work for you to set something here. If you do not wish to approve campaigns inside of GAM, set this to the same status as #4 and it will essentially be ignored, or you can leave it blank.
3. SKIP INVENTORY CHECK WHEN SUBMITTING REQUEST FOR APPROVAL: If set to yes, the system will not check again for Inventory when the Campaign Status is updated to the Status set in #2 above.
4. CAMPAIGN STATUS TO TRIGGER APPROVAL IN GAM: This is the minimum Campaign Status that will trigger a request for APPROVAL to GAM.
5. SKIP INVENTORY CHECK WHEN SUBMITTING APPROVAL: If set to yes, the system will not check again for Inventory when the Campaign Status is updated to the Status set in #4 above.
6. OVERBOOK SPONSORSHIPS WHEN SUBMITTING APPROVAL: This setting is only taken into account when the order goes for approval. It first does the normal approval at the campaign level but if this option is selected, it does a 'reserve with overbook' at the line item level (just for sponsorship lines).
7. REQUEST LINE DELETION IN GAM WHEN LINE IS DELETED: This will send the request to GAM to delete a line if the line is deleted in Naviga Ad.

### Settings <a href="#_toc105408191" id="_toc105408191"></a>

Click the node "settings". Select the Ad Server ID at the top.

#### Profile Selection <a href="#_toc105408192" id="_toc105408192"></a>

Profiles allow you to create different configurations that can be applied to different products. You set your Profile Selection on the Product Setup after selecting the Ad Server for the product.

Create the new Profile ID, and description, or select an existing Profile.

{% hint style="info" %}
Once created and the following Settings have been saved, navigate to Setup -> Product Setup screen and scroll to the Ad Server section choose the Ad Server and profile to attach to the product.
{% endhint %}

#### Under Integration Settings section, these are the fields to fill out:

<figure><img src="../../../../.gitbook/assets/image (666).png" alt=""><figcaption></figcaption></figure>

* Auto-update 3rd party IDs: This field when checked as “Yes” allows the system to read each Creative on the associated line item, parses the description by underscores, takes the last value by underscore, and adds it to the list of 3rd party IDs associated with this line. This is to satisfy a need for users who need multiple 3rd party ids per line item, because the 3rd party ids are on the creative, and one-line item can have many creatives. So, in order to eliminate tedious and manual work for them to extract these, this feature allows the system to read the Creative Description, extract the 3rd party IDs and add them to the line items automatically each time the system retrieves actuals. **This assumes that the 3rd party ID is at the end of each Creative Description, and when broken by "\_", it is the last value.** This makes the integration process with the Gmail reports automatically match up and find the numbers.
* Allow Lines Without Ad Units: If checked as “Yes”, this allows the system to send line items without Ad Units to go to GAM.
* Time Zone Override: Choose the override value of the time zone to place on the orders integrating with GAM.
* Custom Field Source: When using UDF's for GAM Custom Fields, if this is set to Description, the system will pass the answer description to GAM instead of the Value.

#### Email Alerts <a href="#_toc105408194" id="_toc105408194"></a>

* Administrator should enter his email address here, to receive an alert, if the synch between Ad and GAM fails.
* Older Releases prior to 2021.2 Legacy Settings: Process Lines using 2018.3 Engine Cut-Off Date: Cut-off date for legacy users to process lines.

#### Data Sync Options <a href="#_toc105408195" id="_toc105408195"></a>

These are fields specified to write when creating a new order when checked or synched when the order is updated. Check the respective box for each field as needed. This flexibility is given to accomodate those sites who wish to do optimization in GAM directly. If you are frequently updating Targeting inside GAM for example, you would likely want to uncheck the "Overwrite on Update" column for Targeting items, otherwise you will risk overwriting what you did in GAM next time the ad is edited or sync'd inside Naviga Ad.

<figure><img src="../../../../.gitbook/assets/image (1214).png" alt=""><figcaption></figcaption></figure>

Also, note that if you re-save an order line, only that order line gets re-sent, not the entire campaign. To sync the entire campaign, select the edit option "Re-Sync to Ad Server" in the top right dropdown on the campaign header.

### Cross Reference Tables <a href="#_toc71270606" id="_toc71270606"></a>

These cross-reference tables allow for the mapping of key data between Ad and GAM. This data can be done for one or more Ad Server as needed.

Once the administrators set up the data in GAM, and the windows service is installed, these tables will be populated.

#### Advertisers <a href="#_toc71270607" id="_toc71270607"></a>

If starting this for the first time, you will see the Ad Server Advertiser Id and the Ad server Advertiser in this list and the Naviga ID will be blank. Once the Cross-reverence is completed, there will be a Naviga ID populated in the format of Advertiser ID | Brand ID

<figure><img src="../../../../.gitbook/assets/image (655).png" alt=""><figcaption></figcaption></figure>

User can at any time edit these mappings between Ad and GAM.

Click the pencil icon, and window will open to set or update the cross-reference. The Ad Server ID and Ad Server Advertiser name is not editable here. Below the Naviga ID click Search and Find the Advertiser in Naviga Ad. Then select the relevant brand from the brand dropdown and click save.

<figure><img src="../../../../.gitbook/assets/image (897).png" alt=""><figcaption></figcaption></figure>

For ease of setup, you can download this cross-reference into Excel and then fill in the missing data in the spreadsheet and then import it back in.

<figure><img src="../../../../.gitbook/assets/image (1666).png" alt=""><figcaption></figcaption></figure>

#### Agencies <a href="#_toc71270608" id="_toc71270608"></a>

Agencies operate similarly to advertisers in fields, except that Agencies don't have a Brand attached, so it is just the Naviga ID that is needed. Similar to Advertisers, you can download the spreadsheet and then re-upload with the Id's in there.

#### Traffickers <a href="#_toc71270609" id="_toc71270609"></a>

Traffickers in GAM correspond to the production controllers in the Ad system. Every campaign must contain a production controller. If the system is set to communicate with GAM, the campaign will not be sent to GAM unless the production controller has a valid mapping on this screen with GAM.

If the production controller name in the campaign header does not match a valid GAM mapping on the campaign entry screen, user will receive an alert message warning them.

To edit the trafficker information, click the edit hyperlink corresponding to the trafficker name on the setup screen.

<figure><img src="../../../../.gitbook/assets/image (977).png" alt=""><figcaption></figcaption></figure>

Choose the Ad production controller from the drop-down menu to be mapped to the GAM username and ID. The Ad production controller names in the drop-down menu are provided from the Ad User IDs. When you are finished, click the save button.

#### Teams <a href="#_toc71270610" id="_toc71270610"></a>

This node is for the choice of a default Team ID to use when creating new orders which flow into GAM.

Note that this feature can pull data from Ad Servers with the teams feature only if enabled by the admin of the Ad Server.

Navigate to the menu Setup -> Admin -> Ad Server Integration Setup -> Settings and you can choose a "Default Campaign Team" per Ad Server.

When creating a campaign using a product which is connected to this Ad Server, in the campaign header, under the tab “Other Information”, there is a new box for “Ad Server Teams”.

When creating a new campaign, the system will check the "Default Campaign Team" and assign to the default team.

For existing future campaigns, when you edit a campaign, the system will check the "Default Campaign Team". The Windows Service will send/update Campaign Team at the time of upload interval.

#### Sales Reps <a href="#_toc71270611" id="_toc71270611"></a>

The ID, Name and Role columns are the GAM data which the administrator creates in GAM. They are mapped to an Ad user ID. This can be edited to change the Ad user ID.

To edit, click the Edit hyperlink. Choose a sales rep from the drop down and save. The names in this drop-down menu are the Ad User IDs.

#### Ad Units/ Placements <a href="#_toc71270612" id="_toc71270612"></a>

Placements in GAM are a collection of Ad Units. For Example you might create a placement for All Ad Units in the Sports Section, or you might have a placement for all homepages across several websites. In Ad Server Integration Setup select the Placements node and click Save/Import All to bring your GAM Placements in to Naviga Ad to use in Booking.

![](<../../../../.gitbook/assets/image (386).png>)

Similarly, Ad Units will also be imported into Naviga Ad on the Ad Units node.

<figure><img src="../../../../.gitbook/assets/image (278).png" alt=""><figcaption></figcaption></figure>

What level of detail you see here will be dependent on what you set on the "Connection Setup" node on "Ad Unit Usage." If you selected "Use All Ad Unit Levels" then you will see all your nested levels displayed here. If you selected "Top Level Ad Units Align with Products" then here you will only see the Top level of Ad Units.

The Product Link that you see in here will be used when you book "Group Product" product types in Naviga Ad. You can create a group product called Run of Network for example. This Group product will include multiple "Standard Products." When GAM passes back actuals to Naviga Ad and says X impressions ran on Ad Unit 123 and Y impressions ran on Ad Unit 456, we use this mapping to determine what that means for revenue allocation purposes.

See [Product Setup](../product-setup/products/) and [Rate Setup](../product-setup/products/pricing-rules/) for additional information about filtering Ad units per product.

#### Custom Fields <a href="#_toc71270613" id="_toc71270613"></a>

In GAM's Global settings there are custom fields which can be created. Upon import into Naviga Ad, these fields can then be mapped to Naviga UDFs. The type of entry is defined as well, such as drop-down versus string entry versus a toggle field. Then when a user creates a campaign, and sets a Naviga UDF, those settings can also be set in GAM.

#### Creative & Native Templates

Click Save/Import All at the bottom of the screen to import in all the templates from your GAM server. You will see both SYSTEM\_DEFINED and USER\_DEFINED templates are imported in:

<figure><img src="../../../../.gitbook/assets/image (1225).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (1005).png" alt=""><figcaption></figcaption></figure>

On a digital material record, for the Native Format and the Custom Creative Template Creative Types, you will have a dropdown field for Ad Manager Template. Select your ad server from the line above and then select the template from the dropdown. At this time we are only supporting your USER\_DEFINED type templates as the other templates often have required fields that need to be filled in prior to being able to create the container record and that isn't something we are supporting at this time.

### Other Targeting Tables <a href="#_toc71270614" id="_toc71270614"></a>

#### Audience Segments <a href="#_toc71270615" id="_toc71270615"></a>

What is displayed in here will be dependent on your setting in the Connection Setup -> Other Settings for Audience (#10 & 11). If you selected only First Party, you will see first party Audience segments in here. Upon successful import of these segments into Naviga Ad they will be available for targeting in the Custom Targeting section of the GAM tab in order entry

<figure><img src="../../../../.gitbook/assets/image (872).png" alt=""><figcaption></figcaption></figure>

#### Key Value Targets <a href="#_toc71270616" id="_toc71270616"></a>

The screen displays the labels available for use, and some of which are not marked as already imported. If they are marked, then they are already available for use. Otherwise, click the button “Save/ Import All” to import them for your use from the GAM system. This will synchronize the values from GAM to Ad system and make them available for section.

<figure><img src="../../../../.gitbook/assets/image (1145).png" alt=""><figcaption></figcaption></figure>

Navigate to the menu Setup -> Product Setup and choose a digital product from the drop down-menu. Click on the node “Product Details” and scroll to the section labeled “Ad Server Settings” -> “Key Target Filters”.

<figure><img src="../../../../.gitbook/assets/image (608).png" alt=""><figcaption></figcaption></figure>

This area displays all available values and you can leave as is to allow users to view all key values in the system for this product. Or you can narrow down the values to the applicable ones by highlighting them on the left available box and clicking the right arrows to move them to the box labeled “Restrict Only to these Key Targets”. This will limit the section values available in the line item entry screen to these values.

Click the “Save” button when finished.

Click the node “Sections”. This step allows for the default key target values to display in the section of this product in a campaign line entry screen.

<figure><img src="../../../../.gitbook/assets/image (1622).png" alt=""><figcaption></figcaption></figure>

Choose the key target from the drop down, and choose the condition being “is” or “is not”, and choose the values matching the condition and click the + sign. You can choose more than one key target value. Click the “Save” button when finished.

Navigate to the campaign entry screen and add a new line for this product. Click the section “Key Values” and you will see the default key value here for the section, if configured to do so, and you will also be able to add additional key values as allowed by the product setup. Click the + sign to add.

When users are adjusting targeting on a campaign, they can create a new "Value" in the custom targeting section if the Key is of a "FREEFORM" type. You can see if your Target Keys are freeform in Setup -> Admin -> Ad Server Integration Setup, Key/Value Targets node.  For "Predefined" types, the above Create New Values button will be grayed out.

There is a new button in the Custom Targeting shutter:\


<figure><img src="../../../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

Important caveat on this - GAM will not have inventory available for this new value for about 30 days, so any usage of this new value will require that the user selecting it can oversell Google Inventory.  To ensure that the user has permission, navigate to Group Security for Advertising and the Google Ad Manager Inventory section.  The permission will need to be to Allow Overselling, or to Warn, but allow.  IF the user is set to "Do NOT allow overselling" then they won't be able to save the line.\
![](<../../../../.gitbook/assets/image (26).png>)

#### Labels <a href="#_toc71270617" id="_toc71270617"></a>

Click to Save/Import Labels as configured in GAM. These will then be accessible on the Campaign line entry, GAM tab under the heading "labels"

#### Native Style <a href="#_toc71270618" id="_toc71270618"></a>

User can import their own native styles for the creative materials. This allows you to choose these native styles which you created in an outside system to import them now and use later in the campaign line item entry.

Click “Save/ Import All”. This will import the native styles as a creative type to choose from in the campaign line item entry.

#### Locations <a href="#_toc71270619" id="_toc71270619"></a>

Geo-targeting Locations can be imported in from GAM. This will take several minutes to complete the import. After Importing, they can be accessed on campaign lines in the geography section.

#### Device Categories <a href="#_toc71270620" id="_toc71270620"></a>

Current Options are:

<figure><img src="../../../../.gitbook/assets/image (908).png" alt=""><figcaption></figcaption></figure>

Like other fields, once imported they will be available in Campaign Entry for Targeting

#### Device Capabilities <a href="#_toc71270621" id="_toc71270621"></a>

Current Options are:

<figure><img src="../../../../.gitbook/assets/image (737).png" alt=""><figcaption></figcaption></figure>

Like other fields, once imported they will be available in Campaign Entry for Targeting

#### Bandwidth <a href="#_toc71270622" id="_toc71270622"></a>

These will also be available on a Campaign Line for Targeting:

<figure><img src="../../../../.gitbook/assets/image (205).png" alt=""><figcaption></figcaption></figure>

#### Mobile Carriers <a href="#_toc71270623" id="_toc71270623"></a>

Upon Import, these will also be available on a Campaign Line for Targeting

#### Browsers <a href="#_toc71270624" id="_toc71270624"></a>

Upon Import, these will also be available on a Campaign Line for Targeting

#### Device Manufacturers <a href="#_toc71270625" id="_toc71270625"></a>

Upon Import, these will also be available on a Campaign Line for Targeting

#### Operating systems <a href="#_toc71270626" id="_toc71270626"></a>

Upon Import, these will also be available on a Campaign Line for Targeting

{% hint style="info" %}
On all of these targeting settings, once established, they can be updated nightly in the background, so you don't need to come into the setup all the time to refresh these.
{% endhint %}

### Other <a href="#_toc71270627" id="_toc71270627"></a>

The two topics below are very similar conceptually. GAM has had "Targeting Presets" in their system for ages, but until recent years they didn't actually expose that in their API so we weren't able to offer them to you directly.

To give you the same end result, we created the concept of Targeting Templates. If you are just setting up the system for the first time, you will use the "Targeting Presets" concept. If you are already using Templates, you should switch over to using presets.

#### Targeting Presets <a href="#_toc71270628" id="_toc71270628"></a>

GAM has a sophisticated system of targeting by all sorts of criteria. This could include things like country, region, language, device and other factors. Inside GAM, define as many Targeting Presets as desired.

Inside Naviga Ad's Ad Server Integration Setup, import those Presents into Naviga Ad so that they can be used on campaigns.

In Campaign Entry, select the desired preset and it will apply the targeting that is linked to that preset. The Targeting Preset dropdown will clear out once the targeting has been applied to allow more more selections. You can layer as many presets as is relevant to the order.

#### Targeting Templates <a href="#_toc71270629" id="_toc71270629"></a>

Targeting templates are deprecated now that the GAM API gives us access to use Presets. For historical purposes though, and for those still on older versions, here are the steps to use Templates:

1. Setup a House Advertiser in GAM
2. In the External ID for this Advertiser in GAM – enter ELAN\_TEMPLATES
3. Enter one or more Lines in GAM against this advertiser, including the targeting you would want included in your template – that will serve as TARGETING TEMPLATE lines
4. Go to this menu path: Advertising module -> Setup menu -> Admin -> GAM Integration Setup -> Targeting Templates node.
5. Import the items you want to use – give them Shorthand IDs and Descriptions

In Campaign Entry – if you select one of these – the Ad system will copy the targeting information from the Template line in GAM onto the new line as we create it.

You can use these templates to setup complex targeting criteria, using custom tags, etc.

## Additional Related Concepts <a href="#_toc105408221" id="_toc105408221"></a>

### Ad Types <a href="#_toc105408221" id="_toc105408221"></a>

Navigate to the menu Setup menu -> Advertising Setup -> Ad Types. Ad types that you wish to send to GAM must be matched on this screen to a GAM cost type and line item type. So, users can create as many ad types as needed in Ad and map them to a corresponding GAM types.

The Ad system’s code allows for accommodation of ad types that do not quite match any counterpart in GAM. For example, in Google, the concept of flat fee ad type does not exist, while it exists and is used in Ad. If the user wants to send these lines to Google it is recommended that he setup an ad type in Ad as an FF (Flat Fee) type, with a GAM line type of sponsorship and a GAM cost type of CPD (Cost per Day). Ad will then create a CPD line in GAM dividing the total flat fee by the number of days on the line.

The ad type is the first field user chooses on the campaign line item entry screen.

If the GAM line type is set to sponsorship, network or house, the Ad system then sets the primary delivery goal to 100% in GAM.

If the GAM Line Type is set to sponsorship, Ad places the estimated quantity into the contracted units bought field in GAM.

### External Campaign ID <a href="#_toc105408227" id="_toc105408227"></a>

If user already has GAM campaign line items in existence and Ad campaigns matching the GAM campaigns, but they are not connected, user can retrieve the Line Item ID of the GAM campaign and manually enter it in the Ad campaign entry screen.

<figure><img src="../../../../.gitbook/assets/image (584).png" alt=""><figcaption></figcaption></figure>

Once Connected the field will be read-only on the line:

<figure><img src="../../../../.gitbook/assets/image (1626).png" alt=""><figcaption></figcaption></figure>

Once connected, if user clicks view in GAM link by the Google Line ID, user can be directed to access the GAM account if user has a login

<figure><img src="../../../../.gitbook/assets/image (807).png" alt=""><figcaption></figcaption></figure>

### &#x20;<a href="#_toc105408232" id="_toc105408232"></a>

### &#x20;<a href="#_toc105408233" id="_toc105408233"></a>
