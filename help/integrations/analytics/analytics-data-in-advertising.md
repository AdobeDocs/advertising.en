---
title: '[!DNL Analytics] Data in  Adobe Advertising'
description: '[!DNL Analytics] Data in Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
---
# [!DNL Analytics] Data in Adobe Advertising

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

## Analytics Segments

All segments created in [!DNL Analytics] and published to Experience Cloud.

New segments take 24-48 hours to appear in Adobe Advertising. Updates to existing segments are synchronized within about eight hours.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Site Engagement Metrics

>[!NOTE]
>
>* [!DNL Analytics] passes events for the EF ID eVar into Adobe Advertising.  The default integration doesn't support sending calculated metrics or other dimensions (eVars) into Adobe Advertising. If the calculated metric can be wholly captured in a custom event, however, then Adobe Advertising can ingest the custom event.
>* [!DNL Analytics] passes data to Adobe Advertising hourly.

* [!UICONTROL Timespent_secs_1stvisit]: The number of seconds spent on the site during the visitor's first visit.
* [!UICONTROL Timespent_secs_total]: The total number of seconds spent on the site across all visits within the click lookback window.
* [!UICONTROL Pageviews_1stvisit]: The number of page views on the site during the visitor's first visit.
* [!UICONTROL Pageviews_total]: The total number of page views on the site across all visits within the click lookback window.
* [[!UICONTROL Bounces] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: The number of times that [!DNL Analytics] collected an [!UICONTROL EF ID].

## Conversion Metrics

[!DNL Analytics] passes conversion metrics to Adobe Advertising daily.

### Standard Conversion Metrics

* [[!UICONTROL Revenue] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Custom Conversion Metrics

These metrics are specific to the report suite, so the available metrics vary for each customer and report suite.<!-- Does this include metrics with eVars and props, do those need a separate header? -->

<!-- edit below as needed -->

### Custom Conversion Metrics Created from eVars and Props

The available metrics vary for each customer. See "[](/help/integrations/analytics/custom-metrics-from-evars.md)."

### Reserved Conversion Metrics

These metrics are specific to the report suite, so the available metrics vary for each customer and report suite.

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising Metrics in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
