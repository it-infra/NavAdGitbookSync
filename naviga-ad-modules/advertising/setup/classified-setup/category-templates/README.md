# Category Templates

## Category Template <a href="#_toc116920283" id="_toc116920283"></a>

A site can define multiple templates for each Category and/or Sub-category. For example, there could be a Good, Better and Best option that uses the HTML or InDesign templates.

Click the node “Category Template”. Choose the tree and click + to create a new template. Enter an ID and a Description. If this template is to be made available on the Classified Self-service portal, the Portal Description field can also be filled in to display an alternate description to external users. If this is only valid for certain categories, select them in the Categories allowed. Otherwise, leave that blank and the template will be usable for the entire Category Tree.

{% hint style="info" %}
When creating multiple templates for the same category, once you click the + to create new, you can save time by copying a previous template and then making modifications to that instead of creating a brand new template each time. See Instructions below for [Copying templates](./#copying-templates)
{% endhint %}

<figure><img src="../../../../../.gitbook/assets/image (1314).png" alt=""><figcaption></figcaption></figure>

Select Template type of HTML if you will be using HTML to create the template. If you have HTML expertise, you can create the design in the editor using the <> icon in the editor window. If you need some assistance getting started try looking at the sample templates provided in the left navigation.

Please contact Naviga Support/Implementation for more assistance as needed.

Note that you can integrate with In Design by selecting InDesign as the Template type. There is background setup needed to utilize InDesign Server to build from InDesign templates. So if you plan to go that route, contact Naviga Support or your Implementation specialist.

You do not have to choose one or the other. InDesign and HTML can each be used for diffent templates. Enter the template Type as InDesign if this is what you’ll be using and upload the INDD file needed. If using an Indesign-based template the HTML text editor (shown above) will disappear.

Regardless of Template Type, click the Sample Metadata Values and this screen provides a sample preview of the information to fill out in the order. Sample Meta Data Values and Sample Image are optional. If you fill out the Sample MetaData values, this information is stored and used to generate the Sample Image. The Sample image will then be displayed to the user in the Booking Wizard so they can see what the template is going to look like before they select it.

<figure><img src="../../../../../.gitbook/assets/image (829).png" alt=""><figcaption></figcaption></figure>

There is a “Download PDF” button on the Sample Image screen which is used when user creates a template in very small font sizes (5pt and smaller) that might be difficult to see on screen. The PDF feature allows you to download the PDF then zoom it in to verify that the template merge is valid and accurate. There is also the “Download JPG” button to download the image to the desktop to be viewed clearly.

<figure><img src="../../../../../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>

The Download sample data downloads the tags and the sample data in those tags to a json format. This might be helpful when designing the indesign template to ensure that you are using the correct metadata tags to create the content.

Click the node “Product Pricing” and/or "Group Pricing" to choose the various Ratecard + Ratelines to attach to this template, so that user can see these prices when they choose this package. We attach the price to the template so that you can offer good/better/best pricing to go along with good/better/best templates. If multiple Products share the same pricing, you might use the Group Pricing option. If each product has their own unique pricing, then you might use the Product Pricing tab.

<figure><img src="../../../../../.gitbook/assets/image (503).png" alt=""><figcaption></figcaption></figure>

You can select Clients in the Clients tab to limit this category template to these clients and not allow other advertisers to use it in order entry.

## Copying Templates

When creating a new Classified Template, there is a option to copy an existing template of the same category. This will save some setup time when creating similar templates. Since there are elements (like Metadata tags) that are really specific to the category that it is related to, we don't allow copying across categories, but can still be a timesaver when creating additional templates within a category.

<figure><img src="../../../../../.gitbook/assets/image (748).png" alt=""><figcaption></figcaption></figure>

1. Navigate to Setup -> Classified Order Setup -> Classified Category Template Setup
2. Click the + to create a new template
3. Select the Copy button
4. Copy dialog box will open
5.  Select the template you are copying from, and then click Copy\\

    <figure><img src="../../../../../.gitbook/assets/image (1558).png" alt=""><figcaption></figcaption></figure>
6. Close the window
7. _**Enter a new ID for the new Template**_
8. Modify other details as needed for the new template - perhaps there are different rates for this one, or perhaps the HTML is slightly different than the original one.
9. Select Save at the bottom of the screen
