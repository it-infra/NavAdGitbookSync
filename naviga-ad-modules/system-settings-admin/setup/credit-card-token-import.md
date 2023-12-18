# Credit Card Token Import

The credit card token import process will import existing tokens into the system so that you don't need to have existing credit card clients provide their payment information again. You will need to have your processor export this information so that it can be imported into Naviga Ad.

Navigate to System Settings -> Setup -> Credit Card Token Import.

## Import Template

Select the button to Download Template. Fill in the columns as described below. Save the file to your desktop.

<table><thead><tr><th width="168">Field</th><th width="195">Example</th><th width="245">Source of Data</th><th>Mandatory / Optional</th></tr></thead><tbody><tr><td>Customer ID</td><td>100140</td><td>This is the ID of the customer in Naviga. It must match the ID of a customer already created in the system</td><td>Either Customer ID or Legacy Customer ID is required</td></tr><tr><td>Legacy Customer ID</td><td>200157897</td><td>This is the ID of the customer in the Legacy System. It must match the Legacy ID of a customer already created in the system</td><td>Either Customer ID or Legacy Customer ID is required</td></tr><tr><td>Customer Profile ID</td><td>n/a</td><td>This field is no longer used and will be removed in a future version.</td><td>Not used - Leave Blank</td></tr><tr><td>Payment Profile ID</td><td>79739894</td><td>This is the token ID provided by your payment processor</td><td>Mandatory</td></tr><tr><td>Cardholder Name</td><td>Alice D Linn</td><td>Name on the Credit Card</td><td>Optional</td></tr><tr><td>Card Type</td><td>Visa</td><td>Type of Credit Card</td><td>Optional</td></tr><tr><td>Masked Card Number</td><td>************1234</td><td>This will be the masked credit card number displayed in the system and if desired, added to the credit card receipt</td><td>Optional</td></tr><tr><td>Expiry MM</td><td>11</td><td>This is the 1- or 2-digit month of the expiration.</td><td>Optional</td></tr><tr><td>Expiry YY</td><td>25</td><td>This is the 2-digit year of expiration</td><td>Optional</td></tr><tr><td>Bank Code</td><td>BOFA</td><td>This is the Bank Code ID as set up in Naviga <a href="../../accounts-receivable-credit-control/setup-a-r-system-setup/system-tables-setup-a-r.md#bank-setup">Bank Setup</a></td><td>Mandatory</td></tr><tr><td>Card Description</td><td>Marriott Visa</td><td>This is the credit card description displayed on the customer account in Cards on File list</td><td>Optional</td></tr></tbody></table>

Click on “Select” and upload the template you saved. Click “Test Import File” and the system alerts you to any errors in the template you made.

Click “Close” and then click “Remove x”. Navigate back to the template on your desktop and correct the errors. Save the template and then re-select the template to upload into Naviga from the import screen. Once all errors are cleared and the system provides you with a success message, click “Import File”.

Fill in the import template with the details as described below in the given examples. The table provides you with the source of data which must match Naviga data.
