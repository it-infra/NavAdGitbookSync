# System Tables Setup (A/R)

## Payment Terms Setup

Navigate to A/R Module, Setup -> System Tables Setup -> Payment Terms Setup

<figure><img src="../../../.gitbook/assets/image (294).png" alt=""><figcaption></figcaption></figure>

Enter an ID and Description for each of your payment terms. In Due Dates indicate the number of days until the payment is due under the given payment terms. If a discount rule applies, enter the % discount and for how many days that discount is available.

In the dropdown, select the rule for the date calculation. Options are

* Days from invoice date
* From end of invoice date month
* From end of invoice date month plus one

## Currency Setup

Navigate to A/R Module, Setup -> System Tables Setup -> Currency Setup

Click on “New” to create the foreign currency you would like to track throughout the system reports.

Enter the currency ID, name, exchange rate, symbol and HTML symbol (if applicable) to be used in the invoice forms and all templates across Naviga Ad

{% hint style="info" %}
The exchange rate is used to calculate the local equivalency for transactions entered in this currency.

When changing this rate it is recommended that you use the system functionality to revalue transactions with an open balance.

The local currency is calculated by dividing the foreign amount by the exchange rate.

Examples:

If $1.00 (US Dollar) = £0.60 (UK pounds) then: If your local currency is US dollars then the exchange rate will be 0.6000 If your local currency is UK Pounds then the exchange rate will be 1.6700
{% endhint %}

The foreign currency must be setup with a bank which has a remit to address. Naviga Ad uses this Bank's Lockbox address (if any) to display on the Invoices for this currency.

<figure><img src="../../../.gitbook/assets/image (1045).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note: The average rate is only necessary if you have other system instances / databases in different currencies. If so, this rate is used when uploading the G/L from those other databases in to your local G/L.
{% endhint %}

Enter the G/L Settings which are the codes against which any dealings with the currency will be done against these codes.

<figure><img src="../../../.gitbook/assets/image (1191).png" alt=""><figcaption></figcaption></figure>

The first one is the Exchange G/L Code, for calculating the exchange rate and using this GL code for it, the conversion code for when you run the conversion to the local currency and the AR code for posting to AR purposes. Exchange GL Code is used automatically by the system to record differences in Local values caused by changes in Exchange rates over time. However, it is typically between Billing and Cash Receipt, and will be used on Cash Receipt records and “SC” Journal Entries (changes in posted Cash Receipt records).

For example, an Invoice from 2017-10 is CAN$200/USD$180 but is paid with a 2017-11 Payment that is CAN$200/USD$185. In CAN$, the Invoice is paid off, but the system must record that the USD$5 “overpayment” is an FC Exchange loss.

The Conversion G/L Code is an optional one which is rarely used, and only in the case of importing other databases in foreign currencies combined into one conversion G/L code which in this case would be used when uploading these foreign currencies.

The A/R G/L Code is used for Book clients only. Please refer to the helpdesk for any questions on this field if you are a book customer.

## Tax Setup

Navigate to A/R Module, Setup -> System Tables Setup -> Tax Setup

Select New and at a minimum, enter tax ID, Tax Description, tax rate and G/L code for the tax. Tax rate supports up to 5 decimal places.

Enter other settings as needed.

<figure><img src="../../../.gitbook/assets/image (1531).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (465).png" alt=""><figcaption></figcaption></figure>

## Bank Setup

Navigate to A/R Module, Setup -> System Tables Setup -> Bank Setup

![](<../../../.gitbook/assets/image (474).png>)

Click New to create a new bank. At a minimum, the following must be filled in to save the bank

* Bank ID
* Bank Name
* Bank G/L Account
* A/R G/L Account

Add additional G/L codes as needed based on your use of the system. (for example, if you don't deal in foreign currencies, you don't need the Currency Exchange G/L. If you aren't using our A/P, you wouldn't need the A/P G/L's, etc) You will likely want a Discount G/L, a Write-off G/L, and a Default G/L Cash account.

#### For users of our A/P system:

Fill in below fields as needed:

<figure><img src="../../../.gitbook/assets/image (296).png" alt=""><figcaption></figcaption></figure>

The check form dropdown will be set up by Naviga Personnel in the back end of the system. See your implementation specialist or Naviga Support if you need assistance.

If payments below a certain value can use a stored signature then enter the signature image name in the Auto Signature Image Name field, and the max amount allowed for Auto-signature in the field above it. This will need to be coordinated with Naviga to store the Image file.

If approvals are required for amounts over a certain amount, enter the details in the A/P Payment Approval section.

If paying by ACH in the A/P modue, fill in the appropriate fields here. Naviga A/P module will create a file for ACH but doesn't auto process any ACH payments.

#### **BACS**

For Naviga Clients using the UK's BANKERS AUTOMATED CLEARING SYSTEM fill in the BACS section:

![](<../../../.gitbook/assets/image (469).png>)

#### Other Settings

Fill in Lockbox details for this bank. This will be used on foreign currency invoices to direct foreign currency clients to pay to an alternate lockbox address than local currency clients

<figure><img src="../../../.gitbook/assets/image (1640).png" alt=""><figcaption></figcaption></figure>

Credit Card Settings

The Credit Card Gateway selection at the bottom is for Spreedly & Naviga Pay Clients.

<figure><img src="../../../.gitbook/assets/image (90) (1).png" alt=""><figcaption></figcaption></figure>

Naviga Pay Field Delimiter - This assigns an alternate field delimiter to be used for certain Nabiga Pay banks who couldn't use the default delimiter. Do not set anything here unless instructed to do so by Naviga personnel

Spreedly Gateway - Only for sites using Spreedly for payments. Select the applicable Spreedly gateway from the dropdown.

Naviga Pay Gateway - This is a read only field that lets us know that a Naviga Pay gateway is linked to a given bank. (For a bank to be available as a dropdown on Credit Card payments it needs to be linked to a gateway - so this is useful to support and implementation to indicate that the back end link has been done.)

## Class Setup

Navigate to A/R Module, Setup -> System Tables Setup -> Class Setup

See Class Setup informaton in [A/R Invoices section](../invoices/#\_toc65155656)

## Financial Period Setup

Navigate to A/R Module, Setup -> System Tables Setup -> Financial Period Setup. (Can also [Import Financial Periods](../../system-settings-admin/setup/financial-period-setup-and-import.md) in the System Settings Module.)

To manually create new financial periods, enter a number at the top for how many periods you would like to create and click apply.

<figure><img src="../../../.gitbook/assets/image (1621).png" alt=""><figcaption></figcaption></figure>

The system will auto-create the new periods. Change the end period to desired end date for each month if the default isn't want you want. The start date for the next period will auto-adjust to the day after the prior period end date.

## Batch Type Setup

Navigate to A/R Module, Setup -> System Tables Setup -> Batch Type Setup

Enter an ID and description for any payment batch types you wish to create. click the + sign to add it to the list. Check the inactive checkbox for any batch types you no longer with to accept. Click save to save the batch types.

<figure><img src="../../../.gitbook/assets/image (381).png" alt=""><figcaption></figcaption></figure>

## Name Reason Codes

When changing a name/address in the system you can put in the reason for the change

<figure><img src="../../../.gitbook/assets/image (573).png" alt=""><figcaption></figcaption></figure>

Navigate to A/R Module, Setup -> System Tables Setup -> Name Reason Codes. Set up as many Name Reason Codes as you need for your business.

<figure><img src="../../../.gitbook/assets/image (1545).png" alt=""><figcaption></figcaption></figure>

## Address Setup

Navigate to A/R Module, Setup -> System Tables Setup -> Address Setup

In a system table called “Address Setup” user can create countries, country groups, counties, zip codes, import zip codes, states or regions, and time zones.

Note that the values in all the upcoming dropdowns related to taxes, currency, and so forth are values which have to be setup prior to this step in the other respective systems tables.

Once all these values are setup in each node, the system will auto populate default values based on user entries all throughout Naviga. For example, if a user is entering a phone number for a contact in the US, then the system till automatically enter that phone number in the format created in this menu screen.

### Time Zone Setup <a href="#_toc474147074" id="_toc474147074"></a>

Start with the node “Time Zone Setup”. Scroll to the bottom of the screen and enter an ID which is a maximum of 10 characters, a description and then choose a UTC code from the drop down list. Then click on the + sign to add the new time zone.

![](<../../../.gitbook/assets/1 (81).png>)

Once you enter several IDs, you can change the sort number which is the order number of the time zone determining where it appears on the list, and then click on “Apply Sort”. Then click on the “Save” button to store the time zone.

Note that you can delete the time zone using the red x button, only if it has not been used in the system. Once it has been used for clients’ addresses, then you cannot delete it and the red x button turns grey.

### Country Setup <a href="#_toc474147075" id="_toc474147075"></a>

Click on the Country setup node. You can delete any country from this list using the “Delete” button. This will not allow users to be able to choose the country from anywhere in Naviga.

To create a new country, click on “New”.

<figure><img src="../../../.gitbook/assets/image (1009).png" alt=""><figcaption></figcaption></figure>

Enter a country ID, up to 10 characters.

Enter the country name, which is free form text. Choose the continent from the drop down menu. You can choose a country group from the drop down menu to group this country with others for business purposes. For example, a group can be North American or European or Near East and so forth. Choose the default time zone from the drop down and enter a sort number determining the order in which this country will appear on the list and throughout Naviga.

Fill in the ISO codes and numbers if applicable.

<figure><img src="../../../.gitbook/assets/image (1338).png" alt=""><figcaption></figcaption></figure>

Enter the default tax code, currency, and forms language for this country (if applicable)

If International Tax ID and/or Registered Company Number are required before the account can be approved, please check "Yes" on those fields (Common in Norway)

<figure><img src="../../../.gitbook/assets/image (404).png" alt=""><figcaption></figcaption></figure>

Apply all applicable choices regarding the zip codes requirements for shipping and mailing items as well as the phone codes for calling clients. For example, a 011 for international calls and so forth.

Enter the zip code formats as well as the phone number formats in the respective sections. This will determine the automatic formatting which Naviga will adopt when you enter an address or phone number for a client or contact in the system.

<figure><img src="../../../.gitbook/assets/image (551).png" alt=""><figcaption></figcaption></figure>

You can enter more than one format. For example, for the phone number, you can enter the 7 digit number or 10 using parenthesis for the area code, or just the 10 digits with no spaces. Similarly for the zip code, you can enter the accurate number of 5 digits or 5 digits + 4 digits, and so forth. When you need to enter a new line, at any time, click the + next to the menu Add 1 New Lines, or choose Add 2 New Lines and click the +.

Enter the tax registration format in the same way and click the “Save” button.

{% hint style="success" %}
HINT: In the zip formats above you will see the last column (Digits) is asing for a number in this field. This is the number of digits we will validate against. So if you say 5 in **both** the zip and zip plus 4 we only validate the zip code. If you say 9 in zip plus 4 you would either have to load every zip+4 or every time you type one in/import one it will force you to add to the database, so you might want to consider putting 5 in both of those fields.
{% endhint %}

### Country Group <a href="#_toc474147076" id="_toc474147076"></a>

Click the node Country Group to create groups in which you can enter more than one country together. For example, United States and the territories can be in one group. Or all EU countries in one group and so forth. This is for reporting and organization purposes throughout Naviga.

![](<../../../.gitbook/assets/6 (25).png>)

You can always use the delete button to remove a group. Click “New” to create a new group. Name the group and then choose the countries in the group from the drop down menu. Choose the delivery methods by which user will mail items to clients in these countries.

You can also choose special delivery methods from the drop down in case one is needed. Click on the “Save” button when finished.

### County Setup <a href="#_toc474147077" id="_toc474147077"></a>

Click the node County Setup to create new counties. Choose the country and state from the respective drop down menus.

![](<../../../.gitbook/assets/7 (29).png>)

Enter the county ID and description and then click on the + sign. Repeat till all counties are entered and then click on the save button.

### State/ Region Setup <a href="#_toc474147078" id="_toc474147078"></a>

Click the node State/ Region Setup. Choose the country from the drop down menu for which you want to create regions or states.

![](<../../../.gitbook/assets/8 (2) (1).png>)

Enter an ID and description for each region. Choose the Tax Region and whether it is tax exempt or not and then click the + sign. Repeat the process and save when finished.

### Zip Code Setup <a href="#_toc474147079" id="_toc474147079"></a>

Click the node “Zip Code Setup”. This section will fill in default values for when users enter a zip code in the system, and Naviga will populate the name of the county, city and all tax related information as entered below.

Choose a country from the drop down menu. And then click the “New” button.

![](<../../../.gitbook/assets/9 (38).png>)

Enter the new 5 digit zip code, and enter the names of the cities, one for each blank box, which are included in the zip code. Choose the state, tax region, geographic region and time zone from the drop down menus.

Choose the county from the drop down and click the +sign, and then click on the save button. In the future, when you want to edit this zip code, type it in and the list will open displaying the zip code. Click the zip code in the list and all the information will display and be available for editing.

![](<../../../.gitbook/assets/10 (26).png>)

### Import Zip Codes <a href="#_toc474147080" id="_toc474147080"></a>

Click the node “Zip/ Postal Code Import” to bring in many zip codes or postal codes at a time from a spreadsheet.

Click on the button “Download Template”. Note that all yellow highlighted columns must have values which already match values in Naviga, but only the bold columns are mandatory to enter.

![](<../../../.gitbook/assets/11 (4).png>)

<table data-header-hidden><thead><tr><th width="161"></th><th></th><th></th><th></th></tr></thead><tbody><tr><td>Column Name</td><td>Description and Format</td><td>Example</td><td>Mandatory (Yes/No)</td></tr><tr><td>Code</td><td>Zip code or postal code</td><td>45209</td><td>Yes</td></tr><tr><td>Region ID</td><td>This is the name of the region or state.</td><td>OH</td><td>No, but value has to match existing values in the State/ Region Setup node in the address setup table.</td></tr><tr><td>City Name</td><td>Name of the city with this zip code. You can enter several cities with different names and same zip codes on different lines.</td><td>Cincinnati</td><td>Yes</td></tr><tr><td>Time Zone</td><td>This is the time zone of the city or region.</td><td>EST</td><td>No, but value has to match the values entered in the node Time Zone from this menu screen.</td></tr><tr><td>Tax Region ID</td><td>This is the tax region where this code lies.</td><td>OH</td><td>No, but value has to match the value in Naviga</td></tr><tr><td>County</td><td>This is the name of the county where this zip code is.</td><td>Westchester</td><td>No, and value can be any free text format entry.</td></tr><tr><td>County FIPS</td><td>This is the name of the county five-digit Federal Information Processing Standard (FIPS) code (FIPS 6-4) which uniquely identifies counties and county equivalents in the United States, certain U.S. possessions, and certain freely associated states. The first two digits are the FIPS state code and the last three are the county code within the state or possession.</td><td>42-987</td><td>No and free entry with the accurate FIPS for the county.</td></tr></tbody></table>

Fill in as many rows as the template allows. You can use the same zip code but with different cities on several lines.

Save the template on your desktop. Then in the Naviga import screen, click on the select and browse to upload the template. Choose the country from the drop down menu so these zip codes would be associated with this country in the system.

Then click on “Test Import” button. This is mandatory and will alert you to any errors in the template before importing. If you see any errors, click the OK button and read the errors. Click the remove button on the screen to remove the incorrect template from the upload. Browse for the template on your desktop and correct the errors. Be sure to save the template again. Then repeat the upload process in Naviga and test import till all errors are corrected.

When ready, click on “Import File” button. The system will give you an import success message.

To view the imported zip codes, click on the node Zip Code Setup and choose the country from the drop down. Then start typing the first 3 numbers in your zip code and the list will display. Choose the ones you want to review by clicking on them in the list.

![](<../../../.gitbook/assets/12 (23).png>)

You can edit any further fields on this screen and click the save button to store the information.

## Spreedly Gateway Setup

Navigate to A/R Module, Setup -> System Tables Setup -> Spreedly Gateway Setup

This is typically set up by Naviga Personnel

## Email Type Codes

Navigate to A/R Module, Setup -> System Tables Setup -> Email Type Codes

Set up desired Email Types. This will be used when adding email addresses to contact person records.

<figure><img src="../../../.gitbook/assets/image (1410).png" alt=""><figcaption></figcaption></figure>
