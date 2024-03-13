---
title: Activate Authenticated Segments from Universal ID partners
description: Learn about activating authenticated audiences through a universal ID solution.
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
---
# Activate Authenticated Segments from Universal ID partners

<!-- Title:  Manually Activate Authenticated Segments from Universal ID partners ??? If yes, then change here, update filename, create a redirect from the old page to the new one, and update all x-refs. -->

<!-- Some of this is workflow for Adobe RT CDP, and some is about manually sending segments from LiveRamp (and Unified ID2.0?). Shouldn't this be a fourth workflow:  "Workflow for manually importing LiveRamp and (and Unified ID2.0?) segments to DSP" ??? -->

You can manually send authenticated segments to DSP from a supported universal ID partner, using either the [!DNL LiveRamp] [!DNL Connect] dashboard or the <!-- What about Unified ID2.0? -->). 

## Pre-Requisites: Configure Universal ID Settings in DSP

<!-- Are there any pre-requisite settings for either LiveRamp OR UID2???

1. Contact `adcloud-support@adobe.com` to enable the account-level “[!UICONTROL LiveRamp segments]” option, which will allow you to target authenticated segments in DSP campaigns once all steps in the activation workflow are completed.

-->

## Manually Send Authenticated Segments to DSP

<!-- Remove H2 and bump other headers up a level if no pre-requisites -->

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
