---
title: Support for Activating Universal IDs
description: Learn about support to import your universal ID segments, create custom segments to track universal IDs, and convert other user identifiers in your first-party segments to universal IDs for cookieless targeting.
feature: DSP Audiences
---
# Support for Activating Universal IDs

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

DSP supports people-based, universal IDs for cookieless, single-device (not cross-device) targeting across digital formats supported by DSP.

* You can manually send your authenticated [[!DNL LiveRamp] [!DNL RampIDs]] directly to DSP using the [!DNL LiveRamp] [!DNL Connect] dashboard. See "[Manually Import Authenticated Segments from [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)."

* DSP can ingest your first-party segments comprised of hashed email IDs built within your customer data platform (CDP) and convert them to universal IDs. For more information about the supported customer data platforms, supported universal ID types and their available features, and the related workflows, see "[About First-Party Audience Sources](/help/dsp/audiences/sources/source-about.md)."

* You can create custom segments that track users associated with ID5 universal IDs who are exposed to ads from desktop and mobile devices and who visit specific webpages. ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp). For instructions, see "[Create and Implement a Custom Segment](/help/dsp/audiences/custom-segment-create.md)."

* Third-party segments from [!DNL Eyeota] and some other vendors may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.

<!-- Make above statement more generic when other ID types are available 

* Some third-party segment vendors have started including universal IDs in their segments, and you can use them in saved audiences and as placement targets without any extra steps or extra fees.
-->

## Reporting by Universal ID Type

* **Custom reports:** Cost, impression, click, conversion, and frequency data by universal ID type is available in custom reports.

* **[!DNL Analytics] reports:** Advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) who have implemented all required steps can see view-through conversions by universal ID type in [!DNL Analytics].

* **Segment details:** For all segment types, the segment details include the audience size by universal ID type and by the device type tracked by cookies or device IDs.

## How to Target an Universal ID Audience in Your Placements

When you create a placement, do the following:

* In the [!UICONTROL Geo-Targeting] section, specify the geographical areas to target. Each universal ID partner allows user targeting only in specific geographical areas, and only eligible ID types are available in the [!UICONTROL Targeting] settings.

* In the [!UICONTROL Audience Targeting] section, do the following:

  * In the [!UICONTROL Included Audiences] setting, select the segment for which user data was converted to universal IDs.

    You can include additional segments if you want.

  * In the [!UICONTROL Targeting] setting, select the universal ID type to target.
  
    The setting includes the options "[!UICONTROL Legacy IDs]" and "[!UICONTROL Universal ID]," which may include the sub-options "[!UICONTROL ID5]," "[!UICONTROL RampID]," and "[!UICONTROL Unified ID2.0]." The actual sub-options are determined by the selected geographical targets.
    
    You can select both "[!UICONTROL Legacy IDs]" and "[!UICONTROL Universal ID]," but you can select only one type of universal ID per placement. When you select both legacy IDs and universal IDs, bidding preference is given to universal IDs. 

See "[Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)."

## Best Practices for Testing and Data Validation

Use the following best practices for [!DNL RampID]-based segments and ID5-based segments, for which Adobe Analytics measurement is available.

<!-- revisit -->

* About 24 hours after you activate a segment, check the converted ID count for the segment within [!UICONTROL Audiences] > [!UICONTROL All Audiences]. If the ID count is unexpected, then contact your Adobe Account Team. <!-- What can be causes of data variances, and how much variance can be expected? -->

* Don't change your existing packages and placements. However, if you don't have incremental budget to test universal IDs, then reduce the original budgets to fund the tests.

* Copy your original packages and placements, adjust the budgets based on the size of the test, change the audiences to use [!DNL RampID]-based segments (for authenticated users) or ID5-based segments (for unauthenticated users), and verify that the new packages and placements spend their full budgets.

  * To compare the performance of universal ID-based segments with the performance of placements targeting other audience identifiers, such as cookies or mobile advertising IDs, create a campaign with a separate universal ID-based placement and a legacy ID-based placement.

    Use the following configuration:

    * The recommended campaign budget is USD 10,000. Split the budget evenly between the universal ID-based placement (test group) and the legacy ID-based placement (test group).

    * The recommended audience size is 25,000 universal IDs.

    * Run the placements for at least three weeks.

    * Use the following ad types: display, video, CTV, universal video, and audio

    Getting the best performance shouldn't be the primary comparison. Instead, determine which IDs are scaling well, which might inform your optimization and budget allocations later. The long-term goal is to make up for lost impressions and site traffic when cookies are deprecated.

  * To compare total browser reach, target universal ID-based segments and legacy ID-based segments in the same placement. Use the same campaign settings as the previous use case, except that you don't need to split the campaign budget.
  
    Bidding preference is given to universal IDs, but legacy IDs will receive bids when universal IDs aren't available. Make sure to compare reach in different browsers (including Chrome, Safari, and Mozilla).
 
    >[!NOTE]
    >
    >Frequency capping applies to an individual ID. When a user has multiple ID types, you might be reaching that user more than you had expected.

* Remember that the reach for authenticated audience segments is naturally smaller than the reach for cookie-based segments, and that using additional targeting options further decreases your reach. Be judicious about using granular targeting, especially by joining multiple targets with AND statements.

>[!MORELIKETHIS]
>
>* [Create an Audience Source to Activate Universal ID Audiences](/help/dsp/audiences/sources/source-create.md)
>* [Convert User IDs from [!DNL Adobe Real-Time CDP] to Universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convert User IDs from [!DNL Tealium] to Universal IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Create and Implement a Custom Segment](/help/dsp/audiences/custom-segment-create.md)
>* [Manually Import Authenticated Segments from [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
