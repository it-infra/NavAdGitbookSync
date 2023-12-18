# Customers

## Customer Search

See [Advertising Advertiser/Agency Inquiry](../../advertising/customers/#advertiser-agency-inquiry)

## Add An Account

When adding a new account from the CRM Module, there is a handy google search available which will search for accounts on google and bring address, phone and website information in from google where available.

<figure><img src="../../../.gitbook/assets/image (1066).png" alt=""><figcaption></figcaption></figure>

* **Account Name** - When you see the gray "Enter the location" text the google search is available. Start typing in this field and google will return any results for that company name. Select the company and the phone, fax, website, Address, Postal Code, City, and State may be pre-filled based on what is available through Google. **If you are searching for a company that is outside of your home/default country, select the appropriate country from the country dropdown FIRST and then do the Google Search.** Otherwise the system will attempt to put the foreign account into the home country formatting.
* **Account Type** - Options are Advertiser/Exhibitor OR Agency. This is important because only agency accounts will be available to select from in the Agency lists. Agency's cannot book orders. They can only be an agency to an account. The account type cannot be changed once created.
* **Employees / Tier** - Enter the number of employees for the organization. Note that as soon as you enter number of employees in the “Employees” field, the Tier value is automatically selected based on the setup done in [CRM System Settings](../setup/crm-system-settings.md#employee-tiers). These are optional fields and can be left blank. Once entered, they can be found on the account overview screen on the tab “Other”.
* **Annual Revenue / Tier** - Enter the Annual Revenue for the organization. Note that as soon as you enter a number in this field, the Tier value is automatically selected based on the setup done in [CRM System Settings](../setup/crm-system-settings.md#revenue-tiers). These are optional fields and can be left blank. Once entered, they can be found on the account overview screen on the tab “Other”.
* **Client Type** - Client types dropdown is [configurable](../../advertising/setup/client-types.md#client-type-setup) and selection here can set certain [defaults](../../advertising/setup/client-types.md#client-type-defaults-setup.) for account behavior.
* **Industry / PIB Code** - This is a key field in the Naviga Ad System and must be filled in on all accounts. How simple or complex you make it is up to you. The options in this list are created in [System Tables Setup](../../advertising/setup/system-tables-setup-ad/#pib-industry-setup). It is used in various reports in the system, like the [Product Group Analysis](../../advertising/analysis/campaign-reports.md#\_toc121381182) and the [Client Comparison Report,](./#client-comparison) in addition to the [Insights](../../advertising/customers/#customer-account-view) tab on the CRM view of an account.
* **Primary Industry / Secondary Industry** - Enter also the Primary and Secondary Industry values in the respective fields to indicate the company industry specialization. These are generally optional fields, but can be made required by your system administrator.
* **Parent Account** - If applicable, link the advertiser to a parent account field.
* **Multiple Brands / Divisions** - The default here will be influenced by what is set in [Advertising System Parameters](../../advertising/setup/admin/system-parameters.md#general-settings), Option #2
* **Agency ID / Name** - If applicable, link the advertiser to an agency in this field
* **Source** - This dropdown in Configured in CRM System Settings -> Name Sources. Select the source of this new account.
* **Phone / Fax** - This may have been auto-populated by the google search if you used that.
* **Website** - This may have been auto-populated by the google search if you used that.
* **Country** - This will default to your home country from User Security. **If you are using the google search for a company that is outside of your home/default country, select the appropriate country from the country dropdown FIRST and then do the Google Search.**
* **Address, City, State, Zip/Postal Code** - This may have been auto-populated by the google search if you used that. Otherwise fill in the address details

#### Other Settings

* International Tax ID - Enter the Tax ID for the advertiser, if applicable
* Registered Company Number - This is part of a feature for the Norwegian market's electronic Invoices. It is the unique identifer for every account record in Norway.
* Tax Code - This is the tax rate applicable to the advertiser. It must be set up in advance under [System Tables Setup](../../accounts-receivable-credit-control/setup-a-r-system-setup/system-tables-setup-a-r.md#tax-setup)
* Foreign Billing Currency - if the customer wishes to be billed in a foreign currency, select that currency here. It might be defaulted in from the Customer's [Country Setting](../../accounts-receivable-credit-control/setup-a-r-system-setup/system-tables-setup-a-r.md#\_toc474147075). Foreign [currencies](../../accounts-receivable-credit-control/setup-a-r-system-setup/system-tables-setup-a-r.md#currency-setup) must have already been set up.

## My Customers

This is a list of customers which have been flagged as "My Customers" in the CRM. I may or may not also be the rep who will get commissions for this account in the Advertising Module

<figure><img src="../../../.gitbook/assets/image (1087).png" alt=""><figcaption></figcaption></figure>

User can multi-select rows and export only those rows to Excel, or they can export all to excell or pdf using the icons at the top of the results grid.

## My Contacts

Similar to My Customers above, these are the contact people on accounts that are labeled as "my contacts"

<figure><img src="../../../.gitbook/assets/image (1628).png" alt=""><figcaption></figcaption></figure>

## My Comp Subscriptions/ Comp Subscriptions - Serve An Issue

Complimentary Subscriptions can be assigned in Naviga with security controls to limit the number of complimentary subscriptions of publication issues by type.

Navigate to the customers overview screen. Scroll to the shutter “My Contacts”. Click the hyperlink to a contact, and the contact screen opens. Scroll to the shutter “Complimentary Subscriptions”.

![](<../../../.gitbook/assets/1 (22).png>)

Click the “Add New Complimentary Subscription”.

![](<../../../.gitbook/assets/2 (69).png>)

Choose the publication from the drop down menu, and enter the number of copies per issue to serve.

Enter the number of issues to serve to this contact. Enter in the field “Add New Email” the email address of the person to notify when the issues all have been served. Click the + sign. The start date will automatically fill in as today’s date. Then click the save button.

The contact refreshes with the new subscriptions and the remaining issues and the last served.

![](<../../../.gitbook/assets/3 (79).png>)

Note that if you choose to do another complimentary subscription to a client on the same publication, this new subscription will override the exiting complimentary subscription. It will only create a new subscription if it is for a different publication.

### View Subscription <a href="#_toc76450729" id="_toc76450729"></a>

Navigate to the menu Customers -> Comp Subscriptions Serve Issue. Choose the publication from the drop down menu.

![](<../../../.gitbook/assets/4 (29).png>)

You can narrow your search by choosing a type of subscription. Click the button “Get Subscriptions”. The list will show. The data can be limited by the type of subscriptions. These types are setup to be for example, office types, or promotional types, or residential, or any type which is applicable.

### Prerequisite Comp Type Setup <a href="#_toc76450730" id="_toc76450730"></a>

The CRM types can be setup in the CRM System Parameters under the Setup menu.

![](<../../../.gitbook/assets/5 (58).png>)

Click the node “Comp Types”. Enter a new ID, description, and click the + sign. Along with the type, you can enter the number of copies and the number of issues. This will limit the sales rep from dispensing unlimited number of issues and copies without planning. Click the save button.

### Subscription Maintenance <a href="#_toc76450731" id="_toc76450731"></a>

Click the button “Flag Next Issue as Served”. And repeat the search.

![](<../../../.gitbook/assets/6 (20).png>)

The number of issues is decreased by one, and the last served column is updated to today’s date when the serving happened. The system will also show the issues remaining and the number of copies.

Navigate to the menu Customers -> My Comp subscriptions.

![](<../../../.gitbook/assets/7 (13).png>)

The screen will display the sales rep’s list of complimentary subscriptions and the statistics regarding it. The data can be exported to Excel or PDF.

Note that if an address set to “Do Not Use” and no replacement is selected then the complimentary subscription is stripped of address and doesn’t appear on the Comp sub listing for that publication.

## Favorites

A rep can flag any of their accounts as favorites on the Account Overview Screen

<figure><img src="../../../.gitbook/assets/image (735).png" alt=""><figcaption></figcaption></figure>

Any favorites will be displayed in a popup window when this option is selected Customers -> My favorites

<figure><img src="../../../.gitbook/assets/image (1158).png" alt=""><figcaption></figcaption></figure>

## My Prospects

If using the "Leads" functionality within Naviga Ad, that might be a better source for this type of data. These reports were created before the Leads concept existed within Naviga Ad.

#### Prospects by Product/Exhibition/Category

This shows a list of advertisers which have been flagged on the account as having certain "interests"

<figure><img src="../../../.gitbook/assets/image (971).png" alt=""><figcaption></figcaption></figure>

The data comes from this section here:

<figure><img src="../../../.gitbook/assets/image (1272).png" alt=""><figcaption></figcaption></figure>

#### Prospects by Source

This report shows a list of accounts based on the source

<figure><img src="../../../.gitbook/assets/image (1103).png" alt=""><figcaption></figcaption></figure>

The data can be seen here:

<figure><img src="../../../.gitbook/assets/image (1651).png" alt=""><figcaption></figcaption></figure>

## Call Lists

See [CRM Manager Call Lists](../crm-manager.md#call-lists)

## Advertiser Listing

See [Advertiser Listing](../../advertising/customers/#advertiser-listing) in Advertising Module

## Agency Listing

See [AgencyListing](../../advertising/customers/#agency-listing) in Advertising Module

## Advertiser Orders

See[ Advertiser/Agency Reports](../../advertising/analysis/advertiser-reports.md#advertiser-agency-orders) in Advertising Module

## Agency Orders

See[ Advertiser/Agency Reports](../../advertising/analysis/advertiser-reports.md#advertiser-agency-orders) in Advertising Module

## Client Comparison

The client comparison report will compare two clients to each other, and then to everyone else.

<figure><img src="../../../.gitbook/assets/image (248).png" alt=""><figcaption></figcaption></figure>

In the top section:

* Select the two desired clients
* The report can be summarized by total amounts or by a % of the total sales.
* Quotes can be included or not
* The middle section of the report displays products and formats purchased. The totals in these areas can be taken from the last x months. Fill in desired number of months at the top of the screen.
* Click select data.

<figure><img src="../../../.gitbook/assets/image (805).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1389).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1320).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1508).png" alt=""><figcaption></figcaption></figure>
