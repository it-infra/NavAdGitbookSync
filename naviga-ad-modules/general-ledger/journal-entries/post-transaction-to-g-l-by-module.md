# Post Transaction to G/L by Module

The purpose of this document is to explain how users can post journals from various modules to the General Ledger.

## Phantom Scheduler Prerequisite <a href="#_toc111207606" id="_toc111207606"></a>

User must start the phantom scheduler to process and view the journals posted to G/L. To do so, navigate to the System Settings module. Click on the menu Setup -> Phantom Scheduler.

Click on “Enable Scheduler” if it is not already enabled.

## Post to G/L <a href="#_toc111207607" id="_toc111207607"></a>

Navigate to the module General Ledger. Click on the menu Journal Entries -> Post Transaction to G/L by Module.

Choose the “Module to Post” value in the drop-down menu. This can be All Journals or by specific module. Enter the batch number in the field or leave blank to post all batches in a module.

Choose the company from the drop-down menu and choose the financial period up to which to post the journals. Click on “Post to G/L”.

A popup screen displays to allow you to schedule the posting regularly or to run it one time only.

Some users may find it beneficial to run the posting daily or weekly or hourly to ensure the general ledger balance regularly. Click the “Schedule it to run later”.

Choose the “Schedule Type” according to your needs.

### One Time <a href="#_toc111207608" id="_toc111207608"></a>

Choose for example “One Time”. And then you can choose the date and time when you can run this posting process. Then you can enter the email address of the person to be notified when this is complete by receiving an email.

### Hourly <a href="#_toc111207609" id="_toc111207609"></a>

Choose the option “Hourly”. Then choose the date and time to run this posting.

If you want to repeat this indefinitely, click the “No” button to change it to a “Yes”.

![](<../../../.gitbook/assets/1 (52).png>)

Enter the number of times you want this process to be repeated, meaning if you enter 10, then the process will be repeated every hour for 10 hours.

Enter the email address of the person to receive the notification. When finished click “Set Schedule”.

### Daily <a href="#_toc111207610" id="_toc111207610"></a>

Choose the option as “Daily”.

![](<../../../.gitbook/assets/2 (23).png>)

Enter the date and time when to run this daily. Similarly, you can enter the “Yes” indefinitely to keep running the process. Enter the number of times this can be repeated and the email address of the person to be notified when this posting is complete.

### Monthly <a href="#_toc111207611" id="_toc111207611"></a>

Similarly, you can choose the process to be monthly, define the date and time and click the “Yes” to repeat indefinitely as needed. Specify the start date and time on which to post and the number of times the process will repeat.

### Week Days <a href="#_toc111207612" id="_toc111207612"></a>

Similarly, you can choose the process to be on week days only as in Monday through Friday, define the date and time and click the “Yes” to repeat indefinitely if needed. Specify the start date and time on which to post and the number of times the process will repeat. When finished, click on “Set Schedule”.

A pop-up screen displays with the Job ID of the posting.

![](<../../../.gitbook/assets/3 (82).png>)

## Posting History <a href="#_toc111207613" id="_toc111207613"></a>

At any time after the posting is complete, click on the “Posting History” tab and enter the date range during which you want to view the posting records.

Click on “Retrieve History”. Note that the system displays if there are any warnings issued for this posting. Click on the job ID to view the posting details.

## Post from Child Account <a href="#_toc111207616" id="_toc111207616"></a>

This feature is useful when Naviga splits the software into a Book Version and an Ad Version for Clients who must have separate instances because they are on Digital First in Ad, but also still use Book. So, Naviga split the software into two databases, one with Ad Version and one with Book Version. Clients still must keep the full GL on one database, so this is a feature for clients to transfer the Book G/L data over to the Ad G/L Module. Click the node with this title to import and consolidate financial information from additional Naviga Ad databases. This process will get Summary G/L Amounts for one Company and one Financial Period from the Child Database (source) and create a Journal Entry to the matching GL Accounts in this Parent Database (target).

![](<../../../.gitbook/assets/4 (57).png>)

To run the process, select the Child Account code (see below), input the Financial Period, and click the “Get Data” button to see a preview of the G/L Accounts and Amounts which will be on the Journal Entry. Only amounts that have not been previously imported will display so that it is possible to run the same Financial Period again to incorporate new GL Amounts without duplicating.

After reviewing the displayed lines, click the “Run Process” button to create the Journal Entry. Resulting Journal Entries are still unposted and are named “CHILD.UPLOAD.x”, sequentially numbered for each time the process is run.

### Prerequisites <a href="#_toc111207617" id="_toc111207617"></a>

The following rules must be followed, or the import will be unsuccessful:

* The Parent and Child Databases must have the same G/L Structure.
* The Parent Database must have existing G/L Accounts in the target Company that match the GL Accounts (except segment 1 – Company) that are being imported from the source Company.
* If the Child Database is multi-Company, it must not have a Multi-Company Balancing Requirement of “Allow lines for more than one company do not require each company's lines to balance.”

The Child Accounts to Process must first be set up in GL System Setup with Naviga Support assistance. Each Company on the Child Database that will be imported into the Parent Database must have its own entry in the Child Account Integration Settings table.

![](<../../../.gitbook/assets/5 (2).png>)

A three-digit code (alpha-numeric) and description can be chosen to identify the Child Account. Naviga Support will provide or input the required Database Path.

The mapping of Child Company ID to Parent Company ID can be customized: a) a “copy” model would use the same Company in both places, b) a “consolidate” model would map each Child Company ID to a single Parent Company ID where the consolidation is being done.

The Conversion Currency ID column is reserved for future development and should be left blank.

## List of Unposted Items <a href="#_toc111207615" id="_toc111207615"></a>

Click the node with this title to view all items which have not been posted to G/L. These are displayed under each node according to the transaction type.

The “Unposted Transactions Summary” provides a list of all unposted transaction types and the number of each type.

<figure><img src="../../../.gitbook/assets/image (485).png" alt=""><figcaption></figcaption></figure>

Under each subsequent menu, can see the detailed transactions. For example, navigate to Unposted A/R Invoices to see the 2 unposted invoices from the above summary

<figure><img src="../../../.gitbook/assets/image (266).png" alt=""><figcaption></figcaption></figure>

Select level of detail desired from the Report type dropdown:

* Summary by invoice w/o detail shows as above
* Summary by invoice w/ detail will include a > to the left to drill down and see journal entries
* Break by G/L account will group details by G/L Account ID

## Posting Warnings and Errors <a href="#_toc111207614" id="_toc111207614"></a>

Once the posting is complete, the warnings if any display. These do not prevent the posting process. But posting errors if any in certain lines prevent the posting of these journals. To view the errors, click on the node “G/L Posting Error Report”.

Click the expansion arrow for any of the transaction items and the system displays the details of the journal entries in question. You can also follow the transaction type hyperlink to view it in detail such as the invoice or journal entry or other type of transaction.
