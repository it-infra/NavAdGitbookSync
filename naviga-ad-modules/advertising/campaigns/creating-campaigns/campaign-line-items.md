# Campaign Line Items

## Numbers in the Grid

Beneath the campaign header (Campaign Setup node on the left side navigation) are the line items details. You can view the line items in several ways by selecting different views in the Numbers in Grid dropdown.

<figure><img src="../../../../.gitbook/assets/image (78) (1).png" alt=""><figcaption></figcaption></figure>

The default view upon opening up the campaign will be dependent upon characteristics of the campaign and line.

* If it is a flexible campaign, the default will be to always display to the "Display Estimated Net Amounts" as shown in the screenshot above.
* If it is a performance campaign, the above will be the default if none of the lines have begun serving...meaning the campaign has 0 total ad server actual impressions. If the campaign is a performance and has > 0 total ad server impressions, the default view will be "Display Seving Details"

Below are example of all the views available on a performance and flexible campaign and how you might use them -

### Performance Campaign

{% embed url="https://app.supademo.com/demo/C7v-yeIOSz5aI2x6DYFQa" %}

1. **Ad Serving Details** - This view is mostly only relavant for the Digital cost per something lines, though you will see print lines on the list too if they are present on the order. This allows a user to see how much has been served so far and what still remains to be served. User can also see when it was last updated from GAM. If it is running on GAM, the user can also see the Google Status
2. **Estimated Quantities** - This view shows how many (something) are estimated for each line item. For print ads, this simply displays the number of insertions per month. For Digital "cost per" lines, the Estimated quantities view will show the Actuals for past months, and the estimate quantities for current and future months. For flat fee digital, it will just show 1 in each month, and total number of months in the total.
3. **Estimated Gross Amounts** - This view shows the gross prices for each month (meaning total amount before agency commission). For Digital lines, the past months will be the actual amount (since the estimates get updated during the reconciliation process), and future months will show the estimated price.
4. **Estimated Net Amounts** - This view will be the same as #3 above if there is no agency commission on the order. If there is an agency, then this will display the prices net of agency commission.
5. **Actual Quantities** - For print & flat fee digital lines, this will be the same as the estimated quantities. For digital cost per something lines this will only show the actual quantities, so future lines will display as 0. Current month will also be 0 until the reconciliation process has been run.
6. **Actual Gross Amounts** - For Print lines and digital flat fee lines, the actual will be the same as estimated. For digital "cost per" lines, this will display only actual gross amounts, so this will display what actually has been/will be billed for a line. It gets populated during the reconciliation process, so future, unreconciled lines will be 0.
7. **Actual Net Amounts** - Same as #5 above if there is no agency commission on the order. If there is an agency, then this will display the prices net of agency commission.
8. **Sales Rep Assignments** - This view will display the reps for each line on the campaign. The Order rep, Original Rep and Brand Reps are all displayed.

### Flexible Campaign

{% embed url="https://app.supademo.com/demo/Nu1vXxRDMGgOQ05PZxm9e" %}

1. **Serving Details** - This view is mostly only relavant for the Digital cost per something lines, though you will see print lines on the list too if they are present on the order. This allows a user to see how much has been served so far and what still remains to be served. User can also see when it was last updated from GAM. If it is running on GAM, the user can also see the Google Status
2. **Estimated Quantities** - This view shows how many (something) are estimated for each line item. For print ads, this simply displays the number of insertions per month. For Digital "cost per" lines, the Estimated quantities view will show the Actuals for past months, and the estimate quantities for current and future months. For flat fee digital, it will just show 1 in each month, and total number of months in the total.
3. **Billing Gross Amounts** - This displays the gross revenue to be recognized in each month (before agency commission)
4. **Estimated Net Amounts** - This displays the net revenue to be recognized in each month (net of agency commission)
5. **Sales Rep Assignments** - This view will display the reps for each line on the campaign. The Order rep, Original Rep and Brand Reps are all displayed.

## Using Ad Types - Definitions <a href="#_toc111556100" id="_toc111556100"></a>

When entering a line on a Campaign you must enter an Ad Type for the line. The Ad Type controls certain behavior of the line.&#x20;

**Cost Per Column Inch/Cm/Mm** – Most commonly used for print display advertising. It provides more flexibility for charging than flat fee/ modular sizing. User populates two fields in campaign entry: The number of columns and the size in inches, centimeters or millimeters. The inch/cm/mm unit of measure is set at the product setup level.

**Cost per Column Agate Line** – Most commonly used for print liner/classified advertising. In campaign entry, user will select columns and agate lines for pricing.

**Cost per Agate Line** – There are 14 agate lines to an inch, pricing is per agate line and an ad with larger font sizes, borders or images included will price according to the amount of space used by any data in the ad. In campaign entry, user will select columns’ number and enter the ad text lines for pricing in the Material node of the line item entry. The window on the right side displays the insertion preview.

**Cost per Visible Line** – This print line type is priced according to actual lines of text in the ad even if it takes up more space. Images and borders will be excluded from pricing and can be priced separately using adjustments.

**Cost Per Word** – Most commonly used for print liner/classified advertising and most often calculated directly from the liner text entry. System automatically prices the ad based on the number of words entered.

**Flat Fee** – May apply to print or digital and is used to price ads based on a flat amount. For digital ads, this pricing does not require actuals. For print ads, the page layout dimensions are derived from the size table and Ratecard. A Flat-Fee Ad type does not prompt a quantity to be entered on the line; user is required to add a fee. If a Flat-Fee line spans more than one month then you can choose to split the fee by month. Note that on a Performance Campaign you won’t be asked this because it always splits by month. The monthly amount can be based on an even split per month or proportioned by the number of days in a month. Flat Fee Ad Types cannot be used for E-newsletters or Run of Network Ads

**Production Fee** – The production fee pricing type applies as a Flat Fee on the line. Lines that are Production type are filtered out of other features such as flowing to Naviga Plan, GAM, and omitting from Actuals Reconciliation.

**Cost Per Thousand** – Most often used for digital lines based on actual number of impressions. On a digital performance line, this pricing type requires an actual count, not only an estimate. May also be used for print inserts and for E-newsletters.

**Cost Per Day** – Most often used for on website advertising and can be used for events or e-newsletters.

**Cost Per Click** – Most often used for digital advertising where pricing is based on responses to the ad. On a digital performance line this pricing type requires actuals to be entered in the lines to allow for billing.

**Cost Per Unit** – May be used for any pricing that requires a multiplier such as a cost per attendee for webinars or a cost per response on a digital ad. On a digital performance line this pricing type requires actuals to be entered for billing.

Note that in AD Type Setup, there is a flag to control whether this is a continuous type where Digital ad type cost per day enforces contiguous days to allow user to run and bill the client for a digital campaign for specified continuous days from the line start date and not any time throughout a range of the start and end dates. This is controlled by a security flag to allow user to choose between the continuous days or date range days. When you set the flag, the Quantity is tied to the dates / total number of days. If the flag is not set, then the Quantity is unrelated to the dates/ total number of days. This applies only to day line ad type.
