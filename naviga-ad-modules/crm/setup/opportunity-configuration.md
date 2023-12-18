# Opportunity Configuration

Opportunity types in Naviga Ad CRM are configurable (pre-2023.1 it was hard coded as Advertising, Exhibitions, or both). When upgrading from a pre-2023.1 version a conversion will automatically run and will create those three Opportunity Types and any existing opportunities will be assigned to those types based on what type they were assigned when the opportunity was created. Additional Opportunity Types can be added by typing in the ID and Description and clicking the plus to add it. If do not use one of the older Opportunity types they can be deleted. Click and drag the three lines ![](<../../../.gitbook/assets/13 (2)>) to the left of the opportunity type to reorder into your preferred sort. Save the changes.

![](<../../../.gitbook/assets/14 (2)>)

## Opportunity Stages and Master Stages <a href="#_toc122615683" id="_toc122615683"></a>

Opportunities are defined by stages, according to the status of the negotiations with the client. For example, a stage can be in the beginning stage of cold calls and might be given a weight of 10%, then moved to a more advanced stage as talks progress to 25% and so forth. Each stage can be defined by a name which the user can choose in the opportunity screen. Each Opportunity Type can have its own unique stages. Sites already using CRM prior to 2023.1 will see their current opportunity stage setup for each Opportunity type converted over to this new structure with the upgrade.

To allow for reporting across all Opportunity Types, each Opportunity Type now will also be able to be linked to a Master Stage. If you choose to not set up master stages your system will still work as it did in previous releases, but you will only be able to see the Pipeline report one opportunity type at a time. If you have several opportunity types, it may be cumbersome to understand the full picture of all Opportunities.

First, Create the Master Stages:

<figure><img src="../../../.gitbook/assets/image (1326).png" alt=""><figcaption></figcaption></figure>

1. Enter an ID and a Description for the Master Stage (ID does _**not**_ have to be numeric as in the example)
2. Check the box if you wish for this stage to be included in the pipeline. You may wish to exclude some stages from the pipeline, for example lost or won stages are typically not considered to be in pipeline.
3. Select the Stage type (Open, Won or Lost)
4. Select the Lead Qualification for this stage (Open, Qualified or Disqualified, for those using Naviga leads functionality to track pre-opportunity sales progress)
5. Enter the probability of the deal closing
6. Click the plus sign to add to the list and repeat above steps until you have all necessary stages created
7. Drag and drop the 3 lines ![](<../../../.gitbook/assets/16 (1)>) to arrange the sort order for these master stages.
8. Save

Once you have created the Master Stages, then create the Opportunity Stages.

1. Select the appropriate Opportunity type at the top
2. Enter an ID and a Description for the Master Stage
3. Check the box if you wish for this stage to be included in the pipeline
4. Select the Stage type (Open, Won or Lost)
5. Select the Lead Qualification for this stage (Open, Qualified or Disqualified)
6. Select the appropriate Master Stage to display when viewing all opportunity types together in a report.
7. Enter the probability of the deal closing for this stage
8. Click the plus sign to add to the list and repeat above steps until you have all necessary stages created
9. Drag and drop the 3 lines ![](<../../../.gitbook/assets/17 (2)>) to the left of the stage to arrange the sort order for these master stages.
10. Save
11. Repeat these steps for each Opportunity Type that you have created.

<figure><img src="../../../.gitbook/assets/image (934).png" alt=""><figcaption></figcaption></figure>

## **Testing Notes for Stages / Master Stages**

You will only see the below option for “All Opportunity Types (Master)” if you have set up Master Stages and linked them to your stages for each Opportunity Type.

<figure><img src="../../../.gitbook/assets/image (1586).png" alt=""><figcaption></figcaption></figure>

If you do _**not**_ see the option for “All Opportunity Types (Master)” and would like to, follow these steps:

1. Navigate to Opportunity Type Setup (CRM Module > Setup > Opportunity Configuration)
   * Note: default Opportunity Types after upgrading will be Ad, Exhibition, or Advertising / Exhibition.
   * These were previously the hard-coded opportunity type options. If you were previously only using one of the options, you will be able to delete the unused opportunity types. If there are opportunities using that type, you will receive an error message.
   * Add any additional opportunity types needed for your business.
2. Navigate to Opportunity Master Stages and set up as many master Stages as you need
3. Navigate to Opportunity Stages and ensure that there is a master stage for every opportunity stage for each opportunity type.
4.  Navigate to your Opportunity Pipeline Review report

    <figure><img src="../../../.gitbook/assets/image (216).png" alt=""><figcaption></figcaption></figure>
5.  When viewing in the Master view, the stages displayed will be the master stages

    <figure><img src="../../../.gitbook/assets/image (820).png" alt=""><figcaption></figcaption></figure>

## Default Opportunity Type <a href="#_toc122615687" id="_toc122615687"></a>

Navigate to the Setup menu in the CRM module Setup -> User Security -> Access Control node. Click the drop- down menu Default Opp. Type and choose the type. The types displayed in the dropdown will be dependent on the types of opportunities setup previously.

<figure><img src="../../../.gitbook/assets/image (281).png" alt=""><figcaption></figcaption></figure>
