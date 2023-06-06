# Tracking Template field for Yahoo! Japan Ads entities

<!-- Search CRUD and bulk edit of Yahoo! Japan Ads entity settings -->

**[!UICONTROL Tracking Template]:** (Optional) The tracking template or tracking URL, which specifies all off-landing domain redirects and tracking parameters and also embeds the final/landing page URL in a parameter. Use the parameter `!{lpurl}` to indicate the landing page URL. Example: `{lpurl}?source={network}&id=5` or `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` to include a redirect.

You can optionally add third-party redirects and tracking.

For Adobe Advertising conversion tracking, which is applied when the campaign settings include "[!UICONTROL EF Redirect]" and "[!UICONTROL Auto Upload]," Search, Social, & Commerce automatically prefixes its own redirect and tracking code when you save the record.

>[!NOTE]
>
>* The tracking template at the most granular level overrides the values at all higher levels. For example, if both the account settings and the keyword settings include a value, then the keyword value is applied.
>* You can update your tracking templates at any level without resubmitting your ads for approval.
