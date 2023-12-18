# Naviga Parameters

This screen allows users to setup the web parameters. It contains different system settings.

## **General settings**

The server address specifies the URL where users log in to get into the Naviga server. This will be set for you by Naviga when your system is setup. There shouldn't be any need for you to modify what is here.

<figure><img src="../../../.gitbook/assets/image (1165).png" alt=""><figcaption></figcaption></figure>

## **A/R and Publisher Portal Settings**

A/R Portal Server Address: This URL is the location for your Naviga Advertiser Portal, if you are licensed for that module. This will be set for you by Naviga when your system is setup. There shouldn't be any need for you to modify what is here. (Publisher Portal will be blank in most new naviga ad installs)

<figure><img src="../../../.gitbook/assets/image (1299).png" alt=""><figcaption></figcaption></figure>

## **Informer Integration**

These are the settings for informer. This will be set for you by Naviga when your system is setup. There shouldn't be any need for you to modify what is here.

1. Informer is implemented: If checked as yes, then informer is activated.
2. External server address: URL for the informer application on an external server.
3. Internal server address: URL for the informer application on the internal system.

<figure><img src="../../../.gitbook/assets/image (972).png" alt=""><figcaption></figcaption></figure>

## **Search Settings**

These are search settings which define how the search results display.

1. Maximum number of results: This is the number of records user views when performing a search. 200 is the maximum the system will allow.
2. Show Client ID on Name Search Results: If marked as yes, the ID will come back with the name search of the client.
3. Show client Balance on Name Search Results: If marked as yes, then when user searches on the client name, the balance which the client has will also display.
4. Show Client Type on Name Search Results: If set to Yes, then the system defined advertiser type (such as Advertiser, Agency, etc) displays on search screen.
5. Show Advertiser Client Type on Name Search Results: If set to Yes, then the ID of the Advertiser Client Type will be displayed. The Advertiser Client Types are the ones that you define in the Ad Module Setup -> Client Type Setup.

<figure><img src="../../../.gitbook/assets/image (1028).png" alt=""><figcaption></figcaption></figure>

If all 4 are set to yes above, the search results when searching for a client will show the below columns:

<figure><img src="../../../.gitbook/assets/image (1492).png" alt=""><figcaption></figcaption></figure>

## **Address Settings**

There is an option in Parameters screen to set the system home country and to suppress the country in mailing addresses.

1. Home Country: Choose from the drop-down menu the home country of the user.
2. Suppress Country in Mailing Addresses: If this is checked, and if the country in the advertiser’s Account Maintenance menu -> Advertising Setup node -> “Bill-to-ID” field, who is receiving the invoice, is the same as the “Home Country” of the system, then the system will suppress printing of the country in the address for digital, exhibition and sponsorship invoice. Please note this only applies if you’re using the Naviga invoice forms.

## **Prefixes**

Enter any desired prefixes in the fields below for these various items

<figure><img src="../../../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure>

## **Other Settings**

1. From Email Address for Password Changes: This is the email address which user will use to send an email to change the password.
2. Admin Groups: This group chosen from the drop-down menu is the administrative group, so all users in this group will have administrative rights within the menus they’re given access to in Menu and Module Security.

<figure><img src="../../../.gitbook/assets/image (1654).png" alt=""><figcaption></figcaption></figure>

## Email Messages from the system

You can customize the outgoing message when sending the following system generated emails

* Email Message when Adminstrator Requires Password Reset
* Email Message when User has Forgotten Password
* Email Message when Administrator has Setup New User

<figure><img src="../../../.gitbook/assets/image (1288).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1285).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note: be sure to include the #LINK# merge tag, otherwise the user will get a message but won't have the actual link to click on to do anything about it!
{% endhint %}
