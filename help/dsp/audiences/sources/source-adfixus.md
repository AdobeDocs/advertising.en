---
title: Import first-party segments from [!DNL AdFixus]
description: Learn how to import your [!DNL AdFixus] first-party segments consisting of [!DNL AdFixus] universal IDs to DSP.
feature: DSP Audiences
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
# Import first-party segments from [!DNL AdFixus]

*Applicable to advertisers in Australia only*

Use the Advertising DSP integration with [!DNL AdFixus] to import your [!DNL AdFixus] universal IDs with segment mappings for targeted advertising. [!DNL AdFixus] IDs are available in Australia only. DSP doesn't change [!DNL AdFixus] IDs to other ID types, nor convert other ID types to [!DNL AdFixus] IDs.

Once you import your [!DNL AdFixus] segments to DSP, you can target placements to [!DNL AdFixus] IDs and to specific first-party segments from [!DNL AdFixus]. You can also add [!DNL AdFixus] segments to reusable audiences. The details for any segment include the count of applicable [!DNL AdFixus] IDs.

You can view the impression, click, frequency, and other metrics for users with [!DNL AdFixus] IDs in custom reports. Advertisers with [!DNL Analytics for Advertising] can also view view-through data for [!DNL AdFixus] IDs from Adobe Analytics, as well as data from Adobe Analytics within DSP.

1. Use [!DNL AdFixus] to convert your organization's first-party data to segments with [!DNL AdFixus] IDs.

   This requires a separate account with [!DNL AdFixus] and an active license key. You'll also need to implement [!DNL AdFixus]-specific code for your website properties and domains. Work directly with [!DNL AdFixus] to generate segments with IDs.

1. (Advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Set up tracking for [!DNL Analytics] measurement:

   1. (If you haven't already done so) Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md).
   
   1. Deploy [!DNL AdFixus]-specific code on your webpages to match conversions from the [!DNL AdFixus] IDs on desktop and mobile web browsers (but not mobile apps) to view-throughs.

1. Import your first-party [!DNL AdFixus] segments:

   1. [Create an audience source](source-manage.md) of [!UICONTROL Type] **[!UICONTROL AdFixus ID]**. You must consent to the terms of service agreement.

      The source settings will include an auto-generated source key.
   
   1. Share the source key with your [!DNL AdFixus] team so that they can stream the required segments to DSP.

1. Verify in the [!UICONTROL First Party Segments] section of your audience library (which is available when you create or edit an audience from [!UICONTROL Audiences] > [!UICONTROL All Audiences] or within placement settings) that the segment is populating. Compare the number of [!DNL AdFixus] IDs with the number of user IDs within [!DNL AdFixus].

   <!-- Verify:  The segments should be available in DSP within 24 hours. After DSP receives the segment data, the audience count should be visible within nine (9) hours. -->

<!-- Segments are refreshed every 24 hours. However, inclusion in a segment expires after 30 days by default or after a customer-specified expiration period. Refresh your segments by re-pushing them from [!DNL AdFixus] prior to the expiration. -->

>[!MORELIKETHIS]
>
>* [About first-party audience sources](/help/dsp/audiences/sources/source-about.md)
>* [Manage audience sources to activate universal ID audiences](source-manage.md)
>* [Adobe Advertising DSP connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Destinations catalog overview](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Support for activating universal IDs](/help/dsp/audiences/universal-ids.md)
>* [About audience management](/help/dsp/audiences/audience-about.md)
