# Security

The security menu includes Module Security, Menu Security, Group Security, User Security and User Administration. When creating a user, the user will be assigned to a Group. The group they are part of will determine their Module, Menu and Group Security Settings. User Security is individualized for each user.

<table data-view="cards"><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td></td><td><a href="module-menu-security.md#_toc79061545-1">Module Security</a></td><td></td></tr><tr><td></td><td><a href="module-menu-security.md#_toc79061546">Menu Security</a></td><td></td></tr><tr><td></td><td><a href="group-security.md">Group Security</a></td><td></td></tr><tr><td></td><td><a href="user-admin-security.md">User Administration</a></td><td></td></tr><tr><td></td><td><a href="user-admin-security.md#_toc79061550">User Security</a></td><td></td></tr></tbody></table>

## Login Authentication

The two-factor Authentication is available. If enabled, when user logs in the system checks user’s IP Address against a list of IP Address that have been authenticated for the user account. If the IP Address has not been authorized before, the system will send an email to the email address on the user’s account with a code. The Login screen will show a popup asking that user enters this code to authorize access. Once complete, user is good to go. Next time if the same user logs in from another IP or if the internet service provider changes the IP, user will have to go through the process again.

It must be enabled on the account in System Settings by Naviga Support or an Implementation Specialist. If this is enabled, when user views the list of Users in User Administration, user will see a new column of the Authorized IP Addresses for Active Users.

User then can try to login. And user will receive this message for the first time to check their email address and enter the code in the email into the authentication message.

<figure><img src="../../../.gitbook/assets/image (1391).png" alt=""><figcaption></figcaption></figure>

\
Enter the code and you will receive the message in your email: ![](<../../../.gitbook/assets/image (1268).png>)

Once you enter the code and login, you will receive a confirmation email. ![](<../../../.gitbook/assets/image (254).png>)

## Password Lockout <a href="#_toc124155840" id="_toc124155840"></a>

Fields regarding password lockout conditions are available to address user being locked out of the system due to invalid password. These fields are present in the System Admin screens to be handled by Naviga Support team only. The settings include:

1. Should Failed Lockout be enabled
2. If the above is yes, how many failed attempts are allowed before the user is locked out
3. What is the lockout duration (in minutes)

## Strict Page Security

There is a setting we can set for you in the background that will check the user's security on each page load to ensure they have access to a given page. Let Naviga Support or Implementation know if you require that to be set. This prevents a user from bypassing the menu security by clicking a link or editing the URL directly to get to a page they shouldn't be able to access.
