---
title: Manage [!DNL Google Ads] dynamic search targets
description: Learn how to create and manage [!DNL Google Ads] dynamic search targets.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
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
# Manage [!DNL Google Ads] dynamic search targets

*[!DNL Google Ads] accounts only*

You can create, edit, and change the status of dynamic search targets for [!DNL Google Ads] campaigns that use the search network.

## What are dynamic search targets?

Dynamic search targets define whether the ad network uses all or a subset of the pages in your website to target your dynamic search ads. Configure dynamic search targets at the ad group level; they apply to all dynamic search ads in the same ad group.

Depending on your campaign settings, dynamic search targets may be required or optional:

* You must create dynamic search targets when you don't specify a website domain and language in the campaign's "[!UICONTROL DSA Options]" section.

* You can optionally create dynamic search targets when you specify a website domain and language in the campaign's "[!UICONTROL DSA Options]" section.
  
  [!DNL Google Ads] automatically shows your dynamic search ads based on the content of a website specified with these settings.

To best track performance, configure your campaign with one ad group per dynamic search target, and include an ad group that targets all criteria.

For more information about [!DNL Google Ads] dynamic search ads, see https://support.google.com/google-ads/answer/2471185.

## The [!UICONTROL Auto Targets] view {#auto-target-view-about}

The [!UICONTROL Targeting] > [!UICONTROL Auto Targets] view lists all dynamic search targets in the filtered view for the selected advertiser account. You can also manage your dynamic search targets.

Viewing the data requires the [!UICONTROL View Auto Targets] permission. Creating targets and editing their bids or status requires the [!UICONTROL Edit Auto Targets] permission.

### Available actions

* [Create a dynamic search target](#auto-target-create)

* [Edit the settings for dynamic search targets](#auto-target-edit)

* [Change the status of, or delete, dynamic search targets](#auto-target-status)

* [Copy all data in selected rows to your clipboard](#copy-to-clipboard)

* [Assign constraints](#constraint-assign) to dynamic search targets, and [remove constraints](#constraint-unassign) from dynamic search targets

* [Assign label classifications](#classification-values-assign) to dynamic search targets, and [remove label classifications](#classification-values-remove) from dynamic search targets

>[!NOTE]
>
>You can create and edit large amounts of target data (including labels and constraint assignments) at once by uploading [bulksheet files](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) and posting them to the ad network.

## Create a [!DNL Google Ads] dynamic search target {#auto-target-create}

You can create dynamic search targets to define pages in your websites (that is, the domains used in your ads' display URLs) whose content is used to target your dynamic search ads in the same ad group.

You can target all indexed pages or specify up to three criteria.

>[!NOTE]
>
>To best track performance, create a target with the [!UICONTROL All] option for only one ad group per campaign.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Auto Targets]**.

1. Above the data table, click **[!UICONTROL Create Auto Target]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network, account, campaign, and ad group.

1. Specify the remaining [dynamic search target settings](#auto-target-create-settings).

1. Click **[!UICONTROL Review and Save]**.

1. Review the settings. To change any settings, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit") **[!UICONTROL Edit]** in the applicable section and change the settings.

1. Click **[!UICONTROL Create]**.

## Edit [!DNL Google Ads] dynamic search target settings {#auto-target-edit}

You can edit the status or maximum bid for one or more dynamic search targets. You can't change the criteria that are targeted.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each row to edit.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click **[!UICONTROL Edit]**.

1. In the **[!UICONTROL Edit Auto Targets]** panel, edit the [status and bid settings](#auto-target-edit-settings).

   Your changes are applied to all selected targets. Settings that you don't change retain their existing values.

   When the selected targets use multiple currencies, bid editing is disabled. You can still change their status.

1. Click **[!UICONTROL Save]**.

You can also edit a single target's bid directly in the data table by clicking its bid value.

## Change the status of, or delete, [!DNL Google Ads] dynamic search targets {#auto-target-status}

You can pause an active dynamic search target to stop using it for dynamic search ads in the same ad group. You can later resume using the target by changing its status back to active. You can also delete dynamic search targets.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Auto Targets]**.

1. (Optional) Filter the list to include specific dynamic search targets.

1. Do either of the following:
   
   * To change the status of one target, click its value in the **[!UICONTROL Status]** column and select **[!UICONTROL Active]** or **[!UICONTROL Paused]**.
   
   * To change the status of multiple targets, select the check box next to each target, click **[!UICONTROL Edit]** in the bulk actions toolbar, select the **[!UICONTROL Status]** in the **[!UICONTROL Edit Auto Targets]** panel, and then click **[!UICONTROL Save]**.

   * To delete one or more targets, select the check box next to each target, click **[!UICONTROL ...] > [!UICONTROL Delete]** in the bulk actions toolbar, and then click **[!UICONTROL Confirm]** in the confirmation message.

## Copy all data in selected rows to your clipboard {#copy-to-clipboard}

Copy the visible information in selected rows, according to the applied filters and columns visible in the view. The information is saved as tab-separated values (TSV).

1. Select the check box next to each row whose data you want to copy.

1. In the bulk actions toolbar, click **[!UICONTROL Copy]**.

## Manage constraint assignments for dynamic search targets {#constraints}

### Assign a constraint to dynamic search targets {#constraint-assign}

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each dynamic search target to which you'll assign a single constraint.

1. In the bulk actions toolbar, click **+ [!UICONTROL Assign]** > **[!UICONTROL Bid Constraint]**.

1. Select the constraint.

1. Click **[!UICONTROL Assign Now]**.

### Remove constraints from selected dynamic search targets {#constraint-unassign}

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each dynamic search target from which you'll unassign constraints.

1. In the bulk actions toolbar, click **- [!UICONTROL Unassign]** > **[!UICONTROL Bid Constraint]**.

1. Click **[!UICONTROL Confirm]**.

## Manage classification values for dynamic search targets {#classification-values}

### Assign classification values to dynamic search targets {#classification-values-assign}

>[!NOTE]
>
>Label values are inherited by child entities, so don't enter values for dynamic search targets unless you want to override the inherited values.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each dynamic search target to which you'll assign a label value.

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

### Remove label classification values from dynamic search targets {#classification-values-remove}

Removing a classification value removes the association with the account component and all of its child components. Report data for the classification value is no longer available for those components. Removing a classification value doesn't delete the value nor the account components.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each dynamic search target from which you'll remove a label value.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Select the check box next to each classification value to remove from the selected entities.

   To select all assigned values, click **[!UICONTROL Select All]**. To deselect all assigned values, click **[!UICONTROL Deselect All]**.

1. Click **[!UICONTROL Unassign Selected]**.

## [!DNL Google Ads] dynamic search target settings {#dynamic-search-target-settings}

### Settings available during creation {#auto-target-create-settings}

#### [!UICONTROL Auto Target Details]

**Auto-Targets:** The indexed pages whose content is used to target the dynamic search ads in the ad group:

* *[!UICONTROL All]* (the default): Targets all indexed pages.

* *[!UICONTROL Specific]:* Targets pages that match up to three criteria. Select a criterion and enter its value. To add another criterion, click **[!UICONTROL And]**. The criteria are combined with AND, so a page must match all specified criteria. Click **[!UICONTROL Reset]** to clear the criteria.

  * *[!UICONTROL Category]:* The page's [!DNL Google Ads] content category equals the specified value. Enter a value.

  * *[!UICONTROL URL]:* The page's URL contains the specified value, such as `shoes.example.com`. Enter a valid URL.

  * *[!UICONTROL Page Title]:* The page title contains the specified text. Enter a value.

  * *[!UICONTROL Page Content]:* The page content contains the specified text. Enter a value.

You can't change the target criteria after creating the target.

**[!UICONTROL Status]:** The status of the target:

* *[!UICONTROL Active]* (the default): Enables bidding.

* *[!UICONTROL Paused]:* Disables bidding.

**[!UICONTROL Bid]:** The maximum cost per click (CPC) for the target. This value overrides the ad group-level bid. The field is optional; when you enter a bid, the minimum value is 0.01 in the account currency.

>[!NOTE]
>
>If the target is in an optimized portfolio, then the specified CPC bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations.

### Settings available during editing {#auto-target-edit-settings}

#### [!UICONTROL Auto Target Details]

**[!UICONTROL Status]:** Select **[!UICONTROL Active]** or **[!UICONTROL Paused]**.

#### [!UICONTROL Bid details]

Bid editing is disabled when the selected targets use multiple currencies.

**[!UICONTROL Bid adjustment]:** How to change the maximum bids:

* *[!UICONTROL Set to]:* Replace each bid with the amount in [!UICONTROL Set value].

* *[!UICONTROL Increase]:* Increase each bid by the amount or percentage in [!UICONTROL Set value].

* *[!UICONTROL Decrease]:* Decrease each bid by the amount or percentage in [!UICONTROL Set value].

**[!UICONTROL Modifier type]:** (For [!UICONTROL Increase] and [!UICONTROL Decrease]) Select **[!UICONTROL Currency]** or **[!UICONTROL Percentage]**.

**[!UICONTROL Set value]:** The new bid, or the amount or percentage by which to change each bid. The minimum value is 0.01.

**[!UICONTROL Max limit]:** (Optional; for [!UICONTROL Increase] and [!UICONTROL Decrease]) A limit in the account currency. For an increase, this is the maximum resulting bid. For a decrease, this is the minimum resulting bid. When you enter a limit, the minimum value is 0.01.

>[!MORELIKETHIS]
>
>* [(New UI) Manage constraints for search bid units](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(New UI) Manage label classifications](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
