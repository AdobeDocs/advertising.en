---
title: Optional tracking parameters for click-tracking URLs
description: Learn about optional Search, Social, & Commerce tracking parameters and ad network-specific tracking parameters that you can add to your click-tracking URLs.
exl-id: ca619e55-14b1-4768-b866-e339ae2ca6d4
---
# Optional tracking parameters for click-tracking URLs

*Google Ads, Microsoft Advertising, and Yahoo! Japan accounts only*

Instead of using only the standard tracking parameters for a final URL or destination URL, you may add more parameters to track specific data for an ad network account. You can add add any combination of the following parameters in the account settings or the campaign settings:

* You can append any static text string as a parameter in the base URLs for the account/campaign.

* You can append Adobe Advertising- and ad network-specific parameters in the base URLs for the account/campaign to track more data:

  * Adobe Advertising parameters are semi-static. Adobe Advertising inserts a data value when it uploads the base URL to the ad network. For example, when you append `campaign={ef_campaign}` to the base URL, Adobe Advertising replaces `{ef_campaign}` with the actual campaign name (such as "Back-to-school-Campaign") when it uploads the URL.
  
    **Note:** Once the values are inserted, they remain static. If you move a keyword or ad to a different ad group, or move the ad group to a different campaign, then the  {ef_adgroup} or {ef_campaign} parameter isn't automatically updated, so you must manually generate a new destination URL or base (final) URL.

  * Ad network-specific parameters are dynamic, and the search engine inserts a data value when the user clicks an ad. For example, when you append `{param1}` to the base URL, the ad network replaces it with the actual {param1} value when an end user clicks the ad.

>[!NOTE]
>
>* Separate multiple parameters with commas or ampersands (`&`).
>* The following parameters aren't case-sensitive.
>* Special characters in the appended parameters are substituted as follows in the generated destination URL or base (final) URl:
>  * `=` is substituted with `%3D`
>  * `?` is substituted with `%26`
>  * an empty space is substituted with `%2B`
>  For example, when you append the parameter `campaign={ef_campaign}` to the base URL http://www.example.com for a keyword, then the base URL for that keyword is generated as `http://www.example.com/campaign%3D{ef_campaign}`.

## Search, Social, & Commerce static tracking parameters

You can use the following parameters for accounts on any ad network and can combine them with parameters for a specific ad network as needed. Some of these parameters duplicate the parameters that are added automatically for specific ad networks when the account's tracking method is "[!UICONTROL EF Direct]."

All of the following parameters must be specified as a key-value pair; you can include multiple parameters for one value pair. For example, to insert the campaign name, use `<your_parameter_name>={ef_campaign}`, such as `campaign={ef_campaign}`. To insert the match type using specified match type names, use `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`, such as `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. The non-applicable match types don't appear in the resulting URL.

| Parameter | Description |
| ---- | ---- |
| <code>{custom_code}</code> | To insert data from the "Custom URL Param" column in an uploaded bulksheet file into the tracking URL. {custom_code} may be used only at the end of the value of one or more key-value pairs in the tracking URL. Examples:  <code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&b={custom_code}</code><br><br><b>Note:</b> To insert the custom value from the bulksheet file into the tracking URL, upload the bulksheet file using the "Generate Tracking URLs" option. For more information about using bulksheet files, see "[About managing campaign data using bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)." |
| <code>{ef_uniqueid}</code> | To insert the unique ID created by Adobe Advertising. Added automatically when the tracking method is "EF Redirect." |
| <code>{ef_userid}</code> | To insert the unique user ID that Adobe Advertising assigns to the advertiser. |
| <code>{ef_sid}</code> | To insert the numeric ID that Search, Social, & Commerce assigns to the ad network: <i>[!UICONTROL 3]</i> for [!DNL Google Ads], <i>[!UICONTROL 10]</i> for [!DNL Microsoft&reg; Advertising], <i>[!UICONTROL 45]</i> for [!DNL Meta], <i>[!UICONTROL 86]</i> for [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> for [!DNL Naver], <i>[!UICONTROL 88]</i> for [!DNL Baidu], <i>[!UICONTROL 90]</i> for [!DNL Yandex], <i>[!UICONTROL 94]</i> for [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> for [!DNL Yahoo Native] (deprecated), or <i>[!UICONTROL 106]</i> for [!DNL Pinterest] (deprecated). |
| <code>{ef_searchengine}</code> | To insert the ad network name. |
| <code>{ef_campaign}</code> | To insert the campaign name. |
| <code>{ef_campaignid}</code> | To insert the campaign ID. <b>Note:</b> The ID for a new campaign isn't created until the campaign is posted to the ad network. If the account uses the "[!UICONTROL EF Redirect]" and "AutoUpload" options, then Adobe Advertising automatically inserts the campaign ID in the relevant destination URLs or final URLs the next day. If the account doesn't use the "[!UICONTROL EF Redirect]" and [!UICONTROL Auto Upload]" options and you want to insert the campaign ID in the relevant destination URLs or final URLs, you must create the campaign; download a bulksheet file for the new campaign, using the option to "Generate Tracking URLs;" and then post the file to the ad network. |
| <code>{ef_adgroup}</code> | To insert the ad group name. |
| <code>{ef_adgroupid}</code> | To insert the ad group ID. <b>Note:</b> The ID for a new ad group isn't created until the ad group is posted to the ad network. If the account uses the "[!UICONTROL EF Redirect]" and "AutoUpload" options, then Adobe Advertising automatically inserts the ad group ID in the relevant destination URLs or final URLs the next day. If the account doesn't use the[!UICONTROL EF Redirect]" and [!UICONTROL Auto Upload]" options and you want to insert the ad group ID in the relevant destination URLs or final URLs, then you must create the ad group; download a bulksheet file for the new ad group, using the option to "Generate Tracking URLs;" and then post the file to the ad network. |
| <code>{ef_keyword}</code> | To insert the keyword. |
| <code>{ef_keywordid}</code> | To insert the keyword ID. <b>Note:</b> The ID for a new keyword isn't created until the keyword is posted to the ad network. If the account uses the "[!UICONTROL EF Redirect]" and [!UICONTROL Auto Upload]" options, then Adobe Advertising automatically inserts the keyword ID in the relevant destination URLs or final URLs the next day. If the account doesn't use the "[!UICONTROL EF Redirect]" and [!UICONTROL Auto Upload]" options and you want to insert the keyword ID in the relevant destination URLs or final URLs, then you must create the keyword; download a bulksheet file for the new keyword, using the option to "Generate Tracking URLs;" and then post the file to the ad network. |
| <code>{ef_matchtype}</code> | To insert the keyword match type as "Broad," "Exact,"or "Phrase." Included automatically for Google Ads and Microsoft Advertising with the "[!UICONTROL EF Redirect]" tracking method. |
| <code>{ef_adid}</code> | To insert the ad ID. <b>Note:</b> The ID for a new ad isn't created until the ad is posted to the ad network. If the account uses the "[!UICONTROL EF Redirect]" and [!UICONTROL Auto Upload]" options, then Adobe Advertising automatically inserts the ad ID in the relevant destination URLs or final URLs the next day. If the account doesn't use the "[!UICONTROL EF Redirect]" and [!UICONTROL Auto Upload]" options and you want to insert the ad ID in the relevant destination URLs or final URLs, then you must create the ad; download a bulksheet file for the new ad, using the option to "Generate Tracking URLs;" and then post the file to the ad network. |

## Google Ads dynamic tracking parameters

See [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## Microsoft Advertising dynamic tracking parameters

See [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Yahoo Native dynamic tracking parameters

See [https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters](https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters).

## Yahoo! Japan Ads dynamic tracking parameters

See [https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## Yandex dynamic tracking parameters

See [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [About click-tracking URL formats for the Adobe Advertising conversion tracking service](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
