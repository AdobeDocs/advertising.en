---
title: About Audience Management in Advertising DSP
description: Learn about audience management features.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
---
# About Audience Management in Advertising DSP

In DSP, you can create and manage audience segments and audience sets, which you can use as targets for your placements:

* Collect your own first-party audience data by creating and implementing DSP segments. You can later retarget users in the segment with ads or prevent users in the segment from receiving ads. You can create the following types of segments:

   * [Custom segments](/help/dsp/audiences/custom-segment-create.md) to track a) users exposed to ads from desktop and mobile devices and b) users who visit specific webpages. The tracking tag can track either cookie-based users or users associated with ID5 universal IDs.

   * [CCPA opt-out-of-sale segments](/help/dsp/audiences/ccpa-opt-out-segment-create.md) to track the users IDs from consumer opt-out-of-sale requests on your website, per the California Consumer Privacy Act (CCPA). You can retrieve monthly reports of the user IDs from opt-out-of-sale requests.

      For more information about Adobe Advertising support for CCPA opt-out-of-sale requests, see [Adobe Advertising Support for the California Consumer Privacy Act: Consumer Opt-out Support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (Beta feature) [Obtain and use universal IDs for cookieless targeting](/help/dsp/audiences/universal-ids.md):

  * Manually send your authenticated [!DNL LiveRamp] [!DNL RampID] segments directly to DSP.

  * Allow DSP to import first-party segments from your customer data platform and translate them to supported universal ID types.
  
  * Include third-party segments that contain universal IDs in your placement targets without any extra steps.

* Create an audience library of [reusable audiences](/help/dsp/audiences/reusable-audience-create.md). Saved audiences are composed of any of your available audience segments and any of your other saved audiences. Any changes you make to a saved audience are automatically applied to all placements that target or exclude the audience and to all other audiences that include the saved audience.

   Saved audiences allow media planners to group audiences as needed, by including and excluding multiple segments using complex Boolean logic. The size of each individual segment and the total audience size are indicated as you build an audience. Campaign executioners can then simply select one or more saved audiences as placement targets rather than manually configure audience targets for each placement.

Additional audience types are also available for placement targeting.

## Importing First-party and Third-party Data Segments

You have many options to import first-party and third-party data segments into DSP, using the DSP user interface and/or through custom import services.

* DSP can pull in your Adobe Audience Manager and other [!DNL Adobe] audiences for targeting. For prerequisites and instructions, see "[Import Adobe Audience Manager Segments for Ad Targeting](/help/integrations/audience-manager/import-audiences.md).

* DSP can translate first-party data segments from supported customer data platforms to segments with universal IDs using the [Sources feature](/help/dsp/audiences/sources/source-about.md). You can also [manually send your authenticated [!DNL LiveRamp] [!DNL RampID] segments directly to DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP can import your other first-party data segments directly from your data management platform (DMP) and provide them to any set of advertisers, as needed.

* DSP can import custom third-party segments, including complex combinations of third-party segments. You can provide the segments to any set of advertisers, as needed.

Contact your Adobe Account Team for more information.

## Audiences Available as Placement Targets

You can target your placements to all of the following types of audiences.

* All user-created audience sets that were saved in DSP.

* All user-created audience segments that were created in DSP:

   * Custom segments for users who visited specific webpages and users exposed to impressions of specific ads.
   
     No fees are incurred for impressions delivered to universal IDs.

   * CCPA opt-out-of-sale audience segments for users who submitted opt-out-of-sale requests on your website, per the California Consumer Privacy Act (CCPA).

* All of your imported first-party data segments, including segments that were translated to universal IDs.

  Additional fees are charged for impressions delivered to universal IDs. See "[About First-Party Audience Sources](/help/dsp/audiences/sources/source-about.md)" for rates.

* All of your imported custom third-party data segments.

* (Placements targeting the U.S. only) [All third-party data segments available to DSP customers from over 30 providers](/help/dsp/audiences/third-party-data-providers.md), including [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast], and many more.

   You can target specific segments, which target users based on audience data (for example, users with specific demographics, interests or intents, and/or behavioral profiles). You can browse by data provider and category, search for segments by name or segment ID, or filter the results by data provider, total segment size, web browser count, or devices count.

   Third-party segments incur additional fees, which are indicated next to each segment name.

* (Advertisers with Adobe Experience Platform and [!DNL Real-Time CDP], Adobe Audience Manager, or Adobe Analytics who use Adobe Advertising JavaScript conversion tags only) All of your available first-, second-, or third-party audience segments created in [!DNL Real-Time CDP], created in Audience Manager, or published to Adobe Experience Cloud from Audience Manager or [!DNL Analytics].

   Pricing for the use of the segments is pre-negotiated and isn't visible in DSP.

   Segments from [!DNL Analytics] are available about an hour after you create or publish them as Experience Cloud audiences. Segments coming directly from Audience Manager or [!DNL Real-Time CDP] are available within 24 hours after you share them.

   >[!NOTE]
   >
   >See the documentation for [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html), and [the [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) for information about setting up and collecting data for segments in those solutions.

## Audience Size Data

In Audiences > All Audiences and in the Audience Targeting section of placement settings, you can see detailed audience size data:

* The total and active deduplicated audience size across all selected segments and saved audiences is displayed, and you can view details by device type (browser, mobile, or connected TV).

   ![the combined audience size](/help/dsp/assets/audience-size.png)

* For individual segments, the total audience size and CPM (when applicable) are displayed next to the segment name.

   ![the individual segment size](/help/dsp/assets/audience-size-segment.png)

* You can view more details about an individual segment or saved audience, including the size by browser, mobile, connected TV, and universal ID type partner. For saved audiences, the total size is the deduplicated total.

   ![the individual segment or saved audience details](/help/dsp/assets/audience-size-segment-details.png)

## The Audiences Views

### The All Audiences View

In the [!UICONTROL All Audiences] view, or Audience Library, you can save and manage reusable audiences, which include groups of audience segments and even other saved audiences. You can use audiences as targets for multiple placements. The number of placements in which each audience is used is indicated next to the placement name.

You can edit, clone, delete, export, or share any audience.

### The Segments View

In the [!UICONTROL Segments] view, all users can create additional custom segments.

The [!UICONTROL Segments] view also lists the following segment types:

* All user-created custom segments available to the user.

   You can view tracking tags for any of the custom segments you created, and share those segments with other users. You can also edit or delete the custom segments you created.

   You can't edit or share custom segments that other users have shared with you.

* All first-party segments imported as-is that are available to the user.

   You can't edit or share first-party segments that were shared with you. Contact your Adobe Account Team if you need to share first-party segments with additional users.

* All custom third-party segments available to the user.

   You can't edit or share third-party segments that were shared with you. Contact your Adobe Account Team if you need to share third-party segments with additional users.

### The Sources View

In the [!UICONTROL Sources] view, you can configure sources for first-party segments in supported customer data platforms that you want to convert to segments containing specified universal ID types. The source settings include an auto-generated source key, which you'll provide to your customer data platform to establish the connection.

For more information about the supported customer data platforms, supported universal ID types, and the workflows to set up connections to each customer data platform, see "[About Sources](/help/dsp/audiences/sources/source-about.md)."

The translated segments are available to include in reusable audiences and in placement settings for cookieless targeting.

>[!MORELIKETHIS]
>
>* [Support for Activating Universal IDs](/help/dsp/audiences/universal-ids.md)
>* [Create a Reusable Audience](reusable-audience-create.md)
>* [Create and Implement a Custom Segment](custom-segment-create.md)
>* [Create and Implement a [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [About First-Party Audience Sources](/help/dsp/audiences/sources/source-about.md)
>* [Manually Import Authenticated Segments from [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Available Third-party Data Providers](third-party-data-providers.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
