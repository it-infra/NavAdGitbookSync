# Metadata Adjustments

Classified Metadata Adjustments allow for multiple adjustments to be applied to the whole order, first or last insertion based on data qualifiers which user can setup.

Some examples of when you might want to use metadata adjustments:

* Instead of creating a product for Legacy.com you chose to add a metadata prompt for it and will send this ad to Legacy if the metadata choice is "Yes." The fee for this is $X or a Y% Premium over the cost of the print line.
* Instead of having a template specific to having a image, you chose to allow an image in any template, and to charge a fee if an image is present.

**Prerequisite for this is to have some Adjustment codes created on the Product and/or Product Group.**

Navigate to the menu Setup -> Classified Order Setup -> Classified Category Tree Setup.

Click the Metadata Adjustments node and choose the Category Tree, Metadata Field which you’d like to apply these qualifiers for, and the Product to which you’d like to apply the adjustments and qualifiers.

{% hint style="info" %}
Note: Metadata Adjustments by Product or Metadata Adjustments by Group both behave similarly. One is set up at the product level with Product Price Adjustments and the other is set up at the Product Group level with Group Price Adjustments.
{% endhint %}

In the Auto Adjustments section, choose the qualifier to be either “Not Blank”. Choose the Adjustment from the drop-down menu and then choose the application rule to be “Apply to All Insertions”. These conditions mean that when user is entering a classified order where the Metadata field chosen in this product, and the field is not blank in value, the system applies this adjustment you chose to all insertions of the order. Save the settings.

<figure><img src="../../../../.gitbook/assets/image (1001).png" alt=""><figcaption></figcaption></figure>

You can choose another condition on this Metadata Field or another field where the qualifier is “A Specific Value” and then enter this Specific Value in the field titled as such. Choose the Adjustment to apply when this field contains this value and then choose the rule to “Apply to First Insertion”. The system in the line entry will then apply this adjustment to only the first insertion of the line item and not any others.

Here is an example when the metadata is a drop-down:

<figure><img src="../../../../.gitbook/assets/image (461).png" alt=""><figcaption></figcaption></figure>

Here is an example when the metadata is a True/False:

<figure><img src="../../../../.gitbook/assets/image (903).png" alt=""><figcaption></figcaption></figure>

You can repeat the condition above for the same Metadata Field or another one and “Apply to Last Insertion”. This applies this adjustment to only the last insertion in the line item and no others.

Proceed to create a classified ad using a classified package with the Metadata Adjustments above. When you arrive at the field you chose, enter a value that satisfies the rule that has been set up for the adjustment.

Press the tab button through Adjustments.

Note that the system automatically applied the adjustment and listed the conditions for it. Tab through the “Price & Book” tab and view the auto-adjusted price.
