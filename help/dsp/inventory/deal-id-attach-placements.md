---
title: Specify placements and ads for a private deal
description: Learn how to use a private deal with additional placements and ads.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
---
# Specify placements and ads for a private deal

For non-guaranteed deals, you can specify the deal as an inventory target for new placements from the [!UICONTROL Placements] view.

For programmatic guaranteed (PG) deals, you can create placements with specified ads from the [!UICONTROL Deals] view.

You can also [attach ads to placements](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) associated with PG and non-guaranteed deals at any time.

## Specify a non-guaranteed deal as an inventory target for a placement

* [Create a placement from the [!UICONTROL Placements] view](/help/dsp/campaign-management/placements/placement-create.md). In the [!UICONTROL Inventory Targeting] settings, select the private deal.

## Attach placements and ads to a PG deal

1. In the main menu, click **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. In the deal row, click  **[!UICONTROL ...]** > **[!UICONTROL Attach New Placement]**.

1. In the [!UICONTROL Ad & Campaign Selection] settings, select the ads to use for the placement:

       1. Select the advertiser, campaign, and ad type. Optionally select an ad status by which to filter the ads.

       1. From the list of available ads, select the check box next to each ad to use for the deal.

       1. Click **[!UICONTROL Apply]**.

    1. In the placement settings screen:

       1. Enter the placement name.

       1. (Optional) Edit the [placement settings](/help/dsp/campaign-management/placements/placement-settings.md), including overwriting the default bid, which is automatically populated with the CPM value from the deal; changing the date range; or attaching more ads.

         The deal is automatically targeted in the Inventory Targets section. All other targeting options are inapplicable.

       1. Click **[!UICONTROL Create placement]**.

The placement begins running after the publisher activates your PG deal ID.

>[!NOTE]
>
> You don't need to send the deal tag to the publisher for verification.

>[!MORELIKETHIS]
>
>* [About private inventory](private-inventory-about.md)
>* [List the placements and ads for a private deal](/help/dsp/inventory/private-deal-view-placements.md)
>* [Manually create deal ID details](deal-id-create.md)
>* [Manual deal ID settings](deal-id-settings.md)
>* [Set up a programmatic guaranteed deal](programmatic-guaranteed-set-up.md)
