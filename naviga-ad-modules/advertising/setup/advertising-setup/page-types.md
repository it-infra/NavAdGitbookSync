# Page Types

Page types are for use with Preprints / Inserts when using the workflow introduced with 2023.6 Naviga Ad. These Page Types are used with [Size Codes](ad-sizes.md) flagged as "For Preprints" and [Ad Types](ad-types.md) flagged as "For Preprints"

Navigate to **Setup -> Advertising Setup -> Page Types**.  Setup one or more page types as needed for the types of inserts/preprints that you offer.  Page types will set defaults for weight and spoilage %. You may also have certain metadata questions that need to be answered and possibly passed on to the printer to allow them to print the insert properly.

<figure><img src="../../../../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

1. Click New to create a new Page Type
2. Enter a desired ID and Description for the Page Type
3. Optionally, select a default size code.  This can also be manually added / changed on an order
4. External ID - Optional - This doesn't have a function inside of Naviga Ad, but may be included on a feed to the printer.
5. Is Inactive - set this flag to yes if you no longer wish to use a Page Type

**Page Options** - Add as many lines as needed for the given page type.  Enter the page count for each line.  These will be the valid page counts allowed when booking an order.  For each number of pages, set the default weight and default spoilage percent.  These two can be overwritten in order entry if a given insert differs from the default.  Each line can also have an override External ID, or this can be left blank it is shares the same External ID as the Page Type itself.  This is optional and only used in external feeds.

**Custom Fields** - much like the metadata in classified order entry and custom forms setup elsewhere in the system, the custom fields tab on Page Type setup allows the system admin to set up certain questions that the order entry user can (or must) answer before saving the order.

<figure><img src="../../../../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>

* Enter a Label / Question &#x20;
* Select the prompt type from the dropdown
* If appropriate for the prompt type, enter validation information (used with single line text, multi-line text, and dropdown list)
* If available, based on the prompt type, select formatting from the dropdown (used on dates, date ranges, number and number ranges)
* check the required flag if the user is required to answer the question before saving the order.&#x20;
