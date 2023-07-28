---
title: About Adobe Advertising conversion-tracking tags
description: Learn about using the Adobe Advertising conversion-tracking tags.
exl-id: 07403d60-6db2-47e7-977b-4b59c8797c3d
feature: Search Tracking
---
# About Adobe Advertising conversion-tracking tags

Adobe Advertising tracks conversions resulting from clicks on ads using Adobe Advertising conversion tracking tags that are inserted in the webpages that open when a conversion event occurs, such as a "success" page. The tags include embedded information to send the transaction data, along with the user's Adobe Advertising cookie, to a tracking server, from which the transaction is credited to the appropriate ad click or impression (per the advertiser's conversion attribution settings).

>[!NOTE]
>
>If the user doesn't have a valid cookie, then Adobe Advertising doesn't report the conversion.

For each set of conversion metrics you want to track, you must create a separate conversion tag. Provide the tags to the advertiser or agency with a list of webpages on which to insert each. You can generate either of the following types of conversion tags. See "[Generate an Adobe Advertising conversion tag](/help/search-social-commerce/tools/conversion-tag-generate.md)" for instructions.

* (Recommended) JavaScript tags (Version 3 or Version 2), which aren't visible in the webpages.

* HTML image tags to display 1-pixel x 1-pixel transparent images (pixels), which are invisible to end users, on the webpages. Use image tags only when the company has a policy against using JavaScript tags.

For more information about the differences between the tag types, see "[FAQs about Advertising Cloud conversion tracking tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)."

>[!NOTE]
>
>* This feature doesn't add image tags or JavaScript tags to the advertiser's webpages. The tags must be added according to the advertiser's normal procedure for updating webpages.
>* Make sure to consider how long it will take to implement the tags. Depending on the company's policies, implementation may take weeks or even months.

## Features of the Adobe Advertising conversion-tracking tags

The conversion tracking pixel allows Adobe Advertising to do the following:

* Track and report conversion data at the keyword level for search campaigns.

* Track and report conversion data at the ad (creative) level across all marketing channels (paid search and display), which can facilitate creative testing.

* Track and report conversion data at the transaction level across all of your marketing channels.

* Show how your conversions are distributed across your different marketing channels so you can see which is most effective.

* Report and optimize on different attribution levels (such as attributing conversions to the last related event or weighting all events evenly).

* Provide visibility on click assists (search keywords or placements that contributed to a conversion funnel) and channel assists (user events that contributed to a conversion funnel, possibly across multiple marketing channels).

* Provide visibility into the geographical distribution and referring domains of your site traffic and conversions so you can refine your geographical and website targeting.

* Analyze day-of-the-week or intra-day trends, which can be used to improve conversion rates.

>[!MORELIKETHIS]
>
>* [Conversion tracking options](conversion-tracking-about.md)
>* [Generate an Adobe Advertising conversion tag](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format of JavaScript conversion tracking tags version 3](format-conversion-tag-jsv3.md)
>* [Format of JavaScript conversion tracking tags version 2](format-conversion-tag-jsv2.md)
>* [Format of image conversion tracking tags](format-conversion-tag-image.md)
>* [FAQs about conversion and page view tracking tags](faqs-conversion-page-view-tracking-tags.md)
>* [The Adobe Advertising JavaScript conversion mapping tag](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
