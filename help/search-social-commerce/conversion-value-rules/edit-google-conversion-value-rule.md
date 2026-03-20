---
title: Edit a [!DNL Google Ads] conversion value rule
---

# Edit a [!DNL Google Ads] conversion value rule

You can edit a conversion value rule in accounts/campaigns for which conversions are tracked at the individual account level or lower. You can't edit a rule for an account with cross-account conversions that are tracked at a master account level.

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Conversion Value Rules]**.

   By default, the **[!UICONTROL Campaign]** tab is selected to show all campaign-level rules.

1. (Optional) To view all account-level rules instead, click the **[!UICONTROL Account]** tab.

1. Select the check box next to the rule.

1. In the bulk actions toolbar,

   * To activate (enable) paused rules, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit).

1. Edit the [conversion rule settings](google-conversion-value-rule-settings.md).

   You can't edit the condition types for an existing rule, but you can edit the conditions and the value adjustments.

   You must configure a primary condition and a value adjustment. You can optionally configure a secondary condition.

   **Note:** If you add a secondary condition, it must be the same condition type as other rules in the account. For example, if Rule 1 other rules in the account have the secondary condition "Location," then, when the other rules include a secondary condition, the secondary condition must be "Location." When you include a secondary condition, the secondary condition is joined to the primary condition using the Boolean operator ALL, so that both conditions must be met to initiate a value adjustment.

1. Click **[!UICONTROL Review and Save]** to review the settings.

1. Click **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [About [!DNL Google Ads] conversion value rules](about-google-conversion-value-rules.md)
>* [Create a [!DNL Google Ads] conversion value rule](create-google-conversion-value-rule.md)
>* [Change the status of a [!DNL Google Ads] conversion value rule](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] conversion value rule settings](google-conversion-value-rule-settings.md)

