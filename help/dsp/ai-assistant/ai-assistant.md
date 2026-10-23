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

AI Assistant in DSP is a conversational interface that lets you perform any agentic workflow available in DSP from a single chatbox. Your conversation history is maintained for all workflows, with each conversation automatically named. Your queries aren't shared with other users.

<!-- Update this:  ![Example of a query and response](/help/dsp/assets/agent-chat-response.png "Example of a query and response") -->

## Supported workflows

The following workflows can help you accomplish your work more effectively:

<!-- And links to all sections/pages -->

| Feature | Description | Example queries | Responses |
| --- | --- | --- | --- |
| Troubleshooting | Diagnose performance and delivery issues for a selected live package or placement.<ul><li>**Placements only:** Diagnose overspend, underspend, and failure to spend. The agent evaluates related pacing, bidding, targeting, and budget-cap factors.</li><li>**Packages only:** Diagnose performance issues, including a rising CPA or a falling ROAS. The agent doesn't diagnose engagement metrics such as CTR, CPC, clicks, or impressions.</li></ul>Each conversation covers one diagnosis for one package or placement. After receiving a result, start a new conversation to diagnose another issue, package, or placement.<br><br>The agent can't change settings or create or edit campaigns or campaign components. It also can't diagnose paused, completed, archived, or scheduled packages or placements. | Placement spending issues:<ul><li>My placement stopped spending yesterday even though the deal is active. Why?</li><li>Why has this placement been underspending for the past 5 days?</li><li>We're halfway through the flight and significantly behind on pacing. Why?</li></ul>Package performance issues:<ul><li>Why has CPA increased for this package over the last week?</li><li>Why is ROAS declining for this package?</li></ul> | The response includes factors that are limiting performance and provides recommendations to resolve the issues. |
| Insights | Get campaign metrics and full reports without manually creating a report. You can ask simple questions about a specific metric, such as spend or CPA for a campaign, or ask for a more complex report for a specific dimension (such as a single campaign, placement, or audience) or across dimensions (for breakdowns by campaign and advertiser). You can download the results as a CSV file. | <ul><li>How much did [Campaign Name] spend last week?<li>How many conversions did [Campaign Name] get this month?</li><li>Which placements are behind pace by more than 20%?</li></li>Show me the CPA by package for [Campaign Name]</li></ul> | The first few rows of the report are displayed, with links to preview the full report and to download the report as a [!DNL Microsoft Excel] comma-separated values file (.csv). |
| Product documentation search | Search for conceptual and how-to content in the [Advertising DSP Guide](/help/dsp/home.md) and, for advertisers with Advertising Creative, the [Advertising Creative Guide](/help/creative/home.md). Answers are based only on what's documented for these products in [Experience League](https://experienceleague.adobe.com/en/docs/advertising).<br><br>Ask about campaign management, optimization, audience management, deals, reports, and other product features. | <ul><li>How do I attach an ad to a placement?</li><li>What targeting options are available in Adobe DSP?</li><li>What are the consequences of using the different pacing options in placement settings?</li><li>When should I use each type of optimization goal?</li><li>Why might programmatic guaranteed (PG) placements fail to serve impressions?</li><li>Which reports include household-level data?</li><li>What's the difference between a targeted experience and a non-targeted experience in [!DNL Creative]?</li><li>How do I create an ad tag for a [!DNL Creative] experience?</li></ul> | The response includes inline citations and an expandable [!UICONTROL Documentation Sources] list at the bottom. Click any citation or source listing to open the relevant page.<br><br>The response may also include follow-up questions and suggestions to help you refine your query and find more information. |

## Open AI Assistant {#ai-assistant-open}

* In the upper right of any page, click ![Agentic Chat](/help/dsp/assets/agent-chat.png "Agentic chat").

## Expand the chatbox

1. At the top of the [chatbox](#ai-assistant-open), click ![Enter fullscreen](/help/dsp/assets/fullcreen.png "Enter fullscreen") to enter fullscreen mode.

1. To return the chatbox to panel mode, click **[!UICONTROL < Back>]**.

## Submit a query {#query-submit}

1. [Open AI Assistant](#ai-assistant-open).

1. (Insights and troubleshooting queries only; optional) To focus your query on a specific dimension value, such as a specific campaign, click ![Mention an entity](/help/dsp/assets/prompt-entity.png "Mention an entity"), select the dimension, and then select the dimension value.

   <!-- No ability to narrow down list of child entities for a selected parent as of 10/26/26. -->For example, for the dimension [!UICONTROL Campaign], you can select from a list of all your campaigns to report on.

   Available dimensions include:
   
   * Campaign entities: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
   * The advertiser: [!UICONTROL Advertiser],
   * Advertising Creative entities: [!UICONTROL Experience]
   * Ad targets: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

1. Enter your query, and then click ![Submit prompt](/help/dsp/assets/submit.png "Submit prompt") or press the **Enter** key on your keyboard.

   You can create a completely new task, or ask for help continuing a previous task.

   You can ask multiple questions in one message, but only one message at a time. Wait for a response before sending another.

   >[!NOTE]
   >
   >* (Troubleshooting and insight queries) If you don't specify a date range, then the agent selects a reasonable default based on the type of issue. For example, if you ask about campaign metrics without specifying a date range, then the results are for the duration of the campaign.
   >* (Troubleshooting queries) If you have a target CPA in mind, then include it in your query (for example, "diagnose CPA against a target of $50"). If you don't specify one, then the agent uses a default target.

1. If AI Assistant asks for additional information, provide it.

1. (Product documentation queries only; optional) To open a page used as a data source for the response, do either of the following:

   * Click the numbered citation.

   * Click **[!UICONTROL Documentation Sources]** to show a list of all pages cited in the response, and then click the page link.

>[!IMPORTANT]
>
>AI-generated responses may be inaccurate or misleading. Always verify responses and sources before using them for decisions that affect cost or effort.

>[!TIP]
>
>To ask another query that you want to be saved as a separate thread, [start a new conversation](#conversation-new).

## (Insight queries) Download or preview a full report from the chatbox

* To download a copy of the full report, click ![Export](/help/dsp/assets/download.png "Export").

   The file is downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

* To preview the full report in a side panel, click ![Preview](/help/dsp/assets/agent-chat-preview.png "Preview"). To download the report from the preview, click ![Export](/help/dsp/assets/download.png "Export").

   If you download the report, it's downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

## Start a new conversation {#conversation-new}

Each conversation, or query thread, is saved separately so you can distinguish between your previous conversations.

1. At the top of the [chatbox](#ai-assistant-open), click ![Start a new conversation](/help/dsp/assets/new-selection.png "Start a new conversation").

1. [Submit a query](#query-submit).

## Work with previous conversations

### List previous conversations

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

### Open a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Click the conversation entry.

To repeat the same topic verbatim, copy the key details into a new conversation. Otherwise, you can ask AI Assistant to repeat a finite task within a specific conversation.

### Rename a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Next to the conversation entry, click **[!UICONTROL ...] > [!UICONTROL Rename]**.

1. Edit the conversation name, and then click **[!UICONTROL Save]**.

## Best practices of writing prompts {#writing-prompts}

* **Be clear and specific**. Use full questions ("How do I subscribe to On-demand inventory?"), task phrases ("subscribe to On-demand inventory"), or topic phrases ("On-demand inventory").

* **Don't combine different types of requests in the same query** unless you want them to store them in the same conversation.

* **Include date ranges when relevant** to narrow down the data you want.

* **Match UI terms** when possible for product features (such as "campaigns" or "deals").

  For common actions (such as "add," "attach," or "assign"), you can use synonyms.

* **Add detail** to narrow or broaden results. Refine with follow-up questions as needed.

* **Don't worry about punctuation and capitalization** except when they affect meaning.
