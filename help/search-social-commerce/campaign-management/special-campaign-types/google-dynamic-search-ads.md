---
title: Implement [!DNL Google Ads] dynamic search ads
description: Learn about the workflow for setting up [!DNL Google Ads] dynamic search ads.
exl-id: 4c806824-b582-46dc-8d88-85c73bfb0944
feature: Search Campaign Management
---
# Implement [!DNL Google Ads] dynamic search ads

*[!DNL Google Ads] search-only campaigns with creative-level or keyword- and creative-level tracking only*

Dynamic search ads use content from your website, instead of keywords, to decide when to show your ads. You can define the pages in your websites whose content is used to target your dynamic search ads by either setting up separate dynamic search targets for the ad group or choosing a campaign-level setting to target your ads using your website contents.

You can set up dynamic search ads either individually or by using bulksheets. The following instructions include links to creating individual entities. 

## Steps to set up [!DNL Google Ads] dynamic search ads

1. [Create a campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) for dynamic search ads:

   1. Initially set the campaign budget to 10% of your daily search campaign spend.
   
      You can later increase the budget after the ads prove their value.

   1. (If you want [!DNL Google Ads] to show your dynamic search ads based on the content of your website) Specify the root domain and the language for the domain in the [!UICONTROL DSA Options] section of the campaign settings.

      >[!NOTE]
      >
      >Your domain must be indexed by the [!DNL Google Ads] organic search index to be targeted. Also, if the domain contains pages in multiple languages and you want to target all of them, create a separate campaign for each language.
   
      If you don't use your website domain to target your ads, then create dynamic search targets (see Step 4) for each ad group. You can create the targets [individually](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) or using [bulk sheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

   1. Make sure that the campaign targets the search channel and only the [!DNL Google Ads] search network (not the display network). These settings are available from the [!UICONTROL Networks and Devices] tab.
   
   1. (Optional) Exclude keywords on the [!UICONTROL Negatives] tab.
   
   1. (Optional) Configure a campaign-level tracking template, which overrides the account-level tracking template but can be overridden at the lower levels.
   
      (Advertisers with Adobe Analytics without server-side tracking) When you want include tracking for the reverse feed from Search, Social, & Commerce to Analytics, add the s_kwcid tracking code to the account-level append parameters, which add the code to the final URL. See "[The s_kwcid tracking parameter](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md)."

1. [Create an ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) within the campaign, including the following steps:

   1. Set the [!UICONTROL Ad Group Type] to **[!UICONTROL Search Dynamic].**
   
   1. Set the default bid for all ads.
   
      You can override the default bid for individual dynamic search targets, if you configure them.

   1. (Optional) Configure an ad group-level tracking template, which overrides any tracking templates at higher levels but can be overridden at the ad level.
   
      If you added Adobe Analytics tracking at the campaign level and want to include it for the ad group, add it here. See Step 1e.

1. [Create each dynamic search ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) within the ad group.

   [!DNL Google Ads] dynamically generates the headline, the display URL, and the landing page URL for each ad. You can optionally add redirects and tracking to the ad-level tracking template, which overrides tracking templates at higher levels.
   If want to override any Adobe Analytics tracking at higher levels with ad-level tracking, add it here. See Steps 1e and 2c.

1. (Required when you don't include the root domain and the language for the domain in the DSA Options section of the campaign settings; optional otherwise) Create [dynamic search targets](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) for the ad group. You can optionally override the ad group-level bid with target-level bids.

   The targets define whether the ad network uses all or a subset of the pages in your website to target your dynamic search ads. To best track performance, configure your campaign with one ad group per dynamic search target, and include an ad group that targets all criteria.

1. As necessary, [edit the campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) to adjust the campaign budget and to refine traffic by excluding additional keywords from the campaign.
