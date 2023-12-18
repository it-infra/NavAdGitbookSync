# Category Tree / Categories

## Category Tree Setup <a href="#_toc116920282" id="_toc116920282"></a>

This section must be setup first to allow for the choices in the “Classified Categories” in the Product Setup screen.

In the menu Setup -> Classified Order Setup -> Classified Category Tree Setup you can create a high-level tree design which you can use across different products.

<figure><img src="../../../../.gitbook/assets/image (1059).png" alt=""><figcaption></figcaption></figure>

For example, you can use the same category tree for similar industry serving publications.

Click the + sign to create a new category tree and a enter the category name and ID.

<figure><img src="../../../../.gitbook/assets/image (356).png" alt=""><figcaption></figcaption></figure>

* If you will book orders to the highest level of the tree, select Yes to Allow Orders.
* If this category will require Affidavits to be sent (for example "Legals Notices") select "yes" for Allow Affidavits.
* If using the Classified Self service portal and you will allow clients to book orders to this category, select "Yes" to Allow Online.
* If you no longer wish to book orders to this Category Tree, click "Yes" to Is Inactive.

Click Save

## Categories

Once the Tree is created, next create categories belonging to this tree by clicking "Add New Category." In the example above, Automotive is the Tree, and Cars, Trucks and Automotive Services are the Categories.

This category window allows you to establish the hierarchy for the Categories and Sub-categories. If the entry is the top level, leave the Parent field blank. Otherwise, choose an item from the drop down to identify the Parent of the sub-category. See below screenshots of the parent "Automotive" and the subcategory "Cars":

![](<../../../../.gitbook/assets/image (473).png>) ![](<../../../../.gitbook/assets/image (1409).png>)

The parent catefory has optional Online Options that can be filled in. That is for Classified Self Service Portal usage only.

At this time, leave the Classified Stylesheet tab blank.

### Category Metadata

In the category metadata node, you can customize the design of this category. These are the fields displaying in the line item entry for users to supply the details when user selects this Category or Sub-category. Note: the metadata is inherited. For example, all the metadata questions for Automotive would apply to the sub-categories of Cars. Additionally, you can create specific metadata questions for either Cars or Trucks. The questions presented to the user are additive – they would see all generic Automotive questions + the specific ones for Cars, for instance.

<figure><img src="../../../../.gitbook/assets/image (546).png" alt=""><figcaption></figcaption></figure>

You can define the fields by adding their labels and determine if they are required fields by checking the required box. You can also define the field to be a line, image, date, etc. You can determine if validation is allowed such as for valid email addresses. You can also determine the drop-down selections to be multi-selects. Continue to add as many lines as needed.

Continue to add sub-categories as needed and they inherit the metadata design of the parent category.

The parent metadata are not editable for the child category, but the child specific fields as you scroll down in the child metadata node are editable and customizable.

The metadata can be any of the following:

* Image - This will allow the user to upload an image to be used in the ad. Enter the max size in KB in the first box, enter the allowed file types in the second box (separated by a comma and no space). If this is going to be an attention getter image, select the Image folder from the dropdown. If the user will be uploading an image, this can be blank. For internal users, the attention getter folder will just be the default, and they can select a different folder. For Self Service users, they will only see the default images displayed.\
  ![](<../../../../.gitbook/assets/image (357).png>)
* File/Document - Will provide an upload prompt to add a document to an order. It is similar to an image upload, but this would typically be to add a pdf, word doc, or something like that. Not typically used in the body of the ad.\
  <img src="../../../../.gitbook/assets/image (951).png" alt="" data-size="original">
* Single Line Text - will display a string field for the user to enter data. This prompt includes validation options in the validation dropdown. In the Validation column you also can enter the maximum # of characters if desired.\
  ![](<../../../../.gitbook/assets/image (243).png>)
* Multi Line Text - this displays a text box for the user. Typically would be used to enter the body text of the ad. In the Validation column you can enter the maximum # of characters if desired.
* HTML Tags - Somewhat unusual, but in come cases, the desire was to have users enter some simple HTML and use that for the online feed. This option presents the user with a code box and a preview\
  ![](<../../../../.gitbook/assets/image (974).png>)
* Date - The user will be presented with a calendar to select a date. The are formatting options available here.\
  ![](<../../../../.gitbook/assets/image (457).png>)
* Date Range - The user will be presented with a from date and a to date calendar to enter in a date range. Same formatting options as above
* Number - This will only allow for numers to be added. This has formatting options available as well as min and max allowed values.\
  ![](<../../../../.gitbook/assets/image (172).png>)
* Number Range - Same options as above Number, but this would have two fields indicating a beginning and end of the number range.
* Dropdown List Selection - This will present users with a dropdown of pre-filled options. It can be a multi-select if multi-select is checked in Validation. User can enter custom text instead of picking one of the provided options if Allow custom Text is checked. The options in the dropdown shoulsd be entered here with commas separating choices without spaces.\
  ![](<../../../../.gitbook/assets/image (1154).png>)
* True/False - This will present the user with a Yes/No button to select.
* Color Code - This will present the user with a color wheel to select the color.\
  ![](<../../../../.gitbook/assets/image (865).png>)

{% hint style="info" %}
Note - If color code choices are too many options, consider using the Dropdown list Selection and only present the colors you wish to offer. Then use the HTML Template to dictate what that color choice means. For example, you might offer a yellow highlight that is Yellow #ffff33. The user simply selects "Yellow" in the dropdown and the HTML template for the ad understands what that actually means.

\
Also Note: There is an option below the prompt type. This is only relevant if you are using Classified Self-Service module. There might be some metadata questions that are only for internal use and shouldn't be displayed to a client using the customer self-service portal. If that is the case for any metadata question, change the choice to "Hide in Seld-Service." The default is to Allow in Self-Service.
{% endhint %}

Validations and Formatting options that depend on the Prompt Type that is chosen. Not all prompt types have these.

The Merge Tag is used by Templates that automatically create the classified ads. Not all Prompt Type items will appear in print. If a Template does not include a Merge Tag, it won’t be in the print version. But it can still be included in the online version if it is scheduled for an online product.

Note that when you click the Classified Categories screen, you can at any time click the “Delete” button which deletes the category and all its properties. This can only be done if there are no orders against the category.

Click the node for Category Tree node and choose one from the drop-down menu. Click the “Delete” button and the system gives you a warning message that this cannot be undone. Click OK. If there are orders using this category, the system alerts you that the operation cannot be completed. The category is not removed.
