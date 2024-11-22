---
title: Using the DSP Integration with [!DNL Adobe] [!DNL Real-time CDP]
description: Learn how to enable DSP to ingest your [!DNL Adobe] [!DNL Real-time CDP] first-party segments.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
---
# Convert User IDs from [!DNL Adobe Real-Time CDP] to Universal IDs

*Beta feature*

Use the DSP integration with [the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), which is part of the Adobe Experience Platform, to convert your hashed email addresses to universal IDs for targeted advertising.

1. (To convert email addresses to [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Set up tracking for [!DNL Analytics] measurement:

   1. (If you haven't already done so) Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md).
   
   1. Register with the universal ID partner and deploy universal ID-specific code on your webpages to match conversions from the IDs on desktop and mobile web browsers (but not mobile apps) to view-throughs:
   
      * **For [!DNL RampIDs]:** You must deploy an additional JavaScript tag on your webpages to match conversions from the IDs on desktop and mobile web browsers (but not mobile apps) to view-throughs. Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag from [!DNL LiveRamp] Authentication Traffic Solutions. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

1. [Create an audience source](source-manage.md) to import audiences to your DSP account or an advertiser account. You can choose to convert your user identifiers to any of the [available universal ID formats](source-about.md).

   The source settings will include an auto-generated source key, which you'll use in the next step.

1. In Adobe Experience Platform, configure an Advertising DSP destination connection using the [!UICONTROL Source Key] that was generated in the DSP source settings.

   For instructions for activating the DSP destination connection, selecting segments, and accessing control permissions, see "[Adobe Advertising Cloud DSP connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)."

   The source email addresses must be hashed using the SHA-256 algorithm.

1. Verify in your audience library (which is available when you create or edit an audience from [!UICONTROL Audiences] > [!UICONTROL All Audiences] or within placement settings) that the segment is populating, and compare the number of universal IDs with the number of original hashed email addresses.

   The segments should be available in DSP within 24 hours. After DSP receives the segment data, the audience count should be visible within nine (9) hours. For information about acceptable ID translation rates and why the segment counts can vary, see "[Data Variances Between Email IDs and Universal IDs](#universal-ids-data-variances)."

Segments are refreshed every 24 hours. However, inclusion in a segment expires after 30 days by default or after a customer-specified expiration period. Refresh your segments by re-pushing them from Real-Time CDP prior to the expiration. To request a custom segment expiration, contact your Adobe Account Team.

## Troubleshooting

To troubleshoot translation rate and user count issues, see "[Support for Activating Universal IDs](/help/dsp/audiences/universal-ids.md)."

To troubleshooting issues with the conversion procedure, contact your Adobe Account Team or `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [About First-Party Audience Sources](/help/dsp/audiences/sources/source-about.md)
>* [Manage Audience Sources to Activate Universal ID Audiences](source-manage.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Destinations catalog overview](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Support for Activating Universal IDs](/help/dsp/audiences/universal-ids.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
