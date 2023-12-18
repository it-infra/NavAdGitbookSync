# Working in the InDesign Extension

**These are the bare essentials for setting up Naviga Ad to send ads to InDesign. Please also see "**[**Overview - Ad Production & Material Status Workflow**](overview-ad-production-and-material-status-workflow.md)**" for more in depth discussion around how all these settings work together, including a demo video.**

{% hint style="info" %}
NOTE: Extensions didn't exist in Creative Suite, so this will only be able to be used with Creative Cloud (CC) versions of InDesign.\
See Naviga Support or Implementation Specialist for the Installation files for InDesign Extension. A license is required to use this feature.
{% endhint %}

## **IN NAVIGA AD (Admin User):**

### **Setup / Background Config needed**

[**Production Statuses**](../setup/production-workflow-setup.md)

* Master Stages
* Production Workflow Stages (Product-level)

[**Product Deadlines**](../setup/product-setup/)

* Rules are set on the product here:

![](<../../../.gitbook/assets/1 (40).png>)

Ideally, the Defaults should be set on the product BEFORE creating the issue dates, otherwise you will end up with nulls on the deadline and then they will need to be manually set on the Issue Configuration.

**Sizes**

* Modular Sizes must have a size in Width and Depth defined
* Non-Modular Size must have column layout maintenance complete and linked to Product and/or Sections (for ROP) and Categories for Classified.

**Material Approval Templates**

* When an artist marks a material project as being completed, the system will alert either a sales rep or production controller (or both) that it is done and ready for proofing. This HTML template must be set up before and linked to the product.
* SAMPLE HTML (replace XXX with your 3-character site code):

{% code overflow="wrap" lineNumbers="true" %}
```
<p><span style="font-size: 14px;">Hi there.&nbsp; We have built an ad for #ADVERTISERNAME# that we think is really great.&nbsp; Please review and send to them for approval if you agree! &nbsp;</span></p>
<div style="width:100%;box-sizing: border-box; padding: 10px; background-color: #f1f1f1;"><span style="font-size: 14px;"> #APPROVALCOMMENT# </span></div>
<span style="font-size: 14px;">
<br />
<br />
<img alt="" src="#PREVIEWIMAGEURL#" style="max-width: 400px; max-height: 400px;" />
<br />
If you are having trouble viewing the above image, you may click <a href="#PREVIEWIMAGEURL#">here </a>to view in a browser window.
<br />
<br />
Click<a href="https://XXXtest.navigahub.com/EW/XXX/ad/pw/material.aspx?ID=#MATERIALID#"> here </a> to review this material. If you approve, please mark the Approval Status to Pending Customer Approval or Customer Approved if you do not wish to send to the customer.</span>
<p>&nbsp;</p>
```
{% endcode %}

**Product Setup**

**Material Handling (Product Setup, Material Handling node)**

* Set rule for what Production Status gets set when the artist marks a material as complete.
* Template defined above is linked here
* Who gets the email is set up here
* Whether or not to preflight on output is flagged here.
  * if set to YES and if you have preflight setup – when you upload the finals, it attaches them as components, but does not mark a hi res final or JPG preview. It takes the PDF and drops it into the preflight FTP folder. From here – if it passes preflight you should get your hires final and preview from that process – if it fails, someone will have to do something manually

**Default Artist (Optional)**

* If desired, on the product setup screen you can set a default artist for that product

**Artist Setup**

* Name, email address and phone for the artist.
* Optionally can add a product group
  * Product group, if defined, will filter the queue for the artist to only show that product group. Product Groups can be multi-select.
  * If left blank, the artist will see materials for ALL product groups

**Artist workflow Status**

* At least one of these should be marked as “complete”
* When the artist selects “complete” in Indesign, the INDD file, jpg Preview and the high-res PDF will automatically upload into the system and the material will be removed from the artist worklist

**Material Approval Setup**

* If desired, can only send “approved” materials over to plan
* “Allow Approval” will display the material in the Portal for the Client to approve it online.

## **End User in Naviga Ad:**

### **Order Elements needed for Material to Come into InDesign:**

**Material & Material Status**

{% hint style="success" %}
* On the line item of the campaign, the material must be linked
* There must be a size (either modular or columns x depth)
* The first run date that the material is to be used must be in the future
* The Material Status on the line must be a Production Status that is flagged as Internal Artist Required in the background.
* Inside the material itself, the Artwork Production Status must be set to a status that is NOT flagged internally as ‘completed.” Optionally, an artist can be assigned (or artists can pull from an unassigned queue)
{% endhint %}

**Working with Components on the Material record**

**Local components** are to be used with the material attached to the campaign. These components may be copied and used in a new ad for Pickups with Change

**Global components** are those components that may be used many times. Company logos, pictures, specific branding, etc. These components can be tied to a customer OR they can just be linked as an overall global component and tagged into categories for easy searching.

Local Components can currently only be added in Naviga Ad in material maintenance or on a campaign itself.

!\[Graphical user interface, application

Description automatically generated]\(<../../../.gitbook/assets/2 (47).png>)

If an artist needs to EDIT a local component that was received, they may work on that component locally and use the edited image, however, we only store the embedded artwork in the INDD file. We do not store the links. If the INDD file does get copied to be use again, it will have the embedded image that was edited.

Global components can be edited and then the file can be replaced via the InDesign Extension Window. (This was new in version 2022.3)

## **IN INDESIGN:**

### **Installing the Extension InDesign**

1. The extension Zip file will be given to you by your implementation specialist
2. Close InDesign
3. Unzip and place the entire NavigaAd folder in the location below
   1. PC (x64): C:\Program Files\Common Files\Adobe\CEP\extensions
   2. PC (x86): C:\Program Files (x86)\Common Files\Adobe\CEP\extensions
   3. MAC: /Library/Application Support/Adobe/CEP/extensions
4. Re-Open Indesign
5. Open the Extension from Window > Extensions > Naviga Ad Extensions

### **Logging into the Extension in InDesign:**

| API Connection Path          | https://XXXtest.navigahub.com/ElanWebPlatform/XXX           |
| ---------------------------- | ----------------------------------------------------------- |
| API Connection Key           | This will be given to you by your implementation specialist |
| Instance Path                | https://XXXtest.navigahub.com/ew/XXX                        |
| Local Storage Path (PC)      | \~/desktop/NavigaAd\_INDD                                   |
| Local Storage Path (Mac)\*\* | \~/NavigaAd\_INDD                                           |

\*\*Newer Mac OS versions are fussy about applications putting stuff on the desktop, so best to just avoid that issue

It is really important to fill in **all** the above fields on the login screen

XXX should be replaced with YOUR 3-character site code

Remove the “test” from the URLs to point to the live database

Keep the above settings handy. When changes happen to the API, you may be logged out of the extension, and it will require you to fill in those settings again. Beginning with the 2021.3 Naviga Ad Release, you can save a json credentials file to connect rather than filling in the above details manually. Here is a sample json file. Open in a text editor and change the settings to your site-specific and user specific credentials. Save the file with .json file extension.

```
{
  "ArtistId": "artist@email.com",
  "PromptOnFileDrop": false,
  "ApiConnectionPath": "https://xxx.navigahub.com/elanwebplatform/xxx",
  "ApiKey": "NCSElan123",
  "InstancePath": "https://xxx.navigahub.com/ew/xxx",
  "LocalStoragePath": "~/indesignfiles",
  "HighlightColor": "#1B4F72"
}
```

### **INDD Worklist**

**There are two sections in the worklist - "My Creative Projects" and "Unassigned Creatives Projects" - The top section will only be visible to the artist to whom the material is assigned.**\\

<figure><img src="../../../.gitbook/assets/image (1698).png" alt=""><figcaption></figcaption></figure>

Worklist auto sorts in order of items that need to be completed based on the product issue deadlines. (Note: if you didn't setup your product deadlines before creating your issue dates, you might need to go into Issue Configuration in Product Setup to update the config)

Clicking **View** allows the Artist to see what information is available to build the material

![](<../../../.gitbook/assets/4 (80).png>)

* If it was opened from the Unassigned Queue, the artist can then Assign the Material to themselves. Once assigned to them, the material project can be worked.
* Change the artwork status
* Open/Create the InDesign File

### **Artwork Status in InDesign**

This is how the artist can communicate back to the end users in Naviga Ad.

![](<../../../.gitbook/assets/6 (43).png>)

* Workflow statuses flagged with “complete” in Setup will Complete the ad and release it from the artists Worklist

![](<../../../.gitbook/assets/7 (38).png>)

{% hint style="info" %}
_Marking as complete should only be done when the file is ready to be released as the Artist has limited ability to retrieve it once it has been released from the extension (They can use the look-up function on the top of the worklist, but only if they know the material ID). To use other search options, the user would have to go back to Naviga Ad to search and un-complete the ad._
{% endhint %}

### **Artwork Workflow**

* **Open/Create InDesign File / Download/Create InDesign File** is what the Artist should do to start working on the ad
  * If it is a new build this will create the InDesign document
  * If this is a pickup with change this will download the indd file (must be named for the material id).
  * If the artist already started working on it and it coming back to it, it will open the local copy if it is still there. If the artist uploaded the local copy to the server when he stopped working on it, it will download the server copy
* **Get Latest from Server** is for any InDesign file that may have already been started by another Artist
* **Save Copy of InDesign File to Server** is when the artist is done working on the material, but it is not completed.
* **Release this Project** releases everything, the Artist is unassigned – this could be because the artist cannot complete the file or another reason. Be mindful of the options to upload/delete.

![](<../../../.gitbook/assets/9 (1) (1).png>)

* **Log Time** - If managers wish to understand time spent on materials, they can do so in the [Artwork Time Spent Report](managing-materials.md#artwork-time-spent-report). The artist will need to click the button to Log Time here:\
  ![](<../../../.gitbook/assets/image (1673).png>)\
  A screen will pop up with the time that the material has been opened in the current session.\
  ![](<../../../.gitbook/assets/image (1674).png>)\
  Artist can make edits to the time and add comments prior to clicking the submit button.

## **Troubleshooting**

**(Generally this is not needed….but have seen it occasionally)**

When logging in, if not all the fields get filled out or filled out correctly, the information does get cached and may need to be cleared.

This is the error (or similar)

!\[Graphical user interface, text, application

Description automatically generated]\(<../../../.gitbook/assets/10 (18).png>)

May also see an error not related to logging in incorrectly, but if you see an “oh snap” error message when uploading artwork, clearing the CEP Cache below can also sometimes resolve that issue.

**Clear the CEP Cache**

To clear the CEP Cache (the InDesign Extension Cache) and then restart InDesign:

**MAC**

* Close INDD
* Select the Finder menu > Go > Go To Folder
* Paste \~/Library/Caches/CSXS/cep\_cache/
* Move the cep\_cache to the desktop (can delete later)
* Re-Launch INDD

**PC**

* Close INDD
* Locate this folder
  * C:\Users\\\[youruser]\AppData\Local\Temp\CEP\_CACHE
* Move the whole cep\_cache folder to your desktop (you may need permissions), can delete it from there later.
* Re-Launch INDD

**Are you a TownNews site?**

If so, do not be logged into TownNews when working on ad design. TownNews plugin interrupts the upload/complete artwork process.
