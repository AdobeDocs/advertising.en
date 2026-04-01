---
title: Manually import authenticated segments from [!DNL LiveRamp]
description: Learn about activating authenticated audiences through [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
TQID: https://experienceleague.adobe.com/ln4e1Jmq7vRhOIeg25UwNR8yToni5CuokxAcmEPMwEQ
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
---
# Manually import authenticated segments from [!DNL LiveRamp]

*Beta feature*

You can manually send authenticated [!DNL LiveRamp] segments to DSP using the [!DNL LiveRamp] [!DNL Connect] dashboard. You can use imported segments for placement targeting. For first-party segments, fees are USD 0.15 per display ad impression delivered and USD 0.25 per video ad impression delivered.

The segment mapping and uploading for each import job may take up to seven days. 

<!--
Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Complete the following steps in the [!DNL Connect] dashboard:

   1. Activate the destination tile **[!DNL AAC API 1P Onboarding]**.

   1. Set [!DNL Identifier Settings] to **[!DNL Ramp ID]** only.

      ![Identifier settings](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Optional) If you want to still receive cookie-based identifiers, create a second [!DNL AAC API 1P Onboarding] destination tile with “[!DNL Cookies],” "[!DNL IDFA],” and “[!DNL AAID]” selected.

   1. Verify in your audience library (which is available when you create or edit an audience from [!UICONTROL Audiences] > [!UICONTROL All Audiences] or within placement settings) that the entire segment count was imported.

>[!MORELIKETHIS]
>
>* [About first-party audience sources](source-about.md)
>* [Manage audience sources to activate universal ID audiences](source-manage.md)
>* [Adobe Advertising DSP connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [About audience management](/help/dsp/audiences/audience-about.md)
