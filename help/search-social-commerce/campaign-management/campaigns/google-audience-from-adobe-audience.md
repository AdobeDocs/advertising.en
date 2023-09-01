---
title: Create [!DNL Google Ads] customer match audiences from [!DNL Adobe] audiences
description: Learn how to create [!DNL Google Ads] customer match audiences from your existing Adobe Analytics and Audience Manager audiences.
exl-id: 17cf0729-bc13-4ec3-918e-039ecdc91a41
feature: Search Campaign Management
---
# Create [!DNL Google Ads] customer match audiences from Adobe Analytics and Audience Manager audiences

*[!DNL Google Ads] accounts that are eligible for customer match only*

*Advertisers with an Adobe Advertising-Adobe Audience Manager or Adobe Advertising-Adobe Analytics integration only*

Opted-in advertisers can create [!DNL Google Ads] customer match audiences using user IDs from a) [!DNL Analytics] segments that are shared with Adobe Experience Cloud and b) Audience Manager segments that have Search, Social, & Commerce as a destination, including [!DNL Analytics] segments that are published to Adobe Experience Cloud and segments that are created using the Adobe Experience Cloud Audience Library. Search, Social, & Commerce automatically pushes a [!DNL Google] tracking URL back to each [!DNL Analytics] or Audience Manager segment so that [!DNL Google] can track the audience.

Each [!DNL Adobe] audience can be used for only one [!DNL Google] audience.

Each new [!DNL Google] audience has the same name as the original [!DNL Adobe] audience. [!DNL Google] determines how large the audience must be to be targetable.

>[!TIP]
>
>For real-time segmentation, use Audience Manager-created audiences. Segments created in [!DNL Analytics] and synced to Adobe Experience Cloud may have smaller populations because they're only synced daily; a surfer who qualifies for a segment may not be included in the segment until the next day. Segments from [!DNL Analytics] have a data source of "report suite - ."

>[!NOTE]
>
>Search, Social, & Commerce doesn't store any of the customer data from your [!DNL Adobe] segments used to create or edit a [!DNL Google] audience.

1. Complete the prerequisites as needed:
   
   1. (To create user ID remarketing list audiences) An [!DNL Adobe] admin user or account manager must select the advertiser-level setting to enable customer match audiences.

   1. Implement the [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) version 2.0 or higher.

   1. Deploy the following tag as high as possible on the advertiser's webpages from which the audience should be tracked

       `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`
     
       where `Advertising_Cloud_UserID` is the unique numeric user ID assigned to the advertiser.
       
       Example: `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`
     
   1. (If not already completed) An authorized user must configure the advertiser's account to [sync with the advertiser's organization account in Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Audiences] > [!UICONTROL Library]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network and the account name, and then click **[!UICONTROL Continue]**.

1. Specify the audience information:

   1. In the **[!UICONTROL Data Source]** menu, select **[!UICONTROL Adobe Audience]**.

   1. Select the [!UICONTROL Adobe Audience] on which to base the [!DNL Google] audience.

      >[!NOTE]
      >
      >[!DNL Adobe] audiences that are already used for another [!DNL Google] audience aren't available.

      You can optionally search for audiences that contain a specific text string with a minimum of three characters. For any matching audience, click **[!UICONTROL Include]** to select it.

      If you select multiple [!DNL Adobe] audiences, then a separate [!DNL Google] audience is created for each.

   1. Select the **[!UICONTROL Audience Type]** to create: **[!UICONTROL Customer List_User ID]**.

      The advertiser's [!DNL Google Ads] account must be [eligible for custom match](https://support.google.com/adspolicy/answer/6299717) and opted in for [user ID remarketing](https://support.google.com/google-ads/answer/9199250).

   1. Select the check box to indicate that you agree with the terms of the [!DNL Adobe] and ad network privacy policies.

   1. Specify the number of **[!UICONTROL Membership Days]**, which is the number of days a user's cookie stays in the audience.

      Use the length of time for which you expect your ad to be relevant to the user. Remarketing lists have a maximum duration of 540 days. Customer lists don't have a maximum duration; to indicate that the cookie never expires, enter 10000.

   1. Click **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] may take up to 24 hours to process the file.
>
>* See [[!DNL Google Ads] documentation on how customer match works and limitations](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [About audiences](audience-about.md)
>* [Create a [!DNL Google Ads] customer match audience from an Adobe Campaign email list](google-audience-from-campaign-email-list.md)
>* [Manage customer match audiences using customer data lists](audience-from-customer-data-list.md)
>* [Manage dynamic remarketing audiences](audience-dynamic-remarketing-manage.md)
