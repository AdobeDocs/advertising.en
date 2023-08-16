---
title: Click-tracking formats for [!DNL Google Ads]
description: Learn about the click-tracking formats for [!DNL Google Ads] accounts.
exl-id: 68f6da43-3430-4c0a-9369-937fa52c071a
feature: Search Tracking
---
# Click-tracking formats for [!DNL Google Ads]

Following are the base tracking template and landing page suffix (final URL suffix) formats that Search, Social, & Commerce requires for [!DNL Google Ads].

## Tracking template formats

### Search/display network, including sitelinks

The following format applies to all trackable ad types on search and display networks, and for sitelinks.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Example:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` is a variable for the advertiser's unique ID within Adobe Advertising.
>
>* This format indicates that token passing is enabled for the campaign (the default). If token passing is disabled, substitute `cq?` after `<advertiser_ID>` with `c?`.
>
>* The [!DNL ValueTrack] parameters to indicate final URLs in tracking templates must be either `{lpurl}` or `!{unescapedurl}`.
>
>* (Text ads) When you bid by keyword, the parameter `ev_pl` (for placements) has no value. When you bid by placement, `ev_ln` (for keywords) has no value. When you bid by ad group or by any other dimension, both `ev_ln` and `ev_pl` have no values.
>
>* (Dynamic search ads) `{keyword}` indicates the dynamic search target expression, such as `_cat:[VALUE]` or `_url:[VALUE]`.
>
>* (Dynamic search ads) [!DNL Google Ads] determines the final URL dynamically, so you don't need to enter one.
>
>* (Sitelinks) You can see which conversions resulted from a click on a sitelink by generating a [!UICONTROL Transaction Report]. The [!UICONTROL Link Type] column value for a sitelink is `sl:<Sitelink text>`, such as `sl:See Current Offers`.

### Shopping network

The following format applies to shopping ads and product groups in shopping networks. You can specify a tracking template at the account, campaign, ad group, or product group level.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Example:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` is a variable for the advertiser's unique ID within Adobe Advertising.
>
>* This format indicates that token passing is enabled for the campaign (the default). If token passing is disabled, substitute `cq?` after `<advertiser_ID>` with `c?`.
>
>* The [!DNL ValueTrack] parameters to indicate final URLs in tracking templates must be either `{lpurl}` or `!{unescapedurl}`.
>
>* [!DNL Google Ads] uses product URLs in the Google Merchant Center feed as the final URLs, so you don't need to enter final URLs for your product data or product groups.
>
>* You can see which conversions resulted from a click on a shopping ad by generating a [!UICONTROL Transaction Report]. The [!UICONTROL Link Type] column value for a product ad is pla:`<product ID>`, such as `pla:8525822`.

## Landing page suffix (final URL suffix) formats

Accounts that use Adobe Advertising conversion tracking must include the ad network's click identifier (`gclid` for [!DNL Google Ads]) in the suffix:

* When the advertiser has an Adobe Analytics integration, the suffix must include one of the following:
  
  * [!DNL Google Ads] accounts that use the latest AMO ID format (beginning with `s_kwcid`), which supports campaign- and ad group-level reporting for performance max campaigns and drafts and experiments campaigns:

    `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

    If the account has a server-side AMO ID implementation and the account or campaign setting "[!UICONTROL Auto Upload]" is enabled, then the parameter is added automatically. Otherwise, you need to manually add it.

  * All other [!DNL Google Ads] accounts:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* When the advertiser doesn't have an Adobe Analytics integration, the suffix must include the following:

  `&ev_efid={gclid}:G:s`
  
>[!NOTE]
>
>* Landing page suffixes at lower levels override the account-level suffix. For easier maintenance, use only the account-level suffix unless different tracking for individual account components is necessary. To configure a suffix at the ad group level or lower, use the ad network's editor.
>
>* (Dynamic search ads; advertisers with Adobe Analytics and without server-side tracking) When you want include tracking for the reverse feed from Adobe Advertising to Analytics, then append the AMO ID tracking code to the end of the account-level landing page suffix.

>[!MORELIKETHIS]
>
>* [About click-tracking URL formats for the Adobe Advertising conversion tracking service](formats-click-tracking-about.md)
>* [AMO ID formats](/help/integrations/analytics/ids.md#amo-id-formats)
