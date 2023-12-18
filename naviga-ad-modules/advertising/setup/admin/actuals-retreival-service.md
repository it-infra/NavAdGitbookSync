# Actuals Retreival Service

Naviga Implementation resources will help get this set up during your project.

Actuals Retrieval system is available on Ad for the automated retrieval and parsing of the 3rd and 4th party actuals. The data is then moved to the parsed folder. This process is designed to expedite the actuals retrieval and minimize manual efforts of reading and analyzing every email sent by 3rd Party actuals measuring tools.

Navigate to the menu Setup -> Admin -> Actuals Retrieval Service -> Actuals Retrieval Setup.

![](<../../../../.gitbook/assets/20 (7).png>)

Choose the connection to use from the drop-down menu, and then choose the folder which would be monitored because it is receiving the emails from the actuals’ service. Enter the name of the folder to which to move the processed items. See next section on how to create a connection.

Add a line and enter the “From email address” which is the email of the sender of the actuals. You may choose more than one sender and add additional lines as needed by clicking the + sign at the bottom next to add new lines. Be sure to select the correct Attachment Format so that Naviga Ad understands how to parse the data and move it into the chosen folder. Naviga Programming would be required if additional formats are needed. Current support is for DCM/DFA, Sizmek, and Moat.

To create a connection, navigate to the menu Setup -> Admin -> Actuals Retrieval Service -> oAuth Connection Manager.

Click “New” to create the new connection and its configuration, such as the description, the type being google mail, the email address, and client ID. Then click on “Authorize” which will start the process.

This is the connection used to monitor the 3rd and 4th party actuals arriving into the emails.

{% hint style="info" %}
Note that the actuals must have the same 3rd and 4th party IDs on the campaign line items.
{% endhint %}

zz
