---
title: Adobe Advertising IDs Used by [!DNL Analytics]
description: Adobe Advertising IDs Used by [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
---
# Adobe Advertising IDs Used by [!DNL Analytics]

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

*Applicable to Advertising DSP and [!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising uses two IDs for on-site performance tracking:  the *EF ID* and the *AMO ID*.

When an ad impression occurs, Adobe Advertising creates the AMO ID and EF ID values and stores them. When a visitor who has seen an ad enters the site without clicking an ad, [!DNL Analytics] calls these values from Adobe Advertising through the [!DNL Analytics for Advertising] JavaScript code. For view-through traffic, [!DNL Analytics] generates a supplemental ID (`SDID`), which is used to stitch the EF ID and AMO ID into [!DNL Analytics]. For click-through traffic, these IDs are included in the landing page URL using the `ef_id` and `s_kwcid` (for the AMO ID) query string parameters.

Adobe Advertising distinguishes between a click-through or view-through entry to the website using the following criteria:

* A view-through entry is captured when a user visits the site after viewing an ad but not clicking it. [!DNL Analytics] records a view-through if two conditions are met:

    * The visitor has no click-throughs for a [!DNL DSP] or [!DNL Search, Social, & Commerce] ad during the [click lookback window](/help/integrations/analytics/prerequisites.md#lookback-a4adc).

    * The visitor has seen at least one [!DNL DSP] ad during the [impression lookback window](/help/integrations/analytics/prerequisites.md#lookback-a4adc). The last impression is passed as the view-through.

* A click-through entry is captured when a site visitor clicks an ad before entering the site. [!DNL Analytics] captures a click-through when either of the following conditions occurs:

    * The URL includes an EF ID and AMO ID as added to the landing page URL by Adobe Advertising.

    * The URL contains no tracking codes, but the Adobe Advertising JavaScript code detects a click within the last two minutes.

![Adobe Advertising view-based [!DNL Analytics] integration](/help/integrations/assets/a4adc-view-through-process.png)

*Figure 1: Adobe Advertising view-based [!DNL Analytics] integration*

![Adobe Advertising click URL-based [!DNL Analytics] integration](/help/integrations/assets/a4adc-click-through-process.png)

*Figure 2: Adobe Advertising click URL-based [!DNL Analytics] integration*

## Adobe Advertising EF IDs

The EF ID is a unique token that Adobe Advertising uses to associate activity with an online click or ad exposure at the individual browser or device level. EF IDs act primarily as keys for sending [!DNL Analytics] data and Customer Journey Analytics data to Adobe Advertising for reporting and bid optimization within Adobe Advertising.

For [!DNL Analytics], the EF ID is stored in [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) or [!DNL rVar] (reserved [!DNL eVar]) dimension (Adobe Advertising EF ID).

For Customer Journey Analytics, the EF ID is stored in the `trackingIdentities` property of the `conversionDetails` object, which is part of [the [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension).

### EF ID Formats {#ef-id-formats}

>[!NOTE]
>
>EF IDs are case-sensitive. If an [!DNL Analytics] or Customer Journey Analytics implementation forces URL tracking to lowercase, then Adobe Advertising doesn't recognize the EF ID. This impacts Adobe Advertising bidding and reporting but has no impact on Adobe Advertising reporting within [!DNL Analytics] or Customer Journey Analytics.

#### [!DNL Google Ads] search ads

```
{gclid}:G:s
```

where:

* `gclid` is the [!DNL Google Click ID] (GCLID).
* `s` is the network type ("s" for search).

#### [!DNL Microsoft Advertising] search ads

```
{msclkid}:G:s
```

where:

* `msclkid` is the [!DNL Microsoft Click ID] (MSCLKID).
* `s` is the network type ("s" for search).

#### Display ads and search ads on other search engines 

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

where:

* <*Adobe Advertising visitor ID*> is a unique ID per visitor (such as UhKVaAAABCkJ0mDt). Also called the *surfer ID*.

* <*timestamp*> is the time in the format YYYYMMDDHHMMSS (such as 20190821192533 for Year 2019, Month 08, Day 21, Time 19:25:33).

* <*channel type*> is the channel type responsible for the click or exposure:

    * `d` for a click on a DSP display ad (display click-through)
    * `i` for an impression of a DSP display ad (display view-through)
    * `s` for a click on a Search ad (search click-through).

Example `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### The EF ID Dimension in [!DNL Analytics]

In [!DNL Analytics] reports, you can find EF ID data by searching for the [!UICONTROL EF ID] dimension and using the [!UICONTROL EF ID Instance] metric.

EF IDs are subject to the 500k unique identifier limit in Analysis Workspace. Once the 500k value is reached, all new tracking codes are reported under the one-line-item title "[!UICONTROL Low Traffic]." Because of the possibility of missing reporting fidelity, the EF IDs are not classified, and you should not use them for segments or reporting in [!DNL Analytics].

<!-- ## Adobe Advertising AMO IDs {#amo-id} -->

{{$include /help/_includes/amo-id.md}}

### Ways to Implement the AMO ID {#amo-id-implement}

The parameter is added to your tracking URLs in one of the following ways:

* (Recommended) When the server-side insertion feature is implemented.

  * DSP customers: The pixel server automatically appends the s_kwcid parameter to your landing page suffixes when an end user views a display ad with the Adobe Advertising pixel.

  * Search, Social, & Commerce customers:

    * For [!DNL Google Ads] and [!DNL Microsoft Advertising] accounts with the [!UICONTROL Auto Upload] setting enabled for the account or campaign, the pixel server automatically appends the s_kwcid parameter to your landing page suffixes when an end user clicks an ad with the Adobe Advertising pixel.
    
    * For other ad networks, or [!DNL Google Ads] and [!DNL Microsoft Advertising] accounts with the [!UICONTROL Auto Upload] setting disabled, manually add the parameter to your [account-level append parameters](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, which append it to your base URLs.

* When the server-side insertion feature isn't implemented:

  * DSP customers: The [JavaScript code](javascript.md) automatically records click-throughs and view-throughs. When a browser doesn't support third-party cookies, you can still track click-based conversions for the following ad types:

    * For [!DNL Flashtalking] ad tags, manually insert additional macros per "[Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md)." **Note:** This procedure isn't necessary if your organization has a direct partnership with [!DNL Flashtalking] and you use data-pass macros to track the `s_kwcid` and `ef_id` tracking parameters per the [!DNL Flashtalking] support documentation at [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros).

    * For [!DNL Google Campaign Manager 360] ad tags, manually insert additional macros per "[Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md)."

  * Search, Social, & Commerce customers:
  
    * For ([!DNL Google Ads] and [!DNL Microsoft Advertising]) ads, manually add the AMO ID parameter to your landing page suffixes, ideally at the [account level](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} unless different tracking for individual account components is necessary.

    * For ads on all other ad networks, manually add the AMO ID parameter to your [account-level append parameters](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, which append it to your base URLs.

To implement the server-side insertion feature, or to determine the best option for your business, talk to your Adobe Account Team.

### AMO ID Dimension in [!DNL Analytics]

In Analytics reports, you can find AMO ID data by searching for the [!UICONTROL AMO ID] dimension and using the [!UICONTROL AMO ID Instances] metric. The [!UICONTROL AMO ID] dimension houses all AMO ID values captured, whereas the [!UICONTROL AMO ID Instances] metric indicates how often an AMO ID value was captured by the site. For example, if the same search ad was clicked four times but Analytics tracked seven site entries, then [!UICONTROL AMO ID Instances] would be seven (7) and [!UICONTROL Clicks] would be four (4).

For any reporting or auditing within [!DNL Analytics], the best practice is to use the AMO ID along with its corresponding instance. For more information, see "[Click-Through Data Validation for [!DNL Analytics for Advertising]](data-variances.md#data-validation)" in "Expected Data Variances Between [!DNL Analytics] and Adobe Advertising."

## About Analytics Classifications

In [!DNL Analytics], a [classification](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) is a piece of metadata for a given tracking code, such as Account, Campaign, or Ad. Adobe Advertising categorizes raw Adobe Advertising data using classifications so that you can display the data in different ways (such as by Ad Type or Campaign) when you generate reports. Classifications form the basis of Adobe Advertising reporting in [!DNL Analytics] and can be used with the AMO metrics, such as [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions], and [!UICONTROL AMO Clicks], as well as with custom and standard on-site events like [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders], and [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising]](overview.md)
>* [Expected Data Variances Between [!DNL Analytics] and Adobe Advertising](data-variances.md)
