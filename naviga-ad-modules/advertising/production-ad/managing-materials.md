# Managing Materials

## Artwork Production Management

The Artwork Production Management screen is your hub for materials that are being worked on in the Naviga Ad Indesign Extension.

<figure><img src="../../../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>

Across the top, you can select a single product, a group of products or you can leave it blank to see everything.

In the artist dropdown, select an artist to filter by that artist. Select "unassigned" to focus on the unassigned materials if your intent is to make new assignments. OR you can also leave that blank to see all artists and the unassigned together.

In the size dropdown, you can select to see points, Inches, CM, MM or all. If you are doing a mix of print and digital ads in InDesign, I recommend to leave at all, so that you will also see the pixels for Digital Ads. If you filter by say inches, and you have digital lines, you will still see the material, but it will appear as if the size is 0 x 0 Inches.

And finally there is a filter to also show completed lines, including those that were completed during a certain date range.

In the top right corner of the results grid, there are two buttons.

1. Bulk Update Artist Assignment: Select this option to change selected rows from one artist to another. Leave the Change from artist blank if you want to change the unassigned rows to someone. If no rows are selected, then any change will affect all rows that match the "Change from" criteria.
2. Bulk Update Artwork Status: Select this option to change selected rows from one status to another. Same as above, leave the status from as blank to change from null to something else. Check rows to only apply the change to certain rows. if you do not check any rows it will apply to all matching rows.

## Artwork Time Spent Report

The Artwork Time Spent Report is used to display how much time an artist spent on a material. It is optional for the artist to[ log their time ](working-in-the-indesign-extension.md#artwork-workflow)when working in InDesign, so if you plan to use this report, be sure to request that the artist click the button in InDesign to log the time spent. The InDesign Extension will start the clock when they open the ad to start working, but it does require that the artist click the button to submit the time spent. They can also add a comment when submitting.

<figure><img src="../../../.gitbook/assets/image (1507).png" alt=""><figcaption></figcaption></figure>

## View/Edit Materials / New Materials

These two menu options take you to the same screen. The only difference between them is that the New Materials option will take you to the screen already in New Material mode. It iwll auto-assign a new material ID and allow you to fill in the details about the material. Selecting View Edit Materials will assume that you would like to enter in a material ID and open that material or search for an existing material. There is a new button available in case you do not find an existing material and need to create a new one instead.

The Material record is broken up into many sections. This is a brief screen recording of all the sections. Each user can determine the order in which the sections are displayed and whether the shutters are opened or closed. It remembers how you last viewed it and will display the same way next time.

<figure><img src="../../../.gitbook/assets/MaterialRecord.gif" alt=""><figcaption></figcaption></figure>

#### Material Header

The Material Header displays the following information:

![](<../../../.gitbook/assets/image (185).png>)

1. **Material ID:** if in View/Edit mode, enter ID in here and click refresh to open that material. In New mode, the material ID will be auto-assigned here. Can also click the search to find a material by advertiser
2. Material Type (Print, Digital, Semi-Display, or Text): Print and Digital will be the only ones you might actually select when creating a new material in this screen. Semi-Display is a listing ad type, but ready artwork was provided by the client and was uploaded as a pdf during order entry. A text material is similar, but it was a material that was created during order entry, either from a template or manually via the HTML Text editor window.
3.  Material Description. This is the text that you see when looking at the material record when it is assigned to an order. This field may be required based on your Group Security -> Production Node.

    <figure><img src="../../../.gitbook/assets/image (605).png" alt=""><figcaption></figcaption></figure>
4. Advertiser ID / Advertiser Name: The client who owns this material.
5. Date Received: This will default to the date that the material was created, but can be overwritten if necessary
6. Expires on: After this date, the material will no longer appear as an option for Pickup and it won't be displayed on the Client Screen on the Ad Production tab. If you know the ID, you can still look it up by that ID as it will still exist in the file system, but it won't clutter up the UI for the user. For Liner type ads this expiration date will default to 3 years from the create date. For Display/Digital Ads, there is no default, but a user can enter a date in there if desired.
7. Proof Date: Can enter a date in here for proofing purposes. This is informational and doesn't have a function in the Naviga Ad InDesign Extension. (If you are using the InDesign Extension, the proof date can be found in the Approval History section. There could be several dates if there was back and forth before final approval was received.)
8. External ID: Used in Interfaces to 3rd party ad tracking systems.
9. Pickup from ID (or Copied from ID): When a material is created as a copy of another material (Using the "Attach Existing Material" button in Order entry or other screens), the original material ID will be put here. Note - This doesn't have a function in the InDesign Extension, but might be good for informational purposes or for 3rd Party Integrations.

#### Local Components

Local components are intended to be used for just this material record. If the client is providing ready artwork, you might just have a pdf in this section, and that pdf can be used to generate the jpg preview and it can be marked as Final to be the component that is sent to print.

If you are using the Naviga Ad InDesign Extension or 3rd Party Ad Tracking systems, you might have several materials attached here that are intended to be used for the design of the ad.

<figure><img src="../../../.gitbook/assets/image (889).png" alt=""><figcaption></figcaption></figure>

When the material is completed, the InDesign Extension will pass back a jpg preview image, a final pdf and the indd file that was used to output the final ad.

Only one material can be marked as final in this window.

#### Global Components

Global components are meant to be reused for multiple Material projects. Things like logos and stock photos would be considered to be a Global Component. If a global component is already attached to the advertiser from this material, the component can be selected from the dropdown.

<figure><img src="../../../.gitbook/assets/image (209).png" alt=""><figcaption></figcaption></figure>

Click the Search icon to find a global component or Create New to create a new one.

See [Global Component](managing-materials.md#global-components-1) discussion below for more information

#### Print Material Details

This section will display details about the print material. You won't see this section at all if the material is a digital type.

<figure><img src="../../../.gitbook/assets/image (1188).png" alt=""><figcaption></figcaption></figure>

Headline: The headline is a free-format text field to describe the headline on the ad. This MAY be a required field depending on your group security configuration

Material Size info: In the Columns, Inches, CM, Agate Lines, Words, Charcters, Material Size fields you will see some of these filled in, or others, depending on the kind of ad it is. Is this is a display ad that is col x inches, you will see the Columns and Inches filled in. If this is a liner type ad, you might see more info, like Agates, words and characters. If the ad is modular, you will see material size and a Width x height on the right side but no additional sizing information. Typically the sizing info is pulled from the order, so you wouldn't need to fill any of that in manually unless you were creating a material record apart from order entry.

Color: Color info for the material. Like the size, this would typically be pulled from the order.

This is a Coupon: This information is mostly for Planning purposes so that two coupons don't end up on back to back pages in the paper.

#### Digital Material Details

The following will be displayed only for digital materials

<figure><img src="../../../.gitbook/assets/image (1449).png" alt=""><figcaption></figcaption></figure>

Creative Type: This is the type of material that should be expected on the material record. If it is an Image and you would like to have an artist create a static image using the InDesign Extension, you can click "yes" for InDesign Eligible and the material will be sent to InDesign. If you select "3rd Party" then a code snippet will be displayed in this section so that you can copy and paste in some 3rd party code.\
The following Creative types are available in the Creative Type dropdown on a digital Material record.

![](<../../../.gitbook/assets/image (425).png>)

The creative types "Custom" and "Native Format" can have very sophisticated questions to be answered, files to be uploaded, etc. We are not tackling that part at this time. Currently, we allow the creative container to be selected in Naviga and passed across to GAM with the required information to create the creative record, but not to fill in all the information which would be required to actually publish that creative type. That part will still need to be filled in in GAM, but we can send the container over with enough information to create the record for someone to then complete. Please see Google Setup for more information on setting up these creative types

Click URL: this is required if we are sending the material to GAM. Material will be rejected in the integration if the Click thru URL is missing

Size Code: this is info for the size of this material. This is also required by GAM and if the Ad Material is a different size than the what it is expected to be, Google will also reject it.

Hover Text: This is the alt-text that is displayed when hovering the mouse over the ad. This isn't functional in Naviga Ad, but we will pass to the ad server

InDesign Eligible: click yes if you would like an artist to create this material in InDesign

Ad Server and ID on the Ad Server - these are grayed out and are not editable, but will provide the information from Google.

#### InDesign Extension

This section allows for setting up some specifics on the material when the artist is working on the ad. Be sure to select the unit of measure before adding margins, bleed or slug measurements.

Page count & facing pages are intended for Inserts that are being designed in house.

<figure><img src="../../../.gitbook/assets/image (1593).png" alt=""><figcaption></figcaption></figure>

#### Artwork Production

This section will display who the assigned artist is to work this ad in InDesign and what the current status is (if there is any). If the artist is blank then it will show up in the Unassigned queue as long as other [requirements are met for having a material display in Indesign](working-in-the-indesign-extension.md#order-elements-needed-for-material-to-come-into-indesign).

<figure><img src="../../../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure>

If any comments were added in the Artwork Production Management Report, they will be displayed in the comments box above. If the artist logged any design time in the InDesign Extension they will also be logged here, along with any notes they added when logging their time.

#### Approval

The approval section will display the current approval status and any comments that were entered here on the material.

<figure><img src="../../../.gitbook/assets/image (890).png" alt=""><figcaption></figcaption></figure>

The approval history section will display any changes to the approval status. If approval emails are sent from InDesign, they will display here too. If the artist sends the approval from InDesign to a sales rep or production controller, and then that internal user needs to send to client, there is also an option in here to send approval email to client.

#### Notes and Comments

Two separate sections here. Comments are free-format and can be appended to, overwritten, or deleted. Notes are time and date stamped and cannot be deleted. Both will show up in InDesign for the artist to see.

<figure><img src="../../../.gitbook/assets/image (413).png" alt=""><figcaption></figcaption></figure>

#### Edition Splits

This is a client-specific feature (FJI) and covers a very specific use case, so it wouldn't be applicable to most implementations. It is not supported with Naviga Plan workflow.

#### Orders using this Material

This will list all order insertions where this material is in use. If you see an order id here with no issue date, it means that the material was created for an order, but was never linked to an issue date.

Click on the Assign to Other Future Lines to see a list of other orders with future dates, which match this size, and do not already have material assigned to it. From that list, select the lines that you would like to add the material to and click Assign at the bottom of the window.

<figure><img src="../../../.gitbook/assets/image (1471).png" alt=""><figcaption></figcaption></figure>

#### Material Handling

If you are integrating with a Preflight provider, this section will allow you to manually upload a new material for preflighting or view the outcome of an existing material that has already been preflighted.

## Materials by Advertiser

Navigate to Production -> Materials by Advertiser. This same report can also be accessed by opening a customer account from the Advertiser/Agency Inquiry option and then clicking over to the Ad Production tab on the customer overview screen.

<figure><img src="../../../.gitbook/assets/AdvertiserMaterials.gif" alt=""><figcaption></figcaption></figure>

Once the screen is open you can easily navigate to a different customer by using the Quick Account search option at the top right.

## Material Management

This screen is a customer-centric, material-centric approach to assigning materials to orders

<figure><img src="../../../.gitbook/assets/image (933).png" alt=""><figcaption></figcaption></figure>

Select a customer at the top and a date range and click get data.

In the insertions section, select the size that you want to assign material for.

Select consolidate issuee dates to have a single line for each issue:

<figure><img src="../../../.gitbook/assets/image (187).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
NOTE: when viewing in Consolidate Issue Dates mode, you will not be able to assign the production status when it is in a group, since production status is unique per product. switch back to non-consolidated view to assign production status. If the statuses happen to match EXACTLY, we will copy it for all lines to save users from having to select one at a time.
{% endhint %}

Select Show lines with materials if you need to make edits to something that already has material assigned. Set that to no to filter out those with material already.

In the top right, select to attach existing material if you are doing a pickup. Click "Create New Material" to create a new material record. Can also click on the "new" link on the order line itself to create a new material.

Click the "edit material" link to open the material record and make edits.

## Global Components

The concept of Global components was added to the material record for when components are meant to be re-used again and again on Campaigns. A Global Component tied to an advertiser might be a logo or other customer-specific images that will be used across many different material records. Global components are intended to be used in conjunction with the Naviga InDesign Extension. It might be useful with other 3rd party design tools, but would need to be tested for compatibility with the receiving system.

### View / Edit Components

Enter a component ID or click the search magnifying glass to search for a component to open. The search window allows for searching on Advertiser or Component tags

<figure><img src="../../../.gitbook/assets/image (710).png" alt=""><figcaption></figcaption></figure>

The above example component is one that is shared across several different Re/Max Realtors

If there is an associated tag, it can be entered here. Tags must be set up in advance (see Component tag section below)

Enter an External ID (if applicable)

Enter an expires on date (if applicable). After this date, the component will no longer be selectable on a new material

Select Storage type as link or file. If link is selected, the below area will allow for a file URL and a preview URL. If file is selected, the file details section below will allow for selecting and uploading a file into the system. If the file is an image file and not a very large file, you might only need the file details. if the file is very large, you might also want to include a browser friendly preview version of the ad

### New Components

See above descriptions in View/Edit Components. The screen is exactly the same, except it only will allow you to create a new component and the search option will be disabled and you won't be able to enter in a component ID.

### Component Tags

Navigate to Production -> Component tags. This screen is a list of tags that will be used on the New and Edit Compenents options. Add as many here as is needed to support the kinds of global component you will be using in your system. For example, Real Estate tags might be used to include tags across all Real Estate companies (like the R image for Realtor). Employment tags might include EOE logo, etc. My example of "Stock Photos" might be much too general for real life and you might have that more granular.

<figure><img src="../../../.gitbook/assets/image (222).png" alt=""><figcaption></figcaption></figure>
