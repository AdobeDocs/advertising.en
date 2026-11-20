---
title: '[!DNL ChatGPT] ad group settings'
description: Reference the settings for [!DNL ChatGPT] ad groups.
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
---
# [!DNL ChatGPT] ad group settings

*Ads in [!DNL ChatGPT] are a pilot feature by [!DNL OpenAI]*

## [!UICONTROL Basic Settings] tab

*New ad groups only*

**[!UICONTROL Network]:** The ad network.

**[!UICONTROL Account]:** The ad network account.

**[!UICONTROL Campaign]:** The campaign. You can't change the campaign after you create the ad group.

## [!UICONTROL Ad Group Details] tab

**[!UICONTROL Ad Group name]:** An ad group name that's unique within the campaign and includes at least three characters.

**[!UICONTROL Status]:** The display status of the ad group: *[!UICONTROL Active]* or *[!UICONTROL Paused]*. The default for new ad groups is *[!UICONTROL Active]*.

**[!UICONTROL Bid strategy]:** (Campaigns with the objective [!UICONTROL Clicks] or [!UICONTROL Conversions]) How to bid for ads in the ad group:

* *[!UICONTROL Autobid]:* (The default for new ad groups) [!DNL OpenAI] automatically adjusts bids to get the most clicks or conversions, depending on the campaign objective, from your budget. You don't enter a bid amount. This option is available for both daily and lifetime campaign budgets.

* *[!UICONTROL Target CPC]:* (Campaigns with the objective [!UICONTROL Clicks]) Bids toward an average cost-per-click goal. Enter the goal in the [!UICONTROL Target CPC] field.

* *[!UICONTROL Target CPA]:* (Campaigns with the objective [!UICONTROL Conversions]) Bids toward an average cost-per-conversion goal. Enter the goal in the [!UICONTROL Target CPA] field.

* *[!UICONTROL Manual: Max bid]:* (Existing manually bid ad groups only) Retains the existing maximum bid as a read-only amount. You can keep this strategy or switch to [!UICONTROL Autobid] or the target strategy for the campaign objective. This option isn't available for new ad groups or when editing ad groups that already use autobid or target bidding.

Existing manually-bid ad groups aren't automatically changed to another strategy. Editing only a target amount or an unrelated setting doesn't change an existing target bidding strategy.

**[!UICONTROL Target CPC]:** (Ad groups with the bid strategy [!UICONTROL Target CPC]; required) The average cost per click you want to achieve, in the account's currency. Enter a positive amount. This is an average cost goal, not a maximum bid.

**[!UICONTROL Target CPA]:** (Ad groups with the bid strategy [!UICONTROL Target CPA]; required) The average cost per conversion you want to achieve, in the account's currency. Enter a positive amount. This is an average cost goal, not a maximum bid.

**[!UICONTROL Maximum CPC bid]:** (Campaigns with the objective [!UICONTROL Clicks]; existing manually bid ad groups only; read-only) The existing maximum amount you'll pay for each click.

**[!UICONTROL Conversion-optimized bid cap]:** (Campaigns with the objective [!UICONTROL Conversions]; existing manually bid ad groups only; read-only) The existing maximum amount you're willing to bid for a conversion. [!DNL OpenAI] uses the predicted conversion rate to convert this value into a per-impression auction bid.

**[!UICONTROL Maximum CPM bid]:** (Campaigns with the objective [!UICONTROL Reach]) The maximum amount you'll pay for one thousand impressions, in the account's currency. Enter a value from 0.01-5000. Reach campaigns don't have the [!UICONTROL Bid strategy] options.

**[!UICONTROL Context hints (optional)]:** Description of the conversations, topics, or keywords for which your products or services may be relevant. Separate hints with commas or line breaks. Your hints may be used to guide matching but aren't exact-match targeting rules. See [[!DNL ChatGPT Ads] help on how to write effective context hints](https://help.openai.com/en/articles/20001211-create-ad-groups-for-chatgpt#writing-effective-context-hints).

**[!UICONTROL Landing Page Suffix]:** (Optional) Any parameters to append to the end of landing page URLs to track information. Example: `param1=value1&param2=value2`.

>[!MORELIKETHIS]
>
>* [Manage ad groups](ad-group-manage.md)
