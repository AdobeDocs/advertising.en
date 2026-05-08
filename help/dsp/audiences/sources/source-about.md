---
title: About first-party audience sources
description: Learn about converting other user identifiers in your first-party segments to universal IDs for cookieless targeting.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
TQID: https://experienceleague.adobe.com/8wdjwhNF-KDspEa1wSYWwlDOJxc3LiyqnSwEE-Fq9bY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
    internal-label: DSP Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
---
# About first-party audience sources

DSP can ingest first-party segments comprised of hashed email IDs, cookies, and mobile advertising IDs (MAIDs) built within your customer data platforms (CDPs) and convert them to segments comprised of [!DNL LiveRamp] [!DNL RampIDs] and [!DNL Unified ID 2.0 (UID2.0)] IDs.

Advertisers in Australia can also import first-party segments that already contain [!DNL AdFixus] universal IDs (without DSP converting those IDs to other universal ID types). For that workflow, see "[Import first-party segments from [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)."

For all ID types, each resulting ID is people-based, and ad frequency caps are applied at the ID level<!-- Move that info. to somewhere else? -->. Segment details include the size of each universal ID type as well as the size for each device type tracked by cookies or device IDs.

## Universal ID types to which you can translate first-party segments {#universal-id-types}

<!--
  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

You can translate your first-party segments from [!DNL ActionIQ], [!DNL Adobe] [!DNL Real-time CDP], [!DNL Amperity], [!DNL Optimizely], and [!DNL Tealium] to segments with authenticated (deterministic) IDs from the following universal ID partners.

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

  * For retargeting logged-in users.
  
    [!DNL RampIDs] are available for users in North America, Australia, and New Zealand.
    
    Fees are USD 0.15 per display ad impression delivered and USD 0.25 per video ad impression delivered. 
  
  * For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] IDs](https://unifiedid.com):

  * For retargeting logged-in users.
  
    [!DNL UID2 IDs] aren't available for users in the European Economic Area and some additional countries. See the [list of prohibited countries](/help/policies/universal-id-policy.md#prohibited-countries-uid2).
    
    Fees are USD 0.15 per display ad impression delivered and USD 0.25 per video ad impression delivered.

<!--
 Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. Contact your Adobe Account Team for instructions.
-->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## Supported customer data platforms for first-party segments

DSP has established connectors to the following CDPs to quickly ingest your first-party segments.

DSP can also connect to any additional CDPs using batch, streaming, or API-based data sharing. To integrate with a new CDP, contact your Adobe Account Team.

### [!DNL ActionIQ]

You can share your organization's first-party data from the [!DNL ActionIQ] customer data platform with DSP to convert your hashed email addresses to universal IDs for targeted advertising in DSP. This integration requires customization. Contact your Adobe Account Team for more information.

### [!DNL Adobe Real-Time CDP]

DSP is an integrated *destination* for [the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), which is part of the Adobe Experience Platform.

In [!DNL Real-Time CDP], destinations are connections to external data platforms that allow seamless data activation. You can use destinations to activate your hashed email addresses, cookies, and mobile advertising IDs for targeted advertising in DSP. For more information about destinations, see the Experience Platform [Destinations Guide](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), including an overview of the product, instructions for [creating destination workspaces](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) and [creating destination connections](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), and [activating data to destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

To enable DSP to ingest your [!DNL Adobe] [!DNL Real-time CDP] first-party segments and convert your hashed email addresses, cookies, and mobile advertising IDs to universal IDs, see "[Convert user IDs from [!DNL Adobe Real-Time CDP] to universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)."

### [!DNL AdFixus]

Australian advertisers can use the Advertising DSP integration with [!DNL AdFixus] to import first-party segments that contain [!DNL AdFixus] universal IDs. This path is separate from translating hashed email IDs or MAIDs within a CDP connector to [!DNL RampIDs] or [!DNL UID2] IDs. For more information, see "[Import first-party segments from [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)."

### [!DNL Amperity]

You can share your organization's first-party data from the [!DNL Amperity] customer data platform with DSP to convert your hashed email addresses to universal IDs for targeted advertising in DSP. For more information, see "[Convert user IDs from [!DNL Amperity] to universal IDs](/help/dsp/audiences/sources/source-amperity.md)."

### [!DNL Optimizely]

You can share your organization's first-party data from the [!DNL Optimizely] customer data platform with DSP to convert your hashed email addresses to universal IDs for targeted advertising in DSP. For more information, see "[Convert user IDs from [!DNL Optimizely] to universal IDs](/help/dsp/audiences/sources/source-optimizely.md)."

### [!DNL Tealium]

You can share your organization's first-party data from the [!DNL Tealium] customer data platform using [!DNL Amazon Web Services]. For more information about converting your hashed email addresses to universal IDs for targeted advertising in DSP, see "[Convert user IDs from [!DNL Tealium] to universal IDs](/help/dsp/audiences/sources/source-tealium.md)."

>[!MORELIKETHIS]
>
>* [Manage audience sources to activate universal ID audiences](source-manage.md)
>* [Support for activating universal IDs](/help/dsp/audiences/universal-ids.md)
>* [Convert user IDs from [!DNL Adobe Real-Time CDP] to universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convert user IDs from [!DNL Amperity] to universal IDs](/help/dsp/audiences/sources/source-amperity.md)
>* [Convert user IDs from [!DNL Optimizely] to universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
>* [Convert user IDs from [!DNL Tealium] to universal IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Import first-party segments from [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)
>* [About audience management](/help/dsp/audiences/audience-about.md)
>* [Placement settings](/help/dsp/campaign-management/placements/placement-settings.md)
