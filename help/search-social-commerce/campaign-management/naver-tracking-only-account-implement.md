---
title: Implement [!DNL Naver] tracking-only accounts
description: Learn how to set up tracking campaigns for your [!DNL Naver] accounts so that you can track, report on, and visualize performance for the ads you buy directly from the ad network. 
---
# Implement [!DNL Naver] tracking-only accounts

*[!DNL Naver] accounts only*

You can create tracking campaigns for your [!DNL Naver] accounts so that you can track, report on, and visualize performance for the ads you buy directly from the ad network. Search, Social, & Commerce doesn't synchronize data with the ad network, automatically upload tracking, nor place bids for the account.

Tracking campaigns replicate your existing campaigns, ad groups, and keywords. Once you've created the account structure in Search, Social, & Commerce and added tracking to the original campaigns within the ad network, you can upload daily network traffic metrics for your keywords or ads. Search, Social, & Commerce can then attribute your conversions to your ads and keywords.

You can track performance metrics across all of your campaigns and for any individual campaign, ad group, or keyword/ad. You also can include information about them in most basic, advanced, and assist reports, along with data for your other ad networks. Support for exporting the metrics to Adobe Analytics isn't available, but Search, Social, & Commerce can sync [metrics you're tracking in [!DNL Analytics]](/help/integrations/analytics/data/analytics-data-in-advertising.md) into Search, Social, & Commerce.

>[!NOTE]
>
>You can't add tracking campaigns to a portfolio for optimization.

1. Create tracking campaigns in Search, Social, & Commerce:

   1. Create [dummy network account details](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). If you have multiple accounts within a single ad network, then consolidate them into one account in the [!UICONTROL Accounts] view.
   
      [!DNL Naver] doesn't provide API support to upload tracking parameters to the ad network. However, you can generate tracking parameters using bulksheets and manually add them within the ad network (per Step 2). To generate the tracking parameters, you must use the "[!UICONTROL EF Redirect]" tracking method. You can optionally add any append parameters you want.
      
      Search, Social, & Commerce automatically includes the parameter `ev_cl={ef_uniqueid}` in any tracking URLs it generates within bulksheets for the account. This unique ID is used to match the campaign data with any cost and click data you upload.

   1. Set up campaigns to track:

      1. Within the ad network, create a bulksheet file containing all entities, and their required parent entities, that you want Search, Social, & Commerce to track for the account.
   
         You can include data about keywords, including the parent campaigns and ad groups.
      
      1. Edit the bulksheet file, if necessary, so that it follows the Search, Social, & Commerce [bulksheet format required for [!DNL Naver] accounts](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).
       
      1. In Search, Social, & Commerce, [upload the bulksheet file](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).
      
         >[!NOTE]
         >
         >Note: Search, Social, & Commerce doesn't post the data to the ad network account.

1. Set up tracking for the campaigns:

   1. In Search, Social, & Commerce, [download a new bulksheet file](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) using the option to "[!UICONTROL Generate Tracking URLs]."
   
     Using the "[!UICONTROL Generate Tracking URLs]" option populates the [!UICONTROL Destination URL] field for each keyword with the Search, Social, & Commerce tracking code prefixed to the [!UICONTROL Base URL] value.
   
      The following is an example of the destination URL with tracking:
      
      ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. Copy the [!UICONTROL Destination URL] values in the downloaded bulksheet file to the relevant keyword settings on the network.
   
      You may be able to add the URLs to the relevant entities by uploading the file to the network within the ad network's editor. In that case, you may need to remove some columns, according to the network's data requirements. Otherwise, you must enter the URLs manually on the network.

1. Periodically download click and cost data aggregated daily from the ad network for the keywords or ad group-level brand ads that you're tracking, and then [upload the click and cost data](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) to Search, Social, & Commerce in the [required format](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   Include the full account hierarchy and any metrics that you want to include. Search, Social, & Commerce matches the uploaded data with data in existing campaigns.

1. (Optional) If you use Adobe Advertising conversion tracking service tags in your webpages to track conversions that aren't tracked on the ad network, then send feed files containing daily-aggregated conversion data to add to your tracking campaigns.

   For more information, contact your Adobe Account Team.

All uploaded tracking data is available from [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] within the [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups], and [!UICONTROL Keywords] views. It's also available for reports in the [!UICONTROL Insights & Reports] view.

>[!MORELIKETHIS]
>
>* [Appendix - Required bulksheet data for [!DNL Naver] accounts](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [Upload traffic and conversion metrics for [!DNL Naver] tracking-only accounts](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [Metric data requirements for [!DNL Naver] tracking-only accounts](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [Click-tracking formats for [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
