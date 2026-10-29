---
title: Manage keywords
description: Learn how to create and manage biddable and negative keywords and assign constraints to keywords.
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
---
# Manage keywords

*Beta feature*

*[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising], [!DNL Yandex], and existing [!DNL Baidu] accounts only*

A keyword is a word or phrase associated with an ad. Keyword settings include the keyword match type, the maximum bids to be used when your ad is triggered by the keyword, and (for some ad networks) optional tracking parameters. Keyword-level settings override the ad group or campaign settings. Negative keywords prevent ads from being displayed for matching searches.

Once you [make an ad network account accessible via an API connection](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md) and Search, Social, & Commerce has synchronized the account data with the ad network, you can create keywords for search ad groups in [supported campaign types](/help/search-social-commerce/introduction/supported-inventory.md). You also can edit and change the status of keywords, and create and delete negative keywords.

For details about the functionality available for each ad network, see "[Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md)."

## About the [!UICONTROL Keywords] view {#keyword-view-about}

The [!UICONTROL Manage] > [!UICONTROL Keywords] view includes two tabs for the selected advertiser account:

* The [!UICONTROL Keywords] tab lists all biddable keywords in the filtered view.

* The [!UICONTROL Negatives] tab lists all negative keywords in the filtered view.

### Available actions

* [Create keywords](#keyword-create)

* [Create negative keywords](#keyword-negative-create)

* [Edit keyword settings](#keyword-edit)

* [Change the status of, or delete, keywords and negative keywords](#keyword-status)

* [Copy all data in selected rows to your clipboard](#copy-to-clipboard)

* [Assign constraints to keywords, and unassign constraints from keywords](#keyword-constraints)

* [Assign label classifications](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md) to keywords

## Create keywords {#keyword-create}

>[!TIP]
>
>To create a large number of keywords at once, use [campaign bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Keywords]**.

1. On the **[!UICONTROL Keywords]** tab, click **[!UICONTROL Create Keywords]**.

1. In the **[!UICONTROL Basic Settings]** step, select the network, the account, the campaign, and the ad group.

1. Enter the [[!DNL Baidu] keyword settings](keyword-settings-baidu.md), [[!DNL Google Ads] keyword settings](keyword-settings-google.md), [[!DNL LY Ads] keyword settings](keyword-settings-yahoo-japan.md), [[!DNL Microsoft Advertising] keyword settings](keyword-settings-microsoft.md), or [[!DNL Yandex] keyword settings](keyword-settings-yandex.md).

   You can enter or paste up to 2000 keywords in one operation. Separate multiple keywords with commas, or enter them on separate lines.

   >[!NOTE]
   >
   >If the account or campaign settings specify tracking only at the ad level, then Search, Social, & Commerce doesn't generate tracking for keywords.

1. Click **[!UICONTROL Review and Save]**.

1. If necessary, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit") **[!UICONTROL Edit]** and change the entity and/or keyword settings.

1. Click **[!UICONTROL Create]**.

## Edit keyword settings {#keyword-edit}

Changing the keyword text or match type can delete the existing keyword and create a new one, depending on the ad network. See the keyword settings for your ad network for details.

>[!TIP]
>
>To edit a large amount of keyword data at once, including keywords on different ad networks, use [campaign bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Keywords]**.

1. On the **[!UICONTROL Keywords]** tab, select the check box next to each keyword to edit.

1. In the bulk actions toolbar, click **[!UICONTROL Edit]**.

1. Edit the [[!DNL Baidu] keyword settings](keyword-settings-baidu.md), [[!DNL Google Ads] keyword settings](keyword-settings-google.md), [[!DNL LY Ads] keyword settings](keyword-settings-yahoo-japan.md), [[!DNL Microsoft Advertising] keyword settings](keyword-settings-microsoft.md), or [[!DNL Yandex] keyword settings](keyword-settings-yandex.md).

   For multiple keywords, you can edit only the fields that are common to all of the selected keywords, and your changes are applied to all of the selected keywords. For some alphanumeric fields, you can change existing values to a specified value, replace an existing string with a specified string, add a prefix, or append a suffix. For some monetary fields, you can change existing values to a specified value or increase or decrease the amount by a specified percentage or monetary amount, with a limit.

1. Click **[!UICONTROL Review and Save]**.

1. If necessary, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit") **[!UICONTROL Edit]** and change the keyword settings.

1. Click **[!UICONTROL Update]**.

## Create negative keywords {#keyword-negative-create}

*[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising], and existing [!DNL Baidu] accounts only*

You can create negative keywords for a search ad group or campaign that targets the search or display/native network.

>[!NOTE]
>
>You also can create and edit negative keywords in the [ad group settings](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md) and [campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md).

>[!TIP]
>
>To create a large number of negative keywords at once, use [campaign bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Keywords]**.

1. On the **[!UICONTROL Negatives]** tab, click **[!UICONTROL Create Negatives]** and then either **[!UICONTROL Campaign Negative Keyword]** or **[!UICONTROL Ad Group Negative Keyword]**.

1. Select the network, the account, the campaign, and (for ad group-level negative keywords) the ad group.

1. Enter the negative keywords. Use the following syntax, without a minus sign (`-`):

   * Negative broad match: `keyword` (not supported by [!DNL Microsoft Advertising])

   * Negative phrase match: `"keyword"`

   * Negative exact match: `[keyword]`

   Separate multiple values with commas, or enter them on separate lines. You can enter or paste up to 2000 negative keywords in one operation. The following requirements and restrictions apply:

   * Maximum character lengths: [!DNL Baidu]: 30 single-byte or 15 double-byte; [!DNL Microsoft Advertising]: 100 single-byte or 50 double-byte; [!DNL Google Ads] and [!DNL LY Ads]: 80 single-byte or 40 double-byte.

   * [!DNL Baidu] allows only one match type per keyword per ad group. For example, Ad Group 1 can't include both `"keyword"` and `[keyword]`.

   * [!DNL Google Ads]: Each keyword can consist of no more than 10 words and can include only letters, digits, and the following special characters: space `# $ & _ - " [ ] ' + . / :`

1. Click **[!UICONTROL Review and Save]**.

1. If necessary, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit") **[!UICONTROL Edit]** and change the entity and/or the negative keywords.

1. Click **[!UICONTROL Create]**.

## Change the status of keywords and negative keywords {#keyword-status}

You can pause an active, biddable search keyword to disable bidding on it. You can later resume bidding by changing the status back to active.

You also can delete active or paused search keywords or negative keywords. Deleted keywords are deleted from the ad network. They're still visible when you include them in the data filter, but you can't change them.

### Activate or pause keywords

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Keywords]**.

1. On the **[!UICONTROL Keywords]** tab, optionally filter the list, and then select the check box next to each keyword whose status you want to change.

1. In the bulk actions toolbar, change the status:

   * To activate paused keywords, click **[!UICONTROL Activate]**.

   * To pause active keywords, click **[!UICONTROL Pause]**.

### Delete keywords or negative keywords

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Keywords]**.

1. On the **[!UICONTROL Keywords]** or **[!UICONTROL Negatives]** tab, optionally filter the list, and then select the check box next to each keyword or negative keyword to delete.

1. In the bulk actions toolbar, click **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

## Copy all data in selected rows to your clipboard {#copy-to-clipboard}

Copy the visible information in selected rows, according to the applied filters and columns visible in the view. The information is saved as tab-separated values (TSV).

1. Select the check box next to each row whose data you want to copy.

1. In the bulk actions toolbar, click **[!UICONTROL Copy]**.

## Manage constraint assignments for keywords {#keyword-constraints}

You can assign and remove bidding constraints for campaigns, ad groups, keywords, placements, unit-level product groups, and dynamic search targets. Each entity can have only one constraint.

Constraints are inherited by child entities, so you don't need to assign constraints for child entities unless you want to override the inherited values.

Unassigning a constraint removes the association with the account components and all of their child components, and report data for the constraint is no longer available for those components. Unassigning a constraint doesn't delete the constraint or the account components themselves.

>[!NOTE]
>
>* If you later edit a keyword or the ad copy for a non-mutable ad &mdash; thereby creating a new keyword or ad &mdash; then the constraint isn't assigned to the new entity.
>* Active constraints restrict bidding only for assigned bid units in optimized legacy keyword-level portfolios. They're ignored for bid units that are in active portfolios, are in hybrid portfolios, or aren't in portfolios.

### Assign a constraint to keywords {#keyword-constraint-assign}

You can assign a single constraint to one or more keywords.

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Keywords]**.

1. On the **[!UICONTROL Keywords]** tab, select the check box next to each keyword to which you'll assign a single constraint.

1. In the bulk actions toolbar, click **+ [!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Select the constraint.

1. Click **[!UICONTROL Assign Now]**.

### Unassign constraints from keywords {#keyword-constraint-unassign}

Unassigning a constraint doesn't delete it. To delete a constraint, making it unavailable for future use, see "Delete constraints for search bid units" in the Optimization Guide chapter on "Bid Constraints," which is available from within Search, Social, & Commerce.

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Keywords]**.

1. On the **[!UICONTROL Keywords]** tab, select the check box next to each keyword from which you'll unassign constraints.

1. In the bulk actions toolbar, click **- [!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Click **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] keyword settings](keyword-settings-baidu.md)
>* [[!DNL Google Ads] keyword settings](keyword-settings-google.md)
>* [[!DNL LY Ads] keyword settings](keyword-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising] keyword settings](keyword-settings-microsoft.md)
>* [[!DNL Yandex] keyword settings](keyword-settings-yandex.md)
>* [Manage constraints for search bid units](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Manage label classifications](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
