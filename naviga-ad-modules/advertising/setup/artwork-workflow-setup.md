# Artwork Workflow Setup

## Artwork Production Workflow Setup <a href="#_toc113467267" id="_toc113467267"></a>

Also See [Overview Ad Production](../production-ad/overview-ad-production-and-material-status-workflow.md)

Artwork Status is only relevant when you are using the Naviga InDesign Extension for material creation. This is the status that an artist will select in the InDesign workflow

![](<../../../.gitbook/assets/2 (18).png>)

To create a status, enter an ID and a description and click the + to add to the list. Save when complete.

Some definitions of the extra columns here:

* Completed - Any status that has a completed flag, when selected in InDesign, will produce a final PDF (or PNG if digital), a jpg preview, and also an indd document, all of which will upload to the server and will clear the item from the artists workflow queue.
* When Completed from InDesign, clear artist assignment - by default, once an artist as assigned, they won't be unassigned unless the artist, or someone internally, releases the project. That means, if a client doesn't approve the ad in the portal and sends it back for re-work, it will pop back into the artists queue for revision. For one of our clients that wasn't desirable and they wanted it to go back to the unassigned queue for any available artist to take care of. So this flag will accomodate that workflow.
* Suppress emails - This is only selectable for completed statuses. If selected, the usual emails that fire off indicating that the material has been completed will not be sent. This might be desirable in the case of a quick fix where the client doesn't need another email. You wouldn't likely want this on all of your completed items, but perhaps a second status for complete where it was complete w/o email.
* Hidden from Artist's InDesign Queue - when selected, this item will not be displayed in the artists queue. Use case for this was that it would be used in the case where an artist was waiting for some feedback. Use caution with this one - the user providing the additional details will need to be to also remember to change the artwork status upon providing the info or else the artist might not realize that the feedback has been given since it wouldn't be in their queue anymore.
* Color selection - This is used to display the materials with a color code in the [Artwork Production Mgmt Report](../production-ad/managing-materials.md#artwork-production-management)

## Artist Setup

Navigate to Setup -> Artwork Workflow Setup -> Artist setup to create the artists who will log into InDesign to design ads.

<figure><img src="../../../.gitbook/assets/image (373).png" alt=""><figcaption></figcaption></figure>

Enter their Full Name, email, and Phone Number. (email will be what they use to login)

If this artist will only be allowed to access certain Product Groups, select one or more Product Groups in this list. Leave blank if they can see all Product Groups.

Select the checkbox for Inactive if the artist will no longer be used.

Save your changes.
