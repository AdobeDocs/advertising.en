---
title: Create an Audience Source to Activate First-Party Audiences
description: Learn how to create a source to import audiences to your account or an advertiser account.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
---
# Create an Audience Source to Activate First-Party Audiences

*Beta feature*

<!-- Will this remain for admin users/Adobe account teams only? -->

Create a source to import audiences to your DSP account or an advertiser account. Currently, you can import audiences from [the [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html).

>[!NOTE]
>
>After you create a source for the [!DNL Real-Time CDP], you'll need to activate your [!DNL Real-Time CDP] audiences through the Adobe Advertising DSP destination within [!DNL Real-Time CDP] to begin importing them. See [the steps in the activation workflow](source-about.md#workflow-sources).

1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL Sources (BETA)].

1. Click [!UICONTROL Add Source].

1. In the [!UICONTROL Select a Type] menu, select the source type.

   *[!UICONTROL RT-CDP]*:  This source type, for [the [!DNL Adobe Real-Time Customer Data Profile]](source-about.md), is the only option.

1. Specify the [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* or *[!UICONTROL Account]*.

1. Enter the remaining [source settings](source-settings.md).

   Keep a copy of the [!UICONTROL Source Key] that is generated. You'll need the value later.

1. Click **[!UICONTROL Save]**.

1. In Experience Platform, create an Advertising DSP destination connection using the [!UICONTROL Source Key] that was generated in the DSP source settings.

   For instructions for activating the DSP destination connection, selecting segments, and accessing control permissions, see "[Adobe Advertising Cloud DSP connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-connection.html)."

>[!MORELIKETHIS]
>
>* [Audience Source Settings](source-settings.md)
>* [About Activating Authenticated Segments from Audience Sources](source-about.md)
>* [Activate Authenticated Segments from Durable ID Partners](source-durable-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-connection.html)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
