# Naviga Plan Integration

## Configuration Options <a href="#_toc84344761" id="_toc84344761"></a>

Naviga Plan is now integrated with the advertising system digital first platform. Navigate to the menu Setup -> Admin -> Naviga Plan Integration.

This integration works in two parts. When enabled, print order lines in qualifying Status codes are moved into a queue file. The Windows Service monitors this queue file and sends these orders to Naviga Plan every few minutes (or however often it has been configured to run). Naviga Plan then reaches back into Naviga Ad to retrieve the Hi-Res final PDFs (\~/interfaces/material/hires/{materialId}).

This queue is also used to capture qualifying orders for other integration, such as Whiteboard. In these integrations, the queue is processed differently so that for example, the data is sent to a different place.

1. Click the button “**Enable Naviga Plan Integration**” to “Yes” to enable the integration process.
2. For the Naviga Plan end point path, please contact the helpdesk or your administrator. This is the path where Naviga Plan Integration is watching to bring orders into Plan.
3. Enter the recipient email’s address in the “**Email Sync Errors**” field so that this recipient would receive notification should there be errors resulting from the email sync.
4. The “**Order cut off days**” field looks at the issue date for any ads that are created or edited (which would normally trigger a sync with Plan), and it compares it with the cut-off settings to determine if it really should sync or not. If you create or edit a Campaign LINE, if the issue date is sooner than (today – cutoff), then that issue will not send to the queue to be sent to Plan. If the issue date is after (today – cutoff) then it will sync.\
   \
   If you sync the campaign, it will look to see if the campaign end date is after (today – cutoff days). If the campaign ends before today minus the cutoff, then it will not send to the sync queue.

{% hint style="info" %}
As an example, if you edit an order that ran last week, it generally wouldn’t be something that you would want to trigger a sync since it already ran. A zero in this field would sync anything with a future issue date. A 1 in this field would sync anything with an issue date of yesterday, but nothing older. If you put a negative in this field it will look at future dates. So -1 would be Today - (-1) or tomorrow. Do not put a negative in here unless you wouldn't want to sync orders for tomorrow's publishing date.

During testing it is often desirable to set this to a larger number so that you can plan and replan older dates for testing purposes. Once live, it would be unusual to have anything other than 0 here.
{% endhint %}

5. **Require Approval for hi-res final:** When checked to “Yes”, this field only hands back the hi-res final as requested (at our end point \~/interfaces/material/hires/{materialId}) if the Material is Approved. NOTE: For this rule to be enforced, you must setup [Material Approval Status](../../production-ad/overview-ad-production-and-material-status-workflow.md#\_toc113467268) codes, AND set at least one to mean “APPROVED.”
6. **Holdback Future Days:** This will hold ads in the queue if they are set in the future this many days. For example, put 30 in this field if you don't want to send ads to plan until 30 days before they are scheduled to run.\
   This setting was added for TownNews sites where TownNews purges materials based on how long they have been on their server (they are purged after 30 days). If the ad goes over to Town News too soon, it will purge before it ever even runs. So this setting will hold ads back until closer to publishing.
7. **Records per API Post:** This setting allows you to modulate the number of records sent per API POST Request.
8. **Seconds between API Post:** This setting allows you to throttle up or down the time between batches of records sent to the API. Please edit settings #7 & 8 only with consultation with Naviga Support and Implementation

## Status Code Mapping

In the “Status Code Mapping” section, check the boxes for the campaign status whose orders would be automatically sent to Naviga Plan. Click “Save” when finished. These can include all statuses defined in the AD module, such as orders that were deleted, invoiced or issue had been changed. Setting Confirmed thru Deleted statuses are most common. Some sites choose to also send R3 or earlier over. Only a Confirmed (or later) ad will actually get billed in Naviga Ad, so it is generally advisable to use caution sending ads to plan sooner than that.

## Other Naviga Ad items affecting Plan

### Product Configuration <a href="#_toc84344762" id="_toc84344762"></a>

To enable Naviga Plan for a product, navigate to the Setup menu -> Product Setup and choose a print product from the drop-down. Scroll to the bottom of the screen and click the box to “Send Orders to Naviga Plan” and change the box value to “Yes”. Save the settings. You will only see this setting, if the **Enable Naviga Plan Integration** flag is set in Naviga Plan Integration.

### Ad Type Configuration <a href="#_toc84344763" id="_toc84344763"></a>

User can set the order by Ad Type to automatically be sent to Naviga Plan by checking the respective Ad Type checkbox on the Setup -> Advertising Setup -> Ad Types.

![](<../../../../.gitbook/assets/1 (98).png>)

Leaving the box unchecked will prevent these orders from flowing into Naviga Plan. This is so that regular ads for Product ABC will go to Plan, but Inserts for the same product would not if that is desired.

### Print Product Color Configuration <a href="#_toc84344764" id="_toc84344764"></a>

Print products have color codes which can be setup and chosen on the order for materials which will also flow into Naviga Plan. The if a color ad is placed on a B\&W page, the Plan user will receive a warning.

Navigate to the menu Setup -> Advertising setup -> Print Color Setup.

![](<../../../../.gitbook/assets/2 (49).png>)

Add a color ID, description, and number of colors in that color ID and then click the + to add the color to the list, and then click Save at the bottom.

Currently, the Number is Colors is actually a code rather than a count. Full color ads should be set to 7. This is made up of Cyan (4) + Magenta (2) + Yellow (1). (4+2+1 = 7)

{% hint style="info" %}
Here are all the codes that can be used. You do not need to set all of them unless relevant to you.

0 = bw

1 = yellow

2 = magenta

3 = magenta + yellow

4 = cyan

5 = cyan + yellow

6 = cyan + magenta

7 = cyan + magenta + yellow = full colour
{% endhint %}

Navigate to create the campaign with a print product. In the line item full entry, note that the color field is available to choose from its values you have setup above.

Save the line and it will flow into the Naviga Plan application.

### Naviga Plan Queues <a href="#_toc84344765" id="_toc84344765"></a>

To view the Naviga Plan sync queue, navigate to the menu Campaigns -> Naviga Plan Integration -> Naviga Plan Sync Queue.

![](<../../../../.gitbook/assets/3 (67).png>)

Note that any orders you kill or delete in the system, will also be deleted from Naviga Plan if the integration is enabled. Note that when a campaign is cancelled, the system notifies Naviga Plan and records are updated accordingly.

To view the error queue, navigate to the menu Campaigns -> Naviga Plan Integration -> Naviga Plan Sync Error. The screen allows you to view any errors, reprocess them or delete records selected from the list.
