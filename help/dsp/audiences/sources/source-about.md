---
title: About Activating Authenticated Segments from Audience Sources
description: Learn about ingesting first-party segments from a customer data platform.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
---
# About Activating Authenticated Segments from Audience Sources

<!-- Title? Not sure the segments are referred to probabilistic (the IDs/device graphs are), but this now includes non-authenticated segments -->

DSP enables you to convert your first-party <!--AND THIRD-PARTY?--> data to people-based, universal IDs for cookieless, single-device (not cross-device) targeting. DSP can ingest your segments comprised of hashed email IDs or universal IDs built within your customer data platform (CDP). Each resulting ID is people-based, and ad frequency caps are applied at the ID level.

## Universal ID Types

You can create segments with IDs from the following universal ID partners:

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution): For retargeting logged-in users and for measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). [!DNL RampIDs] are available for users in North America, Australia, and New Zealand.

  Measurement requires the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md).<!--AND ANYTHING ELSE -->

* [[!DNL Unified ID 2.0 (UID2.0)] IDs](https://unifiedid.com): For retargeting logged-in users. [!DNL UID2 IDs] aren't available for users in the European Economic Area and some additional countries. See the [list of prohibited countries](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  The vendor looks up the email address to see if an ID already exists. If an ID doesn't exist, then it creates a new ID.

<!--

* Authenticated IDs using hashed email addresses:

  *

  *

* Probabilistic (unauthenticated) IDs using XX data: [VERIFY specifically what data types are allowed, and edit top-level info accordingly if more than hashed emails.]

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

    Measurement requires the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md).
  
    ID5 creates an ID based on soft signals, such as IP address and timestamp. [Reword to clarify]

-->


<!--
Is this a one-time thing, or do we continue to connect with any sources periodically to update the segments? If yes, how often do we update?
-->

Cost, impression, click, conversion, and frequency data by universal ID type is available in custom reports. Advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) can see view-through conversions in [!DNL Analytics].

## Customer Data Platforms with Established Connectors

The following CDPs have established connectors, but DSP can also connect to any CDP using batch, streaming, or API-based data sharing. To integrate with a new CDP, contact your Adobe Account Team.

### [!DNL Adobe Real-Time Customer Data Platform]

DSP is an integrated destination for [the [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), which is part of the Adobe Experience Platform. This integration allows you to share authenticated first-party segments with approved advertisers and users for campaign activation.

In [!DNL Real-Time CDP], *destinations* are connections to external data platforms that allow seamless data activation. For example, you can use destinations to activate your known customer relationships (such as hashed email addresses) for targeted advertising across digital formats supported by DSP. For more information about destinations, see the Experience Platform [Destinations Guide](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), including an overview of the product, instructions for [creating destination workspaces](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) and [creating destination connections](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), and [activating data to destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

To enable DSP to ingest your [!DNL Adobe] [!DNL Real-time CDP] first-party segments, see "[Workflow for Using the DSP Integration with [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)."

### [!DNL ActionIQ]

You can share your organization's first-party data from the [!DNL Action IQ] customer data platform with DSP. This integration requires customization. Contact your Adobe Account Team for more information.

### [!DNL Tealium]

You can share your organization's first-party data from the [!DNL Tealium] customer data platform using [!DNL Amazon Web Services]. For more information, see "[Workflow for Using the DSP Integration with [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)."

## How to Target an Authenticated Audience in Your Placements

In the [!UICONTROL Audience Targeting] section of each placement, a [!UICONTROL Targeting] setting includes the options "[!UICONTROL Legacy IDs]" and "[!UICONTROL Universal ID]," which may include the sub-options "[!UICONTROL RampID]" and "[!UICONTROL Unified ID2.0]." The actual sub-options are determined by the selected geographical targets in the [!UICONTROL Geo-Targeting] section.

You can select both "[!UICONTROL Legacy IDs]" and "[!UICONTROL Universal ID]," but you can select only one type of universal ID per placement.

See "[Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)."

<!--
## Frequency 
-->

>[!MORELIKETHIS]
>
>* [Workflow for Using the DSP Integration with [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Workflow for Using the DSP Integration with [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)

<!--
>* [Workflow for Using the DSP Integration with [!DNL ActionIQ]](/help/dsp/audiences/sources/source-actioniq.md)
-->
