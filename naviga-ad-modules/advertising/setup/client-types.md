# Client Types

## Client Type Setup

The client type setup screen allows you to define the names and IDs for the desired client types in the system. To create a new Client Type, enter an ID and a Description in the blank field and click the + to add. Click Save. To make a Client Type inactive that you don't wish to use anymore, click the inactive flag and save.

<figure><img src="../../../.gitbook/assets/image (1675).png" alt=""><figcaption></figcaption></figure>

When creating a new customer, or editing an existing one, you can select the appropriate client type.

![](<../../../.gitbook/assets/2 (32).png>)

You can set the system to display the client type in the list of search results. The setup is found in the System Settings module in the menu Setup -> Naviga Parameters.

![](<../../../.gitbook/assets/3 (35).png>)

**Show Client Type on Name Search Results:** This will show the kind of account it is - Either AD for Advertiser, AG for Agency, or CC for a Collection Agency. These are hard coded in the system and cannot be changed once an account is created.

**Show Advertiser Client Type on Name Search Results:** This will show the ID of the client type, so be sure to create ID's that are meaningful if you are going to display it here.

If you set both, it will appear like this in the search results:

<figure><img src="../../../.gitbook/assets/image (1429).png" alt=""><figcaption></figcaption></figure>

### Create Bill to in Order Entry

In one of our clients' markets it is common in Real Estate Advertising that the Real Estate Agent will place the order for advertising the home for sale, but the invoice goes to the home owner directly for the ad.

To accomodate this workflow, there is a flag on Client Type Setup:

<figure><img src="../../../.gitbook/assets/image (1657).png" alt=""><figcaption></figcaption></figure>

For any advertisers with a client type that has this flag set, there will be a search and + sign next to the bill-to information in order entry:

<figure><img src="../../../.gitbook/assets/image (1176).png" alt=""><figcaption></figcaption></figure>

Click on the magnifying glass to find a bill to account that already exists in the system, or click the plus to add a new bill-to.

User will be prompted to enter account details below:

<figure><img src="../../../.gitbook/assets/image (1676).png" alt=""><figcaption></figcaption></figure>

The Bill-to account will get it's credit terms and other defaults from the A/R System Setup. (A/R Module -> Setup -> Admin -> A/R System Setup, Client Defaults section.)

Note that the Invoice Delivery Method is selected in here. If email is selected, the email address will be put in two places -

1. in the Name and Address setup node of the Name Maintenance Tree (Email Addresses section)\
   ![](<../../../.gitbook/assets/image (1677).png>)\\
2. In the Advertising Setup node of the same Name Maintenance Tree (Billing Contact section). It will be entered as a Manual Contact type since this is not an actual contact person that can be selected from the dropdown.\
   ![](<../../../.gitbook/assets/image (1678).png>)\\

## Client Type Defaults Setup

If you wish, you may apply client defaults to each Advertiser client type, these will overwrite the system wide defaults (from the A/R System Setup) which will only apply to clients where the client type has been left blank.

<figure><img src="../../../.gitbook/assets/image (741).png" alt=""><figcaption></figcaption></figure>

1. **Default Payment Terms:** See [Payment Terms](../../accounts-receivable-credit-control/setup-a-r-system-setup/system-tables-setup-a-r.md#payment-terms-setup) Setup. This will set a default for this type of Client
2. **Default Tax Code:** See [Tax Setup](../../accounts-receivable-credit-control/setup-a-r-system-setup/system-tables-setup-a-r.md#tax-setup). This will set a default tax code, if desired.
3. **Default Credit Limit:** Set a default credit limit, if desired.
4. **Default Credit Rating:** Free format text field to set a default rating
5. **Credit Stop Days (Ad):** This is the number of days an invoice can age before the account will no longer be able to place (confirm) ads. A user with permissions can override that and confirm anyway.
6. **Default Customer Credit Control Status:** See [Collections Setup](../../accounts-receivable-credit-control/credit-control/collection-letters.md#collection-letter-defaults)
7. **Default Services Charges:** See [Service Charges](../../accounts-receivable-credit-control/invoices/service-charges.md) Setup
8. **Default Show Due / Discount Date on Invoice:** Yes / No field to show or not show the Due Date on the invoice
9. **Auto-Approve New Clients:** Options are Yes / No / Yes, if required fields are set. The required fields are specifically referring to the Norweigan-specific setting on Country setup relating to their Tax ID and Registered Company Number, and will not be relavant for most Naviga Users.\
   ![](<../../../.gitbook/assets/image (589).png>)
10. **Prepayment Required for Advertising Orders:** If set to Prepayment Required, any campaigns for this client will not be able to be confirmed unless a prepayment is present.
11. **Actuals Billing Method:** This is the default and can be overwritten for an advertiser or for a campaign.\
    **No Caps:** Meaning the amount billed to the advertiser is based on the actual count of impressions of the ad, regardless of the source being Ad Server Impressions, or Third Party and so forth. If the client ordered 100,000 impressions and 101,000 were delivered. The order will be billed at 101,000 impressions.

    **Capped at Total Goal:** Meaning there is a cap placed on the total amount on the campaign after entering and saving the actuals for all but the last line in the campaign. In this case, if the campaign is running over the course of several months, each month can be reconciled based on the actual impressions, except for the final month, which will be adjusted to add up to the campaign total amount regardless of the number of actual impressions in that month. So, the advertiser is not overcharged over the promised the campaign total.

    **Capped at Individual Monthly Goals:** This option is the old “Yes” value on this field. It has every month actual amount capped regardless of actual impressions on a line. This results in the same amounts per month charged to the advertiser regardless of the actual impressions in that month.
12. **Actuals Reconciliation:** This is the default and can be overwritten for an advertiser or for a campaign.\
    **Use 3rd Party Numbers** - This will set the "Actuals" billing number to be based on the numbers provided by a third party (commonly used for Agency billing).\
    **Use Estimates** - This will use the original estimated counts for billing regardless of what was actually delivered.\
    **Use Ad Server Numbers** - This will use the counts provided by the Ad Server for the Actuals billing number.\
    **Use Ad Server Viewable Numbers** - This will use the viewable impression counts provided by the Ad Server for the Actuals billing number.
13. **Client Group:** See [Client Group Setup](../../accounts-receivable-credit-control/setup-a-r-system-setup/other-a-r-setup-menu-items.md#client-group-setup)
14. **Generate Statements:** A yes/no flag to default the client to receive statements or not.

All of the above defaults can be overwitted on an account by account basis. Once the account has been created, changing the Client Type will NOT re-set these settings on the account.
