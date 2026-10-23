---
title: Troubleshoot performance and delivery issues using the AI assistant
description: Learn how to use the AI assistant's troubleshooting agent to diagnose spending, pacing, and delivery issues for DSP packages and placements.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Troubleshoot performance and delivery issues using the DSP AI assistant

The AI assistant's troubleshooting agent can identify factors that limit performance and provides recommendations to resolve issues. The troubleshooting agent can help with diagnosing performance and delivery issues for a selected live package or placement:

  * (Placements only) Spending issues, including overspend, underspend, and failure to spend. The agent evaluates related pacing, bidding, targeting, and budget-cap factors as part of the diagnosis.

  * (Packages only) Performance issues, incuding a rising CPA or a falling ROAS. The agent doesn't diagnose engagement metrics such as CTR, CPC, clicks, or impressions.

  Each conversation covers a single diagnosis for a single package or placement. Once the agent delivers a result, start a new conversation to ask about a different issue, or about a different package or placement.

  The agent can't change settings, nor create or edit campaigns or campaign components. It also can't diagnose issues for a paused, completed, archived, or scheduled package or placement.

>[!IMPORTANT]
>
>AI-generated responses may be inaccurate or misleading. Always verify responses and sources before using them for decisions that affect cost or effort.

## Example queries

>[!NOTE]
>
>You don't need to specify a date range. If you don't include one, then the agent selects a reasonable default based on the type of issue.

### Troubleshooting placement spending issues

* My placement stopped spending yesterday even though the deal is active. Why?

* Why has this placement been underspending for the past 5 days?

* We're halfway through the flight and significantly behind on pacing. Why?

### Troubleshooting package performance issues

* Why has CPA increased for this package over the last week?

* Why is ROAS declining for this package?

>[!TIP]
>
>If you have a target CPA in mind, then include it in your query (for example, "diagnose CPA against a target of $50"). If you don't specify one, then the agent uses a default target.

## Submit a query for a live package or placement

You can ask multiple questions in one message, but only one message at a time. Wait for a response before sending another.

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. Do either of the following:

   * (For packages) In the [!UICONTROL Packages] view, click **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]** next to the package name.

   * (For placements) In the submenu, click **[!UICONTROL Placements]**. Next to the placement name, click  **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**.

1. (Optional) To focus your query on a specific dimension value, such as a specific campaign, click ![Mention an entity](/help/dsp/assets/prompt-entity.png "Mention an entity"), select the dimension, and then select the dimension value.

   For example, for the dimension [!UICONTROL Campaign], you can select from a list of your campaigns. Similarly, you can select [!UICONTROL Audience] and select a saved audience to report on or troubleshoot.

   Available dimensions include:
   
   * Campaign entities: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
   * The advertiser: [!UICONTROL Advertiser],
   * Advertising Creative entities: [!UICONTROL Experience]
   * Ad targets: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

1. Enter your query, and then click ![Submit prompt](/help/dsp/assets/submit-prompt.png "Submit prompt") or press the **Enter** key on your keyboard.

   <!-- For more information, see "[Writing prompts](#writing-prompts)." -->

   For performance and delivery queries, the response includes factors that are limiting performance and provides recommendations to resolve the issues.

1. (Optional) Rate the response using the thumbs-up or thumbs-down icon.

>[!TIP]
>
>To ask about a different issue, or about a different package or placement, start a new conversation.
