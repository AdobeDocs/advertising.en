---
title: Manage constraint assignments for ad groups
description: Learn how to assign constraints to ad groups.
feature: Search Optimization, Search Campaign Management
hide: true
exl-id: c9960b5a-4b6c-4ef0-8501-5478af2c40da
TQID: https://experienceleague.adobe.com/6z4-Pt25RaQpLiEYdnp-BXD0guz9S2zQLmamf8uSSXU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# (New UI) Manage constraint assignments for ad groups

*Beta feature*

You can assign and remove bidding constraints for the following search entities: campaign, ad group, keyword, placement, unit-level product group, and dynamic search target. Each entity can have only one constraint.

Constraints are inherited by child entities, so you don't need to assign constraints for child entities unless you want to override the inherited values.

Unassigning a constraint removes the association with the account components and all of their child components, and report data for the constraint is no longer available for those components. Unassigning a constraint doesn't delete the constraint nor the account components themselves.

## Assign a constraint to selected ad groups from the new [!UICONTROL Ad Groups] view

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ad Groups]**.

1. Select the check box next to each ad group to which you'll assign a single constraint.

1. In the bulk actions toolbar, click **+ [!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Select the constraint.

1. Click **[!UICONTROL Assign Now]**.

## Assign a constraint to selected search bid units from the legacy [!UICONTROL Campaigns] views

1. In **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**, select the account component view.

1. Select the check box next to each relevant row.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click **[!UICONTROL More]**, and then click **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Select the applicable constraint.

1. (Optional) Enter additional details:

   1. Next to [!UICONTROL Additional Details], click **[!UICONTROL Open]** to expand the details.

   1. Enter an optional **[!UICONTROL Project Name]** and/or optional **[!UICONTROL Description]**.

1. Click **[!UICONTROL Save]**.

## Unassign constraints from selected ad groups from the new [!UICONTROL Ad Groups] view

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ad Groups]**.

1. Select the check box next to each ad group from which you'll unassign constraints.

1. In the bulk actions toolbar, click **- [!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Click **[!UICONTROL Confirm]**.

## Unassign constraints from search bid units from the legacy [!UICONTROL Campaigns] views

>[!NOTE]
>
>To delete a constraint, making it unavailable for future use, see "Delete constraints for search bid units" in the Optimization Guide chapter on "Bid Constraints," which is available from within Search, Social, & Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. In **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**, select the account component view.

1. Select the check box next to each component from which you want to remove the constraint.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click **[!UICONTROL More]**, and then click **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. In the confirmation dialog, select **[!UICONTROL Yes, Unassign]**.

>[!MORELIKETHIS]
>
>* [(New UI) Manage constraints for search bid units](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(New UI) Manage constraint assignments for campaigns](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [(New UI) Manage constraint assignments for keywords](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [(New UI) Manage constraint assignments for placements](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
