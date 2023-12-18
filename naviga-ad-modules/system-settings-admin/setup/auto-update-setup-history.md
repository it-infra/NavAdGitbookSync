# Auto-Update Setup/History

Admin users can deploy upgrades and patches to their software. The software patches can be deployed nightly, one time only or on a weekly schedule. Admin can also schedule a version upgrade up to the latest version. The deployments are performed automatically overnight to minimize disruption and require that all users be off the system at the time.

## User Setup Settings Prerequisite <a href="#_toc99973684" id="_toc99973684"></a>

The user performing this function must be setup as an administrator. The administrator can be a member of any group but their Administrator flag must be set to "Yes."

Navigate to the main menu and choose the System Settings module. Click the menu Setup -> User Administration. Edit the user who will be the administrator deploying patches by clicking on the pencil icon or create a new user.

![](<../../../.gitbook/assets/1 (12).png>)

Note that the Administrator field must be set to “Yes”. Save the settings.

## Setup Patches <a href="#_toc99973685" id="_toc99973685"></a>

Login as the new administrator user as setup above. Click the menu Setup -> Auto Update Setup/ History.

<figure><img src="../../../.gitbook/assets/image (1583).png" alt=""><figcaption></figcaption></figure>

Click the button “Change/ Cancel Auto-Update”.

![](<../../../.gitbook/assets/3 (24).png>)

You have the option to:

1. Enable Nightly Update: If you click this option, your system will receive nightly patches with all bug fixes and any new features patched back to your version of the software. We do not recommend using this setting in your live environment.
2. Enable Weekly Update: This option is the same as option 1 except that the patches will upload to your system once a week on the weekend. This is the setting you will typically use in Production.
3. Schedule One Time Update: When clicked, the system will automatically schedule an update of a patch only once that night.
4. Cancel/ Disable Auto-Update: This option will cancel any scheduled update and disable whatever setting you have in the system.

Once this step is complete, the patch scheduling is finished, and the system will follow the option you chose.

{% hint style="info" %}
If there is no available patch, then the process will not run. Also, there is a 30-day failsafe built in. If there are no patches processed after 30 days, the system will automatically patch. This is to ensure no customer falls too far behind the current fixes on a given version.
{% endhint %}

## Software Version Upgrade <a href="#_toc99973686" id="_toc99973686"></a>

If you want to upgrade the software version to a higher version than what you currently use, click the button “Schedule Auto-Upgrade”.

![](<../../../.gitbook/assets/4 (46).png>)

The system gives you the option to upgrade to all versions available which are higher than the one you have.

Click the button for the version you’d like to upgrade to, and if you choose a version which is several versions higher than your system, the system will automatically upgrade one at a time till it reaches the version you chose. This is the system’s way of ensuring that the software upgrades are done with all features available and with compatibility in mind.

## Taking Beta Versions

Your Current Status box will look like one of the following depending upon if your system is set as being allowed to install Beta versions.

![](<../../../.gitbook/assets/image (1502).png>) ![](<../../../.gitbook/assets/image (286).png>)

Only Naviga personnel can set your system as being allowed to take Beta versions. Typically, we will allow Beta versions to be installed only during implementation and not once you are live.

## Upgrade Log <a href="#_toc99973687" id="_toc99973687"></a>

On the auto upgrade menu screen, note that there is a log provided for each patch or upgrade performed.

![](<../../../.gitbook/assets/5 (33).png>)

The update history provides you with a hyperlink to the Log ID in order to view details. The log indicates the date and time of the latest upgrade, the process type being a patch or upgrade, the release number of the patch or upgrade and a check box indicating whether the upgrade was successfully or not.

If the upgrade failed, then the box is unchecked, and the system will automatically revert to your current version until all issues are resolved.

If there is no available patch, then the process will not run. Also, there is a 30-day failsafe built in. If there are no patches processed after 30 days, the system will automatically patch. This is to ensure no customer falls too far behind the current fixes on a given version.

{% hint style="info" %}
We won't automatically UPGRADE your system, but we will automatically PATCH your current release. That said, you do want to remain somewhat current on version releases, especially if you are using 3rd party integrations like GAM. GAM depricates their older versions frequently, so to remain compatible with GAM, you do need to stay current. Also, Naviga's ability to patch bug fixes back to earlier versions is limited, for fixes to take effect you will need to remain current. Enhancements are only ever delivered in upgrades, to benefit from new programming you will need to upgrade your system.
{% endhint %}
