# Snippets

## Tracking Template field for Google Ads entities {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

**[!UICONTROL Tracking Template]:** (Optional) The tracking template or tracking URL, which specifies all off-landing domain redirects and tracking parameters and also embeds the final/landing page URL in a [!DNL ValueTrack] parameter. Example: `{lpurl}?source={network}&id=5` or `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` to include a redirect.

For Adobe Advertising conversion tracking, which is applied when the campaign settings include "[!UICONTROL EF Redirect]" and "[!UICONTROL Auto Upload]," Search, Social, & Commerce automatically prefixes its own redirect and tracking code when you save the record.

* For supported parameters to embed the final URL, see the [[!DNL Google Ads] documentation for the supported [!DNL ValueTrack] formats](https://support.google.com/google-ads/answer/6305348). (Go to the "Tracking template only" parameters in the section on "Available ValueTrack Parameters.")

* You can optionally include URL parameters and any custom parameters defined for the campaign, separated by ampersands (&), such as {lpurl}?matchtype={matchtype}&device={device}.

* You can optionally add third-party redirects and tracking.

>[!NOTE]
>
>* Avoid using macros, which aren't substituted for clicks from sources that enable parallel tracking. If the advertiser must use macros, then the Adobe Account Team should work with Customer Support or the implementation team to add them.
>* The tracking template at the most granular level overrides the values at all higher levels. For example, if both the account settings and the keyword settings include a value, then the keyword value is applied.
>* If you update a tracking template at the ad, sitelink, or keyword level, then the relevant ads are resubmitted for review. You can update your tracking templates at the account, campaign, or ad group levels without resubmitting your ads for approval.

## Tracking Template field for Microsoft Advertising entities {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Optional) The tracking template or tracking URL, which specifies all off-landing domain redirects and tracking parameters and also embeds the final/landing page URL in a parameter. Example: `{lpurl}?source={network}&id=5` or `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` to include a redirect.

For Adobe Advertising conversion tracking, which is applied when the campaign settings include "[!UICONTROL EF Redirect]" and "[!UICONTROL Auto Upload]," Search, Social, & Commerce automatically prefixes its own redirect and tracking code when you save the record.

* For supported parameters to embed the final URL, see the [[!DNL Microsoft Advertising] documentation on parameters to indicate the final URL](https://help.ads.microsoft.com/#apex/3/en/56799).

* You can optionally include URL parameters and any custom parameters defined for the campaign, separated by ampersands (&), such as {lpurl}?matchtype={matchtype}&device={device}.

* You can optionally add third-party redirects and tracking.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* The tracking template at the most granular level overrides the values at all higher levels. For example, if both the account settings and the keyword settings include a value, then the keyword value is applied.
>* You can update your tracking templates at any level without resubmitting your ads for approval.

## Text ad template - Note explaining how to insert a dynamic parameter {#inventory-feed-template-insert-dynamic-parameter}

To insert a column name or modifier group as a dynamic parameter, click in the input field, and then click a column name in the column list or a [modifier name](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) in the Modifiers list. To insert the [!DNL Param1] or [!DNL Param2] variable, enter the value `{param1:default text}` or `{param2:default text}`, where &quot;default text&quot; is text that is used if the parameter column in the feed file is empty for an ad row.

## Text ad template - Note explaining how to insert a an ad customizer {#inventory-feed-template-insert-ad-customizer}

To insert an ad customizer, use the following formats, where `Default text` is an optional value to insert when your feed file doesn't include a valid value:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, such as `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, such as `{CUSTOMIZER.Discount:10%}`
