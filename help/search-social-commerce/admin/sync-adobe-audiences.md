---
title: Sync [!DNL Adobe] audiences
description: Learn how to sync metadata, hierarchy data, and unique audience data for your [!DNL Adobe] audiences.
exl-id: 8b8c3aa0-2aa9-4ad7-a4c0-1b7ba881acd3
feature: Search Admin
---
# Sync [!DNL Adobe] audiences

*[!DNL Direct Access] client managers and administrators only*

*Advertisers with an Adobe Advertising-Adobe Audience Manager or Adobe Advertising-Adobe Analytics integration only*

You can allow Search, Social, & Commerce to pull in metadata, hierarchy data, and unique audience data for all of an advertiser's or agency's [!DNL Adobe] audiences into the [!UICONTROL Campaigns] > [!UICONTROL Audiences] views. This information includes data for:

* Adobe Audience Manager segments

* Adobe Analytics segments that are published to Adobe Experience Cloud

* Segments that are created using the Adobe Experience Cloud [!DNL Audience Library]

To be eligible, the advertiser or agency must implement the [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) and provide its organization ID (formerly called [!DNL IMS Org ID]).

The initial sync takes about 24 hours. After that, data is synced in real time, with a one- to two- second delay.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup]**.

1. Enter the unique organization ID for the advertiser's Adobe Experience Cloud account, and then click **[!UICONTROL Submit]**.

   If you don't know the advertiser's organization ID, look it up in the **[!UICONTROL IMS Org ID]** field in the advertiser's settings at [!UICONTROL Admin] > [!UICONTROL Manage Client].

>[!MORELIKETHIS]
>
>* [About audiences](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)
>* [Integration with Adobe Experience Cloud solutions and services](/help/search-social-commerce/introduction/integrations.md)
