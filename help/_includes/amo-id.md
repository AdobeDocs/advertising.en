# Adobe Advertising AMO IDs {#amo-id}

## Adobe Advertising AMO IDs {#amo-id}

The AMO ID tracks each unique ad combination at a less granular level and is used for [!DNL Analytics] and Customer Journey Analytics data classification and ingestion of advertising metrics (such as impressions, clicks, and cost) from Adobe Advertising.

For [!DNL Analytics], the AMO ID is stored in an [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) or rVar dimension (AMO ID).

For Customer Journey Analytics, the AMO ID is stored in the `trackingCode` property of the `conversionDetails` object, which is part of the [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension].

The AMO ID is also called the `s_kwcid`, which is sometimes pronounced as "[!DNL squid]."

### ([!DNL Analytics] users) Ways to Implement the AMO ID {#amo-id-implement}

<!-- Add info about implementing in CJA -->

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

### AMO ID Formats {#amo-id-formats}

#### AMO ID Format for [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

where:

* `AC` indicates the display channel.

* `{TM_AD_ID}` is the Adobe Advertising-generated alphanumeric ad key. It's used an unique identifier for an ad and serves as a key for translating Adobe Advertising entity metadata into readable [!DNL Analytics] and Customer Journey Analytics dimensions.

* `{TM_PLACEMENT_ID}` is the Adobe Advertising-generated alphanumeric placement key. It's used an unique identifier for a placement and serves as a key for translating Adobe Advertising entity metadata into readable [!DNL Analytics] and Customer Journey Analytics dimensions.

Example AMO ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### AMO ID formats for Search, Social, & Commerce ads {#amo-id-format-search}

The parameters vary by ad network, but the following parameters are common to all:

* `AL` indicates the search channel. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` is a unique user ID assigned to the advertiser.

* `{sid}` is replaced by the numeric ID for the advertiser's ad network account: *3* for [!DNL Google Ads], *10* for [!DNL Microsoft Advertising], *45* for [!DNL Meta], *86* for [!DNL Yahoo! Display Network], *87* for [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL Yahoo! Japan Ads], *105* for [!DNL Yahoo Native] (deprecated), or *106* for [!DNL Pinterest] (deprecated).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!88!{creative}!{placement}!{keywordid}`

where:

* `{creative}` is the ad network's unique numeric ID for the creative.
* `{placement}` is the website on which the ad was clicked.
* `{keywordid}` is the ad network's unique numeric ID for the keyword that triggered the ad.

##### [!DNL Google Ads]

These including shopping campaigns using [!DNL Google Merchant Center].

* Accounts that use the latest AMO ID format, which supports campaign- and ad group-level reporting for performance max campaigns and drafts and experiments campaigns:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* All other accounts:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

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

`s_kwcid=AL!{userid}!45!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* All campaign types:

  `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

where:

* `{AdId}` is the ad network's unique numeric ID for the creative.
* `{OrderItemId}` is the ad network's numeric ID for the keyword.
* `{CampaignId}` is the ad network's unique numeric ID for the campaign.
* `{AdGroupId}` is the ad network's unique numeric ID for the ad group.

>[!NOTE]
>
> For accounts with campaigns without the [!UICONTROL Auto Upload] tracking option that weren’t already migrated to the new format, manually update each landing page suffix to include the above format.
>In the meantime, the legacy formats, as follows, still work: 
>* Search campaigns:
>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Shopping campaigns (using [!DNL Microsoft Merchant Center]):
>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Audience network campaigns:
>  `s_kwcid=AL!{userid}!10!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!94!{creative}!{matchtype}!{network}!{keyword}`

where:

* `{creative}` is the ad network's unique numeric ID for the creative.
* `{matchtype}` is the matchtype of the keyword that triggered the ad: `be` for exact, `bp` for phrase, or `bb` for broad.
* `{network}` indicates the network from which the click occurred: `n` for native or `s` for search.
* `{keyword}` is the keyword that triggered your ad.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!90!{ad_id}!{source_type}!!!{phrase_id}`

where:

* `{ad_id}` is the ad network's unique numeric ID for the creative.
* `{source_type}` is the type of site on which the ad has been displayed: *b* for search, *c* for context (content), or *ct* for category.
* `{phrase_id}` is the ad network's numeric ID for the keyword.
