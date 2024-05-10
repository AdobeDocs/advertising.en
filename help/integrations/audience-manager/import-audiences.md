---
title: Import Adobe Audience Manager Segments for Ad Targeting
description: Learn how to import your [!DNL Adobe] audiences into Advertising DSP and Search using Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
---
# Import Adobe Audience Manager Segments for Ad Targeting

Advertising DSP and [!DNL Advertising Search, Social, & Commerce] can each pull in metadata, hierarchy data, and unique audience data for all of an advertiser's or agency's [!DNL Adobe] audiences<!-- segments or audiences? Standardize terms per AAM's docs -->. This includes data for:

* Adobe Audience Manager segments

* Adobe Analytics segments that are published to Adobe Experience Cloud

* Segments that are created using the Adobe Experience Cloud [!DNL Audience Library]

* Segments that are created in Adobe Experience Platform and sent to Adobe Advertising via Audience Manager

To access [!DNL Adobe] audiences in DSP or [!DNL Creative], you must import the audiences into DSP. To access [!DNL Adobe] audiences in [!DNL Search, Social, & Commerce], you must import the audiences into [!DNL Search, Social, & Commerce].

## Prerequisites

* The advertiser must implement [the [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) version 2.0 or higher. The [!DNL Identity Service] provides a universal, persistent ID that identifies your visitors across all solutions in Experience Cloud.

  Implementation includes adding the [!DNL Identity service] code to each webpage on the advertiser's sites.

* The organization must be [enabled for Experience Cloud services](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) and have an Experience Cloud [!DNL Organization ID] (formerly called [!DNL IMS org ID]).

  The [!UICONTROL Organization ID] allows organizations with multiple Adobe Experience Cloud products to share data among some of the products.

* (Advertisers with [!DNL Analytics]) The advertiser must [implement [!DNL Analytics] using `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) version 1.6.4 or higher.

* The advertiser's website visitors don't include a high volume of [!DNL Apple Safari] users.

* (Recommended when the advertiser uses both Audience Manager and [!DNL Analytics]) To reduce calls to each webpage, remove existing Audience Manager [!DNL Data Integration Library] code for data collection and enable server-side forwarding for each [!DNL Analytics] report suite instead. For more information, see "[Server-side forwarding overview](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* (Recommended) For higher match rates, send only first-party website data to Adobe Advertising. If the advertiser bundles third-party data or offline data from a customer relationship management system, data leakage may reduce match rates. 

## Import Audience Manager Audiences to DSP

### Steps to Import Audiences to DSP

The [!DNL Adobe] account and data operations teams perform the following steps.

1. The Adobe Account Team should configure the advertiser-level setting "[!UICONTROL Adobe Analytics Cloud]."

1. The Adobe Account Team should submit a request<!-- Submit a request as a JIRA task? --> to the data operations team<!-- implementation team? --> to import the organization's Audience Manager segments using the Advertising DSP native API integration.

### What Changes Result in Audience Manager?

The API automatically:

* Creates two DSP destinations in Audience Manager:

  * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

  * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* Maps the two destinations to all Audience Manager segments, allowing Audience Manager to share the segments with the DSP advertiser account that's associated with the same Experience Cloud [!DNL Organization ID] used for Audience Manager. <!-- Verify -->

  The organization can optionally remove unneeded segments from the destinations within Audience Manager.

* Adds the following exchange cookie-sync pixel to the organization's Audience Manager container to improve the reach of customer campaigns:

  * Adobe AdCloud: 411 (This comes standard and automatically as part of [!DNL Identity Service] version 2.0. Organizations with [!DNL Identity Service] versions below 2.0 should add this pixel to their Audience Manager container.

## Import Audience Manager Audiences to [!DNL Search, Social, & Commerce]

### Steps to Import Audiences to [!DNL Search, Social, & Commerce]

[!DNL Adobe] personnel perform most or all of the following steps.

1. The Adobe Account Team should submit a request to the data operations team to set up an integration between [!DNL Search, Social, & Commerce] and Audience Manager. Include the names of the Audience Manager segments that you want to export to [!DNL Search, Social, & Commerce]. 

1. Within Audience Manager, configure destinations for [!DNL Search, Social, & Commerce]:

   1. Create two new destinations: `[!UICONTROL Adobe Media Optimizer (HTTP)]` and `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

       [!DNL Media Optimizer] is a former name for [!DNL Search, Social, & Commerce].

   1. Specify the segments for each of the destinations.

       With the [!UICONTROL Automatically map all current and future segments] option, all segments are mapped and synced daily.

       The [!UICONTROL Manually map segments] option allows you to manually map the segments to sync with the batch destination (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). No segments need to be manually mapped to the HTTP destination.

1. Within [!DNL Search, Social, & Commerce], either the [!DNL Search, Social, & Commerce] implementation team or a user with the direct access client manager role should initiate the import from [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

    You must enter the organization's Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID]). The ID must be the same as the one used for the organization's Audience Manager account.

### What Changes Result in Audience Manager?

Two [!DNL Search, Social, & Commerce] destinations become available for the organization in Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## Data Synchronization

The initial import takes about 24 hours. After the initial import, data is synced in real time, with a one- to two- second delay.

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.eversttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].

![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Adobe Advertising display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search, Social, & Commerce]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## Where to Find Your Synced Segments

### In DSP

In DSP, segment names are organized by the Audience Manager taxonomy and available with the corresponding segment membership counts in:

* [Placement settings](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): On the [!UICONTROL Adobe Segments] tab of the [!UICONTROL Audience Targeting] section.

* In [audience settings](/help/dsp/audiences/audience-settings.md): On the [!UICONTROL Adobe Segments] tab.

### In Advertising Creative

In [!DNL Creative], the segments are available in the experience settings for target nodes.

### In [!DNL Advertising Search, Social, & Commerce]

In [!DNL Search, Social, & Commerce], the segments are available when you create a [!DNL Google] audience using the [!UICONTROL Data Source] "[!UICONTROL Adobe Audience]" from [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

For each [!DNL Google] audience that you create, [!DNL Google] supplies the audience size.

>[!MORELIKETHIS]
>
>* [Adobe Advertising Integrations with Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
