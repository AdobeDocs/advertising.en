---
title: Create and Manage Audience Sources to Activate Universal ID Audiences
description: Learn how to create and manage a source to import audiences from your customer data platform and convert them to segments containing universal IDs.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
---
# Create an Audience Source to Activate Universal ID Audiences

*Beta feature*

Create a source in DSP for each first-party audience in your customer data platform that you want to convert to segments containing specified universal ID types. You can import the segments to your organization's DSP account or to an advertiser account. Data charges are applied based on the selected universal ID types.

Additional steps are required to ingest the audiences from each customer data platform. See the note at the end of the procedure.

## Create an Audience Source

1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Click **[!UICONTROL Add Source]**.

1. In the [!UICONTROL Select a Type] menu, select your customer data platform:

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

## Change the ID Types for an Audience Source

1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Hold the cursor over the source row and click **[!UICONTROL Edit]**.

1. Change the [IDs selected for the source](source-settings.md).

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

>[!MORELIKETHIS]
>
>* [Audience Source Settings](source-settings.md)
>* [About First-Party Audience Sources](source-about.md)
>* [Adobe Advertising Cloud DSP connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
