# Ratecards

Navigate to the Setup menu -> Digital Product Setup -> Ratecards node. Choose an existing or create a new ratecard.

## Ratecard Header <a href="#_toc117696617" id="_toc117696617"></a>

No matter what kind of product you are working with, all ratecards are made up of the Ratecard itself (also called the ratecard header) and the ratecard lines.

When creating ratecard headers, there are three ratecard types:

* Digital Rates
* Print Rates
* Listing / Liner Rates

A Digital Product will only allow for creating digital type rates. A Print Product will allow for creating Print or Listing/Liner type rates.

<figure><img src="../../../../../../.gitbook/assets/image (848).png" alt=""><figcaption></figcaption></figure>

#### No matter the product type, these fields are on all ratecard headers:

* Ratecard ID / Ratecard Description - When creating a new ratecard in the system (using the GUI), the ratecard ID will be auto-assigned using a sequential number. When importing ratecards, you can assign a more meaningful Alphanumeric ID.
* Client: If you choose one or more clients to be tied to this Ratecard, only orders for these clients display this Ratecard; others won’t.
* Client Type: If you choose a client type to be tied to the Ratecard, only Clients with this type attached to them on the Advertiser Maintenance screen and on the order will display this Ratecard on the order.
* Category Tree: If this ratecard is only to be used for a certain category tree(s), they can be selected here.
* Currency: if defined, this limits this Ratecard to orders created in this currency only. (use this for foreign currencies. Don't link your system base currency to a ratecard.)
* Only allow this Ratecard on Packages: If selected, this ratecard won't be selectable regular orders. It will only be available for selection in package setup.
* Start Date / End Date: These dates will dictate when this ratecard becomes selectable.

#### Print Products have these additional fields on the ratecard header:

**Default Frequency Rate Discount Schedule:** Each Ratecard can be tied to a discount schedule already created in the Setup menu -> Advertising Setup which would provide [frequency discounts](../../../advertising-setup/frequency-discount-schedule.md). Based on these frequencies, the discounts entered in the frequency discount setup screen will be automatically calculated on the order if the order meets the qualification criteria. Click the “Preview Frequency Discount Schedule” to preview the calculation from your Ratecard when discounted for each frequency. (you need to create the ratecard lines first, then preview the calculations): ![](<../../../../../../.gitbook/assets/image (423).png>)

Check the box for “Apply Frequency Discounts without Contract” to reflect “Yes” value if you wish to apply the discounts without the necessity of tying the client to a contract. Leave as "no" if the frequency discounts are only allowed with a corresponding frequency contract.

## Ratecard Lines

All ratecards allow these options above the ratecard lines:

<figure><img src="../../../../../../.gitbook/assets/image (1543).png" alt=""><figcaption></figcaption></figure>

* New Line - Manually create a new, blank ratecard line
* View Change history - view the history of changes made to the ratecard

{% hint style="info" %}
Note: For each rateline you create, the system also provides a hyperlink called “View Line Change History” which displays an audit trail of the changes made to the line. This allows you to view changes done to the Ratecard and who made the changes.
{% endhint %}

* Create from size table - useful for modular rates. It will look at the product's allowed sizes from product setup and auto-create a line for each size.
* Copy lines from another ratecard - useful if products share the same rates, or even just the same structure. Easier to change the price on something that was already started than re-creating all the details from scratch.
* Sort by description - this will alpha sort the lines by their description.

If you enter the details of the size, description, section/position, Ad Type, and rate, this Ratecard can be used in the Quick Line Entry of a campaign where you choose the rate-line and the system automatically fills in all the corresponding details.

{% hint style="info" %}
Note - if you are coming from Adbase, this requires a bit of a mind-shift. In Adbase the user doesn't generally select a rate. The user selects a product, ad type, size, section, position, etc, and then the system figures out the rate based on the rule tree. Here it is really the exact opposite....the user selects a ratecard/rateline and then the system fills in the size, section, position, etc.
{% endhint %}

### Rateline settings across all Ratecard lines:

Rateline settings is the first tab in the ratecard line setup. Depeding on the ratecard type, there are additional tabs.

* Line ID / Line Description - The LineID is an auto-created sequential number. The description is whatever you want it to say. It is often displayed in reports and on the invoice, so a customer-friendly description of what they are buying is helpful here. For a digital line it might be something like "HomePage takeover," for a classified as it might be something like Classified Word ad, etc.
  * There is also a yes/no flag on the setup here called "Allow Description Override" - this refers to whether or not a user booking an ad would be allowed to override that description in order entry.
* Sort - this is a numeric field relating to the sorting preference. If you leave it blank, the next sequential number will be filled in here as you are creating lines. If you want to re-order, just change the numbers and re-save.
* Section / Position - If the product has sections and/or positions, then they can be added onto a rateline so that the user doesn't have to select it manually. (part of the position setup also dictates if a position can ONLY be selected from the ratecard line - for example a premium position like Back page might not be able to be selected manually if it will require a premium rate to be paid)
* Ad Type - This will dictate what ad type this rateline is valid for. It provides a filter in order entry and also affects how the rate is applied. For example in Print a cost per word ad type will take the rate and multiply it by the number of words in a classified text ad. A digital ad might have a cost per click rate. In that case the price will be determined by the number of clicks that were received, etc.
* G/L Type - This determines which G/L Type (and therefore which G/L number) will be used for the revenue of this order. Only a user with permission will be able to further override this on an order.
* G/L Project - This is a reporting tag that can be optionally added in G/L Setup.
* Default Production Status - Optional line to set a default production status on a line so that the user doesn't have to manually select it. I find it really useful to set the default production status for all listing type ads to "complete" so that nobody needs to worry with changing that, since listing type ads are created during the booking process, there is no need to chase materials later using the Production reports. Any type of ad can have a default production status set here, if desired.
* [Production Link](../../../advertising-setup/production-links.md) - If you choose to setup production links, they can then be linked to the ratecard lines that they apply to.
* Default custom data forms - This is an override from the product itself. It this was set on the product, it can be overwritten here. If it was not set on the product, it can be set here.
* External ID - not a required field, but had some clients using our API with a need for a unique ID across all rate lines, so this allowed them to set that unique ID.
* Pricing - this is going to be different per ad type. See info below in Print-only and Digital only sections.
* Cost Rate - The cost rate is optional. it is used when there is a 3rd party cost to the media company. This is not part of the price calculation that the Advertiser sees, but rather a part of the G/L cost allocated. See [G/L Overrides](../g-l-and-tax-overrides.md#g-l-override) and see [Cost Rate](ratecards.md#cost-rates) below for additional details.
* Allow Description Override - Set to Yes to allow the user to override the description field on the order line. Set to no to disallow this functionality.
* No Tax - Each line can have its own tax determination so the order can charge tax on this line or not. Select YES to Not charge tax.
* Only allow this rate on packages - same function as the flag on the ratecard header, but this would disallow it on regular orders for this rateline only, even if the ratecard itself was allowed.
* Cancel at Full Value - This applies to Flexible campaigns only. [Please see description below](ratecards.md#cancel-at-full-value)
* Is Inactive - if you no longer wish to use this ratecard line for future orders, set this flag to Yes.

#### **Cancel at Full Value**

Ability for a user to cancel a running ad across multiple dates which an advertiser would like to cancel after running in initial issues while allowing the addition of the revenue to the last issue which ran so that user doesn’t lose revenue. This is applicable to all ad types and only on flexible campaigns and done through the Ratecard line flag “Cancel at Full Value”. For example, if an advertiser doesn’t want his ad to continue running for future dates, to avoid receiving inquiries for something that has already been sold or for any reason. But the publication wants the advertiser to pay the full price, even though the advertiser is reducing the days of the ad.

Navigate to the menu Setup -> Product Setup -> Ratecards. Choose a line and check the flag on the line “Cancel at Full Value”. Save the line and the Ratecard.

![](<../../../../../../.gitbook/assets/0 (61).png>)

Create a flexible campaign using the Ratecard line above and create 2 or more dates in the line. Save. Confirm the campaign.

![](<../../../../../../.gitbook/assets/1 (70).png>)

You can bill the campaign or leave as just confirmed.

Return to the campaign and edit the line and remove the last issue. Save the campaign.

![](<../../../../../../.gitbook/assets/2 (88).png>)

Note that the last running issue is now split and includes the amount from the line you deleted. The adjustment at the right side of the line shows +100% added from the deleted line.

Click the split line and click the “Adjustments” tab.

![](<../../../../../../.gitbook/assets/3 (16).png>)

Note that the amount added to the line from the cancelled line is listed with the explanation of the issue date cancelled and the quantity as well as the amount. Other adjustments for any other reasons are listed in separate lines.

#### Cost Rates

The Ratecard line shows a Cost field. This represents the cost to the media company for purchasing this inventory on behalf of the client. The "Rate" amount is what gets billed to the customer.

<figure><img src="../../../../../../.gitbook/assets/image (1350).png" alt=""><figcaption></figcaption></figure>

If a cost is set on the Rate, and a Cost G/L code is set on the G/L Overrides, then in order entry (Full Line Entry only), the Cost Rate is displayed along with an option to override that amount.

<figure><img src="../../../../../../.gitbook/assets/image (1149).png" alt=""><figcaption></figcaption></figure>

In the above example, the normal cost is $10 CPD and if it truly cost that much, i could leave the Override blank and then system will fill in $10 on Save. But in this case the cost to me was only $8, so i was able to fill that in. When the Performance campaign gets billed, or when the Flexible campaign gets Confirmed, the G/L entry will reflect the actual cost so that you can track it in your G/L.

<figure><img src="../../../../../../.gitbook/assets/image (1152).png" alt=""><figcaption></figcaption></figure>

### Print-only Ratecard line settings:

#### Minimum and Maximum Depth (Height) Ratecard Line <a href="#_toc117696618" id="_toc117696618"></a>

Ratecard lines on Ratecards for the cost per ads allow user to set a minimum and maximum height for the ad in order to control the entry of ads using this Ratecard line by dimension. This would be beneficial if an advertiser desires to get a better rate using a classified ad type for placing an ad which in reality should be a display ad. In this case setting the size limitation would give users control over the pricing of the ad to be appropriate for the ad entered.

![](<../../../../../../.gitbook/assets/8 (21).png>)

Enter a Minimum Depth if you’d like to allow for a minimum size Ad and a Maximum Depth if you’d like to limit the Ad depth (be sure to also set the unit of measure). Set Use columns in count if applicable.

Columns in count should be set to yes if you are trying to limit the overall size of the ad. For example, if you set the limit to 10" in depth, and a 2x5 would be as acceptable as a 1x10 to receive this rate, but you wouldn't want to allow it for a 3x4. If this limitation is due to the physical size of the paper where perhaps for aesthetic reasons you don't let Naviga Plan break liner ads over multiple columns...then you might set to not use Column counts because a 1x10, 2x10, 3x10, etc are all ok, but you just don't want the ad deeper than 10"

Save the line and then save the Ratecard.

Navigate to create a campaign using this Ratecard line. Enter an ad where number of inches/CM/MM/agates exceed the maximum or less than the minimum depth in the settings.

![](<../../../../../../.gitbook/assets/9 (16).png>)

Note the Height of the AD dimension in the preview stats window and note that it exceeds the allowed depth. Click “Create Line” and the system won’t allow you to create the ad with the error message as to why. In this case the depth exceeds the setting on the Ratecard line.

The same happens if you enter characters less than the minimum allowed.

![](<../../../../../../.gitbook/assets/10 (31).png>)

Enter the exact depth as setup.

![](<../../../../../../.gitbook/assets/11 (16).png>)

The system allows you to save the line when you click “Add Line”.

This also applies to the Display Ad Type of Column per Inch for example, as the Column x Inch defining the depth (height) on the Ad line.

**Flat Rate on Ratecard Line Overrides Rate x Quantity Calculation**

Flat Rate flag is available on Ratecard lines so that when it’s checked, the system will not consider a calculation of Rate x Quantity, but instead will apply the Ratecard fee to the line.

Navigate to the menu Product -> Product Setup -> Ratecards. Edit an existing or create a new Ratecard line which is for Cost Per Column Inch/MM/CM for a display Ratecard.

![](<../../../../../../.gitbook/assets/4 (66).png>)

Save the line with the “Flat Rate” flag unchecked and save the Ratecard.

Navigate to create a campaign line for this product, Ad type and Ratecard line. Increase the Column count in the line.

![](<../../../../../../.gitbook/assets/5 (40).png>)

Navigate back to the Ratecard line and check the flag “Flat Rate”.

![](<../../../../../../.gitbook/assets/6 (34).png>)

Save the line and the Ratecard settings.

Navigate back to the campaign and create a new line using this Ratecard line.

![](<../../../../../../.gitbook/assets/7 (25).png>)

The Rate Per Insertion now ignores the Quantity x Rate formula and uses the flat rate from the Ratecard Line as the fee.

This is typically used in conjunction with a rateline with a Maximum depth set. For instance, where you get up to X inches for $Y flat price.

#### Pricing features of a Print Line

* Rate - For Modular ad types this is the flat price of the ad, and for Print Col x Something rates, this is the rate that is multiplied by the size to to get the price.
* Lines - This can be left blank if the page eq is to be calculated based on info on the product. See [Page Eq Calculation](../../../../campaigns/campaign-reports.md#page-equivalency-page-eq.-calculation)
* Columns - This will be grayed out except for Print Rate Ratecard types and Ad Types that are Col Inch Ad Types. This is a default # of Columns for a particular rate line
* Inches - This will be grayed out except for Print Rate Ratecard types and Ad Types that are Col Inch Ad Types. This is a default # of Inches for a particular rate line
* Base Rate / Base Qty - Only seen on Listing type rates. This is the default price for whatever the base qty in size is (below). For example, it is common in liner ads to have a $X price for Y inches/words/agates/etc and the $Z per inch/word/agate/etc beyond that.
* Overage Rate - the amount charged per unit of measure if your ad exceeds the Base Rate/Base Qty defined above. If your liner type ad is simply $Y per unit, then Base Rate and Base Quantity might be zero. If the price is simply a flat price, then the base rate will be the price and overage rate might be zero.

### Digital-Only Rateline Settings <a href="#_toc117696618" id="_toc117696618"></a>

* Default Quantiry - Typically used for CPM/CPC type ads, this would be the default Quantity for the rateline. For example, a rateline might be set to give a $10 CPM rate and a default quantity of 50,000 Impressions. The user could edit this amount in order entry, but if this amount was the standard quantity, or the package quantity if this was a package price, then the use wouldn't have to set it.
* Use Ad Server Inventory - Set this to Yes, if the system should query the GAM ad server to determine if inventory is available.

### Day of Week/Special Date Rate Overrides

You can choose to override rates for a date-based product on certain days of the week or even choose a special rate for a specific date.

Click on the line which you would like to setup a special rate schedule for. Choose the Day of the Week Rates day and enter an amount which will override the amount on the Ratecard. Options include Mon - Sunday, Weekdays and Weekends. For example, you might have a different rate for sundays and use the standard price for the other days of the week.

You can also choose to enter a special date rate by choosing the date from the pop-up calendar and enter the special rate which will override the Ratecard line rate. For example, it is common for Thanksgiving to get the sunday pricing in the US, even though it is actually a Thursday.

If the rate type is a Print Rate, you will have an override rate on these tabs. If it is a liner type ad, you will have an override Base Rate, Base Qty and Overage Rate on these tabs.

When finished, click the Apply Changes button and then you must save the Ratecard.

### Discount Escalation (Print and Listing ratecard types only) <a href="#_toc102051437" id="_toc102051437"></a>

Print products have a new escalation pricing option where users can upgrade quantities on orders for their clients at a discount based on rules setup in the Print Product Ratecard. This is only applicable to non-modular print ads, such as column x inch or cost per agate line ads.

Click the “Discount Escalation” tab.

Choose the Rounding Rule from the drop-down. You can choose not to round, Or round to the nearest Dollar, $5 or $10.

Enter the first new line “Up to Quantity” and percent discount. The first line can be the same quantity as the line insertion quantity and the percent can be 0. For example, if the line insertion Quantity is 1x3 = 3, if you enter 3 in this “Up to Quantity” line you can enter 0 in the percent line, so that no discount is offered if the basic line is entered.

The next line can be “Up to Quantity” higher than the first. For example, 6 and the percentage is 5 for 5%.

<figure><img src="../../../../../../.gitbook/assets/image (1202).png" alt=""><figcaption></figcaption></figure>

Add more lines as needed. Note that the “Up to Quantity” is inclusive of values less than and equal this value. For example, if the Ratecard has 2 lines one with this field containing “Up to Quantity” 6 and a discount 5%, followed by a second line “Up to Quantity” 10 and a discount percent of 10%, then if the line item has the Quantity 8, then the discount applies is the value on the second line of 10%.

When finished click Save. Then click Save on the Ratecard.

You’ll be prompted to choose to update future campaigns. Click Yes or No according to your business needs. If you click Yes, the campaigns will be updated according to the Quantities in them and the discounts in this rule.

{% hint style="info" %}
Note - discount escalation changes the rate itself. It doesn't apply an "adjustment" to the rate.
{% endhint %}

### Rate Escalation <a href="#_toc102051438" id="_toc102051438"></a>

Rate Escalation feature on Ratecards allows for override rates based on the total quantity entered. This is only on CPM Ad Types, as well as Display Cost-Per Column/Measure Ad Types. This allows for example Inserts to use the escalation discounts so that when a publication distributes thousands of inserts the advertiser can benefit from a discount based on the number of inserts automatically applied to the order when it’s created. The same is true for CPM Digital type lines. If you buy more impressions, the price per thousand impressions could be less

![](<../../../../../../.gitbook/assets/5 (64).png>)

Click the + sign to add a new line. Enter the “Up to Quantity” field and corresponding Override Rate. This is the value which if entered as Qty on line item, will trigger the override Rate which is different than the Rateline rate for this CPM Ad Type.

Click the + if you’d like to add another up to quantity and the system automatically increments the From Qty from the previous line. Enter the corresponding override rate. Click OK and save the Ratecard.

Enter a campaign and line item using this Ratecard, Ad Type and Up to Quantity.

![](<../../../../../../.gitbook/assets/6 (27).png>)

The Discount Rate kicks in automatically and doesn’t show as an adjustment.

### Google Ad Manager

The Google Ad Manager tab in ratecard setup displays all the targeting attributes accessible to us in the GAM API. This allows you to setup a Ratecard line with sophisticated targeting selections pre-set so that the rep only needs to select a ratecard line in order entry and then all of these settings will be automatically set for them.

These can be overwitten on the order, but it saves the rep a lot of order entry time when there are certain buys that are commonly used.

<figure><img src="../../../../../../.gitbook/assets/image (915).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
NOTE: There is a report called the [GAM Rate Lines Report](../../../gam-rate-lines-report.md) which will help to visualize the setup of the ratecards as it relates to the GAM Settings.
{% endhint %}

## Changing an existing Ratecard

When you change a ratecard, and click save, the system displays the changes and prompts you to choose whether to update future orders with these new values.

Click “Yes” and the system displays a list of future orders only, where you can check the box corresponding to each or all and make the changes.

![](<../../../../../../.gitbook/assets/1 (103).png>)
