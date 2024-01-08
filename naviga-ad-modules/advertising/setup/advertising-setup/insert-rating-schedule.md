# Insert Rating Schedule

**Navigate to Setup -> Advertising -> Insert Rating Schedules**

This inserts workflow does not use the standard rate cards that other kinds of ads use.  This uses a rule-based engine that determines which price to use based on how closely it matches one of these definitions.  Insert Rating Schedules are used with [Size Codes](ad-sizes.md) flagged as "For Preprints" and [Ad Types](ad-types.md) flagged as "Is for Preprints"

Click New to create a new schedule and give it an ID and a Description. &#x20;

<figure><img src="../../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

After clicking "New" you can click the option to copy from another schedule if there is a similar schedule you wish to copy and edit rather than create the new one from scratch.

<figure><img src="../../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

There is an inactive flag as well in case you wish to no longer use it at some point in the future. &#x20;

#### In the Basic Settings section:

<figure><img src="../../../../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>

* Select the Price Type to be used.  Options include Quantity based CPM, Quantity Based, or Flat Rate. &#x20;
* Optional - Enter a Start Date and Valid through date to limit when this rate can be used.
* Priority Code - The appropriate schedule is chosen by the system based on the number of matching qualifiers.  For example, there might be multiple schedules that could potentially be used in order entry.  One schedule might match on just one qualifier, and another one might match several qualifiers. In the event that two rate schedules match on the same number of qualifiers, the priority code will determine which schedule to use.

#### Qualifiers

<figure><img src="../../../../.gitbook/assets/image (145).png" alt=""><figcaption></figcaption></figure>

There are currently 7 attributes or qualifiers that can be checked to determine which rate schedule to use.

1. **Specific Advertiser** - Select a specific advertiser if the advertiser has negotiated a custom price
2. **Page Types** - Select one or more relevant page types for this rating schedule
3. **Product Group** - If applicable select a product group that this rating schedule is valid for
4. **Product(s)** - Select one or more allowed products for this rating schedule
5. **Client Type** - Select a client type that is allowed to use this rate schedule
6. **Ad Type(s)** - Select one or more ad types that can use this rate schedule (Note these ad types are filtered to only ad types flagged with the "Is for Preprints" flag
7. **Matching Days of the week** - Select one or more days of the week which can use this rating schedule.

#### Price Escalations&#x20;

<figure><img src="../../../../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>

For each Rate Schedule, you can have one or more sets of prices that can be used, based on the number of pages (which also links to weight based on Page Type Setup) and number if inserts.  These prices will be flat prices, per insert prices, or per thousand prices based on the Price Type selected in the Basic Settings section. &#x20;

* Select Add New Escalation or click the pencil icon to edit an existing one
* Click the red x in the right column to delete an escalation
* Alternatively, Click copy escalations from another schedule to save some time and copy and edit from a similar schedule.
* Click Clear All Escalations to delete the escalation grid and start over.

<figure><img src="../../../../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>

Click Save to save the changes
