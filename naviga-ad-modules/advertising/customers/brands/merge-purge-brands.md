# Merge / Purge Brands

### Purpose <a href="#_toc77936555" id="_toc77936555"></a>

The purpose of this document is to explain how users merge and purge brands for advertisers based on needs to combine brands into one or get rid of inactive brands. This can be done for the same advertiser or across two different advertisers.

This feature gives users the ability to clean up duplicate clients brands without losing history. This process merges the data without changes to billing rules housed on the brand.

{% hint style="warning" %}
* The orders which are already billed with the old brand will not cancel and rebook with new orders, and there are no changes to the agency or reps.
* Future orders may end up with different rep and agency unless the appropriate checkboxes are checked.
* The process cannot be undone and administrators should limit who has access to this tool. It is recommended that if you are not sure of the impact on your users and orders, you can always mark a brand as “Inactive” instead in the menu Customers -> Brand -> Brand Maintenance and it will prevent users from viewing the brand or using it in order entry screen.
{% endhint %}

### Merge and Purge Brands <a href="#_toc437599622" id="_toc437599622"></a>

To use this tool, navigate to the menu Customers -> Brands -> Merge/ Purge Brands.

<figure><img src="../../../../.gitbook/assets/image (1241).png" alt=""><figcaption></figcaption></figure>

Enter the advertiser ID in the side “Merge This Advertiser/ Brand”, and select the brand from the drop down menu, which you would like to merge into the new advertiser and brand.

On the section “Into This Advertiser/ Brand”, choose the advertiser and brand which you would like merge the other brand into.

* The advertiser ID in this section could be the same as advertiser ID in the first section. For example, if the first advertiser ID has 2 brands which are the same but with slightly different names, such as, “Antiques” and “Classics”, and orders apply to them both similarly, user can choose Antiques as the first brand and merge it into Classics for the same advertiser.
* OR, the advertiser ID could be different for the second advertiser. For example if a large company sold off one of its divisions, you might merge that brand into another account.

![](<../../../../.gitbook/assets/2 (50).png>)

If you would like to override the agency on unbilled orders to be replaced with the new agency for the second brand, click this box to change it to “yes”.

Similarly, check the boxes if you would like to also override the sales rep and the PIB/Category on orders with the new values on the second brand.

Click “Apply Changes”. Click OK to the confirmation warning message. You will then receive a count of the orders changed.

<figure><img src="../../../../.gitbook/assets/image (1061).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note: in the Digital First system all campaigns (print and digital) will be listed as "Advertising Campaigns Changed" and Print Orders should always be zero.

Also Note that the message can show zero orders changed, if the old brand doesn't have any orders
{% endhint %}

### Existing Orders Using Old Brand <a href="#_toc77936557" id="_toc77936557"></a>

These orders if in the state of quote, reserved, running and not billed yet, the orders can still be processed with their existing or new agency, PIB and or Rep depending on the choices you made during the operation.

If the orders are already billed, then no cancel/ rebook will take place. The invoices will remain the same and can be processed as is.

### New Orders Using Merged/Purged Brands <a href="#_toc77936558" id="_toc77936558"></a>

After the merge/ purge process is complete, users will not be able to view or select the brand which was merged or purged in the order entry screen. Users will be able to view and select the new brand which absorbed the older brand.

<figure><img src="../../../../.gitbook/assets/image (995).png" alt=""><figcaption></figcaption></figure>

In this example, Brand “Baker Center” is being absorbed by brand “5th St Towers” for the same advertiser.

Navigate to create a new campaign and view the available brands for this advertiser in the drop down brands in the order entry screen.

<figure><img src="../../../../.gitbook/assets/image (1385).png" alt=""><figcaption></figcaption></figure>

The old brand will not be available for order entry but the brand which absorbed the old one is available.

### Brand Maintenance <a href="#_toc77936559" id="_toc77936559"></a>

Similarly, the brand will not be available for management in the Brand Maintenance screen.

<figure><img src="../../../../.gitbook/assets/image (322).png" alt=""><figcaption></figcaption></figure>

Note that you can always mark a brand as “Inactive” instead of merge and purge if it is applicable till you are certain of the merge/ purge need.
