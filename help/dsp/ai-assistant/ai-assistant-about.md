---
title: About the AI Assistant in Advertising DSP
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
# About the AI Assistant in Advertising DSP

AI Assistant in DSP is a conversational interface that lets you perform any agentic workflow available in DSP from a single chatbox. You can create a new task, or ask for help continuing a previous task.

Your conversation history is maintained for all workflows, with each conversation automatically named. Your queries aren't shared with other users.

<!-- Update this:  ![Example of a query and response](/help/dsp/assets/agent-chat-response.png "Example of a query and response") -->

## Supported workflows

The following workflows can help you accomplish your work more effectively:

<!-- And links to all sections/pages -->

| Feature | Description | Responses |
| --- | --- | --- |
| [Troubleshooting](troubleshooting-agent.md) | (Beta feature) Diagnose performance and delivery issues for live packages and placements.<ul><li>Placements only: Diagnose overspend, underspend, and failure to spend. The agent evaluates related pacing, bidding, targeting, and budget-cap factors.</li><li>Packages only: Diagnose performance issues, including a rising CPA or a falling ROAS. The agent doesn't diagnose engagement metrics such as CTR, CPC, clicks, or impressions.</li></ul>Each conversation covers one diagnosis for one package or placement. After receiving a result, start a new conversation to diagnose another issue, package, or placement.<br><br>The agent can't change settings or create or edit campaigns or campaign components. It also can't diagnose paused, completed, archived, or scheduled packages or placements. | The response includes factors that are limiting performance and provides recommendations to resolve the issues. |
| [Insights](insights-agent.md) | (Beta feature) Get campaign metrics and full reports without manually creating a report. You can ask simple questions about a specific metric, such as spend or CPA for a campaign, or ask for a more complex report for a specific dimension (such as a single campaign, placement, or audience) or across dimensions (for breakdowns by campaign and advertiser). You can download the results as a CSV file. | The first few rows of the report are displayed, with links to preview the full report and to download the report as a [!DNL Microsoft Excel] comma-separated values file (.csv). |
| [Product documentation search](documentation-search.md) | Search for conceptual and how-to content in the [Advertising DSP Guide](/help/dsp/home.md) and, for advertisers with Advertising Creative, the [Advertising Creative Guide](/help/creative/home.md). Answers are based only on what's documented for these products in [Experience League](https://experienceleague.adobe.com/en/docs/advertising).<br><br>Ask about campaign management, optimization, audience management, deals, reports, and other product features. | The response includes inline citations and an expandable [!UICONTROL Documentation Sources] list at the bottom. Click any citation or source listing to open the relevant page.<br><br>The response may also include follow-up questions and suggestions to help you refine your query and find more information. |

## Best practices for writing queries and prompts {#writing-queries}

* **Be clear and specific**. Use full questions ("How do I subscribe to On-demand inventory?"), task phrases ("subscribe to On-demand inventory"), or topic phrases ("On-demand inventory").

* **Don't combine different types of requests in the same query** unless you want them to store them in the same conversation.

* **Include date ranges when relevant** to narrow down the data you want.

* **Match UI terms** when possible for product features (such as "campaigns" or "deals").

  For common actions (such as "add," "attach," or "assign"), you can use synonyms.

* **Add detail** to narrow or broaden results. Refine with follow-up questions as needed.

* **Don't worry about punctuation and capitalization** except when they affect meaning.

>[!MORELIKETHIS]
>
>* [Create reports using AI assistant](insights-agent.md)
>* [Troubleshoot performance and delivery issues using AI assistant](troubleshooting-agent.md)
>* [Create a reusable audience](/help/dsp/audiences/reusable-audience-create.md)
>* [Search for product documentation using AI Assistant](documentation-search.md)
>* [Work with previous AI Assistant conversations](previous-conversations.md)
