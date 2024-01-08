# Other Production Reports

In addition to the various ["Production by ..." Production Reports](./), there are several others that might be useful to your users. These are described in this page.

## Inserts Report

The inserts report is meant to provide a listing of all the Inserts / Preprints for a given issue date, broken down by Zone

<figure><img src="../../../.gitbook/assets/image (1488).png" alt=""><figcaption></figcaption></figure>

Enter the Product and Issue Date desired and click Get Data. By default it will be grouped by Order Line, but that can be edited as needed. This gives a breakdown of each dimension's count for each Zone. This information can be downloaded to Excel or pdf if needed.

## Ad Index Repot

The Ad Index report displays a list of the Campaigns, Order Lines, and Advertiser for any given Product and issue.

<figure><img src="../../../.gitbook/assets/image (477).png" alt=""><figcaption></figcaption></figure>

If using Naviga Plan in addition to Naviga Ad, the page numbers will be updated automatically once the plan has been saved in Naviga Plan. If using a different system for layout, these might be updated manually in the Update Page Numbers in an Issue Report or via Interface.

## Update Page Numbers in an Issue

This is where you can view and edit page numbers and tearsheet URL in an issue. In the Product dropdown you will see a list of Print Products. Select desired product and issue date

<figure><img src="../../../.gitbook/assets/image (574).png" alt=""><figcaption></figcaption></figure>

If a tearsheet URL is added into the tearsheet field, then on the client's invoice or on the Advertiser Portal, you can view the tearsheet image. On the invoice it will be a link to the tearsheet. One the portal, it will be an icon on the order list of Past Print Orders that the user can click on and see the tearsheet.

## Tearsheet Contacts Report

The tearsheet contact report looks at the tearsheet contact on either the brand or a campaign that has been changed since the date selected.

<figure><img src="../../../.gitbook/assets/image (1548).png" alt=""><figcaption></figcaption></figure>

Naviga Ad does not directly send notifications or emails with tearsheets. The tearsheet information is either sent out through an interface to a 3rd party, or it is included as a link on the invoice. If working with a 3rd party, the information can be added to a campaign here, and Interface Link will pick up the information and pass it downstream to the tearsheet provider:

<figure><img src="../../../.gitbook/assets/image (725).png" alt=""><figcaption></figcaption></figure>

To have this information get used on every campaign, the details can be added to the [Brand](../customers/brands/#tearsheet-contacts).

Naviga Plan Viewer

If you are using Naviga Plan, you can optionally allow Naviga Ad users who do not otherwise have access to Naviga Plan to view the layout. This is a read only view, but a rep or other Naviga Ad user can see what the plan looks like. It can be viewed with just Ad Info boxes, or it can be viewed with the actual images of the ad.

<figure><img src="../../../.gitbook/assets/image (182).png" alt=""><figcaption></figcaption></figure>

1. Select the number of spreads you would like to see in each row.
2. Select to see Images or not
3. Select the Product and issue Date
4. If there is an edition, select it.
5.  The Line ID is there in case you don't know the other information. In this example, I have placed the line id (including the insertion number) and it shows the plan, even without the other details:

    <figure><img src="../../../.gitbook/assets/image (721).png" alt=""><figcaption></figcaption></figure>

    The bottom left corner of the viewer will show the name of the plan and the date that the system last checked for updates:

    <figure><img src="../../../.gitbook/assets/image (1608).png" alt=""><figcaption></figcaption></figure>

In this case the plan name is the Product and Date. NAV13 is the product ID and the issue date is Oct 21, 2022

## Editorial Issue Management

For some Naviga clients, e-newsletters are managed in their content or audience systems. In other cases, their workflow is very much a tedious manual process. This report is meant to be used to alleviate the manual process that some of our customers are going through. For those who already have systems doing this, you can certainly continue to do so. Check out our webinar on e-newsletters:

{% embed url="https://dev.navigahub.com/mothership/resources/videos/NewsletterBestPracticesSchedulingAds.mp4" %}

### Editorial Stages and Controllers <a href="#_toc531451671" id="_toc531451671"></a>

Issue-based and date-based digital products can have assigned to them editorial controllers and editorial stages. The stages are pre-set in the Setup menu and serve to manage Editorial Workflow associated with Date-Based and Issue-Based products, like e-newsletters. Editorial Workflow stages are displayed in the Production Calendar for Date-Based Products.

To setup the editorial stages, navigate to the menu Setup -> Editorial Workflow Stages Setup. Enter a description for each stage and choose the color in you want the stage to appear and click on the + sign to add it to the list. Repeat the process to add more stages and then save.

<figure><img src="../../../.gitbook/assets/image (1211).png" alt=""><figcaption></figcaption></figure>

Navigate to the menu Production -> Editorial Issue Management. Choose the type to report by to be the product or the group to which the issue based product belongs.

<figure><img src="../../../.gitbook/assets/image (869).png" alt=""><figcaption></figcaption></figure>

Choose a date range for when the products have issues. Choose the order statuses to include to be Quotes or not and choose to include Editorial Statuses flagged as Completed, or not. Click the “Refresh” button.

The screen displays the list of products, issue date, type being scheduled dates or custom dates, the issue description if available, the close date, the editorial controller, the editorial status and the order count for the product.

To change the controller assignment for any of the orders, choose the controller from the drop-down menu corresponding to the product. Also, choose the editorial status to match the order from the corresponding drop-down menu.

When finished, click on the “Save Changes” button.

![](<../../../.gitbook/assets/3 (50).png>)

Note that the you can do a bulk change on the controllers per product and issue by clicking the button “Bulk Update Controller Assignment”.

![](<../../../.gitbook/assets/4 (6).png>)

The pop-up screen allows you to replace one controller with another. Click Apply and then click Save Changes to store the bulk updates.

You can do the same process to bulk update the editorial status on any of the issues.

## Production Calendar for Date-Based Products

Also see [Inventory section ](../campaigns/inventory-checking.md#production-calendar-for-date-based-products)for this report

Navigate to the date-based products calendar in the menu Production -> Date-Based Product Production. Search on the group or product which is date-based. Enter a date range search where orders exist for this publication.

![](<../../../.gitbook/assets/5 (20).png>)

The screen reflects the calendar agenda for each issue, including the number of orders in the boxes color coded for the different available spots and order statuses. Hover over the last column next to the publication name and the system gives you details of the editorial status, who the issue is assigned to and any editorial notes added if any.

Click on any of the agenda items and a pop-up screen displays.

![](<../../../.gitbook/assets/6 (47).png>)

The screen gives you the options to “View Issue/ Event Detail” or “Filter to These Orders”.

Click the “View Issue/ Event Detail”.

![](<../../../.gitbook/assets/7 (4).png>)

The pop-up displays the issue with the product details including the audience as per setup in the product setup page. It also lists the inventory available, total and orders under each status.

Click “Filter to These Orders” and the bottom half of the screen displays the orders in this issue.

![](<../../../.gitbook/assets/8 (13).png>)

Accounts by Controller

The accounts by controller report gives a view of any Account/Brand combination that has been assigned to a specific Controller.

Select the Controller from the dropdown in the top right

{% hint style="info" %}
Note: only Users marked as Production Conrollers in their User Security setup will be displayed in this dropdown.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (816).png" alt=""><figcaption></figcaption></figure>

## Change Production Controller on Brands

Navigate to Production -> Change Production Controller on Brands. This report will change the Production Controller that is set up on Brands OR on Products. (note there is a brand tab below and a Product tab.)

<figure><img src="../../../.gitbook/assets/image (922).png" alt=""><figcaption></figcaption></figure>

1. Select the desired Production Controller at the top and click Get Data
2. Select the desired Brands and/or Products
3. Select the desired New Production controller at the bottom. Choose to update future orders or not
4. Click Apply change

## Change Production Controller on Campaigns

Navigate to Production -> Change Production Controller on Campaigns. This report will change the Production Controller from one to another for Campaigns Ending on or after a given date.

<figure><img src="../../../.gitbook/assets/image (1631).png" alt=""><figcaption></figcaption></figure>

## Material Trafficking

The material trafficking dashboard is useful for sites who are integrated with preflighting software.

<figure><img src="../../../.gitbook/assets/image (190).png" alt=""><figcaption></figcaption></figure>

Select the product(s) desired from the top of the screen along with starting and ending issue dates. Select desired Preflight status(es) and click select data.

<figure><img src="../../../.gitbook/assets/image (258).png" alt=""><figcaption></figcaption></figure>

Report can be used to quickly locate materials which have failed preflighting so that they can remedy the issue, or can look for other desired statuses as well.
