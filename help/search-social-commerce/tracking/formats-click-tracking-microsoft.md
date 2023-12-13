---
title: Click-tracking formats for [!DNL Microsoft Advertising]
description: Learn about the click-tracking formats for [!DNL Microsoft Advertising] accounts.
exl-id: 4970ac33-4978-4768-8701-6fdd3252bbd1
feature: Search Tracking
---
# Click-tracking formats for [!DNL Microsoft Advertising]

Following are the base tracking template and landing page suffix (final URL suffix) formats that Search, Social, & Commerce requires for [!DNL Microsoft Advertising].

## Tracking template formats

### Search and audience networks (except for sitelinks)

The following format applies for all trackable ad types on search and audience networks.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Example:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` is a variable for the advertiser's unique ID within Adobe Advertising.
>
>* This format indicates that token passing is enabled for the campaign (the default). If token passing is disabled, substitute `cq?` after `<advertiser_ID>` with `c?`.
>
>* `{TargetId}` represents the ID of a) either the keyword or b) the keyword and remarketing list (audience) that triggered the ad (for example, "kwd-123:aud-456" for both a keyword and a remarketing list or "kwd-123" for keyword only).

### Sitelinks

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Example:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` is a variable for the advertiser's unique ID within Adobe Advertising.
>
>* This format indicates that token passing is enabled for the campaign (the default). If token passing is disabled, substitute `cq?` after `<advertiser_ID>` with `c?`.
>
>* `{TargetId}` represents the ID of a) either the keyword or b) the keyword and remarketing list (audience) that triggered the ad (for example, "kwd-123:aud-456" for both a keyword and a remarketing list or "kwd-123" for keyword only).
>
>* `{adextensionid}` is unused.
>
>* (Sitelinks) You can see which conversions resulted from a click on a sitelink by generating a [!UICONTROL Transaction Report]. The [!UICONTROL Link Type] column value for a sitelink is `sl:<Sitelink text>`, such as `sl:See Current Offers`.

### Shopping network

The following formats apply for shopping ads in shopping networks. You can specify a tracking template at the account, campaign, ad group, or product group level.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

Example:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` is a variable for the advertiser's unique ID within Adobe Advertising.
>
>* This format indicates that token passing is enabled for the campaign (the default). If token passing is disabled, substitute `cq?` after `<advertiser_ID>` with `c?`.
>
>*  `{TargetId}` represents the ID of a) either the keyword or b) the keyword and remarketing list (audience) that triggered the ad (for example, "kwd-123:aud-456" for both a keyword and a remarketing list or "kwd-123" for keyword only).
>
>* (Optional) Instead of entering tracking templates at the account, campaign, ad group, or product group level, you can add the tracking URL to the product data within the [!DNL Microsoft Merchant Center] account. To do so, include the tracking URL, together with the value in the "`link`" or "`mobile_link`" field, as appropriate, in a custom column "[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)" within the product feed. The value in the "`bingads_redirect`" field will replace the values in the "`link`" and "`mobile_link`" fields. URLs generated using this method don't include any tracking parameters specified in the Search, Social, & Commerce account or campaign settings.

## Landing page suffix (final URL suffix) formats

>[!NOTE]
>
>Landing page suffixes at lower levels override the account-level suffix. For easier maintenance, use only the account-level suffix unless different tracking for individual account components is necessary. To configure a suffix at the ad group level or lower, use the ad network's editor.

### Search and audience networks

Accounts that use Adobe Advertising conversion tracking must include the ad network's click identifier (`msclkid` for [!DNL Microsoft Advertising]) in the suffix:

* When the advertiser has an Adobe Analytics integration, the suffix must include the following:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* When the advertiser doesn't have an Adobe Analytics integration, the suffix must include the following:

  `&ev_efid={msclkid}:G:s`

### Shopping network

Accounts that use Adobe Advertising conversion tracking must include the ad network's click identifier (`msclkid` for [!DNL Microsoft Advertising]) in the suffix:

* When the advertiser has an Adobe Analytics integration, the suffix must include the following:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* When the advertiser doesn't have an Adobe Analytics integration, the suffix must include the following:

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [About click-tracking URL formats for the Adobe Advertising conversion tracking service](formats-click-tracking-about.md)
>* [AMO ID formats](/help/integrations/analytics/ids.md#amo-id-formats)
