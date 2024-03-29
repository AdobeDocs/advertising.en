---
title: Click-tracking formats for [!DNL Naver]
description: Learn about the click-tracking formats for [!DNL Naver] accounts.
exl-id: b438652e-6e98-4223-8169-2bfb37500670
feature: Search Tracking
---
# Click-tracking formats for sponsored ads on [!DNL Naver]

The following base destination UR format applies to sponsored ads:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=87&ev_cl={ef_uniqueid}&url=<the landing page>`

Example:

`http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` is a variable for the advertiser's unique ID within Adobe Advertising.
>
>* This format indicates that token passing is enabled for the campaign (the default). If token passing is disabled, substitute `cq?` after `<advertiser_ID>` with `c?`.
>
* `<the landing page>` is a variable that represents the URL on your site to which end users are directed.

>[!MORELIKETHIS]
>
>* [About click-tracking URL formats for the Adobe Advertising conversion tracking service](formats-click-tracking-about.md)
>* [AMO ID formats](/help/integrations/analytics/ids.md#amo-id-formats)
