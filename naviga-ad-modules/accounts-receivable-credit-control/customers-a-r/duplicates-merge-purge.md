# Duplicates / Merge / Purge

## Duplicate Checks

To prevent possible duplicated from happening in the first place, the system checks first for duplicates in the system when user enters an account including in the advertiser agency imports if the following conditions are satisfied:

* Name: First 6 characters of the account name in the application match the name which user is entering; and
* Address: First 5 characters of line 1 of the account address in the application match the address for this name; and
* Zip Code: First 5 characters of the account zip code in the application match the ones in being entered.

If these conditions are not met, the system checks for the following conditions to verify if the account is a duplicate of an account existing in the system:

* Address: First 5 characters of line 1 in the address on the account in the application match the entered corresponding characters; and
* Zip Code: First 5 characters of account in the application; and
* Phone Number: The full phone number of the account in the application.

## Duplicate Name Report

Navigate to Customers -> Duplicate Name Report

User can select various criteria upon which to search to find potential duplicates in the system

<figure><img src="../../../.gitbook/assets/image (1458).png" alt=""><figcaption></figcaption></figure>

Once presented with the list, the user can click on the accounts by account ID to research and determine if the account truly is a duplicate.

## Merge / Purge Names (Accounts)

This feature allows user to merge and purge advertisers’ accounts into existing accounts moving all the purged accounts’ details and merging them into an existing advertiser’s account. This is applicable if for true errors where a duplicate was inadvertantly created as well as when one client acquires another client and its products, where the acquiring company still needs to obtain all the records of the company being acquired, such as their invoices, orders, contacts, statements, documents, brands, credits, payments, transactions, cash on account, CRM Pending Actions, To-Do lists, notes, emails and all other information.

To perform the merge, click the menu Customers -> Merge/ Purge Names

<figure><img src="../../../.gitbook/assets/image (586).png" alt=""><figcaption></figcaption></figure>

In the Name/ Account to Merge To drop-down, choose the account to merge accounts into. This is the master account.

In the drop-down menu under “Names/ Accounts to Merge”, choose the account to be merged into the master account. Then click on the + sign. You can choose more than one merge account to be combined with one master account.

Check the box “Merge Brands/ Divisions” if you want the brands from the merged account to be dissolved into the master accounts. If both accounts have an A1 brand, then the merged A1 becomes the master account’s A1 taking on its name and ID. If this is left unchecked, then the merging brand will take on a new ID when merged into the master account and not affect the master account’s A1 brand.

The box “Set Merged Address as Inactive” can be checked if you no longer need this address to be there in the system for the merging company. If the merging company will still exist at that address, you can leave this unchecked. This is applicable in situations where there is an acquisition of the merging company by the master company but the merging company will continue to keep its address and operations.

Click on the button “Merge Accounts”. You will receive a successfully ran merge message.

### Testing Notes

Click on the menu Customers and click on the master account name. On the Accounting Tab, note that the invoices are all moved to the master account, in addition to all payments, card transactions and other items.

Click the CRM tab and note that all the merged accounts’ orders and brands are also displayed as part of the master account’s orders and brands. You can click the hyperlink to the order for further drill down.

The merged account is no longer valid in its name or details to be used in the system and has been absorbed by the master account.

## Delete Name

### Delete Company Account Name <a href="#_toc93343993" id="_toc93343993"></a>

User can delete a name of an individual contact or an advertising account company from the A/R menu Customers -> Delete Name. Enter the client ID or search using the magnifying glass.

![](<../../../.gitbook/assets/1 (92).png>)

The screen displays the analysis of how this name has been used in the system. The “Problem” column highlights whether there is a problem deleting the name or not depending on the usage of this name in the different modules. This applies only to the client advertising companies. If the company has been used in any of the modules, then the “Delete Name” button is greyed out and unavailable for use, so user cannot delete this company.

As an Alternative to deleting the name, user can:

* Remove the company from sales reps’ databases. To do so, open the customer overview screen, and click on the button “Remove from My Customers” by clicking the star.

![](<../../../.gitbook/assets/2 (48).png>)

* Or user can mark an account “Do Not Use” to deem it inactive. From the overview screen of the account, click on “Edit this Account” and “Go to Full Name Maintenance”. When the account displays, then click on the “Do Not Use” button to change it to “Yes”.

![](<../../../.gitbook/assets/3 (59).png>)

Click on the save button. This will remove use of the account throughout the system.

* The third alternative is to use the feature GDPR “The Right to be Forgotten”. For more details on this feature, please refer to the [GDPR Considerations](gdpr-considerations.md)

### Delete Individual Contact Name <a href="#_toc93343994" id="_toc93343994"></a>

In the Delete screen, search for the contact name. Even if the contact has a list of “To-Do-Actions”, or connected in orders, you can still delete the name.

![](<../../../.gitbook/assets/4 (48).png>)

Click on the button “Delete Name”. This removes the name from any association with the employer company.

Note that once this action is complete, the CRM actions tied to this contact are automatically removed from the system. The existing orders with this contact retain the client ID, but not the name.
