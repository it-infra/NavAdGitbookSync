# Campaign Types Explained

When creating a campaign, you must determine the type of campaign. The campaign type affects how the campaign is entered and how it is billed.

There are two different campaign Types.

## Performance Campaign

With a Performance Campaign you will bill the Customer based on when the campaign performs. Actual Performance might be actuals, estimates or 3rd party actuals.

#### Key characteristics

* Digital Orders are entered as “Estimates”.
* Reports / Forecasts can be run based on the Estimates.
* When the Ad has run the actual performance is entered against the order.
  * GAM orders automatically have the actuals imported into the system and a reconciliation process is run to determine if we are billing on actuals, estimates, or 3rd party numbers. This can come from the [client ](../../customers/advertiser-maintenance.md#a-dvertising-billing)(defaults from [client type setup](../../setup/client-types.md)) or override on the order.
* Once reconciliation has been completed then billing can commence.
* On a Campaign that spans months, billing typically occurs at the end of each month.
* Print lines on a campaign do not need to be reconciled and will be billed as run, whether that be daily, weekly, or monthly.

#### Flexible Campaign <a href="#_toc485308652" id="_toc485308652"></a>

Flexible Campaigns are typically used when the Campaign price is fixed or when you need to create a flexible billing schedule.

#### **Key characteristics**

* Orders are entered with a fixed billing amount.
* Billing is based on the fixed billing amount
* A billing schedule must be determined - there are shortcuts where you can easily select to bill at the start, at the end, or in specified increments.
* Since billing can occur at any time the system will create Journal Entries to handle the deferred / earned income
* Entering actual performance against an order will not affect the order’s price or billing schedule. It may cause adjusting Journal Entries to be made.

### Comparison Chart <a href="#_toc485308656" id="_toc485308656"></a>

| Question                                                               | Performance Campaign                                                                                                                              | Flexible Campaign                                                                                                                                        |
| ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **When would I use it?**                                               | When billing is based on actual performance (typically uploaded from an Ad Serving system) For Print, this method is often used for Retail orders | When billing is based on a fixed amount with an agreed billing schedule For Print, this methos is often used in classified orders to bill on expiration. |
| **When does billing occur?**                                           | Typically, at the end of each month after Actual performance numbers have been uploaded                                                           | Based on an agreed billing schedule for the Campaign                                                                                                     |
| **Do I have to reconcile Actuals in order to bill?**                   | Yes                                                                                                                                               | No                                                                                                                                                       |
| **Are Journal Entries created for handling Deferred / Earned Income?** | No. (Revenue is recognized in the month that it was earned and it is billed in the month it was earned as well)                                   | Yes – when a Campaign is Confirmed                                                                                                                       |

​Either type of campaign can be used for tenancy/sponsorship ads or for CPM based ads.

All digital campaigns are assumed to be entered as up-front estimates; actuals may or may not be added depending on the ad as described below.

| Performance                                                                                                                                                                                                                                               | Flexible                                                                                                                                                                                                                     |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| System assumes you will bill as you perform. For example a campaign that runs in July, August and September will present itself for billing on/after July for what ran in July, in August for what ran in August and September for what ran in September. | System makes no assumption regarding billing. User must enter a billing schedule before confirming the campaign, billing can occur at any time. Only system rule is that billing schedule must equal 100% of campaign total. |
| If any line items in the campaign are CPM/CPD/CPU actuals must be entered for the lines to be billed. Without actuals being entered/imported from ad server the lines cannot be billed.                                                                   | CPM/CPD/CPU lines will bill off the estimates. Actuals can be entered for information purposes or actuals can be left blank. They will not impact billing amounts.                                                           |
| As billing and revenue recognition are concurrent no deferred journal entries are created. Revenue and A/R entries are created for each invoice when it is posted to A/R.                                                                                 | When campaign is confirmed system creates deferred journal entries. Automated journal entries reverse the deferrals according to standard GAAP accounting rules                                                              |
