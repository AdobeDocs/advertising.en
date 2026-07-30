---
title: Manage ad groups
description: Learn how to create and manage ad groups.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Manage ad groups

<!-- Go through all -->

*Beta feature*

An ad group includes a set of ads and their related keywords. An ad group in a campaign that targets the display network can also include placements, which are locations on the display network in which your ads can appear. Ad group settings, which apply to all components of the ad group, vary by ad network.

Once you [make an ad network account accessible via an API connection](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) and Search, Social, & Commerce has synchronized the account data with the ad network, you can create ad groups for a [supported campaign type](/help/search-social-commerce/introduction/supported-inventory.md). You also can edit and change the status of ad groups.

For details about the functionality available for each ad network, see "[Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md)."

## About the [!UICONTROL Ad Groups] view {#ad-group-view-about}

The [!UICONTROL Manage] > [!UICONTROL Ad Groups] view lists all ad groups in the filtered view for the selected advertiser account.

### Available actions

* [Create an ad group](#ad-group-create)

* [Rename an ad group from within the row](#ad-group-rename)

* [Edit ad group settings](#ad-group-edit)

* [Change the status of, or delete, an ad group from within the row](#ad-group-status)

* [View a performance graph in the [!UICONTROL Ad Groups] view](#ad-group-performance-graph)

* [Assign bid constraints to ad groups, and unassign constraints from ad groups](#ad-group-constraints)

* [Assign label classifications to ad groups, and remove label classifications from ad groups](#ad-group-classifications)

* [Manage data view reports from the [!UICONTROL Ad Groups] view](#ad-group-reports)

## Create an ad group {#ad-group-create}

>[!TIP]
>
>To create a large number of ad groups at once, use<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [campaign bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ad Groups]**.

1. Click **[!UICONTROL Create Ad Group]**.

1. Specify the [Baidu](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md), or [Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md) ad group settings.

1. Click **[!UICONTROL Review and Save]**.

1. If necessary, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit") and change the ad group settings.

1. Click **[!UICONTROL Create]**.

Later, you can optionally override the ad group-level bids by setting bids for individual keywords or placements in the ad group.

## Rename an ad group {#ad-group-rename}

Quickly rename an ad group without opening the full ad group settings.

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ad Groups]**.

1. Hold the cursor over the ad group row and click **[!UICONTROL ...] > [!UICONTROL Rename]**.

1. Edit the name, and then click **[!UICONTROL Apply]**.

## Edit ad group settings {#ad-group-edit}

You can edit settings for individual ad groups. You can also edit some fields for multiple ad groups at once, including some ad group details, budget options, and URL options that are common to all of the selected ad groups.

>[!TIP]
>
>You can also edit data in bulk using <!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [campaign bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ad Groups]**.

1. Do either of the following:

   * Hold the cursor over the entity name and click **[!UICONTROL ...] > [!UICONTROL Edit]**.

   * Select the check box next to the ad group. In the bulk actions toolbar, click **[!UICONTROL Edit]**.

1. Edit the [Baidu](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md), or [Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md) ad group settings.

1. Click **[!UICONTROL Review and Save]**.

1. If necessary, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit") and change the ad group settings.

1. Click **[!UICONTROL Update]**.

## Change the status of an ad group {#ad-group-status}

Quickly change the status of an ad group without opening the full ad group settings.

You can pause any active ad group on a supported ad network to disable bidding on it. You can later resume bidding by changing the status back to active.

You also can delete any active or paused ad group. Deleted ad groups are deleted from the ad network. They're still visible when you include them in the data filter, but you can't change them.

### Activate or pause an ad group

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ad Groups]**.

1. Hold the cursor over the ad group row and click ![Edit](/help/search-social-commerce/assets/edit.png "Edit") next to the [!UICONTROL Status] column.

1. Change the status:

   * To activate a paused ad group, select **[!UICONTROL Active]**.

   * To pause an active ad group, select **[!UICONTROL Paused]**.

### Delete an ad group

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ad Groups]**.

1. Do either of the following:

   * Hold the cursor over the ad group row and click **[!UICONTROL ...] > [!UICONTROL Delete]**.

   * Hold the cursor over the ad group row and click ![Edit](/help/search-social-commerce/assets/edit.png "Edit") next to the [!UICONTROL Status] column. Select **[!UICONTROL Deleted]**.

## Manage bid constraint assignments for ad groups {#ad-group-constraints}

Each entity can have only one constraint. Constraints are inherited by child entities, so you don't need to assign constraints for child entities unless you want to override the inherited values.

Unassigning a constraint removes the association with the account components and all of their child components, and report data for the constraint is no longer available for those components. Unassigning a constraint doesn't delete the constraint nor the account components themselves.

### Assign a bid constraint to selected ad groups from the new [!UICONTROL Ad Groups] view

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ad Groups]**.

1. Select the check box next to each ad group to which you'll assign a single constraint.

1. In the bulk actions toolbar, click **+ [!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Select the constraint.

1. Click **[!UICONTROL Assign Now]**.

### Assign a bid constraint to selected search bid units from the legacy [!UICONTROL Campaigns] views

1. In **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**, select the account component view.

1. Select the check box next to each relevant row.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click **[!UICONTROL More]**, and then click **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Select the applicable constraint.

1. (Optional) Enter additional details:

   1. Next to [!UICONTROL Additional Details], click **[!UICONTROL Open]** to expand the details.

   1. Enter an optional **[!UICONTROL Project Name]** and/or optional **[!UICONTROL Description]**.

1. Click **[!UICONTROL Save]**.

### Remove bid constraints from selected ad groups from the new [!UICONTROL Ad Groups] view

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ad Groups]**.

1. Select the check box next to each ad group from which you'll unassign constraints.

1. In the bulk actions toolbar, click **- [!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Click **[!UICONTROL Confirm]**.

### Remove bid constraints from search bid units from the legacy [!UICONTROL Campaigns] views

>[!NOTE]
>
>To delete a constraint, making it unavailable for future use, see "Delete constraints for search bid units" in the Optimization Guide chapter on "Bid Constraints," which is available from within Search, Social, & Commerce.

1. In **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**, select the account component view.

1. Select the check box next to each component from which you want to remove the constraint.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click **[!UICONTROL More]**, and then click **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. In the confirmation dialog, select **[!UICONTROL Yes, Unassign]**.

## Assign label classifications to ad groups {#ad-group-classifications}

>[!NOTE]
>
>Label values are inherited by child entities, so don't enter values for child entities unless you want to override the inherited values.

### Assign classification values to ad groups

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ad Groups]**.

1. Select the check box next to each ad group to which you'll assign a label value.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click **+ [!UICONTROL Assign]** > **[!UICONTROL Label Classification]**.

1. For each applicable classification value, do the following:

   1. In the **[!UICONTROL Classifications]** column, specify the classification:
     
      * To use an existing classification, click the classification name to expand it.
     
      * To create a classification, click [!UICONTROL +] in the column heading. In the input field, enter the classification name, and then click ![Save](/help/search-social-commerce/assets/save-checkmark.png "Save") to immediately save the classification. To use the new classification, click the classification name to expand it.
        
        The name must consist of [ASCII characters 32-126](https://www.asciitable.com/), and the maximum length is 27 single-byte characters.
   
   1. In the **[!UICONTROL Value Name]** column, specify the value for the selected classification:
   
      * To use an existing value, select the value.
      
      * To create a value, click [!UICONTROL +] in the column heading. In the input field, enter the value, and then click ![Save](/help/search-social-commerce/assets/save-checkmark.png "Save") to immediately save the value and select it by default.

        The maximum length is 100 characters, and it can include ASCII and non-ASCII characters.

1. Click **+ [!UICONTROL Assign Now]**.

### Remove label classification values from ad groups

Removing a classification value removes the association with the account component and all of its child components. Report data for the classification value is no longer available for those components. Removing a classification value doesn't delete the value nor the account components.

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ad Groups]**.

1. Select the check box next to each ad group from which you'll remove a label value.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Select the check box next to each classification value to remove from the selected entities.

   To select all assigned values, click **[!UICONTROL Select All]**. To deselect all assigned valued, click **[!UICONTROL Deselect All]**.

1. Click **[!UICONTROL Unassign Selected]**.

## View a performance graph in the [!UICONTROL Ad Groups] view {#ad-group-performance-graph}

Open and configure a performance graph with up to three metrics totalled across all ad groups in the view for the specified date range.

### View a performance graph

1. Above the data table, click ![Charts](/help/search-social-commerce/assets/charts.png "Charts").

1. (Optional) Specify the currency and up to three metrics to include in the chart.

### Hide a visible performance graph

* Above the data table, click ![Charts](/help/search-social-commerce/assets/charts.png "Charts").

## Manage data view reports from the [!UICONTROL Ad Groups] view {#ad-group-reports}

Generate a report that includes the data rows for one or more ad groups in the [!UICONTROL Ad Groups] view, and then download the report as a Microsoft Excel worksheet file (XLXS format). The report includes all visible columns in the view.

You can delete any generated report.

See also ">* [(Legacy UI) Download data from a campaign management view](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)" and "[(Legacy UI) Delete a performance data report or bulksheet file from the [!UICONTROL Downloads] menu](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)."

### Generate a report with the filtered data rows

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ad Groups]**.

1. Specify the ad groups whose data you want to download:

   * To download data for specific ad groups, select the check boxes next to the ad groups.

   * To download data for all ad groups, you don't need to select any check boxes. All ad groups are included by default.

1. In the toolbar above the data table, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report") **[!UICONTROL Reports]**.

1. In the [!UICONTROL Grid Reports] settings, enter a unique report name, and then click **[!UICONTROL Generate]**.

   By default, the file is named "ad group_YYYYMMDD_NNNN," where "NNNN" is the sequential job number (such as "ad group_20250402_1326).

   The file is added to the [!UICONTROL Recently Generated] list.

1. (Optional) To download the file once it's completed, click ![Download](/help/search-social-commerce/assets/download.png "Download") next to the file name.

   The file is downloaded according to your browser's normal procedure.

### Download a completed report

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ad Groups]**.

1. In the toolbar above the data table, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report") **[!UICONTROL Reports]**.

1. In the [!UICONTROL Recently Generated] list in the [!UICONTROL Grid Reports] dialog, click ![Download](/help/search-social-commerce/assets/download.png "Download") next to the file name.

   The file is downloaded according to your browser's normal procedure.

### Delete a completed report

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ad Groups]**.

1. In the toolbar above the data table, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report") **[!UICONTROL Reports]**.

1. In the [!UICONTROL Recently Generated] list in the [!UICONTROL Grid Reports] dialog, click ![Delete](/help/search-social-commerce/assets/delete-new.png "Delete") next to the file name.

>[!MORELIKETHIS]
>
>* [Manage constraints for search bid units](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Manage constraint assignments for campaigns](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [Manage constraint assignments for keywords](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [Manage constraint assignments for placements](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [(Legacy UI) Download data from a campaign management view](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [(Legacy UI) Delete a performance data report or bulksheet file from the [!UICONTROL Downloads] menu](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] ad group settings](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md)
>* [[!DNL Google Ads] ad group settings](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md)
>* [[!DNL LY Ads] ad group settings](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md)
>* [[!DNL Microsoft Advertising] ad group settings](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md)
>* [[!DNL Yandex] ad group settings](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md)
