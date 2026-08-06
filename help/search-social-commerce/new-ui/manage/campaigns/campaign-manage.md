---
title: Manage campaigns
description: Learn how to create and manage ad campaigns.
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
# Manage campaigns

*Beta feature*

A campaign is the primary component of an ad network account. For most campaign types, it consists of a set of ad groups or ad sets. Campaign settings include campaign budget parameters, ad targets, and optional tracking parameters for all ads in the campaign. Campaign-level tracking parameters override the account-level parameters but may themselves be overridden at a lower level.

Once you [make an ad network account accessible via an API connection](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) and Search, Social, & Commerce has synchronized the account data with the ad network, you can create new campaigns with [supported campaign types](/help/search-social-commerce/introduction/supported-inventory.md). You also can edit and change the status of campaigns.

For details about the functionality available for each ad network, see "[Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md)."

## About the [!UICONTROL Campaigns] view {#campaign-view-about}

The [!UICONTROL Manage] > [!UICONTROL Campaigns] view lists all campaigns in the filtered view for the selected advertiser account. You can open a list of ad groups in the campaign by clicking the campaign name.

As you add and edit campaign data in the [!UICONTROL Campaigns] views, Search, Social, & Commerce immediately pushes the data changes to the ad network. Search, Social, & Commerce also pulls campaign structure data and click data daily, or more often when new campaigns are detected. For all synced ad networks, you can also sync accounts on demand as needed.

Search, Social, & Commerce pulls performance data hourly from synced [!DNL Google Ads] and [!DNL Microsoft Advertising] accounts and daily for other synced ad network accounts.

### Available actions

* [Create a campaign](#campaign-create)

* [Rename a campaign from within the row](#campaign-rename)

* [Edit campaign settings](#campaign-edit)

* [Change the status of, or delete, a campaign from within the row](#campaign-status)

* [Assign campaigns to a portfolio, and remove campaigns from a portfolio](#campaign-portfolio)

* [View a performance graph in the [!UICONTROL Campaigns] view](#campaign-performance-graph)

* [Assign bid constraints to campaigns, and unassign constraints from campaigns](#campaign-constraints)

* [Assign target constraints to campaigns, and unassign target constraints from campaigns](#campaign-target-constraints)

* [Assign label classifications to campaigns, and remove label classifications from campaigns](#campaign-classifications)

* [Manage data view reports from the [!UICONTROL Campaigns] view](#campaign-reports)

## Create a campaign {#campaign-create}

>[!NOTE]
>
>* Before you create a campaign, [implement conversion tracking tags](/help/search-social-commerce/tracking/conversion-tracking-about.md) in the advertiser's webpages.
>* To create a large number of campaigns at once, use<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [campaign bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. Click **[!UICONTROL Create Campaign]**.

1. Specify the [Baidu](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md), or [Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md) campaign settings.

1. Click **[!UICONTROL Review and Save]**.

1. If necessary, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit") **[!UICONTROL Edit]** and change the campaign settings.

1. Click **[!UICONTROL Create]**.

Depending on the ad network on which the campaign was created, you may need to create associated ad groups and ads before the campaign is pushed to the ad network.

## Rename a campaign {#campaign-rename}

Quickly rename a campaign without opening the full campaign settings.

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. Hold the cursor over the campaign row and click **[!UICONTROL ...] > [!UICONTROL Rename]**.

1. Edit the name, and then click **[!UICONTROL Apply]**.

## Edit campaign settings {#campaign-edit}

You can edit settings for individual campaigns. You can also edit some fields for multiple campaigns at once, including some campaign details, budget options, and URL options that are common to all of the selected campaigns.

>[!TIP]
>
>You can also edit data in bulk using <!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [campaign bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. Do either of the following:

   * Hold the cursor over the entity name and click **[!UICONTROL ...] > [!UICONTROL Edit]**.
   
   * Select the check box next to the campaign. In the bulk actions toolbar, click **[!UICONTROL Edit]**.
 
1. Edit the [Baidu](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md), <!-- [Meta Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-meta.md), --> [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md), or [Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md) campaign settings.

1. Click **[!UICONTROL Review and Save]**.

1. If necessary, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit") **[!UICONTROL Edit]** and change the campaign settings.

1. Click **[!UICONTROL Update]**.

Depending on the ad network on which the campaign was created, the campaign may need to include ad groups and ads before it is pushed to the ad network.

## Change the status of a campaign {#campaign-status}

Quickly change the status of a campaign without opening the full campaign settings.

You can pause any active campaign on a supported ad network to disable bidding on it. You can later resume bidding by changing the status back to active.

You also can delete any active or paused campaign. Deleted campaigns are deleted from the ad network. They're still visible when you include them in the data filter, but you can't change them.

### Activate or pause a campaign

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. Hold the cursor over the campaign row and click ![Edit](/help/search-social-commerce/assets/edit.png "Edit") next to the [!UICONTROL Status] column.
   
1. Change the status:

   * To activate a paused campaign, select **[!UICONTROL Active]**.

   * To pause an active campaign, select **[!UICONTROL Paused]**.

### Delete a campaign

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. Do either of the following:

   * Hold the cursor over the campaign row and click **[!UICONTROL ...] > [!UICONTROL Delete]**.

   * Hold the cursor over the campaign row and click ![Edit](/help/search-social-commerce/assets/edit.png "Edit") next to the [!UICONTROL Status] column. Select **[!UICONTROL Deleted]**.

## Assign campaigns to a portfolio {#campaign-portfolio}

Assigning a campaign to an optimized portfolio allows Search, Social, & Commerce to optimize bids, campaign budgets, and bid strategy targets for keywords and ads in the campaign. You can assign campaigns to a portfolio from the [!UICONTROL Campaigns] view, when you create the portfolio, or by editing a portfolio's settings.

Not all campaign types and ad networks are eligible for optimization; see a list of [supported campaign types](/help/search-social-commerce/introduction/supported-inventory.md) that you can include in a portfolio. In addition, verify the [optimization support for each campaign bid strategy](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

>[!NOTE]
>
>Each campaign can be assigned to only one portfolio. If you assign a campaign that's already associated with another portfolio to a new portfolio, then it's removed from the original portfolio.

### Assign campaigns to an existing portfolio from the [!UICONTROL Campaigns] view

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. Select the check box next to each campaign to assign to a single portfolio.

1. In the bulk actions toolbar, click **+ [!UICONTROL Assign]** > **[!UICONTROL Existing Portfolio]** .

1. Select the portfolio.

1. Click **[!UICONTROL Assign Now]**.

### Assign campaigns to a new portfolio from the [!UICONTROL Campaigns] view

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. Select the check box next to each campaign for which you want to create the new portfolio.

1. In the bulk actions toolbar, click **+ [!UICONTROL Assign]** > **[!UICONTROL New Portfolio]**.

1. In the [!UICONTROL Create Portfolio] screen, specify the portfolio settings.

   The campaigns you selected previously are already assigned to the campaign. You can optionally edit the campaign list for the portfolio.

   For more information about the portfolio settings, see the Optimization Guide, which is available from within Search, Social, & Commerce.

1. Click **[!UICONTROL Review and Save]**.

### Change campaign assignments for a portfolio from the [!UICONTROL Portfolios] view

When you remove a campaign from a portfolio, Search, Social, & Commerce can't optimize bids, campaign budgets, and bid strategy targets for that campaign.

The action is logged in the portfolio's change history.

For more information about optimization, see the Optimization Guide, which is available from within Search, Social, & Commerce.

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Portfolios]**.

1. Select the check box next to the portfolio.

1. In the bulk actions toolbar, click **[!UICONTROL Edit]**.

1. In the portfolio settings, go to the [!UICONTROL Assign Campaigns] section and change the campaign assignments.

   For more information about the portfolio settings, see the Optimization Guide, which is available from within Search, Social, & Commerce.

1. Click **[!UICONTROL Review and Save]**.

1. Review the settings and make changes as necessary, and then click **[!UICONTROL Save]**.

## Manage bid constraint assignments for campaigns {#campaign-constraints}

Each entity can have only one constraint. Constraints are inherited by child entities, so you don't need to assign constraints for child entities unless you want to override the inherited values.

Unassigning a constraint removes the association with the account components and all of their child components, and report data for the constraint is no longer available for those components. Unassigning a constraint doesn't delete the constraint nor the account components themselves.

>[!NOTE]
>
>Active constraints restrict bidding only for assigned bid units in optimized legacy keyword-level portfolios. They're ignored for bid units that are in active portfolios, are in hybrid portfolios, or aren't in portfolios. 

### Assign a bid constraint to selected campaigns from the new [!UICONTROL Campaigns] view

You can assign a single constraint to one or more campaigns.

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. Select the check box next to each campaign to which you'll assign a single constraint.

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

### Remove bid constraints from selected campaigns from the new [!UICONTROL Campaigns] view

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. Select the check box next to each campaign from which you'll unassign constraints.

1. In the bulk actions toolbar, click **- [!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Click **[!UICONTROL Confirm]**.

### Remove bid constraints from search bid units from the legacy [!UICONTROL Campaigns] views

>[!NOTE]
>
>To delete a constraint, making it unavailable for future use, see "Delete constraints for search bid units" in the Optimization Guide chapter on "Bid Constraints," which is available from within Search, Social, & Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. In **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**, select the account component view.

1. Select the check box next to each component from which you want to remove the constraint.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click **[!UICONTROL More]**, and then click **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. In the confirmation dialog, select **[!UICONTROL Yes, Unassign]**.

## Manage target constraint assignments for campaigns {#campaign-target-constraints}

### Assign a target constraint to selected campaigns from the new [!UICONTROL Campaigns] view

You can assign a single target constraint to one or more campaigns.

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. Select the check box next to each campaign to which you'll assign a single target constraint.

1. In the bulk actions toolbar, click **+ [!UICONTROL Assign]** > **[!UICONTROL Target Constraint]**.

1. Select the constraint.

1. Click **[!UICONTROL Assign Now]**.

### Remove target constraints from selected campaigns from the new [!UICONTROL Campaigns] view

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. Select the check box next to each campaign from which you'll unassign a target constraint.

1. In the bulk actions toolbar, click **- [!UICONTROL Unassign]** > **[!UICONTROL Target Constraint]**.

1. Click **[!UICONTROL Confirm]**.

## Assign label classifications to campaigns {#campaign-classifications}

>[!NOTE]
>
>Label values are inherited by child entities, so don't enter values for child entities unless you want to override the inherited values.

### Assign classification values to campaigns

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. Select the check box next to each campaign to which you'll assign a label value.

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

### Remove label classification values from campaigns

Removing a classification value removes the association with the account component and all of its child components. Report data for the classification value is no longer available for those components. Removing a classification value doesn't delete the value nor the account components.

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. Select the check box next to each campaign from which you'll remove a label value.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Select the check box next to each classification value to remove from the selected entities.

   To select all assigned values, click **[!UICONTROL Select All]**. To deselect all assigned valued, click **[!UICONTROL Deselect All]**.

1. Click **[!UICONTROL Unassign Selected]**.

## View a performance graph in the [!UICONTROL Campaigns] view {#campaign-performance-graph}

Open and configure a performance graph with up to three metrics totalled across all campaigns in the view for the specified date range.

### View a performance graph

1. Above the data table, click ![Charts](/help/search-social-commerce/assets/charts.png "Charts").

1. (Optional) Specify the currency and up to three metrics to include in the chart.

### Hide a visible performance graph

* Above the data table, click ![Charts](/help/search-social-commerce/assets/charts.png "Charts").

## Manage data view reports from the [!UICONTROL Campaigns] view {#campaign-reports}

<!-- Wording??????  Filtered data reports? -->

Generate a report that includes the data rows for one or more campaigns in the [!UICONTROL Campaigns] view, and then download the report as a Microsoft Excel worksheet file (XLXS format). The report includes all visible columns in the view.

You can delete any generated report.

See also ">* [(Legacy UI) Download data from a campaign management view](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)" and "[(Legacy UI) Delete a performance data report or bulksheet file from the [!UICONTROL Downloads] menu](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)."

### Generate a report with the filtered data rows

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. Specify the campaigns whose data you want to download:

   * To download data for specific campaigns, select the check boxes next to the campaigns.
   
   * To download data for all campaigns, you don't need to select any check boxes. All campaigns are included by default.

1. In the toolbar above the data table, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report") **[!UICONTROL Reports]**.

1. In the [!UICONTROL Grid Reports] settings, enter a unique report name, and then click **[!UICONTROL Generate]**.

   By default, the file is named "campaign_YYYYMMDD_NNNN," where "NNNN" is the sequential job number (such as "campaign_20250402_1326).

   The file is added to the [!UICONTROL Recently Generated] list.

1. (Optional) To download the file once it's completed, click ![Download](/help/search-social-commerce/assets/download.png "Download") next to the file name.

   The file is downloaded according to your browser's normal procedure.

### Download a completed report

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. In the toolbar above the data table, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report") **[!UICONTROL Reports]**.

1. In the [!UICONTROL Recently Generated] list in the [!UICONTROL Grid Reports] dialog, click ![Download](/help/search-social-commerce/assets/download.png "Download") next to the file name.

   The file is downloaded according to your browser's normal procedure.

### Delete a completed report

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Campaigns]**.

1. In the toolbar above the data table, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report") **[!UICONTROL Reports]**.

1. In the [!UICONTROL Recently Generated] list in the [!UICONTROL Grid Reports] dialog, click ![Delete](/help/search-social-commerce/assets/delete-new.png "Delete") next to the file name.

>[!MORELIKETHIS]
>
>* [Manage constraints for search bid units](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Manage constraint assignments for ad groups](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [Manage constraint assignments for keywords](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [Manage constraint assignments for placements](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [(Legacy UI) Download data from a campaign management view](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [(Legacy UI) Delete a performance data report or bulksheet file from the [!UICONTROL Downloads] menu](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md)
>* [[!DNL Google Ads] campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md)
>* [[!DNL LY Ads] campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md)
>* [[!DNL Microsoft Advertising] campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md)
>* [[!DNL Yandex] campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md)

<!-- >* [[!DNL Meta Ads] campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-meta.md) -->

