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

## Summary reporting

+++ No summary reporting data is available in Customer Journey Analytics for Advertising DSP or Advertising Search, Social, & Commerce.

Verify the following:

* The feed from Adobe Advertising to Customer Journey Analytics is enabled. Check with your Adobe Account Team.
* 
* Your Adobe Advertising dimension/classification/lookup dataset and your summary dataset are included in your Customer Journey Analytics connection.
* 
* Your Adobe Advertising dimensions and summary metrics are included in your Customer Journey Analytics data view.
* 
* Customer Journey Analytics Workspace is referencing the correct data view.

If you verify all of the above settings but you still don't see summary data, then open a support ticket for your organization at [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support).
.

+++

+++ Summary reporting data is available in Customer Journey Analytics for Advertiser 1 but not Advertiser 2.


Verify that the feed from Adobe Advertising to Customer Journey Analytics is enabled for Advertiser 2. Check with your Adobe Account Team.

If the feed is enabled for an advertiser but you still don't see summary data, then open a support ticket for your organization at [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support).
.

+++

+++

+++ (Search, Social, & Commerce users) Summary reporting data is available in Customer Journey Analytics for one [!DNL Google Ads], [!DNL Meta Ads], or [!DNL Microsoft Advertising] account but not for another account.


Verify that the feed from Adobe Advertising to Customer Journey Analytics is enabled for the specific ad network account. Check with your Adobe Account Team.

If the feed is enabled for an account but you still don't see summary data, then open a support ticket for your organization at [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Include the [!UICONTROL Account ID] for the ad network account.
.

+++

+++ Summary reporting data in Customer Journey Analytics Workspace is different than the data in Advertising DSP or Advertising Search, Social, & Commerce, or summary data is missing for some campaigns and campaigns entities.

Verify the following:

* You're using the same date ranges in both [!DNL Workspace] and the Adobe Advertising report.

* Any filters and segments that are applied in [!DNL Workspace] and the Adobe Advertising report aren't causing differences in data.

If you're sure of a data discrepancy, then open a support ticket for your organization at [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Include the [!UICONTROL Account ID] for the ad network account.
. Include screenshots and spreadsheets to show evidence of the discrepancy. Your Adobe Account Team can retroactively fix the data feed to resolve the discrepancy if needed.

+++

## Event-level reporting

+++ Scenario: Conversion data (such as `Page Views`) isn't available for a reporting dimension (such as `Campaign`) in CJA Customer Journey Analytics Workspace.

Verify the following, starting with the items with the fewest barriers:

* The applicable conversion metrics are web/online events, which Adobe Advertising can attribute to dimensions.

* You're using the correct data view.

* Adobe Advertising is tracking clickthroughs and viewthroughs on the applicable site. <!-- Link to validation instructions in the user guide -->

* In the Customer Journey Analytics connection for the classifications dataset, the values for the [!DNL Key] and [!DNL Matching Key] settings are correct: [!DNL Key]: `Tracking Code` (_customername.adLens2.trackingCode), [!DNL Matching Key]: `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)

* The [!DNL Adobe Advertising] service is added to the Adobe Experience Platform datastream, the mapped schema for the datastream is `XDM ExperienceEvent Schema`, and the field group `Adobe Advertising Cloud ExperienceEvent Full Extension` is added to the schema.

* The Adobe Advertising settings are configured correctly in the WebSDK Extension and published.

If you verify all of the above settings but you still don't see conversion data, then open a support ticket for your organization at [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Include the [!UICONTROL Account ID] for the ad network account.
.

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
