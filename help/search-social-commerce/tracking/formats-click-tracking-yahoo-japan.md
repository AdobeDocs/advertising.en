---
title: Click-tracking formats for [!DNL Yahoo! Japan Ads]
description: Learn about the click-tracking formats for [!DNL Yahoo! Japan Ads] accounts.
exl-id: 79e45205-5c72-4612-9b60-36538e3c48c4
feature: Search Tracking
---
# Click-tracking formats for sponsored ads on [!DNL Yahoo! Japan Ads]

The following base tracking template formats apply to sponsored ads:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

or, when the auto-tagging option is set for the account in [!DNL Yahoo! Japan Ads]:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

Example:

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

>[!NOTE]
>
>* `<advertiser_ID>` is a variable for the advertiser's unique ID within Adobe Advertising.
>
>* This format indicates that token passing is enabled for the campaign (the default). If token passing is disabled, substitute `cq?` after `<advertiser_ID>` with `c?`.
>
>* `<the landing page>` is a variable that represents the URL on your site to which end users are directed.

>[!MORELIKETHIS]
>
>* [About click-tracking URL formats for the Adobe Advertising conversion tracking service](formats-click-tracking-about.md)
>* [AMO ID formats](/help/integrations/analytics/ids.md#amo-id-formats)
