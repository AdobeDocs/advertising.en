---
title: About Activating Authenticated Audience Segments from Your First-Party Audiences
description: Learn about converting user identifiers in your first-party segments to universal IDs for cookieless targeting.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
---
# About Activating Authenticated Segments from Your First-Party Audiences

<!-- Title and description? This will eventually include non-authenticated segments with probabilistic IDs -->

DSP supports people-based, universal IDs for cookieless, single-device (not cross-device) targeting.

DSP can ingest your first-party segments comprised of hashed email IDs<!-- or universal IDs --> built within your customer data platform (CDP) and convert them to universal IDs. Each resulting ID is people-based, and ad frequency caps are applied at the ID level.

You can also manually send your authenticated [[!DNL LiveRamp] [!DNL RampIDs]] directly to DSP using the [!DNL LiveRamp] [!DNL Connect] dashboard.

<!-- In addition, some third-party segment vendors have started sending universal IDs with XXX. [explain more] -->

## Universal ID Types {#universal-id-types}

You can create segments with IDs from the following universal ID partners:

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution): For retargeting logged-in users and for measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). [!DNL RampIDs] are available for users in North America, Australia, and New Zealand.

  Measurement requires the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md).<!--AND ANYTHING ELSE -->

* [[!DNL Unified ID 2.0 (UID2.0)] IDs](https://unifiedid.com): For retargeting logged-in users. [!DNL UID2 IDs] aren't available for users in the European Economic Area and some additional countries. See the [list of prohibited countries](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  >[!NOTE]
  >
  >Third-party segments from [!DNL Eyeota] and [!DNL Neustar] may also include UID2.0 IDs.

<!--

* Authenticated (deterministic) IDs using hashed email addresses:

  * Ramp: uses multiple user signals (such as hashed email addresses and phone number) -- With RT CDP, I think we just take HEMs. 

  *

* Probabilistic (unauthenticated) IDs using XX data: [VERIFY specifically what data types are allowed, and edit top-level info accordingly if more than hashed emails.]

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

    Measurement requires the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md).
  
    ID5 creates an ID by stitching together various client/server signals, such as an IP address, user agent string, and hashed email address. [Field-level help says "browser signals (IP address, timestamp) and user signals (email) when available."]

-->


<!--
Is this a one-time thing, or do we continue to connect with any sources periodically to update the segments? If yes, how often do we update?
-->

Cost, impression, click, conversion, and frequency data by universal ID type is available in custom reports. Advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) can see view-through conversions in [!DNL Analytics].

## Customer Data Platforms with Established Connectors

The following CDPs have established connectors, but DSP can also connect to any CDP using batch, streaming, or API-based data sharing. To integrate with a new CDP, contact your Adobe Account Team.

### [!DNL Adobe Real-Time Customer Data Platform]

DSP is an integrated destination for [the [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), which is part of the Adobe Experience Platform. This integration allows you to share authenticated first-party segments with approved advertisers and users for campaign activation.

In [!DNL Real-Time CDP], *destinations* are connections to external data platforms that allow seamless data activation. You can use destinations to activate your hashed email addresses for targeted advertising across digital formats supported by DSP. For more information about destinations, see the Experience Platform [Destinations Guide](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), including an overview of the product, instructions for [creating destination workspaces](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) and [creating destination connections](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), and [activating data to destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

To enable DSP to ingest your [!DNL Adobe] [!DNL Real-time CDP] first-party segments and convert your user data to universal IDs, see "[Convert User IDs from [!DNL Adobe Real-Time CDP] to Universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)."

### [!DNL ActionIQ]

You can share your organization's first-party data from the [!DNL Action IQ] customer data platform with DSP to convert your user data to universal IDs. This integration requires customization. Contact your Adobe Account Team for more information.

### [!DNL Tealium]

You can share your organization's first-party data from the [!DNL Tealium] customer data platform using [!DNL Amazon Web Services]. For more information about converting your user data to universal IDs, see "[Convert User IDs from [!DNL Tealium] to Universal IDs](/help/dsp/audiences/sources/source-tealium.md)."

## How to Target an Authenticated Audience in Your Placements

When you create a placement, do the following:

* In the [!UICONTROL Geo-Targeting] section, specify the geographical areas to target. Remember that [each universal ID partner allows user targeting only in specific geographical areas](#universal-id-types).

* In the [!UICONTROL Audience Targeting] section, do the following:

  * In the [!UICONTROL Included Audiences] setting, select the segment for which user data was converted to universal IDs.

    You can include additional segments if you want.

  * In the [!UICONTROL Targeting] setting, select the universal ID type to target.
  
    The setting includes the options "[!UICONTROL Legacy IDs]" and "[!UICONTROL Universal ID]," which may include the sub-options "[!UICONTROL RampID]" and "[!UICONTROL Unified ID2.0]." The actual sub-options are determined by the selected geographical targets.
    
    You can select both "[!UICONTROL Legacy IDs]" and "[!UICONTROL Universal ID]," but you can select only one type of universal ID per placement. When you select both legacy IDs and universal IDs, bidding preference is given to universal IDs. 

See "[Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)."

<!--
## Frequency 
-->

## Best Practices for Testing and Data Validation

* About 24 hours after you activate a segment, check the converted ID count for the segment within [!UICONTROL Audiences] > [!UICONTROL All Audiences]. If the ID count is unexpected, contact your Adobe Account Team. <!-- What can be causes of data variances, and how much variance can be expected? -->

* Test the following use cases:

  * To compare the performance of universal ID-based segments with the performance of placements targeting other audience identifiers, such as cookies or mobile advertising IDs, create a campaign with a separate universal ID-based placement and a legacy ID-based placement.

    Use the following configuration:

    * The recommended campaign budget is USD 10,000. Split the budget evenly between the universal ID-based placement (test group) and the legacy ID-based placement (test group).

    * The recommended audience size is 25,000 universal IDs.

    * Run the placements for at least three weeks.

    * Use the following ad types: display, video, CTV, universal video, and audio

    Getting the best performance, however, shouldn't be the primary comparison. Instead, determine which IDs are scaling well, which might inform your optimization and budget allocations later. The long-term goal is to make up for lost impressions and site traffic when cookies are deprecated.

  * To compare total browser reach, target universal ID-based segments and legacy ID-based segments in the same placement. Use the same campaign settings as the previous use case, except that you don't need to split the campaign budget.
  
    Bidding preference is given to universal IDs, but legacy IDs will receive bids when universal IDs aren't available. Make sure to compare reach in different browsers (including Chrome, Safari, and Mozilla).
 
    >[!NOTE]
    >
    >Frequency capping applies to an individual ID. When you target multiple ID types, you might be reaching the same user.

<!-- Keep? If so, put this where? 

  * Currently, [!DNL RampIDs] aren't retrievable during on-site events. This means that certain custom goals, such as Lowest CPA and ROAS, aren't available with the use of authenticated segments. Use cookie-based segments only if you have a restrictive performance KPI.

-->

>[!MORELIKETHIS]
>
>* [Convert User IDs from [!DNL Adobe Real-Time CDP] to Universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convert User IDs from [!DNL Tealium] to Universal IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
