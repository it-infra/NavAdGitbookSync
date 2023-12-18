# Plan Integration - A Quick Reference

### Purpose <a href="#_toc84344759" id="_toc84344759"></a>

The purpose of this document is to explain how users can setup the integration between the Naviga Ad (Digital First) system and the print production tool, Naviga Plan, so that users can create advertising orders within Naviga Ad, and they will automatically flow into Naviga Plan for production.

### Flow Summary <a href="#_toc84344760" id="_toc84344760"></a>

Create a campaign with material in Naviga Ad. From the Production Control menu in the Advertising system, you can view the ads which will be posted to Naviga Plan. When you login to Naviga Plan and view the worklist, the orders display where you can drag and drop the material on a page to preview and proceed with production steps.&#x20;

This integration works in two parts. When enabled, qualifying print order lines are moved into a queue file. The Windows Service monitors this queue file and sends these orders to Naviga Plan every few minutes (or however often it is configured to run). Naviga Plan then reaches back into Naviga Ad to retrieve the Hi-Res final PDFs (\~/interfaces/material/hires/{materialId}).

This queue is also used to capture qualifying orders for other integration, such as Whiteboard. In these integrations, the queue is processed differently so that for example, the data is sent to a different place.

### Prerequisite - Setup in Naviga Ad <a href="#_toc84344761" id="_toc84344761"></a>

Before orders will flow over to Naviga Plan, the Windows service must have the Naviga Plan integration enabled so that it processes the queue - this must be done by Naviga Support/Implementation team.

Navigate to the menu Setup -> Admin -> [Naviga Plan Integration](../naviga-ad-modules/advertising/setup/admin/naviga-plan-integration.md).

### Campaign Line Comment and Production Notes <a href="#_toc84344767" id="_toc84344767"></a>

There are two places on an order where notes will flow into Naviga Plan. Navigate to a campaign and edit the line item. Click the tab “Other Options”.

The “Internal Comment” section allows you to enter comments on the line item meant for internal use. When integrated with Naviga Plan, the internal comments flow into Naviga Plan in the Placement Notes field.

On the Production Notes tab in Naviga Ad, you can enter one or more notes. These will be listed in Naviga Plan in the Production Notes area.

See Also [Ad List Column Definitions](https://docs.navigaglobal.com/naviga-plan/plan-user-application/windows-menu/ad-lists/ad-list-column-definitions) in Naviga Plan Documentation

### Naviga Plan Setup <a href="#_toc84344768" id="_toc84344768"></a>

Prior to sending orders over to Naviga Plan, there will be some additional setup on the Plan side. This will be gone over in detail with your implementation resource if you are just starting a project, but here are some highlights to familiarize you with the screens and process.

Naviga Plan Setup is done in a browser with simple tabs going down the left side of the page and across the top page with various settings.  See [Plan Setup Documentation](https://docs.navigaglobal.com/naviga-plan/setup-and-integration/plan-setup) for details on the following:

* The General Tab will define file paths and information about the editorial system to which you will be outputting. Your Plan implementation specialist will set the General Tab up for you in advance of the first training session but will explain to you what all your settings are in case anything changes, and you need to add or modify one of the above settings.
* Product and product codes in Plan will be named the same as the products and their ID’s in Naviga Ad. Each product will be linked to a run order master.
* Sections in Plan are a big list that includes Sections, Positions, Ad Categories and sub-categories (these are imported into Naviga Plan once they are set up in Naviga Ad). The Run Order will organize those sections and positions into a hierarchy and link them to pagination rules.

{% hint style="info" %}
Note that Naviga Ad allows flexibility in business rules for sections and positions. These may be set as not used, as optional or as required. For products interfacing to Naviga plan, there are rules that are enforced by Naviga Plan. It is recommended that these rules are considered when determining what fields are required for ads that will flow to Naviga Plan.

At least ONE of these must be true on an order for it to go to plan:

• There is a section

• There is a position

• There is a section and a position

• There is a classified category (for liner ads and classified display ads) - As classified ads will have a classified category, they do not technically require a section. However, if you do choose to make sections required in Naviga Ad, then you will need to at least have a generic “Classified” section to house all classified categories. This will allow you to populate the required field in Naviga Ad, Naviga Plan will ignore the section if a category is present.
{% endhint %}

Naviga ad views classified sections by product and allows for use of the same section code across multiple products. Naviga Plan allows for the same setup but does not allow for the same section ID to mean different things in different products. For example, if you have a section id 123 meaning “News” in one publication, you cannot have section id 123 meaning “Sports” in another publication. Section ID’s should at least be consistent across products, if not unique across all products.

As Naviga Plan automatically flows advertising by section/position/category it is also not advisable to allow duplication between classified category ID’s and section ID’s. As an example, a classified category of PET should not use the same code as a publication section of PET Duplicating these codes could result in inaccurate pagination.

Please consult with your implementation specialist as you make these setup decisions.
