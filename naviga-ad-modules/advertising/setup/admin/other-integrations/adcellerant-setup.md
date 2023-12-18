# Adcellerant Setup

This document describes the integration basic steps with Adcellerant. Naviga integrated with Adcellerant, which is a third party specializing in digital advertising fulfillment, so that Naviga users can enter orders and bill them in Naviga, while connecting to Adcellerant to fulfill the delivery of the orders. Users must have an Adcellerant account and be logged into Adcellerant to benefit from the integration.

Naviga personnel will need to turn on this integration before you will be able to utilize it.

## Integration Setup

Navigate to Setup -> Admin -> Other Integrations -> AdCellerant Integration Setup

### Integration Settings

<figure><img src="../../../../../.gitbook/assets/image (818).png" alt=""><figcaption></figcaption></figure>

1. Click Yes to Enable the AdCellerant Integration
2. Use Production Environment: While testing, this should be set to No.\
   If you scroll down on the page, there are settings for both Production and Staging environments. If #2 is set to Yes, we will use the Production Settings. If set to No we will use the Staging settings.\
   ![](<../../../../../.gitbook/assets/image (247).png>)
3. How are amounts allocated across months on a line? If a line is running for multiple months, this setting will affect how the revenue is allocated.\
   a. Split the amount across months - allocate by days in month\
   b. Split the amount across months - with equal values in each month\
   c. Put the full amount in first month\
   d. Put the full amount in last month
4. Allow AdCellerant Line Items in the Reconcile Actuals Process - Yes/No - answer will affect whether you will see AdCellerant lines in the [Campaign Actuals Reconciliation](../../../campaigns/ad-server-syncing-reconciliation.md#\_toc105408229) Screen
5. Using AdCellerant Product in Opportunity, Proposals & Campaigns. Choice here are:\
   a. Allow Adcellerant linked Products to be used in Opportunities, Proposals and Campaigns\
   b. Allow Adcellerant linked Products to be used in Opportunities only\
   c. Do not show products linked to Adcellerant in Opportunities, Proposals or Campaigns\\

### Product Group / Profile Cross Reference

The system allows for multiple profiles to be created. This allows for different Products in Naviga Ad (and therefore different G/L mappings and companies) to be created for the same AdCellerant Products. This would typically be used in a large multi-company environment. If you have only a simple structure, you can link the same profile to multiple Product Groups. Create the profiles in the Product Cross Reference, and then come back to this screen to link the profile to the Product Group it belongs to.

## Product Cross Reference <a href="#_toc78989523" id="_toc78989523"></a>

If you are integrating AdCellerant to Naviga Ad, there is a setup screen for mapping the cross reference from AdCellerant products to Naviga Ad products. This must be completed before line items can be created from an AdCellerant Proposal via the API integration. To access this setup screen, Navigate to Setup -> Admin -> Other Integrations -> AdCellerant Product Cross Reference

The AdCellerant Product Key is populated automatically. It is a complete list of all the Products that AdCellerant offers.

For every AdCellerant Product that your site offers, you will need to set up a corresponding Product in Naviga Ad. Additionally, you can define Sections and Positions, as well. The structure will vary depending on the way your site groups and sells the AdCellerant Products. For example, you could create a unique Product in Naviga Ad for each row; or you might choose to create a Product for Display and Email to group several items under a single Product. You would be able to differentiate the types of Display or Email by defining unique Sections and Positions.

So, the first thing you have to do is create any new Products, Sections and Positions that you will need for the Cross Reference. This is done in the normal Setup screen for creating Print or Digital Products in Naviga Ad.

Once Products are created in Naviga Ad, come back to the Product Cross Reference and click the pencil icon beside an AdCellerant Product Key entry to view the Cross Reference Settings pop up. It will show the AdCellerant Product Key and allow you to choose the Product, Ad Type, Section, Position and Line Description.\\

<figure><img src="../../../../../.gitbook/assets/image (904).png" alt=""><figcaption></figcaption></figure>

The Ad Type must be a flat rate. This is due to the fact that Naviga Ad brings in the price that AdCellerant has determined for the Line Item. Naviga Ad does not re-rate the items that are created via the integration.

The Line Description will be used on Order Confirmations, Invoices, etc. So, this can be more descriptive than the internal Product Name or Section that is used in the Cross Reference. click next to move to the next AdCellerant product and match that product with your Naviga Product/AdType/Section/Position combination.

### Product Setup <a href="#_toc78989525" id="_toc78989525"></a>

The product used for this purpose will be a standard digital product

<figure><img src="../../../../../.gitbook/assets/image (1333).png" alt=""><figcaption></figcaption></figure>

In this example product, AdCellerant SEM was set up with a section of Search, and several positions beneath it for the different AdCellerant Search Products

<figure><img src="../../../../../.gitbook/assets/image (1080).png" alt=""><figcaption></figcaption></figure>

This is how it looks in the Product Cross Reference:

<figure><img src="../../../../../.gitbook/assets/image (1151).png" alt=""><figcaption></figcaption></figure>

### Campaigns <a href="#_toc78989526" id="_toc78989526"></a>

Login to Adcellerant first and then in Naviga Ad create the campaign and line items for this product. The system will then toggle you over to Adcellerant so that you can finish the work needed there. The orders can then be billed in Naviga Ad like any other product billing.

<figure><img src="../../../../../.gitbook/assets/image (763).png" alt=""><figcaption></figcaption></figure>

Create a Campaign Header following your site’s normal workflow. When you are on the Line Items screen, you will see two new fields Adcellerant Proposal ID and Adcellerant Budget. The Adcellerant Proposal ID field has a button to the far right of the field. Clicking that will launch the AdCellerant proposal builder in a new tab in your browser.

Tip: Make sure you have already logged into AdCellerant before you click the icon to launch the Proposal builder.

Once inside the AdCellerant screens, complete a proposal as you normally would. Once you Finalize the Proposal, the changes are updated in Naviga Ad.

<figure><img src="../../../../../.gitbook/assets/image (204).png" alt=""><figcaption></figcaption></figure>

In this example, three line items were automatically created in Naviga Ad for Display and Social Products. From here, you can save the Campaign with only AdCellerant Products, or you can add any other Products from Naviga Ad. This example shows three Print line items added after the AdCellerant Products.

If you want to see a walk-through of the order entry process, watch the video linked below. This was a joint webinar with Naviga and AdCellerant:

{% embed url="https://dev.navigahub.com/mothership/resources/videos/NavigaAdandAdCellerant.mp4" %}
