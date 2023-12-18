# Fixed Assets

This document is a guide on how to use the functions on the Fixed Assets menu in the G/L Module.

This module will let you to create Fixed Assets, Depreciate the Assets, Report on the Assets and Dispose or Transfer Assets.

The Fixed Assets functions allow users to keep track of the company’s Fixed Assets, such as:

* When they were purchased
* Where they are located
* How much they have depreciated
* If they were sold or disposed of
* If they were transferred between departments.

Assets can be entered into the system either automatically when entering a Purchase Invoice in the A/P Module or directly through Fixed Asset Maintenance. An asset is always assigned to a Department. You can define different Asset Types (such as furniture, automobiles or computers). The system allows four different methods of depreciating your assets.

## Setup <a href="#_toc85811849" id="_toc85811849"></a>

The following items should be set up before entering your first Fixed Asset.

### Department Setup <a href="#_toc85811850" id="_toc85811850"></a>

Because all assets must be assigned to a Department, first make sure that a list of departments has been set up in the A/P Module (examples: Accounts Payable, Human Resources, and Administration). To view the current list of Departments, navigate to A/P Module --> System Tables Setup --> Department Setup.

![](<../../.gitbook/assets/1 (54).png>)

To add a new Department, enter the desired ID and Name on the bottom row and then click the “+” icon. A Salaries Payable GL Code may be entered if this Department will also be used in the A/P Module.

### Asset Type Setup <a href="#_toc85811851" id="_toc85811851"></a>

For each Department, set up a list of product categories, such as: computer hardware, computer software, telephone equipment, office furniture, office supplies. To view or create these Asset Types, navigate to Fixed Assets --> Asset Type Setup. For each department/category combination, designate the G/L Accounts that will be used to track that Asset Type in the General Ledger. Start typing the description or G/L account number and the system will reveal a list of accounts which include this account.

![](<../../.gitbook/assets/2 (76).png>)

#### Depreciation Method

Finally, for each department/category combination, designate the default depreciation method and rate. During entry of a fixed asset, this default will populate when the asset type is selected but may be overwritten for individual assets.

**Straight Line -** the asset depreciates every year by the percentage entered. A steady decline of the value annually.

**Reducing balance** - the asset depreciates every year by the percentage entered, but the book value of the asset (cost less accumulated depreciation) is used instead of the original cost. So, if the asset is at a $100 value, and is set to depreciate by 2% per year, the value becomes $98 after the first period. The next period the beginning value is $98 and the depreciation by 2% per period is $96.04, and so forth.

**Fixed Amount** – a specific dollar amount of depreciation every period for the asset.

**Accelerated** - every period the asset depreciates by a certain percent according to the accelerated depreciation schedule that is entered. The schedule lists the periods through which the _annual_ percentage rate is as entered.

![](<../../.gitbook/assets/3 (33).png>)

For example, in the above schedule the annual rate is 50% for the first 6 periods (or 4.167% per period), then 30% from period 7 through 10 (2.5% per period), then 15% from period 11 through 20 (1.25% per period), etc.

### G/L Account Maintenance <a href="#_toc85811852" id="_toc85811852"></a>

After creating Asset Types, user may also go to each asset G/L account to add the fixed asset type as a reference on the G/L account. Navigate to G/L Module --> Accounts --> G/L Account Maintenance.

The detail accounts node is highlighted. Click the magnifying glass to search for a G/L account with description including “asset.” Choose the G/L account, and then scroll to the fixed asset type field in the advanced account settings section and choose one from the drop-down menu. Save the G/L account.

![](<../../.gitbook/assets/4 (75).png>)

This enables the automatic entry of fixed assets while entering purchase invoices if such a G/L account is used on the invoice.

## Creating a Fixed Asset <a href="#_toc85811853" id="_toc85811853"></a>

Fixed assets can be entered into the system either automatically when entering a purchase invoice or directly through fixed asset maintenance. Fixed assets may also be imported from a spreadsheet, adding convenience and additional features for use with pre-existing fixed assets.

Note that:

* Each Asset must be tied to an Asset Type
* An Asset can be tied to an A/P Invoice
* You must specify the Purchase Amount and the start Period for depreciation
* You can store documents, photos and Asset details (such as location, serial number) on the Asset

For example, we purchased a Laptop computer for someone in the Finance Department. It cost $1,500 and we are going to start depreciating it in January 2020. By assigning this asset to an Asset Type, the system will know the depreciation method and G/L allocation.

## A/P Invoice Entry <a href="#_toc85811854" id="_toc85811854"></a>

To create a fixed asset automatically when entering a Purchase Invoice, navigate to A/P Module --> Invoices --> A/P Invoice Entry --> Enter/Edit Invoices. This allows the user to create the asset and invoice in one easy step, linking the invoice to the fixed asset. Enter the Invoice as usual, then enter a G/L Account that has a fixed asset type set up. The system will then prompt the user to give more details about this asset.

![](<../../.gitbook/assets/5 (62).png>)

Fill in the fields accordingly and save. Also note that the G/L line item has a building block icon to edit the fixed asset information, different from the other G/L line items which are not fixed asset related.

![](<../../.gitbook/assets/6 (36).png>)

Click the save button and note the invoice ID. The purchase invoice still needs to be posted to A/P and posted to G/L for the new fixed asset record to be created.

If you then retrieve the fixed asset from the fixed asset maintenance menu, observe that the asset has the invoice ID linked to it. Also, fixed assets entered this way will be marked with “From A/P Invoice” = YES to distinguish them from fixed assets that are directly entered yet based on an existing A/P invoice.

## Fixed Asset Maintenance <a href="#_toc85811855" id="_toc85811855"></a>

To create a fixed asset directly, navigate to Fixed Assets --> Fixed Asset Maintenance and use the “New” button. Enter an asset description and vendor ID.

Optionally, if the asset is based on an existing A/P Invoice, choose an invoice ID for this vendor. User can use the magnifying glass to search for an invoice ID. The purchase date, purchase period (and therefore depreciation start period), and amount will populate using data from the invoice. User cannot create a new invoice from this screen to attach to the fixed asset.

Then choose the department and all the asset types created previously will pop up in the list. Selecting an asset type will default-in the depreciation method, rate, and G/L account settings per the set up.

![](<../../.gitbook/assets/7 (41).png>)

Note that if the depreciation method is “Accelerated,” then the depreciation rate will not default-in because the system does not refer to this field for the rate. However, it is still a required field so user will need to enter some data, typically the depreciation rate from the first row of the accelerated depreciation schedule.

Enter the purchase date and purchase period. The depreciation period will default to the same as the purchase period indicating that the fixed asset may be depreciated in the same month as purchased. If this is not the case, then user must manually change the depreciation period to the following month.

Finally, enter the purchase amount and \<Save> the record. Note that the system is not currently designed to account for salvage value. To record fixed assets that have a salvage value, user could enter the current net book value as a modified purchase amount and note the adjustment in the comments field.

Also note that depreciation to-date may not be entered directly. If a fixed asset is not truly new and already has accumulated depreciation, then it should be imported instead of entered directly. Otherwise, user could enter the current net book value as a modified purchase amount and note the adjustment in the comments field.

User may also enter more details about the fixed asset on the other information shutter.

## Import Fixed Assets <a href="#_toc85811856" id="_toc85811856"></a>

To create a fixed asset by importing from a spreadsheet, navigate to the menu Fixed Assets -> Import Fixed Assets. Then click “download template”.

Fill out the template and note that the bold columns are mandatory. The ones highlighted in yellow must match an existing ID in the system. Also note that import fixed assets does not allow for the creation of assets with an accelerated depreciation method. This is because the required accelerated depreciation schedule cannot be entered into the import file.

If a fixed asset is pre-existing (i.e. already has accumulated depreciation against it) outside of the system, then the depreciation to-date column may be non-zero. This is the only method of creating new fixed assets in the system with depreciation already recorded.

Save the completed template to your desktop. Then click the select button and browse for the saved file and click select. Enter the depreciation to-date financial period, and then click test import file button in order to ensure no errors exist in the file.

![](<../../.gitbook/assets/8 (15).png>)

If there are errors, click the OK button to view the nature of the errors. Then correct the errors in the excel template and save it again. Click the button remove to remove the previous file and then select it again. Click the test import file button again. When there is success, click the import file button. Once imported, then the fixed assets from the file will be searchable in the system.

### Import Template <a href="#_toc85811857" id="_toc85811857"></a>

<table data-header-hidden><thead><tr><th width="161"></th><th width="142"></th><th width="293"></th><th></th></tr></thead><tbody><tr><td><strong>Field Name</strong></td><td><strong>Example</strong></td><td><strong>Conditions</strong></td><td><strong>Mandatory/ Optional</strong></td></tr><tr><td><strong>Asset Description</strong></td><td>test</td><td>Free alphanumeric entry</td><td>Mandatory</td></tr><tr><td>Vendor ID</td><td>SH1</td><td>Vendor ID must match the vendor in Naviga Vendor Setup</td><td>Optional</td></tr><tr><td>Invoice ID</td><td>SH123</td><td>Must match the invoice ID in Naviga</td><td>Optional</td></tr><tr><td><strong>Purchase Amount</strong></td><td>1000</td><td>Free entry numeric value</td><td>Mandatory</td></tr><tr><td><strong>Purchase Date</strong></td><td>1/1/2021</td><td>Date entry according to system format</td><td>Mandatory</td></tr><tr><td><strong>Purchase Period</strong></td><td>2021-01</td><td>Must match the financial period format and value in Naviga</td><td>Mandatory</td></tr><tr><td><strong>Depreciation to Date</strong></td><td>2/1/2021</td><td>Free date entry as per Naviga format</td><td>Mandatory</td></tr><tr><td><strong>Department ID</strong></td><td>Art</td><td>Department ID as per the value in Naviga in AP menu Setup -> System Tables Setup -> Department Setup. This is where this asset is linked to the department on import.</td><td>Mandatory</td></tr><tr><td><strong>Asset Type</strong></td><td>AW</td><td>Must match the value in the menu Fixed Assets -> Fixed Assets Type</td><td>Mandatory</td></tr><tr><td><strong>Depreciation Method</strong></td><td>1</td><td>The values are as follows: 1 (Straight Line)<br>2 (Reducing Balance)<br>3 (Fixed Amount)</td><td>Mandatory</td></tr><tr><td><strong>Depreciation Rate</strong></td><td>1</td><td>Percent per year numeric value</td><td>Mandatory</td></tr><tr><td>Serial No</td><td>434343</td><td>Free entry alphanumeric value of the serial number</td><td>Optional</td></tr><tr><td>Location</td><td></td><td>Free entry alphanumeric value of the serial number</td><td>Optional</td></tr><tr><td>State</td><td>MN</td><td>Free entry alphanumeric value of the serial number</td><td>Optional</td></tr><tr><td>Tag No</td><td></td><td>Free entry alphanumeric value of the serial number</td><td>Optional</td></tr><tr><td>License No</td><td></td><td>Free entry alphanumeric value of the serial number</td><td>Optional</td></tr><tr><td>Comment</td><td></td><td>Free entry alphanumeric value of the serial number</td><td>Optional</td></tr></tbody></table>

## Calculate Depreciation <a href="#_toc85811858" id="_toc85811858"></a>

This process will calculate the depreciation amounts for one period, writing them to a new journal entry. Each financial period, you will run the process that calculates each Asset’s depreciation. This screen will show you a history of prior depreciation calculations. Running this process will generate a depreciation Journal Entry.

Navigate to the menu Fixed Assets -> Calculate Depreciation. Choose the desired period and then click “calculate period” and click the OK button. The available periods are controlled by the A/P Module open periods for the default A/P company.

![](<../../.gitbook/assets/9 (23).png>)

The calculate depreciation screen will list the date, time, and user for each calculation performed. The journal entry ID and the respective period of that depreciation are also listed. The journal entry is hyperlinked so that when user clicks the Journal ID, the new screen pops up with the journal details.

![](<../../.gitbook/assets/10 (23).png>)

Each journal entry includes depreciation expense and accumulated depreciation G/L accounts based on the asset type for all fixed assets that have not been previously calculated for the specific period. The total amount of debits (depreciation expense) can be compared with the List of Fixed Assets --> Asset Depreciation for a Year column matching the period.

If the journal entry appears to be missing some depreciation, then user should check for previous calculations of that period or incorrect setup of G/L accounts in asset types.

![](<../../.gitbook/assets/11 (14).png>)

The depreciation of each fixed asset is also recorded on the fixed asset maintenance screen. Navigate to the menu Fixed Assets --> Fixed Asset Maintenance, and type in the asset id. The depreciation for the latest period will be added to the depreciation to-date amount and the new net book value for the asset displays.

![](<../../.gitbook/assets/12 (26).png>)

Finally, the depreciation details shutter will list the amount of depreciation expense that has been calculated for that fixed asset in each period. If a period has been skipped in this list, then calculate depreciation may need to be run again for that period. Note that this section will only list the first 36 periods of depreciation.

![](<../../.gitbook/assets/13 (22).png>)

## Transfer Asset/Change Asset Type <a href="#_toc85811859" id="_toc85811859"></a>

From the asset maintenance screen, user can select an edit option to transfer the asset. For example, if client is moving a piece of equipment from one office to another or from one department to another.

<figure><img src="../../.gitbook/assets/14 (7).png" alt=""><figcaption></figcaption></figure>

Choose the option to transfer the asset. The pop-up window displays options to select the transfer period and then a new department (which then requires a new asset type as well) or new asset type. Click the save button.

![](<../../.gitbook/assets/15 (1).png>)

The system then creates a journal entry for this transfer, moving the asset and accumulated depreciation balances to the new G/L accounts. Click the hyperlink to the journal entry.

## Dispose of the Asset <a href="#_toc85811860" id="_toc85811860"></a>

From the asset maintenance screen, user can select an edit option to dispose of the asset in case they are getting rid of the equipment.

![](<../../.gitbook/assets/16 (13).png>)

Choose the option to dispose of the asset. The pop-up window displays options to select the disposal date, disposal period, and enter the reason. Click the save button.

![](<../../.gitbook/assets/17 (11).png>)

Another journal entry is created for this change. Click the hyperlink to view the details, or to make adjustments for salvage value or disposal costs. The journal entry will credit the entire asset amount and debit the to-date accumulated depreciation, and then record the difference to the disposal G/L account.

<figure><img src="../../.gitbook/assets/18 (1).png" alt=""><figcaption></figcaption></figure>

## List of Fixed Assets <a href="#_toc85811861" id="_toc85811861"></a>

Users can view a list of fixed assets by several different selection criteria and sorting. To do so, navigate to the menu Fixed Assets -> List of Fixed Assets.

1. Lists of fixed assets by their status
   1. Currently Depreciating Assets - for assets that are still depreciating
   2. Fully Depreciated Assets - for assets marked as fully depreciated
   3. Disposed Assets - for assets that have been disposed
2. Lists of fixed assets within a period range, all statuses
   1. Assets by Purchase Period - assets purchased within the range
   2. Assets by Depreciation Period – assets with depreciation recorded within the range
   3. Assets by Transfer Period – assets that were transferred within the range
3. Fixed asset reports
   1. Asset Depreciation for a Period – includes debits and credits from the Journal Entries
   2. Asset Depreciation for a Year – twelve period report
4. Custom Assets Listing - user can create their own criteria

Click the node for the desired listing or report. For other than the first three types, enter the period range or other required input and click Get Assets, then the listing will populate.

User can look up a fixed asset that has just been created by entering the Asset ID in the first column and the screen will refresh to reflect the new asset. User can click the hyperlinks to the Asset ID to get to the asset details screen.

![](<../../.gitbook/assets/19 (6).png>)

User can narrow down the list by typing partial characters from the displayed list. The same applies to the asset description, department, type, purchase period, vendor, invoice ID, and state.

![](<../../.gitbook/assets/20 (5).png>)

User can apply filters on the columns with the filter icon to be equal to, greater than and so forth. Enter the value and click the filter icon and choose the criteria.
