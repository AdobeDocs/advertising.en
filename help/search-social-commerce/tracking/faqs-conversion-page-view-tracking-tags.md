---
title: FAQs about Adobe Advertising conversion and page view tracking tags
description: See a comparison of the Adobe Advertising conversion and page view tracking tags.
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
---
# FAQs about Adobe Advertising conversion and page view tracking tags

The following apply to Adobe Advertising conversion tracking tags and page view tracking tags.

| | JS Tags with ECID | JS Version 3 Tags | JS Version 2 Tags | Image Tags |
| ---- | ---- | ---- | ---- | ---- |
| Can be used on the same webpage as another JS version | &mdash; | &mdash; | &mdash; | n/a |
| Allows the use of multiple tags with the same advertiser user IDs on the same webpage | Yes | Yes | Yes | &mdash; |
| Allows the use of multiple tags with different advertiser user IDs on the same webpage | Yes | Yes | &mdash; | &mdash; |
| Used by the Adobe Advertising extension for Adobe Experience Platform, and compatible with other tags generated using Experience Platform | Yes | Yes | &mdash; | &mdash; |
| Allows all conversions that originate from [!DNL Apple Safari] and [!DNL Mozilla Firefox] to be tracked when used with the Adobe Advertising JavaScript conversion mapping tag | Yes | Yes | Yes | &mdash; |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* All new implementations use JavaScript Version 3.
>* The JavaScript tag with ECID uses the [Adobe Experience Cloud ID (ECID) Service](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) as well as the legacy ef_id and gsurferid to measure conversions. This latest tag creates [first-party Experience Cloud s_ecid cookies](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) and provides tighter integration with other Experience Cloud products.
>* Use JavaScript Version 2 tags only when they're already implemented tags on the advertiser's webpages.
>* The best practice is to use JavaScript tags instead of image tags unless the site has a policy against using them.
>* JavaScript tags are required for advertisers who want to target audiences created in Adobe Experience Cloud, created in Adobe Audience Manager, or published to Adobe Experience Cloud from Audience Manager or Adobe Analytics.

>[!MORELIKETHIS]
>
>* [About Adobe Advertising conversion-tracking tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generate an Adobe Advertising conversion tag](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format of JavaScript conversion tracking tags version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format of JavaScript conversion tracking tags version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format of image conversion tracking tags](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
