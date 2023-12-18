---
description: >-
  The purpose of this document is to provide users with details on how to setup
  trade contracts and orders.
---

# Trade Contracts

Users can create trade contracts that are 100% barter offering advertising for a service by an advertiser, involving no cash, and can be earned and spent accordingly. The contract can be applied to any ad campaign as an earned prepayment. User can record trade usage in the contract when the customer’s offered service is spent when utilized. It also is available with turning on the feature to accept Credit Memos as prepayment.

## Trade Types Setup <a href="#_toc31186429" id="_toc31186429"></a>

These values must be setup in the system as a prerequisite to the contract. Navigate to the menu Billing -> Trade -> Trade Type Setup.

Click the New button and enter the ID and description of the trade. This is the payment you’ll receive in return to your advertising service you provide your client.

The screen refreshes allowing you to choose your trade type which you just created. Once you choose it from the drop-down menu, the screen then displays a list of companies in the system each with a corresponding field for “Trade Usage G/L Account”. Enter a partial number or partial description of this account and the system displays a list of GL accounts matching the partial entry.

![](<../../../.gitbook/assets/1 (29).png>)

Choose the one you want to attach to the trade type you created for the company attached to the trade type and save.

## Trade Contract Setup <a href="#_toc31186430" id="_toc31186430"></a>

Create the contract with the advertiser by navigating to the menu Billing -> Trade -> Trade Contract Setup.

![](<../../../.gitbook/assets/2 (51).png>)

Choose the advertiser from the drop-down menu. Then click New next to the Contract ID field.

Enter the contract ID, and Description in each corresponding field. Click in the Trade Receivables G/L Account field and enter a partial value for the trade receivables GL account ID or description. A list displays from which you can choose the appropriate account.

Enter an expiration date for this contract after which it will not be available for use.

Scroll to the Trade Types shutter and in each line choose from the drop-down menu the trade types you will be attaching to the orders.

![](<../../../.gitbook/assets/3 (57).png>)

If you need more lines, click the + for the “Add 1 New Lines” to add more trade types. Enter a note of description, and the amount attached to this trade type when used.

When finished click the Save button.

Note that the Orders shutter will display the orders created in the system as Trade for this advertiser so that you can keep track of all orders attached to this contract.

Also note that trade contracts are only supported in the system's local currency. Therefore, on foreign currency orders, the dropdown on the payment screen with trade contracts listed will be blank.

## List of Trade Contracts <a href="#_toc31186431" id="_toc31186431"></a>

If you want a view of all trade contracts in the system, navigate to the menu Billing -> Trade -> List of Trade Contracts.

![](<../../../.gitbook/assets/4 (76).png>)

You can search on Client or Trade Type and choose the status to be current, expired or all contracts regarding of status. Click Get Data.

If you search by trade type only, the screen displays the Client ID and Client Name per contract. If you choose client name to search, the system displays the contracts for this client only.

![](<../../../.gitbook/assets/5 (66).png>)

If you choose both Client and Trade Type to search, the screen displays both the contract for the client you search for and other clients with contracts that include this trade type.

![](<../../../.gitbook/assets/6 (18).png>)

## Available Trade Usage Report <a href="#_toc31186432" id="_toc31186432"></a>

This report provides a list of contracts by client or trade type with usage amounts details. Navigate to the menu Billing -> Trade -> Available Trade Report.

![](<../../../.gitbook/assets/7 (7).png>)

Choose the client from the drop-down menu to search on usage for this client regardless of trade type and click “Get Data”. The screen displays the contract details including the usage so far for this client and the balance remaining on the contract.

If you search by both client ID and trade type, the system displays the contract line for this trade type for your client ID as well as other contracts under this trade type.

![](<../../../.gitbook/assets/8 (35).png>)

If you choose only the Trade Type to search for usage, the system displays the details by client for this trade type.

![](<../../../.gitbook/assets/9 (3).png>)

## Trade Order <a href="#_toc31186433" id="_toc31186433"></a>

Navigate to create a new campaign for this advertiser for which you will use a trade. Once the order has been confirmed, click the “Invoice and Payments” node on the campaign tree.

![](<../../../.gitbook/assets/10 (2).png>)

In the Pre-Payment Type drop-down, choose the option “Trade”. Then enter the deposit date if different from the one displayed. In the “COA/Credit/Trade Ref drop-down, choose the contract ID, and then enter the amount in the “Amount” field to match the trade value. Click the + sign to add the trade as a pre-payment for this order. Click the “Save” button.

Note that you can click the red x to un-attach the trade payment from this order.

If you navigate to the menu Billing -> Trade -> List of Trade Contracts and search on this advertiser, the system displays the applied amount of this trade and applied balance remaining.

![](<../../../.gitbook/assets/11 (12).png>)

Navigate to search on the contract under the menu Billing -> Trade -> Trade Contract Setup and note the applied values are reflected in the totals in the header.

![](<../../../.gitbook/assets/12 (21).png>)

Also, the order created and used for the trade is listed in the Orders shutter including the amount.

### Usage <a href="#_toc31186434" id="_toc31186434"></a>

At any time, you can increase the usage amounts in a contract for the lifetime of the contract. Navigate to the contract setup screen and click the “Add Usage” button corresponding to a trade type.

![](<../../../.gitbook/assets/13 (5).png>)

Add the trade usage G/L account associated with the added usage by typing a partial ID or text description of the account and choose the accurate one from the list. Choose the financial period to apply the usage, enter the amount of usage and choose the transaction type from the drop-down. This could be a usage or an adjustment of any value to the line. The usage will be subtracted from the line amount. Enter the date used from the calendar pop-up. Then enter an alphanumeric value for the used by field, used for field describing the purpose and then enter the person or persons entertained by this added usage. When finished click Add Line.

![](<../../../.gitbook/assets/14 (9).png>)

The Usage details are listed in the expansion arrow below the line where you performed the Add Usage function. Note the balance change according to the amount you added as well as the journal entry ID.

Note that the adjustment type of usage is also subtracted from the amount on this line, but no journal ID entry is created for it.

![](<../../../.gitbook/assets/15 (5).png>)

Note that the trade header reflects all Trade Used (Added Usage and Adjustments) amounts as well as trade balance as a result of the added usage. The trade value balance is not affected by the added usage and user can use up the balance to barter on orders with advertiser on this contract.

![](<../../../.gitbook/assets/16 (1).png>)

Generate an Invoice for this order in which you used the trade and the invoice shows $0 Payment Due since the prepayment is set on the order.

![](<../../../.gitbook/assets/17 (15).png>)
