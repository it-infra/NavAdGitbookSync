# Ratecards/Services/Adjustments

## Ratecard Setup

Ratecards are used to determine pricing for a space in an Exhibition order.

Navigate to the menu Setup -> Ratecard Setup. Choose the exhibition from the drop down menu and click “New” to create a new ratecard.

![](<../../../.gitbook/assets/0 (68).png>)

Note that if you have a previous exhibition from which you can copy a ratecard and then modify it, you can click the “Copy from Another Ratecard” button and choose the exhibition from which you want to copy.

### Pricing by Space ID <a href="#_toc9435429" id="_toc9435429"></a>

To use the “Pricing by Specific Space ID” pane, you have to have setup spaces in the menu Setup -> Space Setup as in the section above. Otherwise you will have no data display in this pane. Use this when each booth location, size, and cost has been pre-determined.

![](<../../../.gitbook/assets/1 (39).png>)

Choose the space ID from the drop down menu which will appear when you click in this box. Then enter the dimensions, space type, the number of open sides if any, points and price. The GL data will fill in by default. Click the + sign and save the ratecard.

### Unit Dimension Pricing <a href="#_toc9435430" id="_toc9435430"></a>

If you want to instead enter specific rates for a space type, use the “Unit/Space Dimension Pricing”, where you can enter an ID for the space, choose a space type from the available drop down menu, enter dimensions, description and a fixed price. Then click the + sign to add the line. To enter more, click on “Add a New Line” and repeat as needed. Use this when there are a fixed number of booth sizes available, and the booth cost for each size has been pre-determined.

![](<../../../.gitbook/assets/2 (62).png>)

### Variable/ Area Rate Pricing <a href="#_toc9435431" id="_toc9435431"></a>

Another option is the Variable / Area Rate Pricing pane - Use this when there are no pre-determined booth sizes. The size is determined at order entry, and the rate is calculated after the booth size is entered. For example, at a car show an exhibitor has a stand/area and they have a platform where a car is displayed, the car area is charged at a lower rate than the remaining area. Another example at an outside garden, an exhibitor has a tent area in the middle of the stand, which is sold at a different rate to the area surrounding it.

![](<../../../.gitbook/assets/3 (53).png>)

Enter an ID, description, choose a space type, a rate, a date when this option expires and the GL data will default in the fields. Then click on the + sign and repeat as needed.

Check the “Inactive” box, only to not allow rate card to be available for use in an order entry screen.

Currency Code is an optional field and should be left blank for the default currency. If a code is entered then this ratecard will be restricted to this currency code only.

Exhibitor Type is a field which can be left blank to allow use of all Exhibitor Types in conjunction with this ratecard. Or you can choose the exhibitor type and restrict this ratecard use in order entry only when the exhibitor’s type in the order matches the type on the ratecard.

When finished, click on the save button. Now the ratecard is ready for use in order entry against an exhibition.

## Services Setup <a href="#_toc9435432" id="_toc9435432"></a>

Use this menu to bill items other than for the actual booth sale, but note that these items need to be billed separately and not to be included as price adjustments on the order for the booth sale. This is a feature used in exhibitions if you are providing additional services particular to each exhibitor. For example, catering, additional labor and so forth.

This option is entered through a different pane on the order entry screen. There is also a report which displays only the services ordered for an exhibit.

Navigate to the menu Setup -> Services Setup. Choose the exhibition from the drop down menu and click on “Add a New Line”.

<figure><img src="../../../.gitbook/assets/image (809).png" alt=""><figcaption></figcaption></figure>

Enter the line number in which you want the service to appear on the list of services in order entry.

You can copy settings from another number if such exists to save yourself repetitive typing of data.

Enter a free form description of this service. For example, you can enter “Daily lunch catering”.

Choose the billing type, which can be upfront billing, separate billing with a separate invoice from the order, or billing according to the billing schedule already setup for the order or exhibition.

Allow Description Override if set to “Yes” will allow user in order entry to change the description of the service. This may be allowed to give order entry user freedom in accurately describing the service. If set to “No”, the user in the order entry screen will not be able to override entries.

Allow Rate Override if set to “Yes” will allow the user in the order entry screen to change the rate. If set to “No” then the user will not be able to change the rate.

Rate is the field where you enter the charge amount for this service.

In the GL Account ID field, start typing the description of the code, for example “serv” and all codes which have the letters serv in them will display. Choose the correct one. Or you can enter the code itself. The GL description will automatically default in its field.

Choose the currency only if it is not the local default currency. If you choose a different currency, this will limit the user in order entry to the order and rate card currency and may not display the services if they are entered in a different currency.

Choose the tax code from the drop down to apply only to the service charge.

Check the box for “Allow Rep Commission” if you wish the rep to be paid commission on this service. Leave unchecked if you do not want to include a commission for the rep for the extra service.

Check the box “Automatically Add to New Space Reservations” if this service is related to the booth order itself. This will automatically add this service in the order entry every time you reserve a space for an advertiser. Leave unchecked if it is a different service not related to the booth/ space reserved. This will not automatically add this service to the order whenever a space reservation is included, but will leave that to the order entry user to add if asked for by the advertiser. Note that these settings can be changed later, but the order will not automatically update its services to add or remove an existing line item. But user can edit the order to reflect the services changes in settings.

Check the flag "This is an insurance fee" if this is an insurance charge. If the client later provides prood of insurance, the charge can be reversed.

Click on the “add line” button and repeat adding new lines with other services with same or different parameters. When finished, click on the save button to save the services provided to this exhibition.

If there are other services from another exhibition you want to copy, you can use the option “Copy from Another Exhibition”. But if you do that, these copied entries will replace the ones you entered manually. Click on the save button when finished.

## Price Adjustments <a href="#_toc9435433" id="_toc9435433"></a>

This is a list of additional charges or discounts that can be applied to a booth order. Items billed separately should not be set up here. For example, you can have a discount for a support beam located in the booth area, and call it “beam discount”.

Navigate to the menu Setup -> Price Adjustments.

To set up a price adjustment, enter the Exhibition Id from the drop down menu to enter price adjustments. Note that the exhibition and ratecard must be set up first, then fill in the fields shown below.

![](<../../../.gitbook/assets/5 (69).png>)

Enter the sort order of this adjustment as you want it to appear in the order entry screen. You can always copy from another one if one exists by choosing it from the drop down of “Copy Settings from”.

Enter a free form description of this adjustment allowed in the exhibition order.

“Allow Description Override” if set to “Yes” will allow the order entry user to change the description you entered above. If set to “No”, then the description will be open for editing in the order entry screen.

If the adjustment is a discount be sure to enter a negative sign in front of the “+/- Value” field. You can also leave as “Can be negative or positive”. Price adjustments can be tracked separately in the General Ledger by entering different G/L codes for each type of adjustment.

Value Type can be area provided for the exhibitor, percentage or amount of money.

Prompt for Value Entry can be “No, Use a Fixed Price” which will prompt you to enter the amount in the following field or can be left to “Yes, Prompt for Value” which will force user in order entry screen to enter this value.

In the G/L Code you must enter a valid GL code. You can start typing the first few numbers or letters and the system will provide you a list to choose from to which to post these charges.

The ratecard field can be blank or you can choose a specific ratecard for this exhibition to attach the services to it. If attached to a certain ratecard, then this service will display only when user selects this specific ratecard in the order entry screen. If left unattached to a ratecard, then the user can select services from this setup for this exhibition regardless of the ratecard used in the order entry.

Check the box for “Allow Rep Commission” if you wish the rep to be paid commission on this service. Leave unchecked if you do not want to include a commission for the rep for the extra service.

Check the box “Space Related” if this service is related to the booth order itself. Leave unchecked if it is a different service not related to the booth/ space reserved.
