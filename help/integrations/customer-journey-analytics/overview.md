---
title: Overview of the integration between Adobe Advertising and Adobe Customer Journey Analytics
description: Learn about options to integrate Adobe Advertising with Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
---
# Overview of the integration between Adobe Advertising with Customer Journey Analytics

<!-- title? If I change, change refs throughout -->

*Advertisers with Advertising DSP and [!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising is integrated with Adobe Customer Journey Analytics for bi-directional data sharing and reporting. You have two options for setting up the integration: 

* Advertisers with both [!DNL Analytics for Advertising] and Customer Journey Analytics have the same functionality that they have through [!DNL Analytics for Advertising], with the addition of visualizations in Customer Journey Analytics.

  You'll still track click-through events using the Adobe Experience Platform Web SDK (`alloy.js`) or the Adobe Experience Cloud Identity Service (`visitorAPI.js`). Advertisers with Advertising DSP will still use a JavaScript snippet to track view-through events. Data available in Customer Journey Analytics includes:

  * Campaign performance data from Adobe Advertising in Customer Journey Analytics

  * Site activity and conversions tracked by [!DNL Google Ads] and [!DNL Microsoft Advertising] in Customer Journey Analytics, updated daily

  * Attribution data from [!DNL Analytics] in Adobe Advertising, where it can be used for optimization and reporting

  In this use case, you should still optionally [collect historical data for AMO IDs and EF IDs for use in Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).

<!--
  In this use case, you don't need to perform any extra steps except to optionally [collect historical data for AMO IDs and EF IDs for use in Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
-->

* (Upcoming beta feature) Advertisers with Customer Journey Analytics but not [!DNL Analytics for Advertising] can natively exchange data between Adobe Advertising and Customer Journey Analytics using the [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html). You can track site events using cookies, hashed IP, and universal IDs ([!DNL LiveRamp RampIDs] and ID5 IDs) and attribute site events to paid media activity. The following data is available at the campaign, ad group, package, placement, and keyword levels:

  * Campaign performance data from Adobe Advertising in Customer Journey Analytics

    **Note:** Data from [!DNL Apple] and [!DNL Tiktok] isn't available.

  * Site activity and conversions tracked by [!DNL Google Ads] and [!DNL Microsoft Advertising] in Customer Journey Analytics

  * Attribution data from Customer Journey Analytics in Adobe Advertising, where it can be used for optimization and reporting

  In this use case, use Web SDK to track site events (using cookies, hashed IP addresses, or universal IDs) and attribute the site events to paid media activity in [!DNL Google Ads], [!DNL Microsoft Advertising], and [!DNL Meta], and Adobe DSP. You'll also use Adobe Experience Platform for data collection.

## How to initiate a native integration between Adobe Advertising and Customer Journey Analytics

Contact your Adobe Account Team, who will complete the initial configuration necessary to begin and will help you plan your implementation and data usage based on your organization's needs.

>[!MORELIKETHIS]
>
>* [Prerequisites](prerequisites.md)
>* [Adobe Advertising IDs Used by [!DNL Customer Journey Analytics]](ids.md)
>* [Adobe Advertising metrics and dimensions in Customer Journey Analytics](advertising-data-in-cja.md)
>* (Adobe Analytics users) [Collect Historical Data for AMO IDs and EF IDs for Use in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
