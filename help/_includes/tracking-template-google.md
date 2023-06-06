# Tracking Template field for Google Ads entities

<!-- Search CRUD and bulk edit of Google entity settings -->

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
