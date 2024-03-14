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

<!--

1. Configure Universal ID settings in DSP

<!-- Are there any pre-requisite settings for either LiveRamp OR UID2???

1. Contact `adcloud-support@adobe.com` to enable the account-level “[!UICONTROL LiveRamp segments]” option, which will allow you to target authenticated segments in DSP campaigns once all steps in the activation workflow are completed.
-->

Complete the following steps in the [!DNL Connect] dashboard:

1. Activate the destination tile **[!DNL AAC API 1P Onboarding]**.

1. Set [!DNL Identifier Settings] to **[!DNL Ramp ID]** only.

   ![Identifier settings](/help/dsp/assets/liveramp-tile-settings.png)

1. (Optional) If you want to still receive cookie-based identifiers, create a second [!DNL AAC API 1P Onboarding] destination tile with “[!DNL Cookies],” "[!DNL IDFA],” and “[!DNL AAID]” selected.

>[!MORELIKETHIS]
>
>* [About Activating Authenticated Segments from Audience Sources](source-about.md)
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
