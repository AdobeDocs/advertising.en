---
title: '[!UICONTROL Google AI Max Search Term Combination Report]'
description: Learn about the [!UICONTROL Google AI Max Search Term Combination Report].
feature: Search Reports, Search Specialty Reports
---
# [!UICONTROL Google AI Max Search Term Combination Report]

*Applicable to [!DNL Google Ads] accounts with campaigns enabled for AI max only*

The [!UICONTROL Google AI Max Search Term Combination Report] shows how specific search queries are mapped to AI-generated headlines and dynamic landing pages and to conversion actions for ads in [!DNL Google Ads AI Max]-enabled campaigns within specified accounts. The report includes two sheets:

<!-- verify sheet names, and how they appear in CSV and TSV files (which you could open in a text editor) -->

* <!-- VERIFY -->[!UICONTROL XXXX] sheet: The performance of specific ad combinations and landing pages based on searches within the search network. The sheet includes impression, clicks, and cost data. By default, data includes one row for each search term, headline, and landing page combination that received at least one impression in the specified data range. The rows are in ascending order by date and then by campaign by default.

* <!-- VERIFY all, and explain all conversions-->[!UICONTROL Search Term x Conversion Action] sheet: [!DNL Google Ads]-tracked conversion data by conversion action for each search term and match type. The sheet includes the number of conversions and the conversion value, all conversions and the all conversions value, and cross-device conversions.

<!-- VERIFY ALL -->By default, data includes one row for each search term and conversion action combination in the specified data range. The rows are in ascending order by date and then by campaign by default.

<!-- Make sure I've documented all new report columns -->

Use this report to analyze intent and the performance of the resulting ad elements per query so that you can build robust negative keyword lists. Use it also to understand how each search term drove conversions, broken out by conversion action.

<!-- We're pulling data directly from GGL and not storing it, so no limitations on our end WRT date range. -->

## Default columns

For descriptions of all default and custom columns, see "[Report columns for specialty reports](specialty-report-columns.md)."

<!-- VERIFY -- probably more will be included by default -->

* [!UICONTROL Event Date]
* [!UICONTROL Account Name]
* [!UICONTROL Network Campaign ID]
* [!UICONTROL Campaign Name]
* [!UICONTROL Ad Group Name]
* [!UICONTROL Search Term]
* [!UICONTROL Headline 1]
* [!UICONTROL Headline 2]
* [!UICONTROL Landing Page]
* [!UICONTROL Impressions]
* [!UICONTROL Clicks]
* [!UICONTROL Cost]

>[!MORELIKETHIS]
>
>* [About specialty reports](specialty-report-about.md)
>* [Manage scheduled reports](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [Specialty report settings](specialty-report-settings.md)
>* [Report columns for specialty reports](specialty-report-columns.md)
