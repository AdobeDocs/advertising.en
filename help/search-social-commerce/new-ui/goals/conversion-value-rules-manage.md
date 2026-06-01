---
title: (New UI) Manage [!DNL Google Ads] conversion value rules
description: Learn how to view and manage [!DNL Google Ads] conversion value rules in Search, Social, & Commerce.
feature: Conversions
feature_v2:
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
    internal-label: Conversion tracking
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: a2f79fa9-a8fe-4c1c-961e-75dc3c47f954
    internal-label: Conversion value rules
---
# (New UI) Manage [!DNL Google Ads] conversion value rules

*Beta feature*

[!DNL Google Ads] [conversion value rules](https://support.google.com/google-ads/answer/10518330) let you adjust the values of conversion events based on user information, including the device type, location, and audience segment. You can use rules for value-based bidding in search, display, shopping, and performance max campaigns with Google Smart Bidding. For campaigns with Maximize Conversions and Target ROAS bidding strategies, [!DNL Google Ads] algorithms will start preferring conversions with a higher value.

Campaign-level conversion value rules override account-level rules. When a conversion satisfies multiple conversion value rules, only one of the rules is applied. Usually, the most specific rule is applied, but see the [[!DNL Google Ads] documentation on priorities for the different rule condition types](https://support.google.com/google-ads/answer/10520348).

## The [!UICONTROL Conversion Value Rules] view and functionality

Search, Social, & Commerce automatically syncs the conversion value rules from your [!DNL Google Ads] accounts. All rules created in the [!DNL Google Ads] interface are synced within 24 hours and are available in the [!UICONTROL Goals] > [!UICONTROL Conversion Value Rules] view.

Some accounts can manage their conversion value rules:

* In accounts for which conversions are tracked at the individual account or campaign level, you can [create](#google-conversion-value-rule-create), [edit](#google-conversion-value-rule-edit), and [change the status](#google-conversion-value-rule-change-status) of your account-level and campaign-level rules.

  The accounts can be linked to [[!DNL Google Ads] manager accounts](/help/search-social-commerce/new-ui/), but they can't use cross-account conversions tracking (for which conversions are tracked across all accounts in the manager account).

* In accounts that use cross-account conversion tracking, your account-level and campaign-level rules are inherited from the manager account and are read-only.

## Conversion value rules with Search, Social, & Commerce portfolios

When the advertiser account is configured to upload Search, Social, & Commerce objectives to [!DNL Google Ads], and you include a campaign that uses a conversion value rule in a portfolio with an objective, then [!DNL Google Ads] applies the conversion value rule to the original conversion value specified in the objective. As a result, conversion data in Search, Social, & Commerce differs from the conversion data in [!DNL Google Ads].

For example, suppose the objective uses a single conversion metric "Leads" and gives conversions from mobile devices a weight of 10 and conversions from non-mobile devices a weight of 10. Search, Social, & Commerce counts an event from either device type as one (1) conversion and credits the conversion value as 10. However, suppose a campaign in that portfolio uses a conversion value rule "If Device is Mobile, then multiply by 2." When a mobile Leads event is tracked for that campaign, [!DNL Google Ads] also credits the conversion count as one (1) but the conversion value as (10 x 2) = 20.

To see more information about your rules, including the original conversion values before rules were applied, see the [conversion value rules report in [!DNL Google Ads]](https://support.google.com/google-ads/answer/10519848).

## Create a [!DNL Google Ads] conversion value rule {#google-conversion-value-rule-create}

You can create account-level and campaign-level conversion value rules in [!DNL Google Ads] accounts for which conversions are tracked at the individual account level or lower. You can't create rules for accounts with cross-account conversions that are tracked at a master account level.

Each rule includes up to two conditions, as well as the conversion value adjustment to apply when the conditions are met. All rules in an account must use the same type of primary and (optional) secondary conditions. For example, if Rule 1 includes the primary condition "Audience" and the secondary condition "Location,"  then all other rules in the account must have the primary condition "Audience." When the other rules include a secondary condition, it must be "Location."

You can create multiple campaign-level rules for each campaign. However, [!DNL Google Ads] doesn't yet provide the ability to create new account-level rules outside of the [!DNL Google Ads] editor when an account-level rule already exists. To create additional account-level rules, log directly into [!DNL Google Ads] and use the [!DNL Google Ads] editor.

**Note:** Campaign-level conversion value rules override account-level rules, and only one rule can be applied to a conversion. For more information, see [how [!DNL Google Ads] determines which rule is applied to a conversion when the conversion meets the conditions for multiple rules](https://support.google.com/google-ads/answer/10520348).

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Conversion Value Rules]**.

   By default, the **[!UICONTROL Campaign]** tab is selected to show all campaign-level rules.

1. (Optional) To create an account-level rule instead, click the **[!UICONTROL Account]** tab.

1. In the toolbar, click **[!UICONTROL Create Campaign Rule]** (from the [!UICONTROL Campaign] tab) or **[!UICONTROL Create Account Rule]** (from the [!UICONTROL Account] tab).

1. Select the ad network and the account. For campaign-level rules, also select the campaign. Then click **[!UICONTROL Next]**.

1. Configure the [conversion rule settings](#google-ads-conversion-value-rule-settings).

   You must configure a primary condition and a value adjustment. You can optionally configure a secondary condition.

   Within a condition, multiple targets or exclusions are joined using the Boolean operator `OR`, so that any option may be met to initiate a value adjustment. When you include a secondary condition, the secondary condition is joined to the primary condition using the Boolean operator `ALL`, so that both conditions must be met to initiate a value adjustment. Example: If \[Location is Algeria OR Tunisia\] AND \[Device is Mobile OR Tablet\], then add 1.5.

   **Note:** All rules in an account must use the same type of primary and (optional) secondary conditions. For example, if Rule 1 includes the primary condition "Audience" and the secondary condition "Location," then all other rules in the account must have the primary condition "Audience." When the other rules include a secondary condition, it must be "Location."

1. Click **[!UICONTROL Review and Save]** to review the settings.

1. Click **[!UICONTROL Save]**.

## Edit a [!DNL Google Ads] conversion value rule {#google-conversion-value-rule-edit}

You can edit a conversion value rule in accounts/campaigns for which conversions are tracked at the individual account level or lower. You can't edit a rule for an account with cross-account conversions that are tracked at a master account level.

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Conversion Value Rules]**.

   By default, the **[!UICONTROL Campaign]** tab is selected to show all campaign-level rules.

1. (Optional) To view all account-level rules instead, click the **[!UICONTROL Account]** tab.

1. Select the check box next to the rule.

1. In the bulk actions toolbar, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit).

1. Edit the [conversion rule settings](#google-ads-conversion-value-rule-settings).

   You can't edit the condition types for an existing rule, but you can edit the conditions and the value adjustments.

   You must configure a primary condition and a value adjustment. You can optionally configure a secondary condition.

   **Note:** If you add a secondary condition, then it must be the same condition type as other rules in the account. For example, if Rule 1 other rules in the account have the secondary condition "Location," then, when the other rules include a secondary condition, the secondary condition must be "Location." When you include a secondary condition, the secondary condition is joined to the primary condition using the Boolean operator `ALL`, so that both conditions must be met to initiate a value adjustment.

1. Click **[!UICONTROL Review and Save]** to review the settings.

1. Click **[!UICONTROL Save]**.

## Change the status of a [!DNL Google Ads] conversion value rule {#google-conversion-value-rule-change-status}

You can pause, activate, or delete a conversion value rule in accounts and campaigns for which conversions are tracked at the individual account level.

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Conversion Value Rules]**.

   By default, the **[!UICONTROL Campaign]** tab is selected to show all campaign-level rules.

1. (Optional) To view all account-level rules instead, click the **[!UICONTROL Account]** tab.

1. Select the check box next to each row to change.

1. In the bulk actions toolbar,

   * To activate (enable) paused rules, click **[!UICONTROL ...] > [!UICONTROL Activate]**.

   * To pause active rules, click **[!UICONTROL ...] > [!UICONTROL Pause]**.

   * To delete active or paused rules, click ![Delete](/help/search-social-commerce/assets/delete.png "Delete").

1. In the confirmation message, click **[!UICONTROL Confirm]**.

## [!DNL Google Ads] conversion value rule settings {#google-conversion-value-rule-settings}

| Section | Parameter | Description |
|---|---|---|
| [!UICONTROL Select Campaign] | [!UICONTROL Network] | The ad network. |
| | [!UICONTROL Account] | The ad network account. |
| | [!UICONTROL Campaign] | (Campaign-level conversion value rules only) The ad campaign. |
| [!UICONTROL Conditions] > [!UICONTROL Primary Condition] | \[Condition Type\] | (Read-only for existing rules) The type of condition that must be met to trigger a value adjustment:<ul><li>*[!UICONTROL Device]:* To target all or specific device types.</li><li>*[!UICONTROL Location]:* To target all countries and territories or target and exclude specific locations.</li><li>*[!UICONTROL Audiences]:* To target all or specific audiences</li></ul>**Note:** All rules in an account must use the same type of primary and (optional) secondary conditions. For example, if Rule 1 includes the primary condition "Audience" and the secondary condition "Location," then all other rules in the account must have the primary condition "Audience." When the other rules include a secondary condition, it must be "Location." |
| | \[Condition Type\] > [!UICONTROL Device] and [!UICONTROL Device Level] | (Device conditions only) Which device types to target:<ul><li>*[!UICONTROL All devices]:** To target all device types.</li><li>*[!UICONTROL Select devices]:* To specify one or more device types to target: *[!UICONTROL Desktop]:*, *[!UICONTROL Mobile]*, and *[!UICONTROL Tablet]:*.</li></ul>Within a condition, multiple targets are joined using the Boolean operator `OR`, so that any option may be met to initiate a value adjustment. Example: If \[Device is Mobile OR Tablet\], then Add 1.5. |
| | \[Condition Type\] > [!UICONTROL Location] and [!UICONTROL Location Level] | (Location conditions only) The location targets and exclusions:<ul><li>*[!UICONTROL All countries and territories]:* To target all countries and locations or target and exclude specific locations.</li><li>*[!UICONTROL Enter a location]:* To target and exclude specific locations.</li></ul><ul><li>To expand a location or sublocation, click `>` after the name.</li><li>To add a target, select the target once to show a green check mark.</li><li>To exclude a target, select the target a second time to show a red **[!UICONTROL X]**.</li><li>To remove a target or exclusion, do either of the following:<ul><li>Click ![Delete](/help/search-social-commerce/assets/delete.png "Delete") next to the item in the [!UICONTROL Selections] column.</li><li>Select the target until no check mark or [!UICONTROL X] appears.</li></ul></li></ul>Within a condition, multiple targets or exclusions are joined using the Boolean operator `OR`, so that any option may be met to initiate a value adjustment. Example:  If \[Location is Algeria OR Tunisia\], then Add 1.5. |
| | \[Condition Type\] > [!UICONTROL Audience] and [!UICONTROL Audience Level] | (Audience conditions only) The audience targets:<ul><li>*[!UICONTROL All audience segments]:* To target all [!DNL Google Ads] audience segments.</li><li>*[!UICONTROL Enter audience segments]:* To target specific [!DNL Google Ads] audience segments.</li></ul><ul><li>To expand a category or subcategory into its segments, click `>` after the name.</li><li>To add a target, select the target.</li><li>To remove a target, deselect the target or click ![Delete](/help/search-social-commerce/assets/delete.png "Delete") next to the item in the [!UICONTROL Selection] column.</li></ul>Within a condition, multiple targets or exclusions are joined using the Boolean operator OR, so that any option may be met to initiate a value adjustment. Example:  If \[Audience is Bargain Travelers OR Family Vacationers\], then Add 1.5.<br><br>**Note:** Once you save an audience target, you can add additional audiences but can't remove them outside of the [!DNL Google Ads] editor. If you need to remove an audience target, log directly into [!DNL Google Ads] and use the [!DNL Google Ads] editor. |
| [!UICONTROL Conditions] > [!UICONTROL Secondary Condition] | \[Condition Type\] | (Optional; read-only for existing rules) The type of condition that must be met to trigger a value adjustment. When you include a secondary condition, the secondary condition is joined to the primary condition using the Boolean operator `ALL`, so that both conditions must be met to initiate a value adjustment. Example: If \[Location is Algeria OR Tunisia\] AND \[Device is Mobile OR Tablet\], then Add 1.5.<br><br>See the entries for primary conditions for descriptions.<br><br>**Note:** All rules in an account must use the same type of primary and (optional) secondary conditions. For example, if Rule 1 includes the primary condition "Audience" and the secondary condition "Location," then all other rules in the account must have the primary condition "Audience." When the other rules include a secondary condition, it must be "Location." |
| [!UICONTROL Value Adjustment] | [!UICONTROL Adjustment Operation] and [!UICONTROL Adjustment Value] | Specify the adjustment type, and then enter a positive value:<ul><li>*[!UICONTROL Add]:* Adds the specified value to the conversion value that is passed. The value must be greater than zero (0).</li><li>*[!UICONTROL Multiply]:* Multiplies the conversion value that is passed by the specified value. The value must be from 0.5 to 10.</li></ul> |

<!--
>[!MORELIKETHIS]
>
>* 
-->
