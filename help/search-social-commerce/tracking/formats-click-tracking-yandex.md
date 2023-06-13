---
title: Click-tracking formats for [!DNL Yandex]
description: Learn about the click-tracking formats for [!DNL Yandex] accounts.
exl-id: cf1d6c4b-9bcd-4b82-919f-c14dbaff9a76
---
# Click-tracking formats for sponsored ads on [!DNL Yandex]

The following base destination UR format applies to sponsored ads:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

Example:

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` is a variable for the advertiser's unique ID within Adobe Advertising.
>
>* This format indicates that token passing is enabled for the campaign (the default). If token passing is disabled, substitute `cq?` after `<advertiser_ID>` with `c?`.
>
>* `<the landing page>` is a variable that represents the URL on your site to which end users are directed.
>
>* `source_type`  is the match type.
>
>* `source` is whether the ad was shown on a search or content-based site.
>
>* `position` is the position number for the ad in the block. For non-search traffic, the value is "0."
>
>* `position_type` is the block in which the ad was shown on [!DNL Yandex]. Possible values: "premium" (top block), "other" (right block), or "none" (non-search traffic).

>[!MORELIKETHIS]
>
>* [About click-tracking URL formats for the Adobe Advertising conversion tracking service](formats-click-tracking-about.md)
>* [Formats for the s\_kwcid tracking code](skwcid-tracking-parameter.md)
