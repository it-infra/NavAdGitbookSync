# Advertiser Maintenance

## Advertising Setup node

This section discusses the Advertising Node of the Name Maintenance screen. For Exhibition node see [Exhibitions](../../exhibitions/exhibitors.md#exhibitor-maintenance), for Job Costing Node see [Production](../../production-job-costing/customers.md#customer-maintenance), for all other nodes see [A/R and Credit Control](../../accounts-receivable-credit-control/customers-a-r/#name-address-maintenance)

### Advertising Details

This menu contains all information about the advertiser regarding the advertising module.

For example, the name and main address of the advertiser which you can add here or edit.

**Account Status:** In this screen the status is read only. If it has been put on Credit Hold on the A/R Setup screen, then the status will display in red in here.

**Territory:** Sales Territory where this account belongs.

**Transient Record:** Set this flag to Yes if this is the generic, umbrella account you want to post all Classified Self Service orders to. Do NOT set this flag for regular private party advertisers. The orders for this transient advertiser will be available to view in reports only if the flag for the field “**Display Orders for this transient account record in production system**” is set to “Yes”.

{% hint style="info" %}
See below for additional information on [Transient Advertisers](advertiser-maintenance.md#managing-transient-customers).
{% endhint %}

**Is this an Agency** is a flag to be checked only if this account is an agency. If so, then the Brands node on the screen will disappear as agencies don’t use brands.

**Use Multiple Brands**: If set to No, then the advertiser has only one brand usually named the same as the advertiser name and appears as such in the campaign entry screen. If set to “Yes”, then you can enter multiple brands and each brand can be setup separately on the [brands ](brands/)tab at the top of the screen.

**Pay Sales Rep Commissions on Paid Invoices Only**: If set to “Yes” then Salesrep’s commissions will not be processed unless the order’s invoice has been paid.

**Client Type:** This is a list as per the Setup menu -> Client Type Setup which is optionally set for each advertiser. This value is useful if you’d like to view this in reports as well as set Ratecards to be used for specific Client Types and not others. You can also set defaults by client types.

**Pre-Payment Required:** This can be set as prepayment required for this advertiser to enforce prepayment of a campaign before the campaign is confirmed.

**Auto Apply Cash on Account when Campaign is Confirmed:** If set to Yes then the system enforces that cash on account would be automatically applied to this advertiser’s campaigns before confirming. If the advertiser doesn’t have COA available, then the system will not allow confirming the campaign.

**Default Invoice Form Detail Level:** This option allows for details of the order to display on the invoice to the level you desire.

### More Information

The More Information section allows you to set some more fields such as:

**Bill-to ID:** This allows you to place the advertiser’s ID or another advertiser’s ID to be billed for campaigns.

**Charge Credit Card:** You can set this to Yes and add a credit card on file in the Cards on File tab. This will indicate in order entry that the client has authorized credit card payment. Setting this to "yes" will give a message when confirming the campaign to alert the user that there is a card on file that the customer wants to use.

<figure><img src="../../../.gitbook/assets/image (671).png" alt=""><figcaption></figcaption></figure>

and when the above is set to yes the user will also see this when making a payment:

<figure><img src="../../../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>

If the flag is not set the user will see this when taking a payment:

<figure><img src="../../../.gitbook/assets/image (463).png" alt=""><figcaption></figcaption></figure>

The above message doesn't mean that you can't take a payment....it just means they don't have a preference set to always use a credit card.

**P.O. Required:** This flag makes P.O. Number a required field on Advertising Campaigns in Confirmed (CO) Status.

### Advertising Billing

Advertising Billing section has billing fields specific to the order invoicing in the advertising module.

**Billing Group:** You can choose to place this advertiser in a billing group which you can filter on in the billing menu to bill this group of advertisers at the same time. Each advertiser will receive a separate invoice. Set up Billing Groups in [A/R Setup](../../accounts-receivable-credit-control/setup-a-r-system-setup/other-a-r-setup-menu-items.md#billing-groups)

**Tax Code**: This option defines which tax you can charge on campaigns for this advertiser.

**Terms**: Defined the payment terms.

**Digital Agency %:** If you enter a value here, orders for this advertiser will be charged an agency commission of this value.

**Show Due Date:** Setting this to Yes will display the due date of this invoice on the invoice based on the terms setting.

**Delivery Method:** This option allows for printing the invoice, emailing it, neither, or both. If you choose email, you must have a valid email address for the invoice recipient.

**Actuals Reconciliation:** For digital CPM delivery on a campaign this option determines how the actuals are going to be reconciled with estimates. The options are as follows:

* Use Ad Server Numbers: When you reconcile actual impressions to estimates, the system will use numbers provided by the AD Server your product is connected to such as Google Ad Manager.
* Use Estimates: This option will use the estimates of impressions you enter on the line items and calculate amounts to bill based on these estimates.
* Use Third Party Numbers: The line items will use third party numbers which you provide through third party software programs.
* Use Ad Server Viewable Numbers: This choice will calculate the amounts based on the Viewable numbers of the ads, based on the agreement of the definition of what makes an ad viewable. For example, the ad clicked on by potential viewing client for a predefined number of seconds. If the number of seconds isn’t met, and the viewing client closed the ad before that, then the click isn’t counted as a viewable ad.

Note that the flag on the Product Setup screen -> Product Details for the field “Actuals Reconciliation Override” overrides the setting here. Both can be overridden on the Line Item itself under the “Other” tab. This flag on the Product Setup screen allows for using either the Advertiser Maintenance Setup here or always Use Ad Server Viewable Impression Numbers.

**Actuals Billing Method:** The value here can be overridden directly on a campaign line item. The options are:.

* **No Caps:** Meaning the amount billed to the advertiser is based on the actual count of impressions of the ad, regardless of the source being Ad Server Impressions, or Third Party and so forth.
* **Capped at Total Goal:** Meaning there is a cap placed on the total amount on the campaign after entering and saving the actuals for all but the last month in the campaign. In this case, if the campaign is running over the course of several months, each month can be reconciled based on the actual impressions, except for the final month, which will be adjusted to add up to the campaign total amount regardless of the number of actual impressions in that month. So, the advertiser is not overcharged over the promised the campaign total.
* **Capped at Individual Monthly Goals:** This option has every month actual amount capped at the estimates regardless of actual impressions on a line. This results in the same amounts per month charged to the advertiser regardless of the actual impressions in that month.

### Override Invoice & Statement Form Settings

The invoice forms you choose here will override the forms setup in the Product Group Setup menu. So when you create an order for this advertiser in a product group’s product, these invoice forms here will be used and not the Product Group forms.

### Billing Contact

Billing Contact section contains the name of the person receiving the invoice on the advertiser’s side. You can add or edit the name here.

The billing contact can be a contact person in the system or it can be set with just a name and an email address by selecting the Billing Contact Type of "Enter a Manual Contact".

<figure><img src="../../../.gitbook/assets/image (1679).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note - if using the feature to create Ad hoc billing address in order entry, the billing email address will be added as a Manual Contact here. The ad hoc billing address is enabled for certain client types only. See [Client type setup](../setup/client-types.md#create-bill-to-in-order-entry) for more information
{% endhint %}

<details>

<summary><mark style="color:purple;"><strong>Some nuances to understand regarding who gets the advertising invoice</strong></mark></summary>

In **Name Maintenance, on the A/R Setup Node**, there is a field for the Default Billing Contact. This will be used as the Billing Contact on the Campaign header if there isn't an override set on the Advertising Setup node or on the Brand. This can be typed in as a manual billing contact, or it can be selected from a dropdown list as a contact person\
![](<../../../.gitbook/assets/image (2) (1) (1).png>)

In **Name Maintenance, on the Advertising Setup**, there are two sections related to billing contacts. In the first highlighted box below, this field will override any billing contact set on the default above.\
![](<../../../.gitbook/assets/image (3) (1).png>)

Similarly, on the brand, if there is an override here, it will override what is on the Advertising setup or A/R Setup:\
![](<../../../.gitbook/assets/image (5) (1).png>)

If all three of these billing contacts are blank - then the billing contact on the campaign will also be blank.

<img src="../../../.gitbook/assets/image (4) (1).png" alt="" data-size="original">

This field is what is used to populate the #BILLTO\_CONTACTNAME# tag on the form itself.

When invoices are mailed, not having a billing contact might not be an issue, since the billing address is still there, but when emailing invoices, you need to have someone to send the invoices to. Typically, if you set the delivery method to Email or Print & Email on the Advertiser Setup, the system will not allow save unless a contact person with an email address is entered in (Either in the top dropdown for the Billing Contact, or in the section below it where you can add one or multiple contacts.) There is a system setting, though, in **Setup -> Admin -> System Parameters** that allows that setting to be overwritten:\
![](<../../../.gitbook/assets/image (6) (1).png>)

If the above is set to yes, the system would expect that the billing information is always entered either on the brand or on the A/R Setup node, otherwise you might have an issue in billing where we can't bill b/c we don't know where to send the emailed invoice.

**\*\*\*Very Important Nuance**\*\*\*

If you are EMAILING Invoices....and you are setting up who to email the Invoice to on the Advertiser, as I mentined above, there are two places on advertiser setup that relate to emailing invoices (highlighted below):\
![](<../../../.gitbook/assets/image (3) (1).png>)

Those same two sections are also on the **Brand setup -> Billing** overrides node

<img src="../../../.gitbook/assets/image (1754).png" alt="" data-size="original">

**The top section on the brand will override the top section on the advertiser; the bottom section on the brand will override the bottom section on the advertiser.**

Selecting a person in the TOP circle above on the advertiser will email the invoices to that Advertiser contact ONLY IF there isn't an override on the **top circle** on the brand.

Selecting a person in the BOTTOM circle above on the advertiser will email the invoices to that Advertiser contact ONLY IF there isn't an override in the BOTTOM circle on the brand.

If you mix and match those circles by selecting the top on the advertiser and the bottom on the brand (or vice versa) it will result in the system emailing the invoices to BOTH the Advertiser contact AND the Brand contact.

</details>

### Email Invoices to These Contacts

These email recipients will receive the invoices once you bill a campaign. You can create new contacts here for this advertiser.

<figure><img src="../../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If the Delivery Method in the Advertising Billing section of this page is set to Email or Print & Email, you must have a valid email address. If there is just a single Billing Contact, and it is a contact person on this account, it can simply be selected in the Billing Contact dropdown. If there are multiple contacts, or the contact is on a different account, then it can be added in the "Email Invoices to These Contacts" section. All contacts selected as Email contacts must have an email address.
{% endhint %}

### Contact for Email Confirmation

This is the person receiving the confirmation email from the campaign header screen.

### Default Affidavit Contacts

This is the section where you can enter the name and contact information for affidavits if required.

**Default Number of Tearsheets to Supply:** This is the default number of tearsheets supplied to the advertiser.

### EHF Invoice Settings

In this section the user can click the button "Search ELMA for Recipient." A Window pops open and populates the customer name in the search field. If a match in the ELMA directory exists, then their Customer Registration ID is populated here and also on the AR node as the "Registered Company Number." this number will also show up on other screens if the client country is setup in Address Setup to require this code.

## Managing Transient customers

With the introduction of the classified self-service portal, Naviga introduced the concept of a transient customer. While this concept was initially intended to manage clients creating their own ads on the portal, it may be used internally to avoid cluttering the database with one-time advertisers. One would create a dummy shell customer, and flag that account as the Transient account in Advertiser Maintenance, Advertising node. Ads can be entered using the transient client, avoiding the need to set up one-time advertisers as customers. The transient placeholder would display in reports as the customer name, but depending on the report, the First/Last Name, email and/or phone number of the person could be displayed and filtered on.

**Campaign Entry for a Transient Advertiser**

Select the transient account as the advertiser, the account can be found using any of the standard search methods.

The system will display four additional fields: First Name, Last Name, Email Address, Phone. Enter the desired information in these fields to allow for viewing who the actual advertiser is. The system will not create a customer record, this information will be stored on the campaign. These customers will not clutter the name file and so will not be found if searching for a customer name.

**Searching for Transient Orders**

From the campaign edit screen, these orders can be found in two different ways.

1. If one searches for the transient placeholder customer, all campaigns for that customer will display, and the search results will display the first name, telephone number and email address in the advertiser column.
2. If one is searching for a particular one-time advertiser, type in the name field either the persons first name, last name, telephone number or email address. Only orders for that particular customer will display.
