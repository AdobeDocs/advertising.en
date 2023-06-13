---
title: Implement [!DNL Google Ads] performance max campaigns
description: Learn about the workflow for setting up [!DNL Google Ads] performance max campaigns.
exl-id: afad96b2-d4a6-41ee-ad84-38aa1306d73e
---
# Implement [!DNL Google Ads] performance max campaigns

In [!DNL Google Ads] performance max campaigns, you don't set up ad groups, ads, or keywords. Instead, within the campaign settings, you specify one or more asset groups, which include headlines, descriptions, and uploaded images, logos, and [!DNL YouTube videos]. [!DNL Google Ads] automatically combines the assets to serve ads based on the channel (such as [!DNL YouTube], [!DNL Gmail], or [!DNL Search]).

You can view your existing performance max campaigns, with performance data in table and trend chart format, in the [!DNL Campaigns] view; data isn't available at lower levels. Campaign-level performance data is also available in reports and in Adobe Analytics (for advertisers with an [Analytics integration](/help/integrations/analytics/overview.md). To view performance data for performance max campaigns in [!DNL Analytics], the campaign must use the [upgraded s_kwcid tracking code](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md) (which tracks the campaign ID and ad group ID).

>[!NOTE]
>
>* You must manually upload all image files. Links to [!DNL Google Merchant Center] product feeds aren’t supported.
>* Only required settings are available. For optional settings, log in to the [!DNL Google Ads] editor.
>* Support for listing groups isn't available. To manage and view data for listing groups, log in to the [!DNL Google Ads] editor.

## Steps to set up [!DNL Google Ads] performance max campaigns

You can set up performance max campaigns individually from the [!UICONTROL Campaigns] > [!UICONTROL Campaigns] view.

1. [Create a campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) with campaign type **[!UICONTROL Performance Max]**.

   Specify the [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting], and [!UICONTROL URL Options]. Optionally enter [!UICONTROL Negative Keywords], enter [!UICONTROL Negative Websites], and/or override the [!UICONTROL Campaign Tracking] options.

1. Create asset groups and upload assets for the campaign:

   1. At the bottom of the campaign settings, click **[!UICONTROL Manage Asset Groups]**.
   
   1. Specify the settings for the first asset group, and upload the images, logos, and optional videos for the asset group.
   
      See [descriptions of the asset group settings](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) to understand the requirements and specifications.

   1. Add additional asset groups as needed.

1. Click **[!UICONTROL Post]**.

1. (Optional) Add the campaign to a hybrid portfolio for optimization.
