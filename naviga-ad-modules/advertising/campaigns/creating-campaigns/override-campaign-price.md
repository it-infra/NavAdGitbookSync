# Override Campaign Price

In 2023.5 we introduced a couple of new ways to override the price of a campaign (campaign must be in Quote or Reserved status).  You can click on the Gross Price link at the top of the Campaign lines screen or select one or more lines from the list of lines and then select Price Change - Bottom Line Override in the Line options dropdown:\


<figure><img src="../../../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

Window will open displaying the Current total and the new total as well as the selected line items (or all lines if user simply clicked on the Gross Amount link on the campaign.\


<figure><img src="../../../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

Enter desired campaign override price and click "Run Calculation" button:\


<figure><img src="../../../../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

Adjustments will be proportionately created for each line item.  If there are any existing bottom line overrides on the order already, it will automatically be removed and added back with the new price.  You can only have one bottom line override on an order line.

This new feature is meant to replace the earlier function to add a campaign header discount after lines were created and allow that to copy to the lines.  That earlier function wasn't designed to work with adjustments and so this method will correct that and properly work with adjustments.  Going forward, if a campaign level discount is added, it will only affect new lines added to the campaign.

Occasionally, there can be rounding issues, especially if multiple issues are on a line or multiple lines on a campaign, where the bottom line might be a penny or two off from the desired total.  When that happens, user can manually split the line to have one issue date on a line by itself and then adjust the bottom line on just that line to resolve.
