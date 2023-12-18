---
description: This document is a guide for creating Miscellaneous A/R Invoices and Credits.
---

# Misc. Invoicing

{% hint style="info" %}
See A/R Invoices for [Prerequisite Setup ](../#pre-requisite-setup)for Miscellaneous Invoices.
{% endhint %}

## **Enter/Edit Invoice**

Naviga Ad allows users to enter or edit invoices in the system and will allow user to pdf the invoice and post it to the A/R system.

{% hint style="info" %}
Note that once the invoice has been posted to A/R, the invoice cannot be edited. The system will allow user to view the invoice details still, if user enters the invoice ID.
{% endhint %}

Navigate to the Accounts Receivable module -> Invoicing menu -> Misc. Invoicing -> Enter/Edit Invoices.

<figure><img src="../../../../.gitbook/assets/MiscInvoice.gif" alt=""><figcaption></figcaption></figure>

Search for an existing invoice by clicking the magnifying glass or click the + sign to add new invoice. Note that you can enter your own Invoice ID if you so choose, by entering the Invoice ID directly into the Invoice ID field and pressing the refresh arrow. Or you can allow the system to create a new ID by clicking the + sign to add a new invoice.

Click the drop-down to choose a Batch ID to add the invoice to an existing batch or click the + to create a new batch. Enter the relevant information for the batch such as the batch period, and mark as “Yes” For Delivery if you intend to send a PDF to the Customers. Note that this batch can be used for many invoices.

Enter the Invoice Description.

Click into the “Bill To” ID to find the Customer Account in your database, and the address information will be defaulted in the field. Note: beginning in 23.4 version, the customer's Bill-to Tax code is displayed in the header for informational purposes, so that the user entering invoice line items knows which tax rate to enter for that client.

Click the For Delivery field “Yes” to be able to generate a PDF and send to client after saving the invoice. Set it to "No" if you do not wish to send a PDF invoice.

{% hint style="info" %}
For Delivery, Invoice Date and Invoice Module and Period will default in from what was set on the batch. These can be overwritten for an individual invoice if necessary.
{% endhint %}

If you have setup User Defined Fields, enter the values as defined in the UDF section.

Enter the first few letters of the Product ID for the invoice and the Description will fill in automatically, but you can override or edit the Description.

Click the Add 1 line or choose Add 2 lines if you need to enter more lines to this invoice. Multiple Product IDs can be invoiced together.

Click the Save button. The system will display an invoice number as confirmation.

## Enter/Edit Credits <a href="#_toc112341271" id="_toc112341271"></a>

User can enter new or edit credit on an invoice to a customer. Navigate to the menu Invoicing -> A/R Invoice -> Enter/Edit Credits. Search for an existing credit using the magnifying glass or enter a new credit by using the + sign or entering a Credit ID manually.

Select the Batch from the batch dropdown or click the + for a new batch. Invoices and Credits can be entered in the same batch if desired.

Select the Bill-To ID for the customer to credit. At the bottom, you can enter the Product ID and details and save.

Note that user can credit this against a specific invoice by clicking the magnifying glass. Note that if the Credit is for a Misc. Invoice, the “Copy Lines” feature in \<Enter/Edit Credits> works if the Invoice to be credited was also created in \<A/R Invoicing>. This is because it requires a Product Code and will use the same to reverse.

## Generate PDF for Delivery <a href="#_toc112341269" id="_toc112341269"></a>

User can generate a PDF for these credits and invoices by navigating to the menu Invoicing -> A/R Invoicing -> Generate PDFs for Delivery node. Note that the invoice must be marked as “Yes” for “Delivery”. Click the magnifying glass to search for a batch. A list of batch ids with the details display. Check one or more boxes for the batches and click “Select Batches”.

![](<../../../../.gitbook/assets/12 (4)>)

Click the button “Generate invoices” at the bottom. A success message is displayed, and user is redirected to the print invoices screen.

Then proceed to the next node to Print Invoice(s) / Post to A/R. Find your Batch and click the little green down arrow.

![](<../../../../.gitbook/assets/13 (5)>)

User can now click the Batch No. hyperlink and view the individual invoice hyperlinks. Click the PDF button to view the PDF of the invoice and print it or email it as applicable.

<figure><img src="../../../../.gitbook/assets/image (431).png" alt=""><figcaption></figcaption></figure>

## Regenerate Invoices <a href="#_toc112341270" id="_toc112341270"></a>

User can regenerate invoices which user had entered into the system through the “Enter/Edit Invoice”. Navigate to the menu Invoicing -> A/R Invoicing -> Regenerate invoices and enter the invoice ids to be regenerated. If you would like to regenerate an entire batch, enter the Batch ID

Check the box corresponding to the invoices to be regenerated and then click “Regenerate Selected Invoices”.

<figure><img src="../../../../.gitbook/assets/image (452).png" alt=""><figcaption></figcaption></figure>
