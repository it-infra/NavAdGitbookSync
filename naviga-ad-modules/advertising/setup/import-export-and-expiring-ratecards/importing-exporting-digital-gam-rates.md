# Importing / Exporting Digital GAM Rates

In version 2023.5, so many new fields were added to the Ratecard Import/Export to accommodate GAM targeting, that I thought it warranted its own page here in the documentation to describe everything that's going on here.

It will be much easier on first creation to use the GUI to make these selections, and then export it to really be able to look at it with your own data and understand how this all needs to be formatted. Several of these items are quite detailed multi-valued and sub-valued fields and just are not that easy to display in an excel spreadsheet format.

* **Multi-valued fields are simply separated with a comma**
* **If a value within a field, has multiple parts to it, those pipe | delimited.**
* **If anything within a pipe has multi-values, those are semi-colon delimited.**

#### Here are some examples:

Multiple placements are selected on a rate:\
![](<../../../../.gitbook/assets/image (15).png>)

The above in excel would be represented as follows - these are the ID's of these placements as found in Ad Server Integration Setup\
![](<../../../../.gitbook/assets/image (14).png>)

Slightly more complex, these creative sizes have multiple parts to it. The master size, the companion size and the count. (Please note that Targeting Rules on creatives, AMP Flag, Frequency Caps, and Native Media Orientation on expected creative sizes are not supported in the Import/Export.)

Items with multiple parts are pipe separated: \\

<figure><img src="../../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

ID's are also used here, so this is what the above would look like in excel:\
![](<../../../../.gitbook/assets/image (12).png>)

Now if the above had multiple rows or multiple companion sizes on any one row, then this gets even more complex:\\

<figure><img src="../../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

The above would be represented by the below in Excel:

<figure><img src="../../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

The first 4 is the Master, between the pipes is the list of companions separated by semi-colons, and the 3 is the count. Then after the comma is the second row with 7 being the master, 8, 9, and 10 between the pipes being the companions, and then the creative count is 1.

If it was a creative type without a master, then the first character will be the pipe. Google puts the standard creatives as companions and has no master on those.

Now that you understand the formatting rules, below are the new fields in the ratecard export/import. All fields are optional, but if used, anything that is an ID must represent a value already in the database. The ID's can be looked up most easily from the Ad Server Integration setup.

### Additional Template Fields supporting GAM Targeting:

<table data-full-width="true"><thead><tr><th width="256">Additional columns added</th><th width="188">Example</th><th width="449">Data Source</th><th>Mandatory/ Optional</th></tr></thead><tbody><tr><td>Grace Days</td><td>3</td><td>numeric field from 0-7; See field 1 in below diagram</td><td>Optional</td></tr><tr><td>Max Impressions</td><td>20,000</td><td>numeric field (no decimal); see field 2 in below diagram</td><td>Optional</td></tr><tr><td>Ad Server Override Qty</td><td>20,000</td><td>numeric field (no decimal); see field 3 in below diagram</td><td>Optional</td></tr><tr><td>Ad Server Description</td><td>Test123</td><td>This alpha-numeric field overrides the description for the line item in the Ad Server. See field 4 in below diagram</td><td>Optional</td></tr><tr><td>Target Platform</td><td>BROWSER</td><td>See field 5 in below diagram. Valid entries are:<br>BROWSER MOBILE_APP VIDEO_PLAYER</td><td>Optional</td></tr><tr><td>Default Goal Percent</td><td>50</td><td>Numeric field (no decimal) between 0 and 100 representing the goal % on a sponsorship type campaign. See field 6 in below diagram. This field will be hidden if the Google line type (related to the ad type) is "standard"</td><td>Optional</td></tr><tr><td>Goal Type Limit</td><td>NONE</td><td>Not in diagram below, but will appear where Field 6 is only if ad type has GAM Line Type of Click Tracking or Price Priority. Valid options here are:<br>NONE<br>LIFETIME<br>DAILY</td><td>Optional</td></tr><tr><td>Delivery Priority</td><td>4</td><td>Numeric field. Number ranges from 2 - 16, and valid numbers will depend upon the Google Line Type. See field 8 in below diagram and additional details below the diagrams</td><td>Optional</td></tr><tr><td>Delivery Method</td><td>E</td><td>Alpha code field. Options as follows:<br>E = Deliver Evenly<br>F=Frontloaded Delivery<br>A=As Fast As Possible<br>See field 9 in Diagrams below</td><td>Optional</td></tr><tr><td>Max Duration</td><td>30</td><td>Numeric field. This will only display when the Creative Type is Video. See field 10 in Diagrams below.</td><td>Optional</td></tr><tr><td>Allow Same Advertiser</td><td>TRUE</td><td>Valid options are TRUE or FALSE or Y/N. See field 11 in Diagrams below</td><td>Optional</td></tr><tr><td>Display Creatives</td><td>ONLY_ONE</td><td>Valid Options are:<br>ONLY_ONE, ONE_OR_MORE, ALL_ROADBLOCK, AS_MANY_AS_POSSIBLE, CREATIVE_SET<br>See field 12 in diagrams below. Only relevant to Standard and Video Creative types</td><td>Optional</td></tr><tr><td>Rotate Creatives</td><td>EVEN</td><td>Valid Options are:<br>EVEN, OPTIMIZED, MANUAL, or SEQUENTIAL<br>See field 13 in diagrams below</td><td>Optional</td></tr><tr><td>Creative Type</td><td>S</td><td>Valid Options are:<br>S=Standard<br>V=Video<br>M=Master/Companion<br>See field 14 in Diagrams below</td><td>Optional</td></tr><tr><td>Display Companions</td><td>OPTIONAL</td><td>Valid Options are:<br>OPTIONAL<br>AT_LEAST_ONE<br>ALL<br>UNKNOWN<br>See field 15 in Diagrams below</td><td>Optional</td></tr><tr><td>Included Ad Units</td><td>87642399,<br>87642519*21732251258,<br>21698962035</td><td>Numeric field representing the ad unit ID from GAM. This can be found in Naviga Ad in the ID column in Ad Units node of Ad Server Integration setup. Multiple ad units are separated by commas. A Child AdUnit will be represented with an asterisk between the parent and child. See field 16 in Diagrams below</td><td>Optional</td></tr><tr><td>Excluded Ad Units</td><td>21740211698,233044272,21740211440</td><td>Numeric field representing the ad unit ID from GAM. This can be found in Naviga Ad in the ID column in Ad Units node of Ad Server Integration setup. See field 17 in Diagrams below</td><td>Optional</td></tr><tr><td>Placements</td><td>79362,1301472</td><td>Numeric field representing the placement ID from GAM. Multiples are separated by commas.<br>See field 18 in Diagrams below</td><td>Optional</td></tr><tr><td>Expected Sizes</td><td>With master:<br>4|2|3<br>or without master:<br>|2|3<br></td><td>Alpha-numeric field representing the ID's of sizes. Multiple rows of data are separated by commas, multiple items within a row are separate by a pipe | character. Only fields supported here are the Master, the Companion and the Count. If there is no master the first field is blank and the companion and the count will be displayed<br>See field 19 in Diagrams below</td><td>Optional</td></tr><tr><td>Labels</td><td>380075467</td><td>Numeric field representing the labels selected. These are the ID's of the label, which can be seen in Ad Server Integration setup<br>See field 20 in Diagrams below</td><td>Optional</td></tr><tr><td>Geographies</td><td>21171|I,21164|I,21167|I,1025197|E,200698|E</td><td>Each Geo location in GAM is represented by a numeric ID. That is used in the first position, then a pipe, followed by an I for Include, or an E for Exclude. Multiples are separated by commas.<br>See field 21 in Diagrams below</td><td>Optional</td></tr><tr><td>Custom Targeting</td><td>292392|IS|447697811592;447697811832;447697812072;447697812312</td><td>Numeric field representing ID's of the Custom Key-value pairs. The Key is in the first position, followed by pipe, followed by IS or IS_NOT, followed by another pipe and then the value(s). Values are semi-colon separated. Multiple key-value pairs would be comma separated. See field 22 in Diagrams below</td><td>Optional</td></tr><tr><td>Day Parts</td><td>Sunday|Saturday|8:30 AM|6:00 PM</td><td>Days of weeks and times of days. Multiple data points in the same row are pipe delimited as in the example. Multiple rows of data will be comma delimited. See field 23 in Diagrams below</td><td>Optional</td></tr><tr><td>Frequency Caps</td><td><p>MINUTE|45|2,</p><p>WEEK|1|100</p></td><td>Multiple data points in the same row are pipe delimited, multiple rows are comma separated as in the example. Cap Type (Days, Weeks etc.) are in the first position, then the "per" number in the second position and the quantity in the third. See field 24 in Diagrams below. Valid Cap Types are as follows:<br>MINUTE<br>HOUR<br>DAY<br>WEEK<br>MONTH<br>LIFETIME<br>POD<br>STREAM<br>UNKNOWN</td><td>Optional</td></tr><tr><td>Browsers Type</td><td>I or E</td><td>This indicates if the list of "Browsers" are Include or Exclude.</td><td>Optional</td></tr><tr><td>Browsers</td><td>500072</td><td>Used in conjunction with the above setting. This is the numeric ID for the selected browser. Multiples are comma separated. See field 26 in Diagrams below</td><td>Optional</td></tr><tr><td>Operating Systems Type</td><td>I or E</td><td>This indicates if the list of "Operating Systems" are Include or Exclude.</td><td>Optional</td></tr><tr><td>Operating Systems</td><td>501006</td><td>Used in conjunction with the above setting. This is the numeric ID for the selected operating systems. Multiples are comma separated. See field 28 in Diagrams below</td><td>Optional</td></tr><tr><td>Device Capabilities Type</td><td>I or E</td><td>This indicates if the list of "Device Capabilities" are Include or Exclude.</td><td>Optional</td></tr><tr><td>Device Capabilities</td><td>5000</td><td>Used in conjunction with the above setting. This is the numeric ID for the selected Device Capabilities. Multiples are comma separated. See field 30 in Diagrams below</td><td>Optional</td></tr><tr><td>Device Manufacturers Type</td><td>I or E</td><td>This indicates if the list of "Device Manufacturers" are Include or Exclude.</td><td>Optional</td></tr><tr><td>Device Manufacturers</td><td>40210,40212,40213</td><td>Used in conjunction with the above setting. This is the numeric ID for the selected Device Manufacturers. Multiples are comma separated. See field 32 in Diagrams below</td><td>Optional</td></tr><tr><td>Bandwidths Type</td><td>I or E</td><td>This indicates if the list of "Bandwidths" are Include or Exclude.</td><td>Optional</td></tr><tr><td>Bandwidths</td><td>4,5,6</td><td>Used in conjunction with the above setting. This is the numeric ID for the selected Bandwidths. Multiples are comma separated. See field 34 in Diagrams below</td><td>Optional</td></tr><tr><td>Mobile Carriers Type</td><td>I or E</td><td>This indicates if the list of "Mobile Carriers" are Include or Exclude.</td><td>Optional</td></tr><tr><td>Mobile Carriers</td><td>71230,70090,70092</td><td>Used in conjunction with the above setting. This is the numeric ID for the selected Mobile Carriers. Multiples are comma separated. See field 36 in Diagrams below</td><td>Optional</td></tr><tr><td>Languages Type</td><td>I or E</td><td>This indicates if the list of "Languages" are Include or Exclude.</td><td>Optional</td></tr><tr><td>Languages</td><td>EN</td><td>Used in conjunction with the above setting. This is the 2-digit Alpha code for the selected Language. Multiples are comma separated. See field 38 in Diagrams below</td><td>Optional</td></tr><tr><td>Domains Type</td><td>I or E</td><td>This indicates if the list of "Domains" are Include or Exclude.</td><td>Optional</td></tr><tr><td>Domains</td><td>navigaglobal.com</td><td>Used in conjunction with the above setting. This is the Alpha numeric domains to Include or Exclude. Multiples are comma separated. See field 40 in Diagrams below</td><td>Optional</td></tr><tr><td>Device Categories Type</td><td>I or E</td><td>This indicates if the list of "Device Categories" are Include or Exclude.</td><td>Optional</td></tr><tr><td>Device Categories</td><td>30000,30002</td><td>Used in conjunction with the above setting. This is the numeric ID for the selected device categories. Multiples are comma separated. See field 42 in Diagrams below</td><td>Optional</td></tr><tr><td>Custom Fields (UDF's)</td><td>INET.LINE*<em>TEXT*</em>1|,INET.LINE*<em>NUMERIC*</em>1|1000000,INET.LINE*<em>DATE*</em>1|10/31/2028,INET.LINE*<em>PICKLIST*</em>1|R;M<br></td><td>Multiple data points in the same row are pipe delimited, multiple rows are comma separated as in the example. Multiple choices of the same item are semi-colon separated.<br>See more details below with more detailed explanation.</td><td></td></tr></tbody></table>

<figure><img src="../../../../.gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

**Additional details on Delivery Priority** - if ad type's Google Ad Manager Line Type is set as follows, then the numbers set in this field mean the following

<figure><img src="../../../../.gitbook/assets/image (6) (2).png" alt=""><figcaption></figcaption></figure>

### **Additional Details on Custom Fields (UDF's)**

The example provided for UDF's looks like this:\
INET.LINE\*\_TEXT\*\_1|,INET.LINE\*\_NUMERIC\*\_1|1000000,INET.LINE\*\_DATE\*\_1|10/31/2028,INET.LINE\*\_PICKLIST\*\_1|R;M\
Let's break that down line by line. Remember, each line is separated with a comma. So this item contains 4 lines:

1 - INET.LINE\*\_TEXT\*\_1|\
2 - INET.LINE\*\_NUMERIC\*\_1|1000000\
3 - INET.LINE\*\_DATE\*\_1|10/31/2028\
4 - INET.LINE\*\_PICKLIST\*\_1|R;M\\

The above 4 lines correspond to these UDF's:\
![](<../../../../.gitbook/assets/image (5) (2).png>)

UDF setup for these items is below:

1 - **INET.LINE\*TEXT\*1|** tells us the this is the Field ID #1 of the Text type UDF's

On the rate setup (above) this UDF is blank, so the line for this in the import has the pipe, but nothing after it.\\

<figure><img src="../../../../.gitbook/assets/image (4) (2).png" alt=""><figcaption></figcaption></figure>

2 - **INET.LINE\***_**NUMERIC\***_**1|1000000** tells us that this is Field ID #1 of the Numeric type UDF's\
On the rate setup above, this UDF is 1000000, so that is what is set after the pipe character\\

<figure><img src="../../../../.gitbook/assets/image (3) (2).png" alt=""><figcaption></figcaption></figure>

3 - **INET.LINE\***_**DATE\***_**1|10/31/2028** tells us that this is Field #1 of the Date type UDF's\
On the rate setup above, the UDF is set to 10/31/2028, so that is what is after the pipe\\

<figure><img src="../../../../.gitbook/assets/image (2) (2).png" alt=""><figcaption></figcaption></figure>

\
4 - **INET.LINE\***_**PICKLIST\***_**1|R;M** tells us this is field #1 in the Multi-select fields. With multi-select fields multiple answers are separated with semi-colons. The preset fields on this ratecard example have answers of the Value R and M\\

<figure><img src="../../../../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
