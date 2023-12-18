# Collection Letters

## Collection Letter Templates

Navigate to Setup -> Email/ Letter Templates.

<figure><img src="../../../.gitbook/assets/image (1071).png" alt=""><figcaption></figcaption></figure>

Prior to Sending any collection letters (or even setting up the defaults), the letters themselves need to be configured. There are 5 aging buckets, plus a default form. You don't need a unique form for every aging buckets as some can be reused if you don't want to change the message, but you can if you would like.

1. Click Create New under the heading "Customer Service - Templates"
2. Enter a name for the form
3. Enter a Subject Line. In the event that these collection letters are emailed to a client, this will be the subject line used.
4. Enter an optional description for the template
5. If Applicable, select or upload an attachment. (Might not be applicable for a form being used for a Collection Letter, but these templates are also used elsewhere in the system and an attachment might be more relevant to another scenario).
6. Click View Merge Fields Documentation to open a new tab with all available merge tags to use when creating your document template.
7. Click on the Editor Tab to design the letter using the Design or HTML tabs at the bottom of the window.
8. Click save to save the template

Here is a sample HTML template that can be used as a starting point for you.

{% file src="../../../.gitbook/assets/CollectionsLetter.txt" %}

Repeat above steps for all desired Collection Templates. If you do business in other countries, you can also set up these letters in different languages.

## Collection Letter Defaults

The Collections Setup menu provides a list of default collection letters depending on the aging days’ range.

Navigate to the menu Setup -> Collection Setup.

<figure><img src="../../../.gitbook/assets/image (1379).png" alt=""><figcaption></figcaption></figure>

The screen provides you a list of age ranges so that you can choose a default collection letter template for each range. The values of templates in the drop-down menu were previously created in the menu Setup -> Email/ Letter Templates.

Choose the appropriate template from the drop-down menu for each default age range and click the “Save” button.

### Form override by language

If you set up different forms for different languages, select the language here. Each of the default form lines are repeated for each language and you can link the appropriate form to the correct aging bucket for that language

<figure><img src="../../../.gitbook/assets/image (769).png" alt=""><figcaption></figcaption></figure>

### Collection Status Setup

User should setup the collection statuses in order to be able to use the credit control function defining the different collection statuses for customers.

Navigate to the menu in the Credit Control module or the A/R module called Setup -> Collection Setup. Add the status to the list and a description. Then click the + sign. Repeat as needed and then save the settings.

Once a status is used, it cannot be deleted. In use statuses will have a gray x button. Statuses which can be deleted will display a red x.

## Sending Collection Letters

Navigate to the menu Credit Control -> Collection Letters.

<figure><img src="../../../.gitbook/assets/image (963).png" alt=""><figcaption></figcaption></figure>

Choose the desired filters, such as Aging Method, Credit Controller, Balance, etc. Once appropriate filters are in place, click on “Get Clients”.

In the data results, check the box for the client(s) for which you want to generate letters and click “Generate Letters”. The system produces a pop-up containing the same default values you had chosen previously in the collection setup screen.

<figure><img src="../../../.gitbook/assets/image (1010).png" alt=""><figcaption></figcaption></figure>

You can change the options in this screen for any of the templates’ default values for these clients which you have selected. Enter the New status and the next contact date. If you want to send emails to customers configured to receive emails, leave the "send emails" flag set to yes. If you would like to include open invoices as attachments to the email, leave the Include Invoices option set to "yes." Click the "Generate letters" button.

<figure><img src="../../../.gitbook/assets/image (1438).png" alt=""><figcaption></figcaption></figure>

This screen tells you the letter batch ID so you can view it later. It also states the number of letters generated, emailed and if there are email errors which occurred to alert you if the email did not send.

You can then view and print the letters. This can be for all letters or only the ones which were not emailed. Click one of these buttons.

A separate screen opens, and you will see the letters being generated. You can perform other functions while this function is taking place. It will take time if you have a lot of letters to generate.

Click “Go to List of Letter Batches” to view the PDFs for the letters in this batch. Default date range is for the last month, but you can change the date range to search for older batches. Click the PDF icon for the batch and the letters display in PDF format. Click the red x to delete a batch.

<figure><img src="../../../.gitbook/assets/image (421).png" alt=""><figcaption></figcaption></figure>
