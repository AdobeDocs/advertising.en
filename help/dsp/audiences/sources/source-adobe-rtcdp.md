---
title: "Workflow for Using the DSP Integration with [!DNL Adobe] [!DNL Real-time CDP]"
description: "Learn how to enable DSP to ingest your [!DNL Adobe] [!DNL Real-time CDP] first-party segments."
feature: DSP Audiences
---
# Workflow for Using the DSP Integration with [!DNL Adobe Real-Time CDP]

1. [Allow DSP to translate customer data segments into [!DNL LiveRamp RampIDs]](source-universal-id.md) that are recognizable in a biddable environment.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [Create an audience source](source-create.md) to import audiences to your DSP account or an advertiser account.

1. In Experience Platform, configure an Advertising DSP destination connection using the [!UICONTROL Source Key] that was generated in the DSP source settings.

   For instructions for activating the DSP destination connection, selecting segments, and accessing control permissions, see "[Adobe Advertising Cloud DSP connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)."

For additional support, contact your Adobe Account Team or `adcloud-support@adobe.com`.


>[!MORELIKETHIS]
>
>* [Activate Authenticated Segments from Universal ID Partners](source-universal-id.md)
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Destinations catalog overview](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Workflow for Using the DSP Integration with [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
