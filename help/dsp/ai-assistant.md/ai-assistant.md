---
title: Using AI Assistant in Advertising DSP
description: Learn how to use the DSP AI assistant for troubleshooting packages and placements, reporting, and searching for product usage help.
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
# About AI Assistant in Advertising DSP

AI Assistant in DSP is a conversational interface that lets you perform any agentic workflow available in DSP from a single chatbox.

## Supported workflows

The following workflows can help you accomplish your work more effectively:

<!-- And links to all sections/pages -->

* **Troubleshooting:**  Help with diagnosing performance and delivery issues for a selected live package or placement:

  * (Placements only) Spending issues, including overspend, underspend, and failure to spend. The agent evaluates related pacing, bidding, targeting, and budget-cap factors as part of the diagnosis.

  * (Packages only) Performance issues, incuding a rising CPA or a falling ROAS. The agent doesn't diagnose engagement metrics such as CTR, CPC, clicks, or impressions.

  Each conversation covers a single diagnosis for a single package or placement. Once the agent delivers a result, start a new conversation to ask about a different issue, or about a different package or placement.

  The agent can't change settings, nor create or edit campaigns or campaign components. It also can't diagnose issues for a paused, completed, archived, or scheduled package or placement.

* **Insights:**  Get metrics and full reports for your campaigns without manually creating a report. You can download the results to a CSV file.

* **Product documentation search:** Search for conceptual and how-to content across the [Advertising DSP Guide](/help/dsp/home.md) and (advertisers with Advertising Creative) the [Advertising Creative Guide](/help/creative/home.md). You can ask about campaign management, optimization, audience management, deals, reports, and other product features.

| Feature | Description | Example queries |
| --- | --- | --- |
| Troubleshooting | Diagnose performance and delivery issues for a selected live package or placement.<ul><li>**Placements only:** Diagnose overspend, underspend, and failure to spend. The agent evaluates related pacing, bidding, targeting, and budget-cap factors.</li><li>**Packages only:** Diagnose performance issues, including a rising CPA or a falling ROAS. The agent doesn't diagnose engagement metrics such as CTR, CPC, clicks, or impressions.</li></ul>Each conversation covers one diagnosis for one package or placement. After receiving a result, start a new conversation to diagnose another issue, package, or placement.<br><br>The agent can't change settings or create or edit campaigns or campaign components. It also can't diagnose paused, completed, archived, or scheduled packages or placements. | Placement spending issues:<ul><li>My placement stopped spending yesterday even though the deal is active. Why?</li><li>Why has this placement been underspending for the past 5 days?</li><li>We're halfway through the flight and significantly behind on pacing. Why?</li></ul>Package performance issues:<ul><li>Why has CPA increased for this package over the last week?</li><li>Why is ROAS declining for this package?</li></ul> |
| Insights | Get campaign metrics and full reports without manually creating a report. You can download the results as a CSV file. | |
| Product documentation search | Find conceptual and how-to content in the [Advertising DSP Guide](/help/dsp/home.md) and, for advertisers with Advertising Creative, the [Advertising Creative Guide](/help/creative/home.md). Ask about campaign management, optimization, audience management, deals, reports, and other product features. | <ul><li>How do I attach an ad to a placement?</li><li>What targeting options are available in Adobe DSP?</li><li>What are the consequences of using the different pacing options in placement settings?</li><li>When should I use each type of optimization goal?</li><li>Why might programmatic guaranteed (PG) placements fail to serve impressions?</li><li>Which reports include household-level data?</li><li>What's the difference between a targeted experience and a non-targeted experience in [!DNL Creative]?</li><li>How do I create an ad tag for a [!DNL Creative] experience?</li></ul> |

## Submit a query

You can ask multiple questions in one message, but only one message at a time. Wait for a response before sending another.

1. In the upper right of any page, click ![Agentic Chat](/help/dsp/assets/agent-chat.png "Agentic chat").

1. (Insights and troubleshooting queries only; optional) To focus your query on a specific dimension value, such as a specific campaign, click ![Mention an entity](/help/dsp/assets/prompt-entity.png "Mention an entity"), select the dimension, and then select the dimension value.

   <!-- No ability to narrow down list of child entities for a selected parent as of 10/26/26. -->For example, for the dimension [!UICONTROL Placement], you can select from a list of all your placements to report on or troubleshoot.

   Available dimensions include:
   
   * Campaign entities: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
   * The advertiser: [!UICONTROL Advertiser],
   * Advertising Creative entities: [!UICONTROL Experience]
   * Ad targets: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

1. Enter your query, and then click ![Submit prompt](/help/dsp/assets/submit-prompt.png "Submit prompt") or press the **Enter** key on your keyboard.

   >[!NOTE]
   >
   >* If you don't specify a date range for troubleshooting or insight queries, then the agent selects a reasonable default based on the type of issue. For example, if you ask about campaign metrics without specifying a date range, then the results are for the duration of the campaign.
   >* (Troubleshooting queries) If you have a target CPA in mind, then include it in your query (for example, "diagnose CPA against a target of $50"). If you don't specify one, then the agent uses a default target.

   Responses:

   * **Responses for reporting queries:** The first few rows of the report are displayed, with links to preview the full report and to download the report as a [!DNL Microsoft Excel] comma-separated values file (.csv). 

   * **Responses for performance and delivery queries:** The response includes factors that are limiting performance and provides recommendations to resolve the issues.

   * **Responses for documentation queries:** The reponse includes inline citations and an expandable **[!UICONTROL Documentation Sources]** list at the bottom; click any citation or source listing to open the relevant page. The reponse may also include follow-up questions and suggestions.

>[!IMPORTANT]
>
>AI-generated responses may be inaccurate or misleading. Always verify responses and sources before using them for decisions that affect cost or effort.

>[!TIP]
>
>To ask about a different issue, a different dimension or dimension value, or question [start a new conversation](#conversation-new).

## Start a new conversation {#conversation-new}

Each conversation, or query thread, is saved separately so you can distinguish between your previous conversations.

1. At the top of the chatbox, click ![Start a new conversation](/help/dsp/assets/new-selection.png "Start a new conversation").

1. (Insights and troubleshooting queries only; optional) To focus your query on a specific dimension value, such as a specific campaign, click ![Mention an entity](/help/dsp/assets/prompt-entity.png "Mention an entity"), select the dimension, and then select the dimension value.

   <!-- No ability to narrow down list of child entities for a selected parent as of 10/26/26. -->For example, for the dimension [!UICONTROL Placement], you can select from a list of all your placements to report on or troubleshoot.

   Available dimensions include:
   
   * Campaign entities: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
   * The advertiser: [!UICONTROL Advertiser],
   * Advertising Creative entities: [!UICONTROL Experience]
   * Ad targets: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

1. Enter your query, and then click ![Submit prompt](/help/dsp/assets/submit-prompt.png "Submit prompt") or press the **Enter** key on your keyboard.

## Expand the chatbox

1. At the top of the chatbox, click ![Enter fullscreen](/help/dsp/assets/fullcreen.png "Enter fullscreen") to enter fullscreen mode.

1. To return the chatbox to panel mode, click **[!UICONTROL < Back>]**.

## Work with previous conversations

### List previous conversations

1. At the top of the chatbox, click ![Threads history](/help/dsp/assets/threads.png "Threads history").

### Open a previous conversation

1. At the top of the chatbox, click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Click the conversation entry.

### Rename a previous conversation

1. At the top of the chatbox, click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Next to the conversation entry, click **[!UICONTROL ...] > [!UICONTROL Rename]**.

1. Edit the conversation name, and then click **[!UICONTROL Save]**.

## Basics of writing prompts {#writing-prompts}

* **Be clear and specific.** Use full questions ("How do I subscribe to On-demand inventory?"), task phrases ("subscribe to On-demand inventory"), or topic phrases ("On-demand inventory").

* **Match UI terms** when possible for product features (such as "campaigns" or "deals").

  For common actions (such as "add," "attach," or "assign"), you can use synonyms.

* **Add detail** to narrow or broaden results. Refine with follow-up questions as needed.

* **Don't worry about punctuation and capitalization** except when they affect meaning.
