---
description: >-
  This was a new feature in 2023.5. It crosses multiple modules, so I am
  documenting it here in A/R, but will reference it in other related areas of
  the system.
---

# ACH Payment Processing

Depending upon your payment processor, ACH may now be supported for payment processing in Naviga Ad, both for internal users, and for Advertiser Portal Users (Note - Classified Self-Service is still currently credit card only, but may be considered for a future release).  The processors which currently support ACH transaction processing with Naviga Pay are **Authorize.net, Braintree, ImpressPay (aka FluidPay or AMR), and Edgil Payway**. Stripe is in the works with the NavigaPay dev team and will be coming early 2024.

## Internal Experience&#x20;

### Process Payment Screen

This screen is displayed in Campaign Payment Entry and A/R Invoice Payments. If ACH is enabled for your bank, you will see the "ACH" option in the dropdown for payment type.  The below screen is displayed if the user enters a payment by navigating to any of the following:&#x20;

* A/R module -> Payments -> Pay an Invoice
* A/R module -> Payments -> Prepay an Order
* Advertising module -> Campaigns -> Edit a Campaign, Invoices & Payments node

<figure><img src="../../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

ACH will only be displayed if at least one bank is setup to support ACH, and only those banks supporting ACH will be displayed in the bank dropdown.  Labels have been changed onscreen to be applicable to both ACH and Credit cards.  So "Credit Card to Charge" has been relabeled "Account to Charge."  "Card Number" is now "Account Number", etc.

{% hint style="info" %}
Note - if you do not see ACH as an option in the dropdown, check Advertising Group Security.  There is a setting there to limit the payment types that are available to a user. If you previously set limitations, you will need to also select ACH to allow that to be selected. \
![](<../../../.gitbook/assets/image (38).png>)\
\
If you still do not see ACH as an option, there is a new flag in bank setup where you can force ACH to appear as an option - but only use that flag if you are using one of the above listed processors.  You wouldn't want users to see ACH in the dropdown if it isn't going to be functional for them.\
![](<../../../.gitbook/assets/image (39).png>)
{% endhint %}

The popup displayed when user clicks "new" to add a new account will differ slightly depending upon the processor being used, but typically, the Account number, Routing Number, and Account type will be displayed -

<figure><img src="../../../.gitbook/assets/image (40).png" alt="" width="375"><figcaption></figcaption></figure>

This will be saved as an account on file and will behave much like a credit card in that the masked account number can be viewed and selected to be used for transactions.

{% hint style="info" %}
Important note for Auth.net users - when the processor is in testing mode, ACH transactions will fail if the amount is > $100, so be sure to use small amounts if in test mode.  See [https://developer.authorize.net/hello\_world/testing\_guide.html](https://developer.authorize.net/hello\_world/testing\_guide.html) for Authorize.net testing guide.
{% endhint %}

### Auto-Pay on Campaign

Similar function, but slightly different user experience, on the Campaign Header, if there is an account on file, a bank account now can be selected as an AutoPay method from the Auto Pay Dropdown:

<figure><img src="../../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

The auto pay function is not new, but having Bank Accounts available in that list is new.  Previously, only credit cards were in that dropdown.  Whatever account is selected in the dropdown will be used to pay the invoice during the invoice creation process.

### Auto-Clear Processing

And finally, one additional place that ACH is now supported is in the monthly Auto-Clear processing.

<figure><img src="../../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

Navigate to **Customers -> Advertiser/Agency Maintenance** in Advertising Module or **Customers -> Name Maintenance** in the A/R Module and select the A/R Setup node.  The Auto-clear balance dropdown will now contain both card numbers and bank account numbers for selection for the monthly charge.

{% hint style="warning" %}
NOTE: For those who are electing to license Naviga Ad's Variable Payment by Payment Type module, if you are charging processing fees for Card transactions (or ACH Transactions) the Auto-clear process will now also charge those fees for these transactions.
{% endhint %}
