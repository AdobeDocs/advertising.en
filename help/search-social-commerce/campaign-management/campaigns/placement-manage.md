---
title: Manage [!DNL Google Ads] placements
description: Learn how to create and manage biddable placements for [!DNL Google Ads] ad groups.
exl-id: 91fee1eb-d1d5-4a1b-b1a6-369b98269100
---
# Manage [!DNL Google Ads] placements

*[!DNL Google Ads] accounts only*

You can create and edit placements for ad groups in [supported campaign types](/help/search-social-commerce/introduction/supported-inventory.md) that target the display network within a [synchronized ad network account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)

## Create [!DNL Google Ads] placements

>[!TIP]
>
>To create many placements at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Placements] > [!UICONTROL Placements]**.

1. 1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network, the account, the campaign, and the ad group, and then click **[!UICONTROL Continue]**.

1. Configure the [placement settings](#placement-settings).

1. Click **[!UICONTROL Post]**.

## Edit [!DNL Google Ads] placements

>[!TIP]
>
>To edit many placements at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Keywords] > [!UICONTROL Keywords]**.

1. Select the check box next to each row to edit.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit") .

1. Edit the [placement settings](#placement-settings).

   For multiple placements, your changes are applied to all selected placements. For some alphanumeric fields, you can change existing values to a specified value, replace an existing string with a specified string, add a specified prefix to the beginning of each value, or append a suffix to the end of each value. For some monetary fields, you can change existing values to a specified value or either increase or decrease the amount by a specified percentage or monetary amount, with a limit.

1. Save the data:

   * (Single placements) Click **[!UICONTROL Post]**.
   
   * (Multiple placements) Click **[!UICONTROL Post Now]**.

## Placement settings {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** Sites on the content network on which your ad can appear. Enter a valid URL, such as www.example.com, example.com,or www.example.com/shoes/kids. To specify multiple strings, separate them with commas or enter them on separate lines. The URL can't include a question mark (`?`). **Note:** You can [exclude website placements](placement-negative-create.md) from the [!UICONTROL Placements] > [!UICONTROL Negatives] view and in the ad group and campaign settings.

**[!UICONTROL Status]:** The display status of the placement: *Active* (to enable bidding; the default), *Paused* (to disable bidding), or *Deleted* (to delete the placement; existing placements only).

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (Optional) The maximum cost per click (CPC) or cost per thousand viewable impressions (vCPM) for the placement-based ad, depending on the campaign bid strategy. This value overrides the ad group-level bid.

<!-- If the placement is in a standard optimized portfolio, then the specified bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations. -->

### [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URL]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- note -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [About placements](placement-about.md)
>* [Create negative placements](placement-negative-create.md)
>* [Change the status of placements and negative placements](placement-status-edit.md)
