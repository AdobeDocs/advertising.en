---
title: Using the DSP Integration with [!DNL Adobe] [!DNL Real-time CDP]
description: Learn how to enable DSP to ingest your [!DNL Adobe] [!DNL Real-time CDP] first-party segments.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
---
# Convert User IDs from [!DNL Adobe Real-Time CDP] to Universal IDs

Use the DSP integration with [the [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), which is part of the Adobe Experience Platform, to convert your hashed email addresses to universal IDs for targeted advertising.

1. (To convert email addresses to [!DNL RampIDs] or [!DNL ID5] IDs; advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Set up tracking for [!DNL Analytics] measurement:

   1. (If you haven't already done so) Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md).
   
   1. Register with the universal ID partner and deploy universal ID-specific code on your webpages to match conversions from the IDs on desktop and mobile web browsers (but not mobile apps) to view-throughs:
   
      * **For [!DNL RampIDs]:** You must deploy a second JavaScript tag on your webpages to match conversions from the IDs on desktop and mobile web browsers (but not mobile apps) to view-throughs. Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag from [!DNL LiveRamp] Authentication Traffic Solutions. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.
      
      * **For [!DNL ID5] IDs:** Contact your Adobe Account Team, who will give you instructions for signing a free agreement with [!DNL ID5]. Once you sign the agreement, a member of ID5’s technical team will provide your partner ID, which you must share with your Adobe Account Team. You then must specify the partner ID within your existing JavaScript tracking tags.
      
        <!-- You can verify calls using the network tab of a browser developer tool:  Each call is initiated to the domain `lasteventf-tm.everesttech.net` and contains the parameter `_les_id5` with an encrypted ID5 ID as its value -->

1. [Create an audience source](source-create.md) to import audiences to your DSP account or an advertiser account. You can choose to convert your user identifiers to any of the [available universal ID formats](source-about.md).

1. In Adobe Experience Platform, configure an Advertising DSP destination connection using the [!UICONTROL Source Key] that was generated in the DSP source settings.

   For instructions for activating the DSP destination connection, selecting segments, and accessing control permissions, see "[Adobe Advertising Cloud DSP connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)."

1. After you complete all steps, verify in your audience library (which is available when you create or edit an audience from [!UICONTROL Audiences] > [!UICONTROL All Audiences] or within placement settings) that the segment is populating within 24 hours. Compare the number of universal IDs with the number of original hashed email addresses.

   The translation rate of hashed email addresses to universal IDs should be greater than 90%. For example, if you send 100 hashed email addresses from your customer data platform, they should be translated to more than 90 universal IDs. A translation rate of 90% or less is an issue.
   
   For troubleshooting support, contact your Adobe Account Team or `adcloud-support@adobe.com`.

Segments are refreshed every 24 hours.

>[!MORELIKETHIS]
>
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Destinations catalog overview](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Manually Import Authenticated Segments from [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Convert User IDs from [!DNL Tealium] to Universal IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
