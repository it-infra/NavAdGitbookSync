# Statements

## Prerequisites

### AR Statement Template

To create the AR Statement PDF which is sent to your clients, first navigate to the menu Setup -> AR Statement Template and create one or more templates. Click “View Merge Fields Documentation” to see all HTML fields available for your use on the template. This requires HTML knowledge to design. If you need assistance please contact Naviga Support.

<figure><img src="../../.gitbook/assets/image (368).png" alt=""><figcaption></figcaption></figure>

In the HTML tab, design the HTML template and save it. You can choose this form to be the default for the advertiser in the AR Setup node on the advertiser account maintenance screen. Below is a sample statement to get you started.

{% file src="../../.gitbook/assets/AR Balance FWD Statement - Advertiser.txt" %}

{% file src="../../.gitbook/assets/AR Standard Statement - Advertiser.txt" %}

### Link Templates for Use

For the system to be able to use the templates, they must be linked to where they will be used.

* The [A/R System Parameters](setup-a-r-system-setup/#statement-forms) - Set the default templates here. Three different templates can be set:
  * Default Naviga Statement Form
  * Default Naviga Statement Form for Agencies
  * Default Naviga Statement Form for Parent Companies
* Optional - if you support multiple forms languages, set the form for each language on the A/R System Parameters (above) and set the language on the customer ([Name Maintenance](customers-a-r/#a-r-setup) -> A/R Node)
* Optional - Set form overrides per customer - This can optionally be set on accounts that require a different form template than other accounts. ([Name Maintenance](../advertising/customers/advertiser-maintenance.md#override-invoice-and-statement-form-settings) -> Advertising Node)

## Auto-Clear Client Balances

Navigate to the menu Statements -> Auto-Clear Client Balances

This feature is designed to run pre-statement process which selects all open invoices for a customer, selects a credit card on file that has been designated as the balance pay off card. This allows user to charge total outstanding balance in one transaction prior to sending out statements. It also provides a report that indicates any declines.

Navigate to the menu Customers -> Name Address Maintenance and choose a client in the drop-down menu. Click the AR node on the tree. Choose in the drop-down of the field “Auto-Clear Balance” a credit card on file. If none is present, enter one in the node “Cards on File” on this screen. Save the settings.

<figure><img src="../../.gitbook/assets/image (347).png" alt=""><figcaption></figcaption></figure>

Navigate back to the menu Statements -> Auto-Clear Client Balances.

Run the query to search by Client Group, Company, aging method, credit controller and age of balances. You can also use the credit controller on the account, amounts fields and include COA or not. Click “Get Clients”. These are the clients who have unpaid invoices organized by age bucket.

<figure><img src="../../.gitbook/assets/image (669).png" alt=""><figcaption></figcaption></figure>

Check the box(es) for the ones you’d like to process, or select all by clicking the box in the dark blue header bar and click “Process Payments”.

The screen lists any errors causing this transaction to fail, so that you can correct it. The screen also displays a tab to show successful transactions giving you a report of the transactions which went through.

Once the Auto-Clear process is run, you are ready to produce and send out statements.

## Default Statement Parameters

Navigate to the menu Statements -> A/R Statements

Click on “Default Statement Parameters” to setup the default values in all A/R Statements. These are just a basis on which to start but user can create their own templates for the statements and override any of these parameters.

Navigate to the menu Analysis -> A/R Statements. Click on “Default Statement Parameters” to setup the default values in all A/R Statements.

You can click on any of these parameters’ boxes to change the value from “No” to “Yes” to activate the parameter.

“**Display the Full Pay Amount on the Partial Payments”**, when set to “Yes”, the statement shows not only the Applied Amount, but also the full payment amount. If one payment is applied to multiple invoices, these amounts would be different.

“**Exclude Cash on Account for Pre-Payments**” is the field which when set to “Yes” would not show in the statement the cash on account applied to the prepayments on any invoices.

“**Exclude Cash on Account if no Invoice Type**” when set to “Yes” would exclude from the statement cash on account available in the system but not assigned to a specific invoice type. Only the cash marked as assigned to an invoice type would display.

**“Suppress Display of Credits”** when set to “Yes” would not show on the statement the credits this advertiser(s) has.

**“Suppress Display of Payment Information”** when set to “Yes” would not show the payment details on the statement such as the type of payment being credit card or cash.

**“Include Service Charges”** if set to “Yes” displays on the statement any service charges which the advertiser was charged on orders.

**“Consolidate Statements to Parent Company”** if set to “Yes” would add up to display the children companies’ statements on the parent company statement.

**“Separate Statements by Company”** if set to “Yes” and you are running statements for different companies set up in the system, then each company displays the statements for the advertisers assigned to the specific company. (This is YOUR internal companies, not Advertisers)

**"Sepatate Statements by Advertiser"** is for Agencies. If one Agency has 5 clients a "No" answer here will product one Statement for that Agency. A "Yes" answer here will produce 5 separate statements, one for each Advertiser Account.

**Suppress Balance Forward Details:** When checked, then the system uses the “Suppress Details Before Date” set on the Generate Statement screen to suppress the invoice (open and paid) details as well as the payment details.

**Sort Option** is a drop-down menu which allows you to sort the statement information by Bill-to name, ID or Postal code.

**Print message** if balance is between n-nn days is a free entry field where user can enter a message which they would like to be printed on the statement depending on the number of days the balance is due. So, if the balance is due 0-30 days, you can enter a message different from if the balance is due 31-60 days and so forth. The advertiser will see this message on the statement.

## Generate A/R Statements

Then click on the node “Generate A/R Statements” to begin setting the remaining parameters. For example, “Suppress Details Before Date”, when a date is entered in this field, the statement hides paid invoices before this date. Whether open invoices prior to this date are displayed will be dependent on the Statement Parameter for Balance Forward Suppress Detail setting. If that is set to yes, then all invoices prior to that date will be lumped into a “Prior Balance” total. If that is set to no, then unpaid older invoices will be displayed.

Fill in any desired Customer Selection Criteria, Ad-Specific Criteria or Exhibition-Specific Criteria to filter your results.

You can also override the default parameters in the bottom of the screen. When finished, click on “Generate Statements” and the system prompts you save this as a template to be used later without having to set all these parameters every time you want to generate a statement. You can override the [statement default templates ](setup-a-r-system-setup/#statement-forms)here and you can also choose to run the live batch or a test batch. Test batches won't actually email out the pdf or link the statement to the client account. A live batch will email the statements to customers who have been configured to get emailed statements in [Name / Address Maintenance](customers-a-r/#statement-details).

If using Fabsoft forms click the node “View Reports” and the screen displays all reports with a hyperlink to PDF. If using HTML forms, click the “View Batches” node instead.

<figure><img src="../../.gitbook/assets/image (1018).png" alt=""><figcaption></figcaption></figure>

Once in the list of batches click the pdf icon to see and print the batch of pdfs (could take a few minutes to complete if you have a large batch). To see individual pdf's, click on the batch number and then find the customer you would like to see and click the pdf icon just for that customer.
