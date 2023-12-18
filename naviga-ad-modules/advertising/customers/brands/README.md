# Brands

Naviga allows for a customer hierarchy of parent companies, advertisers and brands. For smaller advertisers, it would be most likely to set the customer to “no this advertiser uses one brand.” This can be set as a system default and overwritten only when customers do need multiple brands.

## Why should I use brands?

There are several benefits when creating multiple brands on larger, more complex customers:

1. You may choose to set up multiple brands to aid in reporting. I may wish to report on just sales to General Motor company. In that case I may set them to not use multiple brands. If I wish to report on sales to Buick, Cadillac, Chevrolet, and GMC it would be advisable to set up General Motors as an advertiser with Buick, Cadillac, Chevrolet, and GMC as brands. This would allow for large advertiser and year on year reporting at the GM level, or more detailed analysis at the brand level while eliminating the confusion of multiple advertiser records.
2. Separate brands are useful when an advertiser often bills to separate ad agencies. Procter and Gamble contracts with different ad agencies for Pampers than it does for Gillette. To simplify order entry and prevent errors it would be better to set up two brands than to have to remember to overwrite the bill to in order entry.
3. Name/address overrides can also be set at the brand level. A local restaurant chain may want their invoices to go to each store location, separate brands allow for an address overwrite.
4. In some cases, separate brands may assist with default salesrep relationships. Default reps can be set at the brand level for all products, they can be managed at the product group level and can even be managed at the product level. In most cases a single brand can support any salesrep assignment. Occasionally the same customer will deal with different reps for advertising in the same product. For example, you may wish to set up a display and a classified brand on an advertiser if they purchase both ad types in the same product and have different default reps for each ad type.
5. Brands can be set to display on the customer portal, or to be hidden from the portal. This allows you to choose if the hierarchy is primarily for your internal use, or if you also wish to expose it to the customer.
6. The setting to use third party actuals on performance based digital campaigns can be overwritten at the brand level. This setting defaults to campaign entry and flags the system to not bill based on the actuals that flow directly from the GAM interface, but to expect entry/import of actuals from a third-party verification.
7. Contracted default discount percentages can be stored at the brand level, applying automated discounts to ratecard lines in campaign entry.
8. The PIB/Industry/Category code is stored at the brand level. For a company such as PepsiCo it would be likely that you would choose to track a different product category on their soda brand versus their Quaker Oatmeal brand.
9. Each brand stores relationships with internal and external contacts. For example, the internal production controller and campaign manager can default on orders from each brand. The brand also stores external default production contacts at the customer.

The advertiser-brand relationship is extremely powerful in the system and displayed in most reports. Brands, and their associated orders, can be merged and can be moved from one advertiser to another.

In some cases, an advertiser-brand hierarchy may not be deep enough. One may wish to track that General Mills is the parent company of Betty Crocker whose brands include Chilled Treats, Baking & Cake Mixes and Bisquick. In this example you could set up Betty Crocker as the advertiser and General Mills as a parent company. While parent relationships do help manage a deeper hierarchy they are not as strongly supported in the system and display only on a limited number of reports.

## How do I create Brands? <a href="#_toc115259172" id="_toc115259172"></a>

In the advertising module, users can create a new brand on the fly from the order entry screen by clicking the + sign next to the brand field. This can be useful especially for a one-time used brand, and user can then maintain this brand from the brand maintenance screens.

![](<../../../../.gitbook/assets/1 (11)>)

Brand management is available only when you navigate to the Customers menu, navigate down to Brands menu then click Brand Maintenance menu. If you are already in the Advertiser / Agency Maintenance menu for an account, you can also get to it from the Advertising node, brands tab.

### Brand Detail

Enter the advertiser id or use the advanced search by clicking the magnifying glass.

Click New to create a new brand for this advertiser. Or choose from the drop-down menu to manage an existing brand.

You can click the box “Auto Assign” in order to allow the system to assign an automatic ID for your brand, or you can enter up to 6 characters. No special characters are allowed.

<figure><img src="../../../../.gitbook/assets/image (269).png" alt=""><figcaption></figcaption></figure>

Note that each advertiser can have one or multiple brands. Enter the brand name characters and choose the Industry Category/ PIB from the drop-down list.

Note the default discount % on digital campaigns is a default value which you cannot edit except where allowed by Group Security. This is the default value for a discount for a client allowed by the administrator.

If you are licenced for the Portal, you can click the respective box to change the value to “Yes”. This allows your clients to utilize the portal for managing orders and invoices.

To assign an agency to a brand, enter the agency settings. Enter the agency ID or search for the agency using the magnifying glass.

Choose Yes or No to remit. This impacts the billing, such that if set to “YES”, the invoice is sent in its entirety to the advertiser including the agency commission, which the advertiser in turn pays, followed by the user paying the agency commission. The Accounts Receivable and Accounts Payable reflect these amounts. If the Remit option is set to “NO”, then the advertiser receives the total invoice minus the agency commission which the user pays directly.

Choose the production controller for the brand. This value will allow the controller for these brands to view the relevant reports.

Choose the campaign manager for the brand. This value will allow the campaign manager for these brands to view the relevant reports.

Actuals Reconciliation: Use the default set on the account, or override it for the brand

<figure><img src="../../../../.gitbook/assets/image (1181).png" alt=""><figcaption></figcaption></figure>

Enter free text in the notes section as relevant to the brand and its maintenance. When finished, click on the “Save” button to store the data.

Brand changes are tracked in the advertiser account history of changes in the advertiser maintenance screen where once you make changes to a brand, the changes are tracked in the history of the account maintenance. The brand fields to be tracked are:

1. Brand Name
2. Agency
3. Remit-To
4. Industry Code
5. Inactive Indicator flag
6. Production Controller
7. Campaign Manager
8. Campaign Discount %
9. Actuals Reconciliation Flag
10. Rep Assignments
11. Production Contacts
12. Tearsheet Contacts
13. Override Billing Address Id
14. Billing Contact
15. Billing Email Contacts
16. Confirmation Email contacts

### Rep Assignments <a href="#_toc115259173" id="_toc115259173"></a>

Click the node “Rep Assignments” to assign a brand to a rep. You have the option to assign at the level of the brand, product group or product.

![](<../../../../.gitbook/assets/2 (10)>)

Note that the system aligns a brand with the rep on the order first, then on the brand setup, then on the product then on the product group.

You can edit the rep assignment in the section “Default Rep Assignment for this Brand” and check the box “Assign in Order Entry”, and the system will prompt the order entry user to choose a Salesrep for the order for this brand while entering the order.

![](<../../../../.gitbook/assets/3 (5)>)

You can edit this value several times anytime even after creating and billing orders. The orders which were already billed will not be affected, but any unbilled orders will be affected by the changes you make here.

### Billing Overrides <a href="#_toc115259174" id="_toc115259174"></a>

These settings override the brand settings for billing if the fields here are filled in.

Click the Billing Overrides node and you can then choose to select existing addresses and contacts from the available dropdowns for this advertiser as per the advertiser maintenance screen values.

<figure><img src="../../../../.gitbook/assets/image (1426).png" alt=""><figcaption></figcaption></figure>

Or you can use the + signs to create a new address or contact for billing.

#### Invoices

You can also override invoice email contacts for this brand.

#### Confirmations

You can also override confirmation email contacts for this brand. This is who receives confirmation emails generated from the campaign maintenance screen.

#### Creative Agency

You can also do the same to assign a creative agency to the brand. Creative agencies work on the materials and creative side of orders using this brand.

### Production Contacts <a href="#_toc115259175" id="_toc115259175"></a>

This is a node where you can define a production contact for orders of this brand. The production contacts are the names of people assigned to work on the production side of orders and will be reflected in production reports throughout Naviga Ad. If an order does not have a production contact, this will prevent you from running reports and sending reminders related to order’s production.

Click the Production Contacts node and note that you can choose a contact from the drop-down menu and enter a job description for this contact, then click the + sign.

<figure><img src="../../../../.gitbook/assets/5 (5)" alt=""><figcaption></figcaption></figure>

You can also add a new contact by clicking the “New Contact” button and entering the contact data.

You can also assign specific products to the contact so that when the order for this brand, and these products, then the order defaults this production contact to the order containing these products.

### Tearsheet Contacts

Select a contact from the dropdown or create a new contact person to be used in sending tearsheets. Naviga ad does not directly send tearsheets to customers, but these settings here are used in conjunction with Interface Link to send this information to a 3rd party. Like Production Contacts, Tearsheet Contacts can be set per product.

### Division Setup <a href="#_toc115259176" id="_toc115259176"></a>

This section affects the Exhibition module where the division is the same as the brand in the Ad module. If your advertiser uses the exhibition module, you can setup the division group and division in these nodes.

### Division Detail <a href="#_toc115259177" id="_toc115259177"></a>

You can use an existing brand from the Ad module and setup the different reps, billing information and contacts, or create a new division just for the exhibition module using the + sign. When an exhibition order is created using this division/ brand, these default values are applied to the order.

### Exhibition Group Overrides <a href="#_toc115259178" id="_toc115259178"></a>

Every exhibition group can have its settings as a whole which would override the exhibition division reps and contact information setup above in the division detail node.

### Orders <a href="#_toc115259179" id="_toc115259179"></a>

This node under List of Orders provide a list of orders for for this particular brand where the user can click the hyperlinks for further drill down into each order or contract.
