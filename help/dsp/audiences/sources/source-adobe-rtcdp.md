---
title: Using the DSP Integration with [!DNL Adobe] [!DNL Real-time CDP]
description: Learn how to enable DSP to ingest your [!DNL Adobe] [!DNL Real-time CDP] first-party segments.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
---
# Convert User IDs from [!DNL Adobe Real-Time CDP] to Universal IDs

Use the DSP integration with [the [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), which is part of the Adobe Experience Platform, to convert your hashed email addresses to universal IDs for targeted advertising.

<!-- Any pre-requisite settings within DSP?

1. Contact `adcloud-support@adobe.com` to enable the account-level “[!UICONTROL LiveRamp segments]” option, which will allow you to target authenticated segments in DSP campaigns once all steps in the activation workflow are completed.

-->

1. [Create an audience source](source-create.md) to import audiences to your DSP account or an advertiser account. You can choose to convert your user identifiers to any of the [available universal ID formats](source-about.md).

1. In Adobe Experience Platform, configure an Advertising DSP destination connection using the [!UICONTROL Source Key] that was generated in the DSP source settings.

   For instructions for activating the DSP destination connection, selecting segments, and accessing control permissions, see "[Adobe Advertising Cloud DSP connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)."

1. After you complete all steps, verify in <!-- Where? Aren't the imported segments available in Audiences > All Audiences, but you have to create/edit a saved audience to see them? They won't show up in Audiences > Segments (which is just for custom segments and CCPA segments you manually create in our UI) Don't you have to  [!UICONTROL Audiences] --> that the segment is populating within 24 hours. Compare the number of universal IDs with the number of original hashed email addresses.

   The translation rate of hashed email addresses to universal IDs should be greater than 90%. For example, if you send 100 hashed email addresses from your customer data platform, they should be translated to more than 90 universal IDs. A translation rate of 90% or less is an issue.
   
   For troubleshooting support, contact your Adobe Account Team or `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Activate Authenticated Segments from Universal ID Partners](source-universal-id.md)
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Destinations catalog overview](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Convert User IDs from [!DNL Tealium] to Universal IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
