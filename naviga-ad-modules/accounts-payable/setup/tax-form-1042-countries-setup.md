# Tax Form 1042 Countries Setup

## Country List

This displays Tax Form 1042 Countries, with Country codes as defined by the IRS. To load the most current list of countries, click the button "Load from IRS" at the bottom of the screen. A warning will be displayed. Select OK on the warning and then, if desired, save the list of countries

<figure><img src="../../../.gitbook/assets/image (53) (1).png" alt=""><figcaption></figcaption></figure>

## 1042 Field Guide

### SAMPLE

#### Spooler-file output

![](<../../../.gitbook/assets/0 (111).png>)

This lists the boxes of the Form 1042 with a short description. The second column shows sample data that will be reported on this Form.

### Setup in G/L Module

Ensure the following fields are filled in from GL Module -> Setup -> Admin -> Company Setup

![](<../../../.gitbook/assets/1 (105).png>)

12A - U.S. Federal Tax ID

12B (and 12C if applicable) - CH3/CH4 Company Status Codes

12D, 12H, 12I - Company Name and Address settings for the 1099 are also used for the 1042

### Setup in A/P Module

#### A/P Module -> Vendors -> Vendor Maintenence

![](<../../../.gitbook/assets/2 (95).png>)

Tax Form Requirement – Yes/No for 1042 (or 1099, or other)

Chapter Selection: Chapter 3 / Chapter 4 gets saved on A/P Invoice Records as of create date

If “Chapter 4” is selected, both CH3 and CH4 data will be available; otherwise CH4 is greyed-out

3A (and 4A if applicable) - CH3/CH4 Exemption Codes get saved on A/P Invoice Records as of create date

3B (and 4B if applicable) – Tax Percent

13A – Tax Payer ID

13B (and 13C if applicable) – CH3/CH4 Vendor Status Codes

13D, 13F, 13G – Vendor Name and Address

13E – Country

A/P Module -> AP Invoice Detail

![](<../../../.gitbook/assets/3 (91).png>)

![](<../../../.gitbook/assets/4 (82).png>)

Tool to update a specific Invoice to add/change:

1. Income Type (“Tax Form Type Code”)
2. CH3/CH4 active at the time Invoice was paid
3. Exemption Codes active at the time Invoice was paid
4. Gross Income to report from this transaction
   1. Withholding Amount comes from the Payment transaction (not editable)
