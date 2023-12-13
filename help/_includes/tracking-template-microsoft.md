# Tracking Template field for Microsoft Advertising entities

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Optional; not available for all entities) The tracking template or tracking URL, which specifies all off-landing domain redirects and tracking parameters and also embeds the final/landing page URL in a parameter. Example: `{lpurl}?source={network}&id=5` or `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` to include a redirect.

For Adobe Advertising conversion tracking, which is applied when the campaign settings include "[!UICONTROL EF Redirect]" and "[!UICONTROL Auto Upload]," Search, Social, & Commerce automatically prefixes its own redirect and tracking code when you save the record.

* For supported parameters to embed the final URL, see the [[!DNL Microsoft Advertising] documentation on parameters to indicate the final URL](https://help.ads.microsoft.com/#apex/3/en/56799).

* You can optionally include URL parameters and any custom parameters defined for the campaign, separated by ampersands (&), such as {lpurl}?matchtype={matchtype}&device={device}.

* You can optionally add third-party redirects and tracking.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* The tracking template at the most granular level overrides the values at all higher levels. For example, if both the account settings and the keyword settings include a value, then the keyword value is applied.
>* You can update your tracking templates at any level without resubmitting your ads for approval.
