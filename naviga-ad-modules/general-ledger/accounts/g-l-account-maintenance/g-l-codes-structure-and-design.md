# G/L Codes Structure and Design

The purpose of this document is to help new users to the system decide on the structure and design of the General Ledger Codes prior to installation and implementation of the Naviga Ad system. This setup is completed during the system initialization, so new clients must determine the structure before Naviga can complete setup and hand over the system.

{% hint style="warning" %}
Note that the code required is complex and if there is any change required later, it will involve Naviga programming and consequently cost to the client, so it is important to get this right up front.
{% endhint %}

## The Chart of Accounts <a href="#_toc31174684" id="_toc31174684"></a>

### Determining the Chart of Accounts Structure <a href="#_toc31174685" id="_toc31174685"></a>

The system allows a maximum of 30 numbers for an account code including an asterisk to separate each level. You can break the number into 5 or less levels. Below we will show you how most of our clients have set up their account structure. The system allows using a wildcard within a level, so you can perform sorting and ranges by sections of the level. For example, you may want your ABC Advertising Revenue code to be 01\*02\*01\*4100 which is a 13 characters code. You can use this as a guide to determine your Chart of Accounts structure:

1. Write your desired code structure using the characters X and \*, then number each level, as shown below:

XX\*XX\*XX\*XXXX

1 2 3 4 (level numbers)

1. Name each level:
   1. level 1(XX) = company (your main company will always be 01)
   2. level 2 (XX) = publication (one number for each publication)
   3. level 3 (XX) = department
   4. level 4 (XXXX) = account

Note that the system reserves level 1 for the company number, but all other levels can be defined as you wish. Your main company, or if you only have one company, will always be “01”. This field can be two or three digits in length (you will tell us prior to setup if you will require two characters or three).

It is recommended to set level 2 as the publication level. This separates all revenues and expenses by publication. At this level, you will have a “00” code for Balance Sheet accounts, and a “90” code for General & Administrative expense accounts. You can use numbers other than 00 and 90. This segment can be more characters than 2...2 is just an example.

1. Set up codes for each level. Before you set up each full account code, such as 01\*02\*01\*4100, you need to create a list of available codes for each level, except for the last level. This step of setting up level codes precedes setting up the full account codes. When the list of codes for each level has been established, you build each full account code by selecting one number from each level.

For example, to build the full account code above, select “01” from level 1 to indicate a Company 01 account, “02” from level 2 to indicate a AMC Publication account, and “01” from level 3 to indicate a Revenue account. The last level is manually entered for each full GL Account ID you set up, in this case “4100” to indicate that the Revenue type is Advertising.

When setting up the level codes, each will be assigned a description, but the description is only for reference purposes. For example, All codes at level 1 = 01 (Company 1), All codes at level 2 = 00 (balance sheet accounts) 01 (ABC Journal accounts) 02 (ABC Monthly accounts) 90 (G\&A accounts). Name each full account code later as you set them up by piecing together codes from each level.

1. Create each full account code by linking a code from each level. Create each G/L code as follows:
   1. Select a code from level 1
   2. Select a code from level 2
   3. Select a code from level 3
   4. Create a code for level 4 as part of the full GL Account ID.

Note to save your 9’s for a ‘dummy’ account (01\*99\*9999\*9999).

### Levels vs Account Codes <a href="#_toc31174686" id="_toc31174686"></a>

This is an example of setting up levels and how levels are used to set up account codes. In this example, our code structure is XX-XX-XX-XXXX, and it has 4 levels. In the Level Maintenance, setup all codes for the first 3 levels, and in the Chart of Account Maintenance create account codes.

![chart of accounts 1](<../../../../.gitbook/assets/1 (51).png>) ![chart of account levels](<../../../../.gitbook/assets/2 (37).png>)

This is an example of an account list for a very small company with only 2 publications. Match up the codes to the left to see how the accounts were created below.

![chart of accounts 3](<../../../../.gitbook/assets/3 (77).png>) ![chart of accounts 2](<../../../../.gitbook/assets/4 (36).png>)

### Examples of General Ledger Structures <a href="#_toc31174687" id="_toc31174687"></a>

In this example, the user is using most of the system modules, but they have assigned each level to have just one function.

Co Industry Product Department Account

XX XX XXXX XX XXXX

Another example is a user with one company and several publications. This structure and the second one will also work well with multiple legal entities. This could also be Co/Pub/Dept/Account.

Co Publication Account SubAccount

XX XX XXXX XXXX

### Import G/L Chart of Accounts <a href="#_toc31174688" id="_toc31174688"></a>

This tool allows you to import general ledger codes from a pre-existing tab delimited text file. The spreadsheet used in the import is provided in the software in the G/L module. For more details please refer to the [G/L Account Import](g-l-account-import.md)
