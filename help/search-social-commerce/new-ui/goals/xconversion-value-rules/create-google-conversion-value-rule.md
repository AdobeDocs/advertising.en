---
title: Create a [!DNL Google Ads] conversion value rule
description: Learn how to create [!DNL Google Ads] conversion value rules.
---
# Create a [!DNL Google Ads] conversion value rule

You can create account-level and campaign-level conversion value rules in [!DNL Google Ads] accounts for which conversions are tracked at the individual account level or lower. You can't create rules for accounts with cross-account conversions that are tracked at a master account level.

Each rule includes up to two conditions, as well as the conversion value adjustment to apply when the conditions are met. All rules in an account must use the same type of primary and (optional) secondary conditions. For example, if Rule 1 includes the primary condition "Audience" and the secondary condition "Location,"  then all other rules in the account must have the primary condition "Audience." When the other rules include a secondary condition, it must be "Location."

You can create multiple campaign-level rules for each campaign. However, [!DNL Google Ads] doesn't yet provide the ability to create new account-level rules outside of the [!DNL Google Ads] editor when an account-level rule already exists. To create additional account-level rules, log directly into [!DNL Google Ads] and use the [!DNL Google Ads] editor.

**Note:** Campaign-level conversion value rules override account-level rules, and only one rule can be applied to a conversion. For more information, see [how [!DNL Google Ads] determines which rule is applied to a conversion when the conversion meets the conditions for multiple rules](https://support.google.com/google-ads/answer/10520348).

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Conversion Value Rules]**.

   By default, the **[!UICONTROL Campaign]** tab is selected to show all campaign-level rules.

1. (Optional) To create an account-level rule instead, click the **[!UICONTROL Account]** tab.

1. In the toolbar, click ![Create](/help/search-social-commerce/assets/add.png "Create").<!-- Upload newer icon -->

1. Select the ad network and the account. For campaign-level rules, also select the campaign. Then click **[!UICONTROL Next]**.

1. Configure the [conversion rule settings](google-conversion-value-rule-settings.md).

   You must configure a primary condition and a value adjustment. You can optionally configure a secondary condition.

   Within a condition, multiple targets or exclusions are joined using the Boolean operator OR, so that any option may be met to initiate a value adjustment. When you include a secondary condition, the secondary condition is joined to the primary condition using the Boolean operator ALL, so that both conditions must be met to initiate a value adjustment. Example:  If \[Location is Algeria OR Tunisia\] AND \[Device is Mobile OR Tablet\], then add 1.5.

   **Note:** All rules in an account must use the same type of primary and (optional) secondary conditions. For example, if Rule 1 includes the primary condition "Audience" and the secondary condition "Location," then all other rules in the account must have the primary condition "Audience." When the other rules include a secondary condition, it must be "Location."

1. Click **[!UICONTROL Review and Save]** to review the settings.

1. Click **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [About [!DNL Google Ads] conversion value rules](about-google-conversion-value-rules.md)
>* [Edit a [!DNL Google Ads] conversion value rule](edit-google-conversion-value-rule.md)
>* [Change the status of a [!DNL Google Ads] conversion value rule](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] conversion value rule settings](google-conversion-value-rule-settings.md)

