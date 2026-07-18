---
title: Manage [!DNL Google Ads] dynamic search targets
description: Learn how to create and manage [!DNL Google Ads] dynamic search targets.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
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

## The [!UICONTROL Auto Targets] view

The [!UICONTROL Auto Targets] view lists all dynamic search targets in the filtered view for the selected advertiser account.

You can create, edit, and change the status of dynamic search targets in the [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Auto Targets] view.

You also can [apply a label](/help/search-social-commerce/campaign-management/label-classifications/classification-values-assign-campaign-management.md) to any target.

### Available actions

<!--
* Create a dynamic search target

* Edit the settings for a dynamic search target

* Change the status of dynamic search targets
-->

* [Assign constraints to dynamic search targets](#constraint-assign), and [unassign constraints from dynamic search targets](#constraint-unassign)

* [Assign label classifications](#classification-values-assign) to dynamic search targets, and [remove label classifications](#classification-values-remove) from dynamic searchh targets

>[!NOTE]
>
>You can create and edit large amounts of target data (including labels and constraint assignments) at once by uploading [bulksheet files](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) and posting them to the ad network.

<!--
Not available yet:

## Create a [!DNL Google Ads] dynamic search target

You can create dynamic search targets to define pages in your websites (that is, the domains used in your ads' display URLs) whose content is used to target your dynamic search ads in the same ad group.

You can target all criteria or up to three individual criteria.

>[!NOTE]
>
>To best track performance, create an "[!UICONTROL All Targets]" target for only one ad group per campaign.

>[!TIP]
>
>To create many account components at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network, the account, the campaign, and the ad group, and then click **[!UICONTROL Continue]**.

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

1. Click **[!UICONTROL Post]**.

## Edit [!DNL Google Ads] dynamic search target settings

You can edit the status or maximum bid for a [!DNL Google Ads] dynamic search target. You can't change the criteria that are targeted.

>[!TIP]
>
>To edit large amounts of data at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each row to edit.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

   For multiple targets, your changes are applied to all of the selected targets. For the [!UICONTROL Bid field], you have options to change existing values to a specified value or to either increase or decrease the amount by a specified percentage or monetary amount, with a limit.

1. Save the data:

   * (Single targets) Click **[!UICONTROL Post]**.
   
   * (Multiple ad groups) Click **[!UICONTROL Post Now]**.

## Change the status of [!DNL Google Ads] dynamic search targets

You can pause any active dynamic search target in a supported campaign type to stop using them for dynamic search ads in the same ad group. You can later use them as targets by changing the ad status back to active.

You can also delete any dynamic target.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. (Optional) Filter the list to include specific dynamic targets.

1. Do either of the following:
   
   * To change the status of one dynamic target, click in the **[!UICONTROL Status]** column and change the status.
   
   * To delete one or more dynamic targets, do the following:
   
     1.  Select the check box next to each dynamic target you want to delete.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."
     
     1. In the toolbar, click ![More](/help/search-social-commerce/assets/more.png "More") and select **[!UICONTROL Delete]**.
     
     1. In the confirmation message, click **[!UICONTROL Delete]**.

## [!DNL Google Ads] dynamic search target settings {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Required when you don't specify a website domain and language in the campaign's [!UICONTROL DSA Options] section; read-only for existing targets) Dynamic search targets for the ad group:

* *[!UICONTROL All Targets]* (the default): Targets all indexed pages.

* *\[Specific Targets\]:* Targets up to three criteria for the indexed pages. When you select this, you must specify the criteria by specifying information categories and specific values for which to target ads (for example, "URL contains shoes.example.com"). To specify more than one criteria, click **[!UICONTROL + And]**. Target criteria include:

  * *[!UICONTROL Category]:* To show ads for indexed pages with a specific [!DNL Google Ads] content category.

  * *[!UICONTROL URL]:* To show ads for indexed pages with a specific URL, where the value may be included anywhere within the URL.

  * *[!UICONTROL Page Title]:* To show ads for indexed pages with specific text in the page title.

  * *[!UICONTROL Page Content]:* To show ads for indexed pages with specific content.

**Status:** The status of the target settings:

* *[!UICONTROL Active]* (the default): Enables bidding.

* *[!UICONTROL Paused]:* Disables bidding.

* *[!UICONTROL Deleted]* (existing targets only): Deletes the target settings.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** The maximum cost per click (CPC) for an ad or cost per 1000 impressions (CPM) for an ad, as applicable for the ad network and campaign pricing model. This value overrides the ad group-level value.

>[!NOTE]
>
>If the target is in an optimized portfolio, then the specified CPC bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations.

-->

## Assign a constraint to selected dynamic search targets from the new [!UICONTROL Auto Targets] view {#constraint-assign}

1. In the main menu, click **[!UICONTROL Target] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each dynamic search target to which you'll assign a single constraint.

1. In the bulk actions toolbar, click **+ [!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Select the constraint.

1. Click **[!UICONTROL Assign Now]**.

## Unassign constraints from selected dynamic search targets from the new [!UICONTROL Auto Targets] view {#constraint-unassign} 

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each dynamic search target from which you'll unassign constraints.

1. In the bulk actions toolbar, click **- [!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Click **[!UICONTROL Confirm]**.

## Assign classification values to dynamic search targets {#classification-values-assign}

>[!NOTE]
>
>Label values are inherited by child entities, so don't enter values for child entities unless you want to override the inherited values.

1. In the main menu, click **[!UICONTROL Target] > [!UICONTROL Auto Targets]**.

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

## Remove label classification values from dynamic search targets{#classification-values-remove}

Removing a classification value removes the association with the account component and all of its child components. Report data for the classification value is no longer available for those components. Removing a classification value doesn't delete the value nor the account components.

1. In the main menu, click **[!UICONTROL Target] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each dynamic search target from which you'll remove a label value.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Select the check box next to each classification value to remove from the selected entities.

   To select all assigned values, click **[!UICONTROL Select All]**. To deselect all assigned valued, click **[!UICONTROL Deselect All]**.

1. Click **[!UICONTROL Unassign Selected]**.

>[!MORELIKETHIS]
>
>* [(New UI) Manage constraints for search bid units](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(New UI) Manage label classifications](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md)
