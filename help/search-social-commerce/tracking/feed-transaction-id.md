---
title: Conversion tracking using a transaction ID feed
description: Learn about using a transaction ID feed for conversion tracking data.
exl-id: 58f231a6-970b-46b4-824b-67b3d3f83051
feature: Search Tracking
---
# Conversion tracking using a transaction ID feed

When an advertiser has both online and offline transactions, Adobe Advertising can track the online transactions via the Adobe Advertising conversion-tracking pixel, and the advertiser can track the offline transactions using a transaction ID and deliver them via a feed:

* For the online transactions, Adobe Advertising tracks the clicks on your ads and the resulting transactions on your website.

* The advertiser must track offline conversions and send transaction-level feed files to Adobe Advertising.

## Implementation overview

*Agency account manager, [!DNL Adobe] account manager, and administrator user roles only*

1. Use the account or campaign tracking options "[!UICONTROL EF Redirect]" and "[!UICONTROL Auto Upload]" to automatically generate a destination URL or final URL for each keyword (for keyword-level tracking) or ad (for ad-level tracking) in the account or campaign.

1. Set up Adobe Advertising conversion tracking for the online conversions. This process is same as for advertisers with Adobe Advertising pixel-based conversion tracking. It's important to generate conversion tags that include a parameter for a unique transaction ID (`ev_transid=<transid>`).

1. For the offline portion of each transaction, the advertiser generates the same transaction ID that was used in the online portion of the transaction to include in the feed file.

1. The advertiser uploads a file with the [required conversion data](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) to the designated server location.

1. Technical Services parses the conversion data in the uploaded files, and then uploads the data into Adobe Advertising. Adobe Advertising then tracks the data against individual keywords, ads, and placements and creates revenue forecasting for each.

1. Technical Services validates the processed data against the feed data and checks for any [orphan transactions](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [File requirements for conversion feed files](feed-file-requirements.md)
>* [Data requirements for data feeds using a transaction ID](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
