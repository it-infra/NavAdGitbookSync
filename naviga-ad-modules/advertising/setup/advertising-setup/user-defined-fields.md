# User Defined Fields

Users can create user defined fields (UDFs) for a product group or a product, so that these different sets of UDFs are available for user in the campaign entry screen and/or the line items.

User Defined Fields are additional customized fields which the system provides in the campaign entry process to allow user to enter data which applies only to user’s needs and which are not available in the standard system fields.

There are two sets of UDFs. The first set is available for setup at the product group level and these display on the campaign User Defined Fields screen when the campaign is created using products which belong to this product group. The second set of UDFs are available for setup per product and will appear on the campaign line item entry screen.

## Campaign User Defined Fields <a href="#_toc79062073" id="_toc79062073"></a>

These are the UDFs which display on the campaign entry screen under the node “User Defined Fields” and which apply to the campaign created for a product group which contains these UDFs.

### Setup <a href="#_toc79062074" id="_toc79062074"></a>

Navigate to the Advertiser module’s menu Setup -> Advertising Setup -> Campaign User Defined Fields.

<figure><img src="../../../../.gitbook/assets/image (1108).png" alt=""><figcaption></figcaption></figure>

Note the types of UDFs which can be created are listed under each node on the left side tree.

* “Text/ Integer Fields” are ones which can be used to enter alphanumeric values. This can be any general information which is beneficial to enter regarding the order. Add specific values to make this a drop down selection, or leave the values blank and it will be a free-format field to enter info.
* The “Money/ Decimal Fields” are ones which you can use to enter dollar amounts or numeric quantities, such as marketing amounts, budgets, and so forth.
* The “Date Fields” are ones where user entering an order sees a pop-up calendar to mark specific dates which are important to attach to the campaign. For example, they can be important production dates, or approval dates of the campaign and so forth.
* Finally, the “Multi-Select Fields” are ones which give entry user a list of options to check one or more values which apply to the campaign. For example, conditions or restrictions which apply to this campaign.

To create any of the fields above, choose the UDF number from the “Selected Field ID” and type a “Field Name” description. This description is what the entry user sees and can fill in in the campaign user defined screen. To allow user to have free entry, leave the “Value” and “Description” fields blank.

Repeat the process to add more than one UDF and click “Save”.

### Product Group UDFs <a href="#_toc79062075" id="_toc79062075"></a>

These UDFs must be assigned to each product group so that they display on the campaign entry screen of user defined fields.

Navigate to the Advertising module’s menu Setup -> Product Setup -> Product Group Details. Search in the drop-down menu of “Product Group” for the group to be setup with the UDFs.

Scroll to the section titled “User Defined Fields” and click on the UDF desired in the left hand side pane “User Defined Fields Not Allowed”. Then click the right arrow -> to move the field to the “User Defined Fields Allowed”.

You can also click the double right facing arrows >> if you would like to move all UDFs to the Allowed pane. When finished, click the “Save” button.

## Campaign Line Item User Defined Fields <a href="#_toc79062076" id="_toc79062076"></a>

These UDFs display on each line item and must be setup separately.

### Setup <a href="#_toc79062077" id="_toc79062077"></a>

Navigate to the menu Setup -> Advertising Setup -> Campaign Line Item User Defined Fields.

Setup looks exactly the same as the Campaign level UDF's, except that these will be available for selection only at the product level.

### Product UDF Setup <a href="#_toc79062078" id="_toc79062078"></a>

These UDFs must be added to the specific product so that they display on the line items for campaigns using this product.

Navigate to the menu Setup -> Product Setup and click the “Product Details” node. Choose the product from the drop-down menu and click the tab “Order UDFs”.

Choose the desired UDF according to the ones which you have setup. Check the “Required” box to make them mandatory in the line item entry if desired. Repeat the process of choosing more UDFs and click the + sign every time. When finished, click the “Save” button.

## Campaign Entry

**For the Campaign-Level UDF:**

In the campaign entry screen using desired group and any product within this group, click the node “User Defined Fields”.

The fields added to the product setup appear on this screen with the Value blank for you to fill in the data as desired.

![](<../../../../.gitbook/assets/image (1521).png>)

**For the Order-Level UDF:**

Create a new campaign or edit an existing one for this product and click the line item.

Click the tab “Custom Fields” and note that the UDF displays where you can enter a value. The system displays a checkmark in the required box if you had set it up as mandatory. Click “Add Line”.

This is a different UDF from the ones created on the campaign.

![](<../../../../.gitbook/assets/image (1274).png>)
