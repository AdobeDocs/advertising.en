---
title: Create an Audience Source to Activate First-Party Audiences
description: Learn how to create a source to import audiences to your account or an advertiser account.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
---
# Create an Audience Source to Activate First-Party Audiences

Create a source in DSP for each first-party audience in your customer data platform that you want to convert to segments containing specified universal ID types. You can import the segments to your organization's DSP account or to an advertiser account. Data charges are applied based on the selected universal ID types.

<!-- 
Create a source in DSP to import your first-party audiences to your DSP account or an advertiser account and convert them to universal IDs. You can create multiple types of IDs for each source (such as a [!DNL RampID] and a [!DNL Unified ID2.0] for each email address). Data charges are applied accordingly.

-->

Additional steps are required to ingest the audiences from each customer data platform. See [the audience-specific activation workflows](source-about.md)

1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Click **[!UICONTROL Add Source]**.

1. In the [!UICONTROL Select a Type] menu, select the source type.

   * *[!UICONTROL RT-CDP]*: [The [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*: The [[!DNL ActionIQ] customer data platform](source-about.md).

   * *[!UICONTROL Tealium CDP]*: (Configured users only) The [[!DNL Tealium] customer data platform](source-about.md).

1. Specify the [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* or *[!UICONTROL Account]*.

1. Enter the remaining [source settings](source-settings.md).

   Keep a copy of the [!UICONTROL Source Key] that is generated. You'll need the value later.

1. Click **[!UICONTROL Save]**.

>[!NOTE]
>
>After you create a source for your customer data platform, you'll need to complete additional steps. See the [workflow for importing audiences from [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> and the [workflow for importing audiences from [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Audience Source Settings](source-settings.md)
>* [About Activating Authenticated Segments from Audience Sources](source-about.md)
>* [Activate Authenticated Segments from Universal ID Partners](source-import-liveramp-segments.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
