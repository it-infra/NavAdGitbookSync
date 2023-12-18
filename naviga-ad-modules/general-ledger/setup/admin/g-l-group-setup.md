# G/L Group Setup

This optional grouping mechanism allows user to create one or several groups of G/L codes which will then be available to allowed users as a filter on certain reports, like the Trial Balance and G/L Transaction reports.

<figure><img src="../../../../.gitbook/assets/image (1208).png" alt=""><figcaption></figcaption></figure>

To create a G/L code group, click the "new" button and give your group a name and an ID. Select one or several users who are allowed to use this group.

## G/L Account Selection Criteria

In the section at the bottom, enter the G/L codes or code ranges which will be part of this group.

* To select a specific Account, enter the "(From) G/L Account" and leave the "To G/L Account" blank
* To select a range of Accounts, enter both a "(From) G/L Account" and "To G/L Account". Range selection do not have to be existing Accounts, but must be a valid Account format.
* To enter a wildcard selection, use the ^ character, e.g. 01\*0000\*^ or 01\*0000\*^00^\*1000 or 01\*0000\*^\*1000

## G/L Account Selection

This read-only listing shows the G/L Accounts that will sum to this Detail Line, based on the G/L Account Selection Criteria entered on the first tab.

<figure><img src="../../../../.gitbook/assets/image (1296).png" alt=""><figcaption></figcaption></figure>

At the bottom, click Delete to remove G/L groups you no longer wish to use

Click save to save any changes

Click cancel to close the group that you are viewing without saving any changes.
