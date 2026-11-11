---
title: (New UI) View a portfolio's change history and bid change history
description: Learn how to view portfolio changes and bid change history, change date ranges, filter portfolio changes, and generate, download, and delete history reports in Adobe Advertising Search, Social, & Commerce.
feature: Search Portfolios, Search Optimization
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
---
# (New UI) View a portfolio's change history and bid change history

*Beta feature*

You can view a log of changes made to the portfolio during any date range. The actions logged include the portfolio creation, all changes to the portfolio's settings, all campaigns assigned to or unassigned from the portfolio, all constraints applied to or removed from bid units in the portfolio, all constraints on bid units in the portfolio that have expired, and other actions that affect the portfolio.

The [!UICONTROL Change History] dialog includes a [!UICONTROL Portfolio Change History] tab for portfolio changes and a [!UICONTROL Portfolio Bid Change History] tab for bid history. By default, both tabs show the last 180 days, ending yesterday.

You can filter portfolio changes by category and change the date range for either tab. You can also download the data to a spreadsheet file.

## View a portfolio's change history {#portfolio-change-history}

Information for each change includes the [!UICONTROL Change Date], [!UICONTROL Changed By], [!UICONTROL Change Type], and [!UICONTROL Description]. Changes are listed from newest to oldest.

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Portfolios]**.

1. Hold the cursor over the portfolio row and click **[!UICONTROL ...] > [!UICONTROL Change History]**.

1. In the [!UICONTROL Change History] dialog, view the **[!UICONTROL Portfolio Change History]** tab.

1. (Optional) Change the information that's displayed:

   * Click ![Calendar](/help/search-social-commerce/assets/calendar-new.png "Calendar") to change the date range for the report.

   * Click ![Filter](/help/search-social-commerce/assets/filter-new.png "Filter") to filter the data by category: [!UICONTROL All], [!UICONTROL Objective], [!UICONTROL Campaign], [!UICONTROL Target], [!UICONTROL Constraints], [!UICONTROL Optimization Levers], or [!UICONTROL Others].

## View a portfolio's bid change history {#portfolio-bid-change-history}

1. [Open the portfolio's change history](#portfolio-change-history).

1. Click the **[!UICONTROL Portfolio Bid Change History]** tab.

1. (Optional) Click ![Calendar](/help/search-social-commerce/assets/calendar-new.png "Calendar") to change the date range.

1. (Optional) Click the date column heading to sort the list by date in ascending or descending order.

To view the history for an individual bid unit, [open the bid unit details from the portfolio's performance details](portfolio-details.md#bid-unit-history). You can also [open bid unit history from the [!UICONTROL Keywords] view](/help/search-social-commerce/new-ui/manage/keywords/keyword-manage.md#bid-unit-history) when the [!UICONTROL Bid Unit ID] column is available.

## Manage reports for portfolio change histories

You can download additional information about the change history for a portfolio to a file in [!DNL Microsoft Excel] workbook (XLSX file) format. The report includes the numeric change ID, the old and new values, the change type (such as "added" or "modified"), the action type (such as "Budget" or "Portfolio Name") and subtype when applicable, the time, and the user name.

You can also generate, download, and delete reports from the [!UICONTROL Portfolio Bid Change History] tab. The report settings are titled [!UICONTROL Portfolio History] for portfolio changes and [!UICONTROL Portfolio Bid History] for bid history.

### Generate a report with the filtered data rows

1. [Open the portfolio's change history](#portfolio-change-history), and then click the tab whose data you want to download.

1. In the upper right, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report").

1. In the [!UICONTROL Portfolio History] or [!UICONTROL Portfolio Bid History] settings, accept the default report name or enter a unique report name, and then click **[!UICONTROL Generate]**.

   By default, the report name includes the history type and the date and time in `YYYYMMDD_HHmm` format, such as "portfolioChangeHistory_20260402_1326." If the name already exists, a numeric suffix is added.

   The file is added to the [!UICONTROL Recently Generated] list.

1. (Optional) To download the file once it's completed, click ![Download](/help/search-social-commerce/assets/download.png "Download") next to the file name.

   The file is downloaded according to your browser's normal procedure.

### Download a completed report

1. [Open the portfolio's change history](#portfolio-change-history), and then click the tab from which you generated the report.

1. In the upper right, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report").

1. In the [!UICONTROL Recently Generated] list in the [!UICONTROL Portfolio History] or [!UICONTROL Portfolio Bid History] settings, click ![Download](/help/search-social-commerce/assets/download.png "Download") next to the file name.

   The file is downloaded according to your browser's normal procedure.

### Delete a completed report

1. [Open the portfolio's change history](#portfolio-change-history), and then click the tab from which you generated the report.

1. In the upper right, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report").

1. In the [!UICONTROL Recently Generated] list in the [!UICONTROL Portfolio History] or [!UICONTROL Portfolio Bid History] settings, click ![Delete](/help/search-social-commerce/assets/delete-new.png "Delete") next to the file name.

>[!MORELIKETHIS]
>
>* [Create a portfolio](portfolio-create.md)
>* [(New UI) Edit a portfolio](portfolio-edit.md)
>* [(New UI) View portfolio performance details](portfolio-details.md)
>* [(New UI) Download data in the [!UICONTROL Portfolios] view](portfolio-view-report.md)
>* [About portfolios](portfolio-about.md)
