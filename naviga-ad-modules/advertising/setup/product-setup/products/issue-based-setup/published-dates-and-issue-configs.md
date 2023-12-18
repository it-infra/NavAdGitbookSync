# Published Dates and Issue Configs

## Published Dates

Navigate to Setup -> Product Setup -> Published Dates. Select a print publication or issue-based digital product from the product drop-down. Also select if you wish to select the dates in order entry by a dropdown list of dates (common for magazines) or by a calendar (common for a daily publication)

Click on each calendar date which applies to this publication.

You can also use the “Auto Select Issues” for a faster choice of dates, especially if this is a daily or weekly publication. Choose the start and end dates, as well as the specific days of the week. When finished, click “Apply” and save the details by clicking on the “Save” button. ![](<../../../../../../.gitbook/assets/image (647).png>)

Note also that some dates are greyed out and not available for selection if you attached a holiday calendar to them in the Product Details node.

Once you have booked orders to a date, the date will also be grayed out and you won't be able to deselect it. If you create an issue, book orders for it, and decise to move the issue to another date, use the procedure to [Change Issue Date/Period](../../../../campaigns/managing-campaigns/change-issue-date-period.md).

## Issue Configuration

This node allows you to setup each issue for the product.

Choose the product from the drop-down menu and choose the start date for viewing the config for the publication or e-newsletter. You can make changes in bulk to the issues by using the drop-down field of “Bulk Update Options”. This allows you to enter the financial period, issue description, closing date, comparison issues and budgets for each issue to be standardized and filled in mass. Save the settings after all the bulk changes. Note that any times such as close time is the server time zone and not your time zone as a user.

<figure><img src="../../../../../../.gitbook/assets/image (1015).png" alt=""><figcaption></figcaption></figure>

If you have set up your product already, the issue close date and the material due date will be filled in automatically when you create the Published Dates in the previous step. If you did not already set up your default deadline before creating issues, you can still add them manually or in bulk here.

The comparison issue is optional, but is helpful if you would like to see comparison information on the Publication analysis report. Financial period is required before saving this config.

## Issue Import

This node allows you to import issues in bulk for a publication or an issue-based digital product.

To do so, navigate to the menu Setup -> Product Setup -> Issue Import node.

<figure><img src="../../../../../../.gitbook/assets/image (482).png" alt=""><figcaption></figcaption></figure>

Click the button “Download Template” which opens a spreadsheet template on your desktop with various fields to fill out.

Alternatively, if the goal is to update an existing set of issues, instead of downloading a blank template, navigate to the Issue Export below the Issue Import and Export existing issues to modify and re-import.

### Issue Import Template <a href="#_toc9433602" id="_toc9433602"></a>

The fields are:

| **Field Name**            | **Example of Data** | **Source of Data and Restrictions**                                                                                       | **Mandatory/ Optional** |
| ------------------------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------- | ----------------------- |
| **Product ID**            | VisitMont           | Must match the product ID in Naviga Ad                                                                                    | Mandatory               |
| **Issue Description**     | March Issue         | The description is free form alphanumeric text                                                                            | Optional                |
| **Issue Date**            | 03/02/2019          | MM/DD/YYYY is the date when the issue is being published                                                                  | Mandatory               |
| **Close Date**            | 03/01/2019          | MM/DD/YYYY is the date when no changes can be made to the issue                                                           | Mandatory               |
| **Financial Period**      | 2019-03             | YYYY-MM is the financial period which must match the one in Naviga Ad and to which this issue is tied.                    | Mandatory               |
| **Budget Pages**          | 30                  | Numeric free form entry of the number of pages in the budget.                                                             | Optional                |
| **Budget Revenue**        | 3000                | Numeric free form of the budget revenue for this issue.                                                                   | Optional                |
| **Comparison Issue Date** | 01/31/2019          | MM/DD/YYYY issue to the prior year issue for comparison in reports.                                                       | Optional                |
| External ID               | 123                 | Alphanumeric ID Unique to this issue. Used as needed for API integrations                                                 | Optional                |
| Close Time                | 16:00 or 4:00 PM    | Text field on the import. Enter in military time or be sure to include PM for afternoon times. 4:00 will come in as 4 AM. | Optional                |
| Material Due Date         | 03/01/2019          | MM/DD/YYYY is the date when materials are due                                                                             | Optional                |
| Digital Edition URL       | https://abc.com     | URL for the e-edition                                                                                                     | Optional                |

{% hint style="info" %}
NOTE on the Close Time - Do not re-use a template that you had from prior releases, or copy and paste these values in from a prior test. The cell formatting is important here so be careful not to paste in formatting from another source.
{% endhint %}

### Import Issues <a href="#_toc9433603" id="_toc9433603"></a>

Fill in one rows per issue in the template and save to your desktop.

<figure><img src="../../../../../../.gitbook/assets/image (1205).png" alt=""><figcaption></figcaption></figure>

On the import page, click on the button “Select” and browse for the template saved on your desktop.

If updating existing issues, set the Overwrite Existing to Yes

On the Import page in Naviga Ad, click the button “Test Import File”. This step is important in clearing out all errors in the import before the import takes place.

![](<../../../../../../.gitbook/assets/4 (51).png>)

Click the OK and read the error messages which the system provides so you can return to the template and make the necessary changes. Re-save the template to the desktop; remove the existing uploaded file by clicking on the import page on the x remove button. Reload the correct template and test it again. Repeat the uploading and testing process till all the errors are gone and the system gives a success message.

![](<../../../../../../.gitbook/assets/5 (65).png>)

Click on the “Import File” button on the import page. Click OK and the system imports the issues.

Click on the node “Issue Configuration” and choose the product from the drop-down menu. Note that the new issues with all the details have been imported to the product and are now ready for use in campaign entry.

<figure><img src="../../../../../../.gitbook/assets/image (1605).png" alt=""><figcaption></figcaption></figure>

## Export Issues

To Export Existing Issue configuration data, navigate to Issue Export in Product Setup

<figure><img src="../../../../../../.gitbook/assets/image (371).png" alt=""><figcaption></figcaption></figure>

To Export the configuration,

1. Select to export a single product, or a Product Group
2. Select the Product or Product Group to export
3. Select the Date Range to Export
4. Click the export button
5. This will download an excel spreadsheet to your downloads folder which can be opened and modified as needed.
6. The downloaded spreadsheet will be in the format needed to then upload via the [Issue Import](published-dates-and-issue-configs.md#issue-import) process. If exporting with the intention of updating issue coniguration details (for example budget data that might come later), be sure to select "Overwrite Existing" in the Issue Import process.
