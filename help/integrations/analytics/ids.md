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

    * The visitor has no click-throughs for a [!DNL DSP] or [!DNL Search, Social, & Commerce] ad during the [click lookback window](#lookback-a4adc).

    * The visitor has seen at least one [!DNL DSP] ad during the [impression lookback window](#lookback-a4adc). The last impression is passed as the view-through.

* A click-through entry is captured when a site visitor clicks an ad before entering the site. [!DNL Analytics] captures a click-through when either of the following conditions occurs:

    * The URL includes an EF ID and AMO ID as added to the landing page URL by Adobe Advertising.

    * The URL contains no tracking codes, but the Adobe Advertising JavaScript code detects a click within the last two minutes.

![Adobe Advertising view-based [!DNL Analytics] integration](/help/integrations/assets/a4adc-view-through-process.png)

*Figure 1: Adobe Advertising view-based [!DNL Analytics] integration*

![Adobe Advertising click URL-based [!DNL Analytics] integration](/help/integrations/assets/a4adc-click-through-process.png)

*Figure 2: Adobe Advertising click URL-based [!DNL Analytics] integration*

## Adobe Advertising EF IDs

The EF ID is a unique token that Adobe Advertising uses to associate activity with an online click or ad exposure. The EF ID is stored in [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) or [!DNL rVar] (reserved [!DNL eVar]) dimension (Adobe Advertising EF ID) and tracks each ad click or exposure at the individual browser or device level. EF IDs act primarily as keys for sending [!DNL Analytics] data to Adobe Advertising for reporting and bid optimization within Adobe Advertising.

### EF ID Format

>[!NOTE]
>
>EF IDs are case-sensitive. If an [!DNL Analytics] implementation forces URL tracking to lowercase, then Adobe Advertising doesn't recognize the EF ID. This impacts Adobe Advertising bidding and reporting but has no impact on Adobe Advertising reporting within [!DNL Analytics].

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

EF IDs are subject to the 500k unique identifier limit in Analysis Workspace. Once the 500k value is reached, all new tracking codes are reported under the one-line-item title “[!UICONTROL Low Traffic].” Because of the possibility of missing reporting fidelity, the EF IDs are not classified, and you should not use them for segments or reporting in [!DNL Analytics].

## Adobe Advertising AMO IDs {#amo-id}

The AMO ID tracks each unique ad combination at a less granular level and is used for [!DNL Analytics] data classification and ingestion of advertising metrics (such as impressions, clicks, and cost) from Adobe Advertising. The AMO ID is stored in an [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) or rVar dimension (AMO ID) and is used exclusively for reporting in [!DNL Analytics].

The AMO ID is also called the `s_kwcid`, which is sometimes pronounced as "[!DNL squid]."

### Ways to Implement the AMO ID {#amo-id-implement}

The parameter is added to your tracking URLs in one of the following ways:

* (Recommended) When the server-side insertion feature is implemented.

  * DSP customers: The pixel server automatically appends the s_kwcid parameter to your landing page suffixes when an end user views a display ad with the Adobe Advertising pixel.

  * Search, Social, & Commerce customers:

    * For [!DNL Google Ads] and [!DNL Microsoft Advertising] accounts with the [!UICONTROL Auto Upload] setting enabled for the account or campaign, the pixel server automatically appends the s_kwcid parameter to your landing page suffixes when an end user clicks an ad with the Adobe Advertising pixel.
    
    * For other ad networks, or [!DNL Google Ads] and [!DNL Microsoft Advertising] accounts with the [!UICONTROL Auto Upload] setting disabled, manually add the parameter to your [account-level append parameters](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, which append it to your base URLs.

* When the server-side insertion feature isn't implemented:

  * DSP customers: The [JavaScript code](javascript.md) automatically records click-throughs and view-throughs. When a browser doesn't support third-party cookies, you can still track click-based conversions for the following ad types:

    * For [!DNL Flashtalking] ad tags, manually insert additional macros per "[Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md)."

    * For [!DNL Google Campaign Manager 360] ad tags, manually insert additional macros per "[Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md)."

  * Search, Social, & Commerce customers:
  
    * For ([!DNL Google Ads] and [!DNL Microsoft Advertising]) ads, manually add the AMO ID parameter to your landing page suffixes, ideally at the [account level](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} unless different tracking for individual account components is necessary.

    * For ads on all other ad networks, manually add the AMO ID parameter to your [account-level append parameters](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, which append it to your base URLs.

To implement the server-side insertion feature, or to determine the best option for your business, talk to your Adobe Account Team.

### AMO ID Formats {#amo-id-formats}

#### AMO ID Format for [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

where:

* `AC` indicates the display channel.

* `{TM_AD_ID}` is the Adobe Advertising-generated alphanumeric ad key. It's used an unique identifier for an ad and serves as a key for translating Adobe Advertising entity metadata into readable [!DNL Analytics] dimensions.

* `{TM_PLACEMENT_ID}` is the Adobe Advertising-generated alphanumeric placement key. It's used an unique identifier for a placement and serves as a key for translating Adobe Advertising entity metadata into readable [!DNL Analytics] dimensions.

Example AMO ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### AMO ID formats for Search, Social, & Commerce ads {#amo-id-format-search}

The parameters vary by ad network, but the following parameters are common to all:

* `AL` indicates the search channel. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` is a unique user ID assigned to the advertiser.

* `{sid}` is replaced by the numeric ID for the advertiser's ad network account: *3* for [!DNL Google Ads], *10* for [!DNL Microsoft Advertising], *45* for [!DNL Meta], *86* for [!DNL Yahoo! Display Network], *87* for [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL Yahoo! Japan Ads], *105* for [!DNL Yahoo Native] (deprecated), or *106* for [!DNL Pinterest] (deprecated).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

where:

* `{creative}` is the ad network's unique numeric ID for the creative.
* `{placement}` is the website on which the ad was clicked.
* `{keywordid}` is the ad network's unique numeric ID for the keyword that triggered the ad.

##### [!DNL Google Ads]

These including shopping campaigns using [!DNL Google Merchant Center].

* Accounts that use the latest AMO ID format, which supports campaign- and ad group-level reporting for performance max campaigns and drafts and experiments campaigns:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* All other accounts:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

where:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` is the [!DNL Google Ads] unique numeric ID for the creative.
* `{matchtype}` is the matchtype of the keyword that triggered the ad: `e` for exact, `p` for phrase, or `b` for broad.
* `{placement}` is the domain name of the website on which the ad was clicked. A value is available for ads in placement-targeted campaigns and for ads in keyword-targeted campaigns that are displayed on content sites.
* `{network}` indicates the network from which the click occurred: `g` for [!DNL Google] search (for keyword-targeted ads only), `s` for a search partner (for keyword-targeted ads only), or `d` for the display network (for either keyword-targeted or placement-targeted ads).
* `{product_partition_id}` is the ad network's unique numeric ID for the product group used with product ads.
* `{keyword}` is either the specific keyword that triggered your ad (on search sites) or the best-matching keyword (on content sites).
* `{campaignid}` is the ad network's unique numeric ID for the campaign.
* `{adgroupid}` is the the ad network's unique numeric ID for the ad group.

>[!NOTE]
>
>* For dynamic search ads, {keyword} is populated with the auto target.
>* When you generate tracking for [!DNL Google] shopping ads, a product ID parameter, `{adwords_producttargetid}`, is inserted before the keyword parameter. The product ID parameter doesn't appear in the [!DNL Google Ads] account-level and campaign-level tracking parameters.
>* To use the latest AMO ID tracking code, see "[Update the AMO ID tracking code for a [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)." <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* All campaign types:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

where:

* `{AdId}` is the ad network's unique numeric ID for the creative.
* `{OrderItemId}` is the ad network's numeric ID for the keyword.
* `{CampaignId}` is the ad network's unique numeric ID for the campaign.
* `{AdGroupId}` is the ad network's unique numeric ID for the ad group.

>[!NOTE]
>
>All accounts with performance max campaigns were migrated to the above format. For accounts with other campaign types, your landing page suffixes will be migrated to use the new s_kwcid format by early 2025. In the meantime, the legacy formats, as follows, still work: 
>* Search campaigns:
>  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Shopping campaigns (using [!DNL Microsoft Merchant Center]):
>  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`
>* Audience network campaigns:
>  `s_kwcid=AL!{userid}!{sid}!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

where:

* `{creative}` is the ad network's unique numeric ID for the creative.
* `{matchtype}` is the matchtype of the keyword that triggered the ad: `be` for exact, `bp` for phrase, or `bb` for broad.
* `{network}` indicates the network from which the click occurred: `n` for native or `s` for search.
* `{keyword}` is the keyword that triggered your ad.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

where:

* `{ad_id}` is the ad network's unique numeric ID for the creative.
* `{source_type}` is the type of site on which the ad has been displayed: *b* for search, *c* for context (content), or *ct* for category.
* `{phrase_id}` is the ad network's numeric ID for the keyword.

### AMO ID Dimension in [!DNL Analytics]

In Analytics reports, you can find AMO ID data by searching for the [!UICONTROL AMO ID] dimension and using the [!UICONTROL AMO ID Instances] metric. The [!UICONTROL AMO ID] dimension houses all AMO ID values captured, whereas the [!UICONTROL AMO ID Instances] metric indicates how often an AMO ID value was captured by the site. For example, if the same search ad was clicked four times but Analytics tracked seven site entries, then [!UICONTROL AMO ID Instances] would be seven (7) and [!UICONTROL Clicks] would be four (4).

For any reporting or auditing within [!DNL Analytics], the best practice is to use the AMO ID along with its corresponding instance. For more information, see "[Click-Through Data Validation for [!DNL Analytics for Advertising]](data-variances.md#data-validation)" in "Expected Data Variances Between [!DNL Analytics] and Adobe Advertising."

## About Analytics Classifications

In [!DNL Analytics], a [classification](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) is a piece of metadata for a given tracking code, such as Account, Campaign, or Ad. Adobe Advertising categorizes raw Adobe Advertising data using classifications so that you can display the data in different ways (such as by Ad Type or Campaign) when you generate reports. Classifications form the basis of Adobe Advertising reporting in [!DNL Analytics] and can be used with the AMO metrics, such as [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions], and [!UICONTROL AMO Clicks], as well as with custom and standard on-site events like [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders], and [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising]](overview.md)
>* [Expected Data Variances Between [!DNL Analytics] and Adobe Advertising](data-variances.md)
