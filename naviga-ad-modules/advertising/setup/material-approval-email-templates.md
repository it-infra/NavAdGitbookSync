# Material Approval Email Templates

Material Approval Templates allow for notification to clients and/or internal users to be notified when a material has been created. They can click on links in the email to go into the Advertiser Portal to approve the ad.

<figure><img src="../../../.gitbook/assets/image (670).png" alt=""><figcaption></figcaption></figure>

* Navigate to Setup -> Material Approval Email Templates
* Select "Create New"
* Give your template a Name and if desired, a description
* This template will be e-mailed, so be sure to enter a Subject Line for the email. If no subject is entered the default subject line is "Material Project 11529 has been completed" (with the actual Material ID in place of those numbers)
* Select desired orientation as Portrait or Landscape
* Select "Active" as true to enable it to be used.
* Use the design or html tabs at the bottom, enter your marketing text and/or images
* Click "View Merge Fields Documentaiton" to see all available merge fields.
* Click Save

See [Product Setup ](product-setup/products/material-handling.md#artist-workflow-integration)for where to link these templates.

Here is a sample internal email to start with...be sure to update URL's with the site-specific URL for your Naviga Ad system.

<pre data-overflow="wrap"><code>&#x3C;p>&#x3C;span style="font-size: 14px;">Hi there.&#x26;nbsp; We have built an ad for #ADVERTISERNAME# that we think is really great.&#x26;nbsp; Please review and send to them for approval if you agree!
&#x26;nbsp;&#x3C;/span>&#x3C;/p>
&#x3C;div style="width:100%;box-sizing: border-box; padding: 10px; background-color: #f1f1f1;">&#x3C;span style="font-size: 14px;">
#APPROVALCOMMENT#
&#x3C;/span>&#x3C;/div>
&#x3C;br />
&#x3C;br />
&#x3C;img alt="" src="#PREVIEWIMAGEURL#" style="max-width: 400px; max-height: 400px;" />
&#x3C;br />
If you are having trouble viewing the above image, you may click &#x3C;a href="#PREVIEWIMAGEURL#">here &#x3C;/a>to view in a browser window.
&#x3C;br />
Click&#x3C;a href="<a data-footnote-ref href="#user-content-fn-1">https://XXX.navigahub.com/EW/XXX/ad/pw/material.aspx?ID=#MATERIALID#</a>"> here &#x3C;/a> to review this material.  If you approve, please mark the Approval Status to Pending Customer Approval or Customer Approved if you do not wish to send to the customer.
&#x3C;p>&#x26;nbsp;&#x3C;/p>
</code></pre>

Here is a sample client-facing email to start with....

<pre data-overflow="wrap"><code>&#x3C;div style="margin:10px;  width: 700px; font: 14px arial, sans-serif;line-height:150%;">
&#x3C;div style="background-color: #B8B7B5; width: 100%; padding: 10px; box-sizing: border-box;">
&#x3C;img alt="" src="<a data-footnote-ref href="#user-content-fn-2">https://pages.navigaglobal.com/rs/531-ETU-453/images/NavigaColorLogo.png</a>" style="height: 40px; display: inline-block; outline: none; border-width: 0px;" />
&#x3C;/div>
&#x3C;span style="font-size: 14px;">We have created an amazing ad for you - please agree and approve!
&#x3C;/span>
&#x3C;div style="width:100%;box-sizing: border-box; padding: 10px; background-color: #f1f1f1;">&#x3C;span style="font-size: 14px;">
#APPROVALCOMMENT#
&#x3C;/span>&#x3C;/div>
&#x3C;span style="font-size: 14px;">
&#x3C;br />
&#x3C;img alt="" src="#PREVIEWIMAGEURL#" style="max-width: 400px; max-height: 400px;" />
&#x3C;br />
If you are having trouble viewing the above image, you may click
&#x3C;a href="#PREVIEWIMAGEURL#"> here &#x3C;/a>to view in a browser window.
&#x3C;br />
&#x3C;br />
If you have access to our portal, you may click &#x3C;a href=<a data-footnote-ref href="#user-content-fn-3">"https://XXX.navigahub.com/Portal/Client/XXX/login.aspx?ReturnUrl=%2fportal%2fclient%2fXXX%2fdefault%2fmaterials%2fpending"></a> here &#x3C;/a> to approve or reject this online.  If you do not have portal access, please &#x3C;a href="mailto:<a data-footnote-ref href="#user-content-fn-4">someone@example.com</a>">email us&#x3C;/a> and we can set you up with a portal account.&#x3C;/span>&#x3C;/div>
&#x3C;p style="margin:10px;  width: 700px; font: 14px arial, sans-serif;line-height:150%;">Alternatively, you may email me, your Production Controller, at &#x3C;a href="mailto:#FIRSTUSEREMAIL#">#FIRSTUSEREMAIL#&#x3C;/a> or call #FIRSTUSERPHONE#.&#x3C;/p>
&#x3C;p style="margin:10px;  width: 700px; font: 14px arial, sans-serif;line-height:150%;">Your Sales Rep is #FIRST_SALES_REPS# and can be reached at &#x3C;a href="mailto:#FIRST_SALES_REPS_EMAIL#">#FIRST_SALES_REPS_EMAIL#&#x3C;/a> or #FIRST_SALES_REPS_PHONE#.&#x3C;/p>
&#x3C;p style="margin:10px;  width: 700px; font: 14px arial, sans-serif;line-height:150%;">Sincerely,&#x3C;/p>
&#x3C;p style="margin:10px;  width: 700px; font: 14px arial, sans-serif;line-height:150%;">#FIRSTUSERFIRSTNAME# #FIRSTUSERLASTNAME#&#x3C;/p>
</code></pre>

[^1]: Enter your code here for the XXX

[^2]: Replace with a link to your own logo

[^3]: Replace XXX with your site code. also replace 'default' with your portal profile ID.

[^4]: replace with appropriate email
