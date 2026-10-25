---
title: Create reports using AI assistant
description: Learn how to use Adobe Advertising DSP AI Assistant's insights agent to query campaign metrics, generate reports, and download CSV files.
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
# Create reports using AI assistant

Use the AI Assistant's insights agent to get metrics and full reports for your campaigns, campaign components, Advertising Creative experiences, advertisers, and ad targets &mdash; without manually creating a report. You can ask simple questions about a specific metric, such as spend or CPA for a campaign, or ask for a more complex report for a specific dimension (such as a single campaign or audience) or across dimensions (for breakdowns for each campaign and advertiser). You can download the results as a CSV file.

>[!IMPORTANT]
>
>AI-generated responses may be inaccurate or misleading. Always verify responses and sources before using them for decisions that affect cost or effort.

## Example queries

* How much did [Campaign Name] spend last week?

* How many conversions did [Campaign Name] get this month?

* Show me the CPA by package for [Campaign Name].

* Which placements are behind pace by more than 20%?

* Compare the net spend for all campaigns and packages in the last 15 days.

## Submit a query

You can ask multiple questions in one message, but only one message at a time. Wait for a response before sending another.

1. In the upper right of any page, click ![Agentic Chat](/help/dsp/assets/agent-chat.png "Agentic chat").

1. Build the query:

   1. Do either of the following:

      * Enter your own query.

      * To see examples of queries:
   
        1. Click **[!UICONTROL Insights]** to expand the section.
     
        1. (Optional) To copy the text of an example query into the input field:
     
           1. Click the example.
        
           1. (Optional) Edit the text to suit your needs. 

   1. (Optional) To focus your query on a specific dimension value (such as a specific campaign), optionally insert the cursor where you want the dimension value to appear, click ![Mention an entity](/help/dsp/assets/prompt-entity.png "Mention an entity"), select the dimension, and then select the dimension value.
    
      For example, for the dimension [!UICONTROL Campaign], you can select from a list of all your campaigns to report on.
      
      Available dimensions include:
      
      * Campaign entities: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
      * The advertiser: [!UICONTROL Advertiser]
      * Advertising Creative entities: [!UICONTROL Experience]
      * Ad targets: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

   For more information about queries, see "[Best practices for writing queries and prompts](ai-assistant-about.md#writing-queries)."

1. Click ![Submit query](/help/dsp/assets/submit-prompt.png "Submit query") or press the **Enter** key on your keyboard. If the agent requests additional information, provide the required information.

   The first few rows of the report are displayed, with links to preview the full report and to download the report.

   A few rows of the generated report are shown.

>[!TIP]
>
>To ask about a different issue, or about a different package or placement, [start a new conversation](#conversation-new).

## Download or preview a full report from the chatbox

* To download a copy of the full report, click ![Export](/help/dsp/assets/download.png "Export").

   The file is downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

* To preview the full report in a side panel, click ![Preview](/help/dsp/assets/agent-chat-preview.png "Preview"). To download the report from the preview, click ![Export](/help/dsp/assets/download.png "Export").

   If you download the report, it's downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

## Start a new conversation {#conversation-new}

Each conversation, or query thread, is saved separately so you can distinguish between your previous conversations.

1. At the top of the [chatbox](#ai-assistant-open), click ![Start a new conversation](/help/dsp/assets/new-selection.png "Start a new conversation").

1. [Submit a query](#query-submit).

>[!MORELIKETHIS]
>
>* [About the AI Assistant in Advertising DSP](ai-assistant-about.md)
>* [Work with previous AI Assistant conversations](previous-conversations.md)
