# Sections & Positions

## Sections

Sections can be created for a product if the Product Details -> Campaign Parameters are set to "Yes or Mandatory" in the Enter Sections question. See [Import Sections and Positions](importing-sections-and-positions.md#\_toc117696626) to Import Sections. See below to create a section Manually. Note: you can also [Copy sections and Positions](./#copy-sections-and-positions) from one Product to another.

Click the button "New" to enter a new section.

Give the section a name and an ID.

Section URL: Enter URL for this product (if applicable)

If a section can only be selected from a ratecard and not selected manually in order Entry, select Yes to only used on ratecards. This is often used if a section has special pricing and shouldn't be selected without the appropriate ratecard.

Inactive: Set to yes to this section will no longer be used. It will still be available on reports, but won't be able to be selected in order entry.

### Digital-Specific Settings:

If this digital product is integrating with GAM, you can assign default Key/Value targeting for this section.

### Print-Specific Settings:

Sections can have restrictions by day or date or layout. This allows the section to be visible only under each of these conditions regardless of the product’s setup.

This section is only published on: Select one or more days of week as applicable. For example, a Print Product might be distributed daily, but Section ABC may only be printed on Sundays.

Override Layout for this section: The default layout for a product is defined on the Product details node. If this section publishes on a separate grid from the rest of the product, select the alternate layout here. Otherwise, leave blank.

Date Restrictions for this section: Enter allowed dates for this section. Sometimes special sections are set up as their own products and sometimes a special section is set up as a section that only publishes on a specific date or date range inside the primary product.

## Positions

In the Position node, you will enter positions for a product if on the Product Details -> Campaign Parameters are set to "Yes or Mandatory" in the Enter Positions question. If the Positions by Section selection indicates that Positions are defined within each section, then you will select the section first and then create positions for that section. If the Positions by Section indicates that sections are independent of position, or if sections are not used at all for a product, then you will create positions without selecting a section first. Positions can be [imported ](importing-sections-and-positions.md#\_toc117696625)if desired and they can be [copied ](./#copy-sections-and-positions)from another product.

To create a new product, click the + and enter a position ID and position Name

### Digital-Specific Settings:

Choose the applicable size(s) for the position from the drop-down menu.

Choose the “Inventory Type” which could be Sponsorships, Impressions or No Inventory.

Enter the percentage of sellout warning above which the Sales Reps with one or more Campaigns in a Quoted or Reserved status will receive a system alert when the Total Available Impressions for this Position in a given month reach this level. For example, if there are 100,000 impressions available and this warning is set to 40%, the Sales Reps will be alerted when the Total Available Impressions for January reach 40,000 or below.

“Selling Warning by Order” field can be used to enter a percentage, for example, 10%. The Sales Reps with one or more Campaigns in a Quoted or Reserved status will receive a system alert when the Total Available Impressions for this Position falls within this margin when compared to the quantity on the Sales Rep's specific campaign. If this is set to 10%, when the available inventory for the month of January reaches 40,000 impressions, all Sales Reps with quotes or reserved orders in the month of January with quantities between 36,000 and 40,000 will receive an alert informing them that available inventory is almost gone.

### Print-Specific Settings

For Print Product Position the screen contains more fields to accommodate the flow into Naviga Plan.

The following settings do not impact on Naviga Ad, but they will impact the placement of ads in Naviga Plan if you Auto Plan the orders onto pages. Users can choose to manually place orders elsewhere in Plan, but these settings will affect where Plan will automatically place ads.

* Page Priority:
  * Any page: No control in plan from this field, ads will flow with other ads when being sent to plan. May be used with other fields below.
  * Absolute page: Plan will auto place the ad on the page number entered in “Requested Page Number” field. If that number is positive Plan will count that many pages forward from front of publication. If negative Plan will count that many pages backwards from last page of publication. For example, 2 would be page 2 or inside front cover, -2 would be 2 pages in counting from back cover or Inside Back Cover. When "Absolute Page" is selected it is counting from the total number of pages in the Product.
  * Relative page: This is the same as Absolute Page in that it is looking at the number in the requested page number field, but the difference is that this is looking at the page number relative to the section it is in. If there are no sections in this product, it will be the same as Absolute Page. If you do have sections, for example Sports section, Back Page position will be Relative page and -1 in the Requested Page number. This will be the Back Page Relative to the Sports section, but may not be the last page in the entire publication.
  * Early: Plan would place ad as far forward as possible after any absolute/relative pages. "Early" means in the first 25% of the pages.
  * Front Half: Ad would be placed within first ½ of publication
  * Back Half: Ad would be placed within last ½ of publication
* Quadrant: This determines placement on page for ads that are less than full page. Options here are Top, Left, Bottom, Right, Top Left, Top Right, Bottom Left, Bottom Right.
* Page Position: This can be don't care, left hand page, or right hand page.
* Requested Page Number: See above as referenced.
* Position is Guaranteed: If yes, then this position is guaranteed on an order for the ad. This will set a visible flag on the ad so that the planning user knows now to manually move the ad elsewhere.

The following WILL affect the booking behavior in Naviga Ad:

* Max. Pages Allowed: ex. 1.000 - this will limit the number of pages permitted to be booked for a single issue date.
* Conflicting Positions: You can choose other Positions to indicate they conflict with this Position. The conflict will be based on two Advertisers with the same industry code. For example, General Motors cannot buy the Back Page if Toyota has purchased the Inside Back Page.
* Only Used on Ratecards: If yes, then this position is available only when you use a Ratecard on the order.
* Max Ad Count: Entering a quantity in this field allows you to control the maximum number of ads even if the maximum number of pages which can be sold on this Position in an issue has not been reached. The system alerts the user to lack of inventory while entering the order. Leave this field blank or zero value if you do not want a maximum number of ads enforced in an issue position. When used, the Maximum Page Count is first checked, and if set to a value greater than zero, the system then applies the Max Ad Count number if there is adequate Maximum Page Count remaining.
  * For e-newsletters the Max Ad Count field must be filled in for the position to be available in line item entry.
* This Position is only Published on: This day of week dropdown allows you to select one or more days of the week that this position should be allowed on. When booking, the system first evaluates issue dates for the product, then issue dates/days of week for the section, and then it evaluates the position. For example, if the section only runs on Fridays, setting a position for that section as running on mondays is not going to allow you to book anything.

### As Relates to Naviga Plan <a href="#_toc117696623" id="_toc117696623"></a>

Naviga Ad allows flexibility in business rules for sections and positions. These may be set as not used, as optional or as required. For products interfacing to Naviga plan, there are rules that are enforced by Naviga Plan. It is recommended that these rules are considered when determining what fields are required for ads that will flow to Naviga Plan.

**At least ONE of these must be true on an order for it to go to plan:**

* There is a section
* There is a position
* There is a section and a position
* There is a classified category (for liner ads and classified display ads)

As classified ads will have a classified category, they do not technically require a section. However, if you do choose to make sections required in Naviga Ad, then you will need to at least have a generic “Classified” section to house all classified categories. This will allow you to populate the required field in Naviga Ad, Naviga Plan will ignore the section if a category is present.

Naviga ad views classified sections by product and allows for use of the same section code across multiple products. Naviga Plan allows for the same setup but does not allow for the same section ID to mean different things in different products. For example, if you have a section id 123 meaning “News” in one publication, you cannot have section id 123 meaning “Sports” in another publication. Section ID’s should at least be consistent across products, if not unique across all products.

As Naviga Plan automatically flows advertising by section/position/category it is also not advisable to allow duplication between classified category ID’s and section ID’s. As an example, a classified category of PET should not use the same code as a publication section of PET Duplicating these codes could result in inaccurate pagination. Please consult with your implementation specialist as you make these setup decisions.

## Inventory by Position <a href="#_toc117696624" id="_toc117696624"></a>

This is only relevant for Digital Products with Impression-based Inventory, and only if using Naviga Inventory. Click the node “Inventory by Position” to enter inventory of the positions for the product. Note the current calendar year defaults in the field.

You have the option to enter each month’s budget manually or click the “Auto Fill” button so that you can automatically fill in the value of the $ budget amounts equally in each month or divide it evenly per month. When finished click the Save button.

You can also instead click “Copy” button to copy the budget from another product’s existing budget, or to copy from a different year from the same product.

## Copy Sections and Positions

Sections and/or positions can be copied from one product to another.

<figure><img src="../../../../../../.gitbook/assets/image (804).png" alt=""><figcaption></figcaption></figure>

Select the Copy "from" and "to" products at the top. Select one or multiple sections to copy and be sure to check the "include positions" option if you also wish to include positions.
