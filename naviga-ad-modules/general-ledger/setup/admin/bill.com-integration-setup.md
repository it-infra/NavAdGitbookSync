# Bill.com Integration Setup

Bill.com is a 3rd party software solutions for A/P Invoices and Payments management. This integration pulls Bills, Credits and Payments from Bill.com and imports them into the system as Journal Entries, with allocation detail for each transaction line item.

## Integration Settings

<figure><img src="../../../../.gitbook/assets/image (1386).png" alt=""><figcaption></figcaption></figure>

1. Click Yes to enable the Bill.com integration
2. Click Yes to use the settings (below) for Production environment. If set to NO, all calls will be made to the Staging settings.
3. Enter A/P account ID to be used when importing A/P credits and Payments
4. Enter A/P Foreign Exchange G/L Account
5. This is list of Approval Codes from bill.com that should be considered as APPROVED and imported in. Leave this blank to always import these items regardless of Approval Status.
6. This is list of Approval Codes from bill.com that should be considered as APPROVED and imported in. Leave this blank to always import these items regardless of Approval Status.
7. This is a comma separated list of IDs to ignore when pulling data from bill.com.

## Staging Environment Parameters

Enter appropriate settings below as provided by your Bill.com administrator.

<figure><img src="../../../../.gitbook/assets/image (1174).png" alt=""><figcaption></figcaption></figure>

## Production Environment Parameters

Same settings as above, but for the Bill.com production environment
