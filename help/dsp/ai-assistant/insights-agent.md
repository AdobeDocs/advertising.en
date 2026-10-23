---
title: XXX using the AI assistant
description: Learn how to use the AI assistant's insights agent to XXXX.
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
# XXXs using the DSP AI assistant

The AI assistant's insights agent can 


You can ask simple questions about a specific metric, such as spend or CPA for a campaign, or ask for a more complex report for a specific dimension (such as a single campaign, placement, or audience) or across dimensions (for breakdowns by campaign and advertiser).

<!-- probably rename, finish this description, and add a link to the page -->**Insights:**  XXXXXX. Get metrics and reports for your campaigns without manually creating a report. You can download the results to a CSV file.



>[!IMPORTANT]
>
>AI-generated responses may be inaccurate or misleading. Always verify responses and sources before using them for decisions that affect cost or effort.

## Example queries

* How are my active campaigns performing this week?

* Which placements are behind pace by more than 20%?

* Show me the CPA by package for [recent campaign].

* Compare the net spend for all campaigns and packages in the last 15 days.

## Submit a query

You can ask multiple questions in one message, but only one message at a time. Wait for a response before sending another.

1. In the upper right of any page, click ![Agentic Chat](/help/dsp/assets/agent-chat.png "Agentic chat").

1. (Optional) To specify the relevant report dimension (such as a specific campaign), click ![Mention an entity](/help/dsp/assets/prompt-entity.png "Mention an entity"), select the dimension, and then select the dimension value.

   Available dimensions include:
   
   * Campaign entities: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
   * The advertiser: [!UICONTROL Advertiser],
   * Advertising Creative entities: [!UICONTROL Experience]
   * Ad targets: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

1. Enter your query, and then click ![Submit prompt](/help/dsp/assets/submit-prompt.png "Submit prompt") or press the **Enter** key on your keyboard. If the agent requests additional information, provide the required information.

   <!-- For more information, see "[Writing prompts](#writing-prompts)." -->

   The first few rows of the report are displayed, with links to preview the full report and to download the report.
   A few rows of the generated report are shown.

1. (Optional) To download a copy of the full report, click ![Export](/help/dsp/assets/download.png "Export").

   The file is downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

1. (Optional) To preview the full report in a side panel, click ![Preview](/help/dsp/assets/agent-chat-preview.png "Preview"). To download the report from the preview, click ![Export](/help/dsp/assets/download.png "Export").

   If you download the report, it's downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

