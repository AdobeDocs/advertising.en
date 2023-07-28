---
title: Data requirements for traffic and conversion metrics for [!DNL Naver] tracking-only accounts
description: Reference the data upload requirements for [!DNL Naver] tracking-only accounts.
exl-id: 6f79730b-f8d6-4a7f-9d31-f42fe63e6b5d
feature: Search Tools
---
# Metric data requirements for [!DNL Naver] tracking-only accounts

The following are the data requirements for [!DNL Naver] traffic and conversion metrics for tracking-only accounts.

Data files must be in TSV, CSV, or TXT format.

The following header fields are required and optional. Each data row must include a daily-aggregated value for at least one metric field.

| Header Field/Column Name | Type | Description |
| ---- | ---- | ---- |
| Period | DateTime | The date for which the data applies, in the format `YYYY.MM.DD.` (such as `2019.11.15.`, with a period after the day). |
| Campaign | Case-sensitive string | The campaign name. |
| Adgroup (as one word) | Case-sensitive string | The ad group name. |
| Keyword | Case-sensitive string | (Keyword ads) The keyword that generated the ad. |
| [Metric] | Integer | (Optional) The number of [whatever the metric is measuring].</br><br>Standard metrics include Impressions, Cost, and Clicks. You can include any additional metrics you want from the ad network. Include each metric in a separate column.<br><br><b>Notes:</b><ul><li>The column header for Cost must be &quot;Cost (KRW).&quot;</li><li>To include Cost (KRW) for brand ads, manually divide the fixed monthly cost by day at the ad group level.</li><li>Remove all commas from standard metric values. For example, use 1000 instead of 1,000.</li><li>For null values, use 0.</li></ul> |

>[!MORELIKETHIS]
>
>* [Implement [!DNL Naver] tracking-only accounts](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Appendix - Required bulksheet data for [!DNL Naver] accounts](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [Upload traffic and conversion metrics for [!DNL Naver] tracking-only accounts](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
