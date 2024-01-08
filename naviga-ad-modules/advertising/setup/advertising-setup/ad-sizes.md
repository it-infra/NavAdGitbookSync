# Size Setup

## Size Setup

This menu displays the sizes which can be used in orders. Add new sizes and save the settings. Note that these sizes allow for different dimensions measurement such as inches, pixels, etc. When marked as inches, it allows you to check the box to mark this size for print products’ use while entering a campaign or order.

You can then also include the line equivalency for the Modular ad size.

<figure><img src="../../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

To manually create an ad size, click + Ad New at the top of the screen. (see [below ](ad-sizes.md#toc111625567)for importing Ad Sizes)

* Add a **Size Code** and a **Size Description**.
* **Line Eq** will only be relevant for Print ads, so it is only editable on Ads with Dimension type of Inches, CM or MM. This is where reports in the system will look to get the Page Eq for **modular** type ads. See Page Eq discussion [below ](ad-sizes.md#page-eq-equivalency-for-print-a-ds)for more on Page Eq for different kinds of ads.
* **Width and Depth** - This will be the physical size of the ad, in whatever dimension type was selected above. For a digital banner this might be 320x50 in Pixels. In a Print ad it might be a 9.83 x 21 Inches for a Full Page Broadsheet, etc.
* **For Print** - Will indicate that this is a print ad
* For Preprints - Will indicate that this is for a Preprint Ad Type using the workflow introduced with 2023.6.  These sizes will only be displayed in the wizard workflow, so do not check it if you are using the Full Line Entry workflow for entering preprints.
* **Inactive** - select Yes to mark this as inactive and it will no longer be selectable in Order Entry.

## Size Import <a href="#toc111625567" id="toc111625567"></a>

Navigate to the menu Setup -> Advertising Setup -> Size Import. The import screen displays. Click the “Download Template” button.

An excel sheet displays where you can fill in the data according to the template below. Save the template on your desktop and click the “Select” button to browse and upload the template.

Click the button “Test Import File” which will alert you to any errors in the template. If you have any, click the x remove button to remove the uploaded template from the screen. Correct the errors in the excel template on your desktop and save it.

Repeat the select and upload and test steps till the system provides you the confirmation message.

![](<../../../../.gitbook/assets/1 (73).png>)

Click the “Import File” button to import the section to the product. Click OK to the warning message. The system then confirms that the import was completed successfully. Click OK.

Navigate to the menu Setup -> Advertising Setup -> Size Setup. The imported sizes(s) display with ID and description in alphabetical order. These types are ready to be used in the advertising system.

### Size Import Template <a href="#toc111625568" id="toc111625568"></a>

These are the fields in the excel template with a sample of data entry and conditions on their data.

<table data-header-hidden><thead><tr><th width="149"></th><th width="94"></th><th width="338"></th><th></th></tr></thead><tbody><tr><td><strong>Field Name</strong></td><td><strong>Example</strong></td><td><strong>Conditions</strong></td><td><strong>Mandatory/ Optional</strong></td></tr><tr><td><strong>Size ID</strong></td><td>326</td><td>Alphanumeric ID for the size of the line item. Note that no spaces/slash allowed.</td><td>Mandatory</td></tr><tr><td><strong>Description</strong></td><td>Mirror</td><td>Alphanumeric description of the size.</td><td>Mandatory</td></tr><tr><td>Width</td><td>3</td><td>Numeric width value for the AD in the units below. For example, the width of the ad is 3”.</td><td>Optional</td></tr><tr><td>Height</td><td>2</td><td>Numeric height value for the AD in the units below. For example, the height of the ad is 3”.</td><td>Optional</td></tr><tr><td><strong>Dimension Type</strong></td><td>NATIVE</td><td><p>The type of the dimension. This is a hard- coded value and must match the dimension type in the advertising system in upper case as follows:</p><p>UNDEFINED: This shouldn't be used if interfacing with an ad building or pagination software such as Naviga Plan. Those types of systems really need this to understand the size of the ad.</p><p>INCHES</p><p>MILLIMETERS</p><p>CENTIMETERS</p><p>POINTS: These can be used to measure print ads more precisely. There are 72 Points per Inch.</p><p>PIXELS: Pixels are used for digital ads as an exact measure of size such as 160x600.</p><p>NATIVE: This option marks dimensions are irrelevant and is interpreted by the system to not take dimensions into consideration. This is applicable to product with an embedded photo or video.</p></td><td>Mandatory</td></tr><tr><td>Line Eq</td><td>420</td><td><p>Line count Equivalency of the ad numeric value. The line equivalency is traditionally used only for print but has two roles:</p><ul><li>For newspapers this is the count of lines which make up a page.</li><li>For magazines, it is traditionally 420 because it is divisible by all the typical page sizes. For example, if you’re entering a ½ Page size ad, this field on the Ratecard line is 210.</li></ul><p>This field is reflected in reports across the advertising module. It is also used for inventory checking. If it is set incorrectly, then the inventory will not function correctly for print ads.</p></td><td>Optional</td></tr><tr><td>For Print</td><td>Y</td><td>This is a flag which when set at “Y”, it is applied to print products only and if set to “N” it is applied for non-print products.</td><td>Optional</td></tr><tr><td>Inactive</td><td>N</td><td>This is a flag which when set to “Y”, it marks the size as inactive and will not be available in orders. If set to “N” it is active and ready to be used.</td><td>Optional</td></tr></tbody></table>

## Page Eq (Equivalency) for Print Ads

There are several reports in the system that show the size of each print advertisement and provide a total number of advertising pages.

Print orders can be entered using modular sizes, column x depth sizes or by entering the text of the ad. Because of the variety of ways in which ads are sized, the system performs different calculations on each type of order to calculate total size.

How the system determines the size of an ad:

1. For modular ads the system determines the dimensions using the size code table. The size code is most often stored on the Ratecard, in some cases one may select a size code during campaign entry. If you are seeing inaccurate information for modular ads, check the dimensions on the size table, and the lines per page set up on the product. The unit of measure on the size code is used to convert the width to points for the page total.
2. For Cost Per Column by depth ads where the user enters the number of columns and inches, centimeters, millimeters or agates, the width is determined from the [**column layout**](column-layout-maintenance.md). The system checks the number of columns order line, checks the column layout from the product (possibly overwritten by section or classified category) and matches the number of columns on the order to the column width in column layout maintenance. The system checks the number of units (inches, centimeters, millimeters or agates) to calculate the height of the ad. If you are seeing inaccurate information for these ads check the column layout for the product or section or classified category. The system converts the column with points for the page total.
3. If this is a listing type ad (determined by the listing checkbox on the ad type). The system measures the material that was created/entered via the listing entry screen for the height. The width is calculated in the same way and validated against the column setup for that classified category. Verify that the column setup is accurate and that the dimensions on the ad are correct. The system again converts the width to points before calculating the total.

To then calculate the Page EQ now that we know the size of the ad, formula for MODUALAR ADS is the Line Eq for the ad size / lines per page of the product setup. So, to take an easy example, if the ad was modular and the lines per page was 420 and the Line Eq on the Ad Size was 210, then the Page eq for size would be .5 or a half page ad.

To calculate the Page EQ for non-modular, we need to know the physical size of the material (as determined in steps 2 and 3 above) and divide that by the physical size of the page. So if the page itself is 206.43 inches, like my example product here:\\

<figure><img src="../../../../.gitbook/assets/image (432).png" alt=""><figcaption></figcaption></figure>

Then based on the Column Layout Maintenance for 4 columns (that is the # of columns in this product) the width of 4 columns \* half the depth of the page (10.5 Inches in this example) should be 103.215.

{% hint style="warning" %}
When doing the calculation, if lines are specified in a ratecard (on the rateline) then that number will be favored OVER the the setup above. If the ratecard setup had a number of lines of null, it would fall back to the above material height and width calc. So when troubleshooting, if the calculations aren't coming out as expected, check the rateline setup to see if there is an override.
{% endhint %}
