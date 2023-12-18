# Overview - Ad Production & Material Status Workflow

## Material Workflows and Statuses <a href="#_toc113467264" id="_toc113467264"></a>

The world of material workflows and updating statuses can be quite complex, especially with some of our clients using our InDesign Extension, some using 3rd party ad tracking systems and others simply chasing materials and not doing much in house design at all. This document aims to make clear how to set up the system so that Production Statuses, Artwork Statuses and Approval Statuses all work together.

Here is a video overview of production workflow as well from one of our User Conferences. This video also shows a little of how materials work with Plan.

{% embed url="https://dev.navigahub.com/mothership/resources/videos/NavigaAdProductionWorkflow.mp4" %}

## First, some definitions <a href="#_toc113467265" id="_toc113467265"></a>

### Production Status <a href="#_toc113467266" id="_toc113467266"></a>

This is linked to the product and to each issue date on an order line. It is setup in Setup > Production Workflow Setup. Production workflows can be different per product, and you can copy from one Product to another.

![](<../../../.gitbook/assets/1 (6).png>)

### Artwork Status <a href="#_toc113467267" id="_toc113467267"></a>

This is linked to the Material itself and is what the ARTIST selects in InDesign. It is setup under Setup > Artwork Workflow Setup > Artwork Production Workflow Setup. This is defined once for the system, so it is shared by all products. Artwork Status is only relevant when you are using the Naviga InDesign Extension for material creation.

![](<../../../.gitbook/assets/2 (18).png>)

### Approval Status <a href="#_toc113467268" id="_toc113467268"></a>

Also linked to the Material but can be auto-selected based on what Production Workflow Status is selected. Can trigger a material to be available in the Portal for a customer to approve (Allow Approval flag) and can also trigger whether the material should be available in Plan, if desired (Approved Flag). This is setup under Setup > Material Approval Setup.

![](<../../../.gitbook/assets/3 (30).png>)

Now let’s talk about how these all get used in the system. In the system configuration there are a few places where these different settings can be selected.

First off, let us discuss the **Material Handling on the Product Setup**. There are two sections on this page that are relevant to this discussion:

![](<../../../.gitbook/assets/4 (78).png>)

In the Engage Portal / Material Approval settings, you can select the product-specific **Production Status** that gets selected when a material is approved or rejected.

In the Artist Workflow Integration section, there is also a **Production Status** that can be selected there which indicates what should happen to the Production Status when a material for this product is completed by an artist in InDesign.

![](<../../../.gitbook/assets/5 (9).png>)

Linked to these Production Statuses in the Production Status setup is an **Approval Status**. This tells the system, when I change a Production Status on this product, what should the associated material approval status. These approval statuses here are used by InDesign, Order Entry, and by the Print Production Report. If using the Portal for material management, Approval settings used by Portal are configured in Portal Setup.

![](<../../../.gitbook/assets/6 (3).png>)

If you are using the Portal for material management. There are just a couple of fields to configure there. The following screen can be found about halfway down the page on the _Setup > Admin > Portal Setup > Portal Setup screen._

![](<../../../.gitbook/assets/7 (53).png>)

The Status on approval and status on rejected are for the Approval Status that you would like selected when the client approves the ad in the portal.

_Note: Items #2 and #3 are redundant to what we now can do with the Production Workflow setup. In a future release we will be able to remove these two and just follow what settings are used elsewhere in the system to set the Approval status based on the Production Workflow status, but for now, please set these items if you are using the Client Portal for Material Management._

The Material Rejected Artwork Stage (introduced in version 2022.4) is where you would select the Artwork Status that you would like the material to go to when the artwork is rejected in the Portal. This field is only necessary if you are using our InDesign Extension to build the material. It puts the material back into the Artist’s queue when re-work is requested.

## An End User’s View - Use Cases <a href="#_toc113467269" id="_toc113467269"></a>

Now that we have talked setup, let us discuss some workflows where these settings may be used. We will use the same product as the screenshots above in the example use cases, so you can follow along with the setup. You might not use ALL the following use cases in your own environment, but different Naviga Clients do things differently, so all these are supported ways to work.

### #1 – Workflow of an Artist Completing a material using InDesign <a href="#_toc113467270" id="_toc113467270"></a>

When an Artist in InDesign sets a material for this product as complete, the following will happen in the above example product.

![](<../../../.gitbook/assets/8 (4).png>)

• Production Status will be set to “Out to Proof” because on the Product Setup Material Handling Screen this was set:

![](<../../../.gitbook/assets/9 (10).png>)

• The Approval Status on the material will be set to “Proof out to Client” because of the Production workflow setup for the above Out to Proof setting

![](<../../../.gitbook/assets/10 (6).png>)

• Above Approval Status will allow this material to be approved in the Portal because of the Approval Status setup for “Proof out to Client”.

![](<../../../.gitbook/assets/11 (27).png>)

• Not related to status, but emails may be sent out to one or multiple people based on settings on the Product Material Handling screen

![](<../../../.gitbook/assets/12 (4).png>)

### #2 – Naviga Ad User reviews the Material on the Material Record itself and wishes to Approve or Reject it. <a href="#_toc113467271" id="_toc113467271"></a>

If a Naviga Ad user gets an email that the material was completed by an artist that email might contain a link directly to the material record to make it easy to approve/reject the material.

![](<../../../.gitbook/assets/13 (4).png>)

From that material record the user can select Approved or Rejected in the dropdown for Approval Status. “Approved” and “Rejected” are flags on the Approval Status setup, and that is what we use to understand if the material is being approved or rejected. Then based on the setting on the Product’s material handling, the Production Workflow will be updated accordingly. (Note, the “Rejected” flag was new in 2022.4)

![](<../../../.gitbook/assets/14 (12).png>)

If the Material is Approved, that is all that is needed to be done here.

![](<../../../.gitbook/assets/15 (19).png>)

If the Material is Rejected, the user should scroll up on the Material Record and set the Artwork status to a non-complete status like below. This will ensure that the material pops back into the artist’s queue to be re-worked. The artist assignment can also be optionally removed if you wish for the material to go back into the queue for any artist to pickup and work on the corrections.

![](<../../../.gitbook/assets/16 (8).png>)

While here on the material screen, of course it will also be necessary to add a note and/or new components, so that the artist understands what additional work is needed.

If you are using the InDesign Extension for building the materials, going to the Material record itself for approvals and rejections is the Naviga Recommended method of doing this function. The reason being that IF a material needs to be sent back to the artist for re-work, the notes and the Artwork status are all right here on this record, so it is less jumping around for the user.

### #3 – Naviga Ad User reviews the material from the Print Production Report and wishes to approve or reject it. <a href="#_toc113467272" id="_toc113467272"></a>

Rather than linking to the material directly from an email, in some cases, the user might prefer to work from the Print Production Report and filter by status to find all materials that are ready for proofing.

![](<../../../.gitbook/assets/17 (6).png>)

From here, the user might select one or more campaign lines and set the workflow status of selected orders from the dropdown menu.

![](<../../../.gitbook/assets/18 (7).png>)

Based on the Production Status selected here, the Approval Status also will be updated accordingly. (According to what was set up on the Production Status Setup)

Alternatively, on this same screen, rather than updating the status right here, the user might select the Line Number to open the Line Edit screen:

![](<../../../.gitbook/assets/19 (15).png>)

A new status selected here will also update the Approval Status according to setting on the Production Status setup.

In both of these options under Use Case #3, IF you are designing the ad using our InDesign Extension, and IF you are updating the status to REJECT the material, then you must also go to the material record itself to update the notes so that the artist knows what to change and possibly also add components so that the artist actually knows what needs to be modified. The Artwork Status will also need to be updated to something other than complete as well. That can be done from the Production report or from the Material Record itself

### #4 – Naviga Ad User reviews the material from order entry screen and wishes to approve or reject it. <a href="#_toc113467273" id="_toc113467273"></a>

If the user is working in the campaign itself, they can open the line item and update the Production Status here and the material approval status will update accordingly

![](<../../../.gitbook/assets/20 (2).png>)

Same comment here as use case #3 – if you are rejecting the material, you would also need to go to the material itself and update the Artwork Status and notes so the artist will get the material back in their queue.

### #5 – Customer, using the portal reviews the material and wishes to approve or reject it. <a href="#_toc113467274" id="_toc113467274"></a>

If you are using the Client Portal to accept and reject materials the customer can log onto the portal and see any available materials pending approval

<figure><img src="../../../.gitbook/assets/image (227).png" alt=""><figcaption></figcaption></figure>

Materials will be displayed in the portal for a client to see and approve if the following conditions are met:

*   The material itself is in an Approval status indicating that it is allowed for approval as set in Material Approval Setup

    <figure><img src="../../../.gitbook/assets/image (1220).png" alt=""><figcaption></figcaption></figure>
*   The Portal setup option “Hide Materials Pending Approval” is set to “no”

    <figure><img src="../../../.gitbook/assets/image (901).png" alt=""><figcaption></figcaption></figure>

If I client clicks the thumbs up on the material, they can optionally add comments and then submit their approval. If a client clicks the thumbs down on the material, they will be required to enter comments before submitting their rejection.

The approval status will be updated based on the settings here on the Portal setup:

<figure><img src="../../../.gitbook/assets/image (1396).png" alt=""><figcaption></figcaption></figure>

The Production Status will be updated according to the setting on the Material Handling on the Product

<figure><img src="../../../.gitbook/assets/image (745).png" alt=""><figcaption></figcaption></figure>

If a material is rejected, the material itself will need to go back to an artist. The Material Rejection Artwork Stage on the Portal Setup will set the Artwork status to the appropriate setting to return to the artist’s queue.

If it is desired to go back to the unassigned queue for modification rather than the original artist, it is recommended to clear artist assignment upon completion of the material in InDesign using this setting on the Artwork Production Workflow setup.

<figure><img src="../../../.gitbook/assets/image (1427).png" alt=""><figcaption></figcaption></figure>
