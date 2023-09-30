---
title: Conversion tracking using an EF ID feed
description: Learn about using an EF ID feed for conversion tracking data.
exl-id: fd065313-3d27-4bb9-a934-e815e02cf405
feature: Search Tracking
---
# Conversion tracking using an EF ID feed

In this method, Advertising Cloud collects an `ef_id` value each time a user clicks and ad and arrives at the landing page, and the advertiser stores the `ef_id` value with the conversion data and sends it in a data feed.

## Implementation overview

*Agency account manager, [!DNL Adobe] account manager, and administrator user roles only*

1. Use the account or campaign tracking options "[!UICONTROL EF Redirect]," the redirect type of "[!UICONTROL Token]," and "[!UICONTROL Auto Upload]" to automatically generate a destination URL or final URL with an Adobe Advertising token (ef_id) for each keyword (for keyword-level tracking) or ad (for ad-level tracking) in the account or campaign.

   >[!NOTE]
   >* This method doesn't require the advertiser to use Adobe Advertising conversion-tracking tags.
   >* If you switch the redirect type for an existing account or campaign from [!UICONTROL Standard] to [!UICONTROL Token], or vice versa, then you must regenerate all applicable tracking URLs.
   
   The ef_id is populated and appended to the landing page URL when the end user clicks the ad and is redirected to an Adobe Advertising server. The ef_id is then passed to the advertiser in the destination URL or final URL for the ad or keyword. The following is an example of a destination URL that's passed to the advertiser during the redirect:
   
   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. The advertiser extracts the ef_id from the redirect and stores it with the relevant conversion data to include in the feed file. Don't alter the ef_id or change its case.

1. (Optional but recommended) The advertiser may create a unique transaction ID for each transaction to include in the feed file.

1. The advertiser uploads a file with the [required conversion data](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) to the designated server location.

1. Technical Services parses the conversion data in the uploaded files, and then uploads the data into Adobe Advertising. Adobe Advertising then tracks the data against individual keywords, ads, and placements and creates revenue forecasting for each.

1. Technical Services validates the processed data against the feed data and checks for any [orphan transactions](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [File requirements for conversion feed files](feed-file-requirements.md)
>* [Data requirements for data feeds using EF IDs](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
