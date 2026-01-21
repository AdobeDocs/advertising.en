---
title: Bulk edit portfolio settings using bulksheet files
description: Learn how to edit the settings for multiple portfolios using a bulksheet file.
feature: Search Portfolios, Search Optimization
hide: yes
exl-id: 20f7419d-9f5e-4477-ae8d-8b85a79b1e81
---
# Bulk edit portfolio settings using bulksheet files

*Beta feature*

A portfolio bulksheet is a file that contains portfolio settings in a specific format and can be used to quickly review and modify the settings. You can generate (download) bulksheets with settings for one or more portfolios. The file is downloaded as an [!DNL Excel] workbook with two worksheets (XLSX format). The workbook includes:

* A read-only [!UICONTROL Instructions] worksheet with information about editing the fields.

* A [!UICONTROL Portfolio Settings Edit] tab, with one row per included portfolio. You can optionally edit the fields as needed, save the file locally, and subsequently [upload the edited file](#portfolio-bulksheet-upload) to Search, Social, & Commerce. The editable fields are highlighted in color.

## Download a bulksheet file with portfolio settings

1. (Optional) Select the check box next to each portfolio to include in the bulksheet.

   If you don't select specific portfolios, you can download the settings for all portfolios.

1. In the toolbar above the data table, click:

   * (For all portfolios) **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export All Portfolios]**.
   
   * (For selected portfolios) **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export Selected Portfolios]**.

1. Enter the name of the bulksheet file to create, and then click **[!UICONTROL Export Now]**.

   The file is saved to your browser's default Downloads folder.

## Upload a bulksheet file with updated portfolio settings {#portfolio-bulksheet-upload}

The file must be XLSX format.

1. In the toolbar above the data table, click **[!UICONTROL Bulk Operations]** > **[!UICONTROL Import Portfolio Details]**. <!-- Should be "Import Portfolio Settings" -- "Details" may be too vague and suggest it may include something else. -->

1. In the [!UICONTROL Import Portfolio Details File] dialog:<!-- reword if we change the name of the operation -->

    1. Either drag and drop a file into the box, or click **[!UICONTROL Browse File]**<!-- "Browse for file" or just "Browse"??? --> to select a file from your device or network.

    1. Click **[!UICONTROL Import]**.

You can check the status of the upload from the [!UICONTROL Global Sync Status] button (![Global Sync Status](/help/search-social-commerce/assets/global-sync-status.png "Global Sync Status")) next to the date range selector.<!-- icon similar to Refresh -->. If any of the changes weren't successful, then you can download an error file showing what failed.

Notifications are also added to Notification Center, and you can open the Notifications pane from the ![Notifications](/help/search-social-commerce/assets/notifications-new.png "Notifications") icon next to the [!UICONTROL Global Sync Status] button (![Global Sync Status](/help/search-social-commerce/assets/global-sync-status.png "Global Sync Status")).

## Data requirements for uploaded bulksheet files

All bulksheet files must include the column [!UICONTROL Portfolio ID], and each data row must include a value for the [!UICONTROL Portfolio ID] to be actionable. For more information about the data requirements, see the [!UICONTROL Instructions] tab on the downloaded bulksheet file.

For explanations of the portfolio setting columns on the [!UICONTROL Portfolio Settings Edit] tab, see the Optimization Guide, which is available from within Search, Social, & Commerce.

<!--
## Data fields on the [!UICONTROL Portfolio Settings Edit] tab

| Field | Required to import data? | Description |
| ----- | ------------------------ | ----------- |
| Portfolio ID |  |  |
| Portfolio Name |  |  |
| Status |  |  |
| Spend Strategy |  |  |
| Target |  |  |
| Hybrid |  |  |
| Auto adjust campaign budgets |  |  |
| Spend Multiple |  |  |
| Minimum Campaign Budget |  |  |
| Objective |  |  |
| Cost Half-Life |  |  |
| Revenue Half-Life |  |  |
| Min. Target CPA |  |  |
| Max. Target CPA |  |  |
| Min. Target ROAS |  |  |
| Max. Target ROAS |  |  |

-->

>[!MORELIKETHIS]
>
>* [(New UI) Edit a portfolio](portfolio-edit.md)
>* [Create a portfolio](portfolio-create.md)
>* [(New UI) About portfolios](portfolio-about.md)
