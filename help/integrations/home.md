---
title: What's New
description: Learn about updates to integrations between Adobe Advertising and other products and services in Adobe Experience Cloud.
cloud: Experience Cloud
product: advertising cloud
index: yes
exl-id: e5874077-d2a8-43bb-ad4e-55547442c8a4
---
# What's New

The following features are new or recently changed.

| Date | Feature | Description | For More Information |
| ---- | ------- | ----------- | -------------------- |
| 26 March 2026 | [!DNL Adobe Analytics for Advertising] | (Advertisers with Search, Social, & Commerce; [!DNL Microsoft Advertising] accounts; and [!DNL Adobe Analytics for Advertising]) For accounts with the [!UICONTROL Auto Upload] tracking option, the format of the AMO ID parameter in the landing page suffixes for all campaign types was updated to the latest format. Previously, performance max campaigns for most accounts were migrated to the new format.<br><br>For accounts without the [!UICONTROL Auto Upload] tracking option that weren’t already migrated to the new format, however, you must manually update each landing page suffix to include the new AMO ID format.<br><br>Current format: `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}` | See "[Overview of [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)" and the [AMO ID formats](/help/integrations/analytics/ids.md#amo-id-formats)." |
| Released 29 October 2024 | [!DNL Adobe Analytics for Advertising] | (Advertisers with [!DNL Adobe Analytics for Advertising] and [!DNL Microsoft Advertising] performance max campaigns) Asset group-level data for your performance max campaigns is now available in Adobe Analytics when you implement a new AMO ID ([!DNL s_kwcid]) parameter in the tracking URLs for your performance max campaigns, which don’t include ads and keywords. Tracking for most accounts with performance max campaigns was already migrated to the new format. For accounts with performance max campaigns without the [!UICONTROL Auto Upload] tracking option that weren’t already migrated to the new format, however, you must manually update each landing page suffix to include the new AMO ID format.<br><br>Adobe Analytics data for your performance max campaigns is also available in Search, Social, & Commerce. | See the new [AMO ID format](/help/integrations/analytics/ids.md#amo-id-formats) and [when and how to add the parameter to your tracking URLs](/help/integrations/analytics/ids.md#amo-id-implement). |
| 13 November 2024 | [!DNL Analytics for Advertising] | (Advertisers with [!DNL Analytics for Advertising] and Adobe Customer Journey Analytics) If you use reserved variables to capture your AMO IDs and EF IDs, then you can prepare for a future integration between Adobe Advertising and Adobe Customer Journey Analytics by copying your reserved variables for the AMO ID and the EF ID into standard [!DNL eVars] as soon as possible. This will allow the collection of historical data for the AMO IDs and EF IDs as soon as you complete the task, and the historical data will be available for future use. Your Adobe Account Team will let you know if you use reserved variables and need to complete this task. | See “[Collect Historical Data for AMO IDs and EF IDs for Use in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).” |
| 16 December 2023 | Help | A new document explains how to set up A/B tests in [!DNL Target] for click-through traffic from ads in Search, Social, & Commerce, as well as tips on how to measure and visualize your tests in [!DNL Analytics]. | See "[Configure A/B Tests in Adobe Target for Search, Social, & Commerce Ads](/help/integrations/target/ab-tests-search.md)." |
| 8 August 2023 | [!DNL Analytics for Advertising] | Some [!DNL Analytics] success event metrics, including standard, custom, and reserved conversion metrics and traffic metrics, are automatically available in DSP and in Search, Social, & Commerce. Now, you now can also configure your own success metrics based on your existing [!DNL Analytics] [!DNL eVars] and [!DNL props] by funneling [!DNL eVar]- and [!DNL prop]-level data into a custom success event. | See "[Create Conversion Metrics from Adobe Analytics [!DNL eVars] and [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)." |
| 13 July 2023 | Reporting | (DSP users with [!DNL Analytics for Advertising]) View-through conversions for connected TV (CTV) placements are now included in conversion data available within Adobe Analytics. | See the section on "Examples of How to Use the Integration" in "[Overview of [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md#integration-examples)." |
| 1 November 2022 | Help | A new document explains how to implement click-through and view-through signal sharing between Advertising DSP and Adobe Target, set up an A/B test activity in [!DNL Target] for your DSP ads, and how to set up Adobe Analytics Analysis Workspace to view the test data. | See "[Configure A/B Tests in Adobe Target for Advertising DSP Ads](/help/integrations/target/ab-tests-dsp.md)." |
| 17 August 2022 | Help  | A new chapter explains all ways in which Adobe Advertising is integrated with Adobe Audience Manager. | See the chapter on "Integration with Adobe Audience Manager," including an overview of "[Adobe Advertising Integrations with Adobe Audience Manager](/help/integrations/audience-manager/overview.md)." |
| 27 April 2021 | [!DNL Analytics for Advertising] | Learn why and how to add [!DNL Analytics for Advertising] macros to your [!DNL Google Campaign Manager 360] ad tags to send click data to Adobe Analytics. | See "[Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md)." |
| 19 April 2021 | [!DNL Analytics for Advertising] | Learn why and how to append macros to your [!DNL Flashtalking] ad tags to send click data to Adobe Analytics. | See "[Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md)." |
| 27 October 2021 | [!DNL Analytics for Advertising] | If your organization wants to switch from using the legacy Adobe Analytics `visitorAPI.js` library to the [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) library (`alloy.js`) for data collection, you must make some changes to enable ID stitching. | See "[Using the [!DNL Last Event Service] JavaScript Library with Adobe Experience Platform [!DNL Web SDK]](/help/integrations/analytics/web-sdk.md)." |
| 26 May 2021 | Help | The chapter "[!DNL Analytics for Advertising]" now includes a subchapter on "Working in [!DNL Analytics Marketing Channels]." | See: "[Fundamentals of Marketing Channels](/help/integrations/analytics/marketing-channels/mc-overview.md)," "[Using Adobe Advertising IDs to Create [!DNL Analytics Marketing Channels] Processing Rules](/help/integrations/analytics/marketing-channels/mc-ids.md)," "[Using [!DNL Analytics Marketing Channels] with Adobe Advertising Data](/help/integrations/analytics/marketing-channels/mc-ac-data.md)," and "[Why Channel Data Can Vary Between Adobe Advertising and [!DNL Analytics Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)." |
| 26 May 2021 | Help | A link to all video tutorials about [!DNL Analytics for Advertising] was added. | See: "[Video tutorials about Adobe Advertising integrations](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/overview.html)." |

{style="table-layout:auto"}

<!-- At some point, just make this an overview page instead?

Adobe Advertising is integrated with the following Adobe Experience Cloud products:

* [Adobe Analytics](/help/integrations/analytics/overview.md)

* Adobe Audience Manager

* Adobe Campaign (Adobe Advertising Search only)

 -->
