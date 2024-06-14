---
title: Manage Audience Sources to Activate Universal ID Audiences
description: Learn how to create and manage a source to import audiences from your customer data platform and convert them to segments containing universal IDs.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
---
# Manage Audience Sources to Activate Universal ID Audiences

*Beta feature*

Create a source in DSP for each first-party audience in your customer data platform that you want to convert to segments containing specified universal ID types. You can import the segments to your organization's DSP account or to an advertiser account. Data charges are applied based on the selected universal ID types. Once you create a source, additional steps are required to ingest the audiences from each customer data platform. See the note at the end of the procedure to create a source.

You can later change the universal ID types to which the source audience is translated, and view a log of the changes.

You can also delete a source.

## Create an Audience Source

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Click **[!UICONTROL Add Source]**.

1. In the [!UICONTROL Select a Type] menu, select your [customer data platform](source-about.md):

   * *[!UICONTROL RT-CDP]*: The [!DNL Adobe Real-Time Customer Data Platform].

   * *[!UICONTROL ActionIQ]*: The [!DNL ActionIQ] customer data platform.

   * *[!UICONTROL Amperity]*: The [!DNL Amperity] customer data platform.

   * *[!UICONTROL Optimizely]*: The [!DNL Optimizely] customer data platform.

   * *[!UICONTROL Tealium CDP]*: (Configured users only) The [!DNL Tealium] customer data platform.

1. Specify the [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* or *[!UICONTROL Account]*.

1. Enter the remaining [source settings](#source-settings).

   Keep a copy of the [!UICONTROL Source Key] that is generated. You'll need the value later.

1. Click **[!UICONTROL Save]**.

>[!NOTE]
>
>After you create a source for your customer data platform, you'll need to complete additional steps to import your audience. See the [workflow for [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md),<!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), --> the [workflow for [!DNL Amperity]](source-amperity.md), the [workflow for [!DNL Optimizely]](source-optimizely.md), and the [workflow for [!DNL Tealium]](source-tealium.md).

## Change the ID Types for an Audience Source

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Hold the cursor over the source row and click **[!UICONTROL Edit]**.

1. Change the [IDs selected for the source](#source-settings).

1. Click **[!UICONTROL Save]**.

## Delete an Audience Source

Deleting a source removes the segments translated through the source.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Hold the cursor over the source row and click **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Delete]**.

## View the Change Log for an Audience Source

You can view details about changes to an audience source record and optionally attach notes to the log.

1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Hold the cursor over the source row and click **[!UICONTROL Change log]**.

1. (Optional) To attach a note to the change log:

   1. Hold the cursor over the source row and click **[!UICONTROL Add Notes]**.

   1. Enter the note, and then click **[!UICONTROL Save]**.

      The maximum length is 256 characters.

1. (Optional) To open the log in a larger detail screen, hold the cursor over the source row and click **[!UICONTROL View Details]**.

## Audience Source Settings {#source-settings}

**[!UICONTROL Data Visibility Level]:** Whether the segments are available to a single advertiser with access to the account (*[!UICONTROL Advertiser]*) or to all advertisers with access to the account *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Advertiser-level visibility only) The advertiser for whom the segments are available. Select one from the list of advertisers with access to the account.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] sources only) The Adobe Experience Cloud organization ID for the [!DNL Adobe Experience Platform] account.

**[!UICONTROL Convert PII to the following IDs]:** The ID types to which you'll convert your personally identifiable information (PII). If you select multiple types, the generated segment is populated with values for each selected ID type (such as a [!DNL RampID] and a [!DNL Unified ID2.0] for each email address). Data charges are applied accordingly.

For [!DNL RampID] and [!DNL Unified ID2.0], the vendor looks up each email address to see if an ID already exists and translates the address to a matching ID when available. If an ID doesn't exist for the address, then it creates a new ID.

>[!NOTE]
>
>You can target only one type of ID in a single placement. To test performance by ID type, [create a separate placement](/help/dsp/campaign-management/placements/placement-create.md) for each ID type in the segment.

* *[!DNL RampID]:* To convert PII to a [!DNL RampID]. You can use [!DNL RampIDs] for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

* *[!DNL Unified ID2.0] (Beta):* To convert PII to a [Unified ID 2.0](https://unifiedid.com) ID for retargeting logging-in users.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** The terms of service agreement for converting PII to universal IDs. You or another user in the DSP account must accept the terms once before you can convert data to a new ID type. For customers with managed service contracts, your Adobe Account Team will get your consent and accept the terms on your organization's behalf. To read the terms, click **>**. To accept the terms, scroll to the bottom of the terms and click **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Read-only; generated automatically) The source key you can use to create a destination connection in the customer data platform to push audiences to Advertising DSP. You can copy the value to your clipboard to paste into the destination connection settings or into a file.

>[!MORELIKETHIS]
>
>* [About First-Party Audience Sources](source-about.md)
>* [Support for Activating Universal IDs](/help/dsp/audiences/universal-ids.md)
>* [Convert User IDs from [!DNL Adobe Real-Time CDP] to Universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convert User IDs from [!DNL Amperity] to Universal IDs](/help/dsp/audiences/sources/source-amperity.md)
>* [Convert User IDs from [!DNL Optimizely] to Universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
>* [Convert User IDs from [!DNL Tealium] to Universal IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
