# Ad Types

## Line Types Defined

When entering a line on a Digital Campaign you must enter an Ad Type for the line. The Ad Type controls certain behavior of the line.

**Cost Per Column Inch/Cm/Mm** – Most commonly used for print display advertising. It provides more flexibility for charging than flat fee/ modular sizing. User populates two fields in campaign entry: The number of columns and the size in inches, centimeters or millimeters.

**Cost per Column Agate Line** – Most commonly used for print liner/classified advertising. In campaign entry, user will select number of columns and agate lines will be calculated based on the depth of the ad for pricing. The calculation is 14 agate lines per inch.

**Cost per Agate Line** – There are 14 agate lines to an inch, pricing is per agate line and an ad with larger font sizes, borders or images included will price according to the amount of space used by any data in the ad. In campaign entry, user will select columns’ number and enter the ad text lines for pricing in the Material node of the line item entry. The window on the right side displays the insertion preview.

**Cost per Visible Line** – This print line type is priced according to actual lines of text in the ad even if it takes up more space. Images and borders will be excluded from pricing and can be priced separately using adjustments.

**Cost Per Word** – Most commonly used for print liner/classified advertising and most often calculated directly from the liner text entry. System automatically prices the ad based on the number of words entered.

**Flat Fee** – May apply to print or digital and is used to price ads based on a flat amount. For digital ads, this pricing does not require actuals. For print ads, the page layout dimensions are derived from the size table and Ratecard. A Flat-Fee Ad type does not prompt a quantity to be entered on the line; user is required to add a fee. If a Flat-Fee line spans more than one month then you can choose to split the fee by month. Note that on a Performance Campaign you won’t be asked this because it always splits by month. The monthly amount can be based on an even split per month or proportioned by the number of days in a month. Flat Fee Ad Types cannot be used for E-newsletters or Run of Network Ads

**Production Fee** – The production fee pricing type applies as a Flat Fee on the line. Lines that are Production type are filtered out of other features such as flowing to Naviga Plan, GAM, and omitted from Actuals Reconciliation.

**Cost Per Thousand** – Most often used for digital lines based on actual number of impressions. On a digital performance line, this pricing type requires an actual count, not only an estimate. May also be used for print inserts and for E-newsletters.

**Cost Per Day** – Most often used for on website advertising and can be used for events or e-newsletters.

{% hint style="info" %}
Note that in Ad Type Setup, there is a flag to control whether this is a continuous type where ad type cost per day enforces contiguous days to allow user to run and bill the client for a digital campaign for specified continuous days from the line start date and not any time throughout a range of the start and end dates. This is controlled by a security flag to allow user to choose between the continuous days or date range days. When you set the flag, the Quantity is tied to the dates / total number of days. If the flag is not set, then the Quantity is unrelated to the dates/ total number of days. This applies only to cost per day line ad type.
{% endhint %}

**Cost Per Click** – Most often used for digital advertising where pricing is based on responses to the ad. On a digital performance line this pricing type requires actuals to be entered in the lines to allow for billing.

**Cost Per Unit** – May be used for any pricing that requires a multiplier such as a cost per attendee for webinars or a cost per response on a digital ad. On a digital performance line this pricing type requires actuals to be entered for billing.

## AD Type Setup <a href="#_toc111556102" id="_toc111556102"></a>

Navigate to the Setup -> Advertising Setup -> Ad Type Setup.

Click Add New or edit an existing type. The screen provides multiple options to link to various fields.

![](<../../../../.gitbook/assets/1 (99).png>)

When creating a new Ad Type, click on + Ad New button at the top of the list of existing Ad Types.

Enter an **ID and a Description.** Both are displayed when selecting in Order Entry, so it is good to be descriptive. If there is a long list users can start typing the name or ID to filter.\
![](<../../../../.gitbook/assets/image (301).png>)

The **G/L Type** which is used for this ad type can be selected here (for example, this might be be a display print G/L type).

{% hint style="info" %}
What is set here is frequently overwritten by the ratecard setup, since we also set the G/L Type on the Ratecard Line. The G/L Type that is set on the Ad Type will be what gets used in the case where there isn't a ratecard. In come cases this may never be used - for example if you set on the product that a ratecard is required for booking this product...then this will always be ovewritten by the ratecard setting. But, especially with Digital products and Marketing Services, you might not even set a rate card for these and instead allow the user to simply type in the price.
{% endhint %}

Select the appropriate **Line Type** for this Ad Type. This will be important for how the screen is displayed to the user when booking.

**Default Material Approval Status -** This is really only applicable to clients using Naviga Plan and requiring proofs to be approved by sales or the client before sending the material to Plan. The proof approval process is more commonly used for Display type ads and not really for Liner type ads. If you require material to be approved before going to Plan, you might want to set up liner ads as "approved" by default. (See [Approval Status](../../production-ad/overview-ad-production-and-material-status-workflow.md#\_toc113467268))

**Ad Serving Platform** - You can choose the Ad serving Platform choice at this level as well as at the Product Setup level. This is the advertising platform such as any social advertising media platform and when chosen here will default on the campaign entry line. This allows for reporting on which lines were serving on other non-GAM servers. These are not required but can provide additional reporting and a link to additional questions needed for each server. The names of the platforms can be setup in the menu Setup -> Advertising Setup -> Ad Serving Platforms.

**Google Ad Manager Cost Type / Google Ad Manager Line Type** - See [Ad Server Integration](../admin/ad-server-integration.md#\_toc105408221-1) setup for description

**Send to Naviga Plan** - This flag will be used in conjunction with the flag on the Product to determine if an order is eligible to be sent to plan. Typically all your print ad types will be flagged to go to plan with the exception of PrePrints.

**Discounts not Allowed** - set to yes if this ad type does not allow discounting

**Require Category Selection in Full Line Entry** - This is for your classified ads, and specifically the Classified Display types. Listing ads you cannot even really complete without selecting a category since the material size (width) is determined by the category. With Class Display type ads where the user is entering a col x inch size it can be easy to forget to also select a Category.

**Ignore Required Metadata Field Rules in Full Line Entry** - Again, typically meant for Class Display type ads. If there are some required metadata fields intended for building the text of a liner ad, it might not be relevant to enter it in for a Class display ad in the same category.

**A flag to check to mark it as a Listing Entry** - This flag will display the Classified text editor tab in order entry.

**No Agency Commission** - Set to true if this ad type is not eligible for Agency Commission.

**No Rep Commission** - Set to true if this ad type is not eligible for Sales Rep Commission.

There are two places where you can link an ad type to a product. - In Ad Type Setup and also in Product Setup. If your ad types are already created, and you are making a new product, it is convenient to select the applicable ad types during product setup. If your products are already created, and you have decided you need a new ad type to be added to many products, it might be more convenient to link to the products all together on the ad type setup. Both ways will accomplish the same result.

You can click save and next to move onto the next record or save and close to close this window.

## Ad Types Import <a href="#_toc62052314" id="_toc62052314"></a>

Navigate to the menu Setup -> Advertising Setup -> AD Types Import. The import screen displays. Click the “Download Template” button.

An excel sheet displays where you can fill in the data according to the template below. Save the template on your desktop and click the “Select” button to browse and upload the template.

Click the button “Test Import File” which will alert you to any errors in the template. If you have any, click the x remove button to remove the uploaded template from the screen. Correct the errors in the excel template on your desktop and save it.

Repeat the select and upload and test steps till the system provides you the confirmation message.

![](<../../../../.gitbook/assets/1 (97).png>)

Click the “Import File” button to import the section to the product. Click OK to the warning message. The system then confirms that the import was completed successfully. Click OK.

Navigate to the menu Setup -> Advertising Setup -> Ad Types. The imported type(s) display with ID and description in alphabetical order. These types are ready to be used in the advertising system.

### Ad Type Import Template <a href="#_toc62052315" id="_toc62052315"></a>

These are the fields in the excel template with a sample of data entry and conditions on their data.

<table data-full-width="true"><thead><tr><th width="216">Field</th><th width="119">Example</th><th width="466.96172839506175">Conditions</th><th>Mandatory/ Optional</th></tr></thead><tbody><tr><td><strong>Ad Type ID</strong></td><td>IMP</td><td>Alphanumeric value for the ID</td><td>Mandatory</td></tr><tr><td><strong>Description</strong></td><td>Import</td><td>Alphanumeric description for the Ad Type</td><td>Mandatory</td></tr><tr><td><strong>G/L Type</strong></td><td>IMP</td><td>G/L Type ID which must match what already is in the Advertising system</td><td>Mandatory</td></tr><tr><td><strong>Line Type</strong></td><td>FF</td><td><p>Line Type ID which must match the value already in the Advertising system. The values are:</p><p>CPM for Cost Per Thousand</p><p>CPD for Cost Per Day</p><p>CPC for Cost Per Click</p><p>CPU for Cost Per Unit</p><p>CPCI for Cost Per Column Inch</p><p>CPCC for Cost Per Column Centimeter</p><p>CPMM for Cost Per Column Millimeter</p><p>CPCA for Cost Per Column Agate Line</p><p>CPVL for Cost Per Visible Line</p><p>CPAL for Cost Per Agate Line</p><p>CPW for Cost Per Word</p><p>FF for Flat Fee</p><p>PROD for Production</p></td><td>Mandatory</td></tr><tr><td>Listing Entry</td><td>Y</td><td>Y for yes this is a listing advertisement or N for no this is not a listing ad.</td><td>Optional</td></tr><tr><td>Enforce Contiguous Days</td><td>Y</td><td>Y for yes to enforce that the days when the ad runs are contiguous and N for no the days can be separate</td><td>Optional</td></tr><tr><td>No Agency Comm</td><td>Y</td><td>Y for this will not allow agency commission and N for no this will allow agency commission</td><td>Optional</td></tr><tr><td>No Rep Comm</td><td>Y</td><td>Y for this will not allow rep commission and N for no this will allow rep commission</td><td>Optional</td></tr><tr><td>Google Cost Type</td><td>CPM</td><td><p>Alphanumeric value of the Google Cost Type which must match the following valid codes representing the Google Cost Types that we currently support:</p><p>CPC</p><p>CPD</p><p>CPM<br>VCPM</p></td><td>Optional</td></tr><tr><td>Google Line Type</td><td>FF</td><td><p>Alphanumeric value of the Google Cost Type which must match the following valid codes representing the Google Cost Types that we currently support:</p><p>SPONSORSHIP</p><p>STANDARD</p><p>NETWORK</p><p>BULK</p><p>PRICE_PRIORITY</p><p>HOUSE</p><p>LEGACY_DFP</p><p>CLICK_TRACKING</p><p>ADSENSE</p><p>AD_EXCHANGE</p><p>BUMPER</p><p>UNKNOWN</p></td><td>Optional</td></tr><tr><td>Send to Naviga Plan</td><td>Y</td><td>Y for yes to send to Naviga plan and N for no don’t send to Naviga Plan</td><td>Optional</td></tr><tr><td>Discounts Not Allowed</td><td>Y</td><td>Y for yes Do Not Allow Discounts and N for No to Allow discounts</td><td>Optional</td></tr><tr><td>Default Material Approval Status</td><td>1</td><td>This value must match the value in the menu Setup -> Material Approval Setup</td><td>Optional</td></tr><tr><td>Ad Serving Platform</td><td>YT</td><td>These values are the ID codes for the Ad Serving Platforms in the menu Setup -> Advertising Setup -> Ad Serving Platform.</td><td>Optional</td></tr><tr><td>Is For Preprints</td><td>Y</td><td>Y or N value for the flag "Is For Preprints"</td><td>Optional</td></tr><tr><td>Require Category Selection in Full Line Entry</td><td>Y</td><td>Y or N value for the flag to require Category Selection in Full Line Entry. (Categories are for Classified Ads - Class Display ad types you may wish to require that a category is selected)</td><td>Optional</td></tr><tr><td>Ignore Required Metadata Field Rules in Full Line Entry</td><td>Y</td><td>Y or N value for the flag to ignore metadata required flags. (This is sometimes used for Classified Display ad types where metadata might be required for a liner ad, but not for a display ad in the same category)</td><td>Optional</td></tr></tbody></table>
