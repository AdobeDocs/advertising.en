---
title: (New UI) The data used for reports
description: Learn about the different types of data available in data views and custom reports.
feature: Search Reports
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: ff99aaef-142d-4c93-a88c-011e979e3843
    internal-label: Advanced reports
  - id: c916feea-e212-4773-b673-4daed287b8a3
    internal-label: Assist reports
  - id: adcb1be7-7ed0-464d-a8d4-c905c9d47742
    internal-label: Basic reports
  - id: fa0141e5-dc99-4fbd-9c0e-40aff66de606
    internal-label: Model accuracy reports
  - id: b36a77b1-3c8f-4e1c-8b0b-6e0ba3fb2664
    internal-label: Specialty reports
  - id: e246c273-d720-4ece-b29b-7aaba7d50169
    internal-label: Reports
---
# (New UI) The data used for reports

Search, Social, & Commerce includes a comprehensive set of performance reports based on click and conversion data. You can view basic performance data for the various components of a portfolio or ad account from the [!UICONTROL Portfolios] and [!UICONTROL Campaigns] views as well as by generating various basic and advanced reports.

Advertisers who use the Adobe Advertising conversion tracking service also can identify the number of clicks for a geographical location or domain name of a referring website, how ads in each channel and the various events leading to a conversion contribute to the overall conversion rate, and the distribution of conversions for a single [conversion metric](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) by marketing channel. The reports available vary by user account type. The Adobe Account Team has access to all reports.

Most reports can be customized to display only the information you want to see. The following standard metrics are available in most reports and are calculated at the ad level:

* **Standard performance metrics:**
   
   * **[!UICONTROL Impressions]:** The total number of times the ad was placed.
   
   * **[!UICONTROL Clicks]:** The total number of times a link in the ad was clicked.
   
   * **[!UICONTROL Cost]:** The total cost of the ad. The cost for pay-per-click (PPC) advertising is always the number of clicks multiplied by the cost per click.
   
   * **[!UICONTROL Cost per Click]:** The average cost for one click for an ad, which is the cost of the ad divided by the total number of clicks for the ad. For example, if you spend 100 USD for an ad impression and the ad generates 10 clicks, then the cost per click is 100 USD/10=10 USD per click.
   
   * **[!UICONTROL Average Position]:** (When applicable) The average position of an ad that has been placed, weighted by the number of impressions.
   
   * **[!UICONTROL Estimated Clicks]:** (Included in advanced reports for advertisers with the Adobe Advertising conversion tracking service only) The total number of estimated clicks for a city or domain name of a referring website. This may include data for ad networks for which an advertiser doesn't have an advertising account.

* **Conversion metrics:** The total number of conversions for each of the advertiser's conversion metrics, or transaction data tracked toward a conversion metric. This can include conversion and site engagement metrics, but not calculated metrics and advanced calculated metrics, that are synced from Adobe Analytics.

  This also may include [[!DNL Google Ads]-tracked conversions](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) and [[!DNL Google Analytics]-tracked conversions](/help/search-social-commerce/admin/data-sources/data-source-about.md) that are synced for the advertiser account.

* **Custom metrics:** Your own metrics, which you derive by creating formulas based on existing metrics (such as the cost per order).

## Data availability

When you generate reports, you can choose how to attribute conversion data in a series of events that lead to a conversion. For example, you can choose to attribute the entire conversion to the last event or to weight the last event more than the others. By default, conversions are attributed to the last event.

Depending on the attribution rule you specify for the report, data for each report type is available for the following dates.

| Report Group | Report | Dates for Which Data Is Available |
| --- | --- | --- |
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | Beginning on 15 May 2021.<br><br><b>Exception:</b> Prominence metrics data is available beginning on 8 September 2022. |
| | All other [!UICONTROL Basic Reports] | The previous 36 months.<br><br><b>Exception:</b> Prominence metrics data is available beginning on 8 September 2022. |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | The previous 45 days. |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | The previous two (2) months plus the current month. |
| [!UICONTROL Assist Reports] | All | The previous 18 months. |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | The previous year.|
| | [!UICONTROL Google Asset Group Performance Report] | No limitations |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report], [!UICONTROL MSA Network Impression Share Report], [!UICONTROL MSA Network Performance Report] | The last 180 days. |
| | [!UICONTROL RSA Assets Report] | Beginning on 10 August 2022. |
| | All other [!UICONTROL Specialty Reports] | The previous two (2) months. |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | The previous 18 months. |
| [!UICONTROL Change History Report] | &mdash; | The previous 31 days. |

>[!MORELIKETHIS]
>
>* [About reports](report-about.md)
>* [Initial setup tasks for reports](initial-setup.md)
