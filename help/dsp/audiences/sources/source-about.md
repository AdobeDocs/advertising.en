---
title: About Activating Authenticated and Probabilistic Audience Segments from Your First-Party Audiences
description: Learn about importing your universal ID segments and converting other user identifiers in your first-party segments to universal IDs for cookieless targeting.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
---
# About Activating Authenticated and Probabilistic  Segments from Your First-Party Audiences

<!-- Title and description? This will eventually include non-authenticated segments with probabilistic IDs -->

DSP supports people-based, universal IDs for cookieless, single-device (not cross-device) targeting across digital formats supported by DSP.

* DSP can ingest your first-party segments comprised of hashed email IDs<!-- or universal IDs --> built within your customer data platform (CDP) and convert them to universal IDs. Each resulting ID is people-based, and ad frequency caps are applied at the ID level<!-- Move that info. to somewhere else? -->.

* You can manually send your authenticated [[!DNL LiveRamp] [!DNL RampIDs]] directly to DSP using the [!DNL LiveRamp] [!DNL Connect] dashboard.

* Some third-party segment vendors have started including universal IDs in their segments, and you can use them in saved audiences and as placement targets without any extra steps.

Segment details include the size of each universal ID type as well as the size for each device type tracked by cookies or device IDs.

## Universal ID Types {#universal-id-types}

You can create segments with IDs from the following universal ID partners. <!-- Verify -->Each of the segments is updated every 24 hours.

* Authenticated (deterministic) IDs using hashed email addresses:

  * [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution): For retargeting logged-in users and for measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). [!DNL RampIDs] are available for users in North America, Australia, and New Zealand.<!-- Add fee info when available -->

    Measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). In addition, you must deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match conversions from the IDs to view-throughs. Contact your Adobe Account Team to get the tag and instructions for where to implement it.<!-- For instructions, see "[JavaScript Code for [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)." -->
  <!-- Will later require yet another JS tag too -->

  * [[!DNL Unified ID 2.0 (UID2.0)] IDs](https://unifiedid.com): For retargeting logged-in users. [!DNL UID2 IDs] aren't available for users in the European Economic Area and some additional countries. See the [list of prohibited countries](/help/policies/universal-id-policy.md#prohibited-countries-uid2).<!-- Add fee info when available -->

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).<!-- What countries/geos are these available for? Everywhere?--><!-- no fee -->

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    Measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). In addition, you must deploy a second JavaScript tag for [!DNL ID5] on your webpages to match conversions from the IDs to view-throughs. Contact your Adobe Account Team to get the tag and instructions for where to implement it.<!-- For instructions, see "[JavaScript Code for [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)." -->
    <!-- Will later require yet another JS tag too -->

    <!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
    -->

### Reporting by Universal ID Type

* **Segment details:** Segment details include the audience size by universal ID type and by device type.

* **Custom reports:** Cost, impression, click, conversion, and frequency data by universal ID type is available in custom reports.

* **[!DNL Analytics] reports:** Advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) who have implemented all required steps can see view-through conversions by universal ID type in [!DNL Analytics].

## Supported Customer Data Platforms

DSP has established connectors to the following CDPs to quickly ingest your first-party segments.

DSP can also connect to any additional CDPs using batch, streaming, or API-based data sharing. To integrate with a new CDP, contact your Adobe Account Team.

### [!DNL Adobe Real-Time Customer Data Platform]

DSP is an integrated *destination* for [the [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), which is part of the Adobe Experience Platform.

In [!DNL Real-Time CDP], destinations are connections to external data platforms that allow seamless data activation. You can use destinations to activate your hashed email addresses for targeted advertising in DSP. For more information about destinations, see the Experience Platform [Destinations Guide](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), including an overview of the product, instructions for [creating destination workspaces](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) and [creating destination connections](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), and [activating data to destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

To enable DSP to ingest your [!DNL Adobe] [!DNL Real-time CDP] first-party segments and convert your user data to universal IDs, see "[Convert User IDs from [!DNL Adobe Real-Time CDP] to Universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)."

### [!DNL ActionIQ]

You can share your organization's first-party data from the [!DNL Action IQ] customer data platform with DSP to convert your user data<!-- hashed email addresses ? --> to universal IDs for targeted advertising in DSP. This integration requires customization. Contact your Adobe Account Team for more information.

### [!DNL Tealium]

You can share your organization's first-party data from the [!DNL Tealium] customer data platform using [!DNL Amazon Web Services]. For more information about converting your user data<!-- hashed email addresses ? --> to universal IDs for targeted advertising in DSP, see "[Convert User IDs from [!DNL Tealium] to Universal IDs](/help/dsp/audiences/sources/source-tealium.md)."

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

* Remember that the reach for authenticated audience segments is naturally smaller than the reach for cookie-based segments, and that using additional targeting options further decreases your reach. Be judicious about using granular targeting, especially by joining multiple targets with AND statements.

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
