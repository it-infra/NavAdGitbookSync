---
description: (4 Hours)
---

# Finance & Customer Tables

This session will focus on code tables that are used when setting up customers. Defaults can be applied when creating customers manually. These codes will be required in the customer import file. We will review the manual creation of customers and will discuss the required file format for importing customers.

* Payment Terms\
  Default payment terms can be applied to each customer, and these defaults may be overwritten at the campaign level. For example, Net 30, 2% 10 days.
* Currencies\
  The system will be set with a base/local currency. If you also sell in other currencies, you will need to set up each currency to be used in the system.
* Currency Tracking\
  This is an optional advanced feature that allows for more detailed foreign currency reporting. While the system always allows for reporting in local and foreign currencies, this feature allows for additional reporting currencies. For example, in a system where the local currency is US Dollars, and an order is entered in Euros, one could choose to report on that order in Sterling.
* Tax Codes\
  Tax codes are applied to each customer and flow automatically to all eligible purchases. This table is also available for use with accounts payable if implemented.
* Banks\
  At least one bank should be set up for cash receipts, additional bank records may be created to ease bank reconciliation. Default banks will be needed for the customer portal and should be considered if the portal will be implemented.
* Account Alerts\
  Alerts can be created to pop up when a customer record is accessed. These warnings are used when it is extremely important that users are aware of a special note about the customer.
* Client Types\
  If you wish to report on sales by different types of clients, or if you wish to have different default rates for different types of clients you can set up a list of client types. Client types can control ratecards, can be used to filter client searches and can be used to filter some reports. Client Types can be imported from existing systems during conversion and if you wish can be required when new accounts are created.
* Client Type Defaults Setup\
  System level defaults can be set to speed the creation of new clients and to enforce business rules. If you wish the system defaults can be overwritten for different client types. When creating a client, the system can append default terms, taxes, credit limits etc. based on client type. System security can control who can amend these defaults.
* Billing Groups\
  When running invoicing, one may filter by group of products or by product. One may also wish to filter billing by groups of clients. For example, some publishers bill private parties on a different schedule than corporate clients, or some clients may be billed weekly versus monthly. If you wish to bill different groups of clients in separate billing runs this allows you to create billing groups. Each client would then be assigned to a group to allow for filtered invoicing.
* Client Groups\
  For running statements and aging reports, clients can optionally be placed in client groups and the groups can be used to filter statement or aging.
* Name Reason Codes\
  When editing a name, the system tracks who made the change and when the change was made. If you wish you can supplement this audit trail by asking the user to select a reason for making the edit.
* Industry Codes\
  These codes are applied to each customer and from there default into each campaign. By identifying customers by their segment of your market you can create statistical reports and analyse your sales by customer line of business. The industry code is a required field in the customer import, at least one default code must be set up. Industry codes may also be used to determine GL codes by customer line of business if one wishes to post separately to the GL by industry. You may choose to use standard codes such as PIB, SIC, NAICS or you may create a custom list of codes.
* External System ID Codes\
  When integrating with external system, Naviga may need to store the client ID from the external system in order to interface data. One can create a table that identifies the external system to display where the external code is used. By using standard codes, it is easier to see which External ID goes with each system.
* Email Type Codes\
  It is possible to add multiple email addresses to names in the system. To better communicate to users, one may wish to assign email types to identify the intended use of each address. This field does not impact system logic.
* Personal Data Report Template\
  If data protection rules require that you notify customers of what information is stored against their names, these templates can be used to merge in data and provide to customers
* Customer User Defined Fields\
  The system allows you to set up custom fields for additional information. This set of fields allows for additional information stored on customers and visible when editing a name. There are also additional customer fields viewed from CRM and additional fields to store data on campaigns/orders.
* Account Maintenance
  * Name and Address Setup
  * Employees / Contacts & External Contacts
  * Addresses
  * Advertising Setup
  * A/R Setup
  * Stored Credit Cards
* Brand/Division Maintenance:
  * Billing Overrides
  * Default Salesperson
* Advertisers / Agencies Import\
  We will review several imports that can be used to populate the system with legacy data. This is the first import that would need to be completed prior to importing orders, invoices or payments. The import will create companies and individuals. The advertising import is used for most data, this import may be supplemented with the CRM import if desired.
* CRM Name Import\
  The Advertiser Import allows for import of companies or individuals; it may be used to import all names. The CRM import allows for more demographic information on individuals and may be preferable for importing contacts. Note that the “Salesperson ID” in the CRM import refers to the user ID of the CRM user for whom the name is being imported.
* Import Brands\
  In most implementations the brands are automatically created when importing campaigns. The default rep and default agency relationship are created from the relationships on the orders. If you have a source for the advertiser/agency and advertiser/rep relationships and wish to import them in a separate file you may use this import format. (Pre-requisite Salesrep Setup)
* Import Sales Rep Assignments\
  As an alternative the system provides a salesrep assignment import option. Once advertisers and brands have been created this optional import allows for default salesrep assignments. (Pre-requisite Salesrep and Brand Setup)
