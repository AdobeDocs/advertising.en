---
title: Activate Authenticated Segments from Universal ID partners
description: Learn about activating authenticated audiences through a universal ID solution.
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
---
# Activate Authenticated Segments from Universal ID partners 

<!-- How much of this intro and Tasks sections are applicable to other ID partners? Re-word/reorganize accordingly. -->

To activate authenticated audiences through a universal ID solution within Advertising DSP, your segments must be translated into [!DNL RampIDs], which are recognizable in a biddable environment. You can accomplish this by either:

* Leveraging the DSP integration with the [!DNL Adobe Real-Time Customer Data Platform (CDP)] and the [!DNL Adobe-LiveRamp Retrieval API].

* Manually sending authenticated segments to DSP from the [!DNL LiveRamp] [!DNL Connect] dashboard.

## Tasks

1. For either option, contact `adcloud-support@adobe.com` to enable the following settings in DSP, which will allow you to target authenticated segments in DSP campaigns once [all steps in the activation workflow are completed](source-adobe-rtcdp.md):

    * The account-level “[!UICONTROL LiveRamp segments]” option

    * The campaign-level "[!UICONTROL Cross Device Graph]" setting for *[!UICONTROL People]* and the "[!UICONTROL Device Graph]" setting for *[!DNL LiveRamp]* before you begin sharing segments from [!DNL Real-Time CDP]

1. (Users manually sharing authenticated segments from [!DNL LiveRamp]) Complete the following steps in the [!DNL LiveRamp] [!DNL Connect] dashboard:

    1. Activate the destination tile **[!DNL AAC API 1P Onboarding]**.

    1. Set [!DNL Identifier Settings] to **[!DNL Ramp ID]** only.

       ![Identifier settings](/help/dsp/assets/liveramp-tile-settings.png)

    1. (Optional) If you want to still receive cookie-based identifiers, create a second [!DNL AAC API 1P Onboarding] destination tile with “[!DNL Cookies],” "[!DNL IDFA],” and “[!DNL AAID]” selected.

## Best Practices for Testing and Data Validation

* **Target universal ID-based segments and cookie-based segments in separate campaigns.**

  * Campaign settings allow for only one identifier to be prioritized.

  * Currently, [!DNL RampIDs] aren't retrievable during on-site events. This means that certain custom goals, such as Lowest CPA and ROAS, aren't available with the use of authenticated segments. Use cookie-based segments only if you have a restrictive performance KPI.<!-- get update on this, and if it applies to other ID types too -->

* **Create one placement in both the universal ID-based and cookie-based campaigns.**

  * Target the segments that are shared from the universal ID partner using the standard segment activation process.

  * Work with your Adobe Advertising support team to validate proper data distribution.

>[!MORELIKETHIS]
>
>* [About Activating Authenticated Segments from Audience Sources](source-about.md)
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
