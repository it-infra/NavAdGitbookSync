# System Tables Setup (Ad)

Many of these are shared with the A/R Module -> Setup -> [System Tables Setup](../../../accounts-receivable-credit-control/setup-a-r-system-setup/system-tables-setup-a-r.md). This list will only define those that are unique to the Ad Module. See the A/R Module documentation for the other System tables

## Invoice Form Logos

Navigate to Setup -> System Tables Setup -> Invoice Form Logos.

This table stores the logos that will get called into Templates, such as the Invoice form and Order Confirmation Template.

<figure><img src="../../../../.gitbook/assets/image (1416).png" alt=""><figcaption></figcaption></figure>

At the bottom of the screen add an ID and a description for the logo, then click select and navgate to the location of the image on your computer and add it to the form by clicking the + sign. Click Save when you are finished uploading all desired logos.

## PIB / Industry Setup

These codes are applied to each customer and from there default into each campaign. (Technically it is stored on the Brand, because an advertiser with multiple brands could have different brands in different industries). By identifying customers by their segment of your market you can create statistical reports and analyze your sales by customer line of business. The industry code is a required field in the customer import, at least one default code must be set up. Industry codes may optionally be used to determine GL codes by customer line of business if one wishes to post separately to the GL by industry. You may choose to use standard codes such as PIB, SIC, NAICS or you may create a custom list of codes.

Navigate to Setup -> System Tables Setup -> PIB/Industry Codes

<figure><img src="../../../../.gitbook/assets/image (1184).png" alt=""><figcaption></figcaption></figure>

There is an import template for this on the "Import" node of this setup.

Download the template and fill in all the fields. Any missing groups are created at the same time the PIB Codes are created with the import.

<table><thead><tr><th>Field</th><th width="345.3333333333333">Description</th><th>Required?</th></tr></thead><tbody><tr><td>Code</td><td>10-digit Alpha Numeric field which is the ID for the PIB Code</td><td>Yes</td></tr><tr><td>Description</td><td>Description of the PIB Code</td><td>Yes</td></tr><tr><td>Group Code</td><td>10-digit Alpha Numeric field which is the ID for the PIB Group</td><td>Yes</td></tr><tr><td>Group Description</td><td>Description of the PIB Group</td><td>Yes</td></tr></tbody></table>

When importing, choose YES if you want to overwrite existing PIB Code. Choose No if you are adding new codes to the existing list.

If you choose to change PIB Codes, you can use the swap values function to change from the old value to the new. This change can take effect on Brands/Divisions, on Ad Campaigns and/or Exhibition Orders depending on which flags you set to YES.

<figure><img src="../../../../.gitbook/assets/image (1537).png" alt=""><figcaption></figcaption></figure>

## Currency Tracking

Navigate to Setup -> System Tables Setup -> Currency Tracking

You will see a list with all the Currencies that have been setup in the system. See [Currency Setup](../../../accounts-receivable-credit-control/setup-a-r-system-setup/system-tables-setup-a-r.md#currency-setup) for setting these currencies up.

Check the box for each currency you would like to be displayed and used throughout the system. Click on the “Save” button to store the tracking settings. See [Currency Tracking](currency-tracking.md) for further information on the functionality and the reports where it is used.

<figure><img src="../../../../.gitbook/assets/image (1373).png" alt=""><figcaption></figcaption></figure>

## External System ID Codes

Navigate to Setup -> System Tables Setup -> External Systems Setup

This table of External systems is used for [adding External IDs to Name Records](../../../accounts-receivable-credit-control/customers-a-r/#external-system-ids). The idea is that by using standard codes, it is easy to determine which External ID goes with which system.

<figure><img src="../../../../.gitbook/assets/image (1591).png" alt=""><figcaption></figcaption></figure>
