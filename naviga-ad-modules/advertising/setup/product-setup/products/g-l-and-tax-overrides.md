# G/L & Tax Overrides

### G/L Override

Click the G/L Overrides tab and enter G/L codes for any G/L Types that deviate from what the Default revenue G/L code is for this product.

In the simple example below, the default G/L for this print product is the Display Revenue for the Daily Paper. In the G/L Overrides, the Print Classified G/L is defined. The product will need to be set up with G/L Overrides for anything that deviates from the default G/L.

<figure><img src="../../../../../.gitbook/assets/image (1570).png" alt=""><figcaption></figcaption></figure>

Note that for allowing you to split Ratecard and campaign entry line to track cost on third party lines, you can apply a Cost G/L code and a Cost A/P Code.

<figure><img src="../../../../../.gitbook/assets/image (762).png" alt=""><figcaption></figcaption></figure>

See Ratecard setup for more info on [Cost Rates.](pricing-rules/ratecards.md#cost-rates)

### G/L Override Import

G/L Override Import is available in the Product Setup screen. These are the G/L codes necessary for the Product to work in Naviga and these can be imported to override the default G/L accounts in the Product Setup.

Navigate to the menu Setup -> Product Setup -> G/L Override Import node. Click Download Template button and the system provides excel template with the fields below for you fill in the data. Once complete save the template to your desktop.

Click Select to upload the template and then click Test Import to make sure the template alerts you to any errors in the template before importing. If there are any errors, click the red x to remove the template from the import screen. Fix the errors and re-save, then re-select the file to upload it. Once all errors are gone and the test import passes successfully, click on the “Import File” button.

### Template fields <a href="#_toc117528548" id="_toc117528548"></a>

<table data-header-hidden><thead><tr><th width="146"></th><th width="127"></th><th width="317"></th><th></th></tr></thead><tbody><tr><td><strong>Field Name</strong></td><td><strong>Example</strong></td><td><strong>Conditions</strong></td><td><strong>Mandatory/ Optional</strong></td></tr><tr><td><strong>Product ID</strong></td><td>WP</td><td>Mandatory and must match the Product ID in Naviga</td><td>Mandatory</td></tr><tr><td><strong>GL Type Code</strong></td><td>DISP</td><td>GL Type ID must match Naviga ID found in the menu Setup -> Advertising Setup -> G/L Type</td><td>Mandatory</td></tr><tr><td><strong>Revenue GL Code</strong></td><td>01*00*0002*00*0000</td><td>This is the revenue G/L code which must match G/L code in the system to attach to revenue.</td><td>Mandatory</td></tr><tr><td><strong>Agency Commission GL Code</strong></td><td>01*00*0007*00*0000</td><td>This is the revenue G/L code which must match G/L code in the system to attach to agency commission.</td><td>Mandatory</td></tr><tr><td>Industry Code</td><td>Books</td><td>This is the Industry Code to be overridden for the brand/advertiser. It’s a drop-down value to be chosen</td><td>Optional</td></tr><tr><td>Industry Rev GL Code</td><td>01*00*0007*00*0440</td><td>This is the industry revenue GL code override for this industry code</td><td>Optional</td></tr><tr><td>Industry Agency Comm GL Code</td><td>01*00*0007*00*0077</td><td>This is the agency commission GL code override for this industry code.</td><td>Optional</td></tr></tbody></table>

### Tax Override

If the Product is Taxable then the Billing process will use the Tax Code on the Clients Record. You can override the Client's Tax Code by setting an override Tax Code for this Product.

Click the Tax Overrides node and in the override tax code field, enter tax information you want to override the tax information in an order. In the bottom section, you can add exclusions. For example, supposed you have tax codes 1, 2, and 3 on various client accounts. But this product you want to always use Tax code 1, except if the client is using tax code 3. You could select tax code 1 as the override, and tax code 3 as an exclusion.

<figure><img src="../../../../../.gitbook/assets/image (1231).png" alt=""><figcaption></figcaption></figure>
