---
title: Duplicate a Package
description: Learn how to duplicate a package.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
---
# Duplicate a Package

Duplicate a package to create a package with similar settings. You can:

* Duplicate the package within the original advertiser and campaign or within different ones

* Optionally duplicate the placements within the package

* (For duplicated packages within the original campaigns) Optionally duplicate the original ads and placement-level event pixels

* Modify the flight dates of the new package

See "[What's Not Duplicated](#package-not-duplicated)" for a list of placement settings that aren't duplicated.

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign to open the [!UICONTROL Packages] view.

1. Next to the package name, click  **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Specify the new package settings:

    1. Enter the new package name.

    1. (Optional) Change the default settings.

         By default:

         * The new package is assigned to the original advertiser and campaign.

         * The new package becomes active on the current day.<!-- and the flight continues for NN  days. -->

         * Placements within the original package are copied to the new package.

         * The ads and the placement-level event pixels aren't copied to the new package.

1. Click **[!UICONTROL Submit]**.

## What's Not Duplicated {#package-not-duplicated}

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

## Best Practices to Configure the New Package

>[!TIP]
>
>* Use bulksheets to [make changes to multiple campaign components at once](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Use ad tag sheets to [upload multiple third-party ads](/help/dsp/campaign-management/ads/ad-create-multiple.md). 

* Pause the new package until you're ready to activate it.

* Consider the following, and edit the new package as needed:

  * Does the account have enough funding to accommodate the new package budget?

  * Does the new package need a different budget than the previous package?

  * Upload creatives, including any necessary custom ad weighting and scheduling, and attach them to the placements. 

  * Attach event pixels as necessary to the placements and ads.

  * Include geographic targets and placement-level [!DNL DoubleVerify Authentic Brand Safety] segments as needed to placements.

  * For programmatic guaranteed deals, use new deal IDs and create default placements.

  * Create new placements for [!UICONTROL Simple Ad Serving] deals as needed.

* For packages that use custom optimization goals, use the [[!UICONTROL Linked Package for Optimization Learnings Carryover] setting](/help/dsp/campaign-management/packages/package-settings.md) for each package to use the previous campaign's historic data as input for optimizing the package.

>[!MORELIKETHIS]
>
>* [About Package Management](package-about.md)
>* [Create a Package](package-create.md)
>* [Edit a Package](package-edit.md)
>* [View the Change Log for a Package](package-change-log.md)
>* [Package Settings](package-settings.md)
