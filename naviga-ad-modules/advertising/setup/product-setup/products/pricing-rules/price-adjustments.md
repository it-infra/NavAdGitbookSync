# Price Adjustments

## Price Adjustment Details <a href="#_toc117696619" id="_toc117696619"></a>

This node allows you to create options of price adjustments to apply to orders, such as discounts or additional fees which the advertiser must pay. You can prompt for a value or percentage or enter a fixed value or percentage.

{% hint style="info" %}
Price adjustments will adjust the rate on digital CPM lines - so if you are rating per thousand, your adjustment will be per thousand. if you need to do a flat price adjustment against a CPM line, it will need to be created as a separate flat adjustment line.
{% endhint %}

You can enter an override G/L for each line of adjustment to post this adjustment against the G/L account entered here. Override G/L is only permitted on Products where the "Split Lines" opton is checked.

<figure><img src="../../../../../../.gitbook/assets/image (1207).png" alt=""><figcaption></figcaption></figure>

Price adjustments can be created for a Product or for a Product Group. They can be copied from other products to save time in setup.

To create a new adjustment, slect "add a new line" from the top right.

<figure><img src="../../../../../../.gitbook/assets/image (793).png" alt=""><figcaption></figcaption></figure>

Insert At - will default to the next sequential number, but you can change that if you want to insert this adjustment somewhere else in the list.

Copy Settings From - will display the other Adjustments for this product so you can copy a similar adjustment and then simply make changes

Hide on Forms - select yes if you do not wish to display this adjustment on forms, like the invoice or order confirmation

Currency - only set this for a foreign currency. if it is for your base system currency, leave blank.

External ID - not a required field, but had some clients using our API with a need for a unique ID across all rate lines, so this allowed them to set that unique ID.

Description - this is what is displayed to the user when selecting the adjustment in order entry (and if shown on forms, also what gets displayed to the customer on the form.

Allow Description Override - Click yes if the user is allowed to override the description in order entry.

\+/- Values - Options include Can be positive or negative, must be positive, must be negative. If an adjustment is intended to be a discount, select must be negative. if intended to be a premium, select must be positive. If it is open ended, select either.

Value Type - Options include % of Gross, % of Net, or Amount - % of gross looks at the rate itself and applies the adjustment there. % of Net will apply the adjustment after other adjustments. Ad amount is just an adjusted amount off the rate. When amount is selected an additional field will be displayed - Prompt for Qty.

Prompt for Value Entry - Yes or No options as to whether or not the user will be prompted to enter an amount.

Amount Value - This is the default value of the discount. it might be a fixed amount, or the user might be able to adjust it depending on the answer to the Prompt for value option

Prompt for Qty - only displayed if the value type is Amount. Options here are yes/no/per insertion. Per insertion means that the system will apply the adjustment amount per insertion. yes/no sets whether or not the user can set a quantity for the adjustment when applying it or if it is assumed to be a 1x adjustment.

## Ad Type

If this Adjustment is only allowed on certain Ad Types, select one or more ad types from the dropdown.

## Plan Position Code

Enter a code here to have Plan sort items with this Adjustment code before other items. See ["Top of Category...."](price-adjustments.md#top-of-category-feature-in-naviga-ad-and-naviga-plan) below

## Section/Position

If this Adjustment is only allowed on certain Sections/Positions, select one or more from the dropdown.

## Override G/L

If this adjustment is to be applied to a different G/L than the revenue on the order, enter the override G/L here.

{% hint style="info" %}
Note, you must select the "split lines" option on product setup for this option to be honored.
{% endhint %}

## Application Rule

Options here are apply to first insertion, apply to last insertion, apply to all insertions. Note that this option is only allowed in the booking wizard. If you are in full line entry and you wish to apply an adjustment to only one of the issue dates, you will need to manually split that line to separate that date from the others.

## Inactive Flag

Check the inactive flag to no longer be able to use this adjustment in future orders.

## Top of Category Feature in Naviga Ad and Naviga Plan

_Requires Naviga Plan build 138170 (Oct 10, 2022) or later._

First thing you will want to do is create an Adjustment. This can be done on the Product or the Product Group.

<figure><img src="../../../../../../.gitbook/assets/image (282).png" alt=""><figcaption></figcaption></figure>

Just below the Ad Type filter is a “Plan Position Code” field. You can put anything you want in there. I named mine “FIRST.” It doesn’t matter what you call it, but what is important is that Plan will treat these codes alphabetically. So “FIRST” does come before “SECOND” but “FOURTH” would come after first but before SECOND. So just keep that in mind when you come up with your naming scheme. Typically, there won’t be many of these codes, and likely only will have one.

If you aren’t booking liner orders using metadata:

* This adjustment code can be manually added to an order at any time.
* Using Auto Adjustments, you can tie it to a Ratecard and Ratecard line, to have it auto-applied if you select the “category leader rate” perhaps.

If you are booking liner orders using metadata:

* This adjustment code can be manually added to an order at any time .
* Using a metadata question, you can ask, either with a yes/no question if there is only one option, or a dropdown where you can select First or Second perhaps. And then tie that answer to an automatic charge using Metadata Adjustments in Classified Category setup.

When this comes into Plan, the Integration will tell Plan what the Adjustment Position Code is. It will be blank and just treated as a normal ad and will sort alphabetically, or it will have a code in there and will be sorted at the top of the category. If there is more than one ad with the same position code, then it will sort first by the Position Code and then by the sort text.

Here is an example:

![](<../../../../../../.gitbook/assets/image (654).png>) ![](<../../../../../../.gitbook/assets/image (1510).png>)

The job posting that starts out “Zoom Marketing” would typically be among last in the category but it is now first because it had a position code called “ffirst”.

The ad that starts out ZZZ Category Test is second in the list because it has a sort of “ssecond” and ss comes after ff.

<figure><img src="../../../../../../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>

All the remaining ads are in alphabetical order “Full Time Position” followed by “Full Time Salary” then “Full Time Supported” and finally “Seasonal Openings”.

There is nothing to configure in Plan to make this work other than setting it up in ad and having a Plan version that is dated newer than Oct 10th 2022.
