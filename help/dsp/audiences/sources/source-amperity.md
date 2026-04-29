---
title: Convert user IDs from [!DNL Amperity] to universal IDs
description: Learn how to enable DSP to ingest your [!DNL Amperity] first-party segments.
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
TQID: https://experienceleague.adobe.com/LOl3N6NB0alkOXiTNe7Xzj9mcVVfYxog3x-iIuVa82M
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
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
---
# Convert user IDs from [!DNL Amperity] to universal IDs

*Beta feature*

Use the DSP integration with the [!DNL Amperity] customer data platform to convert your organization's first-party hashed email addresses to universal IDs for targeted advertising.

1. (To convert email addresses to [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Set up tracking to enable [!DNL Analytics] measurement](#analytics-tracking).

1. [Create an audience source in DSP](#source-create).

1. [Prepare and share segment-mapping data](#map-data).

1. [Request a data push from [!DNL Amperity] to DSP](#push-data).

1. [Compare the number of universal IDs with the number of hashed email addresses](#compare-id-count).

## Step 1: Set up tracking for [!DNL Analytics] measurement {#analytics-tracking}

*Advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

To convert email addresses to [!DNL RampIDs] or [!DNL ID5] IDs, you must do the following:

1. (If you haven't already done so) Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
1. Register with the universal ID partner and deploy universal ID-specific code on your webpages to match conversions from the IDs on desktop and mobile web browsers (but not mobile apps) to view-throughs:
   
   * **For [!DNL RampIDs]:** You must deploy an additional JavaScript tag on your webpages to match conversions from the IDs on desktop and mobile web browsers (but not mobile apps) to view-throughs. Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag from [!DNL LiveRamp] Authentication Traffic Solutions. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

## Step 2: Create an audience source in DSP {#source-create}

1. [Create an audience source](source-manage.md) to import audiences to your DSP account or an advertiser account. You can choose to convert your user identifiers to any of the [available universal ID formats](source-about.md).

   The source settings will include an auto-generated source key, which you'll use to push the segment data.

1. After you create the audience source, share the source code key with the [!DNL Amperity] user.

## Step 3: Prepare and share segment-mapping data {#map-data}

The advertiser must prepare and share segment-mapping data.

1. Within [!DNL Amperity], hash the email IDs for the audience using the SHA-256 algorithm.

1. The advertiser must give segment-mapping data to the Adobe Account Team to create the segments in DSP. Use the following column names and values in a comma-separated values file:

   * **External Segment Key:** The [!DNL Amperity] segment key associated with the segment.
   
   * **Segment Name:** The segment name.
      
   * **Segment Description:** The purpose or rule of the segment, or both.
      
   * **Parent ID:** Keep blank
      
   * **Video CPM:** 0
   
   * **Display CPM:** 0

   * **Segment Window:** The segment time-to-live.
   
## Step 4: Request a data push from [!DNL Amperity] to DSP {#push-data}

1. After the segment is mapped within DSP, the advertiser must work with their [!DNL Amperity] representative to distribute the segment data to DSP.

1. The advertiser must then confirm with the Adobe Account Team that the segment data was received.

The segments should be available in DSP within 24 hours. Verify in your audience library (which is available when you create or edit an audience from [!UICONTROL Audiences] > [!UICONTROL All Audiences] or within placement settings) that the segment is available and is populating.

The segments will be refreshed as configured for the advertiser within [!DNL Amperity]. Regardless of how frequently the segment is refreshed, inclusion in a segment expires after 30 days by default or after a customer-specified expiration period. Refresh your segments by re-pushing them from [!DNL Amperity] prior to the expiration. To request a custom segment expiration, contact your Adobe Account Team.

## Step 5: Compare the number of universal IDs with the number of hashed email addresses {#compare-id-count}

After DSP receives the segment data, the audience count should be visible within nine (9) hours.

In your audience library (which is available when you create or edit an audience from [!UICONTROL Audiences] > [!UICONTROL All Audiences] or within placement settings) compare the number of universal IDs with the number of original hashed email addresses. For information about acceptable ID translation rates and why the segment counts can vary, see "[Data variances between email IDs and universal IDs](#universal-ids-data-variances)."

## Troubleshooting

To troubleshoot translation rate and user count issues, see "[Support for activating universal IDs](/help/dsp/audiences/universal-ids.md)."

To troubleshooting issues with the conversion procedure, contact your Adobe Account Team or `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [About first-party audience sources](/help/dsp/audiences/sources/source-about.md)
>* [Manage audience sources to activate universal ID audiences](source-manage.md)
>* [Support for activating universal IDs](/help/dsp/audiences/universal-ids.md)
>* [About audience management](/help/dsp/audiences/audience-about.md)
