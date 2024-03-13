---
title: Activate Authenticated Segments from Universal ID partners
description: Learn about activating authenticated audiences through a universal ID solution.
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
---
# Activate Authenticated Segments from Universal ID partners 

<!-- Some of this is workflow for Adobe RT CDP, and some is about manually sending segments from LiveRamp (and Unified ID2.0?). Shouldn't this be a fourth workflow:  "Workflow for manually importing LiveRamp and (and Unified ID2.0?) segments to DSP" ??? -->

To activate authenticated audiences through a universal ID solution within Advertising DSP, your segments must be translated into universal IDs that are recognizable in a biddable environment. You can accomplish this by either:

* Leveraging the DSP integration with the [!DNL Adobe Real-Time Customer Data Platform (CDP)] and the universal ID partner retrieval API (either the [!DNL Adobe-LiveRamp Retrieval API] or the <!-- What about Unified ID2.0? -->).

* Manually sending authenticated segments to DSP from the universal ID partner (using either the [!DNL LiveRamp] [!DNL Connect] dashboard or the <!-- What about Unified ID2.0? -->). 

## Pre-Requisites: Configure Universal ID Settings in DSP

<!-- This doesn't apply to ActionIQ and Tealium sources, but only to RT CDP sources and manually imported segments? -->

1. For either option, contact `adcloud-support@adobe.com` to enable the following settings in DSP, which will allow you to target authenticated segments in DSP campaigns once [all steps in the activation workflow are completed](source-adobe-rtcdp.md):

    * The account-level “[!UICONTROL LiveRamp segments]” option. <!-- ??? -->

    * *[!DNL LiveRamp]* *[!DNL RampID]* campaign configuration before you begin sharing segments from [!DNL Real-Time CDP]. <!-- ??? And this isn't for RT-CDP customers after all? -->

## Manually Send Authenticated Segments to DSP

*Users manually sharing authenticated segments from a universal ID partner only*

### Manually Send Segments from [!DNL LiveRamp]

Complete the following steps in the [!DNL LiveRamp] [!DNL Connect] dashboard:

1. Activate the destination tile **[!DNL AAC API 1P Onboarding]**.

1. Set [!DNL Identifier Settings] to **[!DNL Ramp ID]** only.

   ![Identifier settings](/help/dsp/assets/liveramp-tile-settings.png)

1. (Optional) If you want to still receive cookie-based identifiers, create a second [!DNL AAC API 1P Onboarding] destination tile with “[!DNL Cookies],” "[!DNL IDFA],” and “[!DNL AAID]” selected.

### Manually Send Segments from [!DNL Unified ID2.0]

Complete the following steps in <!-- ??? -->

>[!MORELIKETHIS]
>
>* [About Activating Authenticated Segments from Audience Sources](source-about.md)
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
