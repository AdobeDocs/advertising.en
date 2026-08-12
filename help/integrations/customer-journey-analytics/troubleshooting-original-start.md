---
title: Troubleshooting Adobe Advertising data in Customer Journey Analytics
description: Learn how to troubleshoot and resolve issues with Adobe Advertising data in Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
---
# Troubleshooting Adobe Advertising data in Customer Journey Analytics

The following are potential issues and their causes.




## Installation and setup issues


### WebSDK extension doesn't initialize

Symptoms:

* No alloy() calls are visible in the browser network tab
* Console error: alloy is not defined
* No interact or collect requests to edge.adobedc.net

| Cause | Fix |
| ----- | --- |
| Library not published or in draft state | Go to [Publishing Flow](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) and make sure the library that contains the WebSDK extension is in the approved/published state. |
| Embed code missing or wrong environment | Verify that the [!DNL Tags] embed code on the webpage references the correct environment (Dev/Stage/Prod). Look for the environment in the `<head>` tag for the `//assets.adobedtm.com/...` script tag. |
| Async vs. synchronous load conflict | Make sure that only one [!DNL Tags] embed code is present per webpage. Duplicate embed codes cause race conditions. |
| Content security policy (CSP) blocking | Add `edge.adobedc.net` `and assets.adobedtm.com` to your CSP `connect-src` and `script-src` directives. |

### Datastream not configured or misconfigured

Symptoms:

* Requests reach the edge but return 400 or 500 errors
* No data appears in Adobe Analytics or Adobe Advertising reports<!-- It's not useful to organize this info by cause, not symptom -->
* Error in network response: "datastream not found"

| Cause | Fix |
| The datastream ID for the tag property is missing or incorrect. | <ol><li>In [!DNL Tags], open the [datastream configuration settings](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) for your tag property.</li><li>Confirm that the [!UICONTROL Datastream] field points to the correct datastream for each environment (development, staging, and production), as well as to the correct scema and dataset.<br><br>Each environment should have its own datastream unless you explicitly share one datastream across all three environments.</li></ol> |
| Datastream services aren't enabled for the tag property. | [Open the datastream settings](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) and make sure that the following services are enabled:<ul><li>Adobe Advertising (for conversion/audience sync)</li><li>Adobe Experience Platform (for profile ingestion)</li></ul>
| Sandbox mismatch |  Make sure the datastream belongs to the same Adobe Experience Platform sandbox as your schema and dataset. A common mistake is creating a datastream in the production sandbox but pointing schemas to the development sandbox. |

## [!UICONTROL Advertising] extension setup issues

Symptoms:

* No view-through or click-through conversions are recorded for the webpage.

  To verify if conversions are recorded:

  1. Open the webpage with `ef_id=test&s_kwcid=test` appended to the URL.
  1. Open your browser's code inspection tool (often called [!DNL Inspect]), open the [!DNL Network] tab, and look for an interact call for event_type="advertising.enrichment_ct" from Adobe Experience Platform.
  1. In the Data Collection interface, [open the schema definition](https://experienceleague.adobe.com/en/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas) for the website data you want to collect and confirm that `xdm->_experience->adcloud->conversionDetails->trackingCode` and `trackingIdentities` contain `ef_id` and `s_kwcid`.

* `_experience.adcloud` is missing from the Experience Data Model (XDM) payload for click-throughs.

* Conversions are confirmed in a debugger tool but don't appear in Adobe Advertising reports

| Cause | Fix |
| The `Adobe Advertising` service isn't enabled for the datastream | <ol><li>In [!DNL Tags], open the [datastream configuration settings](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) for your tag property.</li><li>Enable the following services, and save the settings:<ul><li>Adobe Advertising (for conversion/audience sync)</li><li>Adobe Experience Platform (for profile ingestion)</li></ul></ol> |
| The `Adobe Advertising` component isn't enabled for the [!UICONTROL WebSDK] extension | The `Adobe Advertising` component within the WebSDK extension is disabled by default and must be explicitly enabled before any tracking for Adobe Advertising click-throughs or view-throughs is functional, regardless of how the XDM schema or rules are configured.<ol><li>>In [!DNL Tags], open the [build options for the property in the Adobe Experience Platform Web SDK configuration settings](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/custom-build-components).</li><li>Enable the **Advertising** component, and save the settings.<li><li>Rebuild and republish the library.</li></ol> |
| ----- | --- |
| ----- | --- |
| ----- | --- |





| Cause | Fix |
| ----- | --- |
| ----- | --- |
| ----- | --- |
| ----- | --- |
| ----- | --- |

| Cause | Fix |
| ----- | --- |
| ----- | --- |
| ----- | --- |
| ----- | --- |
| ----- | --- |

| Cause | Fix |
| ----- | --- |
| ----- | --- |
| ----- | --- |
| ----- | --- |
| ----- | --- |


## Reporting issues

### Summary reporting

+++ No summary reporting data is available in Customer Journey Analytics for Advertising DSP or Advertising Search, Social, & Commerce.

Verify the following:

* Customer Journey Analytics Workspace is referencing the correct data view.

* The feed from Adobe Advertising to Customer Journey Analytics is enabled. Check with your Adobe Account Team.

* Your Adobe Advertising dimension/classification/lookup dataset and your summary dataset are included in your Customer Journey Analytics connection.
  
* Your Adobe Advertising dimensions and summary metrics are included in your Customer Journey Analytics data view.

If you verify all of the above settings but you still don't see summary data, then open a support ticket for your organization at [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support).

+++

+++ Summary reporting data is available in Customer Journey Analytics for Advertiser 1 but not Advertiser 2.

Verify the following:

* The feed from Adobe Advertising to Customer Journey Analytics is enabled for Advertiser 2. Check with your Adobe Account Team.

* The setting "[!UICONTROL Backfill all existing data]" is enabled for your three datasets (dimension/classification/lookup, summmary, and event metrics) in trics) in your Customer Journey Analytics connection..

If you verify all of the above conditions but you still don't see summary data, then open a support ticket for your organization at [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support).

+++

+++ (Search, Social, & Commerce users) Summary reporting data is available in Customer Journey Analytics for one [!DNL Google Ads], [!DNL Meta Ads], or [!DNL Microsoft Advertising] account but not for another account.

Verify that the feed from Adobe Advertising to Customer Journey Analytics is enabled for the specific ad network account. Check with your Adobe Account Team.

If the feed is enabled for an account but you still don't see summary data, then open a support ticket for your organization at [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Include the [!UICONTROL Account ID] for the ad network account.

+++

+++ Summary reporting data in Customer Journey Analytics Workspace is different than the data in Advertising DSP or Advertising Search, Social, & Commerce, or summary data is missing for some campaigns and campaigns entities.

Verify the following:

* You're using the same date ranges in both [!DNL Workspace] and the Adobe Advertising report.

* Any filters and segments that are applied in [!DNL Workspace] and the Adobe Advertising report aren't causing differences in data.

* The [!UICONTROL Time Zone] for your Customer Journey Analytics data view matches the [[!UICONTROL Default Timezone] for your Advertising DSP account](/help/dsp/admin/user-own-profile-edit.md).

* The setting "[!UICONTROL Backfill all existing data]" is enabled for your three datasets (dimension/classification/lookup, summmary, and event metrics) in trics) in your Customer Journey Analytics connection..

If you're sure of a data discrepancy, then open a support ticket for your organization at [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Include the [!UICONTROL Account ID] for the ad network account.
. Include screenshots and spreadsheets to show evidence of the discrepancy. Your Adobe Account Team can retroactively fix the data feed to resolve the discrepancy if needed.

+++

### Event-level reporting

+++ Conversion data (such as `Page Views`) isn't available for a reporting dimension (such as `Campaign`) in CJA Customer Journey Analytics Workspace.

Verify the following, starting with the items with the fewest barriers to verification:

* You're using the correct data view.

* The applicable conversion metrics are web/online events, which Adobe Advertising can attribute to dimensions.

* Adobe Advertising is tracking clickthroughs and viewthroughs on the applicable site. <!-- Link to validation instructions in the user guide -->

* In the Customer Journey Analytics connection for the classifications dataset, the values for the [!DNL Key] and [!DNL Matching Key] settings are correct: [!DNL Key]: `Tracking Code` (_customername.adLens2.trackingCode), [!DNL Matching Key]: `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)

* The [!DNL Adobe Advertising] service is added to the Adobe Experience Platform datastream, the mapped schema for the datastream is `XDM ExperienceEvent Schema`, and the field group `Adobe Advertising Cloud ExperienceEvent Full Extension` is added to the `XDM ExperienceEvent` schema.

* The Adobe Advertising settings are configured correctly in the WebSDK Extension and published.

If you verify all of the above settings but you still don't see conversion data, then open a support ticket for your organization at [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Include the [!UICONTROL Account ID] for the ad network account.

+++


<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

>[!MORELIKETHIS]
>
>* [Overview](overview.md)
>* [Adobe Advertising IDs used by [!DNL Customer Journey Analytics]](ids.md)
>* [Prerequisites](prerequisites.md)
>* [Set up data collection, data transfer, and reporting](set-up.md)
>* [Adobe Advertising metrics and dimensions in Customer Journey Analytics](advertising-data-in-cja.md)
>* (Adobe Analytics users) [Collect historical data for AMO IDs and EF IDs for use in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
