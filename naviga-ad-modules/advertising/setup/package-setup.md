# Package Setup

Navigate to the menu Setup -> Package Setup. Create a new package by clicking the “New” button.

![](<../../../.gitbook/assets/1 (79).png>)

**Template Description:** Enter the description of your package to assist the order entry user while choosing this on the Quick Line Entry screen.

**Valid From/To:** Enter the dates during which this package is Valid. If this date range falls within the campaign start date, the system then displays this package. Otherwise it won’t appear for the order entry user to use.

**Currency:** Leave the Currency field blank if this is local currency. Otherwise choose the foreign currency from the drop-down. The package appears only on campaigns using this currency.

**Client Types:** Enter the Client Types that are allowed to use this package. Leave blank to allow for all client types.

**Category Tree/Category:** Entered desired Category Tree and Category (see [below ](package-setup.md#\_toc99541349)for more details)

**Do not allow line deletion in order entry:** Select “Yes” if you don’t want the order entry user to have flexibility in removing lines from the package during order entry.

**Do Not Allow Price Changes in Order Entry:** Check the box to “Yes” if you don’t want the order entry user to have flexibility in changing the price on the lines from the package during order entry.

**Prompt for Product Selection:** Package Setup allows for prompting user in order entry to choose one or more from the products on the package

**Minimum Product Selection Allowed:** Used in Conjunction with the item above. For example, if the user is presented with a list of 7 products on the package and they are required to select at least 4 enter a '4' in this field.

**Prompt for Package Multiplier:** allows user to multiply the lines on the package. (For example if the package is created for one issue date on each product and the client would like 3 issues, enter a 3 in the multiplier field to schedule it for that many dates.)\
Package Multiplier and Product Selection fields can be used together or independently.

![](<../../../.gitbook/assets/2 (28).png>)

**Internal Note:** Enter a note description if you wish which will be viewed only by the user at the order entry and not by external clients.

Save the settings to the package setup.

Scroll to the Products shutter and choose a product from the "Add a product" drop-down menu.

![](<../../../.gitbook/assets/3 (43).png>)

You can choose then the section and position and click the + to add the line. You can also leave Section/Position blank at the bottom at choose them in the Product grid along with the other attributes.

Select the appropriate Ratecard, and Ratecard line, as well as section and position.

Date Selection Types:

<figure><img src="../../../.gitbook/assets/image (779).png" alt=""><figcaption></figcaption></figure>

* Specific Issue or Date Range: This allows for selecting an issue (for print/issue-based digital products) or a date range for digital products. You can also limit to specific days of the week. You can leave this blank and the system will put it in the next available issue based on the campaign start date.
* Days / Issues from Campaign Start: This uses relative days. In the example above the Mobile App line is using this type. It is 0 offset days and 30 issues or days. That means this will start on the same day the campaign starts and will run for 30 days.
* Days / Issues from Previous line: This looks at the row above. The 2nd Navigator Magazine row uses this. The first Navigator Magazine is starting on a specific date and running a full page ad. The second one will start in the next available issue after that and run 3 times.

Adjust Ad Type, Rate and Quantity as needed to make the package line as specific as possible, or choose the product, rate and quantity without a Ratecard.

Note the following rules:

* If Client Type is used on Package, only rate cards that have ALL the Client Types on the package are available for selection.

{% hint style="info" %}
If that made you go, "huh?" Don't worry - makes more sense with an example - If you are creating a package that is allowed to be used by both National and Local client types, but the rate you are looking for is only allowed for National client types, you can see why that wouldn't work out well....so those rates that won't be valid are filtered out from the selection dropdown.
{% endhint %}

* Select rate cards carefully, all rate cards (aside from above exception) are available for selection.
* If a Rateline has expired, it will be removed from the package lines on the campaign even though you may see it in the initial entry of the campaign lines.

When finished click the + sign and keep repeating adding lines. When finished with creating the package, click the save button.

## Category and Category Tree in Packages <a href="#_toc99541349" id="_toc99541349"></a>

User can enter Category and Category Tree Information in Packages Setup screen. This saves user effort when entering the package where the system defaults these category values in the line item.

Navigate to the menu Setup -> Package Setup.

![](<../../../.gitbook/assets/4 (28).png>)

Enter the new package details or edit an existing one and choose the Category and Category Tree from the drop-down menu. Enter the corresponding lines in the package which apply to the Category and Category Tree selected above.

Navigate to enter a campaign using Quick Line Entry and use this package.

![](<../../../.gitbook/assets/5 (13).png>)

The Category and Category Tree fields default in the line entry.

Campaigns built from a package store the package Id on each line item.

## Copy Package <a href="#_toc59107281" id="_toc59107281"></a>

User can copy packages into an existing package to replace it or into a new package and then edit as needed.

Navigate to the menu Setup -> Package Setup. Choose an existing package from the system. Or you can choose to click “New” to create a new package into which you can copy another one’s details.

Then Click “Copy”.

![](<../../../.gitbook/assets/6 (35).png>)

Choose the package you’d like to copy from the drop-down menu and click copy.

A new screen containing the copied package’s details display. Note that the existing package on the screen retains only its ID, and all its details are replaced by the package you copied.

You can then proceed to edit the description, the dates, and the lines details of products to include in the package. When finished click “Save”.

You can then proceed to use the copied package in orders.

If you copy into a “New” package, the details of the copied package display in the new package and a new ID is generated for this copied package. You can then edit the details as you wish.

## Using Package on the Advertiser Portal

The middle section on the Package setup pertains to allowing this package on the Advertiser Portal.

<figure><img src="../../../.gitbook/assets/image (658).png" alt=""><figcaption></figcaption></figure>

**Offer this Package on the Portal:** Click Yes to enable this package to be used on the Advertiser Portal

**Short Description for Portal:** This is displayed at the top of the box in the "Description" Column

**Logo Path:** URL to the logo as displayed to the left of the Package Description

**Valid Until:** The package will disappear from the portal if this date is before today. This package will also disappear from the portal if the inventory if no longer available for the products in the product list.

**Product Group:** Select the product group for this package. If using profiles in the portal, this could cause certain packages to be shown or hidden depending on which profile the client is in and whether or not you filter out certain product groups.

**Long Description for Portal:** This is a client-friendly description of the products that are being offered. Can use the Design and/or HTML tabs in the editor window to create the design.

This is how the above package appears on the Portal:

<figure><img src="../../../.gitbook/assets/image (1642).png" alt=""><figcaption></figcaption></figure>

If desired, below is the html for the above description.

{% code overflow="wrap" lineNumbers="true" %}
```
<p>Running Now through the end of the month:</p>
<ul>
    <li>100,000 Guaranteed Run-of-Site Impressions on our&nbsp;<span style="text-decoration: underline;">Demo Website 1</span></li>
    <li>100,000 Estimated Run-of-Site Impressions on our&nbsp;<span style="text-decoration: underline;">Demo Website 2</span></li>
    <li>25% Share-of-Voice on our&nbsp;<span style="text-decoration: underline;">Demo Mobile App</span></li>
    <li>10 evenly paced Instagram and/or Twitter endorsements from our&nbsp;<span style="text-decoration: underline;">Demo Social Media Audience Engagement</span>&nbsp;team</li>
    <li>250,000 pre-roll impressions on our&nbsp;<span style="text-decoration: underline;">Demo Video Channel</span>&nbsp;team</li>
    <li>Up to 50 lead pass-throughs from our&nbsp;<span style="text-decoration: underline;">Demo Lead Generation Service</span>&nbsp;team</li>
</ul>
<p style="color: red;">This package would normally cost you $4,000 - on sale now for just $2,750 - that's more than 30% off!</p>
<p><a href="http://www.navigaglobal.com/" target="_blank">Click here for Spec Details</a></p>
```
{% endcode %}

Note about using the Package in the portal - The portal packages are set up for specific dates and the issue date in the package product details must be after the Valid Until Date in the setup.
