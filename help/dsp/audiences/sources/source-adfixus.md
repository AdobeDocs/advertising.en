---
title: Using the DSP integration with [!DNL AdFixus]
description: Learn how to enable DSP to ingest your [!DNL AdFixus] first-party segments.
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
# Ingest user IDs from [!DNL AdFixus]

*Beta feature*

Use the DSP integration with [!DNL AdFixus] to import your [!DNL AdFixus] universal IDs for targeted advertising.

1. Send your organization's first-party data from your customer data platform to [!DNL AdFixus] to convert the data to [!DNL AdFixus] IDs.

   This requires a separate account with [!DNL AdFixus] and an active license key.
   
   You'll also need to implement [!DNL AdFixus]-specific code for your website properties and domains.

1. <!-- Is any of this step necessary since you aren't converting IDs to RampIDs? -->(Advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Set up tracking for [!DNL Analytics] measurement:

   1. (If you haven't already done so) Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md).
   
   1. <!-- Clarify if you need to do this and what the instructions should be -->Deploy [!DNL AdFixus]-specific code on your webpages to match conversions from the [!DNL AdFixus] IDs on desktop and mobile web browsers (but not mobile apps) to view-throughs.

1. [Create an audience source](source-manage.md) to import your [!DNL AdFixus] audiences to your DSP account or an advertiser account.<!-- what exactly happens here?  And are you importing a single audience, multiple, or what?  -->

   The source settings will include an auto-generated source key, which you'll use in the next step.

1. <!-- clarify if this is applicable -->In Adobe Experience Platform, configure an Advertising DSP destination connection using the [!UICONTROL Source Key] that was generated in the DSP source settings.
   
   For instructions for activating the DSP destination connection, activating audiences, and validating data export, see "[Adobe Advertising DSP connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)."

   >[!NOTE]
   >
   >Don't use the legacy connection, which includes support for only hashed email addresses and is now called "[Legacy Adobe Advertising Cloud DSP connection](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection-legacy)..

1. <!-- Verify if this is applicable, what the behavior is, and the wording -->Verify in your audience library (which is available when you create or edit an audience from [!UICONTROL Audiences] > [!UICONTROL All Audiences] or within placement settings) that the segment is populating, and compare the number of universal IDs with the number of user IDs within [!DNL AdFixus].

   The segments should be available in DSP within 24 hours. After DSP receives the segment data, the audience count should be visible within nine (9) hours.

Segments are refreshed every 24 hours. However, inclusion in a segment expires after 30 days by default or after a customer-specified expiration period. Refresh your segments by re-pushing them from Real-Time CDP prior to the expiration. To request a custom segment expiration, contact your Adobe Account Team.

## Troubleshooting

<!-- What's applicable here? -->

To troubleshoot translation rate and user count issues, see "[Support for activating universal IDs](/help/dsp/audiences/universal-ids.md)."

To troubleshooting issues with the conversion procedure, contact your Adobe Account Team or `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [About first-party audience sources](/help/dsp/audiences/sources/source-about.md)
>* [Manage audience sources to activate universal ID audiences](source-manage.md)
>* [Adobe Advertising DSP connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Destinations catalog overview](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Support for activating universal IDs](/help/dsp/audiences/universal-ids.md)
>* [About audience management](/help/dsp/audiences/audience-about.md)
