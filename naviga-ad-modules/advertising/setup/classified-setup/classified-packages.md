# Classified Packages

You can then create various packages and choose to attach a template to each along with prices.

You have some different options available to you for Classified Self Service Packages vs what you can offer to Internal system users, so those will be explained separately.

## For use Internally

Click the + to create a new package, enter the ID, Description, and choose the product group to attach to this package so that when in order entry screen, this package displays only for this product group.

You can optionally choose a template from the drop-down menu to limit the template that can be used for this package. During order entry then this package will be selected and the user won't be able to change it.

Can enter from and to dates to limit when this package can be used.

You have the option to make each package a flat fee or dynamic pricing. If flat fee is chosen, enter the flat amount in the next field.

The “Prompt for Product Selection” if set to “Yes” the system will prompt the user in line item entry to choose one or more products. (The products in the grid below will be what is offered.)

The field “Minimum Product Selection Allowed” can be blank and this will force the entry user to choose one product. You can enter 1 or more to force the user to choose at least this number of products in the campaign.

Check the box “Prompt for Package Multiplier” to “Yes” and this will prompt the entry user to multiply the lines on the entry screen. This option offers the user the option for how many times the ad will run. For example, you might have a package that is specifically for a 2 week run. In the Number of days in the product section at the bottom might then be displayed for 14 issues (of a daily) or 2 issues (of a weekly)...and then the multiplier wouldn't be needed. But suppose for example, you wanted to leave it up to the customer how long they wanted to run the ad. Instead of creating a bunch of packages for different durations, you could select the package multiplier option and set the products to just be for a single issue. If the customer wants a 14-day run, the user enters 14. if they only want one day, then the user selects 1.

You can then choose the products from the drop-down menu, enter the number of days or number of issues to run the ad, the interval (days weeks or months), and you can also check the boxes for any dates to which to restrict the ad to running.

{% hint style="info" %}
In the below example, if weeks was selected instead of days, without any issue day restriction set, the behavior will be to run the ad for 3 consecutive weeks (one issue per week) starting from the start date of the package. The default will be the start date of the campaign, but prior to selecting the package, the user can select a different start date in the booking wizard.  The result will be to schedule 3 insertions on the same day of week as the start date.\
\
If months was selected in the package setup, the behavior would be to run one issue per month on the same day of month as the start date, so if the start date was the 14th day of the month, the result would be to run for 3 months, on the 14th of each month.
{% endhint %}

You can now save.

<figure><img src="../../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Creating a package as shown above, with dynamic pricing, the price of the ad will be picked up from the template selected.

If you instead create a flat fee package, the product grid will change, and you will enter the rate card / rate line combination here, along with the fee for each line. The fee entered here should match the flat fee price on the ratecard line chosen and it should total up to the Flat Fee amount for the package.

<figure><img src="../../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

If you check the box for flat fee, then you will not have the option to remove lines in the campaign entry.

### Classified Package - Copying

When creating a new Classified Package, there is an option to copy an existing package. This will save some setup time when creating similar packages.

<figure><img src="../../../../.gitbook/assets/image (264).png" alt=""><figcaption></figcaption></figure>

1. Navigate to Setup -> Classified Order Setup -> Classified Package Setup
2. Click the + to create a new package
3. Select the Copy button
4. a Copy dialog box will open
5.  Select the tree and package you are copying from, and then click Copy\\

    <figure><img src="../../../../.gitbook/assets/image (507).png" alt=""><figcaption></figcaption></figure>
6. Close the window
7. _**Enter a new ID for the new package**_
8. Modify other details as needed for the new package
9. Select Save at the bottom of the screen

## For use in Classified Self Service Portal

These are the differences from above when you are creating the package for Self Service:

* Self Service portal does not allow for Product Selection options or the Package multiplier option
* Self-Service package must have a template selected. If you wish to offer multiple styles in Self Service you can use the other optional templates or you can have separate packages.
*   If using a flat fee package, a couple of things to note below:\
    \- Flat fee Package flag is set\
    \- Rate card and rate line is selected below\
    \- Values entered here must in the lines must total to the "Flat Fee Amount" at the top.\
    \- If you aren't finding the rates you expect in the dropdown, check in your rate setup. The Ad Type on the rate must be set up as a Flat Fee type, with the listing flag set to yes, and the Send to plan flag set to yes if it is a print line and if you use Naviga Plan)\\

    <figure><img src="../../../../.gitbook/assets/image (336).png" alt=""><figcaption></figcaption></figure>
*   Click on the "online Options" tab and fill in text to describe the package for the online user. Here is a sample of the text entered on this tab:

    <figure><img src="../../../../.gitbook/assets/image (1588).png" alt=""><figcaption></figcaption></figure>

    On the portal, the above package displays like this:\\

    <figure><img src="../../../../.gitbook/assets/image (1183).png" alt=""><figcaption></figcaption></figure>

The first product that is entered on the package will be the product whose column measurement will be used for the preview for the customer when they are creating the ad. If it is a web-only package that does not have a column measurement, then the “Web-Only preview width” that is entered on the Online Options (described below) will be the width for the preview. The Web-Only Preview Width is in pixels.
