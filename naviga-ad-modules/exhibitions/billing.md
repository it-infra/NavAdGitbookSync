# Billing

## Exhibition Billing <a href="#_toc475530857" id="_toc475530857"></a>

After an order is confirmed and has a billing schedule, user can then navigate to the Exhibition module and click on the menu Billing -> Exhibition Billing.

<figure><img src="../../.gitbook/assets/image (673).png" alt=""><figcaption></figcaption></figure>

Choose the exhibition from the drop down menu and note that you can select more than one exhibition for which to generate the invoices.

In the field “Days in Advance”, you can leave blank to return orders which have a scheduled billing date of today (or sooner). Otherwise, if the scheduled billing is set for 7 days from today, then enter 7. This will return these orders due to be billed in a week.

Click on “Get Orders”. The orders will display with the details. Check the box for the orders you want to invoice and click on “Generate Invoices”.

Choose whether it is a trial run to view the invoice prior to generating the real invoice, or click on Live Run to generate the actual final invoice which the client will receive.

![](<../../.gitbook/assets/2 (26).png>)

Enter the financial period against which this invoice will be posted and the date to print on the invoice. You can choose the date to be different than the financial period range only of the security settings allow you to do so. Otherwise the date on invoice must be within that selected financial period.

Choose to enter comments or leave blank and then click on “Generate Invoices”.

Using the [HTML Invoice Forms](setup/exhibition-invoice-forms.md), the system will generate the invoice in PDF form. Client setup will determine if they are to get an emailed invoice (which the system will send out when the Live Run batch is generates), or a print invoice (which the billing user can print out after the batch is generated), or they can receive both a printed & emailed invoice.

![](<../../.gitbook/assets/3 (70).png>) ![](<../../.gitbook/assets/4 (20).png>)

This message will be displayed once the batches are created:

![](<../../.gitbook/assets/image (819).png>)

Click the View/Print Invoices not emailed to open the "Print" batch. Or click on the Go to list of Invoice Batches and you will see that the system created multiple batches depending upon the type of delivery. If you had all three options in the batch, then you will see three batches. User can open the pdf of the Print and Print & Email batches and print the batches for mailing.

## Separate Invoice <a href="#_toc79059419" id="_toc79059419"></a>

Some orders are created with the main exhibition space expense and then with service orders added to the exhibition order itself. The system allows you to setup the billing type for services to be separate from the main order itself and have its own invoice.

Exhibitions order entry screen, click the node Invoices / Payments and the system shows the separately billed invoices if the services are setup for separate billing type.

As a prerequisite, navigate to the Setup menu -> Services and add new services with separate billing type from the billing schedule of the order or exhibition.

![](<../../.gitbook/assets/5 (5).png>)

Then navigate to the menu Orders -> Enter a New Order. Add separate line item for the services which is marked as separate billing.

![](<../../.gitbook/assets/6 (49).png>)

Confirm the order and add a billing schedule. Navigate to the billing menu and bill the invoice. Note that the billing screens displays both line item and services as separate invoices.

![](<../../.gitbook/assets/7 (22).png>)

Check the boxes and generate the invoices as described in the billing section of this document.

Then navigate to the order to view the payments/ invoices node.

![](<../../.gitbook/assets/8 (43).png>)
