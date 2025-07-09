---
title: Configure feed data settings
description: Learn how to configure the settings that control how feed data is processed.
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
---
# Configure feed data settings

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (delete actions only), and [!DNL Yandex] accounts only*

You can configure how to handle ad groups, keywords, and ads in feed data files, and how to process the data in FTP files specifically, via the feed settings.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**.

1. In the toolbar above the data table, click **[!UICONTROL Settings]**.

1. Specify the [feed data settings](#feed-data-settings):

   1. In the [!UICONTROL Obsolete Item Auto-Processing] section, select information in the fields.
   
   1. (Advertisers uploading data via FTP or via a direct link to a merchant center account) In the [!UICONTROL FTP/GMC Account Auto-Processing] section, select information in the fields.
   
   1. In the [!UICONTROL Miscellaneous Auto-Processing] section, select information in the fields.

1. Click **[!UICONTROL Save]**.

## Feed data settings {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** Applies all of the [!UICONTROL Obsolete Item Auto-processing] settings to:

* *[!UICONTROL Ad Groups Only]:* Obsolete ad groups only.

* *[!UICONTROL Keywords Only]:* Obsolete keywords and product groups only.

* *[!UICONTROL Ad Variations Only]* (the default): Obsolete ads only.

* *[!UICONTROL Keywords and Ad Variations]:* Both obsolete keywords/product targets/product groups and obsolete ads.

>[!NOTE]
>
>* For [!DNL Google Ads] shopping ads, only the lowest-level product group is affected.
>* For [!DNL Yandex] accounts, obsolete item auto-processing tasks are always performed on ad variations, regardless of this setting.

**[!UICONTROL When the Scheduled End Date is reached]:** (Manually posted data only) What to do with line items in a feed file posted with a specified end date and time once the end time arrives:

* *[!UICONTROL Delete]* (the default): Delete all relevant components when the specified end time arrives. You can't reverse this operation.

* *[!UICONTROL Pause]:* Pause all relevant components when the specified end time arrives. You can reactivate the components later, if necessary.

* *[!UICONTROL None]:* Don't change the status of the relevant components.

**[!UICONTROL Missing line items in a manually uploaded feed]:** What to do with existing items when they aren't included in a new feed file that was uploaded manually or when they don't map to existing campaigns or ad groups per the Map Only settings in the template:

* *[!UICONTROL Delete]:* Delete the existing components.

* *[!UICONTROL Pause]:* Pause the existing components. They're reactivated if a new feed file contains any of the same line items, and they retain their history and quality scores. **Note:** If all of the child product groups for a parent product group are missing, then the parent product group is deleted because you can't pause product groups.

* *[!UICONTROL None]* (the default): Don't change the existing components.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** What to do with existing items when 1) they aren't included a) in a new feed file that was uploaded to an FTP directory or b) in a merchant center account the next time that Search, Social, & Commerce syncs with it, or 2) when they don't map to existing campaigns or ad groups per the [!UICONTROL Map Only] settings in the template.

* *[!UICONTROL Delete]:* Delete the existing components.

* *[!UICONTROL Pause]:* Pause the existing components. They're reactivated if new data contains any of the same line items, and they retain their history and quality score. **Note:** If all of the child product groups for a parent product group are missing, then the parent product group is deleted because you can't pause product groups.

* *[!UICONTROL None]* (the default): Don't change the existing components.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** What to do with line items that include a stock level when:

* (For feeds with numeric-only stock values in the specified column) The stock level is at or below a specified quantity. The default quantity is zero (0).

* (For feeds with text values in the specified column) The value for [!UICONTROL Availability] is "[!UICONTROL out of stock]"; the value isn't case-sensitive. **Note:** **In feed templates, indicate text-based stock level columns using the check box for "[!UICONTROL This column has non-numeric values]."

Select the action for both cases:

* *[!UICONTROL Delete]* (the default) Delete the components.

* *[!UICONTROL Pause]:* Pause the components. When the data is updated, the components are reactivated if the numeric stock values go above the specified quantity or if the [!UICONTROL Availability] is "[!UICONTROL in stock]" or "[!UICONTROL preorder]". The components retain their history and quality score.

The stock level for each line item comes from a column in the feed file, as specified in the "[!UICONTROL Stock Level]" field for each template.

>[!TIP]
>
>* For products or services that you expect to restock or increase availability for, you should pause ad groups, keywords, and ads rather than deleting them and recreating them. Pausing allows them to retain their quality scores.
>* If you enable obsolete auto-processing for ad groups, and new data includes a stock level for the ad group, then it's meaningful to delete or pause the ad group only when the specified stock level is at the category level rather than at the brand/item level. For example, if you have an ad group "convertibles," then the stock level for the ad group should be the total for all individual convertible models represented in the ad group.

**[!UICONTROL Propagate feed data through all applicable templates]:** (Advertisers uploading data files via FTP or a merchant center account) Automatically propagates new data through the applicable templates. The option is selected by default. If you disable the option, then you can still manually propagate data for any feed file or account, or for any template.

>[!NOTE]
>
>* For FTP files, the feed service checks for updates in the FTP directory every two hours (even-numbered hours in the PST time zone). This option processes all files that were uploaded since the last check.
>* For merchant center accounts, Search, Social, & Commerce synchronizes with the account daily at approximately 06:00 in the advertiser's time zone. This option processes all data that was updated since the last sync.
>* Propagated data is available from the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] tabs until the data is posted to the ad network or to the [!UICONTROL Bulksheets] view.

**[!UICONTROL Post to the SE]:** (Advertisers uploading data files via FTP or a merchant center account) Automatically creates bulksheet files in the correct formats for the relevant ad networks after new data is propagated through the applicable templates. This option also removes the data from the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] tabs, unless any subcomponents have errors.

This option is disabled by default. To enable this option, select the check box and then specify whether to post bulksheet files to the ad networks:

* *[!UICONTROL Immediately]* (the default): Posts the bulk sheet files to the relevant ad networks after the data is propagated through the templates. The bulksheet files remain available in the [!UICONTROL Bulksheets] view for 30 days.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:** Doesn't post the bulksheet files to the relevant ad networks but lists them in the [!UICONTROL Bulksheets] view, from which you can post them later. The bulksheet files remain available in the [!UICONTROL Bulksheets] view for 30 days. When the bulksheet file is more than 10 MB but smaller than 2 GB, the file is in ZIP format; you don't need to unzip the file to post it. **Tip:** If you haven't previously validated your landing pages, then use this option so you can validate them from the [!UICONTROL Bulksheets] view before you post the data to the ad network.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** Precludes posting keyword phrases with more than a specified number of words to the ad network. When this option is selected, keyword phrases with more than the maximum number of words are propagated and listed on the [!UICONTROL Keywords] tab, but they aren't posted when you try to post the data.

This option is disabled by default so that all keywords are posted, regardless of how many words the phrase includes. If you select this option, select the maximum number of words to post (from 3-10).

>[!MORELIKETHIS]
>
>* [About inventory feeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propagate feed data through templates](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Post campaign data generated from feeds to ad networks](propagated-data-post.md)
