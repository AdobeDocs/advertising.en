---
title: Troubleshoot performance and delivery issues using the AI assistant
description: Use Adobe Advertising DSP AI Assistant's troubleshooting agent to diagnose spending, pacing, and delivery issues for DSP packages and placements.
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
# Troubleshoot performance and delivery issues using AI assistant

*Beta feature*

AI Assistant's troubleshooting agent can identify factors that limit the performance of live packages and placements and provides recommendations to resolve issues. The troubleshooting agent can help diagnose the following types of performance and delivery issues:

  * (Placements only) Spending issues, including overspend, underspend, and failure to spend. The agent evaluates related pacing, bidding, targeting, and budget-cap factors as part of the diagnosis.

  * (Packages only) Performance issues, incuding a rising CPA or a falling ROAS. The agent doesn't diagnose engagement metrics such as CTR, CPC, clicks, or impressions.

  Each conversation covers a single diagnosis for a single package or placement. Once the agent delivers a result, start a new conversation to ask about a different issue, or about a different package or placement.

  The agent can't change settings, nor create or edit campaigns or campaign components. It also can't diagnose issues for a paused, completed, archived, or scheduled package or placement.

>[!IMPORTANT]
>
>AI-generated responses may be inaccurate or misleading. Always verify responses and sources before using them for decisions that affect cost or effort.

## Example queries

### Troubleshooting placement spending issues

* My placement stopped spending yesterday even though the deal is active. Why?

* Why has this placement been underspending for the past 5 days?

* We're halfway through the flight and significantly behind on pacing. Why?

### Troubleshooting package performance issues

* Why has CPA increased for this package over the last week?

* Why is ROAS declining for this package?

## Submit a query from AI Assistant

You can ask multiple questions in one message, but only one message at a time. Wait for a response before sending another.

1. In the upper right of any page, click ![Agentic Chat](/help/dsp/assets/agent-chat.png "Agentic chat").

1. Build the query:

   * Enter your own query.
   
   * To see examples of queries, click **[!UICONTROL Troubleshoot]** to expand the section.
     
     1. (Optional) To copy the text of an example query into the input field:
     
        1. Click the example.
        
        1. (Optional) Edit the text to suit your needs. 

   For more information about queries, see "[Best practices for writing queries and prompts](ai-assistant-about.md#writing-queries)."

   >[!NOTE]
   >
   >* If you don't specify a date range, then the agent selects a reasonable default based on the type of issue. For example, if you ask about campaign metrics without specifying a date range, then the results are for the duration of the campaign.
   >* If you have a target CPA in mind, then include it in your query (for example, "diagnose CPA against a target of $50"). If you don't specify one, then the agent uses a default target.

1. Click ![Submit query](/help/dsp/assets/submit-prompt.png "Submit query") or press the **Enter** key on your keyboard.

1. If AI Assistant asks for additional information, provide it.

>[!TIP]
>
>To ask about a different issue, or about a different package or placement, [start a new conversation](#conversation-new).

## Submit a query from the [!UICONTROL Placements] or [!UICONTROL Placements] view

You can ask multiple questions in one message, but only one message at a time. Wait for a response before sending another.

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. Do any of the following:

   * (For packages) In the [!UICONTROL Packages] view, click **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]** next to the package name.

   * (For placements) In the submenu, click **[!UICONTROL Placements]**. Next to the placement name, click  **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**.

1. Build the query:

   * Enter your own query.
   
   * To see examples of queries, click **[!UICONTROL Troubleshoot]** to expand the section.
     
     1. (Optional) To copy the text of an example query into the input field:
     
        1. Click the example.
        
        1. (Optional) Edit the text to suit your needs. 

   For more information about queries, see "[Best practices for writing queries and prompts](ai-assistant-about.md#writing-queries)."

   >[!NOTE]
   >
   >* If you don't specify a date range, then the agent selects a reasonable default based on the type of issue. For example, if you ask about campaign metrics without specifying a date range, then the results are for the duration of the campaign.
   >* If you have a target CPA in mind, then include it in your query (for example, "diagnose CPA against a target of $50"). If you don't specify one, then the agent uses a default target.

1. Click ![Submit query](/help/dsp/assets/submit-prompt.png "Submit query") or press the **Enter** key on your keyboard.

1. If AI Assistant asks for additional information, provide it.

>[!TIP]
>
>To ask about a different issue, or about a different package or placement, [start a new conversation](#conversation-new).

## Start a new conversation {#conversation-new}

Each conversation, or query thread, is saved separately so you can distinguish between your previous conversations.

1. At the top of the [chatbox](#ai-assistant-open), click ![Start a new conversation](/help/dsp/assets/new-selection.png "Start a new conversation").

1. [Submit a query](#query-submit).

## Expand and minimize the chatbox

1. At the top of the [chatbox](#ai-assistant-open), click ![Enter fullscreen](/help/dsp/assets/fullscreen.png "Enter fullscreen") to enter fullscreen mode.

1. To return the chatbox to panel mode, click **[!UICONTROL < Back>]**.

>[!MORELIKETHIS]
>
>* [About the AI Assistant in Advertising DSP](ai-assistant-about.md)
>* [Work with previous AI Assistant conversations](previous-conversations.md)
