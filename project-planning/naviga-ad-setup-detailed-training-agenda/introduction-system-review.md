---
description: (2 hours)
---

# Introduction/System Review

## Initial Implementation Phone Meeting

To speed data entry, provide shortcuts, and enforce consistency and security, the Naviga Advertising system is designed with dropdown lists and defaults for most of the data fields in the system. Before using the software, there are several tables that will need to be populated. We will work with you to aid in making the business decisions necessary to ensure that the system best suits your needs.

This session lays the foundation for our setup meetings. We will provide a quick overview of the components in the software. We will then briefly highlight a common workflow to show how the parts of the software interact.

We are then going to spend some time focusing in more detail on some of the main system functions including entering a sample campaign.

The intent is not to train on these functions, we are using this as a basis for discussion of how you would like to set up your system. Most of the tables we need to set up are used in the tasks we will demonstrate. As we are presenting sample data, please think of what actual data would be useful for you.

Overview of what software is included in the system:

* Quick discussion of icons on login screen

Overview of common workflow:

* Customer creation
* Opportunity
* Proposal
* Customer Portal
* Integration to Naviga Plan
* Integration to GAM
* Invoicing
* Cash Receipts
* Credit and Collections
* GL Interface

More detailed view of system to help with other meetings to be held over the next few weeks:

* Proposal/Campaign Entry
  * Adding print display line items
  * Adding line items for website products
  * Adding line items for date-based products
  * Entering liner ads
  * Entering preprint/inserts
  * Estimates versus Actuals
* Production Workflow
* Invoicing
* Cash Receipts
* Credit & Collections
* Reports & Tools

Setup Screens:

* Overview
* Fields to be set up after today’s meeting

Before we can give you access to your system there is some setup that we will need to complete. These are items that are difficult to change once set up and they need to be confirmed before other setup can begin. We will need your input to ensure that we set up the system correctly:

* **Number of legal entities and their names**\
  Please provide a list of the legal entities that make up your organization. We will set up each legal entity using the name you provide. The software uses a two digit "company code" to identify each legal entity. This code is used as the first two digits of all GL codes for the legal entity. In organizations comprised of only one legal entity we automatically assign 01 as the company code and all GL codes would start with 01.
* **GL Code Structure**\
  Even if you are not using the Naviga GL, transactions will be posted to the Naviga GL. That posting process will create the export file to upload GL transactions to your external GL. Naviga expects that all GL codes will follow the same format. For example, if GL codes are 24 characters long, every code must contain exactly 24 characters. There are some system rules in Naviga regarding GL structure, and there is the ability to translate codes from Naviga to the external GL if they are set up differently. Early in the implementation you will need to assemble a list of all GL codes needed in the software. All that is required at this point is the format of the codes.
* **Fiscal year**\
  We will need two decisions regarding financial periods. What is the structure and what is the earliest period needed. What is your fiscal calendar? Do you follow a calendar year, if not what is your first period. Do periods follow a calendar number of days? Naviga can support calendar and non calendar fiscal years. We do not recommend non calendar fiscal months as integration with other systems such as GAM becomes complicated.
* **First Financial period**\
  What is the first fiscal period you would like set up in the software? If you are importing historical data, you will need financial periods as far back as the first transaction period in the import.
* **Account three letter acronym**\
  The URL to access the software will contain a unique three letter acronym to identify your instance of the software. There are some restrictions on what can be used, we will ask for your approval of available codes.
* **Structure for country codes**\
  The system validates address data against standard ISO codes. Do you wish us to validate country codes against the two-character country code e.g. US or against the three-digit country code e.g. USA. If we are interfacing customer data to external systems your interface would be simpler if we match the external system requirement. You may also wish to set codes to match your legacy system so that you do not need to translate the initial data import.

To ensure that the implementation is a success we need to know what our goal is in replacing your current software with Naviga. Our final request for this meeting is to agree on goals for the implementation so that we can measure our success during and post implementation.
