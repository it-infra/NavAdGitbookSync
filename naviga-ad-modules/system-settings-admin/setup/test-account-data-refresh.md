# Test Account Data Refresh

This document explains how users can set the test account to refresh from the production/live system. This will not affect the existing data in the live data account, but it will override the data in the test account since it is replaced with the live system data (with the exception of the data defined below). Once selected, the data will refresh overnight during your regular nightly maintenance window. If your test and live accounts are not on the same software version, this process will replace the software version on test with the version that is currently on Live. So, if you plan to test a new software version, but with fresh data from Live, you should first copy over the data and then set the upgrade flag on the test account.

## Overview <a href="#_toc115691378" id="_toc115691378"></a>

To facilitate system and data testing you have access to both a production/live account and a test/sandbox account. We strongly recommend that any large changes or data imports are first implemented in the test system and verified prior to processing in the live account.

You can update the data in the test account by refreshing test from live. This will occur overnight during the system maintenance. The test system data will be completely erased and replaced with the data in your live system.

System maintenance starts after midnight in your server time zone, during the maintenance routine you will not be able to access your system. Maintenance runs on the live account first and an hour later maintenance runs on TEST, it is during this second process that the test refresh occurs.

## Test Account Refresh <a href="#_toc115691379" id="_toc115691379"></a>

{% hint style="info" %}
Schedule the refresh in your TEST account. It will use the data from the live account, but you should set the flag by logging into the test system and scheduling the refresh.
{% endhint %}

Navigate to the Systems Settings module in Naviga and click on the Setup menu -> Test Account Data Refresh.

![](<../../../.gitbook/assets/1 (80).png>)

In the option Test Account Set to Auto Refresh, you can click the “Yes” option. This means that the test account software version will be overwritten with the latest Live version during the maintenance time period mentioned above.

After it runs according to the nightly schedule, this flag will automatically set itself to “No” as the copy has occurred. To repeat the process, user must change this option back to “Yes” for the next refresh.

{% hint style="info" %}
Note that if left at “No” permanently, the environment gradually becomes out of date and irrelevant.
{% endhint %}

The next option “Email when Refresh is Completed” allows you to enter one or more email addresses of recipients you want to receive an email notification when the test account is refreshed successfully.

The next 3 fields are for information only and are automatically filled in after the refresh is complete.

Auto-Refresh Last Set by User: This is the user ID who set the auto refresh last.

Last Test Account Refresh Date / Time: This gives you the date and time stamps of when the test account was last refreshed.

Messages: This provides any messages from the system during the refresh process.

When finished, click on the “Save” button to store these settings.

## Items Not Overwritten <a href="#_toc115691380" id="_toc115691380"></a>

The following items will retain Their Original Values. They are client-facing fields and screens which are saved off before the refresh and then copied back into place after the refresh. Naviga Personnel - See Internal Documentation for back end/non-client-facing fields

<table><thead><tr><th width="271">Screen Name</th><th>Fields</th></tr></thead><tbody><tr><td>Naviga Parameters</td><td>ALL</td></tr><tr><td>Auto-Import A/R Payments</td><td>ALL</td></tr><tr><td>Phantom Scheduler Process Queue</td><td>ALL</td></tr><tr><td>Material Preflight settings</td><td>ALL</td></tr><tr><td>Salesforce Setup</td><td>ALL</td></tr><tr><td>Ad Server Setup</td><td>ALL</td></tr><tr><td>Advertising Setup</td><td>INVOICE SETTINGS --> OVERRIDE EMAIL TO ADDRESS</td></tr><tr><td>A/R System Parameters</td><td>INVOICE FORMS --> OVERRIDE EMAIL TO ADDRESS</td></tr></tbody></table>

### Naviga Parameters

Navigate to System Settings -> Setup -> Naviga Parameters

<figure><img src="../../../.gitbook/assets/image (1525).png" alt=""><figcaption></figcaption></figure>

### Auto-Import A/R Payments

Navigate to A/R Module -> Setup -> Auto Import of A/R Payments (both sub-menus)

![](<../../../.gitbook/assets/image (1004).png>) ![](<../../../.gitbook/assets/image (1014).png>)

### Phantom Scheduler Process Queue

Navigate to System Settings -> Setup -> Phantom Scheduler

<figure><img src="../../../.gitbook/assets/image (1060).png" alt=""><figcaption></figcaption></figure>

### Material Preflight settings

Prior to 2023.2, this was found on the Portal Setup, and only the Preflight section was saved off and then copied back in during a data refresh. It is now it's own screen and is used by both internal users and portal users, so this entire screen will be retained in a data refresh.

<figure><img src="../../../.gitbook/assets/image (1398).png" alt=""><figcaption></figcaption></figure>

### Salesforce Setup

In the Advertising Module, Navigate to Setup -> Admin -> Salesforce Integration Setup

<figure><img src="../../../.gitbook/assets/image (1484).png" alt=""><figcaption></figcaption></figure>

### Ad Server Setup

In the Advertising Module, Navigate to Setup -> Admin -> Ad Server Integration Setup

<figure><img src="../../../.gitbook/assets/image (1265).png" alt=""><figcaption></figcaption></figure>

### Advertising Setup

Navigate to Advertising Module -> Setup -> Admin -> System Parameters (Prior to 2023.1 this menu was found under Setup -> Advertising Setup -> System Parameters). This is a field that typically will be set to an internal address for testing, but you would not want to set that in a production environment or your clients wouldn't receive their invoices.

<figure><img src="../../../.gitbook/assets/image (1164).png" alt=""><figcaption></figcaption></figure>

### A/R System Parameters

Navigate to A/R Module -> Setup -> Admin -> A/R System Setup. Similar to above setting, but this would be for Misc A/R Invoices. Typically this is only set in a test environment.

<figure><img src="../../../.gitbook/assets/image (1481).png" alt=""><figcaption></figcaption></figure>
