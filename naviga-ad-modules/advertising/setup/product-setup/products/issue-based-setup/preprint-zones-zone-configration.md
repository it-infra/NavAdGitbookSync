# Preprint Zones / Zone Configration

## Zone Groups Setup <a href="#toc21458135" id="toc21458135"></a>

Zones give user the ability to build multiple distribution layers for Inserts/Preprints. Each layer contains smaller zones within the group. User can create this data within the Advertising system or import it using system provided templates. Zones allow user to store up to 5 dimensions of data. For example, in postal code 10012 there are XX subscribers, XY non-subscribers, YY dealers, and so forth. The Zone Groups hierarchy allows the order entry user to select a city and it could auto select all child zip codes. The Zone selection in Order Entry allows user to see and select from this hierarchy and even build a radius map.

Note that Zone Group must be setup for the Zones tab to appear in the campaign line entry screen. When you create zones, they must be assigned to a group.

Navigate to the menu Setup -> Product Setup -> Zone Groups. Select a product from the drop-down menu.

<figure><img src="../../../../../../.gitbook/assets/image (773).png" alt=""><figcaption></figcaption></figure>

Click the button “Add a New Group”. Enter the information in the respective fields as needed.

<figure><img src="../../../../../../.gitbook/assets/image (695).png" alt=""><figcaption></figcaption></figure>

The sort codes allow for the display of the group in alphabetical order.

Continue to build sub-groups as needed and click the save button after each group is created.

Alternatively, you can import the hierarchical group structure using the provided template. Click on the button “Import Data”.

![](<../../../../../../.gitbook/assets/3 (44).png>)

Click the button “Download Empty Template” to fill out all the groups and sub-groups from scratch. Or if you have some groups in the system on which you’d like to build, click the button “Download Template with Current Groups”. This template downloads the sheet prefilled with existing information from the Advertising system.

The template consists of the following fields:

<table data-header-hidden><thead><tr><th width="155"></th><th></th><th width="314"></th><th></th></tr></thead><tbody><tr><td>Field Name</td><td>Example</td><td>Conditions</td><td>Mandatory/ Optional</td></tr><tr><td><strong>Group ID</strong></td><td>SH2</td><td>Must match the group ID already existing in the advertising system</td><td>Mandatory</td></tr><tr><td>Group Name</td><td>First sub- group</td><td>Alphanumeric value for the group name for column one</td><td>Optional</td></tr><tr><td><strong>Parent ID</strong></td><td>SH1</td><td>Must match the parent group ID which already exists in the advertising system</td><td>Mandatory</td></tr><tr><td>Country Code</td><td>US</td><td>Country code value</td><td>Optional</td></tr><tr><td>Postal Code</td><td>10583</td><td>Alphanumeric value for the zip code</td><td>Optional</td></tr><tr><td>Latitude</td><td>44.0051</td><td>Numeric Latitude of the location</td><td>Optional</td></tr><tr><td>Longitude</td><td>73.7846</td><td>Numeric Longitude of the location</td><td>Optional</td></tr></tbody></table>

You can click the button on the import window to “Replace Current Groups” and this overwrites the current groups for this product. If left unchecked at the value “No”, then the groups originally in the system will remain and the imported ones will be added according to the layout in the template.

When finished, save the template to your desktop and upload it to the Advertising system using the button “Import Groups” on the import window. When finished, click the save button.

## Zone Setup <a href="#toc21458136" id="toc21458136"></a>

The system allows for a more detailed setup for zones for the date-based products. Click the node “Zone Setup” on the tree.

<figure><img src="../../../../../../.gitbook/assets/image (213).png" alt=""><figcaption></figcaption></figure>

The screen allows you to enter details for each zone using the group structure you created above. You can also enter numbers for the [zone dimensions](../../../advertising-setup/zone-dimensions.md) per day. The dimensions are an additional layer of details for the zones. You must assign the zone to a group in order for the Zones tab to display on the line item entry screen.

Note the Inactive flag available for each zone. Use this flag to indicate that a zone that was used in the past will no longer be available for use. For orders that have already been created while the zone was active, the order will not be modified. If you open the order, you will see that it is now inactive, and new orders will not have the option to select that Zone anymore.

<figure><img src="../../../../../../.gitbook/assets/image (619).png" alt=""><figcaption></figcaption></figure>

Any FUTURE orders that were already booked using that zone will need to manually be edited to have the zone removed if the delivery will not be done to the zone anymore.

## Zone Import

Zone import and Zone Import by Date Range allow you to enter the zones and circulations for an issue and mass import them into the Ad system instead of manually entering them. The difference between them is that the Zone Import will be expecting a count for each issue date. The Zone import by date range will have a start and stop date and day of week. So you could them import a count for say Wednesdays between Jan 1 and March 31 of a given year, and a different number for Sundays in that same date range.

The Zone import is also imported per product. The Zone import by date range can be done for multiple products simultaneously.

Navigate to the menu Setup -> Product Setup -> Zone Import. Choose the product from the drop-down menu. Only issue based products display in the list.

Click the field “Create Missing Zones” to change its value to “Yes” if you would like the import to create the zones. If the zones are new, and do not exist in the system, this must be a “Yes”. If left as “No”, the template must have Zone IDs that match ones in the system for the issues.

Click the button “Download Template”. This opens a spreadsheet template with the following fields which you can fill out and save to your desktop.

#### Template <a href="#toc40970099" id="toc40970099"></a>

<table data-header-hidden><thead><tr><th width="149"></th><th width="130"></th><th width="267"></th><th></th></tr></thead><tbody><tr><td><strong>Field Name</strong></td><td><strong>Example</strong></td><td><strong>Data Source and Conditions</strong></td><td><strong>Mandatory/ Optional</strong></td></tr><tr><td><strong>Issue Date</strong></td><td>2/28/2019</td><td>This is the date of the issue for the product and must match an existing issue date in the system.</td><td>Mandatory</td></tr><tr><td><strong>Zone ID</strong></td><td>19545</td><td>Free format alphanumeric. Must match system values if the field to create missing zones is set to No.</td><td>Mandatory</td></tr><tr><td>Zone Description</td><td>Philadelphia</td><td>Free format alphanumeric description of the zone ID.</td><td>Optional (but really should use one, even if the same as the ID)</td></tr><tr><td>Parent ID</td><td>CITY</td><td>Zone Group this Zone belongs to. (select the immediate parent here, not the grandparent.)</td><td>Mandatory</td></tr><tr><td><strong>CirculationA</strong></td><td>15000</td><td>Numeric free entry</td><td>Mandatory</td></tr><tr><td><strong>CirculationB, etc</strong></td><td>17500</td><td>Numeric free entry</td><td>Mandatory if you are using additional <a href="../../../advertising-setup/zone-dimensions.md">dimensions </a>in Setup.</td></tr></tbody></table>

On the import page, click on the “select” button and upload the file from your desktop to the system. Click on the button “Test Import File”. The system alerts you to any errors on the sheet.

If there are any, click the x remove button by the template you uploaded to remove it from the system. Then correct all the errors in the sheet. Resave the file to your desktop and then re-upload it, using the select button on the import page.

Repeat this step to test the import file till all errors have been fixed and the system provides you a success message.

Click the button “Import File”. The system provides a success message.

If you navigate to the Issue Configuration node on the tree on the left side of the screen and click on “Zones” hyperlink per issue as per the import, the system displays the zones and circulation, which you imported, attached to the issues.

## Zone Import by Date Range

You can import zones also by start and end date range for a product. Once the end date passes, these zones are no longer valid for the product and will no longer be visible in the line item entry screen.

#### By Date Template <a href="#toc40970101" id="toc40970101"></a>

<table data-header-hidden><thead><tr><th width="161"></th><th width="124"></th><th width="309"></th><th></th></tr></thead><tbody><tr><td><strong>Field Name</strong></td><td><strong>Example</strong></td><td><strong>Data Source and Conditions</strong></td><td><strong>Mandatory/ Optional</strong></td></tr><tr><td><strong>Product ID</strong></td><td>BE</td><td>The ID must match that of a product in the advertising system</td><td>Mandatory</td></tr><tr><td><strong>Start Date</strong></td><td>04/01/2019</td><td>MM/DD/YYYY date format and can be any start date.</td><td>Mandatory</td></tr><tr><td><strong>End Date</strong></td><td>04/01/2022</td><td>MM/DD/YYYY date format and can be any end date past the start date</td><td>Mandatory</td></tr><tr><td><strong>Zone ID</strong></td><td>NW</td><td>The Zone ID must match the zone ID in the advertising system if the field “Create Missing IDs” on the import screen is set to “No”.</td><td>Mandatory</td></tr><tr><td>Zone Description</td><td>Northwest territory</td><td>Text describing the zone</td><td>Optional (but really should use one, even if the same as the ID)</td></tr><tr><td>Parent ID</td><td>BG</td><td>The zone parent ID of the zone for the zone to be imported and must match the value in the advertising system</td><td>Mandatory</td></tr><tr><td><strong>Day of Week</strong></td><td>Monday</td><td>Monday through Sunday using the full word upper or lower case.</td><td>Mandatory</td></tr><tr><td><strong>Circulation A</strong></td><td>20000</td><td>Numeric value for the circulation.</td><td>Mandatory</td></tr><tr><td><strong>Circulation B</strong></td><td>20000</td><td>Numeric value for the circulation.</td><td>Mandatory if you are using additional <a href="../../../advertising-setup/zone-dimensions.md">dimensions </a>in Setup.</td></tr><tr><td><strong>Circulation C</strong></td><td>20000</td><td>Numeric value for the circulation.</td><td>Mandatory if you are using additional <a href="../../../advertising-setup/zone-dimensions.md">dimensions </a>in Setup.</td></tr><tr><td><strong>Circulation D</strong></td><td>20000</td><td>Numeric value for the circulation.</td><td>Mandatory if you are using additional <a href="../../../advertising-setup/zone-dimensions.md">dimensions </a>in Setup.</td></tr><tr><td><strong>Circulation E</strong></td><td>20000</td><td>Numeric value for the circulation.</td><td>Mandatory if you are using additional <a href="../../../advertising-setup/zone-dimensions.md">dimensions </a>in Setup.</td></tr><tr><td>Sort Code</td><td>1</td><td>Value by which the zone is sorted in the list as displayed on menus for users.</td><td>Optional</td></tr><tr><td>Country Code</td><td>US</td><td>This is the 2-digit ISO Country Code.</td><td>Optional</td></tr><tr><td>Postal Code</td><td>10591</td><td>5-digit zip code for the zone.</td><td>Optional</td></tr><tr><td>External Reference</td><td>ABC123</td><td>Alpha-numeric Field used in integration with 3rd party</td><td>Optional</td></tr><tr><td>External Group</td><td>ABC</td><td>Alpha-numeric Field used in integration with 3rd party</td><td>Optional</td></tr></tbody></table>

Follow the same steps to import as in the previous section of this document.

## Issue Zone Configuration

For the most part, Zones and Zone counts will always be imported. It just isn't practical to manually enter in so many zones...ain't nobody got time for that!

That said, this page is helpful if you need to visualize what you just imported and ensure that what you intended has gone into the correct places, and/or to make a minor correction to something. This displays per issue date. (I will often peek in here to remind myself if I imported in next years zones or not.) Just find the desired date and click the Zones link. The popup display will show the counts for the zones in that issue.

<figure><img src="../../../../../../.gitbook/assets/image (262).png" alt=""><figcaption></figcaption></figure>
