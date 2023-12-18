---
description: >-
  This document explains how users can enter a campaign using the full and quick
  entry methods as well as Booking Wizard.
---

# Creating Campaigns

## Campaign Header Entry <a href="#_toc531451673" id="_toc531451673"></a>

Navigate Campaigns -> Enter a new campaign to a enter new campaign from the Campaigns menu. Or Navigate to Campaigns -> Edit a Campaign to make changes to an existing campaign. For someone who does not have access to create or edit campaigns, you can give them a read-only view of the details with Campaigns -> Campaign Inquiry.

{% embed url="https://app.supademo.com/demo/2MsbYFKIXYB9ITMa80pwg" fullWidth="true" %}

For a new campaign, enter a description, advertiser ID from the drop-down, choose the brand, and the agency and billing information default into the respective fields according to the setup of the brand.

![](<../../../../.gitbook/assets/1 (69).png>)

Select the product group from the drop-down. Based on your User Security, you might have a pre-filled default product group. Group Security can limit the Product Groups that you have access to.

You can also choose the order contact, production controller, and campaign manager from the list.

{% hint style="info" %}
The **order contact** will also be the person who receives a renewal notice if you choose to email renewal notices. This field may or may not be required based on your Group Security.

The **production controller** list will be users in the system who are marked as Production Controllers in User Security -> Advertising -> User Settings. This might be pre-filled based on Brand Setup.

The **campaign manager** contains all the users which are setup in the Naviga Ad system. These are optional values but can be used for reporting purposes across the application.. This might be pre-filled based on Brand Setup.
{% endhint %}

Enter the start and end dates of the campaigns. A single campaign can run for up to 2 years and can contain multiple order lines. (2 year limit is set by Google Ad Manager)

#### Run Until Cancel

You can click “Run until cancel” button if you’d like the campaign to run indefinitely. The purpose of this flag is to allow you to filter on this campaign in the expiring campaigns list so that you can easily find and renew it when this campaign expires. The run until cancel is also known as “TFN” and “Till Forbid”. Even a TFN ad requires Start/End Dates for this campaign. See [Expiring Campaigns](../expiring-campaigns.md#\_toc51353214) for more details

You can choose a foreign currency from the currency drop-down or leave blank to use the local currency instead. (Group security may prevent you from changing the currency). Note that only the Ratecards which match the currency will display when it’s time to enter the line information.

If there is a default discount setup on the brand maintenance screen, it defaults in the Default Discount field. You can override this value as you wish or leave blank. This value will automatically be applied to the total order amount.

If the client has a credit card on file and would like to use this credit card during the billing process, then choose the card from the drop-down menu. You can add new cards from the button “Manage Cards on File”. This can be left blank. This is not the same as a prepayment. When selecting an Auto-Pay method, the card will be charged during the invoicing process for the amount that is being billed at that time.

If the client has a contract setup already, the contract defaults in the drop-down, but you can remove it by selecting the blank option in the drop-down menu. If the contract field is populated, the contract discount(s) will be applied to the order. If left blank, then no discount from the contract is applied.

Choose the status of the order from the drop-down. These values are pre-setup in the order status setup menu. The status can be edited at any point to any other value. Once in the CO confirmed status, you cannot change it back to Q or R status. But the campaign can be cancelled at any time.

<figure><img src="../../../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

To tie this order to a marketing campaign, start typing partial letters of the marketing campaigns setup in the CRM module and a list displays to choose from. This is an optional field which is reflected in reports across the application.

The Industry code is the PIB/ Category code setup for the brand on the brand maintenance screen which you can also edit in this screen.

The Sensitivity code, if entered, will let Naviga Plan know if this is a sensitive topic. Typically used with Political Ads, Alcohol, Marijuana ads, etc., so that Pagination users can use special handling to ensure it is on a page with appropriate content & other ads.

Default Artwork type: This will affect ad deadlines in the event that you have different close dates for a camera ready ad vs one with ad designed by an inhouse or 3rd party artist/designer.  Artwork type can be set here as a default for the campaign, and it can also be overwritten on the order line.

Enter a P.O. number which is optional for purchase order number. If the P.O. number field is setup in the Advertising Setup to be mandatory, you won’t be able to confirm the campaign without filling in the value in this field.

Customer Ref. No. and External Campaign ID fields are optional fields if you want to link these external references to the campaign.

The Invoice Form Detail Level gives you multiple options of how detailed you’d like the invoice to be when the customer receives it:

* Show Each Line - No Costs: The invoice reflects each line item on the campaign but without an amount for each line.
* Show only the Description and Total Price: The invoice reflects the order description and the total campaign amount but no line details.
* Show Each Line - Including Costs: The invoice reflects each line item with details and cost of each item and the total amount of the campaign.

{% hint style="info" %}
The Invoice Form detail can be set on the Advertiser if the advertiser always wants their invoices to be shown in a certain way.
{% endhint %}

Marketing Content Template: Choose the template from the drop-down menu. The template is previously setup under the menu Setup -> Templates -> Marketing Content Templates. This field is optional. The Marketing Content Template is an HTML marketing message which can be displayed on the order proposal / confirmation.

The following will only be shown if you are licensed to use the Advertiser Portal:

* Signature Template: This field is also an optional field with a list of templates to choose from as previously setup in the menu Setup -> Templates -> Order Confirmation Email Templates -> Campaign email templates node.
* Ready to Sign: If this field is checked as “Yes”, and your client has access to the Portal, the client can then sign the proposal approval and the campaign will be marked as signature received.
* The client will ONLY see the Signature Template you chose above if you do not email them an actual proposal. In most cases, the user will email the client a proposal and that email will prompt them to log into the portal to sign the proposal. That emailed proposal will override whatever is set on the signature template field from the campaign header.

When finished click on “Save”. Depending upon your user security, you may be directed to Quick Line Entry, Full Line Entry, or you may be prompted to choose which you prefer to use for this campaign.

![](<../../../../.gitbook/assets/3 (58).png>)

## Full Line Entry <a href="#_toc119674076" id="_toc119674076"></a>

In the center of the Line Items screen, you must choose a product and ad type and then click “Full Line Entry”. In this case, choose a digital product.

<figure><img src="../../../../.gitbook/assets/image (344).png" alt=""><figcaption></figcaption></figure>

The line item entry screen displays the “Pricing Details” tab which contains items relevant to the order and the selected ad type, such as the ratecard, section, positions, size, discount rate, and estimated impressions. (if you choose a flat rate ad type you will see Share of Voice instead of impressions; if you choose CPC, you will see clicks; if you choose CPD you will see days.)

![](<../../../../.gitbook/assets/4 (49).png>)

The start and end dates as well as the Proportion Values are in the lower section of the screen under Line Details. Dates will default in based on the dates of the campaign. These can be edited to start later or end earlier than the campaign, but they must remain within the date range of the overall campaign.

The 3rd and 4th Party related fields are under the “Tracking Services” tab.

Note that the contract, if carried over from the campaign header, can apply its discount to the line or if you remove it will not be applied to this line item.

If the discount applies, it appears under the Adjustments tab. If not, and you have discounts setup attached to the Ratecard, these will appear and be applied to the amounts.

The tab “Other” contain fields which apply to production platforms such as social media sites where the ad is placed.

The tab “Creatives/ Materials” allow you to choose an existing material(s) or create a new one to attach to this line. You can attach various components to the material such as files, or links as well as allowing for a preview of the images attached to this line item.

You can enter relevant production notes in the next tab for the production team to review.

If your Group Security allows, you can also override the Salesrep for this line item in the “Rep Assignments” tab and then click “Override Sales Reps” to change it to “Yes”. Then enter the sales rep from the drop-down menu. You can enter more than one rep each with his own commission percentage. On the right panel, the system displays the campaign rep, brand rep and original rep before your replacement took place.

The “Google AD Manager” tab applies to any line items that are being sent to GAM. The screen allows you to enter the fields details related to GAM as per the Ad Server setup for this website.

The “User Defined Fields” tab contains all the necessary UDFs if applicable to user’s campaign. At any point, user can check the Ad Server Inventory, position inventory or product inventory by clicking the respective buttons. Once all inventory is cleared, click “Add Line”.

### Other Information <a href="#_toc119674077" id="_toc119674077"></a>

Once the line is added, navigate to the “Other Information” tab on the campaign header details screen.

The screen allows you to choose various information about the order. For example, whether the I.O. was received or not. Also, it displays who entered the order and when the order was entered.

It displays the rep on the campaign, original rep who should be the same as the original rep if no changes have been made. It also displays the order’s brand rep as setup in the brand maintenance.

It displays any GAM information as applicable. It also allows you to mark this campaign as a space holder. If you check the button “This is a Space Holder Ad”, and its value is “Yes”, then you can attribute other line items to this campaign. A Spaceholder Ad might also be called a Ganged Ad or a Parent/Child Ad. Sometimes it is called a Co-op ad, but Co-op is something different in Naviga Ad. To us a Co-op is a split bill between two or more parties.

### Enter Order with Zones <a href="#_toc21458138" id="_toc21458138"></a>

Navigate to the menu Campaigns -> Enter a New Campaign to enter a new one using a product with [Preprint Zones](../../setup/product-setup/products/issue-based-setup/preprint-zones-zone-configration.md) setup. In the line item entry screen, after entering all the line details, click the tab “Zones”. From here you can either us the Grid or the map to select Zones.

<figure><img src="../../../../.gitbook/assets/image (1523).png" alt=""><figcaption></figcaption></figure>

The highest level Zone groups will display

<figure><img src="../../../../.gitbook/assets/image (274).png" alt=""><figcaption></figcaption></figure>

Click on a sub-group to drill down further or select the whole zone

<figure><img src="../../../../.gitbook/assets/image (406).png" alt=""><figcaption></figcaption></figure>

At any time, click on the breadcrumb trail at the top to jump back to a prior group.

Note that the Zones and Zone Groups display where you can select the zone dimensions such as Subscribers and Retail. The totals automatically are updated as you click the boxes.

Click the button “Use Map to Select Zones” if you would like to do so. The map appears with a suggestion of location based on the advertiser's address. You can enter the location you wish or change the radius as you wish.

<figure><img src="../../../../.gitbook/assets/image (1532).png" alt=""><figcaption></figcaption></figure>

Click “Get Postal Codes” and the screen displays a list of all the area’s postal codes. Any postal code that matches a zone configured in Product setup will automatically be checked. (note in the screenshot that the bottom postal code in my area is not a delivery zone with counts supplied in the Subscriber/non-Subscriber/Retail columns.)

Check/uncheck the box(es) for codes you’d like to add/remove and click the no buttons at the top to turn the desired columns to "yes" to include those counts. Then click the button “Use Selected Zones”. This adds the selected zones to the order.

<figure><img src="../../../../.gitbook/assets/image (652).png" alt=""><figcaption></figcaption></figure>

Click “Add Line” to sav the line to the campaign.

The line displays

<figure><img src="../../../../.gitbook/assets/image (1450).png" alt=""><figcaption></figcaption></figure>

## Quick Line Entry <a href="#_toc531451674" id="_toc531451674"></a>

Quick Entry tool uses packages with ratecards which has previously been setup with all details of a line, even with GAM Targeting and other details as setup on the ratecard line. Once user chooses the ratecard line, these values automatically populate the line item fields on the campaign entry screen. This simplifies the line item entry process removing any additional need for user to enter numerous values in all different types of fields every time user enters a new line item. User is still allowed to edit the line items details to fit the specific needs of the campaign and the advertiser.

{% hint style="info" %}
Quick Line Entry is only for Digital and Display type ads. Classified Ads must use either the Booking Wizard or Full Line Entry.
{% endhint %}

Create a new campaign and click on the “Save” button on the campaign header. In the pop-up, click on “Quick Entry” button. You can also use the "Quick Line Entry" button from any existing campaign under the Line Items node.

You can then select a package, copy another campaign, or select a Product/Ad Type/Rateline combination:

<figure><img src="../../../../.gitbook/assets/image (709).png" alt=""><figcaption></figcaption></figure>

You can edit the line items if the package is setup to allow editing or deleting items.

Or you can select a product from the drop-down menu and a ratecard line.

<figure><img src="../../../../.gitbook/assets/image (1037).png" alt=""><figcaption></figcaption></figure>

Note that once you choose the ratecard line, the fields are auto-populated with the values from the ratecard. You can still change the fields’ values in the line as you see fit before you add the line to the campaign.

{% hint style="info" %}
Note that if you are connected to GAM, the system recognizes if you are considering inventory from the Naviga Ad side or from GAM side and will display the Qty with a note indicating whether the line is inventoried.
{% endhint %}

Click on the button “Check Line Inventory” at the bottom of this screen and the system lets you know if there is available inventory or not. Once the inventory is cleared, you can click “Create Lines” to add the line item. If you click Create Lines without having done the inventory check, the system will still check inventory and will prevent the user from proceeding if the inventory is not available (depending upon permissions, user _may_ still be able to proceed)

Note that there is a Discount percentage button which overrides the discount on the campaign header and is applied to each line item you are adding.

Hover over the Qty field inventory mark and note that the system displays inventory available broken by month if the line is running for multiple months.

### Quick Entry for a Print Ad Type <a href="#_toc119674079" id="_toc119674079"></a>

Quick Line Entry of print type product allows user to enter multi-select dates as end date where it fits within the campaign dates. Note that classified ads are not allowed in quick entry.

Navigate to a campaign and choose the “Quick Line Entry” option. Choose a print product from the “Select a Product” drop-down menu. Choose the ad type and rate line from the drop-down menus.

Note that the Start/ End field contains a button “Multi-select” to choose the issues for the product.

Note that the issues available within the campaign date range are there to be chosen.

Choose the issues and click Apply. The lines are added to the list

<figure><img src="../../../../.gitbook/assets/image (857).png" alt=""><figcaption></figcaption></figure>

Once you click “Create Lines”, the system consolidates the issues into the one line if the setup allows for not splitting lines.

## Booking Wizard <a href="#_toc98168271" id="_toc98168271"></a>

Booking Wizard order entry method allows for bulk entry across multiple products for classified, both print and digital classified products.

Please note that Booking Wizard doesn’t support CPM Print or Digital entry. CPM is supported through the traditional Quick Line Entry or Full Line Entry methods.

There are three booking wizard options to choose from. See Details below or check out our Webinar on the topic:

{% embed url="https://dev.navigahub.com/mothership/resources/videos/BookingWizardWebinar_2022-07-27.mp4" %}

### Template Based Classified Ad

In Campaign Line Entry screen, click the “Booking Wizard” icon and then choose “Build a Template-Based Classified Ad”.

![](<../../../../.gitbook/assets/8 (3).png>)

Click Continue.

The Classified Ad pop-up screen displays from which you can use the Start Date of the Ad, the category tree, category, package or product(s). In the popup, choose the dates you wish to include.

<figure><img src="../../../../.gitbook/assets/image (192).png" alt=""><figcaption></figcaption></figure>

Apply in this screen and then click next to continue

Next step is the Category Metadata and this will change based on the category tree and/or category chosen in the first step. One or more of these metadata fields will be utilized to create the text of the ad. Depending on setup some of the fields might be used to trigger automatic charges. For example, if you upload a graphic like an attention getter or border, you may automatically be charged a fee; or if you selected an online upsell like OwnLocal or Recruitology in the metadata, those fees might be added, and that metadata might also be used to trigger the feed to send that listing to those third party sites.

Click next to continue to template selection.

<figure><img src="../../../../.gitbook/assets/image (718).png" alt=""><figcaption></figcaption></figure>

Depening on your setup, you might have one or more styles to choose from. The rate that will be applied is tied to the setup in this workflow so that you can choose good/better/best templates and automatically receive good/better/best pricing. Booking Wizard option 1 rates can be based on standard product rates or they could be based on Product Group Rates. See [Rate setup](../../setup/product-setup/products/pricing-rules/) for more information on setting up rates.

You may see an example preview of the style in here if your administrator created one.

The templates can be HTML-based or InDesign Based.

The system will create one or more versions of the material, as necessary to accomodate the column configuration of the products you are booking in. In this example, there are two versions because of of the products has a 5-column legal section and the other has a 6-column section:

<figure><img src="../../../../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure>

HTML-based ads can be edited in an editor window. InDesign templates cannot be edited by the end user in the browser. Click "Edit Template Text" in the top right to open the editor

<figure><img src="../../../../.gitbook/assets/image (701).png" alt=""><figcaption></figcaption></figure>

After applying any manual adjustments, click next and continue to the adjustments tab. Automatic adjustments based on the metadata entered will be displayed here as read only and you can also manually add additional surcharges and discounts at either the product or product group level.

Click next and you will see the Price Breakdown for each issue in the package

<figure><img src="../../../../.gitbook/assets/image (591).png" alt=""><figcaption></figcaption></figure>

Use the fields at the top to add a % discount across the whole campaign, or select/deselect a contract.

Click next to be taken to the final step in the wizard. This summarizes the pricing of the campaign, including tax, where applicable. There is a link on the "Total Amount Due" field where you can override the bottom line price of the campaign

<figure><img src="../../../../.gitbook/assets/image (499).png" alt=""><figcaption></figcaption></figure>

This example order is $170.68. I could override the price to, say $150 if that was the negotiated price that it was sold for. If this campaign is in a reserved or confirmed status, the "take prepayment" button will be enabled and i can optionally take a prepayment at this time.

### Compose or Upload a Classified Ad

Option #2 of the Booking wizard is for those sites who prefer to create the ad manually in a text editor, rather than using the template.

This option requires Product Group Ratecards to be created. (See [Product Group RateCards](../../setup/product-setup/products/pricing-rules/#group-rate-cards) for Setup)

Click “Booking Wizard” and choose the second option “Compose or Upload a Classified Ad” then click “Continue”.

![](<../../../../.gitbook/assets/9 (8).png>)

The pop-up screen for the Classified Ad displays.

<figure><img src="../../../../.gitbook/assets/image (345).png" alt=""><figcaption></figcaption></figure>

You can choose a category tree. Choose the Print Rate Line and/ or Digital Rate Line from the drop-down buttons.

You have the choice of a package if applicable, or select one or more products.

{% hint style="danger" %}
Since you are manually creating the material in this workflow, your column configuration must be the same between products! If you have products that do not share a column size, you cannot create them together using booking option 2. You would need to do them separately. You can have more than one booking wizard package on a single campaign if necessary.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/image (1620).png" alt=""><figcaption></figcaption></figure>

Category Metadata may or may not be necessary in this workflow. If you are using metadata to create surcharges and trigger feeds to go out for digital upsells, then you will still need to enter that data. Likewise if your digital orders are using the metadata to display the ad text online, you will still need to enter the metadata. If you are only using it to generate the text of the print ad via template, then you can likely skip it in this workflow.

Next, create the material or you can pickup an existing material

<figure><img src="../../../../.gitbook/assets/image (1253).png" alt=""><figcaption></figcaption></figure>

The default material type is listing text. This will enable the text editor where you can type or copy and paste the ad text into the editor.

{% hint style="info" %}
To control the font sizes viewed in line entry, these can be defined in the menu Setup -> Advertising Setup -> System Parameters in the fonts section. You can also choose to only allow custom fonts and provide Naviga Support with the fonts you would like to be used.
{% endhint %}

Change the Material Type to Listing Display if the client has supplied a pdf for the material and you would like to upload it. If you select Listing Display as the Material Type, the editor window will disappear.

Click next to continue to Adjustments. You can choose an option of the adjustment for the product or for the group. Choose one or both as applicable and then click the + sign and enter the data.

You can also click “Check Incentives” and apply existing incentives.

Once you reach the final tab, you can check the “Take Prepayment” or uncheck it. If you check it, the system displays the payment screen where you can process the check or credit card payment.

The result is multiple lines filled in with details of the order across multiple products.

### <mark style="color:blue;">Book a Display Ad</mark>

This option allows you to book a classified display ad across multiple products in bulk. Click this option from the Booking Wizard.

The pop-up screen allows you to enter the Start date, the Product Group Rate for both print and digital as well as selecting one or multiple individual products using the checkboxes.

{% hint style="info" %}
Note - Like option 2, this workflow requires the use of [Group Rate Cards](../../setup/product-setup/products/pricing-rules/#group-rate-cards).
{% endhint %}

You can also choose Group Section and Group Position if you have them setup in the Product Group Ratecards screen.

<figure><img src="../../../../.gitbook/assets/image (719).png" alt=""><figcaption></figcaption></figure>

If the rate line is for a Col x In (or mm or cm) type, you will see the columns and inches displayed:

<figure><img src="../../../../.gitbook/assets/image (1038).png" alt=""><figcaption></figcaption></figure>

Like the other Wizard options, the cross product buy pop up screen allows you to enter the specific day filter where you can choose particular days to run the ad or leave blank to include all days. It also allows you to enter Issue Count for the number of issues to place the ad for all print products. Also, you can enter the duration of the months for the ad to run in the digital products. Click Apply.

If this is a class display running in the classified section, be sure to select a category tree and category on the next page so that the ad can be placed in the correct Classification. Depending upon your workflows, you may or may not need to fill in the metadata fields for the Classified Display ads.

Next step is Material. Like other display ads in Full Line Entry, the Materials can be added here or they can be added later. In this type of ad the size comes from what you entered in the first step, so actually receiving the material is not yet required. The ad might be created later by a designer or it might be coming in as ready artwork from the advertiser.

Price Breakdown tab is just a little different from the other options. This workflow also allows you to assign the material to specific issues, only if you created material in the previous step.

<figure><img src="../../../../.gitbook/assets/image (208).png" alt=""><figcaption></figcaption></figure>

Proceed by clicking Next to go through the remaining screens and the system displays the price.

## Notes on All Booking Wizard Options

Note that in every case above, once the lines are saved to the campaign, the system lists the Line ID as well as the Line Group ID.

<figure><img src="../../../../.gitbook/assets/image (1036).png" alt=""><figcaption></figcaption></figure>

Depending on the Campaign Status and System Configuration, the hyperlink to the Line ID or the Line Group ID will either open up the individual line or re-open the booking wizard. Navigate to Setup -> Advertising Setup -> System Parameters. Line 15 displays what your cut-off is for opening in Wizard or Full Line Entry. Invoicing Started is the default, but you can change it to behave differently in your system.

<figure><img src="../../../../.gitbook/assets/image (984).png" alt=""><figcaption></figcaption></figure>

Some notes on Incentives and booking wizard ads:

* If there are any incentives applied to the lines, and you re-open the campaign in the booking wizard, the incentives will be removed and the user must re-check incentives to validate that they are still elegible after any line editing is complete.
* If there is already one or more lines on the campaign, and you add a booking wizard line to add additional lines to the campaign, you will not see the option to check incentives in the booking wizard. The incentives at that point would have to be checked on the campaign line items screen because incentives are meant to be evaluated across a whole campaign and not just on some of the lines.

### Affidavit Entry <a href="#_toc119674082" id="_toc119674082"></a>

Note that you can enter an affidavit on a line item using the Affidavit button. The Booking Wizard Entry screen displays the “Affidavit” tab upon choosing any of the options to enter a line item, classified template or classified non template or display. Click that button and enter the details. The system saves the information on the line item.

Note that Affidavits are generated by line / issue and cannot be reconciled backwards to the Booking Wizard once generated.

### Bottom Line Overrides in Booking Wizard with Uneven Break Out Rates Placed on Last Insertion of Group <a href="#_toc119674081" id="_toc119674081"></a>

When user applies a bottom line override in Booking Wizard or Package rates which don’t break out evenly, the override amount will be spread equitably across the issues. This can vary by adjusting the rate first (up or down).

Navigate to create a campaign using the Booking Wizard with multiple lines.

![](<../../../../.gitbook/assets/10 (24).png>)

Click

If you click the hyperlink to the lines again before confirming the campaign, the system alerts you to the override value and that it will remove it.

![](<../../../../.gitbook/assets/13 (2).png>)

You can then proceed to keep the amounts or change them.

Another Example is as follows with formulae applied in red.

![](<../../../../.gitbook/assets/14 (14).png>)

This is an example of 4 insertions/ issues with the original rate being $5400 for all 4 issues and an override rate of $5333.37.

## My orders Quick Entry

Navigate to the menu Campaigns -> My orders Quick Entry.

<figure><img src="../../../../.gitbook/assets/image (705).png" alt=""><figcaption></figcaption></figure>

By default, when navigating to this page, you will see all campaign lines that you entered "today" though you can change the start date to see lines you entered in the past. You cannot change the end date to tomorrow and see what you are going to get done tomorrow....sorry! But you can set the end date to something earlier and see all the ads that you created, say, last week.

There are 4 booking options in here as well. Each option is designed to ask minimal information to populate the campaign header with what is required without seeing all the options of regular campaign entry

1.  New Single Line order - after filling in the basic info you will be taken to full line entry for a single product.

    <figure><img src="../../../../.gitbook/assets/image (724).png" alt=""><figcaption></figcaption></figure>
2.  New Multi-Line order - After filling in the basics, you will be taken to Quick Line Entry

    <figure><img src="../../../../.gitbook/assets/image (314).png" alt=""><figcaption></figcaption></figure>
3.  New Classified Package order - After filling in the basics you will be taken to the booking wizard for whichever booking type you selected on the header.

    <figure><img src="../../../../.gitbook/assets/image (722).png" alt=""><figcaption></figcaption></figure>
4. Full Campaign Entry - This is a short cut to Campaigns -> Enter a new campaign

## Edit Campaign Header Options <a href="#_toc119674083" id="_toc119674083"></a>

The drop-down menu on the top right of the campaign header screen allows you to perform some functions to edit the campaign information. The functions you see on your dropdown may be limited based on your Group Security Permissions

<figure><img src="../../../../.gitbook/assets/image (338).png" alt=""><figcaption></figcaption></figure>

### Cancel Campaign

This is a full cancel / credit campaign and should only be used if the campaign was entered in error and must be completely cancelled. if it has already been Invoiced, then the invoice should be credited.

If it is not your intention to fully cancel and credit the entire campaign, then do not use this option. Instead you might want to put a credit on a line if only one issue ran in error. Or perhaps a future issue is being cancelled or changed for another date. Those corrections can be done on the line item without cancelling the entire campaign.

### Change Advertiser <a href="#_toc119674084" id="_toc119674084"></a>

This feature allows user to change the advertiser on a campaign from the campaign header edit options where the advertiser is locked out and disabled on a campaign based on status. This feature is not allowed on advertisers with credit stop, or billed campaigns or where a prepayment has been applied. User will receive warnings if there are conditions which should be considered, such as contracts applying to the client or if campaigns have gone to third party interfaces.

Navigate to create a new campaign in the Reserved status.

![](<../../../../.gitbook/assets/15 (7).png>)

Note that the Advertiser ID and Name fields are greyed out and can no longer be changed from the campaign header. Instead, in the Edit drop-down options, use “Change Advertiser”.

![](<../../../../.gitbook/assets/16 (9).png>)

In the pop-up screen, choose the advertiser and brand to replace the existing ones on the campaign.

The system lists any errors which would stop you from changing the advertiser, such as credit stops or other limitations. It’ll also list warnings which are for information purposes and will allow you to proceed with the change.

Edit the line item once the new advertiser has been changed and note:

1. The price on the campaign remains the same.
2. The product remains the same.
3. The Material displays as belonging to the original advertiser.

![](<../../../../.gitbook/assets/17 (1).png>)

Prepay the campaign in the Invoice & Payments tab. This could be a partial prepayment. Then attempt to change Advertiser again.

![](<../../../../.gitbook/assets/18 (4).png>)

The pop-up screen displays the Error Exception of the prepayment being applied as a condition to prevent the change of advertiser. The Save button is disabled. In this case, you must remove the prepayment from the Invoices & Prepayment tab to allow for changing the advertiser. The same applies if the campaign is billed where you cannot change the advertiser.

### Change Agency / Agency Percentage

This will open a dialog box where you can see the current agency and % and change it to a new agency:

<figure><img src="../../../../.gitbook/assets/image (1209).png" alt=""><figcaption></figcaption></figure>

If you attempt to change the agency on a campaign that has already started billing, you will be warned that the changes will only affect future invoices:

<figure><img src="../../../../.gitbook/assets/image (1478).png" alt=""><figcaption></figcaption></figure>

If you need to make a corretion and change a past invoice to a new agency, use the billing function to Reverse Campaign Invoicing, and then change the agency and re-invoice the campaign.

{% hint style="info" %}
Note: if the existing agency is billed to a foreign currency and the new agency is billed to a local currency, and there are line items on the order, user will be advised to cancel the campaign and re-book since the lines would be using different rate cards for the different currencies.\
If there are no line items yet on the order, and the agency is changed to one using a different currency than the original, then the campaign will be updated to reflect the billing agency's currency.
{% endhint %}

Change Campaign End Date

This function is used typically if a client has terminated a campaign sooner than the original end date, though it could also be used to extend a campaign longer.

<figure><img src="../../../../.gitbook/assets/image (249).png" alt=""><figcaption></figcaption></figure>

### Change Terms

This function will only affect future invoices if the campaign has already started invoicing. It is used to change the payment terms for this campaign.

<figure><img src="../../../../.gitbook/assets/image (595).png" alt=""><figcaption></figcaption></figure>

### Change Campaign Type

This is used to switch a performance campaign to a flexible, or to change a flexible to a performance. This can only be done if billing has not already started.

<figure><img src="../../../../.gitbook/assets/image (712).png" alt=""><figcaption></figcaption></figure>

### Change Order Reps / Change Original Reps

Both of these options look the same, but one will change the Order Rep and the other will change the Original Rep

<figure><img src="../../../../.gitbook/assets/image (1187).png" alt=""><figcaption></figcaption></figure>

### Change Status of the Campaign

This option will not be available one the campaign has started billing. It may also be limited by your user permissions or on credit issues with the account.

The below example shows that I can change the status to a later quote status or to a reserved status, but i cannot confirm it due to the account be overdue and my user does not have permission to confirm an ad if the account is overdue.

<figure><img src="../../../../.gitbook/assets/image (938).png" alt=""><figcaption></figcaption></figure>

If there are no limitations to confirming, the change status screen for confirmed appears like this:

<figure><img src="../../../../.gitbook/assets/image (188).png" alt=""><figcaption></figcaption></figure>

There are no limitations or warnings in the Campaign Status Messages section and if i am allowed to, i may be able to apply Cash on Account to prepay for the ad.

### Renew this Campaign

This function will renew (pickup) this ad. It will copy the original ad materials as well and it will attempt to schedule in a similar way to the original. See [Expiring Campaigns](../expiring-campaigns.md) for additional information

<figure><img src="../../../../.gitbook/assets/image (561).png" alt=""><figcaption></figcaption></figure>

### Re-Sync to Ad Server(s)

Select this to re-sync the campaign to Google Ad Manager

### Re-Sync to Naviga Plan

Select this option to re-sync all lines on this campaign to Naviga Plan. If there are lines on the campaigns with past dates, those will not likely be re-sync'd to plan, though that depends on your configuration. During testing and training it may be desirable to re-sync an old date. In real life, that would typically not be allowed to happen.
