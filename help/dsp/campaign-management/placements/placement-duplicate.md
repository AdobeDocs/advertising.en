---
title: Duplicate Placements
description: Learn how to duplicate one or more placements.
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
---
# Duplicate Placements

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplicate one or more placements to create placements with similar settings. You can:

* Make multiple duplicates of placements
* Duplicate placements within the original advertisers and campaigns or within different ones
* (For duplicated placements within the original campaigns) Optionally duplicate the original ads
* Modify the status and flight dates of the new placements

See "[What's Not Duplicated](#placement-not-duplicated)" for a list of placement settings that aren't duplicated.

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the submenu, click **[!UICONTROL Placements]**.

1. Do either of the following:

    * To duplicate one placement, click  **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** next to the package name.

    * To duplicate multiple placements:

        1. Select the check box next to each placement to duplicate.

        1. In the bulk actions toolbar, click **[!UICONTROL Duplicate]**.

1. Specify the new placement settings:

    1. (Single placements) Enter the new placement name.

    1. In the **[!UICONTROL Choose Package (Required)]** menu, select either the parent package or **[!UICONTROL No package]*.

    1. (Optional) Change the default settings.

    The settings apply to all selected placements.

    By default, the new placements are for the original ad type, are assigned to the original advertisers and campaigns, have flight schedules that begin on the current day, are paused, and don't include the original ads.

    When you create multiple placements, the new placement names are appended with a number, in sequence, using the convention <*original_placement_name #N*>, such as "My Placement #2."

1. Click **[!UICONTROL Submit]**.

## What's Not Duplicated {#placement-not-duplicated}

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

## Best Practices to Configure the New Placements

>[!TIP]
>
>* Use bulksheets to [make changes to multiple campaign components at once](/help/dsp/campaign-management/campaign-components-review-edit.md).
* Use ad tag sheets to [upload multiple third-party ads](/help/dsp/campaign-management/ads/ad-create-multiple.md). 

* Pause the new placements until you're ready to activate them.

* Consider the following, and edit the new placement settings as needed:

  * Does the account have enough funding to accommodate the new placement budgets?

  * Do the new placements need different budgets than the previous placements?

  * Upload creatives, including any necessary custom ad weighting and scheduling, and attach them to the placements. 

  * Attach event pixels as necessary to the placements and ads.

  * Include geographic targets and placement-level [!DNL DoubleVerify Authentic Brand Safety] segments as needed to the placements.

  * For programmatic guaranteed deals, use new deal IDs and create default placements.

  * Create new placements for [!UICONTROL Simple Ad Serving] deals as needed.

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Create a Placement](placement-create.md)
>* [Edit Placements](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
