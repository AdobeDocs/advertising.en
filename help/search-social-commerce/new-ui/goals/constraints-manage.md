---
title: Manage constraints for search bid units
description: Learn about constraints to restrict bids for bid units in CPC campaigns in legacy keyword-level portfolios.
feature: Search Campaign Management, Search Optimization
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: c800239a-06eb-4249-9aef-771973d24d35
    internal-label: Portfolios
---
# Manage constraints for search bid units

*Applicable for bid units in CPC campaigns in legacy keyword-level portfolios only*

Bid unit constraints are rules that restrict optimized bids for all [bid units](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/glossary.html) with cost and revenue models that are associated with the constraint.

## About constraints

Each constraint applies to a specific currency and optionally includes triggering conditions that must be met during a specified data evaluation period in order for the rule to apply. The data to be evaluated can include channel type, match type, click data, conversion data, or derived metrics. For example, you can restrict bids to a specific monetary range, continuously increase or decrease bids by a specified amount, or bid according to the average bid for the portfolio. Each constraint has an applicable start date and either expires on a specific date or is applied indefinitely.

After you set up a constraint, you can assign it to specific bid units or to all bid units within specific ad groups or campaigns. Each bid unit can have one constraint. Constraints are inherited by child entities but can be overridden. A constraint assigned at the lowest level always overrides a constraint assigned at a parent level. When you assign a constraint to a bid unit, bidding operates within the specified constraints for that bid unit, regardless of how much revenue the bid unit generates, when the bid unit has cost and revenue models.

>[!CAUTION]
>
>When you assign constraints to a bid unit, you override the bid optimization system's decision and assume responsibility for the ROI on that bid unit yourself.

>[!NOTE]
>
>* Active constraints restrict bidding only for assigned bid units in optimized legacy keyword-level portfolios. They're ignored for bid units that are in hybrid portfolios, are in active portfolios, or aren't in portfolios. **Tip:** In the portfolio settings, turn on the portfolio option to "'Auto adjust campaign budget limits." The recommended "Multiple" value is "1."
>* Bid constraints are ignored for bid units without enough data to generate cost and revenue models.
>* (Campaigns with a CPC or eCPC bid strategy) When a bid constraint conflicts with a portfolio-level bid limit, the constraint overrides the portfolio-level limit. For example, if a portfolio's minimum bid is 5 USD but you constrain a bid unit in the portfolio to a minimum bid of 3 USD, then the bid unit is bid to 3 USD or higher. Overall spending for constrained bid units, however, is determined by the portfolio's ["Spend Around Constraints" parameter](#spend-around-constraints).
>* Constraints operate on the base bid. Any type of bid adjustment to the base bid (such as raising the bid for end users on mobile devices) may move the bid outside of the allowable range for the constraint. For example, if the constraint requires a maximum CPC of 6 USD, the base bid is already 6 USD, and the portfolio auto-optimizes bid adjustments for mobile devices at 50%-60%, then the maximum CPC is 9.00-9.60 USD &mdash; not 6 USD.

### Constraint types {#constraint-types}

* **[!UICONTROL Bid]:** Restricts bids to a monetary range.

* **[!UICONTROL Bid Shift]:** Continuously changes the optimized bids for all associated bid units by a specified amount, within bidding bounds. A bid shift causes the relevant portfolios to over- or under-spend by the total amount caused by the bid shift, regardless of the portfolio's setting for "Spend Around Constraints." Note: If the current CPC bid is already equal to or greater than the Max Bid, or equal to or lower than the Min Bid, then the constraint is ignored and the bid isn't changed. Also, bid shift constraints aren't applied to bid units without enough data to generate cost and revenue models.

* **[!UICONTROL Incremental Bidding]:** (Applicable only to keywords with no impressions) Increases or decreases the bid incrementally at a specified rate until the bid reaches a designated target.

* **[!UICONTROL Search Engine Min Bid]:** ([!DNL Google Ads] accounts only) Uses the minimum CPC bids determined by the search engine as your minimum bids. As the search engine changes its minimum bids, your bid changes accordingly. You can optionally specify additional bid limits for all associated bid units.

* **[!UICONTROL Impression Share]:** ([!DNL Google Ads] and [!DNL Microsoft Advertising] CPC campaigns with exact match only) Restricts bids to a monetary range when the ads are between a minimum and maximum impression share. **Note:** When the constraint isn't cost-efficient, the optimization capability may override it.

### When to apply constraints

Some reasons to constrain bid units include the following:

* To quickly expose untested keywords and ads.

* To mitigate risks for new portfolios, accounts, campaigns, and ad groups. For example, before you launch a portfolio, you can set maximum bids on high-traffic bid units and then gradually raise the values each day. This allows the bidding model to adjust each day without the risk of big bid increases.

* To make sure that tail keywords with high conversion rates aren't bid down.

* To bid up specific terms that are central to your brand or during promotions.

### Where to view information about constraints within the UI

Besides opening the [[!UICONTROL Constraints] view](#constraints-view), you can also see information related to your constraints in the following ways:

* All of your constraints are label values for a single [label classification](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/label-classifications/classification-about.html) called "[!UICONTROL Constraints]."

  * "[!UICONTROL Constraints]" is included in the "[!UICONTROL Classifications]" list in your default and custom view settings and in scheduled reports. You can add the column wherever you want to see the constraints assigned to the relevant entities.
  
  * When you download a bulksheet, "[!UICONTROL Constraints]" is listed under the "[!UICONTROL Classifications]" column for the applicable entities in the [!UICONTROL Download Bulksheet] dialog. When you include the column, the downloaded bulksheet includes any constraints assigned to the relevant entities.
   
  The [!UICONTROL Constraints] classification isn't included in the [!UICONTROL Label Classifications] view &mdash; the [!UICONTROL Constraints] view is separate. The  [!UICONTROL Constraints] classification also isn't included in the 30-label classification limit.

* [The [!UICONTROL Constraint Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/constraint-report.md) includes cost, click, and (optionally) conversion data for constraints that use the label classification architecture.

### The [!UICONTROL Constraints] view {#constraints-view}

The [!UICONTROL Goals] > [!UICONTROL Constraints] view lists all of your constraints. Available columns include the constraint status; constraint type, start and end dates; the number of campaigns, ad groups, keywords, ads, placements, auto targets, and product groups with which the constraint is associated; impressions, clicks, and cost data; and revenue data for all visible conversion metrics.<!-- Clarify why "Ads" is listed, unless it's to identify the relevant ads -->

>[!IMPORTANT]
>
>The performance data for a row in the [!UICONTROL Constraints] view may not match the performance data for the top-level entity to which the constraint is assigned. Bbecause a constraint assigned at the lowest level always overrides a constraint assigned at a parent level, a constraint assigned to a campaign or ad group may not remain assigned to the child ad groups and keywords. For example, if Campaign A is assigned Constraint A, then all of the ad groups and keywords in Campaign A automatically inherit Constraint A. However, those ad groups and keywords could later be assigned to other constraints, such as Constraint B, and they would then lose their association with Constraint A.

>[!NOTE]
>
>Assign constraints to bid units, and unassign them, from the relevant entity management view (such as from the [!UICONTROL Campaigns] view for campaign-level constraints).

#### Available actions

* [Create a constraint](#constraint-create).

* [Edit constraint settings](#constraint-edit).

* [Change the status of constraints](#constraint-change-status).

## Create a constraint {#constraint-create}

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Constraints]**.

1. In the upper right toolbar above the data table, click **[!UICONTROL Create Constraint]**.

1. Enter the [constraint settings](#constraint-settings).

   To move between the [!UICONTROL Constraint Type] tab and the [!UICONTROL Conditions] tab, either click the tab that you want to open or click the [!UICONTROL Next] and [!UICONTROL Back] buttons.

1. Click **[!UICONTROL Review and Save]** to review the settings.

1. Click **[!UICONTROL Save]**.

Once you create a constraint, you can [assign it](#constraint-assign) to campaigns, ad groups, keywords, placements, and unit-level product groups.

## Edit constraint settings {#constraint-edit}

You can edit the settings for one constraint at a time.

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Constraints]**.

1. (Optional) Filter the list [from the toolbar](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) or from a [column heading](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Select the check box next to the constraint you want to edit.

1. In the bulk actions toolbar, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit").

1. Edit the [constraint settings](#constraint-settings).

   To move between the [!UICONTROL Constraint Type] tab and the [!UICONTROL Conditions] tab, either click the tab that you want to open or click the [!UICONTROL Next] and [!UICONTROL Back] buttons.

1. Click **[!UICONTROL Review and Save]** to review the settings.

1. Click **[!UICONTROL Save]**.

## Change the status of constraints {#constraint-change-status}

You can pause any active constraint to disable it. You can later enable it by changing the status back to *active*.

You also can delete a constraint, which removes all associations with account components and makes the constraint unavailable for future use. Report data for the constraint is longer available. **Note:**  To simply disassociate a constraint from an account component, see "[Remove constraints from search bid units](#constraints-unassign)."

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Constraints]**.

1. (Optional) Filter the list [from the toolbar](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) or from a [column heading](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Select the check box next to each constraint whose status to want to change.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click the status button:

   * To activate all selected rows, click ![Activate](/help/search-social-commerce/assets/activate-new.png "Activate").

   * To pause all selected rows, click ![Pause](/help/search-social-commerce/assets/pause-new.png "Pause").

   * To delete all selected rows, click ![Delete](/help/search-social-commerce/assets/delete-new.png "Delete").
   
1. In the confirmation message, click **[!UICONTROL Confirm]**.

## Constraint settings {#constraint-settings}

| Tab | Parameter | Description |
|---|---|---|
| \[Basic information\] | [!UICONTROL Constraint Name] | A unique name for the constraint. |
| | [!UICONTROL Currency] | The currency in which any applicable bid units are bid. Bid units for which a different currency is used are ignored. |
| | [!UICONTROL Status] | The status of the constraint:<ul><li>**Active:** (The default) The constraint is applied during the specified conditions and date range.</li><li>**Paused:** The constraint isn't applied.</li></ul> |
| [!UICONTROL Constraint Type] | [!UICONTROL Constraint Type] | The type of constraint. For descriptions of the constraint types and the eligible ad networks for each, see "[Constraint types](#constraint-types)." |
| | [!UICONTROL Start Date] | The first day on which the constraint takes effect. The default is the current day. To change the date, enter a date or click ![Calendar](/help/search-social-commerce/assets/calendar-new.png "Calendar") to open the calendar and select a date. |
| | [End Date] | Whether the constraint will become ineffective on a specific date. To apply the constraint indefinitely, such as when the bid unit is central to the company's brand, leave the field empty. To end the constraint on a specific date, enter a date or click ![Calendar](/help/search-social-commerce/assets/calendar-new.png "Calendar") to open the calendar and select a date. **Note:**  The constraint can't expire before tomorrow. |
| | [!UICONTROL Set constraint options for Bid] | ([!UICONTROL Bid] constraints only) Settings include:<ul><li>**[!UICONTROL Min Bid]:** The minimum base bid for associated bid units.</li><li>**[!UICONTROL Max Bid]:** The maximum base bid for associated bid units.</li></ul> |
| | [!UICONTROL Set constraint options for Bid Shift] | ([!UICONTROL Bid Shift] constraints only) The type and amount of bid shift to continuously apply to the base bid:<ul><li>*[!UICONTROL Increases]:* Increases bids by a specified percentage or currency value. Enter the amount to change, and then select either *$* or *%*. Also enter a **[!UICONTROL Max Limit]**, which is the highest possible bid (ceiling) when the constraint is applied. **Note:** If the current CPC bid is already equal to or greater than the [!UICONTROL Max Limit], then the constraint is ignored and the bid isn't changed.</li><li>*[!UICONTROL Decreases]:* Decreases bids by a specified percentage or currency value. Enter the amount to change, and then select either *$ or %*. Also enter a **[!UICONTROL Min Limit]**, which is the lowest possible bid (floor) when the constraint is applied. **Note:** If the current CPC bid is already equal to or less than the [!UICONTROL Min Limit], then the constraint is ignored and the bid isn't changed.</li></ul>**Notes:**<ul><li>A bid shift will cause the relevant portfolios to over- or under-spend by the total amount caused by the bid shift, regardless of the portfolio's setting for "[!UICONTROL Spend Around Constraints]."</li><li>If you specify an end date for the constraint and the optimization capability is automatically adjusting spending limits for the campaigns in the portfolio, then the bids don't simply revert to the original amounts after the end date but are adjusted as optimal.</li><li>Bid shifts aren't applied to bid units without enough data to generate cost and revenue models.</li></ul> |
| | [!UICONTROL Set constraint options for Incremental Bidding] | ([!UICONTROL Incremental Bidding] constraints only) A bid target, and how much and how often to increase or decrease the bid incrementally until it reaches the target:<ul><li>**[!UICONTROL Bid target]:** The target bid amount.</li><li>**[!UICONTROL Incrementally change bids by]** and **[Type]:** How much to incrementally increase or decrease bids, and whether to change bids by a currency value (**$**) or percentage (*%*).</li><li>**[!UICONTROL Every __ days]:** How often to increment bids.</li></ul>For example, say that the current bid for one of the keywords is 100 cents and that you want to change the bid by 10% every day until you reach a bid target of 500 cents. On Day 1 after the constraint is set, the bid for that keyword is 110 cents (current bid + 10%). On Day 2, the bid is 120 cents (current bid for Day 1 + 20%), and so on. However, if the bid target is 50 cents and the other parameters are the same, then the bids incrementally decrease until the bid reaches 50 cents. |
| | [!UICONTROL Set constraint options for Search Engine Min Bid] | ([!UICONTROL Search Engine Min Bid] constraints) Uses the minimum bid required to show a bid unit on the first page of search results on Google ([!UICONTROL Google First Page CPC]). Optionally enter a **[!UICONTROL Min Bid]** value and/or a **[!UICONTROL Max Bid]** value to define the range of eligible bids for the constraint. For example, if you specify a [!UICONTROL Min Bid] of 2.50 USD and a [!UICONTROL Max Bid] of 4 USD, then you won't bid on the bid unit if the [!DNL Google Ads] first page bid is below 2.50 USD or above 4 USD. |
| | [!UICONTROL Set constraint options for Impression Share] | ([!UICONTROL Impression Share] constraints only) Settings include:<ul><li>**[!UICONTROL Min Bid]** (Optional) The minimum base bid for associated bid units.</li><li>**[!UICONTROL Max Bid]:** (Optional) The maximum base bid for associated bid units.</li><li>**[!UICONTROL Min Impression Share]:** The lowest impression share, as a percent, that will trigger the constraint for the applicable bid units. It must be between 10 and 90. **Note:** When the constraint isn't cost-efficient, the optimization capability may override it.</li><li>**[!UICONTROL Max Impression Share]:** The highest impression share, as a percent, that will trigger the constraint for the applicable bid units. It must be between 10 and 90.**Note:** When the constraint isn't cost-efficient, the optimization capability may override it.</li></ul>> |
| [!UICONTROL Conditions] | [!UICONTROL Condition Type] | Whether to apply conditions to the constraint:<ul><li>*[!UICONTROL No Condition]:* (the default) The constraint is applied unconditionally during the specified date range.</li><li>*[!UICONTROL Satisfy]:* The constraint is applied only when specified conditions are met during a specified data evaluation period.</li></ul> |
| | [!UICONTROL Data Evaluation Period] | (When conditions are set) The time period for which to valuate data for the specified criteria. If you select *[!UICONTROL Custom date range],** specify the **[!UICONTROL Start Date]** and the **[!UICONTROL End Date]** by entering each date in the format `MM-DD-YYYY` (such as 03-29-2026 for March 29, 2026) or by clicking ![Calendar button](/help/search-social-commerce/assets/calendar-new.png "Calendar button") to open the calendar and selecting each date. |
| | [!UICONTROL When to Apply Constraints] | (When conditions are set) How many filter conditions must be met to apply the constraint:<ul><li>*[!UICONTROL Match All Filters]:* Applies the constraint when every specified filter condition is met.</li><li>*[!UICONTROL Match Any Filters]:* Applies the constraint when at least one of the specified filter conditions is met.</li></ul> |
| | [!UICONTROL Filters] | (When conditions are set) One or more criteria that must be met. To create a filter, select a property or metric from the list. For properties (such as [!UICONTROL Channel Type]), select the applicable values in the list. For metrics (such as [!UICONTROL Clicks]), select an operator, and then enter the applicable value. For example, to return only bid units with more than 100 clicks, select **Clicks**, select **greater than**, and then enter `100` in the input field.</li></ul> |

## Assign constraints to search bid units {#constraint-assign}

You can apply bid unit constraints to any campaign, ad group, keyword, placement, or dynamic search target (auto target).

Each entity can have only one constraint. You can assign a single constraint to one or more entities at the same time.

>[!NOTE]
>
>* If you later edit a keyword or the ad copy for an ad &mdash; thereby creating a new keyword or ad &mdash; then the constraint isn't assigned to the new entity.
>* See the same instructions within the [[!UICONTROL Campaigns] view](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md), [[!UICONTROL Ad Groups] view](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md), [[!UICONTROL Keywords] view](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md), or [[!UICONTROL Placements] view](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md). <!-- ADD LINK WHEN AVAILABLE for dynamic search targets (auto targets). -->

1. From the main menu, open the relevant management view.

   For example, to assign constraints at the campaign level, go to [!UICONTROL Manage] > [!UICONTROL Campaigns].

1. (Optional) Filter the list [from the toolbar](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) or from a [column heading](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Select the check box next to each entity to which you'll assign a single constraint.

1. In the bulk actions toolbar, click **+ [!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Select the constraint.

1. Click **[!UICONTROL Assign Now]**.

## Unassign constraints from search bid units {#constraints-unassign}

>[!NOTE]
>
>* To delete a constraint, making it unavailable for future use, see "[Change the status of constraints](#constraint-change-status)."
>* See the same instructions within the [[!UICONTROL Campaigns] view](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md), [[!UICONTROL Ad Groups] view](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md), [[!UICONTROL Keywords] view](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md), or [[!UICONTROL Placements] view](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md). <!-- ADD LINK WHEN AVAILABLE for dynamic search targets (auto targets). -->

1. In the main menu, open the relevant management view.

   For example, to unassign campaign-level constraints, go to [!UICONTROL Manage] > [!UICONTROL Campaigns].

1. Select the check box next to each entity from which you'll unassign constraints.

1. In the bulk actions toolbar, click **- [!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Click **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [Manage constraint assignments for campaigns](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [Manage constraint assignments for ad groups](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [Manage constraint assignments for keywords](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [Manage constraint assignments for placements](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [The [!UICONTROL Constraint Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/constraint-report.md)
