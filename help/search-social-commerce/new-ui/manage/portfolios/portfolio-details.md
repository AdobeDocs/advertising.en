---
title: (New UI) View View portfolio performance details
description: Learn how to view portfolio performance details, including actual and predicted metrics at the portfolio level and for each assigned campaign.
feature: Search Portfolios, Search Optimization
hide: yes
exl-id: b5178856-1b0e-45cf-a351-6f31c0b0ec76
---
# (New UI) View portfolio performance details

*Beta feature*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

The portfolio detail view includes the following information about a portfolio:

* The actual and predicted values for up to three performance metrics. The reports include the total metric values for the portfolio and the metric breakdown by date.<!-- Not for active portfolios only?  -->

* Model accuracy data for active portfolios, which shows how much the models deviated from predictions. The report shows the overall daily or rolling seven-day cost accuracy, click accuracy, and objective value accuracy.

  You can view data by click date (the default) or by transaction date.   You also can view the data as either a trend chart (the default) or as a table.

* The target spend versus the actual spend for active portfolios. You can optionally also include the total campaign budgets for the portfolio.

* The accuracy of cost, click, or [objective value](/help/search-social-commerce/glossary.md#o-p) predictions for active portfolios by ad network.<!-- Verify -->

* The portfolio settings.

  You can optionally open the portfolio settings to edit them.

## Open performance details for a portfolio

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Portfolios]**.

1. Click the portfolio name.

1. (Optional) From the **[!UICONTROL Granularity]** menu, change the data granularity between *[!UICONTROL Daily],* *[!UICONTROL Weekly],* or *[!UICONTROL Monthly].*

1. (Optional) To change the date range for the portfolio details, click the date range in the upper right, specify the date range, and then click **[!UICONTROL Apply]**.

## Customize the [!UICONTROL Portfolio Overview] tab

* (Optional) To customize the [!UICONTROL Portfolio Performance] reports, do any of the following:

  * To change the performance metrics used for both the total metrics and the detailed metrics, click **[!UICONTROL Metrics]** and select up to three metrics.
  
    The default metrics are *[!UICONTROL Cost]*, *[!UICONTROL Clicks]*, and the *[!UICONTROL Objective Value]*.<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->

  * For the detailed metrics:
  
    * Move the switch next to **[!UICONTROL Display predictions]** to show or hide the predicted metric values.
    
    * Switch between the chart view (![Chart View](/help/search-social-commerce/assets/chart-view.png "Chart View")) and table view (![Table View](/help/search-social-commerce/assets/table-view.png "Table View")).

    * (In chart view) To see data for any point on the chart, hold the cursor over that point.

* (Optional) To customize the [!UICONTROL Model accuracy] trend chart, do any of the following:

  * Switch between the chart view (![Chart View](/help/search-social-commerce/assets/chart-view.png "Chart View")) and table view (![Table View](/help/search-social-commerce/assets/table-view.png "Table View")).

  * Switch between viewing data by *[!UICONTROL Click Date]* and *[!UICONTROL Transaction Date]*.

  * Switch between viewing data about the *[!UICONTROL Daily Accuracy]* and the *[!UICONTROL 7 Day Rolling Accuracy]*.
  
    [!UICONTROL 7 Day Rolling Accuracy] is the average accuracy of the forecast for the previous seven days, expressed as a percentage. For example, the value for 8 May 2025 is the average accuracy for the period of 1 May - 7 May 2025.

  * (In chart view) To see data for any point on the chart, hold the cursor over that point.

* (Optional) To customize the [!UICONTROL Target vs actual spend] trend chart, do any of the following:

    * Move the switch next to **[!UICONTROL Display budget]** to show or hide the total campaign budget for each date.
    
    * To see data for any point on the chart, hold the cursor over that point.

* (Optional) To customize the [!UICONTROL Network Accuracy] trend chart, do any of the following:

  * Change the reported metric to *[!UICONTROL Cost]*, *[!UICONTROL Clicks]*, or *[!UICONTROL Objective Value]*.

  * To see data for any point on the chart, hold the cursor over that point.

## List the campaigns in the portfolio

* Click the **[!UICONTROL Campaigns]** tab.

## List the ad groups in the portfolio

* To view all ad groups in a campaign within the portfolio, click the **[!UICONTROL Campaigns]** tab, and then click the campaign name.

## List the keywords in the portfolio

* To view all keywords in the portfolio, click the **[!UICONTROL Keywords]** tab.

* To view all keywords in an ad group within the portfolio, click the **[!UICONTROL Ad Groups]** tab, and then click the ad group name.

## View and edit the portfolio settings

* To view or hide the portfolio settings, click **[!UICONTROL Portfolio Settings]**.

   * To edit visible portfolio settings, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit") next to the setting section and [edit the portfolio settings](portfolio-edit.md).

For more information about the portfolio settings, see the Optimization Guide, which is available from within Search, Social, & Commerce.

>[!MORELIKETHIS]
>
>* [(New UI) About portfolios](portfolio-about.md)
>* [(New UI) Edit a portfolio](portfolio-edit.md)
>* [(New UI) Download data in the [!UICONTROL Portfolios] view](portfolio-view-report.md)
