---
title: Manually Import Authenticated Segments from [!DNL LiveRamp]
description: Learn about activating authenticated audiences through [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
---
# Manually Import Authenticated Segments from [!DNL LiveRamp]

<!-- Title:
Workflow to Manually Import Authenticated Segments from [!DNL LiveRamp]
Manually Activate Authenticated Segments from [!DNL LiveRamp]
Manually Activate Authenticated Segments from Universal ID partners

If I change it, update filename, create a redirect from the old page to the new one, and update all x-refs.
-->

You can manually send authenticated [!DNL LiveRamp] segments to DSP using the [!DNL LiveRamp] [!DNL Connect] dashboard. 

<!-- 1. Probably selected by default for all users, but verifyContact `adcloud-support@adobe.com` to enable importing of [!UICONTROL LiveRamp] segments. Include the account name and applicable advertisers.  -->

<!--Is this necessary for this process, too?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   Measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). In addition, you must deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

-->

1. Complete the following steps in the [!DNL Connect] dashboard:

   1. Activate the destination tile **[!DNL AAC API 1P Onboarding]**.

   1. Set [!DNL Identifier Settings] to **[!DNL Ramp ID]** only.

      ![Identifier settings](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Optional) If you want to still receive cookie-based identifiers, create a second [!DNL AAC API 1P Onboarding] destination tile with “[!DNL Cookies],” "[!DNL IDFA],” and “[!DNL AAID]” selected.

   1. Verify in your audience library (which is available when you create or edit an audience from [!UICONTROL Audiences] > [!UICONTROL All Audiences] or within placement settings) that the entire segment count was imported.

>[!MORELIKETHIS]
>
>* [About Activating Authenticated Segments from Audience Sources](source-about.md)
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
