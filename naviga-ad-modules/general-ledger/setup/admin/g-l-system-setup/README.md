# G/L System Setup

## Default Settings

<figure><img src="../../../../../.gitbook/assets/image (668).png" alt=""><figcaption></figcaption></figure>

1. Select the primary/default company from the list of configured system companies. This will be the default company for the general ledger module menus.
2. First Open Financial Period: This value is the first financial period open in the G/L module.
3. Last Open Financial Period: This value is the last open financial period in the G/L module.\
   (In addition to setting them here just for the G/L module, one can also use the Setup -> Admin -> Set Open Periods option to set periods across all modules.
4. Last Updated On: Automatic timestamp of when theses settings were last modified
5. Last Updated By: Automatic setting of who last modified these settings.
6. Multi-Company Balancing Requirements: See below...

## Multi-Company G/L Control Accounts

See [next section](multi-company-balancing-and-intercompany-control-accounts.md)

## Budget / Forecast Entry Restrictions

This menu restricts the changes in entry of budgets and forecasts to specific dates. Add more than one line as needed for each year. Each year has one line. This sets the last allowed date for updating the Budget, Forecast 1, and Forecast 2.

<figure><img src="../../../../../.gitbook/assets/image (320).png" alt=""><figcaption></figcaption></figure>

## Other G/L Parameters

<figure><img src="../../../../../.gitbook/assets/image (447).png" alt=""><figcaption></figcaption></figure>

1. Local Currency: This section is to set what the local currency is in the system.
2. Posting Interface Program: If there is a custom program used for posting, it is entered here. Contact Naviga administrator for this information. If you don't know what goes in here, it should probably be blank in your system.
3.  When posting from A/R, the company filter only applies to A/R codes: - When posting A/R Invoice transactions to the G/L (using Journal Entries -> Post Transactions to G/L by Module), there is a filter for company (shown below). Depending upon the transaction and your setup, there could be several companies involved in the revenue side of the transaction. If set to yes, this posting process will only look at the Receivable G/L Code to determine the company of the transaction.\\

    <figure><img src="../../../../../.gitbook/assets/image (1494).png" alt=""><figcaption></figcaption></figure>

## Child Account Integration Settings

<figure><img src="../../../../../.gitbook/assets/image (509).png" alt=""><figcaption></figcaption></figure>

This section will only be utilized when a system is using multiple Naviga Ad systems and consolidating to a single G/L. In 2022 Naviga Ad and Naviga Book split into two separate systems. Only a few clients were using both Ad and Book. The Naviga Ad digital first system becomes the system where the G/L lives and the Book system will be linked to it through these settings here to be able to consolidate G/L reporting. This linking can also link together separate Naviga Ad databases into a single G/L if, for example, you have a separate database for different divisions but wish to report the G/L together.
