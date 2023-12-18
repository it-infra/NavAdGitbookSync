# Import Financial Statement Reports

User can import a financial statement report from the menu Financial Reports -> Financial Statement Reports. It is recommended to download the template and fill out the columns, test the import file then when the import is error free, user can import the file and view it.

![](<../../../../.gitbook/assets/3 (60).png>)

## Financial Report Template

Click the button download template.

<table><thead><tr><th width="137">Field</th><th width="134">Example</th><th width="425">Purpose</th><th>Required?</th></tr></thead><tbody><tr><td>Line ID</td><td>1</td><td>Unique numeric Identifier of the line.</td><td>Yes</td></tr><tr><td>Line Type</td><td>D</td><td><p>Valid <strong>Line Type</strong> values are:</p><ul><li>H (Heading)</li><li>D (Detail)</li><li>T (Total)</li><li><p>M (Math / Calculated Line)</p><ul><li>Note: Math lines are inserted in the positions from the import, but the calculations must be entered by editing the report after import.</li></ul></li><li>P (Spacer / Blank Line)</li></ul></td><td>Yes</td></tr><tr><td>Debit or Credit</td><td>D</td><td><p>Valid <strong>Debit or Credit</strong> values are:</p><ul><li>D (Debit)</li><li>C (Credit)</li></ul></td><td>No</td></tr><tr><td>Description 1</td><td>Revenue</td><td>This is the description which will appear on the report for the line.</td><td>Yes</td></tr><tr><td>Description 2</td><td>Ad Revenue</td><td>The is an optional section line of the description</td><td>No</td></tr><tr><td>Line Style</td><td>1</td><td><p>Valid <strong>Line Style</strong> values are:</p><ul><li>[Blank] (None)</li><li>1 (Single Overline)</li><li>2 (Single Underline)</li><li>3 (Single Over/Underline)</li><li>4 (Double Overline)</li><li>5 (Double Underline)</li><li>6 (Double Over/Underline)</li></ul></td><td>No</td></tr><tr><td>Bold Line</td><td>Y</td><td><p>Values are:</p><ul><li>Y (Yes)</li><li>N or [Blank] (No)</li></ul></td><td>No</td></tr><tr><td>Print Line</td><td>N</td><td><p>Values are:</p><ul><li>Y (Yes)</li><li>N or [Blank] (No)</li></ul></td><td>No</td></tr><tr><td>Statistical Line</td><td>N</td><td><p>Values are:</p><ul><li>Y (Yes)</li><li>N or [Blank] (No)</li></ul></td><td>No</td></tr><tr><td>G/L Account Selection</td><td><strong>01*0000*0000*1000</strong></td><td><p>The <strong>G/L Account Selection</strong> allows you to enter complex, multi-valued account criteria. Multiple entries must be separated with commas and hyphens used to define ranges.<br>The following are valid examples using a 4-level G/L structure</p><ul><li>Select a single account: <strong>01*0000*0000*1000</strong></li><li>Select multiple accounts: <strong>01*0000*0000*1000</strong>, <strong>01*0000*0000*1001</strong>, <strong>01*0000*0000*1002</strong></li><li>Select a wildcard driven range: <strong>01*0000*0000*^000</strong></li><li>Select a range: <strong>01*0000*0000*1000</strong> - <strong>01*0000*0000*2000</strong></li><li>Select a combination: <strong>01*0000*0000*1000</strong> - <strong>01*0000*0000*2000</strong>, <strong>01*0000*0000*3000</strong>, <strong>01*0000*^000*0000</strong></li></ul></td><td>No</td></tr><tr><td>Total Lines</td><td></td><td><p><strong>Total Lines</strong> allows you to enter multiple lines to sum. Input must be in one of the following three formats:</p><ul><li>Select Lines on this Report: <strong>100</strong>, <strong>110</strong>, <strong>120</strong>, <strong>130</strong></li><li>Select Lines from other reports: <strong>200:110</strong>, <strong>200:120</strong>, <strong>300:130</strong></li><li>Mixed: <strong>200:110</strong>, <strong>200:120</strong>, <strong>130</strong></li></ul></td><td>No</td></tr><tr><td>Comment</td><td>Note about Something</td><td>Internal comment for the line. Enter optional Alpha Numeric text here.</td><td>No</td></tr></tbody></table>

To import the report:

* Enter the report ID to be able to view the report later by ID.
* Enter the description of the report.
* Choose the report type as profit and loss or balance sheet.
* Enter the calculation sequence, if needed. (used if one report builds upon another) - can leave as zero or blank if not needed for your report.
* Choose the file to import from the desktop which user filled out according to the instructions above.

Click the icon test import file to resolve any errors in the file data before executing the import. You will receive the message indicating success or errors.

![](<../../../../.gitbook/assets/4 (55).png>)

Click OK to view the error details.

![](<../../../../.gitbook/assets/5 (71).png>)

Correct the error in the excel sheet and then save to the desktop. The error message specifies the line where the number is.

Save the file again, and then click the x to remove the file from the system import select field. Re-select the file to ensure that the fresh copy is loaded. Click test import again and observe the error resolved.

To view the report, user navigates to the Financial Report Setup screen and selects the report ID from the list. User must check the user name boxes for users who can view this report and saves settings.

User then navigates to the financial reports menu and can pull up the report ID from the list to view.
