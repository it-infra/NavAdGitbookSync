# Material Handling

If you haven't already, before completing this setup, give [_**"Overview - Ad Production & Material Status Workflow"**_](../../../production-ad/overview-ad-production-and-material-status-workflow.md) a read as that looks at a high level at several of these settings and how they tie together with workflow.

## Engage Portal / Material Approval Integration

This section is about what happens to the Production Status of the orders using a material when a client approves/rejects a material online.

The first two settings in here are also used when an internal user approves a material on the material record.

<figure><img src="../../../../../.gitbook/assets/image (1590).png" alt=""><figcaption></figcaption></figure>

**Production Status on Material Approval -** When the material is approved in the Advertiser Portal OR via the Material record, order production statuses using this material will be updated to what is set here.

**Production Status on Material Rejection -** When the material is rejected in the Advertiser Portal OR via the Material record, order production statuses using this material will be updated to what is set here.

**New Material Upload Preflight Status -** This is only used for customers using the Advertiser Portal and the built in Integration with Twist / Asura. Some clients instead use Interface Link for Preflight Integration and in those workflows Production Statuses will be updated with statuses and this field will not be used.

**Notify User / Email User -** these settings will put an alert on the CRM alerts for the selected user or send an email to the provided email address when a client uploads material through the Advertiser Portal.

## Engage Portal / Production Workflow Integration

The following settings are only used when a client uploads new material or selects existing materials through the Advertiser Portal

<figure><img src="../../../../../.gitbook/assets/image (1362).png" alt=""><figcaption></figcaption></figure>

**Production Status on Pickups -** this will be the production status set on the order / issue when a client selects to re-use exiting material for a future issue

**Production Status on New Materials -** this will be the production status set on the order / issue when a client selects to upload new material for a future issue

**Notify User / Email User -** these settings will put an alert on the CRM alerts for the selected user or send an email to the provided email address when a client uploads material through the Advertiser Portal.

## Preflight / Production Workflow Integration

This is only used for customers using the built in Integration with Twist / Asura. Some clients instead use Interface Link for Preflight Integration and in those workflows Production Statuses will be updated with statuses via Integration Link and this section will not be used.

<figure><img src="../../../../../.gitbook/assets/image (930).png" alt=""><figcaption></figcaption></figure>

## Artist Workflow Integration

This section is only used by Naviga users who use our InDesign Extention integration. If you are not using InDesign Integration, this section can be disregarded.

<figure><img src="../../../../../.gitbook/assets/image (1316).png" alt=""><figcaption></figcaption></figure>

Artwork Completed Production Status - When a material is completed in InDesign, this will be set as the Production Status for any orders using that material (in this product)

Preflight on Complete - This is only used for customers using the built in Integration with Twist / Asura. Some clients instead use Interface Link for Preflight Integration and in those workflows the integration with preflight software is driven by production statuses and not via built-in Preflight settings.

[Internal Email Notification Form](../../material-approval-email-templates.md) - When the artist completed material in InDesign, a notification email is sent out to one or more people (as determined by the email setting below). The form selected here will be the form used for Internal notifications.

[Client Email Notification Form](../../material-approval-email-templates.md) - When the artist completed material in InDesign, a notification email is sent out to one or more people (as determined by the email setting below). The form selected here will be the form used for external/client notifications.

Email Notifications To - There are 4 options in here. You can select one ore more of the choices

* Sales Rep(s) on the order
* Production Controller on the Campaign header
* Production Controller on the Product
* The client (The client person selected for the email will be the production contact from the campaign, which may have been defaulted onto the order from the Brand setup)
