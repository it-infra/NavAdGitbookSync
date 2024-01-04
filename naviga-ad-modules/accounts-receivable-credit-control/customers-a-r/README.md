---
description: >-
  This will take you through Account overview screen for Accounting and the A/R
  part of Account Maintenance
---

# Customers (A/R)

## Customer Account Overview <a href="#toc124065030" id="toc124065030"></a>

In the A/R and Credit Control modules, navigate to Customers -> Customer Account Overview

This will take you to a seach screen to find existing or create a new customer account. Search by Name at the top, or on the advanced search tab you can search by Name and many other fields. Can also search by a credit card (last 4-digits and card type) on the Search by Card Transaction tab.

<figure><img src="../../../.gitbook/assets/image (1192).png" alt=""><figcaption></figcaption></figure>

Once search results are displayed click on the customer name or ID to open the Account Summary screen. Use the "History" tab to quickly select a recently accessed account (last 50 accounts displayed)

<figure><img src="../../../.gitbook/assets/image (158).png" alt=""><figcaption></figcaption></figure>

From here, user can review a customer account to drill down into Paid Invoices, Payments, orders, notes, CRMs to do, and credit control notes to view relative information.

The light blue bar at the bottom of the above screenshot will take you to several quick actions:

* Go to Account Setup will take you to the Name / Address Maintenance screen for this account.
* Add a Contacted Note - opens a screen to add a Credit Contol note. Upon save, the note will appear in the "Credit Control Notes" section of this screen.
* Add an Internal Note - This will also appear in the Credit Control Notes section of this screen, but the difference is that the Credit Control Status and planned next contact date is not displayed when creating an internal note. There are permissions in Group Security controlling who can create an internal note vs a contact note.
* Apply a credit
* Enter a check payment
* Enter a credit card payment

If you do not see the light blue bar, that is because you do not have access to those functions. Sales users typically will not be able to see the light blue bar or access those functions.

### Access to different modules <a href="#toc124065031" id="toc124065031"></a>

User can click the different CRM, Production or Exhibition links to view and act regarding the account displayed on the screen. See Also [Advertising > Customers](../../advertising/customers/)

## Name / Address Maintenance

This page contains account setup information for the various modules within the system. For detailed information on Account Setup for [Advertising](../../advertising/customers/#advertising-setup-node), [Job Costing](../../production-job-costing/customers.md#customer-maintenance), and [Exhibition](../../exhibitions/exhibitors.md#exhibitor-maintenance), please see those modules in the documentation.

### Name and Address Setup

This page contains name, ID, parent account, Name Aliases, Sources, email information, social media links, Legacy ID, and logo.

{% hint style="info" %}
Note - if using the feature to create Ad hoc billing address in order entry, the billing email address will be added to the email information section of the Name and Address Setup node here. The ad hoc billing address is enabled for certain client types only. See [Client type setup](../../advertising/setup/client-types.md#create-bill-to-in-order-entry) for more information
{% endhint %}

If you are creating a new account from this screen, click the + to the right of the Account ID field. You will be prompted to select New Agency or New Advertiser.

<figure><img src="../../../.gitbook/assets/image (1610).png" alt=""><figcaption></figcaption></figure>

The fields entered for an agency are a little different than fields entered for an advertiser. For an advertiser the screen will look like this:

<figure><img src="../../../.gitbook/assets/image (1128).png" alt=""><figcaption></figcaption></figure>

For an agency, the fields below will be displayed:

<figure><img src="../../../.gitbook/assets/image (877).png" alt=""><figcaption></figcaption></figure>

Note that the PIB code disappears for a new agency since the PIB/Industry code is only related to the advertiser on the orders. Mobile number also disappears for Agencies. (Contact people at an agency might have a mobile number, but the agency itself likely doesn't) Agencies also don't have Brands or agencies.

{% hint style="info" %}
We recommend limiting the Name field to 30 characters. While Naviga Ad will allow more than 30, downstream integrations can have issues with longer name fields.
{% endhint %}

#### Employees/ Contacts

You can use the link Add a new contact to add many contacts for this advertiser. You can also edit the contact information.

#### Addresses

This node allows you add or edit addresses for the advertiser.

#### External Contacts

Lists external contacts for this account. Typically used for Agency/Client Relationships. If you are looking at the client account, it will list agency contact people who you contact related to this account.

<figure><img src="../../../.gitbook/assets/image (631).png" alt=""><figcaption></figcaption></figure>

You cannot add or remove from this screen. To add a new related contact person go to the Customer Account Overview screen, CRM Tab, and click either "Link a Contact" from the light blue bar or from the My Contacts section click on "Add a Contact from Another Account.

#### External System IDs

Prerequisite: One or multiple external accounts can be configured in Advertising -> Setup > [System Tables Setup.](../../advertising/setup/system-tables-setup-ad/#external-system-id-codes)

This will store the account ID's for the customer in the pre-configured external systems.

<figure><img src="../../../.gitbook/assets/image (1617).png" alt=""><figcaption></figcaption></figure>

#### Account Overview

Click on account overview to be taken to the Account overview view of this customer.  If you are looking at the name maintenance of an individual rather than a customer account, the Account overview will take you to the Account overview of the contact's employer.

### A/R setup

#### AR Details

This node allows you to setup all fields regarding the accounts receivable side of the advertiser.

Main Address ID and Address - To edit the main address on the account, click the pencil icon. To add a new address click the plus sign.

**Client Groups** - Select one or more client groups for this client. For setup see [A/R Setup](../setup-a-r-system-setup/other-a-r-setup-menu-items.md#client-group-setup)

You can set the advertiser on credit stop if you check the option “Credit Stop” to be a “Yes”. See [Credit Control section](../credit-control/credit-stop.md) for more details on Credit Stop.

You can also “Approve Account” if it’s a new account awaiting approval.

**Allow generation of** [**collection letters**](../credit-control/collection-letters.md) is a flag when checked allows you to generate collection letters for this client.

**Auto-Clear Balance:** Select a card on file to use to when clearing this account's invoice balance in this field. The client must have a credit card on file in the “Cards on File” tab below. The auto-clear process creates a single card transaction for all outstanding invoice balances.

#### **Client Access Codes** (Only displayed if Naviga Support turns the feature on for your site)

The standard design of the Naviga Ad system assumes that any system user can search for, and find, any client. Once the client is accessed the data is filtered depending on user/group security. Order information can be filtered by what was purchased and/or by who sold the ads, CRM information can be filtered and A/R information can be hidden. This allows for minimizing duplicates while segregating order and CRM data. The lack of duplicates streamlines reporting and allows for unique customer records for interfaces.

While not a standard, or necessarily recommended, setting; it is possible to hide certain customer records entirely. If this setting is selected, duplicate clients will be created, this will have an impact on reporting and integration to external systems. Setting this will limit duplicate checking and allow for creation of duplicate clients without warning.

If your business requires this strong segregation of name information, notify Naviga to activate the system wide default. [Set up the client access codes](../../system-settings-admin/setup/client-access-code-setup.md). These may be loaded from your product codes or your company codes, or may be set up as a unique table. Ensure that an access code is included for each client in your client import. Set the appropriate client codes that each group of users should see in name security for each user security group.

When new customer records are created in the system, the software will default in the access code(s) from the security group of the user that created the name record. These code(s) can be edited by users that have access to the A/R screen in name maintenance.

On customer searches, system reports and all screens in the software users will only have access to clients coded to match their security access. Other clients will be hidden.

#### Credit Information

**Credit Rating** is a free entry of any value such as good, bad, and so forth.

**Credit Limit** is an amount which is free entry such as 20,000. When the orders for this advertiser reach this amount and these orders are in the confirmed status, then based on security option setup, the order entry user will receive an alert or be stopped from confirming orders for this advertiser.

**Credit Stop Days (Ad):** These are the number of days which when reached on invoiced campaigns which haven’t been paid, then the user cannot confirm anymore campaigns for this advertiser.

**Credit Controller:** This allows for setting a default credit controller for the account.

**Refund Vendor ID** - only relevant if using our A/P Module. This is the A/P vendor who will be used if a refund check needs to be created.

**Debt Collector** - Free Format field used by some to indicate an external collection agency. (More of a legacy function. Typically we now see the debt being "transfered" to a collection agency account and tracked for collection purposes in that account.)

**Query Code** - Free Format field used by some to enter text that is then used in Informer

**Generate Statements** - select Yes if this account is to receive A/R Statements. Select No to surpress statements for this account

**Service Charges** - select Yes if this account is to receive Service Charges. Select No to not include this account when calculating service charge fees.

**TAS Reference Number** - Not used anymore. Had been used in our Book module.

**Credit Application on File** - yes/no indicator that a credit application has been received and is on file. This is also displayed on the Account Approvals report in A/R -> Customers Menu -> Approve Pending Accounts

#### More Information

**International Tax ID / VAT Validation** - Enter tax ID and click Validate VAT to validate the client's tax ID

**Currency** - Select customers desired currency. Depending on Country setup and on user's Group Security, this may be defaulted in from the country code and may or may not be editable by the user.

**Territory** - Sales Territory where this account belongs.

**Sort Order** - Legacy field. Not used anymore in Digital First. Used to be used in reports and such to sort an account on a different letter. (ie. might want to sort "The Gap" with the G's rather than the T's). In more modern software a quick Ctrl-F in a pdf or the page, or a filter at the top of the column can easily be used to find what you are looking for as opposed to flipping through pages of a report.

**Registered Company Number** - This is part of a feature for the Norwegian market's electronic Invoices. It is the unique identifer for every account record in Norway. User would typically not type the number directly in here, but rather search for the number on the Advertising Node in the EHF Invoice Settings

#### **Default Billing**

This section contains the parameters of the billing which will be the default values for the advertiser.

Preferred Forms Language - On invoice, signature, and confirmation forms in the system you can set different forms to be used for different languages. If you choose to take advantage of this function, you can select which language this client will get forms in.

Tax Code - This is the tax code that will be used for this customer. This may be set by default based on the client's location or client type.

Terms - This sets the terms for when an invoice is due

Show Due Date - this sets whether or not the due date is displayed on invoice forms

Billing Contact Type - The billing contact can be a contact person in the system or it can be set with just a name by selecting the Billing Contact Type of "Enter a Manual Contact".

{% hint style="info" %}
This setting here is only for A/R Invoices. For billing information for Advertising, Exhibitions and Job Costing Modules, see Account Setup in those modules.
{% endhint %}

#### Miscellaneous Billing Details

This section is for the setup of the miscellaneous invoices for this advertiser. These include contacts even from other advertisers.

{% hint style="info" %}
If the Delivery Method in the Misc Billing Details section of this page is set to Email or Print & Email, you must have a contact with a valid email address selected. If there is just a single Billing Contact, and it is a contact person on this account, it can simply be selected in the Billing Contact dropdown above. If there are multiple contacts, or the contact is on a different account, then it can be added in the "Email Invoices to These Contacts" section. In the case that multiple invoice contacts are added, all contacts selected as Email contacts must have an email address before you will be able to save the record.
{% endhint %}

#### Statement Details

This is the section for defining the recipient and delivery method for A/R Statements.

#### Also Pays For

Use this section to define the other accounts which this advertiser pays for their invoices. This option can be used in the A/R Payments screen to view and pay these other advertisers’ invoices.

#### Electronic Payments

Section to define the methods to pay electronically for the invoices of this advertiser.

#### UDFs

This is the list of user defined fields which you can fill in here and it will be always defaulted and available across the system. These UDF fields are created in the menu in the Accounts Receivable menu Setup -> Customer User Defined Fields.

### Advertising Setup

See [Advertising Details](../../advertising/customers/#advertising-details) in the Advertising documentation module

### Job Costing

This screen contains the setup of the job costing (Production module). For details, please see [Production](../../production-job-costing/customers.md#customer-maintenance)

### Exhibition Setup

This screen contains the billing and tax setup for the exhibition module. For details, please see [Exhibitions](../../exhibitions/exhibitors.md#exhibitor-maintenance)

### Attachments

This screen allows for attaching documentation or links to the advertiser. These can be any types of documents such as contracts.

### Cards on File

This screen allows for adding new credit cards of the advertiser to store and use to pay for campaigns.

### Account Alerts

This screen allows you to add alerts which the user entering orders for this advertiser will see when choosing the advertiser in the order entry screen. To create a new alert, select Add New Alert. The alert type down down is configured in [A/R Setup](../setup-a-r-system-setup/other-a-r-setup-menu-items.md#account-alert-type-setup). You can select a date range during with the alert should appear.

### History of Changes

This screen tracks any changes made to the advertiser information including who made the changes and when they’re made as well as any reason for the change. This will also include any changes to the brands related to this account.

### &#x20;<a href="#bookmark29" id="bookmark29"></a>
