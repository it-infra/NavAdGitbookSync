# Group Security (Exhibitions)

Administrators can use this screen to control the permissions of users of a group to perform functions within the Exhibitions module.

## **Group ID**

1. Choose the group ID from the drop-down to setup exhibitions for this group of users.
2. Decription will display the name of the selected Group ID. It is a read-only field in this screen. To change the Description, use the Security Group Setup node.

## **Status Settings**

1. Select the default status for new campaigns
2. Click on the code you want available and move to the right side by clicking the right arrow into the allowed table. This will restrict the user not only from Creating an Exchibition order in that status, but also prevent them from editing a campaign in that status.

## **Exhibitor Types**

1. Move the types desired from the left to the right pane using the arrows. Exhibitor Types are created in Exhibition Code Tables -> Exhibitor Type Setup

## **Floor Plan Settings**

1. **Floorplan is View Only:** This option if checked will allow users to view the floor plan but not edit it. If this option is checked, the remaining options in the section will be set to No and will not be selectable. If set to No, the remaining options will fine tune what functions they can edit in the floorplan.
2. **Allowed to Split Booths:** This allows user to split the booth in the floor plan for sharing purposes.
3. **Allowed to Merge Booths:** This allows user to merge more than one booth together to give larger space for the exhibitor.
4. **Allowed to Renumber Booths:** User can assign different numbers to the booths than already existing.
5. **Allowed to Transfer Booths:** This allows user to transfer booths from one exhibitor to another.
6. **Allowed to Delete Booths:** If option is checked the user can delete the booth.
7. **Allowed to Move Booths:** User can move the booth from one spot to another on the plan if this option is checked.
8. **Allowed to Add/ Copy Booths:** If checked, user can add a new booth or copy an existing one.
9. **Allowed to Redraw Booths:** If checked, user can redesign a booth.
10. **Allowed to Re-size booths:** If checked, the user can resize the booth.

## **Order Amending**

1. **Allowed to Change Confirmed Orders:** If checked, this option allows user to change an order which has been confirmed. Otherwise, if this is not checked, once the order has been confirmed, user cannot change it. Typically, for unconfirmed orders the reps can make this change and pricing will be overwritten. If this option is Yes, then Option 2 will automatically be yes. If this is set to no, you have the choice to set option 2 to yes or no. Also, if this option is set to No, option 3 and 4 will also be set to no. If you are not allowed to change a confirmed order, you also should not be allowed to change a billed order.
2. **Allowed to Swap Stand Assignment on Confirmed Orders:** This option, if checked, allows reps to change the stand number on a confirmed order and move an exhibitor from one stand to another. For confirmed orders the rep is not allowed to change pricing but could move an exhibitor to another stand of the same size; regardless of exact dimensions of the stand.
3. **Allowed to Change Orders when Billing has started:** If checked, user can change the order after billing started. Otherwise, user will not be able to change a billed order. If this option is Yes, then Option 4 will automatically be yes. If this is set to no, you have the choice to set option 4 to yes or no.
4. **Allowed to Swap Stand Assignment where Billing Has Started:** This option, if checked, allows reps to change the stand number on a billed order and move an exhibitor from one stand to another. For billed orders the rep is not allowed to change pricing but could move an exhibitor to another stand of the same size; regardless of exact dimensions of the stand.

{% hint style="info" %}
For the above options:

If user cannot make changes (options 1 and/or 3 is no) but can change stand then following rules apply:

Call up order and click in stand number field, delete existing stand number.

Drop-down list will display only stands of the same total size (regardless of dimensions, so a 2 \* 5 is the same as a 1 \* 10). For most users, this may mean that someone must set up the stand before they can move the exhibitor to it.

This does not impact any pricing, so it is possible that pricing will be left as is unintentionally. For example, if the stand they were in or the one to which they are being moved has fixed pricing, the change will not change pricing, it will always use pricing from the original order.

The system will not look at adjustments, so for example, a stand that has a pillar in it might not be the same size as one that does, the system is only looking at actual stand size.
{% endhint %}

5. Allowed to Change Orders after the Show Date Has Passed: If checked, once the exhibition starts, user can still change the order.

## **Order Entry**

1. **Allowed to Create Divisions from Order Entry:** User can create the divisions from the order entry screen.
2. **Allowed to Set/Change Sales Rep Assignments on a New Order:** User can change to assign the sales rep in the order entry screen.
3. **Prompt to Save Modified Sales Rep Assignments as the Defaults on the Division:** Once the rep is assigned in the order, system can prompt the user to save this setting, so they are not prompted again. User can then choose yes/no to this prompt in the order entry screen. This will be set to no if option 2 is set to no.
4. **Allowed to Enter Pre-Payment:** User can enter a prepayment for an order if this option is checked.
5. **Allow Overbooking of Space Reservations on Quotes:** If checked, user can overbook space reservations on orders in the status “Quote”.
6. **Disable the Ability to Update Forms Tracking Dates from Order Entry:** This option if checked gives the ability to users to disable any changes to the dates in the Forms node in the order entry screen.
7. **For combined advertising campaigns the bill-to on the exhibition order must match the bill-to on the advertising campaign:** This option, if checked, forces the user to have the same “Bill-To” ID on the Exhibition order as the “Bill-To” ID on the campaign header. If checked the system will not allow user to proceed further with confirming and billing if they do not match.
8. **Disable Manual Billing Schedule Options if Templates Available:** When set to YES, options to ADD, DELETE and change the DATE on Billing Schedule lines will be disabled, and the user will be forced to select a valid billing schedule template. If no billing schedule templates are available, this rule is ignored.

## **Available Exhibition Reports**

1. Move the report from the reports not allowed to the reports allowed column. These reports are then visible to the CRM Dashboard users.

## **Other Settings**

1. Hide Budget Information on Exhibition Dashboard: When checked to “Yes” the budget information will not be displayed on the Exhibition Dashboard. If a Production Job is linked to the show, this will also control whether or not the P\&L details are displayed.
