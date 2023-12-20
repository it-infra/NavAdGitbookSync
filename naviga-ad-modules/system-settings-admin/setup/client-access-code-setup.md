---
description: This will only display if Client Access Codes are enabled by Naviga Support
---

# Client Access Code Setup

Also See [Name Maintenance](../../accounts-receivable-credit-control/customers-a-r/#a-r-setup) for additional information on Client Access Codes

<figure><img src="../../../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

Navigate to **System Settings module -> Setup -> Client Access Code Setup**.  Note this will only be displayed as an option if Naviga support/implementation personnel have enabled the system to use access codes.  Please contact support if you need this to be enabled.

To manually create access codes, enter an ID and a Description and click the + to add to the list. Repeat for each needed Access Code. If the access codes are the same as the companies in your system or the Product Groups in your system, use the short cut buttons at the top to load all companies or Product Groups as Access Codes.

Click Save to save the codes.

## Assign/Update Access Codes via Spreadsheet

Access codes can be assigned to clients via Spreadsheet from this screen. &#x20;

1. Click the button "Import from Spreadsheet.
2. Click Download Template button to download template with the following fields:

<table><thead><tr><th width="185">Field</th><th width="108">Example</th><th>Description</th><th>Required?</th></tr></thead><tbody><tr><td>Client / Legacy ID</td><td>123456</td><td>This is the Naviga ID if the Client or the Legacy ID of the client.  If using Legacy IDs be sure to click Yes on the Import Screen</td><td>Yes</td></tr><tr><td>Access Code(s)</td><td>AA,BB</td><td>This is the ID from the above Access Code table.  Can assign multiple with comma separating the values.  Code provided must match code already setup in the system.</td><td>Yes</td></tr><tr><td>Append / Replace / Delete</td><td>R</td><td>R=Replace<br>A=Append<br>D=Delete</td><td>No.  If left blank the R will be applied and any existing access codes will be replaced with the new value.  D will delete just the access codes in the spreadsheet.</td></tr></tbody></table>

3. Fill in the spreadsheet and save to your desktop.
4. Click select in the File to Import field and navigate to your saved spreadsheet.
5. If using legacy ID in the Client ID field, click Yes to use Lagacy ID
6. Click test import file and note any errors
7. If any errors were found in the file, click the x to remove the spreadsheet from the File to Import field and open the spreadsheet and correct the errors
8. resave the file and repeat steps 4-7 until no errors are found.
9. Click Import File to import the file and update customer records.
