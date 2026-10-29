---
title: Manage placements
description: Learn how to create and manage Google Ads placements and negative placements and assign constraints to placements.
feature: Search Optimization, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# Manage placements

*Beta feature*

*[!DNL Google Ads] accounts only*

Placements are locations on the display network in which your ads can appear. Placement settings include the maximum bid and optional tracking parameters. Placement-level settings override the ad group or campaign settings. Negative placements prevent ads from being displayed on specified sites.

Once you [make an ad network account accessible via an API connection](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md) and Search, Social, & Commerce has synchronized the account data with the ad network, you can create placements for ad groups in [supported campaign types](/help/search-social-commerce/introduction/supported-inventory.md) that target the display network. You also can edit and change the status of placements, and create and delete negative placements.

>[!NOTE]
>
>[!DNL Google Ads] doesn't provide ad-level performance data for placements.

## About the [!UICONTROL Placements] view {#placement-view-about}

The [!UICONTROL Targeting] > [!UICONTROL Placements] view includes two tabs for the selected advertiser account:

* The [!UICONTROL Placements] tab lists all biddable placements in the filtered view.

* The [!UICONTROL Negatives] tab lists all negative placements in the filtered view.

Viewing the page requires the [!UICONTROL View Placements] permission. Creating placements or negative placements, editing placements, changing placement status, and deleting placements or negative placements requires the [!UICONTROL Edit Placements] permission.

### Available actions

* [Create placements](#placement-create)

* [Create negative placements](#placement-negative-create)

* [Edit placement settings](#placement-edit)

* [Change the status of, or delete, placements and negative placements](#placement-status)

* [Copy all data in selected rows to your clipboard](#copy-to-clipboard)

* [Assign constraints to placements, and unassign constraints from placements](#placement-constraints)

* [Assign label classifications to placements](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)

## Create placements {#placement-create}

>[!TIP]
>
>To create a large number of placements at once, use [campaign bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Placements]**.

1. On the **[!UICONTROL Placements]** tab, click **[!UICONTROL Create Placement]**.

1. In the **[!UICONTROL Basic Settings]** step, select the network, the account, the campaign, and the ad group.

1. Enter the [placement settings](#placement-create-settings).

   To create multiple placements, separate the website URLs with commas.

1. Click **[!UICONTROL Review and Save]**.

1. Review the settings. To change any settings, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit") **[!UICONTROL Edit]** in the applicable section and change the settings.

1. Click **[!UICONTROL Create]**.

## Create negative placements {#placement-negative-create}

You can create negative placements for a [!DNL Google Ads] campaign or ad group that targets the display network.

>[!NOTE]
>
>You also can create and edit negative placements in the [ad group settings](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md) and [campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md).

>[!TIP]
>
>To create a large number of negative placements at once, use [campaign bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Placements]**.

1. On the **[!UICONTROL Negatives]** tab, click **[!UICONTROL Create Negative]** and then either **[!UICONTROL Campaign Negative]** or **[!UICONTROL Ad Group Negative]**.

1. In the **[!UICONTROL Basic Settings]** step, select the network, the account, the campaign, and (for ad group-level negative placements) the ad group.

1. In the **[!UICONTROL Manage Websites]** step, enter the negative website URLs, such as `www.example.com` or `example.com/shoes`.

   Separate multiple URLs with commas. This form accepts website URLs, not topic or category strings.

1. Click **[!UICONTROL Review and Save]**.

1. Review the settings. To change any settings, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit") **[!UICONTROL Edit]** in the applicable section and change the settings.

1. Click **[!UICONTROL Create]**.

## Edit placement settings {#placement-edit}

You can edit the status, bid, base URL, and tracking template for one or more placements. You can't change the targeted website URL or edit deleted placements.

>[!TIP]
>
>To edit a large amount of placement data at once, use [campaign bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Placements]**.

1. On the **[!UICONTROL Placements]** tab, select the check box next to each placement to edit.

1. In the bulk actions toolbar, click **[!UICONTROL Edit]**.

1. In the **[!UICONTROL Edit Placements]** panel, edit the [placement settings](#placement-edit-settings).

   For multiple placements, your changes are applied to all selected placements. You can set bids to a specified value or increase or decrease them by a specified percentage or monetary amount, with a limit. For URLs, you can replace the existing value, find and replace text, add a prefix, or append a suffix.

   Bid editing is disabled when the selected placements use multiple currencies.

1. Click **[!UICONTROL Save]**.

## Change the status of placements and negative placements {#placement-status}

You can pause an active, biddable placement to disable bidding on it. You can later resume bidding by changing the status back to active.

You also can delete active or paused placements or negative placements. Deleted placements are deleted from the ad network. They're still visible when you include them in the data filter, but you can't change them.

### Activate or pause placements

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Placements]**.

1. On the **[!UICONTROL Placements]** tab, optionally filter the list, and then select the check box next to each placement whose status you want to change.

1. In the bulk actions toolbar, click **[!UICONTROL Edit]**.

1. In the **[!UICONTROL Placement Details]** section, change the **[!UICONTROL Status]**:

   * To activate paused placements, select **[!UICONTROL Active]**.

   * To pause active placements, select **[!UICONTROL Paused]**.

1. Click **[!UICONTROL Save]**.

### Delete placements or negative placements

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Placements]**.

1. On the **[!UICONTROL Placements]** or **[!UICONTROL Negatives]** tab, optionally filter the list, and then select the check box next to each placement or negative placement to delete.

1. In the bulk actions toolbar, click **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

## Copy all data in selected rows to your clipboard {#copy-to-clipboard}

Copy the visible information in selected rows, according to the applied filters and columns visible in the view. The information is saved as tab-separated values (TSV).

1. Select the check box next to each row whose data you want to copy.

1. In the bulk actions toolbar, click **[!UICONTROL Copy]**.

## Manage constraint assignments for placements {#placement-constraints}

You can assign and remove bidding constraints for campaigns, ad groups, keywords, placements, unit-level product groups, and dynamic search targets. Each entity can have only one constraint.

Constraints are inherited by child entities, so you don't need to assign constraints for child entities unless you want to override the inherited values.

Unassigning a constraint removes the association with the account components and all of their child components, and report data for the constraint is no longer available for those components. Unassigning a constraint doesn't delete the constraint or the account components themselves.

>[!NOTE]
>
>* If you later edit a keyword or the ad copy for a non-mutable ad &mdash; thereby creating a new keyword or ad &mdash; then the constraint isn't assigned to the new entity.
>* Active constraints restrict bidding only for assigned bid units in optimized legacy keyword-level portfolios. They're ignored for bid units that are in active portfolios, are in hybrid portfolios, or aren't in portfolios.

### Assign a constraint to placements {#placement-constraint-assign}

You can assign a single constraint to one or more placements.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Placements]**.

1. On the **[!UICONTROL Placements]** tab, select the check box next to each placement to which you'll assign a single constraint.

1. In the bulk actions toolbar, click **[!UICONTROL Assign] > [!UICONTROL Bid Constraint]**.

1. Select the constraint.

1. Click **[!UICONTROL Assign Now]**.

### Unassign constraints from placements {#placement-constraint-unassign}

Unassigning a constraint doesn't delete it. To delete a constraint, making it unavailable for future use, see "[Manage constraints for search bid units](/help/search-social-commerce/new-ui/goals/constraints-manage.md#constraint-change-status)."

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Placements]**.

1. On the **[!UICONTROL Placements]** tab, select the check box next to each placement from which you'll unassign constraints.

1. In the bulk actions toolbar, click **[!UICONTROL Unassign] > [!UICONTROL Bid Constraint]**.

1. Click **[!UICONTROL Confirm]**.

## Placement settings {#placement-settings}

### Settings when creating placements {#placement-create-settings}

#### [!UICONTROL Basic Settings]

**[!UICONTROL Network]:** The ad network. Only [!DNL Google Ads] is supported.

**[!UICONTROL Account]:** The ad network account.

**[!UICONTROL Campaign]:** The campaign.

**[!UICONTROL Ad Group]:** The ad group.

#### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** Sites on the display network on which your ad can appear. Enter a valid website URL, such as `www.example.com`, `example.com`, or `example.com/shoes`. Separate multiple URLs with commas. The URL can't include a question mark (`?`).

To exclude websites instead, [create negative placements](#placement-negative-create) from the [!UICONTROL Targeting] > [!UICONTROL Placements] > [!UICONTROL Negatives] tab or use the ad group and campaign settings.

**[!UICONTROL Status]:** The display status of the placement: *[!UICONTROL Active]* (to enable bidding) or *[!UICONTROL Paused]* (to disable bidding).

#### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (Optional) The maximum cost per click (CPC) or cost per thousand viewable impressions (vCPM) for the placement-based ad, depending on the campaign bid strategy. This value overrides the ad group-level bid.

#### [!UICONTROL Tracking URLs]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!NOTE]
>
>The new-UI creation form requires the base URL and tracking template, when specified, to start with `http://` or `https://`.

### Settings when editing placements {#placement-edit-settings}

The [!UICONTROL Edit Placements] panel supports the following settings for one or more selected placements. You can't change the targeted website URL.

#### [!UICONTROL Placement Details]

**[!UICONTROL Status]:** *[!UICONTROL Active]* or *[!UICONTROL Paused]*.

#### [!UICONTROL Bid Details]

**[!UICONTROL Bid adjustment]:** How to change the bid:

* *[!UICONTROL Set to]:* Replace the existing bid with a specified value.

* *[!UICONTROL Increase]:* Increase the existing bid by a specified amount or percentage.

* *[!UICONTROL Decrease]:* Decrease the existing bid by a specified amount or percentage.

**[!UICONTROL Modifier type]:** (For increases or decreases) Whether the adjustment uses *[!UICONTROL Currency]* or *[!UICONTROL Percentage]*.

**[!UICONTROL Set value]:** The new bid or the adjustment amount. The minimum value is 0.01.

**[!UICONTROL Max limit]:** (For increases or decreases; optional) The limit for the adjusted bid. For an increase, this is the maximum bid; for a decrease, this is the minimum bid. The minimum limit value is 0.01.

Bid editing is disabled when the selected placements use multiple currencies.

#### [!UICONTROL Tracking Urls]

**[!UICONTROL Base Url]**, **[!UICONTROL Tracking Template]:** For each field, select how to modify the value:

* *[!UICONTROL Set To]:* Replace the value. Enter a valid website URL that begins with `http://` or `https://`.

* *[!UICONTROL Find/Replace]:* Replace specified text within the value. Enter the text to find and the replacement text.

* *[!UICONTROL Add Suffix]:* Append text to the value. Enter the suffix text.

* *[!UICONTROL Add Prefix]:* Add text to the beginning of the value. Enter the prefix text.

>[!NOTE]
>
>All new base URLs must be valid URLs that begin with `http://` or `https://`.

>[!MORELIKETHIS]
>
>* [Manage constraints for search bid units](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Manage label classifications](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
