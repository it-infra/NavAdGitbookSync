# Sample Classified HTML Templates

## Sample Templates

There are two types of templates that can be used for Classified ads in Naviga Ad. You can create HTML templates or InDesign templates. This document relates to creating ads with HTML. There is a separate document on best practices when creating InDesign Templates.

When using InDesign templates, you can create the PDF ads as CMYK natively. When using HTML templates, HTML doesn’t support CMYK, so the ads are created in RGB and need to be converted later to CMYK. Naviga Plan, when outputting the Classified pages as “Block” pdfs, Naviga Plan will convert the pdf to CMYK. Alternatively, you (or your printer) will likely run the page pdfs thru preflighting software prior to printing which will also correct for any RGB.

Please note, throughout this document, the items in the HTML code with the # at the start and the end are the metadata merge tags from Naviga Ad Category setup. **The tags below may or may not match your defined merge tags. Edit these sample tags, fonts and styles to suit your preferred styles and metadata questions.**

These are the styles used in demos, as well as some clever examples borrowed from some of our customers, which we wanted to share with you to get you started.

<table><thead><tr><th width="262">Example</th><th>HTML/CSS Code</th></tr></thead><tbody><tr><td><p><img src="../../../../../.gitbook/assets/1 (28).png" alt="">Note on this one: When Naviga Plan output to CMYK, I noticed that the text in this ad wasn’t getting converted to true black. Turned out that the Black heading, combined with the text wrapped around the top image was causing trouble. I put a very small 1px x 1px transparent image after the black heading and all was good after that. If you also see issues, you might want to try that trick.</p><p><mark style="background-color:yellow;">This one points to a transparent image on my server, you would need to add one to your images and point to it on your server</mark></p><p><img src="../../../../../.gitbook/assets/image (337).png" alt="" data-size="original"></p><p>(same place you store your attention getters). See documentation on <a href="../images.md">images</a>, your Naviga Implementation Specialist or Naviga Support if you need help adding images.</p></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.newspaper {
column-count: 1;
column-gap: 10px;
font-family: Arial, Helvetica, sans-serif;
background-color: white;
color: black;
background-color: white;
}
.borderbox {
border-style: solid;
border:2px
padding: 5px;
font-size: 8pt;
text-align:justify;
}
.heading {
padding: 5px;
color: white;
background-color: black;
font-weight: bold;
width: 99%;
text-align: center;
font-size: 200%;
line-height: 110%;
}
.hideIfNoContent[data-content=""] {
display: none;
}
img[src*="placeholder-image.jpg"] {
display: none;
}
&#x3C;/style>
&#x3C;div class="borderbox newspaper">
&#x3C;div class="heading">#LAST#, #FIRST#&#x3C;/div>
&#x3C;img src="https://internal.navigahub.com/EW/DEM/localstorage/ImageLibrary/Catalog/AttentionGetters/transparentpx.png" alt="" /> &#x3C;img style="float: left; width: 25%; margin: 0; padding: 3px 2px 2px 2px; line-height: 110%;" src="#PHOTO#" alt="" />
&#x3C;div style="padding: 2px 4px; line-height: 125%;">&#x3C;strong>#BIRTH# - #DEATH#&#x3C;/strong> - #OBIT#&#x3C;/div>
&#x3C;div style="text-align: center; text-decoration: underline;">#URL#&#x3C;/div>
&#x3C;br />&#x3C;img style="width: 98%; padding: 2px;" src="#LOGO#" alt="" />&#x3C;/div>
</code></pre></td></tr><tr><td><img src="../../../../../.gitbook/assets/2 (30).png" alt="" data-size="original"></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.body {
font-family: Arial;
}
.heading {
text-transform: uppercase;
padding: 1px;
font-weight: bold;
font-size: 155%;
line-height: 110%;
}
.hideIfNoContent[data-content=""] {
display: none;
}
img[src*="placeholder-image.jpg"] {
display: none;
}
&#x3C;/style>
&#x3C;div class="heading">#LAST#&#x3C;/div>
&#x3C;p class="body" style="margin: 0; padding: 0;">&#x3C;span style="text-transform: uppercase; font-weight: bold; font-size: 10pt;"> #FIRST# &#x3C;/span> &#x3C;img style="display: block; margin-left: auto; margin-right: auto; padding: 0; min-width: 140px; max-width: 190px;" src="#PHOTO#" alt="" /> &#x3C;img style="float: left; width: 25%; margin: 0; padding: 2; line-height: 110%;" src="#AGPHOTO#" alt="" />&#x3C;/p>
&#x3C;div class="body hyphenate" style="padding: 1px; font-size: 11pt; text-align: justify;">#OBIT#&#x3C;/div>
&#x3C;div style="text-decoration: underline; text-align: center;">#URL#&#x3C;/div>
&#x3C;p style="margin: 0; padding: 0;">&#x3C;img style="display: block; margin-left: auto; margin-right: auto; padding: 0; min-width: 140px; max-width: 145px;" src="#LOGO#" alt="" />&#x3C;/p>
</code></pre></td></tr><tr><td><img src="../../../../../.gitbook/assets/3 (89).png" alt="" data-size="original"></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.body {
font-family: Arial, Helvetica, sans-serif;
font-size: 8pt;
text-align:justify;
}
.borderbox {
border-style: solid;
padding: 5px;
}
.subHeading{
background-color: #ddd;
padding: 5px;
font-weight: bold;
font-family: Arial, Helvetica, sans-serif;
font-size: 8pt;
line-height: 110%;
}
.hideIfNoContent[data-content=""] {
display: none;
}
img[src*="placeholder-image.jpg"] {
display: none;
}
&#x3C;/style>
&#x3C;div class="borderbox body">
&#x3C;div class="body" style="padding: 1px; font-weight: bold; box-sizing: border-box; width: 100%; text-align:center; font-size: 150%;">
#HEADLINE#
&#x3C;/div>
&#x3C;img alt="" src="#IMAGE#" class="center" width="95%" />
&#x3C;div class="hideIfNoContent" data-content="#DATE#">
&#x3C;div class="subHeading">Date Available: #DATE#&#x3C;/div>
&#x3C;/div>
#BEDROOMS# Bedrooms, #BATHROOM# Bathrooms, &#x3C;span class="hideIfNoContent" data-content="#SQFT#"> #SQFT# Sq. Ft. &#x3C;/span> #LONG_DESCRIPTION# &#x3C;span class="hideIfNoContent" data-content="#PRICE#">$#PRICE#/Month
&#x3C;/span>
&#x3C;/div>
</code></pre></td></tr><tr><td><p><img src="../../../../../.gitbook/assets/4 (35).png" alt="" data-size="original"></p><p>Just a simple line ad, with a bold heading, but has several places where things are hidden if no content is in certain metadata that isn’t required and may sometimes be omitted.</p><p><mark style="background-color:yellow;">In this example, the “hide if no content” style is defined up in the style tags and then in the body itself it will not display the text “Sq. Ft.” if there is no content in the metadata tag #SQFT#.</mark><br><img src="../../../../../.gitbook/assets/image (1255).png" alt=""></p></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.body {
font-family: Arial, Helvetica, sans-serif;
font-size: 8pt;
text-align:justify;
}
.hideIfNoContent[data-content=""] {
display: none;
}
&#x3C;/style>
&#x3C;div class="body">
&#x3C;strong>#HEADLINE#&#x3C;/strong> - &#x3C;span class="hideIfNoContent" data-content="#DATE#">Date Available: #DATE#&#x26;nbsp;&#x3C;/span>#BEDROOMS# Bedrooms, #BATHROOM# Bathrooms, &#x3C;span class="hideIfNoContent" data-content="#SQFT#">#SQFT# Sq. Ft. &#x3C;/span> #LONG_DESCRIPTION# &#x3C;span class="hideIfNoContent" data-content="#PRICE#">$#PRICE#/Month
&#x3C;/span>
&#x3C;/div>
</code></pre></td></tr><tr><td><p><img src="../../../../../.gitbook/assets/5 (10).png" alt="" data-size="original"></p><p>Notes: In this example, if I didn’t have an image uploaded, the text would collapse and not show placeholder images. This is because of the “img” definition inside the style tags.</p><p>Also, similar to the above example, there is a Price and a Sq Ft tag in the content which contains a $ sign and “Sq. Ft.” text if a value is placed in that field. The field is not required though, so if the field is blank, the additional text will not be added. This is because if the “hideIfNoContent” defined in the style tags.</p></td><td><pre class="language-html" data-overflow="wrap"><code class="lang-html">&#x3C;style>
.body {
font-family: Arial, Helvetica, sans-serif;
font-size: 8pt;
}
.borderbox {
border-style: solid;
}
.center {
display: block;
margin-left: auto;
margin-right: auto;
width: 98%;
}
.columnLeft {
float: left;
width: 33.33%;
height:75px;
padding: 5px;
}
.columnRight {
float: right;
width: 50%;
height:75px;
padding: 5px;
}
.hideIfNoContent[data-content=""] {
display: none;
}
img[src*="placeholder-image.jpg"] {
display: none;
}
&#x3C;/style>
&#x3C;div class="borderbox body">
&#x3C;div style="padding: 5px; color: #fff; background-color: #000; font-weight: bold; box-sizing: border-box; width: 100%; text-align:center; font-size: 200%;">OPEN HOUSE&#x3C;/div>
&#x3C;img alt="" src="#IMAGE#" class="center" />
&#x3C;div class="body" style="padding: 4px; text-align: justify;">&#x3C;span style="text-transform: uppercase; font-weight: bold;">#BEDROOMS#BR, #BATHROOM#BA, &#x3C;span class="hideIfNoContent" data-content="#PRICE#"> $#PRICE#&#x3C;/span>&#x3C;/span>
&#x3C;span class="hideIfNoContent" data-content="#SQFT#">
&#x26;nbsp;#SQFT# Sq. Ft. &#x3C;/span>
- #LONG_DESCRIPTION# &#x3C;br />
&#x3C;img alt="" src="#HEADSHOT#" style="max-width: 45%; height:75px; margin:0; padding: 0;" />
&#x3C;img alt="" src="#LOGO#" style="max-width: 45%; height:75px; margin: 0px; padding: 0px; float: right;" />
&#x3C;/div>
&#x3C;/div>
</code></pre></td></tr><tr><td><img src="../../../../../.gitbook/assets/6 (62).png" alt="" data-size="original"></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.body {
font-family: Arial, Helvetica, sans-serif;
font-size: 8pt;
text-align:justify;
line-height: 110%;
}
.borderbox {
border-style: solid;
border-color: #000;
border-width: 2px;
}
.center {
display: block;
margin-left: auto;
margin-right: auto;
}
.h2 {
text-transform: uppercase;
font-weight: bold;
background-color: #000000;
color: #ffffff;
font-size: 10pt;
text-align: center;
line-height: 150%;
}
.subheading {
line-height: 110%;
font-size: 8pt;"
font-weight: bold;
background-color: #ddd;
padding: 4px;
}
.hideIfNoContent[data-content=""] {
display: none;
}
img[src*="placeholder-image.jpg"] {
display: none;
}
&#x3C;/style>
&#x3C;div class="borderbox body">
&#x3C;div class="h2"> #HEADLINE# &#x3C;/div>
&#x3C;div class="hideIfNoContent" data-content="#ADDRESS#">
&#x3C;div class="subheading">&#x3C;strong>Address:&#x3C;/strong> #ADDRESS# #DATE#&#x3C;/div>
&#x3C;/div>
&#x3C;div style="padding: 3px;">#LONG_DESCRIPTION# &#x3C;/div>
&#x3C;div class="center">
&#x3C;img alt="" src="#PHOTO#" style="padding: 2px; width: 98%;" />
&#x3C;/div>
&#x3C;/div>
</code></pre></td></tr><tr><td><img src="../../../../../.gitbook/assets/7 (8).png" alt="" data-size="original"></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.newspaper{
font-family: Arial, Helvetica, sans-serif;
font-size: 8pt;
text-align:justify;
line-height: 110%;
padding: 2px;
}
.borderbox {
border-style: solid;
border-color: #000;
border-width: 1px;
}
.h2 {
text-transform: uppercase;
font-weight: bold;
font-size: 10pt;
text-align: left;
line-height: 150%;
}
&#x3C;/style>
&#x3C;div class="borderbox newspaper">
&#x3C;div class="h2">#HEADLINE# &#x3C;/div>
&#x3C;div class="hyphenate">#LONG_DESCRIPTION# &#x3C;/div> &#x3C;/div>
</code></pre></td></tr><tr><td><p><img src="../../../../../.gitbook/assets/8 (2).png" alt="" data-size="original"></p><p>This example is utilizing some custom color options. The Heading, the Salary box and the border are all sharing a custom color set in the metadata tag. If no salary is disclosed in the ad, then the entire salary line including the background color will disappear.</p></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.borderbox {
border-style: solid;
border-color: #BACKCOLOR#;
border-width: 2px;
padding:0;
font-family: Arial, Helvetica, sans-serif;
font-size: 8pt;
text-align:justify;
line-height: 100%;
}
.center {
display: block;
margin-left: auto;
margin-right: auto;
}
.heading2 {
text-transform: uppercase;
font-weight: bold;
background-color: #BACKCOLOR#;
color: #TEXTCOLOR#;
font-size: 10pt;
text-align: center;
line-height: 150%;
margin: 0px 0px 3px;
}
.heading3 {
font-weight: bold;
background-color: #BACKCOLOR#;
color: #TEXTCOLOR#;
font-size: 9pt;
text-align: left;
line-height: 125%;
margin: 0px 0px 3px;
padding: 4px;
}
img[src*="placeholder-image.jpg"] {
display: none;
}
.hideIfNoContent[data-content=""] {
display: none;
}
&#x3C;/style>
&#x3C;div class="borderbox">
&#x3C;div class="heading2">#HEADLINE# &#x3C;/div>
&#x3C;img alt="" src="#LOGO#" class="center" style="width: 90%;" />
&#x3C;div class="hideIfNoContent" data-content="#SALARY#">
&#x3C;div class="heading3">&#x3C;strong>Salary:&#x3C;/strong> #SALARY# #SALARYTYPE#&#x3C;/div>
&#x3C;/div>
&#x3C;div style="padding:4;">#LONG_DESCRIPTION# #BENEFITS#&#x3C;/div>
&#x3C;/div>
</code></pre></td></tr><tr><td><img src="../../../../../.gitbook/assets/9 (28).png" alt="" data-size="original"></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.body {
font-family: Arial, Helvetica, sans-serif;
font-size: 8pt;
text-align:justify;
line-height: 125%;
background-color:#BACKCOLOR#;
color:#TEXTCOLOR#;
padding:5px;
}
.hideIfNoContent[data-content=""] {
display: none;
}
&#x3C;/style>
&#x3C;div class="body">&#x3C;span style="text-transform: uppercase; font-weight: bold;">#HEADLINE# &#x3C;/span> -
#LONG_DESCRIPTION# #BENEFITS#&#x26;nbsp;
&#x3C;span class="hideIfNoContent" data-content="#SALARY#"> Salary: $#SALARY# #SALARYTYPE#&#x3C;/span>.
&#x3C;/div>
</code></pre></td></tr><tr><td><p><img src="../../../../../.gitbook/assets/10 (4).png" alt="" data-size="original"><img src="../../../../../.gitbook/assets/11 (1) (1).png" alt="" data-size="original"></p><p>Both images use the same style. TOP has white BACKCOLOR and Black TEXTCOLOR. 2nd image has the reverse.</p></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.borderbox {
border-style: solid;
border-color: #BACKCOLOR#;
border-width: 2px;
padding:0;
font-family: Arial, Helvetica, sans-serif;
font-size: 8pt;
text-align:justify;
line-height: 115%;
}
h2 {
font-weight: bold;
background-color: #BACKCOLOR#;
color: #TEXTCOLOR#;
font-size: 16pt;
text-align: center;
line-height: 150%;
margin: 0px 0px 1px;
}
h3 {
font-weight: bold;
background-color: #BACKCOLOR#;
color: #TEXTCOLOR#;
font-size: 9pt;
text-align: left;
line-height: 125%;
margin: 0px 0px 3px;
padding: 4px;
}
img[src*="placeholder-image.jpg"] {
display: none;
}
.hideIfNoContent[data-content=""] {
display: none;
}
&#x3C;/style>
&#x3C;div class="borderbox">
&#x3C;h2>#HEADLINE#&#x3C;/h2>
&#x3C;img alt="" src="#LOGO#" style="float: left; width: 25%; margin:0; padding-top: 5; padding-right: 5; line-height: 110%;" />
&#x3C;div style="padding: 2px 2px; border-top: 2px solid #TEXTCOLOR#; box-sizing: border-box; line-height: 125%;">
#LONG_DESCRIPTION# &#x3C;span class="hideIfNoContent" data-content="#SALARY#">#SALARY# #SALARYTYPE# &#x3C;/span>#BENEFITS#&#x3C;/div>
&#x3C;/div>
</code></pre></td></tr><tr><td><img src="../../../../../.gitbook/assets/12 (16).png" alt="" data-size="original"></td><td><pre class="language-html" data-overflow="wrap"><code class="lang-html">&#x3C;style>
.borderbox {
border-style: solid;
border-color: #000;
border-width: 2px;
padding:0;
font-family: Arial, Helvetica, sans-serif;
font-size: 8pt;
text-align:justify;
line-height: 125%;
}
h2 {
text-transform: uppercase;
font-weight: bold;
background-color: #000;
color: #fff;
font-size: 12pt;
text-align: left;
line-height: 125%;
margin: 0px 0px 0px;
padding:2;
}
h3 {
font-weight: bold;
background-color: #ddd;
color: #000;
font-size: 9pt;
text-align: left;
line-height: 150%;
margin: 0px 0px 3px;
padding: 0px;
}
img[src*="placeholder-image.jpg"] {
display: none;
}
.hideIfNoContent[data-content=""] {
display: none;
}
&#x3C;/style>
&#x3C;div class="borderbox">
&#x3C;h2> #HEADLINE#&#x3C;/h2>
&#x3C;img alt="" src="#MAIN_IMAGE#" style="width: 95%; margin:0; padding: 5;" />
&#x3C;div style="padding: 4px;">
&#x3C;h3>#MAKE# #MODEL# #YEAR#&#x3C;/h3>
&#x3C;span class="hideIfNoContent" data-content="#PRICE#">$#PRICE#.&#x3C;/span>
&#x3C;span class="hideIfNoContent" data-content="#MILES#">#MILES# Miles.&#x3C;/span>
&#x3C;span class="hideIfNoContent" data-content="#COLOR#">#COLOR# Exterior.&#x3C;/span>#LONG_DESC# #PHONE# #EMAIL# #WEB#&#x3C;/div>
&#x3C;/div>
</code></pre></td></tr><tr><td><img src="../../../../../.gitbook/assets/13 (14).png" alt="" data-size="original"></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.borderbox {
border-style: solid;
border-color: #fff;
border-width: 2px;
padding:0;
font-family: 'Times New Roman', Times, serif;
text-align:justify;
line-height: 115%;
padding:0;
}
headline {
text-transform: uppercase;
font-weight: bold;
color: #000;
font-size: 10pt;
text-align: center;
}
img[src*="placeholder-image.jpg"] {
display: none;
}
.hideIfNoContent[data-content=""] {
display: none;
}
&#x3C;/style>
&#x3C;div class="borderbox">
&#x3C;img alt="" src="#MAIN_IMAGE#" style="width: 95%; margin:0; padding: 5;" />
&#x3C;div style="padding: 4px;">&#x3C;span style="text-transform: uppercase; font-weight: bold; line-height: 125%;">#HEADLINE#&#x3C;/span>
#MAKE# #MODEL# #YEAR#.
&#x3C;span class="hideIfNoContent" data-content="#PRICE#">$#PRICE#.&#x3C;/span>
&#x3C;span class="hideIfNoContent" data-content="#MILES#">#MILES# Miles.&#x3C;/span>
&#x3C;span class="hideIfNoContent" data-content="#COLOR#">#COLOR# Exterior. &#x3C;/span>#LONG_DESC# #PHONE# #EMAIL# #WEB#&#x3C;/div>
&#x3C;/div>
</code></pre></td></tr><tr><td><img src="../../../../../.gitbook/assets/14 (21).png" alt="" data-size="original"></td><td><pre class="language-html" data-overflow="wrap"><code class="lang-html">&#x3C;style>
.borderbox {
border-style: solid;
border-color: #000;
border-width: 2px;
padding:0;
font-family: Arial, Helvetica, sans-serif;
text-align:justify;
line-height: 125%;
padding:0;
font-size: 8pt;
}
h2 {
text-transform: uppercase;
font-weight: bold;
background-color: #000;
color: #fff;
font-size: 16pt;
text-align: center;
line-height: 150%;
margin: 0px 0px 0px;
}
img[src*="placeholder-image.jpg"] {
display: none;
}
.hideIfNoContent[data-content=""] {
display: none;
}
&#x3C;/style>
&#x3C;div class="borderbox">
&#x3C;h2>#HEADLINE#&#x3C;/h2>
&#x3C;img alt="" src="#MAIN_IMAGE#" style="width: 95%; margin:0; padding: 5;" />
&#x3C;div style="padding: 4px;">&#x3C;span style="text-transform: uppercase; font-weight: bold; line-height: 125%;">#MAKE# #MODEL# #YEAR#.&#x3C;/span>
&#x3C;span class="hideIfNoContent" data-content="#PRICE#">$#PRICE#.&#x3C;/span>
&#x3C;span class="hideIfNoContent" data-content="#MILES#">#MILES# Miles.&#x3C;/span>
&#x3C;span class="hideIfNoContent" data-content="#COLOR#">#COLOR# Exterior.&#x3C;/span>#LONG_DESC# #PHONE# #EMAIL# #WEB#&#x3C;/div>
&#x3C;/div>
</code></pre></td></tr><tr><td>This ad will have 2 columns of text no matter how many columns are chosen in order entry. This might take up 3 columns in the paper, but will always just have 2 legs b/c in the style tag I put column-count: 2; See next example for that setting to be dynamic.<img src="../../../../../.gitbook/assets/15 (21).png" alt=""></td><td><pre class="language-html" data-overflow="wrap"><code class="lang-html">&#x3C;style>
.bodytext {
font-family: Arial, Helvetica, sans-serif;
font-size: 8pt;
text-align:justify;
line-height: 110%;
padding: 2px;
}
.newspaper {
column-count: 2;
column-gap: 10px;
}
.borderbox {
border-style: solid;
border-color: #000;
border-width: 1px;
font-size: 8pt;
text-align:justify;
line-height: 110%;
padding: 2px;
}
.h2 {
column-span: all;
text-transform: uppercase;
font-weight: bold;
font-size: 10pt;
text-align: left;
line-height: 150%;
text-align: center;
}
&#x3C;/style>
&#x3C;div class="borderbox">
&#x3C;div class="newspaper">
&#x3C;div class="h2">#HEADLINE# &#x3C;/div>
&#x3C;div class="bodytext">#LONG_DESCRIPTION# &#x3C;/div>
&#x3C;/div>
&#x3C;/div>
</code></pre></td></tr><tr><td><p><img src="../../../../../.gitbook/assets/16 (2).png" alt="" data-size="original"></p><p>In this example, the number of wrapped columns will vary based on the # of columns selected when booking. Without the #<em>COLS# tag, you can specify exactly how many columns you want (like in the previous example. In some cases, the former might be preferred, in some cases this might be. The #</em>_COLS# tag is a naviga-provided tag, you don't need a metadata field for it.</p><p>In this example, the text will wrap around the photo if a photo is provided and if it isn’t provided the text will just fill in that space.</p></td><td><pre class="language-html" data-overflow="wrap"><code class="lang-html">&#x3C;style>
.newspaper {
column-count: #_COLS#;
column-gap: 10px;
font-family: Arial, Helvetica, sans-serif;
font-size: 8pt;
text-align:justify;
line-height: 110%;
padding: 2px;
}
h2 {
column-span: all;
text-transform: uppercase;
font-weight: bold;
font-size: 12pt;
text-align: left;
line-height: 125%;
}
photoWrap {
float: left;
margin:0;
padding: 2;
line-height: 110%;
max-width: 50%;
}
footer {
column-span: all;
font-family: Arial, Helvetica, sans-serif;
font-size: 12px;
text-decoration: underline;
text-align: center;
padding: 5px;
}
img[src*="placeholder-image.jpg"] {
display: none;
}
&#x3C;/style>
&#x3C;h2 style="text-align: left;">#LAST#, #FIRST#&#x3C;/h2>
&#x3C;div class="newspaper" style="text-align: justify;">
&#x3C;photowrap>&#x3C;img alt="" src="#PHOTO#" style="width: 100%;" />
&#x3C;/photowrap>
&#x3C;span style="text-transform: uppercase; font-weight: bold; line-height: 125%;">
#BIRTH# - #DEATH#&#x3C;/span> - #OBIT# &#x3C;br />
&#x3C;footer>#URL# &#x3C;br />
&#x3C;img alt="" src="#LOGO#" style="max-width: 80px;" />
&#x3C;/footer>
&#x3C;/div>
</code></pre></td></tr><tr><td><p><img src="../../../../../.gitbook/assets/17 (19).png" alt="" data-size="original"></p><p>In this example here, I needed to have text and an image sharing the top row, then a row with dates, followed by a paragraph with another image formatted to the right, and then finally a signature line at the bottom. This is a Thank you note from a family after a funeral.</p><p>I found it easiest to style the ad using a table. So the table itself has 4 rows and two columns. Only the first row is really using both columns, the others have a rule that says “colspan=2” which is telling it that the text displayed there should span across both columns. You could probably accomplish the same results without the table, but I found it easier to do it this way to keep everything lined up like it should be.</p></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.borderbox {
border-style: solid;
border-color: #000;
border-width: 2px;
padding: 0px;
font-family: Arial, Helvetica, sans-serif;
}
.heading {
padding: 5px;
color: #fff;
background-color: #000;
font-weight: bold;
width: 100%;
text-align: center;
font-size: 200%;
line-height: 110%;
}
.hideIfNoContent[data-content=""] {
display: none;
}
img[src*="placeholder-image.jpg"] {
display: none;
}
&#x3C;/style>
&#x3C;table class="borderbox">
&#x3C;tbody>
&#x3C;tr>
&#x3C;td style="font-size: 10px;">#FULLNAME#&#x3C;/td>
&#x3C;td>&#x3C;img alt="" src="#IMAGE#" width="100%" />&#x3C;/td>
&#x3C;/tr>
&#x3C;tr>
&#x3C;td style="text-align: center;" colspan="2">&#x3C;span style="font-size: 8px;">#DATES#&#x3C;/span>&#x3C;/td>
&#x3C;/tr>
&#x3C;tr>
&#x3C;td colspan="2" style="text-align: justify;">&#x3C;span style="font-size: 9px;">&#x3C;img alt="" src="#PHOTO#" style="float: right; width: 25%; margin:0; padding: 2; line-height: 110%;" />#BODYTEXT#&#x3C;/span>
&#x3C;/td>
&#x3C;/tr>
&#x3C;tr>
&#x3C;td colspan="2" style="text-align: right;">&#x3C;span style="font-size: 9px;">&#x3C;strong>#FROMNAMES#&#x3C;/strong>&#x3C;/span>&#x3C;/td>
&#x3C;/tr>
&#x3C;/tbody>
&#x3C;/table>
</code></pre></td></tr><tr><td><p><img src="../../../../../.gitbook/assets/18 (9).png" alt="">This was a little unusual in that the name of the person was supposed to be within the frame itself.</p><p>Important bits here are that the heading had a negative number for the top margin to make it inset within the frame, and it had a white background to block out part of the frame/border. -6px seemed best for me, otherwise it would be too high and outside the ad itself, and the main part of the ad needed a wider than normal top margin so that it started well below the frame.<br><img src="../../../../../.gitbook/assets/image (403).png" alt=""></p></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.borderbox {
border-style: solid;
border-color: #000;
border-width: 2px;
padding:2;
font-family: Arial, Helvetica, sans-serif;
font-size: 8pt;
text-align:justify;
line-height: 125%;
}
.heading{
display: block;
margin-left: auto;
margin-right: auto;
width:40%;
margin-top:-6px;
background:white;
}
.main{
width:100%;
margin-top:10px;
text-align: justify;
background:white;
}
img {
display: block;
margin-left: auto;
margin-right: auto;
padding: 0;
min-width: 140px;
max-width: 190px;
}
&#x3C;/style>
&#x3C;div class="borderbox">
&#x3C;div class="heading" style="text-align: center;">
#FIRST# #LAST#&#x3C;/div>
&#x3C;div class="main">&#x3C;img alt="" src="#PHOTO#" />&#x3C;/div>
&#x3C;div class="main">#OBIT#&#x3C;/div>
&#x3C;/div>
</code></pre></td></tr><tr><td><p><img src="../../../../../.gitbook/assets/19 (10).png" alt="" data-size="original"></p><p>This one was a fun challenge. The requirement was for a fixed sized ad that included multiple images in specific locations on the ad and also allowed for some upsells (couple of different colored backgrounds and the red flag in the top left corner of the home photo could be added.) Metadata surcharges allows for the site to add a premium for those additions, if desired.</p></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.-na-template *
{
font-family: Arial, Arial, Helvetica, sans-serif;
font-size: 7pt;
}
.-na-template
{
height: 2.70in;
width: 4.83in;
border: 3px solid black;
padding: 0;
margin: 0;
overflow: hidden;
position: relative;
border-collapse: collapse;
table-layout: fixed;
}
.-na-template.yellow
{
color: #000;
background-color: #ffdb7c;
}
.-na-template.white
{
color: #000;
background-color: #FFFFFF;
}
.-na-template.pink
{
color: #000;
background-color: #fad5e5;
}
.-na-template.blue
{
color: #000;
background-color: #d4effc;
}
.-na-template .heading
{
background-color: black;
padding: 0 8px;
margin: 0;
color: white;
text-align: center;
font-size: 175%;
overflow: hidden;
white-space: nowrap;
}
.-na-template img.headshot
{
height: 0.92in;
width: 1.05in;
background-color: transparent;
}
.-na-template img.photo
{
width: 100%;
margin: 0 5px 3px 0;
background-color: transparent;
height: 1.5in;
box-sizing: border-box;
padding: 0;
text-align: center;
}
.-na-template .image1
{
position: relative;
top: 0;
left: 0;
}
.-na-template .image2
{
position: absolute;
top: 26px;
left: 8px;
height: 0.6in;
width: 0.6in;
}
.-na-template img.logo
{
max-width: 100%;
max-height: 30px;
text-align: center;
margin: 2px 2px 2px 0;
background-color: transparent;
}
.-na-template table
{
width: 100%;
border-collapse: collapse;
table-layout: fixed;
}
.-na-template td
{
vertical-align: top;
overflow: hidden;
}
.-na-template .invisible
{
height: 0;
margin: 0;
padding: 0;
font-size: 0;
line-height: 0;
}
.-na-template .hideIfNoContent[data-content=""]
{
display: none;
}
.-na-template a
{
text-decoration: none;
}
.-na-template img[src*="placeholder-image.jpg"]
{
display: none;
}
&#x3C;/style>
&#x3C;table class="-na-template #BACKGROUND#">&#x3C;!-- The first row determines the column layout - so we need this here -->
&#x3C;tbody>
&#x3C;tr>
&#x3C;td class="invisible" style="width: 54%;">&#x26;nbsp;&#x3C;/td>
&#x3C;td class="invisible">&#x26;nbsp;&#x3C;/td>
&#x3C;/tr>
&#x3C;tr>
&#x3C;td class="heading" colspan="2">#HEADLINE# - $#PRICE#&#x3C;/td>
&#x3C;/tr>
&#x3C;tr>
&#x3C;td>
&#x3C;table style="width: 100%; height: 2.42in;">
&#x3C;tbody>
&#x3C;tr>
&#x3C;td style="padding: 4px 2px 0 5px;">&#x3C;img class="photo image1" src="#IMAGE#" alt="" /> &#x3C;img class="photo image2" style="width: 0.6in; height: 0.6in;" src="#BANNER#" alt="" />&#x3C;/td>
&#x3C;/tr>
&#x3C;tr>
&#x3C;td style="vertical-align: top; text-align: center; padding: 0px;">
&#x3C;div style="height: 0.75in; overflow: hidden;">
&#x3C;div style="font-size: 125%; font-weight: bold; white-space: nowrap; overflow: hidden;">#NAME#&#x3C;/div>
&#x3C;div style="font-size: 100%; white-space: nowrap; overflow: hidden;">#PHONE#&#x3C;/div>
&#x3C;div style="white-space: nowrap; overflow: hidden;">&#x3C;a href="mailto:#EMAIL# style=text-decoration:none;"> &#x3C;span style="color: #000000;">#EMAIL#&#x3C;/span> &#x3C;/a>&#x3C;/div>
&#x3C;div style="white-space: nowrap; overflow: hidden;">&#x3C;strong>#WEBSITE#&#x3C;/strong>&#x3C;/div>
&#x3C;span class="hideIfNoContent" data-content="#LOGO#">&#x3C;img class="logo" src="#LOGO#" alt="" />&#x3C;/span>&#x3C;/div>
&#x3C;/td>
&#x3C;/tr>
&#x3C;/tbody>
&#x3C;/table>
&#x3C;/td>
&#x3C;td style="padding: 4px;">
&#x3C;table style="width: 100%; height: 100%;">
&#x3C;tbody>
&#x3C;tr>
&#x3C;td>
&#x3C;div style="font-weight: bold; margin-bottom: 2px; white-space: nowrap; overflow: hidden;">#BEDROOMS#&#x3C;span class="hideIfNoContent" data-content="#BEDROOMS#"> BD | &#x3C;/span>#BATHROOM# &#x3C;span class="hideIfNoContent" data-content="#BATHROOM#">BA | &#x3C;/span>#SQFT# &#x3C;span class="hideIfNoContent" data-content="#SQFT#">SQ. FT.&#x3C;/span>&#x3C;/div>
&#x3C;div style="overflow: auto; max-height: 1.5in;">#LONG_DESCRIPTION# &#x3C;br />&#x3C;span class="hideIfNoContent" style="margin-top: 10px; font-weight: bold; white-space: nowrap; overflow: hidden;" data-content="#MLS#">MLS# #MLS#&#x3C;/span>&#x3C;/div>
&#x3C;/td>
&#x3C;/tr>
&#x3C;tr>
&#x3C;td style="vertical-align: bottom; text-align: right;">&#x3C;img class="headshot" src="#HEADSHOT#" alt="" />&#x3C;/td>
&#x3C;/tr>
&#x3C;/tbody>
&#x3C;/table>
&#x3C;/td>
&#x3C;/tr>
&#x3C;/tbody>
&#x3C;/table>
</code></pre></td></tr><tr><td><p><img src="../../../../../.gitbook/assets/20 (8).png" alt="" data-size="original"></p><p>The challenge on this one was that the images needed to be stacked on top of eachother while having the text wrapping around the images.</p><p>The key on getting this to work was adding the <em><mark style="background-color:yellow;">style="clear: left;</mark>"</em> to each of the image tags after the 1st one.</p></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.heading {
text-transform: uppercase;
font-family: PoynterAgateOne-Reg;
font-weight: bold;
transform: scale(.9524, 1);
}
.body {
font-family: PoynterAgateOne-Reg;
text-align: justify;
}
.hideIfNoContent[data-content=""] {
display: none;
}
.squarePhoto {
float: left;
margin:0;
padding: 2;
line-height: 110%;
width: 93px;
height: 93px;
}
img[src*="placeholder-image.jpg"] {
display: none;
}
.emblemSize {
display:block;
margin-left: auto;
margin-right: auto;
padding: 2;
width: Auto;
}
&#x3C;/style>
&#x3C;div class="heading" style="text-align: left;">&#x3C;span style="font-size: 10.5pt; line-height: 114.3%; font-family: PoynterAgateOne-CondBold;">#LAST#&#x3C;span class="hideIfNoContent heading" style="font-size: 10.5pt; line-height: 114.3%; font-family: PoynterAgateOne-CondBold;" data-content="#MAIDENNAME#"> (#MAIDENNAME#)&#x3C;/span>, #FIRST# &#x3C;span class="hideIfNoContent heading" style="font-size: 10.5pt; line-height: 114.3%; font-family: PoynterAgateOne-CondBold;" data-content="#MIDDLE#">#MIDDLE# &#x3C;/span>&#x3C;span class="hideIfNoContent heading" style="font-size: 10.5pt; line-height: 114.3%; font-family: PoynterAgateOne-CondBold;" data-content="#NICKNAME#">"#NICKNAME#" &#x3C;/span>&#x3C;/span>&#x3C;/div>
&#x3C;div>&#x3C;img class="squarePhoto" src="#PHOTO1#" alt="" /> &#x3C;img class="squarePhoto" style="clear: left;" src="#PHOTO2#" alt="" /> &#x3C;img class="squarePhoto" style="clear: left;" src="#PHOTO3#" alt="" /> &#x3C;img class="emblemSize" style="clear: left;" src="#EMBLEM1#" alt="" align="left" /> &#x3C;img class="emblemSize" style="clear: left;" src="#EMBLEM2#" alt="" align="left" /> &#x3C;img class="emblemSize" style="clear: left;" src="#EMBLEM3#" alt="" align="left" /> &#x3C;img class="emblemSize" style="clear: left;" src="#EMBLEM4#" alt="" align="left" />&#x3C;/div>
&#x3C;div class="hyphenate">&#x3C;span style="font-size: 6.5pt; line-height: 107.7%; font-family: PoynterAgateOne-Reg;">#TEXT#&#x3C;/span>&#x3C;/div>
</code></pre></td></tr><tr><td><p><img src="../../../../../.gitbook/assets/image (1270).png" alt="" data-size="original"></p><p>This was a clever template “borrowed” from one of our customers. This is one template, with a metadata selection on what image size was desirable. The metadata options here are the style names:</p><p><img src="../../../../../.gitbook/assets/image (1412).png" alt="" data-size="original"></p><p>In this case D and E aren’t really doing anything other than giving the user something to pick. This bit of code here will take care of a case when the image isn’t uploaded (their option D_no photo) img[src*="placeholder-image.jpg"] {</p><p>display: none;</p><p>And their “E” choice is really just not overriding the style with something else and allowing the image to be full width of the column.</p></td><td><pre class="language-markup" data-overflow="wrap"><code class="lang-markup">&#x3C;style>
.A_2column {
float: right;
margin:0;
padding: 4;
line-height: 110%;
max-width: 3.14in;
max-height: 2in;
}
.B_1column {
float: right;
margin:0;
padding: 4;
line-height: 110%;
max-width: 1.47in;
max-height: 2in;
}
.C_thumbnail {
float: right;
margin:0;
padding: 4;
line-height: 110%;
max-width: .667in;
height: 1in;
}
img[src*="placeholder-image.jpg"] {
display: none;
}
&#x3C;/style>
&#x3C;p style="margin: 0px; padding: 0px; text-align: center;">&#x3C;span style="font-size: 12pt;">&#x3C;strong>&#x3C;span style="text-transform: uppercase;">#FIRST# #LAST#&#x3C;/span>&#x3C;/strong>&#x3C;/span>&#x3C;/p>
&#x3C;div class="#PHOTO_SIZE#" style="text-align: justify;">&#x3C;img style="width: 100%;" src="#PHOTO#" alt="" />&#x3C;/div>
&#x3C;p style="margin: 0px; padding: 0px; text-align: left;">&#x3C;span style="font-size: 8.3pt;">#OBIT#&#x3C;/span>&#x3C;/p>
</code></pre></td></tr><tr><td><img src="../../../../../.gitbook/assets/image (1198).png" alt=""><br><img src="../../../../../.gitbook/assets/image (393).png" alt=""><br>Another really clever one I think. This is a real life example from one of our customers. The ad itself reads First name Last Name, but they wanted to have the sort text prepend the last name in front of the normal sort text so that it would sort by last name in Naviga Plan.<br>To do this, they have a sorttext style defined at the top which has visibility:hidden and then prior to the text itself, the last name metadata tag is prepended.</td><td><pre class="language-markup"><code class="lang-markup"><strong>&#x3C;style type="text/css">
</strong>.newspaper {
    }
.body {
    margin:0px;
    font-family: MyriadPro-SemiExt;
    text-align: justify;
    font-size: 8pt; 
    line-height: 9pt; 
    font-weight: normal;
    }
    .ending{
    margin: 0px;
    font-size: 8pt; 
    line-height: 9pt; 
    font-family: MyriadPro-SemiExt;
    font-weight: normal;
    }
    .bodyverse {
    padding-top: 10px;
    padding-bottom: 10px;
    margin:0px;
    font-family: MyriadPro-SemiExtIt;
    text-align: center;
    line-height: 7.5pt; 
    font-size: 7.5pt; 
   }
   .body br  { display: block; margin: 7px; content: ""; }
   .bodyverse br  { display: block; margin: 4px; content: ""; }
   .borderbox {
          outline: 1px solid #000000;
          outline-offset: -2px;
          padding: 10px;
          margin: 2px;
    }
    .image {
    image-align: center;
    padding: 5px; 3px 5px 0px;
     }
   .sorttext {
    display: inline-block;
    padding: 5px;
    margin:0;
    font-family: MyriadPro-Regular;
    font-size: 6pt;
    background: white;
    position:absolute;
    top:0px;
    left:15px;
    visibility:hidden;
    }
   .heading {
    margin: 5px 0 0;
    text-transform: uppercase;
    padding: 0px;
    font-family: MyriadPro-BoldSemiExt;
    font-weight: bold;
    font-size: 9.5pt;
    line-height: 9.5pt;
    text-align: center;
    }
    .heading2 {
    margin:5px;
    text-transform: capitalize;
    padding: 0px 0px 0px 0px;
    font-size: 8pt; 
    font-family: MyriadPro-SemiExt;
    line-height: 8pt;
    }   
    .heading3 {
    margin:5px;
    text-transform: uppercase;
    padding: 0px;
    font-weight: normal;
    font-family: MyriadPro-BoldSemiExt;
    font-size: 9pt;
    font-weight: bold;
    line-height: 9pt;
    }
    .hideIfNoContent[data-content=""] {
    display: none;
    }
    img[src*="placeholder-image.jpg"] {
    display: none;
    }
&#x3C;/style>
&#x3C;div class="borderbox">
&#x3C;div class="sorttext" style="text-align: left;">#LAST_NAME#&#x3C;/div>
&#x3C;div class="newspaper" style="text-align: center;">&#x3C;span class="image" style="padding: 0px; text-align: center;"> &#x3C;img style="width: 192px; height: 192px; margin: 0px;" src="#PHOTO#" alt="" />&#x3C;/span>
&#x3C;div class="website-content">
&#x3C;p class="heading" style="text-align: center; padding-top: 5px;">&#x3C;strong>#TITLE#&#x3C;/strong>&#x3C;/p>
&#x3C;p class="heading3 hideIfNoContent" style="text-align: center;" data-content="#ALTERNATE_NAME#">#ALTERNATE_NAME#&#x3C;/p>
&#x3C;p class="heading2 hideIfNoContent" style="text-align: center;" data-content="#DATE_TITLE#">#DATE_TITLE#&#x3C;/p>
&#x3C;hr align="center" width="25%" />
&#x3C;p class="body">#PASSAGES_TEXT#&#x3C;/p>
&#x3C;p class="bodyverse hideIfNoContent" style="text-align: center; margin: 0; padding-top: 10px; padding-bottom: 10px;" data-content="#VERSE#">&#x3C;em>#VERSE#&#x3C;/em>&#x3C;/p>
&#x3C;p class="ending hideIfNoContent" style="text-align: center; padding-top: 10px; padding-bottom: 10px;" data-content="#ENDING#">#ENDING#&#x3C;/p>
&#x3C;/div>
&#x3C;span class="image" style="padding: 0px; text-align: center;"> &#x3C;img style="width: 75%; max-height: 75px; margin: 3px;" src="#LOGO#" alt="" />&#x3C;/span>&#x3C;/div>
&#x3C;/div>
</code></pre></td></tr><tr><td></td><td></td></tr></tbody></table>

```html
```

## Tips and Tricks

### Hide text if No Metadata

If you are looking to **show/hide certain items** depending on whether a certain tag is filled in or not, and you don’t wish to make the tag itself required, you can do that with a bit of CSS. This is shown in several examples above.

Example below is the case where I have a real estate ad. I wanted to have a metadata tag #SQFT# but I did not want that tag to be required on all ads. But where it was provided, I didn’t want to show only that number, I wanted the ad to read “It has XXX Sq. Ft.!” and leave off the entire sentence if the #SQFT# tag was blank. This is how to do it. It will also work with \<span> tag instead of \<div> if you want it within the same paragraph as the rest of the tags.

_Add below line between the \<style>\</style> tags:_

```
.hideIfNoContent[data-content=""] { display: none; }
```

Example of some content with above style/class, that hides itself if nothing is in the #SQFT# field:

```html
<div class="hideIfNoContent" data-content="#SQFT#">
It has #SQFT# Sq. Ft.!
</div>
```

If the user put 1500 in the Square Ft metadata, the ad would read "It has 1500 Sq. Ft.!"

### Custom Fonts

If you are looking to use a **custom font** in your setup, you can give the fonts to Naviga to upload to the server, or there is a pretty easy way to do it by including the font into in your template.

You will start out by using an online tool to convert your font to base64

This example uses two separate fonts. Here is the first important part of the HTML, defining the font itself:

@font-face {

font-family: Ted;

src: url(data:font/ttf;base64,T1RUTwALAIAAAwAwQ0ZGICd07cwAAAvEAABvqkdQT1OsQl

LOTS OF EXTRA FONT DATA

}

@font-face {

font-family: TedBold;

src: url(data:font/ttf;base64,T1RUTwALAIAAAwAwQ0ZGICd07cwAAAvEAABvqkdQT1OsQl

LOTS OF EXTRA FONT DATA

}

And then if we want to specify that font just for one tag:

Account No: \<span style="font-family: TedBold;">#BILLTO\_ID#\</span>

And here is if we want to specify it for pretty much everything else:

.body {

font-family: Ted;

font-size: 1.00em;

line-height: 125%;

text-align: left;

color: #555;

vertical-align: top;

}

A handy online tool for converting TTF or OTF to base64 is Font Squirrel:

[https://www.fontsquirrel.com/tools/webfont-generator](https://www.fontsquirrel.com/tools/webfont-generator)

Click on “Expert” to get the option to convert to base64…

<figure><img src="../../../../../.gitbook/assets/image (1660).png" alt=""><figcaption></figcaption></figure>

After selecting this, section below will expand. Scroll down and check this:

<figure><img src="../../../../../.gitbook/assets/image (1661).png" alt=""><figcaption></figcaption></figure>

A bunch of stuff will download in a Zip file. All you actually need is the stylesheet.css. Copy everything from the @font-face tag until the end. Paste it into your template, inside the \<style> tag.

Adobe Type 1 fonts will need a different tool, like FontLab.

### **Hidden Tags!**

To place the name and or address of the advertiser right in the text of the ad without the need to type it in as metadata, you can use the tags **#\_ADVERTISER\_NAME#** or **#\_ADVERTISER\_ADDRESS#** in your template.

The **#\_COLS#** tag can be used in your template to indicate the # of columns defined on the order in order entry. For example:

<figure><img src="../../../../../.gitbook/assets/image (926).png" alt=""><figcaption></figcaption></figure>

### Image tricks

Images are often used in ads and can be part of your template by using an \<img> tag. If you have an image tag in your template, but don’t actually upload an image, you will by default get a placeholder image in the ad copy. If you plan to swap it later for an actual photo that the customer will send you, you can leave the default placeholder in place.

If you prefer to use the same templates when you do and do not have images, you can add some code to the \<style> tag on the template and it will remove the placeholder and collapse the ad.

If you would like to remove the placeholder, add this inside the \<style> tag

```css
img[src*="placeholder-image.jpg"] {
display: none;
}
```

If you prefer to have the placeholder in there to get the correct price and then replace it with a real image later, then you can leave it out. If you want the best of both worlds, make your own placeholder image and call it something other than our “placeholder-image.jpg” and then you can choose when to insert a placeholder and when to not, but still have the same templates.

|     Leaving the place holder will look like this:     |            Removing it will look like this:            |
| :---------------------------------------------------: | :----------------------------------------------------: |
| ![](<../../../../../.gitbook/assets/image (948).png>) | ![](<../../../../../.gitbook/assets/image (1079).png>) |

### Using Metadata for styling

Think outside the box a little too on the metadata! If you want to give your users some options on styling, but not allow them to go too crazy, you can set up some metadata and html controls to allow them to do things like change border thickness, change leading, etc. Here are some examples set up in a demo category:

<figure><img src="../../../../../.gitbook/assets/image (925).png" alt=""><figcaption></figcaption></figure>

In this example, the metadata tags above are used in the CSS and HTML:

<figure><img src="../../../../../.gitbook/assets/image (734).png" alt=""><figcaption></figcaption></figure>

Things to note above…you can see in the metadata for the backgrounds, I gave only 4 choices…yellow, black, gray, and white. These were then used as style names and the codes under that style define the exact font, size, text color and background shade of yellow allowed by the media company.

Then outside the Style tag, I call a class called “#BACKGROUND#” which defines which of the above styles should be pulled in. Similarly, I made tags for leading with “line-height” and allowed for custom Border thickness with the #BORDERWEIGHT# tag. The border thickness, I did with a dropdown so they could pick no border, 1pt, 2pt, 3pt or 4pt, but nothing else. I did the leading with just a number field with 2 decimals so that they could be very specific if need-be. The #BACKGROUND\_HEADER# tag allowed the user to have a different background for the header (for example if the header was reversed, they could select “Black” in the metadata dropdown and then the header would be given a black background with white text (as was defined in the style called “.black”

### **Turning on Hyphenation**

If you wish to turn on hyphenation during order entry, you can click this button:

<figure><img src="../../../../../.gitbook/assets/image (680).png" alt=""><figcaption></figcaption></figure>

If you want it to be set automatically in the template, you will need to add class = “hyphenate” to your div or span tag around the text. Here is an example:

<figure><img src="../../../../../.gitbook/assets/image (1603).png" alt=""><figcaption></figcaption></figure>

You do not need to define the class in the CSS style tags at the top. This class is something already understood in our software.

ALTERNATIVELY, Some sites are very specific about rules around hyphenation. Instead of the above simple class=”hyphenate” code in the HTML, you can alternatively enter very specific hyphenation rules in the CSS. Below is an example from one of our customers CSS styles.

<figure><img src="../../../../../.gitbook/assets/image (1200).png" alt=""><figcaption></figcaption></figure>

In this example, rules were defined to only hyphenate when there were at least a certain number of characters before and after the hyphen. Limits can be set for aesthetic reasons to only have a certain number of lines in a row with hyphens, etc. The above lines starting with -webkit vs hyphenate are basically duplicating the same commands, but different browsers support different ways of coding it, so in this case both versions were included to support the users using different browsers. I found a good article [here](https://medium.com/clear-left-thinking/all-you-need-to-know-about-hyphenation-in-css-2baee2d89179) that describes the various options in more detail.

### **First x words bold/italics/something else in your style**

In basic HTML and CSS, there isn’t a capability to have the first x words in a certain format. HTML understands first word, but it doesn’t understand first two words or first three words, so that is something we needed to program into the system to allow you to manage that.

Here is what you need to do to set it up:

1. In your template, include a style rule called .-na-firstwords
2. In this style rule you must include a new attribute called -na-wordcount: ##; where ## is the number of words that are affected
3. In your HTML template area – you must add a class called -na-first-words-container to any text areas where this rule is to be applied

Here is an example template:

![](<../../../../../.gitbook/assets/image (1465).png>) ![](<../../../../../.gitbook/assets/image (538).png>)

Here is the style tag above for ease of copy/paste:

```css
.-na-firstwords
{
-na-wordcount: 2;
color: green;
font-weight: bold;
text-transform: uppercase;
}
```

And here is the div or span tag:

```html
<span class="hyphenate -na-firstwords-container">
```

(remove the “hyphenate” if you do not wish to turn on hyphenation. Our example is from a style which does hyphenate.)

### Customizing Bullets and Numbered Lists

I made a little video of how to customize the look of bulleted/numbered lists in the css.

{% embed url="https://dev.navigahub.com/mothership/resources/videos/BulletListTips.mp4" %}

For ease of copy and pasting, this is the little bit of code that I added to the templates that I wanted to have smaller bullet margins. Add this inside your style tags in the templates:

```
   ul {
   margin-left: -2em;
   }
   ol {
   margin-left: -2em;
   }
```

If you prefer to go with the Code Block option, here is the code for the Bullets:

```
<ul style="margin-left: -2em;">
    <li>&nbsp;</li>
</ul>
```

And for the Numbered List:

```
<ol style="margin-left: -2em;">
    <li>&nbsp;</li>
</ol>
```
