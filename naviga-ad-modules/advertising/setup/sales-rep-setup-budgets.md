# Sales Rep Setup / Budgets

## Sales Rep Group <a href="#_toc118884994" id="_toc118884994"></a>

Rep Groups are used in User Security to provide access to certain orders in some reports such as the Orders by Product Report. For example, if I run the Orders by Product report for a certain date range and certain product and I only have access to Rep Group ABC, then only the orders belonging to Rep Group ABC will be returned in that report. It is also used in grouping Reps together in the Sales Manager's performance view on the Rep Activity screen.

Navigate to the advertising module on the system and click on the menu Setup -> Sales Rep Setup/ Budgets -> Sales Rep Setup -> Groups node.

To create a new group, click the New button. Enter a new ID, and description. Then select a sales rep from the drop-down menu if any exist. You can leave this blank until you create a new sales rep. Choose the rep and then click the + sign to add the sales rep to the new group.

Once the new group is saved, the delete option can delete the newly created group.

Repeat the process of adding more sales reps to the group and save.

![](<../../../.gitbook/assets/1 (53).png>)

Sales reps can be removed from the group by mouse clicking the red x button.

## Territories <a href="#_toc118884995" id="_toc118884995"></a>

The sales reps’ territories are beneficial in the analysis reports to display the sales by reps’ territories.

Click the node Territories under the setup tree. Type in a new territory id and description then click the + sign to add a new territory to your list.

![](<../../../.gitbook/assets/2 (57).png>)

Remember to click Save before navigating to a different screen.

## Sales Rep Setup <a href="#_toc118884996" id="_toc118884996"></a>

Click the Sales Reps node under the setup tree. You can maintain the rep information from this screen or add a new rep. To create a new one, click the New button.

![](<../../../.gitbook/assets/3 (21).png>)

Enter the sales ID in the New Sales Rep ID field, and sales rep name in the Sales Rep Name field. Choose the Primary Group from the drop-down menu, which is the group you created in this guide above.

Choose the territory to assign to the rep from the Territory drop-down menu. Enter the contact information for the rep.

At any time, to mark this rep as inactive and hide the rep from users in the system, click the box for “Inactive” to change that value to “Yes”. Marking a rep as inactive will not nullify their previous orders or their commissions. This action is reversible. The inactive flag prevents selection of the rep in order entry and brand maintenance. The Salesrep’s orders will still be displayed in reporting. If you wish to hide the Salesrep in reporting, first move the Salesrep to a different Salesrep group and limit access to this group in order to filter reporting.

Mark the rep as an outside rep and not in your company by clicking on the box for “Outside Sale Rep” to change that value to “Yes”. This is beneficial to users who hire rep firms so that instead of having a salesperson on payroll, user can have a contract with an agency that sells ads for the user. Outside rep firms are much more likely to have a simple commission structure. For every ad the rep sells, the user pays the external rep a percentage of the price of the ad. This makes processing the external rep’s commissions simpler in paperwork and processing.

This is tracked in the commission report when the data is exported to Excel. In the export, user can filter on the outside reps separately from the internal reps. This is also mapped in Informer reports.

Enter the commission percent for product orders for this rep under the Commissions section, which will default into the orders in the order entry screen.

In the field “Alert via Email when Campaign Approval is Required” you can select the rep’s manager(s) who must approve orders when the system is setup to allow for manager’s approval. When the sales rep creates an order, the user(s) listed here receives an email which allows him to review the order and approve or reject it.

Click Save to create the new settings.

## Sales Rep Import <a href="#_toc118884997" id="_toc118884997"></a>

For your convenience, you can Import a list of sales reps into the system by using the Import function. Click the Import node under the Sales rep setup tree and click Download Template button to use the system template. This will ensure an error free import of your sales rep. Fill out the columns provided with the respective data and save the template to your desktop. These columns are as follows:

<table data-header-hidden><thead><tr><th width="171"></th><th width="131"></th><th width="340"></th><th></th></tr></thead><tbody><tr><td><strong>Field Name</strong></td><td><strong>Example</strong></td><td><strong>Source</strong></td><td><strong>Mandatory</strong></td></tr><tr><td>ID</td><td>SHF</td><td>Free alphanumeric entry maximum 10 characters. All special characters will be removed and all lower case will be converted to upper case.</td><td>Yes</td></tr><tr><td>Full Name</td><td>David Smith</td><td>Free alphanumeric entry</td><td>Yes</td></tr><tr><td>Primary Group ID</td><td>SH Group</td><td>Value pre-existing in system</td><td>No</td></tr><tr><td>Primary Group Name</td><td>South Hampshire</td><td>Value pre-existing in system. If the value does not match the existing name, the existing name will be updated.</td><td>No</td></tr><tr><td>Territory ID</td><td>NE</td><td>Value pre-existing in system</td><td>No</td></tr><tr><td>Territory Name</td><td>North East</td><td>Value pre-existing in system</td><td>No</td></tr><tr><td>Email</td><td>david@cvb.com</td><td>Free entry of valid email</td><td>No</td></tr><tr><td>Phone</td><td>9145654444</td><td>Free entry of valid phone number</td><td>No</td></tr><tr><td>Mobile</td><td>9145654444</td><td>Free entry of valid phone number</td><td>No</td></tr><tr><td>Digital Commission Percent</td><td>5</td><td>Free entry Numeric value</td><td>No</td></tr><tr><td>Reference ID</td><td>3232</td><td>Alphanumeric ID for the rep</td><td>No</td></tr><tr><td>Outside Rep</td><td>Yes</td><td>“Yes” for an outside rep and No for an internal rep</td><td>No</td></tr><tr><td>Discounts Up to Percent</td><td>10</td><td>Numeric percentage value to indicate how much discount percentage of the order this rep is allowed to give users.</td><td>No</td></tr><tr><td>Campaign Approval Alert Email Address</td><td>KSMITH</td><td>This field has been changed in newer versions and must now be the User ID of the approving user and not actually the email address.</td><td>No</td></tr><tr><td>Inactive</td><td>Y</td><td>Y for Yes, it is inactive and N for No it’s active.</td><td>No</td></tr></tbody></table>

Fill in the template and save to your desktop.

Click the Select button, browse for the template. If you choose to Overwrite Existing Files and set that box to “Yes”, then the existing sales rep names in system will be replaced with the new data in the template. Leave the option as “NO” if you are importing new sales reps. Then click the Import button. The reps will be imported in the system.

You can view and edit the imported sales reps and their data by navigating to the Sales Reps node and viewing them in the drop-down list.

## Associate Sales Rep with User ID <a href="#_toc118884998" id="_toc118884998"></a>

You can map a user to one or more sales rep and sales rep groups.

Navigate to the menu Setup -> User Security.

Choose the user ID from the drop-down menu which can be the same as the sales rep ID. Click the node “Rep/ User Integration”.

<figure><img src="../../../.gitbook/assets/image (475).png" alt=""><figcaption></figcaption></figure>

Scroll to the section “Access to Orders”. Click on the sales rep group(s) which you want to associate with this user/sales rep and click on the right >, which will move to the “Assigned Sales Reps Groups”. This allows this user ID to view orders for all sales reps in this group(s).

In some cases a sales person exists in the system only for recognition as the selling rep for commission purposes and they do not log into the system at all. In other cases, the sales reps are logging in and using the CRM and/or Order Entry portions of the system. If the rep is actually logging into the system, the the section “Ad Reps < -- > User ID Association” will link the USER ID with the REP ID, click on the sales rep(s) and click the > to move this to the “Ad Reps Assigned to this User”

Under Advertising -> Analysis -> Commissions, there are a number of commission reports, where one rep may have access to these, so the system checks User Security, Rep/User Integration, Assigned Sales Rep Groups and allows this rep to see commission details for ALL reps in the rep group to which he has access. Note that you must ensure to use menu security to restrict access to these reports as the current system setup allows reps access to order information for all co-reps, but not to all these reports.

Under the CRM Rep shortcut menu, reps can access the “My Commissions” menu. The reps available in this dropdown are controlled by User Security, Rep/User Integration, Ad Rep <--> User ID Associations. If user associates his login with another rep or more, he will see these reps’ names and can select one or both. If the rep is set to only see himself, then the information to other reps is hidden from the rep.

## Sales Rep Budget <a href="#_toc118884999" id="_toc118884999"></a>

### Budget by Product

Navigate to the menu Setup -> Sales Rep Setup/ Budget -> Sales Rep Setup Budgets by Product.

Choose the sales rep from the drop down, the product and the year.

<figure><img src="../../../.gitbook/assets/image (675).png" alt=""><figcaption></figcaption></figure>

In the respective fields for each month, enter the budget amount, any forecast amounts you expect of this month and rep. You may use the “Auto Fill Numbers” button for a speedier data entry. Click the “Save” button when finished.

Repeat the process if applicable for each rep and product in this screen. (Or see below for procedure to Import)

### Budget by Format

Navigate to the menu Setup -> Sales Rep Setup/ Budget -> Sales Rep Setup Budgets by Format.

Choose the sales rep from the drop down, the format and the year.

<figure><img src="../../../.gitbook/assets/image (731).png" alt=""><figcaption></figcaption></figure>

In the respective fields for each month, enter the budget amount, any forecast amounts you expect of this month and rep. You may use the “Auto Fill Numbers” button for a speedier data entry. Click the “Save” button when finished.

Repeat the process if applicable for each rep and format in this screen. (Or see below for procedure to Import)

## Import Rep Budget <a href="#_toc78201764" id="_toc78201764"></a>

### Import Salesrep Budgets by Product <a href="#_toc78201764" id="_toc78201764"></a>

Navigate to the menu Setup -> Salesrep setup/ Budgets -> Import Salesrep Budgets -> Import Salesrep Budgets by Product node.

![](<../../../.gitbook/assets/1 (90).png>)

Note that you can choose the import to be for Budget or Forecasts. Choose which one you wish from the drop-down menu.

Click the button “Download Template” and fill in the columns as described below in the template section.

Save the template on your desktop. Click the “Select” button to browse for the saved template. Then click “Test import File”.

If there are errors in the file, the system alerts you to that during the testing step. If there are errors, click the x remove button and then fix the errors in the template.

Resave the template and re-upload the file. Repeat the step to iron out all the issues in the template.

![](<../../../.gitbook/assets/2 (43).png>)

When there are no more errors, click “Import File”.

Once the file is successfully imported, then you can search for the Salesrep budget in that menu searching by product.

#### Salesrep Budgets by Product Template <a href="#_toc78201765" id="_toc78201765"></a>

<table data-header-hidden><thead><tr><th width="161"></th><th width="115"></th><th width="306"></th><th></th></tr></thead><tbody><tr><td><strong>Field</strong></td><td><strong>Example</strong></td><td><strong>Conditions</strong></td><td><strong>Mandatory/ Optional</strong></td></tr><tr><td><strong>Rep ID</strong></td><td>SHIGH</td><td>This is the ID of the Salesrep as it is in the system under Salesrep Setup menu.</td><td>Mandatory</td></tr><tr><td><strong>Product ID</strong></td><td>AST</td><td>This is the Product ID as it is in the system in the Product Setup menu</td><td>Mandatory</td></tr><tr><td><strong>January</strong></td><td>444,000</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>February</strong></td><td>444,500</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>March</strong></td><td>445,000</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>April</strong></td><td>445,500</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>May</strong></td><td>446,000</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>June</strong></td><td>446,500</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>July</strong></td><td>447,000</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>August</strong></td><td>447,500</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>September</strong></td><td>448,000</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>October</strong></td><td>448,500</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>November</strong></td><td>449,000</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>December</strong></td><td>449,500</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr></tbody></table>

### Import Salesrep Budgets by Format <a href="#_toc78201766" id="_toc78201766"></a>

This menu allows you to import Salesrep budgets by format of the product being print, digital or otherwise. Navigate to the menu Setup -> Salesrep setup/ Budgets -> Import Salesrep Budgets -> Import Salesrep Budgets by Format node.

Note that you can choose the import to be for Budget or Forecasts. Choose which one you wish from the drop-down menu.

Repeat the download, upload and import steps as described in the section above of import by product.

The budget/ forecast numbers can be viewed after the format in the menu Setup -> Salesrep Setup/ Budgets -> Salesrep Budget by Format.

#### Salesrep Budgets by Format Template <a href="#_toc78201767" id="_toc78201767"></a>

<table data-header-hidden><thead><tr><th width="147"></th><th width="152"></th><th width="332"></th><th></th></tr></thead><tbody><tr><td><strong>Field</strong></td><td><strong>Example</strong></td><td><strong>Conditions</strong></td><td><strong>Mandatory/ Optional</strong></td></tr><tr><td><strong>Rep ID</strong></td><td>SHIGH</td><td>This is the ID of the Salesrep as it is in the system under Salesrep Setup menu.</td><td>Mandatory</td></tr><tr><td><strong>Format ID</strong></td><td>ENEWS</td><td>This is the Product Format ID as it is in the system in the Setup -> Product Format Setup menu</td><td>Mandatory</td></tr><tr><td><strong>January</strong></td><td>444,000</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>February</strong></td><td>444,500</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>March</strong></td><td>445,000</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>April</strong></td><td>445,500</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>May</strong></td><td>446,000</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>June</strong></td><td>446,500</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>July</strong></td><td>447,000</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>August</strong></td><td>447,500</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>September</strong></td><td>448,000</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>October</strong></td><td>448,500</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>November</strong></td><td>449,000</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr><tr><td><strong>December</strong></td><td>449,500</td><td>Free entry numerical entry of the amount of budget in this month.</td><td>Mandatory</td></tr></tbody></table>

## Rep Budget Summary <a href="#_toc118885000" id="_toc118885000"></a>

You may view the budget of several reps by product group, from the CRM module if you click the menu tile Budgets/Quotas. In this screen, choose the Product Group which encompasses the products which have the reps you had setup above. Choose the period through which the data is retrieved, the option of budget or forecast for the print and digital and then press “Select Data”.

<figure><img src="../../../.gitbook/assets/image (1029).png" alt=""><figcaption></figcaption></figure>

The data can be grouped by sales rep, product name, product format, annual budget, YTD Budget, YTD Billed Amount, Confirmed Amount, Reserved Amount, and Quoted Amount.

These amounts are calculated as follows:

The YTD Billed amount displays amount reflecting the total amounts billed for orders in the billed status starting from the beginning of the current year until the period preceding the period you entered in the selection criteria. For example, if the period you entered in 2018-06 (June 2018), this field reflects the total of the billed amounts starting January 2018 till May 2018.

Confirmed Amounts field displays the totals for the orders ranging from the period entered in the financial period selection criteria till the end of the current year where these orders are confirmed and in the running status. For example, if you enter the period of 2018-06 for June 2018 in the selection criteria, this field gives the total of orders ranging from 2018-06 through 2018-12 for confirmed orders in the running status.
