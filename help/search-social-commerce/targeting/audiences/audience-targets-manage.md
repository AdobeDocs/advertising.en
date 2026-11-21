---
title: Manage audience targets for campaigns and ad groups
description: Learn how to manage audience targets and their bid adjustments for Google Ads and Microsoft Advertising.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Manage audience targets for campaigns and ad groups

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts only*

[!DNL Google Ads] campaigns and ad groups, and [!DNL Microsoft Advertising] ad groups, can target specific [audiences](audience-manage.md) from the same ad network. The ad network determines how large an audience must be to be targetable.

An audience target associates an existing audience with a campaign or ad group. You can edit the bid adjustment and status of existing targets.

>[!NOTE]
>
>[Audience exclusions](audience-exclusions.md) always override targets.

## About the [!UICONTROL Targets] view {#audience-targets-view-about}

The [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Targets] view lists the audience targets in the filtered view for the selected advertiser.

Viewing the data requires the [!UICONTROL View Audiences] permission. Editing, changing the status of, and deleting targets requires the [!UICONTROL Edit Audience Targets] permission.

### Available actions

<!--
Restricted to internal beta users:

* [Configure audience targets](#audience-targets-create)
-->

* [Edit audience target bid adjustments and status](#audience-targets-edit)

* [Change the status of, or delete, audience targets](#audience-targets-status)

* [Copy all data in selected rows to your clipboard](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience target creation.

## Configure audience targets {#audience-targets-create}

Creating targets requires the [!UICONTROL Edit Audience Targets] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Targets]** tab.

1. Click **[!UICONTROL Create Target]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups to target:

   * Select each applicable campaign or ad group for inclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

   You can't configure a target for both a parent campaign and a child ad group that automatically uses the target.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

1. (Optional) [Set a bid adjustment](#audience-targets-edit) for the new targets.
-->

## Edit audience target bid adjustments and status {#audience-targets-edit}

You can edit one or more audience targets at a time. Your changes apply to all selected targets.

>[!NOTE]
>
>Search, Social, & Commerce automatically optimizes the bid modifier when the parent campaign uses the CPC bid strategy and is in a portfolio configured to auto-optimize bid adjustment values for audience targets. Bid modifiers for [!DNL Microsoft Advertising] dynamic remarketing audience targets aren't optimized.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Targets]** tab.

1. Select the check box next to each target to edit.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click **[!UICONTROL Edit]**.

1. Edit the **[!UICONTROL Bid Modifier]** or **[!UICONTROL Status]**, or both. See the [editing settings](#audience-targets-edit-settings).

   Leave a field unchanged to retain the existing value.

1. (Optional) Expand **[!UICONTROL ADDITIONAL DETAILS]** and enter a **[!UICONTROL Project Name]** and **[!UICONTROL Description]**.

1. Click **[!UICONTROL Save]**.

You can also edit a single target's bid adjustment directly in the data table by clicking its value in the **[!UICONTROL Bid Adjustment]** column.

## Change the status of, or delete, audience targets {#audience-targets-status}

You can pause an active audience target to disable bidding for that target, and later resume bidding by activating it. You can also delete active or paused targets.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Targets]** tab.

1. (Optional) Filter the list to include specific audience targets.

1. Select the check box next to each target whose status you want to change.

1. In the bulk actions toolbar, click one of the following:

   * **[!UICONTROL Activate]** to activate the selected targets.

   * **[!UICONTROL Pause]** to pause the selected targets.

   * **[!UICONTROL Delete]** to delete the selected targets.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

## Copy all data in selected rows to your clipboard {#copy-to-clipboard}

Copy the visible information in selected rows, according to the applied filters and columns visible in the view. The information is saved as tab-separated values (TSV).

1. Select the check box next to each row whose data you want to copy.

1. In the bulk actions toolbar, click **[!UICONTROL Copy]**.

## Audience target editing settings {#audience-targets-edit-settings}

**[!UICONTROL Bid Modifier]:** How to change the audience bid adjustment:

* *[!UICONTROL Set To]:* Replace the existing bid adjustment with the specified percentage.

* *[!UICONTROL Increase]:* Increase the existing value by the specified percentage.

* *[!UICONTROL Decrease]:* Decrease the existing value by the specified percentage.

For [!UICONTROL Increase] and [!UICONTROL Decrease], enter a nonnegative value.

For a set value, 0% doesn't adjust the bid. Other supported values range from -90% to 900%. For example, if the keyword-level bid is 1 USD and the audience bid adjustment is 50%, the bid for that audience increases to 1.50 USD.

**[!UICONTROL Status]:** Select **[!UICONTROL Active]** to enable bidding or **[!UICONTROL Paused]** to disable bidding for the target.

>[!MORELIKETHIS]
>
>* [Manage audiences](audience-manage.md)
>* [Manage audience exclusions for campaigns and ad groups](audience-exclusions.md)
