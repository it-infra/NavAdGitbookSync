# A/P Advance Payments

An advance payment for a vendor happens when a user pays partial or in full an amount prior to receiving the invoice from the vendor. It is more common in the Book Publishing world than in Advertising, but sometimes payment in advance is necessary.

## Advance Payment Setup <a href="#_toc31642349" id="_toc31642349"></a>

Navigate to the menu **Payments -> A/P Advance Payments**

![](<../../../.gitbook/assets/1 (1) (1).png>)

1. Select the bank from the drop-down menu.
2. Enter the check number in the Check No. field and press enter.
3. Select the vendor in the Vendor ID drop-down field
4. enter a comment as needed in the Comment field
5. select the financial period and date in the respective fields.
6. Enter the advance payment amount
7. choose the tax from the drop-down field for Tax.
8. Enter a partial ID or description of the G/L account to which you attach this payment in the G/L Account field and then enter the amount to be posted to this G/L account. This amount must match the check amount at the top
9. In the Attachments section, you can choose to enter a image or document by entering a description of the attachment, then press the “Select File” button to upload the attachment. Click the + sign when done. You can repeat this step several times as needed to add more attachments.
10. When finished, click the Apply button. This saves the record in the system.

{% hint style="info" %}
Note that the system does not create a Check or Electronic payment for the Advance Payment, because the payment is assumed to have been manually generated.
{% endhint %}

## Applying an Advance Payment to an Invoice <a href="#_toc31642350" id="_toc31642350"></a>

When entering a Vendor invoice, you can now apply the Advance Payment to the invoice. Click the menu **Invoices -> A/P Invoice Entry**.

![](<../../../.gitbook/assets/2 (1) (1).png>)

Choose the vendor in the Vendor ID field, then click in the Invoice ID field to choose the invoice to which you can apply the advance payment. In the “Advance Payment to Apply” field, choose the Advance Payment you created in the previous segment of this document. Fill the remaining fields as needed and save the invoice.

### Posting Invoice Batch to A/P <a href="#_toc31642351" id="_toc31642351"></a>

The actual process of matching the invoice and payment takes place when you Post the invoice Batch to A/P. Note that if the payment record has already been posted to the G/L then the system will auto generate a journal entry that Credits the original G/L allocation on the payment and Debits Accounts Payable.

If there is a remaining balance on the invoice after the Advance has been applied, then that balance will be available for payment in **Payments -> Pay A/P Invoices**.
