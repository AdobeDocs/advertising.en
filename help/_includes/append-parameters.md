# Append Parameters field in account and campaign settings

**[!UICONTROL Append Parameters]:** (Optional) Any additional tracking parameters to append to the base URLs.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. The advertiser-level append parameters are included by default at the account level and the campaign level, but you can override either.

You can use any static text string, including third-party tracking parameters, or any of the [supported tracking parameters](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md), which insert an appropriate data value in the base URL.

Separate multiple parameters with commas or ampersands (&). Nested brackets aren't supported.

**Notes:**

* Changes to append parameters aren't controlled by the [!UICONTROL Auto Upload] option. If you change the append parameters for existing base URLs, then new URLs aren't generated automatically. Add the new parameters by downloading a bulksheet file for the account or campaign, updating the [!UICONTROL Base URL/Final URL] fields, and then uploading and posting the bulksheet.

* (Ad networks with parallel tracking) Avoid using macros, which aren't substituted for clicks from sources that enable parallel tracking. If the advertiser must use macros, then the Adobe Account Team should work with Customer Support or the implementation team to add them.

* (Advertisers with an Adobe Advertising-Adobe Analytics integration) To include an AMO ID parameter to send Search, Social, & Commerce data to [!DNL Analytics], see the [ad network-specific formats](/help/search-social-commerce/tracking/amo-id-tracking-parameter.md). It's not necessary to manually add the parameter for [!DNL Google Ads] and [!DNL Microsoft Advertising] accounts with a server-side AMO ID implementation.
