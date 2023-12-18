# Production Workflow Setup

The sections below show how to set up the Production workflow. See also [Ad Production and Material Status Workflow ](../production-ad/overview-ad-production-and-material-status-workflow.md)guide to see how the various statuses within Naviga Ad work together

### Master Stages <a href="#_toc76551976" id="_toc76551976"></a>

You can setup a basic set of stages which you can then draw from to apply to product-specific material stages. They define the workflow steps required for the material process flowing through the Ad module. On reports showing a single product, the Product's Production Stage will be displayed, but on reports that show various products together (Production by Product Group or Production by Sales Rep for example), the master status will be displayed.

1. Navigate to the menu Setup -> Production Workflow setup and click the node Master Stages.
2. Enter the description, check the box to mark any order line item with a material in this stage as completed. Leave unchecked if the stage is not for a completed work. Once the material is marked as completed in an order, these line items with this materials completed will not display in the Production by Controller list. Only unfinished items will display.
3. Save the stages.
4. You can now mark the stages with any colors you’d like to be reflected in the production reports.

### Material Stages <a href="#_toc76551977" id="_toc76551977"></a>

1.  Navigate to the menu Setup -> Production Workflow setup and select the node "Stages" to create or copy another publication’s different workflow stages.

    <figure><img src="../../../.gitbook/assets/image (641).png" alt=""><figcaption></figcaption></figure>
2. Choose the publication from the drop-down.
3. Enter description and choose the Master stage related to this stage.
4. Select the Approval status appropriate for certain stages (where applicable). Typically you should only need a material approval stage in Proof out or later stages.
5. You can then check the box to allow the production stage to be visible and used in the line item entry. In the production screens all production stages are visible, but in order entry, you may choose to restrict some.
6. Check the box corresponding to Artist Required if indeed an artist is required to work on this material.
   1. Some sites will use our Indesign Extenstion (Internal Artist Required)
   2. Some sites will use a 3rd party design software (External Artist Required)
   3. Some sites will use both, but only one should be selected per stage, otherwise the material will show up in Indesign AND be sent to 3rd party and there will be duplication of efforts.
7. Check the box if this stage requires the order to have the material attached in the order entry screen (typically used in a status such as "pickup" or "materials received" to ensure that a rep doesn't change the status but forget to attach the material.
8. Continue to add stages and then save.
9. You can then edit the line color which is reflected in the Production reports screens for each line item which has material corresponding to this stage. It’s recommended that the colors for items from the master list be marked the same as the colors you chose in the Master Stages setup so that the production reports are clearer.

### Stage Reminders Setup <a href="#_toc76551978" id="_toc76551978"></a>

1. On the same screen, click the reminders node to configure email reminders for the different stages to the production contacts and reps on each order. You can setup also the automatic system change of the production workflow stage once the reminder has been sent.

![](<../../../.gitbook/assets/3 (84).png>)

1. You can choose the email templates to use for each reminder. These templates are created under from the Ad -> Setup -> Templates -> [Production Reminder Email Templates](templates.md#production-reminder-email-templates) menu.
2.  The days' reminder duration are the days counting backwards from the material due date. So, for example, if you enter 5 and the material due date is 12/25, then the system will count backwards from the 25th by 5 days and then allow you to view the orders with the reminders due on the Print Production Reminder by Controller screen. Note that the Material Lead Time (Days) is entered under the menu Setup -> Product Setup -> Product Details.

    <figure><img src="../../../.gitbook/assets/image (332).png" alt=""><figcaption></figcaption></figure>
