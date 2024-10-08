---
title: Support for Activating Universal IDs
description: Learn about support to import your universal ID segments, create custom segments to track universal IDs, and convert other user identifiers in your first-party segments to universal IDs for cookieless targeting.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
---
# Support for Activating Universal IDs

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta feature*

DSP supports people-based, universal IDs for cookieless, single-device (not cross-device) targeting across digital formats supported by DSP.

* You can manually send your authenticated [[!DNL LiveRamp] [!DNL RampIDs]] directly to DSP using the [!DNL LiveRamp] [!DNL Connect] dashboard. See "[Manually Import Authenticated Segments from [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)."

* DSP can ingest your first-party segments comprised of hashed email IDs built within your customer data platform (CDP) and convert them to [!DNL LiveRamp] [!DNL RampIDs] and [!DNL Unified ID 2.0 (UID2.0)] IDs. For more information about the supported customer data platforms, the available features for each supported universal ID type, and the related workflows, see "[About First-Party Audience Sources](/help/dsp/audiences/sources/source-about.md)."

* You can create custom segments that track users associated with ID5 universal IDs who are exposed to ads from desktop and mobile devices and who visit specific webpages. ID5 uses a probabilistic model to assign an ID derived from various user signals and browser signals. For instructions, see "[Create and Implement a Custom Segment](/help/dsp/audiences/custom-segment-create.md)."

* Third-party segments from some vendors may automatically include universal IDs in addition to users tracked by cookies or device IDs. For example, segments from [!DNL Eyeota] may automatically include ID5 IDs, and segments from [!DNL Lotame] may include UID2.0 IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.

## Reporting by Universal ID Type

* **Custom reports:** Cost, impression, click, conversion, and frequency data by universal ID type is available in custom reports.

* **[!DNL Analytics] reports:** Advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) who have implemented all required steps can see view-through conversions by universal ID type in [!DNL Analytics].

  >[!IMPORTANT]
  >
  >For proper conversion attribution, make sure that the clickthrough URLs for your ads include both the [EF ID and the AMO ID](/help/integrations/analytics/ids.md).

* **Segment details:** For all segment types, the segment details include the audience size by universal ID type and by the device type tracked by cookies or device IDs.

## How to Target a Universal ID Audience in Your Placements

>[!NOTE]
>
>You can't change the targeted ID types in a live placement. If necessary, you can duplicate a live placement and change the targeted ID types in the new placement.

In a new, scheduled, or paused placement, do the following:

1. In the [!UICONTROL Geo-Targeting] section, specify the geographical areas to target. Each universal ID partner allows user targeting only in specific geographical areas, and only eligible ID types are available in the [!UICONTROL Targeting] settings.

1. In the [!UICONTROL Audience Targeting] section, do the following:

   1. In the [!UICONTROL Included Audiences] setting, select the segment for which user data was converted to universal IDs.

      You can include additional segments if you want.

   1. In the [!UICONTROL Targeting] settings:
  
      1. Select the universal ID type to target.
      
         The setting includes the options "[!UICONTROL Legacy IDs]" and "[!UICONTROL Universal ID]," which may include the sub-options "[!UICONTROL ID5]," "[!UICONTROL RampID]," and "[!UICONTROL Unified ID2.0]." The selected geographical targets determine the available sub-options.
         
         You can select both "[!UICONTROL Legacy IDs]" and "[!UICONTROL Universal ID]," but you can select only one type of universal ID per placement. When you select both legacy IDs and universal IDs, bidding preference is given to universal IDs.

      1. (If necessary) Accept the terms of service agreement for using universal IDs.
      
         Before you can convert data to a new ID type, a user in the DSP account must accept the terms of service agreement. The terms must be accepted only once per ID type, per account.

See "[Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)."

## Best Practices for Testing and Data Validation

Use the following best practices for [!DNL RampID]-based segments and ID5-based segments, for which Adobe Analytics measurement is available.

* About 24 hours after you activate a segment, check the converted ID count for the segment within [!UICONTROL Audiences] > [!UICONTROL All Audiences]. If the ID count is unexpected, then contact your Adobe Account Team.

  See "[Data Variances Between Email IDs and Universal IDs](#universal-ids-data-variances)" for more information about how the segment counts can vary.

* Don't change your existing packages and placements. However, if you don't have any incremental budget to test universal IDs, then reduce the original budgets to fund the tests.

* Copy your original packages and placements, adjust the budgets based on the size of the test, change the audiences to use [!DNL RampID]-based segments (for authenticated users) or ID5-based segments (for unauthenticated users), and verify that the new packages and placements spend their full budgets.

  * To compare the performance of universal ID-based segments with the performance of placements targeting other audience identifiers, such as cookies or mobile advertising IDs, create a campaign with a separate universal ID-based placement and a legacy ID-based placement.

    For a full retargeting test, target both RampIDs for authenticated users and ID5s for unauthenticated users.

    Getting the best performance shouldn't be the primary comparison. Instead, determine which IDs are scaling well, which might inform your optimization and budget allocations later. The long-term goal is to make up for lost impressions and site traffic when cookies are deprecated.

  * To compare total browser reach, target universal ID-based segments and legacy ID-based segments in the same placement. Use the same campaign settings as the previous use case, except that you don't need to split the campaign budget.
  
    Bidding preference is given to universal IDs, but legacy IDs receive bids when universal IDs aren't available. Make sure to compare reach in different browsers (including Chrome, Safari, and Mozilla).
 
    >[!NOTE]
    >
    >Frequency capping applies to an individual ID. When a user has multiple ID types, you might reach that user more than you expect.

* Remember that the reach for authenticated audience segments is naturally smaller than the reach for cookie-based segments, and that using additional targeting options further decreases your reach. Be judicious about using granular targeting, especially by joining multiple targets with AND statements.

## Data Variances Between Email IDs and Universal IDs {#universal-ids-data-variances}

### Acceptable levels of variance

The translation rate of hashed email addresses to universal IDs should be greater than 90%; the translation rate for [!DNL RampIDs] in particular should be 95% if all hashed email addresses are unique. For example, if you send 100 hashed email addresses from your customer data platform, they should be translated to at least 95 [!DNL RampIDs] or more than 90 other types of universal IDs. A lower translation rate may indicate an issue. See "[Causes of variance](#universal-ids-data-variances-causes" for possible explanations.

For [!DNL RampIDs], contact your Adobe Account Team for further investigation if translation rates are lower than 70%.

### Causes of variance {#universal-ids-data-variances-causes}

* All segments:

  The segment-to-device count uses a probabilistic model, which has an error variance of +/- 5%. This means that it can overestimate or underestimate the audience count by 5%.

* Hashed email IDs translated to [!DNL RampIDs]:

  * When multiple profiles use the same email ID, the DSP segment count can be lower than the profile count within your customer data platform. For example, in Adobe Photoshop, you can create a company account and a personal account using a single email ID. But if both profiles belong to the same person, then the profiles map to one email ID and correspondingly to one [!DNL RampID]. 

  * A [!DNL RampID] can be upgraded to a new value. If [!DNL LiveRamp] doesn't recognize an email ID or can't map it to an existing [!DNL RampID] in its database, then it assigns a new [!DNL RampID] to the email ID. In the future, when they can map the email ID to another [!DNL RampID] or can gather more information about the same email ID, they upgrade the [!DNL RampID] to a new value. [!DNL LiveRamp] refers to this action as upgrading from a "derived" [!DNL RampID] to a "maintained" [!DNL RampID]. However, DSP doesn't get mappings between derived and maintained [!DNL RampIDs] and therefore can't remove the previous version of the RampID from the DSP segment. In this case, the segment count can be more than the profile count.

    Example: A user logs in to the [!DNL Adobe] website and visits the Photoshop page. If [!DNL LiveRamp] doesn't have any existing information about the email ID, then they assign it a derived [!DNL RampID], say D123. Fifteen days later, the user visits the same page, but [!DNL LiveRamp] has upgraded the [!DNL RampID] during those 15 days and has reassigned the [!DNL RampID] to M123. Even though the customer data platform's segment "Photoshop Enthusiast" has only one email ID for the user, the DSP segment has two RampIDs: D123 and M123.

## Troubleshooting

If you don't see user counts, or if your audience sizes are low, then check the following:

* If you use [!DNL Flashtalking] or [!DNL Google Campaign Manager 360] ads, then make sure that your ads' clickthrough URLs are appended with the correct macros. See the macros for [[!DNL Flashtalking] ads](/help/integrations/analytics/macros-flashtalking.md) and [[!DNL Google Campaign Manager 360] ads](/help/integrations/analytics/macros-google-campaign-manager.md).

* Make sure that the correct, universal ID partner-specific code is implemented on your website to match on-site events and ad exposures. Work with your [!DNL LiveRamp] or [!DNL ID5] representative as needed.

* (For [!DNL RampIDs] and [!DNL UID 2.0] IDs) Make sure that your [DSP data source is configured correctly](/help/dsp/audiences/sources/source-manage.md#source-settings), and that user counts are populated for the generated audience segments.

* If your reach is less than you expect, check that the audience segment logic isn't too granular.

* Make sure that your campaign, package, and placement settings are correct.<!-- wording-->

If you can't resolve the issue, then contact your Adobe Account Team.

>[!MORELIKETHIS]
>
>* [About First-Party Audience Sources](/help/dsp/audiences/sources/source-about.md)
>* [Manage Audience Sources to Activate Universal ID Audiences](/help/dsp/audiences/sources/source-manage.md)
>* [Create and Implement a Custom Segment](/help/dsp/audiences/custom-segment-create.md)
>* [Manually Import Authenticated Segments from [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
