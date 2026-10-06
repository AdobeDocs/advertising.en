---
title: '[!UICONTROL Label Classification Report]'
description: Learn about the [!UICONTROL Label Classification Report].
feature: Search Reports, Search Basic Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
  - id: 1d59f142-734e-5689-9ee3-a3bf4d5c5a51
    internal-label: Search Basic Reports
---
# [!UICONTROL Label Classification Report]

The [!UICONTROL Label Classification Report] includes cost, click, and (optionally) conversion data by keyword-level or ad-level label classification aggregated across ad networks, accounts, campaigns, or ad groups. By default, the data includes one row for each applicable keyword-level label classification for keywords, ads, and placements that received impressions for each time unit in the specified date range. The rows are in ascending order first by the start date for the time unit, then by label classification, and then by label value, by default.

You can view data for the previous 36 months.

>[!NOTE]
>
>* Reporting by ad-level label classifications isn't available for [!DNL Microsoft Advertising] dynamic search ad (DSA) campaigns.
>* More than one label classification may apply to the same entity, so the total for each metric may be higher than the actual total for the entity. For example, say a keyword "suede shoes" has two label values, "suede" and "footwear," and the keyword received 100 clicks. The Clicks column would show "100" for each of those label values, so the total for both rows would be "200."
* Any changes you make to label classifications and the child label values for an entity are visible in about one hour.

## Default columns

For descriptions of all default and custom columns, see "[Report columns for basic and advanced reports](basic-advanced-report-columns.md)."

* [!UICONTROL Label Classification]
* [!UICONTROL Label Value]
* [!UICONTROL Start Date]
* [!UICONTROL End Date]
* [!UICONTROL Impressions]
* [!UICONTROL Cost]
* [!UICONTROL Clicks]
* [!UICONTROL CPC]
* [!UICONTROL Avg Position]
* [!UICONTROL Impr. (Abs. Top) %]
* [!UICONTROL Impr. (Top) %]

>[!MORELIKETHIS]
>
>* [About basic and advanced reports](basic-advanced-report-about.md)
>* [Manage scheduled reports](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [Basic and advanced report settings](basic-advanced-report-settings.md)
