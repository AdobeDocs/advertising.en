---
title: About Activating Authenticated Segments from Audience Sources
description: Learn about ingesting first-party segments from a customer data platform.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
---
# About Activating Authenticated Segments from Audience Sources

DSP can ingest first-party segments comprised of hashed email IDs or universal IDs built within a customer data platform (CDP). You can use the ingested segments as targets for your placements.

The following CDPs have established connectors, but the DSP can also connect to any CDP using batch, streaming, or API-based data sharing. To integrate with a new CDP, contact your Adobe Account Team. 

## [!DNL Adobe Real-Time Customer Data Platform]

DSP is integrated with [the [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), which is part of the Adobe Experience Platform.

In [!DNL Real-Time CDP], *destinations* are connections to external data platforms that allow seamless data activation. For example, you can use destinations to activate your known customer relationships (such as hashed email addresses) for targeted advertising across digital formats supported by DSP. For more information about destinations, see the Experience Platform [Destinations Guide](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), including an overview of the product, instructions for [creating destination workspaces](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) and [creating destination connections](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), and [activating data to destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

See "[Workflow for Using the DSP Integration with [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)."

## [!DNL ActionIQ]

You can share your organization's first-party data from the [!DNL Action IQ] customer data platform with DSP. You can then target your DSP placements to the segments using [!DNL RampIDs] or [!DNL Unified IDs 2.0].

This integration requires customization. Contact your Adobe Account Team for more information.

## [!DNL Tealium]

You can share your organization's first-party data from the [!DNL Tealium] customer data platform using [!DNL Amazon Web Services]. You can then target your DSP placements to the segments using [!DNL RampIDs]. See "[Workflow for Using the DSP Integration with [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)."

>[!MORELIKETHIS]
>
>* [Workflow for Using the DSP Integration with [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Workflow for Using the DSP Integration with [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)

<!--
>* [Workflow for Using the DSP Integration with [!DNL ActionIQ]](/help/dsp/audiences/sources/source-actioniq.md)
-->
