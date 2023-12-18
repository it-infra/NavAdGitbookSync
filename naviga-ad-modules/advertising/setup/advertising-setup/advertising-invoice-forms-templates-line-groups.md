# Advertising Invoice Forms / Templates / Line Groups

## Prerequisites

* In Advertising Setup -> System Parameters, select the option #10, Use Naviga Forms = "Yes". In older versions of Naviga Ad there was an option to use a 3rd party form provider called Fabsoft. These instructions are to use the Naviga HTML forms instead of Fabsoft.
* In Setup -> System Tables Setup -> [Invoice Form Logos](../../../accounts-receivable-credit-control/setup-a-r-system-setup/system-tables-setup-a-r.md#invoice-form-logos) must be confugured before you can select the Default Logo on the template. Default logos can be overwitten on the Product Group or even on the customer account.
*   If applying grouping to the invoice details is desired, setup for Invoice Template Line Groups should be completed so that the ID's can be referenced in the Invoice HTML. These Groups will be linked to the Products that they apply to. Any products not set with a line group will be included in an "Other" group.

    <figure><img src="../../../../.gitbook/assets/image (408).png" alt=""><figcaption></figcaption></figure>

## Create Invoice Templates

Navigate to the Advertising module menu Setup -> Advertising Setup -> Advertising Invoice Forms.

<figure><img src="../../../../.gitbook/assets/image (1048).png" alt=""><figcaption></figcaption></figure>

You can create a new template by clicking the node “Create New”. Enter a title and description for the template. Select the Print orientation as Portrait or Landscape. Select Default Logo. If you would like the Page number and Invoice Number displayed in the footer, toggle the Yes/No flag to Yes. Ensure that the Active flag is set to "yes" to enable the template for use.

In the HTML tab, paste the provided sample templates and then edit the HTML to modify as needed. Click “Save” to save the template.

Below are sample templates for Performance and Flexible Campaign types.

{% file src="../../../../.gitbook/assets/PerformanceInvoiceSample.txt" %}

{% file src="../../../../.gitbook/assets/FlexibleInvoiceSample.txt" %}

{% hint style="info" %}
Note: the link at the top for paying the portal online is only applicable if you are licensed to use the Advertiser Portal.
{% endhint %}

#### Invoice Line Groups

In the sample HTML provided, you will find the following in the code:

<pre><code>&#x3C;!-- #LINES_PRINT_START# -->
<strong>&#x3C;!-- #LINES_PRINT_END# -->
</strong>
&#x3C;!-- #LINES_DIGITAL_START# -->
&#x3C;!-- #LINES_DIGITAL_END# -->
</code></pre>

The PRINT and DIGITAL must match what you set up in Invoice Template Line Groups for the ID's. If you used different ID's than was used in the example, just edit the code to match what you used.

#### Group by Package

Beginning in 2023.3, you can group invoices by package. To take advantage of this grouping, instead of the above HTML, you will use the following code lines at the beginning and end of the details:

```
<!-- #LINES_BY_PACKAGE_START# -->
    <!-- #PACKAGE_LINES_START# -->

    <!-- #PACKAGE_LINES_END# -->
<!-- #LINES_BY_PACKAGE_END# -->
```

Here are sample templates which use package grouping to use as a guide in setting this up:

{% file src="../../../../.gitbook/assets/Package_Performance_Invoice.txt" %}

{% file src="../../../../.gitbook/assets/Package_Flexible_Invoice.txt" %}

#### Include Ad Image on the Invoice

There are a couple of image related merge tags available on invoices.  The first will display a preview of the JPG preview image of the material.  The second is used in conjunction with the first for some formatting control.  Here are the new tags:

\#AD\_IMAGE#\
\#IMAGE\_TRUE\_WIDTH#\
\#IMAGE\_TRUE\_HEIGHT#

Here is an example of how it might be used - note that I placed it in my sample inside of the "Item" tag of my print lines line groups.\
![](<../../../../.gitbook/assets/image (19).png>)

This is a sample of how the above would display across a 2-page invoice:\
![](<../../../../.gitbook/assets/image (20).png>)



## Next steps

Once the invoice template has been created, then it needs to get linked somewhere to be available to use.

* Required: Invoice templates get linked to one or more [Product Groups](../product-setup/product-groups.md#invoicing).
* Optional: Invoice forms can also be used as an override form on an account. This is set at the account level ([Advertising node](../../customers/advertiser-maintenance.md#override-invoice-and-statement-form-settings))
* Optional: If you are an international media company and send invoices out in multiple languages, the correct form for each language is set up on the Product Group, and the Customer's preferred language is setup on the Account ([Name Maintenance](../../../accounts-receivable-credit-control/customers-a-r/#a-r-setup) -> A/R node)
