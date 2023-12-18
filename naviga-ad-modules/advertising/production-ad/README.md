# Production (Ad)

The Production dropdown menu in the Ad Module is where you will go primarily for managing the collection of materials, but also for some other production-related functions.

We'll start with the multiple "Production by..." reports. Depending on the user's Role, they might use one or several of these reports. They all offer essentially the same view, but there are differences in search options and in the functions that are available.

## Production by Product Group

Production by Product Group screen displays the list of orders by production status for a product group. The statuses displayed here are the Master Statuses, since this report shows orders from several different products. Configuration options allow user to customize the columns displaying on the screen and the excel export.

<figure><img src="../../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

Navigate to the menu **Production -> Production by Product Group**. Choose the group from the drop-down menu, and the date range of products. The dates entered can be the run dates (line dates) or they can be the Material Due Dates. Click on “Get Data”.

Click the box “Break by Month” to display the digital line items by month even from within the same order line. Print lines will already be broken out by issue date, so this flag only affects the digital lines.

Select Yes/No to Include quotes in the list. Selecting no will filter this list to only show Reserved and confirmed orders (including Invoicing Started status).

Scroll to the shutter “Configure Output” and move the columns from one side to the other to add them or remove them from the screen display. Drag and drop or use the up and down arrows to rearrange the order in the "Selected Grid Columns". Click “Save Configuration” to store this column display setting.

<figure><img src="../../../.gitbook/assets/image (825).png" alt=""><figcaption></figcaption></figure>

On the right side, you can do the same but for the excel export output of the data. Click “Save Configuration” to store the excel export column setting.

You can also create templates to run which you can save in the system to run without having to re-enter criteria each time. Please refer to the “[Orders by Product](../campaigns/campaign-reports.md#orders-by-product)” report for details on how to create and use templates.

The data in this report displays the orders and is color coded by status. Note that you can click the hyperlinks to the campaigns and line items for more details. Click the line ID to ad/edit material for this line, or also to change the campaign status of this line.

In the top right of the data grid, there is a dropdown with various functions.

![](<../../../.gitbook/assets/image (891).png>)

Select one or multiple lines (white checkbox on the far right of the line) and then select an item from this dropdown

1. Email selected Primary contacts: This allows you to email the "Primary Contact" on an order. ![](<../../../.gitbook/assets/image (1505).png>)
2.  Change Production Status of Selected order(s): This allows you to update the Production Status in Bulk for multiple orders. Note: if you have selected lines for more than one product, you will need to update each Product separately since Production workflows are configured at the product level. Optionally you can also assign an artist in this screen as well

    <figure><img src="../../../.gitbook/assets/image (411).png" alt=""><figcaption></figcaption></figure>
3. Generate Excel File of Custom Data Froms Data: Custom Data Forms allow you to configure custom fields that need to be filled in for a product. This is typically information required by production to actually set up the buy. For example if you have sold a custom eNewsletter sponsorship, you will need to provide details about the message, perhaps the audience, etc. These can be filled in on a custom form. For ease of setting these up in an external system, you can download the data in Excel format.
4. (Re)Sync to Naviga Plan: Sometimes it is necessary to send campaigns in Bulk over to Naviga Plan. This option allows you to do so for a group of products for a date range rather than one product at a time like you can do on the Production by Print Product report.

{% hint style="info" %}
Please use discretion when sending in bulk based on the number of products in the group and the volume of ads you generally have so as to not overwhelm the feed going to Plan. For example, if you have 100 products in your group and each product has upwards of 100 ads a day, perhaps it wouldn't be one of your better ideas to send 6 months worth of ads over at once.
{% endhint %}

## Production by Product (non-print)

Use this report for any non-print product, so Standard web products, Group products, and also date-based digital products like eNewsletters will be available in the Product dropdown.

Select a run date range and answer the question if you would like break lines by month or include quotes. Click Refresh to get the data.

Like the Production by Product Group Report, the Production by Product (non-print) also includes the template concept. You can create and save templates to run this report without having to re-enter criteria each time. Please refer to the “[Orders by Product](../campaigns/campaign-reports.md#orders-by-product)” report for details on how to create and use templates.

<figure><img src="../../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

The production statuses shown in this report are the production statuses configured for this product. Click on a production status to filter by that status or use a combination of filters on the left panel to narrow down the results.

The white box at the top of each column can also be used to further filter.

Select one or more lines to perform one of the actions in the top right box:

![](<../../../.gitbook/assets/image (746).png>)

The first three choices are described above in the Production by Product Group section. The last choice is to Download components. This choice will download all the component materials that have been linked to the material record assigned to the ad. It will download in a zip file with a separate subfolder for each order and material ID. This is handy if designing the materials manually in house. If integrating with a 3rd party ad building tool, it is likely that Interface Link will have passed the materials to that 3rd party and you wouldn't need to do it manually here.

## Production Control by Controller

This screen provides a list of orders by the controller name. Who the controller is can be determined either from the campaign header or from the product setup. Choose which you want from the Controller Assignment dropdown.

This report can be filtered by product group, can return only lines that will go to Plan, and can include/exclude quote orders. The "as of date" is looking at when the ad is running. So if I was running this report "as of" today's date, it will return rows for orders running now or in the future. The "Issue Date" column can be a little confusing because for digital lines, it really doesn't have an "issue" but rather a date range that it is running for. If you run this "as of" today and see some issue dates in the past, don't let it confuse you....that is likely a digital line that started in the past (the Issue date is the start date, but it is continuing to run, so it is displayed here).

The data is color coded according to the setup of colors of the Master Status in Production Workflow setup since this report will contain multiple products.

<figure><img src="../../../.gitbook/assets/image (1405).png" alt=""><figcaption></figcaption></figure>

Select one or multiple lines and choose an action to complele in the top right of the report details or click on a line ID, Campaign ID or Material ID to get to the details of that one line.

![](<../../../.gitbook/assets/image (236).png>)

A description of each of these is above in the above sections for Product Group and Non-Print Products. This report also gives the option to Change the artwork status. The artwork status is only used by sites that are also using the InDesign extension for creating materials.

## Production by Sales Rep

At some sites the Sales Person on an order is responsible for chasing the materials from the customer, so this report was created to give those reps an easy way to find their orders that are waiting for materials.

<figure><img src="../../../.gitbook/assets/image (949).png" alt=""><figcaption></figcaption></figure>

Filters at the top are for Sales Person, Date Type, Date Range, and Campaign Status. Like the other reports, this one can break digital lines into separate lines for each month if desired. This one will also show the Master Production statuses since the results will be across several products.

Select one or more lines and choose an edit option on the top right of the details. This reports allows for emailing the Primary Contact person or changing the production status..

## Production by Print Product

Again, conceptually similar to all the above Production reports, but this one is just for Print Products.

Two additional filters at the top that aren't on other reports: Include Classified ads and Display Children of Spaceholder ads.

Include Classified Ads will also include liner type ads. Typically this report is used for chasing materials of display type ads, so liners would typically be omitted from view here. But, this report is also handy for re-syncing lines to plan and if that were the case, you might have a need to re-sync multiple liner type ads.

Include children of Spaceholder ads will display the child ads in what we call "Spaceholder ads" (aka a ganged ad or parent-child ad). If you are wanting to link material to a child ad or update the production status of the child ad from this report, you will want to select this option so that the children are displayed and editable. Without this selected, child ads are only displayed as materials on the parent ad.

<figure><img src="../../../.gitbook/assets/image (1549).png" alt=""><figcaption></figcaption></figure>

Couple of additional features on this report that were not mentioned on the other reports above:

1. In the dropdown menu on the top right, in addition to the items that were described on other reports, you can also select to download press ready finals. For the most part, clients using external editorial systems for content will send their final artwork through to Naviga Plan for layout and then passed on to editoral from there. A few sites use Interface Link to send materials elsewhere. The other option is used more for a manual type workflow where someone wants to just download the ready materials for an issue. This option here will download the materials to a zip file on your local computer. The materials will be named for the material name of the final component. So this filename here:\
   &#x20;![](<../../../.gitbook/assets/image (436).png>)
2.  Generate XML option in the same menu will generate an XML file with material details for any selected ad in the list.

    <figure><img src="../../../.gitbook/assets/image (884).png" alt=""><figcaption></figcaption></figure>

The Print Production report also allows the option to display a thumbnail preview of the ad which makes it really handy to be able to see if material is assigned or missing. If you have pdf material marked as the final AND you have a jpg preview, you will see a thumbnail of the ad. If you have pdf material marked as final but you don't have a jpg preview attached, you will be a pdf icon displayed. If you do not have material or you have forgotten to mark it as final, you will see an empty preview icon.

<figure><img src="../../../.gitbook/assets/image (400).png" alt=""><figcaption></figcaption></figure>

Like the Production by Product Group Report, the Production by Print Product also includes the template concept. You can create and save templates to run this report without having to re-enter criteria each time. Please refer to the “[Orders by Product](../campaigns/campaign-reports.md#orders-by-product)” report for details on how to create and use templates.

## Production Reminders

Production controllers can send out production reminders for materials that are required.

<figure><img src="../../../.gitbook/assets/image (1434).png" alt=""><figcaption></figcaption></figure>

Select a Production Controller from the dropdown. It can be the Controller assignment on the Product, or the Production Controller on the Campaign. The production controller on the campaign can come from the Product Group Setup or it can come from the Brand setup. This allows you to have some general rules, but also provide some overrides, perhaps if a client needs some special white-glove treatment.

Add additional filters as needed. The report is already only looking at future ads that are missing materials. If you want to add additional date parameters, perhaps to only look at ads for tomorrow or next week for example, you can add date parameters to filter this down.

Ad Type, Product and Master stage drop downs will only be enabled after you run this first for at least a production controller. Those additional filters can then be added and run again to further filter the list.

<figure><img src="../../../.gitbook/assets/image (775).png" alt=""><figcaption></figcaption></figure>

Select one or more lines to send reminders to and you will see a pop up with some additional settings:

* Do you wish to CC the rep(s) on the order
* Do you wish to CC yourself
* Do you wish to alert the rep(s) on the order (an alert is a notification which will appear on the rep(s) homepage next time they visit that page.

{% hint style="info" %}
You can only send a production reminder to Clients where you have a "Primary Contact" defined and that contract has an email address. If there is no contact, the checkbox will be grayed out and you won't be able to select it.

See Production Workflow Setup for details on what gets sent to the client in this reminder email.
{% endhint %}
