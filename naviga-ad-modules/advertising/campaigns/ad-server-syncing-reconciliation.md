# Ad Server Syncing / Reconciliation

<table data-view="cards"><thead><tr><th></th></tr></thead><tbody><tr><td><a href="ad-server-syncing-reconciliation.md#_toc105408230">Import Actuals from a File</a></td></tr><tr><td><a href="ad-server-syncing-reconciliation.md#_toc105408229">Reconcile Campaign Actuals</a></td></tr><tr><td><a href="ad-server-syncing-reconciliation.md#reconcile-engagements">Reconcile Engagements</a></td></tr><tr><td><a href="ad-server-syncing-reconciliation.md#_toc105408224">Ad Server Sync Queue</a></td></tr><tr><td><a href="ad-server-syncing-reconciliation.md#_toc105408225">Ad Server Actuals Sync Log</a></td></tr><tr><td><a href="ad-server-syncing-reconciliation.md#_toc105408226">Ad Server Sync Errors</a></td></tr><tr><td><a href="ad-server-syncing-reconciliation.md#_toc105408233">3rd Party Server Queue</a></td></tr></tbody></table>

## Import Actuals from a File <a href="#_toc105408230" id="_toc105408230"></a>

User can import actuals in bulk from a file. Naviga Ad supplies a template which user must populate to apply the accurate numbers to the respective campaigns.

Navigate to the menu Campaigns -> Import actuals from a file.

Click the button download import template in the bottom left of the screen. Populate the template with the data.

The spreadsheet contains columns to be filled with the accurate data from the system.

Save the file to your hard drive. Then navigate back to the import screen. Click the select button then browse and click the spreadsheet you saved.

Click the button check data from file. This is very beneficial in displaying issues in the spreadsheet before importing. The issue displays on the screen with an explanation of the reason for the error under the section items cannot be imported.

To correct the issue, fix the spreadsheet. Click the remove button for the existing file and re-upload.

Then click again the check data from file. The item now moves up to the section labeled items that can be imported.

![](<../../../.gitbook/assets/16 (3).png>)

Check the box for the items to apply the actuals to the campaign line.

<figure><img src="../../../.gitbook/assets/image (272).png" alt=""><figcaption></figcaption></figure>

In the pop up box, click the button drop down menu apply imported numbers to and choose the applicable item. Click on yes or no to apply to Actuals. If yes is selected, you will be further prompted with additional questions to Adjust future estimates and/or to Ignore 3rd Party rules.

<figure><img src="../../../.gitbook/assets/image (214).png" alt=""><figcaption></figcaption></figure>

Click the save button.

Navigate to the campaign edit screen for the campaign to which you imported the actuals and click the option “Display serving details” to view the serving percentage delivered and the actual amounts equaling the amount in the spreadsheet.

<figure><img src="../../../.gitbook/assets/image (486).png" alt=""><figcaption></figcaption></figure>

User is now ready for billing as the campaign has the actuals amounts applied.

## Reconcile Campaign Actuals <a href="#_toc105408229" id="_toc105408229"></a>

1. Navigate to the menu Campaigns -> Reconcile Campaign Actuals. Choose the campaign type, the Product group and date range for which to enter actuals.
2.  Click the button get campaigns. The list of campaigns awaiting actuals displays.\\

    <figure><img src="../../../.gitbook/assets/image (1063).png" alt=""><figcaption></figcaption></figure>
3. User can click the button apply quantity served. This will apply the estimates to the actuals, copying the amount in est., amount column to the actual amount column and the est., qty., column to the actual qty., column. This is performed for all campaigns listed. Once user saves actuals, the data can only be changed manually. When user clicks the save actuals after applying quantity served, user will receive the message prompting them to adjust the estimates to match the actuals. This will automatically adjust the estimates on lines with a future date to this same amount to be a realistic reflection of what’s to be expected as estimates. This could be useful to give user a realistic estimate rather than a mere guess. User can choose not to do so.
4. If user would like to apply quantity served to individual campaign lines, user clicks the bow icon under the apply column per campaign line item.
5. Note the column labeled "Reconcile to" will indicate if the actual qty will be taken from the Estimates, from the Actuals of it it will use 3rd party actuals.
6. Note that a flat fee ad type will automatically apply the fee to the actual amount in this list since it is a flat fee and not based on the number of impressions or clicks.
7. The column cap actuals, if checked in the Advertiser Maintenance Setup screen or the Brand Maintenance as an override of account setup, provides a cap for the number of impressions and clicks which once reached, will be the maximum amount paid by user. For example, if the user wants to cap the amount paid to a certain dollar amount, user can do this and not pay additional amounts even if more impressions and clicks have been achieved. This is a protection measure to not exceed a certain dollar amount the user would pay for services.
8. The filter exclude lines w/o external ID will exclude which do not have external IDs entered in the campaign header or the line item entry screens.
9.  For run of network campaigns, user can click the Edit hyperlink on the list, and manage the individual estimates for the digital products forming the run of network.

    <figure><img src="../../../.gitbook/assets/image (976).png" alt=""><figcaption></figcaption></figure>

## Reconcile Engagements

For Digital and e-newsletters, you can setup [Social Engagement Codes](../setup/advertising-setup/engagement-codes.md). These are setup prior to this step in the Setup -> Advertising Setup menu. Social Media Engagement Codes are available to be tied to track and gather metrics related to digital orders such as those placed on social media sites or e-newsletters. The codes are tied to product setup and any given product can track up to ten metrics.

In this example the product is an eNewsletter and the desire is to track Open and Forwards. This tracking would be done externally, but this screen allows you to update the campaigns with the actual engagement records. This can be compared in reporting to a goal set on the campaign at the time of order entry.

<figure><img src="../../../.gitbook/assets/image (674).png" alt=""><figcaption></figcaption></figure>

## Ad Server Sync Queue <a href="#_toc105408224" id="_toc105408224"></a>

This menu allows user and administrators to view the status, time intervals, last write to and retrieval from GAM and Naviga Ad. If there is a campaign in the queue waiting to be sent to GAM, it will be listed in the queue.

Navigate to menu Campaigns -> AD Server Sync Queue.

<figure><img src="../../../.gitbook/assets/image (1347).png" alt=""><figcaption></figcaption></figure>

The line service interval is the number of minutes between every read by GAM of the campaign lines in the Ad system. In this case, every 5 minutes, GAM reads the lines from Ad and serves them.

The actuals service interval is the number of minutes where GAM counts the actual impressions and clicks and sends them back to the AD system as actuals, in this case every 30 minutes.

The last writes and last retrievals fields provide the exact date and time when these services were done by GAM.

The Connected Ad sever tab will show the Ad Servers that are connected and Active

<figure><img src="../../../.gitbook/assets/image (1619).png" alt=""><figcaption></figcaption></figure>

## Ad Server Sync Log <a href="#_toc105408225" id="_toc105408225"></a>

This screen provides a history log of the write and retrieval by date, time and number of items the services were performed and can be found in the menu Campaigns. This data will be quite long and will take up multiple pages. User can navigate using the navigational arrows on the bottom of the screen to see past history. How many days worth of data gets displayed here is dependent upon how often you sync. This log will show up to 5 pages

The data can also be exported to Excel or pdf using the icons on the top right of the data table.

<figure><img src="../../../.gitbook/assets/image (1489).png" alt=""><figcaption></figcaption></figure>

## Ad Server Sync Errors <a href="#_toc105408226" id="_toc105408226"></a>

User can view the errors in the synchronization between GAM and Naviga AD by navigating the menu Campaigns -> Ad Server Sync Errors.

<figure><img src="../../../.gitbook/assets/image (1473).png" alt=""><figcaption></figcaption></figure>

There are campaign lines hyperlinks to direct the user to the campaign itself to investigate the error in the entry. There could be a missing production controller or sales rep which is not setup in Google accurately, or there could be an ad type which is not mapped to a GAM ad type and cost line item.

The error message is an indicator to administrators of the error source.

If the error is on the Naviga Ad side, correcting and resaving the line will put the line back into the Queue to re-sync the ad. The error in the Queue can be then ignored or deleted if it subsequently was re-processed successfully. If the ad was on the GAM side, after the correction is made one or several lines in this list can be selected and Re-processed with a click on "Reprocess Selected Records" at the bottom of the page.

## 3rd Party Server Queue <a href="#_toc105408233" id="_toc105408233"></a>

{% hint style="info" %}
This feature will take some coordination with Naviga Programming. Consult with your Implementation Specialist or Naviga Support to get this setup.
{% endhint %}

User is to setup the 3rd party to email daily reports that include a 3rd party ID (first column in grid) and the clicks and impressions to a Gmail address. In the background on a schedule the system is monitoring this Gmail inbox for emails from a specific email address. This screen allows for the user to match those lines to line IDs in the AD system, which will then save those 3rd party actuals so they can be viewed on the campaign lines screen.

<figure><img src="../../../.gitbook/assets/image (1053).png" alt=""><figcaption></figcaption></figure>

These are the objects and fields that we are either setting or updating. Not all of them are set every time as many depend on what settings you have in the system and what things are on each order/line.
