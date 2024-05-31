---
title: Manually Import Authenticated Segments from [!DNL LiveRamp]
description: Learn about activating authenticated audiences through [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
---
# Manually Import Authenticated Segments from [!DNL LiveRamp]

*Beta feature*

You can manually send authenticated [!DNL LiveRamp] segments to DSP using the [!DNL LiveRamp] [!DNL Connect] dashboard. You can use imported segments for placement targeting. For first-party segments, fees are USD 0.15 per display ad impression delivered and USD 0.25 per video ad impression delivered.

The segment mapping and uploading for each import job may take up to seven days. 

<!--Is this first step relevant for this process?

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
>* [About First-Party Audience Sources](source-about.md)
>* [Create an Audience Source to Activate Universal ID Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
