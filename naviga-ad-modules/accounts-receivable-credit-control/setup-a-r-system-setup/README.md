# Setup (A/R System Setup)

Navigate to the menu Setup in the A/R module -> Admin -> A/R System Setup.

This menu determines the defaults settings for the A/R system such as the open financial period(s), invoice and receipt options, emails for notifications, A/R related client settings, write off G/L's, etc.

## Financial Period Control

<figure><img src="../../../.gitbook/assets/image (81) (1).png" alt=""><figcaption></figcaption></figure>

First and last open financial periods are the dates available for users to post invoices and payments in the accounts receivable module.

{% hint style="info" %}
This also affects Advertising Module and periods that invoices can be posted to and dates that can be selected in applying payments and prepayments in order entry
{% endhint %}

Enforce date within open financial period when checked as yes, will force user to post the dates to be within the financial period. For example, an invoice or check date has to be the same month as the financial period to which the invoice or check Is posted.

## A/R parameters <a href="#_toc458780180" id="_toc458780180"></a>

1. Service Charge % - enter the % fee to charge for service fees
2. Select the Class code to use for service charges\
   See [Service Charges](../invoices/service-charges.md#\_toc102547786) section for Service Charge related options

<figure><img src="../../../.gitbook/assets/image (82) (1).png" alt=""><figcaption></figcaption></figure>

3. **DSO Calculation Methods:** Options are DSO or Media Credit Association. See Naviga Support for specific details on these. Both are fairly complex calculations with the DSO option being based on actuals and the MCA option being based on averages.
4. **Foreign Currency Indicator:** This is to control the behavior on individual accounts. Options are to allow the client to only be billed in a single currency (the currency on record for that client/client's country), allow them to be billed in multiple currencies, or do NOT allow foreign currencies.
5. **Statement / Invoice Date Format:** select the format for invoice and statement dates (this is only relevant if you are using Fabsoft forms)
6. **Allowed From Addresses for Customer Service / Collection emails:** When sending emails, if nothing is entered in this field, the logged in users email will be used. This field would typically be used if you wanted the option to send the email instead from a generic email address like accounting@mediacompany.com or something like that. See the options below in sending an email. The first address is the logged in user's address, and the other two were the additional optional email from addresses.

<figure><img src="../../../.gitbook/assets/image (1355).png" alt=""><figcaption></figcaption></figure>

7. **Custom Program to run when posting to A/R:** this is a read only field and only relevant if there is a custom process that Naviga programmers set up for your account.

## Service Charge Class Per Company <a href="#_toc458780181" id="_toc458780181"></a>

In the previous section the default Service Charge % and Class Code was defined. If this setting differs per company, overrides can be set in this section, per company.

<figure><img src="../../../.gitbook/assets/image (241).png" alt=""><figcaption></figcaption></figure>

## Automatic Inter Company G/L Allocations <a href="#_toc458780181" id="_toc458780181"></a>

These are the A/R From and To Accounts which user can change, delete or add.

![](<../../../.gitbook/assets/2 (4)>)

See Section on [Multi-Company Balancing](../../general-ledger/setup/admin/g-l-system-setup/multi-company-balancing-and-intercompany-control-accounts.md) in the G/L section of documentation for information on Intercompany G/L Allocations.

## Email Notifications <a href="#_toc458780182" id="_toc458780182"></a>

This section specifies the email recepient of emails when A/R financial conditions are met. For example, if an invoice is of a certain age, credit stop clients, G/L cash is entered, checks greater than a certain amount are received, currency is revalued, client is deleted, invoice is flagged as contended, and invoice is transferred to a collection agency. If there is no email address listed, then no email with be sent for the given event.

<figure><img src="../../../.gitbook/assets/image (83) (1).png" alt=""><figcaption></figcaption></figure>

Users can setup email notifications on the following:

1. If an Invoice is older than "X" days is paid,
2. If a client is put on or removed from credit stop,
3. If G/L cash is entered,
4. If a check is received greater than "X",
5. If a payment is received from a client on Credit Stop,
6. If currency is revalued,
7. If client is deleted,
8. If an invoice is flagged as contended,
9. If invoices are transferred to a Collection Agency

## Invoice and Cash Receipts Options <a href="#_toc458780183" id="_toc458780183"></a>

These are options of invoices and cash. For example, automatically allocate credits, whether to enter cost of sales amount on invoice, publication entry to be required to enter on a miscellaneous invoice entry, enforce the tax code on the miscellaneous invoice entry, the tax G/L account number and name, the maximum amount a G/L user can write off, and so forth.

<figure><img src="../../../.gitbook/assets/image (84) (1).png" alt=""><figcaption></figcaption></figure>

For example, some of these fields are ones that may not be self-explanatory:

* Auto Allocate Credits (1): If checked, this box will allow the system to automatically allocate all credits to the existing payments due to user from their customers.
* Enter Cost of Sales amount on invoice (2): this is for Miscellaneous Invoices in A/R. If set to Yes, there will be a Cost column in the Invoice Line Item section. If set to no, the Cost column will be hidden.
* Maximum Write-off Amount (6) - this has been replaced by the write-off amounts in Group Security, so it can be disregarded here.
* Remove prepayments on returned checks (7): This option if checked will automatically remove the prepayments by the customer on any check which user returns to customer, and amounts will be credits in the system to this customer.
* Default Misc. Invoice Module (8): This is the default value for a module on all miscellaneous invoices which user enters in the system.
* A/R Invoices - Print and Email (9 & 10): These are only used for FabSoft forms. If using Naviga HTML Forms, see Invoice Forms setup below.
* Auto Assign New Batch IDs by default (11): This option, if checked as yes, will give all batch IDs which user creates an ID. If this option is not checked and its value is “No”, then user can enter their own batch ID. User can always override this by checking the box in the G/L Cash entry or payment entry screens to “Yes” and let the system provide an automatic batch ID.

## Invoice Forms <a href="#_toc70321838" id="_toc70321838"></a>

This section determines the HTML Invoice forms setup and defaults. See [Invoice Template Setup](../invoices/#\_toc112341266) in AR Invoices section for information on the fields in this section

## Statement Forms

Use this section to set defaults for AR Statements and to set language preferences so that your clients can receive the statements in their local language if different than yours.

<figure><img src="../../../.gitbook/assets/image (61) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (85) (1).png" alt=""><figcaption></figcaption></figure>

Statement forms selected can be different for Agencies vs Advertisers vs Parent companies. Select the appropriate form for each. (and if using the language overrides at the bottom, you have the same three options.

Enter the email Subject line and Body Text in the space provided. (again that can be different for language overrides). Any of the Single-value merge tags from statement setup will be able to be used in the Subject and body as long as HTML formatting is not required since this is just a text box and not full HTML controls like you have in the creation of the statement itself. (That means things like Customer name, contact name, account number, total balance would be fine to put in, but the Logo wouldn't be, since that would require HTML formatting.

Override Email From Address - This will display the desired from address (perhaps "statements@mediacompany.com" or "accounting@mediacompany.com"

Override Email To Address - This will override the To email address to be a specific email address. This comes in handy when you are testing a new statement form, or during an implementation where you don't want to risk sending test statements out to actual clients.

## Write-offs and Refunds <a href="#_toc458780185" id="_toc458780185"></a>

This is the section for the write offs and refunds settings in A/R.

<figure><img src="../../../.gitbook/assets/image (1298).png" alt=""><figcaption></figcaption></figure>

They include the company name and write off and refund G/L accounts ID and description. User can add more than one line to the list.

## Client Defaults <a href="#_toc70321840" id="_toc70321840"></a>

This section defines the pre-populated values for new clients, which users create in the system.

<figure><img src="../../../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

For example, the default payment terms, tax, credit limit, control status, automatically approve new clients or require a manager to approve them and if prepayment is mandatory on all orders by new clients. If this is mandatory, then orders will remain in the reserved or quote status until a prepayment is attached to them. If there is an [Advertising Client Type](../../advertising/setup/client-types.md#client-type-defaults-setup) set on the client, then those defaults will override those that are set here.

## European Union Tax Settings <a href="#_toc70321841" id="_toc70321841"></a>

These are the settings for EU tax rules to be used or not, default values for EU tax code, EU tax exempt code and non-EU exempt code.

<figure><img src="../../../.gitbook/assets/image (87) (1).png" alt=""><figcaption></figcaption></figure>

## Client Budget/ Forecast Entry Restrictions <a href="#_toc458780187" id="_toc458780187"></a>

User can set dates where the budgets and/or forecasts cannot be changed after a certain date. These restrictions can be erased using the x red button. More lines can be added using the + sign and user can fill in more restrictions per different years.

<figure><img src="../../../.gitbook/assets/image (88) (1).png" alt=""><figcaption></figcaption></figure>

## Email Pay Link Settings <a href="#_toc124065024" id="_toc124065024"></a>

This section is only for Naviga clients licensed to use the Client Portal.

See [Pay invoices with Credit Card](../payments-and-credits/#pay-invoice-with-credit-card) for details on using the paylink function.

<figure><img src="../../../.gitbook/assets/image (89) (1).png" alt=""><figcaption></figcaption></figure>

* Enter the desired amount of time to allow this link to be valid for (in days minutes and hours). 999 is the limit in any of the fields, but if you set minutes to 999, it will automatically expand that out to 16 hours and 39 minutes, entering 999 in the hours field will expand that out to 41 days and 15 hours. (And, if you enter 999 in the days field, you might want to re-think your credit policies)
* Enter the desired default Subject Line text
* Using the Design and HTML tabs at the bottom, create your desired default text. Here is our sample HTML from above:

{% code overflow="wrap" %}
```html
<p style="font-size: 16px"><a style="font-size: 16px; font-weight: bold" href="#LINK#">Click here</a> to view your and process your payment. <br>
<br>
</p>
```
{% endcode %}

The only tag available for this template is the <mark style="color:blue;">#LINK#</mark> tag which will give you the URL for the temporary link

If you are using multiple profiles, the above messaging can be overwritten in the [Portal Setup ](../../../portals/advertiser-portal/#quick-pay-setup)if you choose to have different text per portal profile.

## Credit Card Options

<figure><img src="../../../.gitbook/assets/image (1706).png" alt=""><figcaption></figcaption></figure>

1. Prompt to Save Card on File - This is a Yes/No flag that is set to no by default. If you would like to use in production it will need to be tested with your specific credit card gateway to ensure compatibility. Different gateways offer different options.\
   \
   If set to yes, the user will be prompted in the credit card entry if that card should be saved for future use.

<div data-full-width="false">

<figure><img src="../../../.gitbook/assets/image (833).png" alt=""><figcaption></figcaption></figure>

</div>

Items 2 - 6 relate to the variable pricing by payment type feature. This is an add on for Naviga Ad which allows for a transaction fee to be charged based on the type of payment being taken. This affects payments taken on some screens in both the Advertising Module and the A/R module. There can be a different % fee for Card transactions than for Electronic Transfers like ACH. There is no fee for cash/check payments. In some areas of the world, this is a standard practice and in other areas it may not be allowed by your payment processor, so it is important to verify your terms with your processor prior to implementing. You will only see options 2 - 6 if your site has opted to add this feature to your system.

2. **Add Processing Fee** - set this to "yes" to add a processing fee
3. **Processing Fee Description** - This is the description that the customer will see on receipts
4. **Processing fee for Card Transaction -** set the % amount that will be charged for card transactions
5. **Processing fee for Electronic Transfers** - set the % amount that will be charged for electronic transfers.
6. **Processing Fee Class Codes for Card Transactions/Electronic Transfers** - See [Class Code Setup](../invoices/#\_toc65155656) in A/R Module for setup details. The Class Code selected here will determine the G/L allocation for these fees. This can be different per system company.
