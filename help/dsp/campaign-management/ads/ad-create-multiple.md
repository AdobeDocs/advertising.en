---
title: Create Multiple Third-Party Ads
description: Learn how to create multiple third-party ads at one time.
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
---
# Create Multiple Third-Party Ads

You can create up to 500 third-party ads at a time by uploading tags that point to creative assets hosted on third-party ad servers. You can include tracking pixels for the ads.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

You can upload either [!DNL DoubleClick] and [!DNL Flashtalking] tag sheets or a manually-populated file using the provided template.

>[!TIP]
>
> The best practice is to use third-party ads that are served securely using HTTPS. URLs served using HTTPS begin with "https."

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign in which the ad will be included.

1. Above the data table, click **[!UICONTROL Create]**. In the Ad Types section of the menu, click **[!UICONTROL Bulk upload ads]**.

1. Select the ad server on which the ad is hosted: *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]*, or *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] and [!DNL Flashtalking] ads) Select the tag type to use for each video asset and each display asset. The available options vary by ad server.

1. (Ads on all ad servers except [!DNL DoubleClick] and [!DNL Flashtalking]) Click **[!UICONTROL Download this template]** to download a template in [!DNL Microsoft Excel] spreadsheet (XLSX) format, which you can populate with ad data and save locally. The required columns include [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag], and [!UICONTROL Ad Types].

1. Click **[!UICONTROL Upload]** and select a file in .xlsx or .xls formats from your device or network.

   For [!DNL DoubleClick] and [!DNL Flashtalking] ads, upload unedited tag sheets from the ad server. For other ad servers, use the template you downloaded in Step 3.

1. After the upload is complete, click **[!UICONTROL Start Building Ads]**.

1. Review the details and status of each ad:

   1. Review the status of each ad, which is based on validation checks on the uploaded tag.

   1. (Optional) Do any of the following for each ad:

      * To preview an ad, click ![play](/help/dsp/assets/play.png) in the ad row.

      * To edit the ad details, click ![edit](/help/dsp/assets/edit.png), edit the details, and then click **Save**.

      * To remove an ad, click **[!UICONTROL X]** in the ad row.

1. Click **[!UICONTROL Create *N* Ad(s)]**.

1. Do one of the following:

   * Click **[!UICONTROL Done]**.

   * (If an ad is rejected; optional) To edit the ad record and resubmit the ad for review:

      1. Click the ad name.

      1. Edit the ad settings.
      
      1. Click **[!UICONTROL Save & submit for review]**.

>[!MORELIKETHIS]
>
>* [About Ad Management](ad-about.md)
>* [Ad Specifications](ad-specs.md)
>* [Create a Single Ad](ad-create.md)
>* [Video: How to Bulk Upload Third-Party Ad Tags](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)
