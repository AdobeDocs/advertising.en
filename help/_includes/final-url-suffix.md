# Final URL Suffix definition

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** ([!DNL Google Ads] and [!DNL Microsoft Advertising] accounts only; optional) Any parameters to append to the end of final URLs to track information; include all parameters that your business must track. Example:`param1=value1&param2=value2`

In accounts that use Adobe Advertising conversion tracking, the suffix must include the ad network's click identifier (`msclkid` for [!DNL Microsoft Advertising]; `gclid` for [!DNL Google Ads]).

Accounts with an Adobe Analytics integration must use the s_kwcid parameter. If the account has a server-side s_kwcid implementation, then the parameter is added automatically when a user clicks an ad; otherwise, you must manually add it here. See the [required suffix formats for [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) and [required suffix formats for [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* This field isn't updated by the [!UICONTROL Auto Upload] tracking setting.
>* Final URL suffixes at lower levels override the account-level suffix. For easier maintenance, use only the account-level suffix unless different tracking for individual account components is necessary. To configure a suffix at the ad group level or lower, use the ad network's editor.
