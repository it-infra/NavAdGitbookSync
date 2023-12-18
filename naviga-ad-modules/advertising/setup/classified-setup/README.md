# Classified Setup

Users can setup and book Classified Listing Ads on Digital First Platform

## Prerequisites to Booking Classified Orders <a href="#_toc116920274" id="_toc116920274"></a>

### Ad Types <a href="#_toc116920274" id="_toc116920274"></a>

Navigate to the menu Setup -> Advertising Setup -> [Ad Types](../advertising-setup/ad-types.md#\_toc111556102). Add the new listing Ad type ID, and description. For liner type ads where you are creating the text inside the Order Entry text editor, select "Listing Entry" equal to YES. For a classified display type ad, this will not be checked.

![](<../../../../.gitbook/assets/1 (7).png>)

### Classified Categories <a href="#_toc116920278" id="_toc116920278"></a>

[See Category Tree/Categories](category-tree-categories.md)

### Layout Maintenance <a href="#_toc116920284" id="_toc116920284"></a>

Click the menu Setup -> Advertising Setup -> [Column Layout Maintenance](../advertising-setup/column-layout-maintenance.md).

### Product Setup <a href="#_toc116920275" id="_toc116920275"></a>

#### Tie CLS Ad Types to the Product

Next, the Ad Type(s) can be added to the product(s) where they will run. This can be done from Product Setup or from Ad Type setup.

![](<../../../../.gitbook/assets/3 (31).png>)

Save the Settings

#### Tie Classified Categories / Layouts to the Product

Each product and Category can be tied to the layout template of your choice. Click the menu Setup -> Product Setup and then click the node Classified Categories.

Choose the product from the drop-down list and then use the Add Categories option at the bottom to add the appropriate categories in use for the product and click the + sign.

Select layout templates from the dropdowns to choose the corresponding layout to the category tree ID. This allows the system to generate the different creatives for the different line items in the same order.

Classified categories can also be limited to certain days of the week by Product. For example, perhaps in one product the Real Estate section only runs on Sundays and Tuesdays, even though other sections might run every day.

On Product Setup, the category node will allow Day of Week selections. If it runs every day, the field can remain blank

<figure><img src="../../../../.gitbook/assets/image (1046).png" alt=""><figcaption></figcaption></figure>

Save the settings.

Then when booking a liner order for that category (in Full line or Booking wizard), you will only see issue dates allowed for that category.

![](<../../../../.gitbook/assets/image (1428).png>)

For class display ads, the category might not be selected prior to the booking schedule being entered, so there we do a check upon saving the ad. If you selected invalid run dates for the category you picked, you will be prompted on save to remove them:

<figure><img src="../../../../.gitbook/assets/image (1515).png" alt=""><figcaption></figcaption></figure>

### Ratecard <a href="#_toc116920277" id="_toc116920277"></a>

Click the node Ratecards. Click the “New” button to create a listing ratecard.

<figure><img src="../../../../.gitbook/assets/image (863).png" alt=""><figcaption></figcaption></figure>

Enter the ratecard description. Use the option “Listing/ Liner Rates” for the Ratecard Type. Enter the date range of start and end when the ratecard is active. See [Ratecard Setup](../product-setup/products/pricing-rules/) for more details.

Click the button to add a new line and enter the description of the line, the Section/ Position, choose the newly created Ad type above, the G/L type, the base qty and rate. You can also choose the Overage rate for a line which is used when you’re entering a cost per unit and this is the extra charge to be added if you exceed this limit. This would be the base quantity x base rate. (For example the rate may be $X gets you Y lines, and every line beyond that is $Z/line.)

Click the Save button.

## Top of Category Feature in Naviga Ad and Naviga Plan <a href="#_toc116920290" id="_toc116920290"></a>

_Note: Requires Naviga Ad 22.5 (or later) and Naviga Plan build 138170 (Oct 10, 2022) or later._

First thing you will want to do is create an Adjustment. This can be done on the Product or the Product Group.

Just below the Ad Type filter is a “Plan Position Code” field. You can put anything you want in there. I named mine “FIRST.” It doesn’t matter what you call it, but what is important is that Plan will treat these codes alphabetically. So “FIRST” does come before “SECOND” but “FOURTH” would come after first but before SECOND. So just keep that in mind when you come up with your naming scheme. Typically, there won’t be many of these codes, and likely only will have one.

If you aren’t booking liner orders using metadata:

* This adjustment code can be manually added to an order at any time.
* Using Auto Adjustments, you can tie it to a Ratecard and Ratecard line, to have it auto-applied if you select the “category leader rate” perhaps.

If you are booking liner orders using metadata:

* This adjustment code can be manually added to an order at any time .
* Using a metadata question, you can ask, either with a yes/no question if there is only one option, or a dropdown where you can select First or Second perhaps. And then tie that answer to an automatic charge using Metadata Adjustments in Classified Category setup.

When this comes into Plan, the Integration will tell Plan what the Adjustment Position Code is. It will be blank and just treated as a normal ad and will sort alphabetically, or it will have a code in there and will be sorted at the top of the category. If there is more than one ad with the same position code, then it will sort first by the Position Code and then by the sort text.

Here is an example:

The job posting that starts out “Zoom Marketing” would typically be among last in the category but it is now first because it had a position code called “ffirst”.

The ad that starts out ZZZ Category Test is second in the list because it has a sort of “ssecond” and ss comes after ff.

All the remaining ads are in alphabetical order “Full Time Position” followed by “Full Time Salary” then “Full Time Supported” and finally “Seasonal Openings”.

There is nothing to configure in Plan to make this work other than setting it up in ad and having a Plan version that is dated newer than Oct 10th 2022.
