# Module / Menu Security

## Pre-requisite <a href="#_toc79061545" id="_toc79061545"></a>

Groups need to be established prior to setting up the module and menu security. You don't need to assign all the Group Security functions yet, but you do need to create the groups.

{% hint style="info" %}
Do not remove any groups that come with the system. ROOT group is for Naviga Personnel only. Do not attempt to modify or delete. You will not be able to assign any users to the ROOT Group.
{% endhint %}

## Module Security <a href="#_toc79061545" id="_toc79061545"></a>

1. In System, navigate to the Systems Settings module -> Security menu -> Module Security.
2. In the drop down of Security Group, choose a group to setup.
3. Check one or more modules to which this group of users should have access. For example, Credit and Collections, CRM, Advertising, and so forth. Then click Save.
4. Repeat for all groups that you have created in Group Security

{% hint style="info" %}
Note: you can select the tab "Users in Group" to see a list of users who are in the selected group and will receive the modules selected in Module Security
{% endhint %}

The modules you see in this list will be determined by the modules you are contracted for. (See Security -> License Information)

<img src="../../../.gitbook/assets/image (372).png" alt="" data-size="original">

## Menu Security <a href="#_toc79061546" id="_toc79061546"></a>

1. Navigate to the Systems Settings module -> Security -> Menu Security.
2. Choose the security group from the drop down menu and then choose the module to setup for this group.
3. Check the corresponding box to each main menu item to display for this security group for that module.
4. The “All Other Menu Options” section can be left blank and this will default the security group to access all the sub menus corresponding to the main menu items checked above.
   1. If this security group is to be limited to a specific set of sub menu items, then click the drop down menu drop down “Disallow or Allow” and choose Allow the Following Processes. Then scroll to the bottom of the page, choose the sub menu from the “Add Menu Item” and click Add. Repeat the process as needed.
   2. If the security group is to be allowed all sub menu items except for a small subset of sub menus, click on the drop down “Disallow or Allow” and choose Disallow the following Processes. Then scroll to the bottom of the page, choose the sub menu from the “Add Menu Item” and click Add. Repeat the process as needed.
   3. If all sub menus are allowed or disallowed, click the drop down menu drop down “Disallow or Allow” and choose Allow or disallow and click on Add All. You can check and uncheck the respective boxes to allow or disallow the menu options from displaying on the security group’s users’ screens. Click the Save button.
   4. If the user is not allowed to use a menu item, but it is desired to show the menu and sub menus display in a disabled mode, check the box “Show Disabled Menu Items”.

<figure><img src="../../../.gitbook/assets/image (1039).png" alt=""><figcaption></figcaption></figure>

Menu security can be copied from one group to another for ease of setup when Groups are similar, but have just a few differences.

Click the View Menu Audit to view a summary of the Menus that they will have available.
