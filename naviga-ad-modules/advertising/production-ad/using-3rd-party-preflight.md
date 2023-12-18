---
description: >-
  Asura and Twist are supported in this workflow.  Other Preflight systems can
  be used with Interface Link, but don't follow this specific workflow since
  Interface Link integrations are custom per site.
---

# Using 3rd Party Preflight

## Preflight Overview

The following scenarios are points where integrations with Preflight may be invoked.

1. Finished artwork is uploaded by the customer via the portal
2. Finished artwork is manually added to the Material record and flagged as ready for Preflight
3. Finished artwork is uploaded from the Production by Print Product dashboard
4. Artwork is finished by an artist using Naviga Ad InDesign Extension and Preflight option is set to yes in Product Setup -> Material Handling

The result of uploading artwork into the Preflight workflow is that the file is dropped into an FTP folder that the 3rd party preflight software is monitoring

* Naviga Ad then monitors an out folder – also via FTP
* Typically, the preflight software provides Naviga Ad the file that was submitted plus an XML file that indicates if the image passed the preflight. With some 3rd parties, we also receive a JPG preview and SWOP proof (crop marks jpg for the client). The naming of the jpg preview must be xxx\_thumbnail.jpg where xxx is the material ID.
* The information in the XML that is sent back, allows Naviga Ad to move the artwork forward in the workflow process by mapping the responses in the XML to production statuses in Naviga Ad.
* Naviga Ad users can monitor the progress on the Material Trafficking screen. This dashboard identifies preflight exceptions. This essentially means monitoring this report for errors, reviewing them and resubmitting corrections via the Material screen.

The first half of this document will review each of these scenarios. The last half will explain the settings and setups needed to integrate to 3rd party Preflight software.

## Scenario 1: Finished artwork is uploaded by the customer via the portal

In this example, the customer, Home Depot, has logged into the Customer Portal and clicked on the Print Advertising Orders option. They are then presented with a list of their Upcoming Print Ads. The bottom line in this grid shows an order that does not have artwork attached.

![](<../../../.gitbook/assets/1 (104).png>)

The user clicks Manage this Order to access the window where they can upload a print file.

They are able to upload the image file, create an Ad Headline, Description and type in Production Notes

![](<../../../.gitbook/assets/2 (94).png>)

On the Portal, the status changes to show the images is Processing through the Preflight software.

![](<../../../.gitbook/assets/3 (90).png>)

If an internal user of Naviga Ad, looks at the Material Record for the Line Item on this campaign, they can see that material has been uploaded and is being processed by the Preflight software.

![](<../../../.gitbook/assets/4 (81).png>)

## Scenario 2: Finished artwork is manually added to the Material record and flagged as ready for Preflight

The below screenshot is a section from the Material record:

![](<../../../.gitbook/assets/5 (74).png>)

The user clicks the Upload New File for Preflight to select the finished artwork that he wants submitted. Saving the changes on the Material record will trigger the artwork file to be moved to the FTP site that the Preflight software is monitoring.

## Scenario 3: Finished artwork is uploaded from the Production by Print Product dashboard

![](<../../../.gitbook/assets/6 (67).png>)

If the use selects a product and date range from today or a future date, if there is no material ID currently assigned to the order line, the Material ID column can include a button to upload the finished artwork for preflight. The following screen opens after clicking "upload":

![](<../../../.gitbook/assets/7 (56).png>)

The user can identify characteristics about the material including a flag for Bleed, Coupon or if they will supply a proof with crop marks.

{% hint style="info" %}
Note: There is a system level setting that has to be flagged by naviga personnel to allow the upload button to be shown onscreen. Contact support or your implementation specialist if you would like to use this feature and aren't seeing it.

Also note: if the line is past the due date, you will no longer see the Upload/Pickup buttons.
{% endhint %}

## Scenario 4: Artwork is finished by an artist using Naviga Ad InDesign Extension and Preflight option is set to yes

1. Navigate to Product Setup -> Material Handling node. Scroll to the bottom and set Preflight on Complete=Yes is you wish to send material to preflight.

<figure><img src="../../../.gitbook/assets/image (1688).png" alt=""><figcaption></figcaption></figure>

2. When InDesign user completes the material and the system uploads the finals (INDD file, jpg preview and pdf), it attaches them as components, but does not mark a hi res final or JPG preview. It takes the PDF and drops it into the preflight FTP folder. From here – if it passes preflight you will get your hires final and preview from that process – if it fails, someone will have to do something manually

## Material Trafficking

Regardless of what scenario above is in use, the Material Trafficking Dashboard (Advertising module, Production -> Material Trafficking) allows a user to see all Campaigns that have materials being processed or approved via Preflight software.

The folder monitor tab shows the progress of preflight items from Naviga Ad to the In Folder on the ftp site to the Out folder on the ftp site

![](<../../../.gitbook/assets/9 (40).png>)

The Materials Tab shows the items that have been processed through preflight

![](<../../../.gitbook/assets/10 (37).png>)

The Material record is updated once a response is received from the Preflight software. The preview (if provided) will be displayed in the preview image area at the top right of the material record. The XML file can be downloaded from the "Preflighted XML File" box below.

<figure><img src="../../../.gitbook/assets/image (1685).png" alt=""><figcaption></figcaption></figure>

If the Material is Accepted, it is moved to the Component area of the Material Record; the Preview file is created; and the Hi-Res file is marked. This is the PDF that will be passed to Naviga Plan for pagination.

![](<../../../.gitbook/assets/12 (27).png>)

## Preflight Integration Setups for Naviga Ad

1.  Setup -> Admin -> Preflight Integration\\

    <figure><img src="../../../.gitbook/assets/image (1686).png" alt=""><figcaption></figcaption></figure>
2. Material Upload Configuration Settings - enter your ftp connection settings below - Ftp, Ftps, and Sftp protocols are supported.

<figure><img src="../../../.gitbook/assets/image (1687).png" alt=""><figcaption></figcaption></figure>

3. Product Setup -> Material Handling -> Preflight/Production Workflow Integration

![](<../../../.gitbook/assets/16 (20).png>)

Site needs to define the Workflow status settings that correspond to the settings coming back from the Preflight system.

The third dropdown in the Material Approval Integration section below will only be displayed if the Preflight Integration in the admin setup area is set to preflight w/o Twist or Asura, or in other words a manual preflight. If using Twist or Asura, the material will be set as "Processing" upon upload and will be automatically updated once complete.

![](<../../../.gitbook/assets/17 (20).png>)

{% hint style="info" %}
For Naviga Personnel - See Internal Documentation page for the Admin settings you will need to set for your customers to be able to use preflighting.
{% endhint %}
