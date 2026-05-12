---
title: Available [!DNL Google Analytics] metrics
description: Reference the [!DNL Google Analytics] metrics available for data sources.
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/hRYeNcQu4uUTCAHXcF9zaZfQm-mw6kDlqvs2AxZhED8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
    internal-label: Search admin
subfeature_v2:
  - id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
    internal-label: Search data sources
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
---
# Appendix - Available [!DNL Google Analytics] metrics

The following metrics, except for the exclusions noted, are available when they're enabled in the customer's implementation in [!DNL Google Analytics].

<!--
 Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| Category | Excluded | Comments |
| ---- | ---- | ---- |
| \[All\] | Metrics with a data type of "PERCENT" | Metrics presented as a percentage are always excluded. |
| User | ga:1dayUsers, ga:7dayUsers, ga:14dayUsers, ga:28dayUsers, ga:sessionsPerUser | &mdash; |
| Session | ga:uniqueDimensionCombinations | &mdash; |
| Goal Conversions | &mdash; | &mdash; |
| Page Tracking | ga:entrances, ga:timeOnPage, ga:exits | &mdash; |
| Internal Search | &mdash; | The friendly names of all metrics from Internal Search are prepended with the value "InternalSearch: " |
| Event Tracking | &mdash; | &mdash; |
| Ecommerce | &mdash; | &mdash; |
| Social Interactions | &mdash; | &mdash; |
| Exceptions | &mdash; | &mdash; |
| Custom Variables or Columns | ga:calcMetric_* | Calculated metrics are always excluded. |

>[!MORELIKETHIS]
>
>* [About syncing [!DNL Google Analytics] conversion metrics](data-source-about.md)
>* [Prerequisites for configuring a [!DNL Google Analytics] data source](data-source-prerequisites.md)
>* [Configure a [!DNL Google Analytics] view as a data source](data-source-configure.md)
>* [Edit a [!DNL Google Analytics] data source](data-source-edit.md)
>* [Pause syncing of a data source](data-source-pause.md)
>* [Reauthenticate a [!DNL Google Analytics] data source](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] data source settings](data-source-settings.md)
