---
title: Click-tracking formats for [!DNL Baidu]
description: Learn about the click-tracking formats for [!DNL Baidu] accounts.
exl-id: 4f4ed518-aa25-4a29-b263-c01f78b69b92
feature: Search Tracking
---
# Click-tracking formats for sponsored ads on [!DNL Baidu]

The following base destination UR format applies to sponsored ads:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

Example:

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` is a variable for the advertiser's unique ID within Adobe Advertising.
>
>* This format indicates that token passing is enabled for the campaign (the default). If token passing is disabled, substitute `cq?` after `<advertiser_ID>` with `c?`.
>
>* `<campaignID>` is a variable for the numeric campaign ID.
>
>* `<the landing page>` is a variable that represents the URL on your site to which end users are directed.

>[!MORELIKETHIS]
>
>* [About click-tracking URL formats for the Adobe Advertising conversion tracking service](formats-click-tracking-about.md)
>* [AMO ID Formats](/help/integrations/analytics/ids.md#amo-id-formats)
