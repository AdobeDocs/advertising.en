---
title: Prerequisites and Key Information for Implementing [!DNL Analytics for Advertising]
description: Prerequisites and Key Information for Implementing [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
---
# Prerequisites and Key Information for Implementing [!DNL Analytics for Advertising]

*Advertisers with Advertising DSP and [!DNL Advertising Search]*

Review the following information before you integrate Adobe Advertising with Adobe Analytics.

## Requirements for Reporting Adobe Advertising Data in [!DNL Analytics]

* Either of the following:
  * Adobe Experience Platform Web SDK: `alloy.js`
  * Experience Cloud Identity Service: `visitorAPI.js` version 2.0 or higher
* Any version of Adobe Analytics (including [!DNL Prime], [!DNL Premium], or [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` version 2.1 or higher

>[!TIP]
>
>To improve data fidelity, use the most recent version of each library.

## Requirements for Sharing Analytics Segments with Adobe Advertising

* Experience Cloud Identity Service: `visitorAPI.js` version 2.1 or higher
* Adobe Analytics: `appMeasurement.js` version 1.8 or higher

## Requirements for Reporting [!DNL Analytics] Data in Adobe Advertising

Provide the Adobe Advertising implementation team with the following:

* The [!DNL Analytics] report suite ID that will be used for reporting on paid media activity and for feeding site activity for optimization and reporting in Adobe Advertising
* The company's Experience Cloud Organization ID (Org ID).

You can find both of these IDs on the [Summary tab of the Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Experience Cloud Debugger Summary screen](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Data in Adobe Advertising {#lookback-a4adc}

Because [!DNL Analytics] data is sent to Adobe Advertising for reporting and optimization, the data is subject to the attribution rules, including the impression and click lookback windows, that are configured for the advertiser in Adobe Advertising.

![advertiser-level lookback window settings in Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising attribution click lookback window: The number of days after the first click occurs in which the click can be attributed to a conversion. By default, this value is 60 days; the maximum is 90 days  
* Adobe Advertising attribution impression lookback window: The number of days after an ad impression occurs in which the impression can be attributed to a conversion. By default, this value is 14 days; the maximum is 30 days

    >[!NOTE]
    >
    > The impression lookback window is specific to Adobe Advertising, not [!DNL Analytics for Advertising], reporting.

The [!DNL Analytics for Advertising] JavaScript uses these settings to determine how far back to consider a view-through entry or click-through entry to the site as valid. For more information about how view-throughs and click-throughs are determined, see "[Adobe Advertising IDs Used by Analytics](ids.md)."

## Adobe Advertising Data in [!DNL Analytics]

[!DNL Analytics] sets Adobe Advertising IDs (AMO IDs) within the Analytics hit, subject to the advertiser's eVar persistence setting, which applies to both click-throughs and view-throughs. The persistence setting is configured on the Adobe Advertising back end, and your Adobe Account Team can change it.

* [!DNL Analytics for Advertising] eVar expiration: 60 days by default for AMO IDs

>[!NOTE]
>
>To segment data for a different timeframe, you can [set up custom segments](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) with different lookback windows within Analysis Workspace.

## Supported Ad Environments

* Search
* Display
* Video
* Online Video
* Native

Contact your Adobe Account Team for the latest supported ad environments in each channel.  

## Things to Know Before You Implement

* The Adobe Advertising implementation team will set up the integration.

* No additional costs are billed for this integration, nor do server calls result in additional [!DNL Analytics] or Adobe Advertising fees.

* [!DNL Analytics for Advertising] is ad server-agnostic: a view-through or click-through may occur from any ad server, and the proper IDs are generated upon site entry.

* The integration passes only [!DNL Analytics] standard and custom events to Adobe Advertising for bid optimization of subsequent paid media and advertising efforts. It doesn't pass [!DNL Analytics] segments, calculated metrics, and eVars to Adobe Advertising for bid optimization.

* Adobe Advertising creates persistent IDs within [!DNL Analytics] based on the last advertisement clicked or viewed before the user enters the site, based on the [click and view-through lookback windows](#lookback-a4adc) configured in Adobe Advertising. If a site visitor were to have both types of site entry interactions within their profile, and the click is within the lookback period, then the visitor's click-through ID would override the view-through ID for site reporting.

* [!DNL Analytics for Advertising] conversion tracking in Adobe Analytics uses a configurable tracking lookback window (60 days by default). Adobe Advertising reports reflect site conversions and engagement through the end of this tracking lookback window.

* All ad types are supported. However, not all ad environments are supported.

    For example, connected TV (CTV) ads aren't tracked because no clicks occur in CTV and no conversions can occur on the same device. However, if the ad is viewed within a desktop environment, then some view-through site entry data may be tracked.

* [!DNL Analytics] conversions are currently tracked and attributed only to a visitor on the same device.

* [!DNL Analytics for Advertising] doesn't support in-app view-through conversions.

* View-through tracking isn't supported for advertisers using a server-side forwarding implementation of [!DNL Analytics].

### Supplemental ID

Once the Experience Cloud Identity Service is implemented for a site, hits that contain data from [!DNL Analytics] or Adobe Advertising contain a supplemental ID.

Example: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

For accurate data integration, all Adobe Advertising calls used by an [!DNL Analytics for Advertising] activity to deliver content or record the goal metric must have a corresponding [!DNL Analytics] hit that shares the same supplemental ID.

When you're troubleshooting in [!DNL Analytics], be sure to confirm that the supplemental ID is present for [!DNL Analytics] hits. In the [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), you can see this ID in the Adobe Advertising tab as the `sdid` parameter.

>[!NOTE]
>
> This implementation works similarly to the [!DNL Analytics for Target] integration.

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript Code for Analytics for Advertising](/help/integrations/analytics/javascript.md)
