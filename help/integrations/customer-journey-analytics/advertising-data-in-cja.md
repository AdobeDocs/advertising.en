---
title: Adobe Advertising metrics and dimensions in Customer Journey Analytics
description: Reference the Adobe Advertising metrics and dimensions that are available in Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
---
# Adobe Advertising metrics and dimensions in Customer Journey Analytics

*Advertisers with an Adobe Advertising-Customer Journey Analytics Integration Only*

>[!NOTE]
>
>* Adobe Advertising passes traffic metrics and dimensions to [!DNL Customer Journey Analytics] daily.
>* [!DNL Web SDK] captures Adobe Advertising click-throughs and view-throughs in real time and passes them to Customer Journey Analytics.

## Adobe Advertising traffic metrics

<!-- Verify column names -->

>[!NOTE]
>
>* 
>* "XDM Field Name" is the field name in Adobe Experience Platform.
>* "XDM Field Display Name" indicates the display name within Customer Journey Analytics.

| Adobe Advertising Field Name | XDM Field Name | XDM Field Display Name | Source |
|------------------------------|----------------|------------------------|--------|
| Date | Date | All | |
| AMO ID | skwcid | Adobe Advertising ID | All |
| AMO Impressions | adobe_advertising_impressions | Adobe Advertising Impressions | All |
| AMO Clicks | adobe_advertising_clicks | Adobe Advertising Clicks | All |
| AMO Cost | adobe_advertising_cost | Adobe Advertising Cost | All |
| Currency Code | currency | Currency | All |
| AMO Views | adobe_advertising_views | Adobe Advertising Views | Ad Cloud DSP |
| AMO Views 25% Complete | adobe_advertising_views_25_pct | Adobe Advertising Views 25% Complete | Ad Cloud DSP |
| AMO Views 50% Complete | adobe_advertising_views_50_pct | Adobe Advertising Views 50% Complete | Ad Cloud DSP |
| AMO Views 75% Complete | adobe_advertising_views_75_pct | Adobe Advertising Views 75% Complete | Ad Cloud DSP |
| AMO Views 100% Complete | adobe_advertising_views_100_pct | Adobe Advertising Views 100% Complete | Ad Cloud DSP |
| AMO Minutes Viewed | adobe_advertising_minutes_viewed | Adobe Advertising Minutes Viewed | Ad Cloud DSP |
| AMO Viewable Impressions | adobe_advertising_viewable_impressions | Adobe Advertising Viewable Impressions | Ad Cloud DSP |
| AMO Not Viewable Impressions | adobe_advertising_not_viewable_impressions | Adobe Advertising Not Viewable Impressions | Ad Cloud DSP |
| AMO Measurable Impressions | adobe_advertising_measurable_impressions | Adobe Advertising Measurable Impressions | Ad Cloud DSP |

<!--
| Adobe Advertising Landing Page Views | adobe_advertising_landing_page_views | Adobe Advertising Landing Page Views | Meta Only |
| Adobe Advertising App Events | adobe_advertising_app_events | Adobe Advertising App Events | Meta Only |
| Adobe Advertising Engagements | adobe_advertising_engagements | Adobe Advertising Engagements | Meta Only |
| Adobe Advertising Ad Platform Conversions | adobe_advertising_ad_platform_conversions | Adobe Advertising Ad Platform Conversions | Meta Only |
| Adobe Advertising App Installs | adobe_advertising_app_installs | Adobe Advertising App Installs | Meta Only |
| Adobe Advertising Ad Platform Conversion Value | adobe_advertising_ad_platform_conversion_value | Adobe Advertising Ad Platform Conversion Value | Meta Only |
| Adobe Advertising Ad Platform Leads | adobe_advertising_ad_platform_leads | Adobe Advertising Ad Platform Leads | Meta Only |
| Adobe Advertising Page Like | adobe_advertising_page_like | Adobe Advertising Page Like | Meta Only |
| Adobe Advertising Phone Calls | adobe_advertising_phone_calls | Adobe Advertising Phone Calls | Meta Only |
| Adobe Advertising Messages | adobe_advertising_messages | Adobe Advertising Messages | Meta Only |
-->

## Adobe Advertising dimensions

>[!NOTE]
>
>* "XDM Field" is the field name in Adobe Experience Platform.
>* "XDM Field Display Name" indicates the display name within Customer Journey Analytics.

| Adobe Advertising Field Name | XDM Field Name | XDM Field Display Name | Source |
|------------------------------|----------------|------------------------|--------|
| Key | skwcid | Adobe Advertising ID |
| Ad Platform | adobe_advertising_ad_platform | Adobe Advertising Ad Platform |
| Account | adobe_advertising_account | Adobe Advertising Account |
| Campaign | adobe_advertising_campaign | Adobe Advertising Campaign |
| Ad Group | adobe_advertising_ad_group | Adobe Advertising Ad Group |
| Keyword | adobe_advertising_keyword | Adobe Advertising Keyword |
| Ad | adobe_advertising_ad | Adobe Advertising Ad |
| Placement | adobe_advertising_placement | Adobe Advertising Placement |
| Match Type | adobe_advertising_match_type | Adobe Advertising Match Type |
| Ad Title | adobe_advertising_ad_title | Adobe Advertising Ad Title |
| Ad Description | adobe_advertising_ad_description | Adobe Advertising Ad Description |
| Ad Destination URL | adobe_advertising_ad_destination_url | Adobe Advertising Ad Destination URL |
| Ad Display URL | adobe_advertising_ad_display_url | Adobe Advertising Ad Display URL |
| Device | adobe_advertising_device | Adobe Advertising Device |
| Keyword MatchType | adobe_advertising_keyword_matchtype | Adobe Advertising Keyword MatchType |
| Network | adobe_advertising_network | Adobe Advertising Network |
| Ad Type | adobe_advertising_ad_type | Adobe Advertising Ad Type |
| Product Target | adobe_advertising_product_target | Adobe Advertising Product Target |
| Landing Type | adobe_advertising_landing_type | Adobe Advertising Landing Type |
| Optimization | adobe_advertising_optimization | Adobe Advertising Optimization |

>[!MORELIKETHIS]
>
>* [Overview](overview.md)
>* [Prerequisites](prerequisites.md)
>* [Adobe Advertising IDs Used by [!DNL Customer Journey Analytics]](ids.md)
