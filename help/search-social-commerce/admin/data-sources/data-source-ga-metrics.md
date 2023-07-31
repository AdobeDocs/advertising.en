---
title: Available [!DNL Google Analytics] metrics
description: Reference the [!DNL Google Analytics] metrics available for data sources.
role: User, Admin
exl-id: f7ac93e3-1aed-4165-ae65-7966ca192c84
feature: Search Admin, Search Data Sources
---
# Appendix - Available [!DNL Google Analytics] metrics

The following metrics, except for the exclusions noted, are available when they're enabled in the customer's implementation in [!DNL Google Analytics].

<!-- Notes as FYI to self:
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
