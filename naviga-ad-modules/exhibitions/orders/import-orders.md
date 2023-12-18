# Import Orders

User can import exhibition orders into the Exhibition module using a provided template. This process allows you to import historical and billed orders that can be used for reporting and analysis. This import requires that each show and its associated setup tables are setup in Exhibition before importing the orders. The imported orders will be flagged as billed. Changes to these orders will not be allowed. The Order Amounts should be in the Billing Currency. A Ratecard is required on each order. The import will create a fixed rate price line on the ratecard for the space id.

Navigate to the menu Orders -> Import Orders.

![](<../../../.gitbook/assets/1 (20).png>)

To use a legacy client ID in the spreadsheet which matches the Exhibition client, click on the corresponding box to that field to change the value to “Yes”. If you do not wish to use a legacy client ID in the sheet, then leave the value as “No”.

To create any missing divisions not existing in Exhibition already for this client, click on the corresponding box to change that value to “Yes”. If the divisions for the imported orders for this client already exist in Exhibition, then leave the value as “No”.

Click on the button “Download Template” and an excel sheet will open with different columns related to the exhibition’s order.

### Import Template <a href="#_toc74924941" id="_toc74924941"></a>

The fields are to be filled out as follows:

<table data-header-hidden><thead><tr><th width="157"></th><th width="130"></th><th width="270"></th><th></th></tr></thead><tbody><tr><td><strong>Field Name</strong></td><td><strong>Sample</strong></td><td><strong>Source</strong></td><td><strong>Optional/ Mandatory</strong></td></tr><tr><td><strong>Exhibitor ID</strong></td><td>14009</td><td>Must be either the Legacy client ID matching a value in Exhibition or must be the Exhibition client ID.</td><td>Mandatory</td></tr><tr><td><strong>Division ID</strong></td><td>A3</td><td>This must match the Exhibition division ID for this client.</td><td>Mandatory</td></tr><tr><td><strong>Division Name</strong></td><td>Hand Made</td><td>Free form alphanumeric for the division name.</td><td>Optional</td></tr><tr><td><strong>Bill-to ID</strong></td><td>14009</td><td>The bill to ID for this client. Value must match the ID in Exhibition. Information is found in the exhibitor maintenance screen.</td><td>Optional</td></tr><tr><td>Bill-to Contact ID</td><td>14090</td><td>This is the contact ID for the bill-to contact which must match the value in Exhibition. This can be found in the exhibitor maintenance screen.</td><td>Optional</td></tr><tr><td>Order Amount</td><td>1000</td><td>Numeric value for the total amount of the order.</td><td>Optional</td></tr><tr><td>Tax Amount</td><td>2</td><td>Free form numeric value for the tax amount. If this field is entered, the system will request a tax code to be entered in that field, but the reverse is not true.</td><td>Optional</td></tr><tr><td>Currency ID</td><td>USD</td><td>This is the currency used in the billing of this order and the value must match the ID defined in Exhibition in the currency system table setup screen.</td><td>Optional</td></tr><tr><td>Rep ID</td><td>SH</td><td>This is the rep ID which must match the value in the sales rep setup screen. This rep will be attached to this order.</td><td>Mandatory</td></tr><tr><td>Legacy Order ID</td><td>1344</td><td>This is the legacy order ID which value will be stored in Exhibition.</td><td>Optional</td></tr><tr><td>Tax Code</td><td>21</td><td>Must match the tax code setup in Exhibition tax systems table.</td><td>Optional</td></tr><tr><td>Show ID</td><td>2SH</td><td>This is the exhibition ID which must match an existing value in Exhibition in the exhibition setup screen.</td><td>Mandatory</td></tr><tr><td>Entry Date</td><td>04/20/2020</td><td>Date the order is entered for this show</td><td>Optional</td></tr><tr><td>Hall ID</td><td>1</td><td>This is the hall ID where the exhibitor order is placed; also found in the exhibition setup screen.</td><td>Optional</td></tr><tr><td>Section ID</td><td>H1</td><td>This is the section ID for this order and the value must match the existing Exhibition value in the exhibition setup screen.</td><td>Optional</td></tr><tr><td>Space ID</td><td>H111</td><td>This is the ID of this space assigned to this order and value must match the space ID in the exhibition setup screen in Exhibition.</td><td>Mandatory</td></tr><tr><td>Description</td><td>3 x 3</td><td>This is the space description in free form alphanumeric entry.</td><td>Optional</td></tr><tr><td>Length</td><td>3</td><td>Free form numeric value of the length of the space.</td><td>Optional</td></tr><tr><td>Depth</td><td>3</td><td>Free form numeric value of the depth of the space.</td><td>Optional</td></tr><tr><td>Adjustment</td><td>2</td><td>Free form numeric of the adjustment if any to this order as needed to add or subtract space.</td><td>Optional</td></tr><tr><td>Open Sides</td><td>2</td><td>Numeric value of the open sides on this space.</td><td>Optional</td></tr><tr><td>Points</td><td>4</td><td>Free form numeric of number of points in the space.</td><td>Optional</td></tr><tr><td>Industry Type ID</td><td><a href="mailto:adv@adv.org">ACC</a></td><td>This is the PIB/ Industry code value which must match an existing value in Exhibition.</td><td>Optional</td></tr><tr><td>Order Type ID</td><td>NBS</td><td>This is the order type ID as setup in the systems tables and must match that value existing in Exhibition.</td><td>Mandatory</td></tr><tr><td>Exhibitor Type ID</td><td>SH</td><td>This is the exhibitor type ID value which must match the value in Exhibition systems tables’ setup.</td><td>Optional</td></tr><tr><td>Ratecard ID</td><td>SHD</td><td>This is the ratecard used for this exhibition and the value must match the one in Exhibition in the ratecard setup menu.</td><td>Mandatory</td></tr><tr><td>Space Type ID</td><td>SP</td><td>This must match the space type ID defined in Exhibition exhibition setup screen.</td><td>Mandatory</td></tr><tr><td>Ratecard Line ID</td><td>100</td><td>This must match the existing Ratecard Line ID in Naviga</td><td>Mandatory</td></tr><tr><td>UDF Text 1</td><td>Testing</td><td>Text to fill in the first UDF text field as per setup in Naviga</td><td>Optional</td></tr><tr><td>Service Id 1</td><td>12</td><td>Alphanumeric value for Service ID</td><td>Optional</td></tr><tr><td>Service Description 1</td><td>Service provided</td><td>Alphanumeric value for service description 1</td><td>Optional</td></tr><tr><td>Service Amount 1</td><td>300</td><td>Numeric value for the amount for the service</td><td>Optional</td></tr><tr><td>Service Tax Code 1</td><td>0</td><td>Tax Code ID for the service tax</td><td>Optional</td></tr><tr><td>Service Tax Amount 1</td><td>0</td><td>Numeric amount for the tax.</td><td>Optional</td></tr></tbody></table>

Note that:

* The imported orders will be flagged as fully billed.
* Changes to these orders will not be allowed.
* The Order Amounts should be in the Billing Currency.
* A Ratecard is required on each order
  * The import will create a fixed rate price line on the ratecard for the space id

Once finished, save the spreadsheet to your desktop, and then on the import screen, click on the button “Select”.

Browse for the file and upload it to Exhibition. Click on the button “Test Import File”. The system will alert you to any errors if you click OK on that message.

![](<../../../.gitbook/assets/2 (80).png>)

Click on Close and then fix the error in the spreadsheet and save it and repeat the select and test process every time till you get a success message to import.

![](<../../../.gitbook/assets/3 (25).png>)

Click on “Import File”. You will receive a success message.

To view the imported order(s), navigate to the Home page and see the list of orders.

![](<../../../.gitbook/assets/4 (7).png>)

You can click the hyperlink to the order and view the order but not edit the order.

You can also navigate to Analysis -> Orders by Show and find the orders for that show.
