---
title: Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags
description: Learn why and how to add [!DNL Analytics for Advertising] macros to your [!DNL Flashtalking] ad tags
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
---
# Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

*Organizations without a direct partnership with [!DNL Flashtalking] only*

*Applicable to Advertising DSP only*

If you use ad tags from [!DNL Flashtalking] for your Advertising DSP ads, you must append tracking parameters to your landing page URLs. To use the Advertising DSP partnership with [!DNL Flashtalking], append Analytics for Advertising parameters to your landing page URLs. The parameters record AMO ID (`s_kwcid`) and `ef_id` query string parameters in the landing page URL, allowing Adobe Advertising to send click data for the ads to Adobe Analytics.

>[!NOTE]
>
>If your organization has a direct partnership with [!DNL Flashtalking], then this procedure isn't necessary for you. Instead, log in to your [!DNL Flashtalking] account and follow the [!DNL Flashtalking] support documentation to collect click data using data-pass macros at `https://support.flashtalking.com%2Fhc%2Fen-us%2Farticles%2F4409808166419-Accessing-Data-Pass-Macros`.

Use macros for [!DNL Flashtalking] display and video ads for the following types of [!DNL Analytics for Advertising] implementations:

* **Advertisers with the [!DNL Adobe] [!DNL Analytics for Advertising] JavaScript code implemented on their websites**: The JavaScript code already records the AMO ID (`s_kwcid`) and `ef_id` query string parameters. However, using macros extends tracking to include click-based conversions when third-party cookies aren't supported. The best practice is to add the macros in the following sections to your ad tags to capture additional click-through data that isn't captured through the JavaScript code.

  >[!NOTE]
  >
  >The JavaScript code is a solution for click tracking only while cookies are still available. Once cookies are discontinued, implementing the following macros will be necessary.

* **Advertisers whose websites don't use the [!DNL Analytics for Advertising] JavaScript code and instead rely on [!DNL Analytics] server-side forwarding for click-through data only** (without any view-through data): The following macros are required to report on-site click activity driven from ads you buy through Adobe Advertising.

## Display Ad Tags

Within the [!DNL Flashtalking] ad tag settings, append the following macro to the end of the click-through URL in the `Clicktag` field:

```
[ftqs:[AdobeAMO]]
```

If it's the first or only query string after the base URL, then separate it from the base URL with a `?`. If the base URL includes multiple query strings, then begin the first string with a `?` and each subsequent string with a `&`.

Examples:
  
`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Video Ad Tags

Within the [!DNL Flashtalking] ad tag settings, append the following macro to the end of the click-through URL in the `Clicktag` field:

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

If it's the first or only query string after the base URL, then separate it from the base URL with a `?`. If the base URL includes multiple query strings, then begin the first string with a `?` and each subsequent string with a `&`.

Examples:

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising IDs Used by [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md)

