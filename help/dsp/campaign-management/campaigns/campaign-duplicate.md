---
title: Duplicate a Campaign
description: Learn how to duplicate a campaign.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
---
# Duplicate a Campaign

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplicate a campaign to create a new campaign with similar settings. You can:

* Duplicate the campaign for the original advertiser or for a different one

* Optionally duplicate the original packages and placements

* Modify the flight dates of the new campaign

See "[What's Not Duplicated](#campaign-not-duplicated)" for a list of placement settings that aren't duplicated.

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Next to the campaign name, click **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Specify the new campaign settings:

    1. Enter the new campaign name and the end flight date.

    1. (Optional) Change the default settings.

         By default, the new campaign is assigned to the original advertiser, has a flight schedule that begins on the current day, and includes the original packages and placements.

1. Click **[!UICONTROL Submit]**.

## What's Not Duplicated {#campaign-not-duplicated}

All settings from the original placements are duplicated except:

* Experiment settings
* (If you change the flight dates) Custom ad scheduling
* (If you don't attach ads) Custom ad weighting and scheduling
* Default placements for programmatic guaranteed (PG) deals and placements for [!UICONTROL Simple Ad Serving] deals
* (If you copy placements to a different campaign):
   * Geo targets
   * Event pixels
   * Ads
   * Placement-level [!DNL DoubleVerify Authentic Brand Safety] segments (which override the advertiser-level segments)

## Best Practices to Configure the New Campaign

>[!TIP]
>
>* Use bulksheets to [make changes to multiple campaign components at once](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Use ad tag sheets to [upload multiple third-party ads](/help/dsp/campaign-management/ads/ad-create-multiple.md). 

* Pause the new campaign until you're ready to activate it.

* Consider the following, and edit the new campaign settings as needed:

  * Does the account have enough funding to accommodate the new campaign budget?

  * Does the new campaign need a different budget than the previous campaign?

  * Upload creatives, including any necessary custom ad weighting and scheduling, and attach them to the placements. 

  * Attach event pixels as necessary to the placements and ads.

  * Include geographic targets and placement-level [!DNL DoubleVerify Authentic Brand Safety] segments as needed to placements.

  * For programmatic guaranteed deals, use new deal IDs and create default placements.

  * Create new placements for [!UICONTROL Simple Ad Serving] deals as needed.

* For performance campaigns (that is, campaigns with packages that use custom optimization goals), use the [[!UICONTROL Linked Package for Optimization Learnings Carryover] setting](/help/dsp/campaign-management/packages/package-settings.md) for each package to use the previous campaign's historic data as input for optimizing the package.

>[!MORELIKETHIS]
>
>* [About Campaign Management](campaign-about.md)
>* [Create a Campaign](campaign-create.md)
>* [Edit a Campaign](campaign-edit.md)
>* [View the Change Log for a Campaign](campaign-change-log.md)
>* [Campaign Settings](campaign-settings.md)
