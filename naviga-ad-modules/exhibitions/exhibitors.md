# Exhibitors

## Exhibitor Overview

In the Exhibitions module, navigate to Customers -> Exhibitor Overview. This is the same search as the Advertiser/Agency Inquiry Search in Advertising module or the Customer Account Overview in A/R & Credit Control Modules.

This will take you to a seach screen to find an existing customer account. Search by Name at the top, or on the advanced search tab you can search by Name and many other fields. Can also search by a credit card (last 4-digits and card type) on the Search by Card Transaction tab.

<figure><img src="../../.gitbook/assets/image (489).png" alt=""><figcaption></figcaption></figure>

Once search results are displayed click on the customer name or ID to open the Account Summary screen. Use the "History" tab to quickly select a recently accessed account (last 50 accounts displayed). The only difference in searching via the different modules is the tab that you land on when opening the account. When searching in Exhibitions, the screen will open up on the Exhibition Sales tab on the customer screen. Navigate to CRM or Accounting for additional related details. This displays all exhibition orders for this client over time and a chart at the top to visually see the client's exhibition spend over time.

<figure><img src="../../.gitbook/assets/image (801).png" alt=""><figcaption></figcaption></figure>

## Exhibitor Maintenance

This takes you to the Account's Name Maintenance Screen. For full details on all parts of this Maintenance Screen see the [A/R Module's Customer documentation](../accounts-receivable-credit-control/customers-a-r/#name-address-maintenance). In this section we will discuss the fields specific to Exhibition Setup.

<figure><img src="../../.gitbook/assets/image (1599).png" alt=""><figcaption></figcaption></figure>

### Exhibitor Details

* Main Address ID - Select an address to use as their main address. Click the pencil icon to edit the address or the + to add an additional address for the account.
* The following are read-only information about the account
  * Account Status - green if in good standing, red if the account is on credit stop.
  * Account Opened - date of when the account was first created
  * Last Updated - date when the account was last edited
  * Is this an Agency - flag to indicate if the account was created as an agency type account
* Use Multiple Divisions - if set to yes, the account will have an additional tab at the top to take you to the various divisions. If set to no, there will be a button beside it to open the division details. Divisions in Exhibitons is similar to a brand in advertising.
* [Exhibitor Type](setup/exhibition-code-tables.md#\_toc9435401) - drop down selection for the type of exhibitor this customer is.

### Billing info

* Proof of Insurance received - This is a flag to indicate if insurance proof has been received.
* Proof of Insurance valid thru - Date field to display when the current insurance will be expired. (note that this field is also displated read-only on the Account Overview screen in Sales CRM , on the Other tab)
* [Tax Code ](../accounts-receivable-credit-control/setup-a-r-system-setup/system-tables-setup-a-r.md#tax-setup)- this is the tax code used for exhibition orders.
* [Terms ](../accounts-receivable-credit-control/setup-a-r-system-setup/system-tables-setup-a-r.md#payment-terms-setup)- this is the billing terms dictating when an invoice is due.
* Delivery Method - this can be set to Print, Email, or both. The contact person is then selected below.

## Division Maintenance

This section affects the Exhibition module where the division is the same as the brand in the Ad module. If your advertiser uses the exhibition module, you can setup the division group and division in these nodes.

### Division Detail

You can use an existing brand from the Ad module and setup the different reps, billing information and contacts, or create a new division just for the exhibition module using the + sign. When an exhibition order is created using this division/brand, these default values are applied to the order.

<figure><img src="../../.gitbook/assets/image (1245).png" alt=""><figcaption></figcaption></figure>

The bill for this division may be different from the bill-to on the account. If so, set it here.

For any exhibition there are generally forms that must be filled out. This is where you set who the default form recipient is for this division. This can be overwritten on an order.

<figure><img src="../../.gitbook/assets/image (450).png" alt=""><figcaption></figcaption></figure>

A Sales person can be assigned for this division. The system supports up to 4 reps sharing the same account and splitting the commission.

<figure><img src="../../.gitbook/assets/image (1423).png" alt=""><figcaption></figcaption></figure>

In the default settings, add any preferred defaults for this division. This also can be overwritten on an order.

### Exhibition Group Overrides

Every exhibition group (product group) can have its own overrides which would override the following settings, exhibition division reps, and contact information setup above in the division detail node.

<figure><img src="../../.gitbook/assets/image (1254).png" alt=""><figcaption></figcaption></figure>
