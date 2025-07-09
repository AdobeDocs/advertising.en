---
title: Create and edit campaign data in bulk using copy and paste
description: Learn how to manage campaign data in bulk using the copy and paste feature.
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
---
# Create and edit campaign data in bulk using copy and paste

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex], and existing [!DNL Baidu] accounts only*

*[!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] views*

You can to copy up to 10,000 rows from the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] views, and paste them into [!DNL Microsoft Excel] or another editor to edit any non-ID fields. You can then copy the [!DNL Excel] rows and paste them as tab-separated data back into the view to make the changes. The feature uses your computer's clipboard.

You can use this feature to edit existing campaign objects (with ID fields) and to create new campaign objects without ID fields.

## Copy data rows

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**.

1. Select the check box next to each row you want to copy.

   You can copy up to 10,000 rows.

1. In the toolbar above the data table, click ![More](/help/search-social-commerce/assets/more.png "More"), and then click **[!UICONTROL Copy]**.

   Alternately, you can use your operating systems's "copy" keyboard command, such as **[!DNL Ctrl+C]** for [!DNL Microsoft Windows] or **[!DNL Command-C]** for [!DNL Apple Mac].

1. In the [!UICONTROL Copy to Clipboard] dialog, click **[!UICONTROL Continue]**. When the data is ready to copy, click **[!UICONTROL Copy]**.

1. Paste the rows into [!DNL Excel] or another editor.

## Edit and create data rows

1. Edit the data according to the following requirements:

   * The pasted data must include a header row and the necessary campaign object values; see the required bulksheet columns for [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Display Network](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), [Yahoo! Japan](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md), and [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). The column order doesn't matter.
     
     * For existing objects that you want to edit, you must include all of the relevant ID columns, entity names, and the attribute to edit. Don't edit the numeric ID for the object.
     
     * For new campaign objects, include all relevant entity names and attributes but don't include object IDs (which are automatically generated). For example, if you create a new ad, leave the [!UICONTROL Ad ID] field blank. The ad network automatically creates an ID when you post the object.
   
   * The value in any non-required column may be null (blank), but each row must have the same number of tab-separated values.

1. Save the data as tab-separated values.

## Paste data rows into the campaign management views

>[!NOTE]
>
>If the pasted rows contain any data that's identical to that in the existing entities, or that duplicates an existing entity, then the duplicate data is ignored.

1. In [!DNL Excel] or other editor, copy the relevant tab-separated rows.

1. In the Search, Social, & Commerce main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. Open the view in which to paste data (**[!UICONTROL Live] > \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**).

1. In the toolbar above the data table, click ![More](/help/search-social-commerce/assets/more.png "More"), and then click **[!UICONTROL Paste]**.

   Alternately, you can use your operating systems's "paste" keyboard command, such as **[!DNL Ctrl+V]** for [!DNL Microsoft Windows] or **[!DNL Command-V]** for [!DNL Apple Mac].

1. Paste the data into the input box, and then click **[!UICONTROL Process]**.

1. (Optional) Enter additional details:
   
   * (If **[!UICONTROL Additional Details]** is compressed) Click ![Open](/help/search-social-commerce/assets/chevron-up.png "Open") to expand the details.
   
   * Enter an optional **[!UICONTROL Job Name]** and/or optional **[!UICONTROL Job Description]**.

1. Click **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [About managing campaign data using bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [Edit settings directly within a row](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [Manage campaigns](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [Manage ad groups](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [Manage keywords](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [Manage ads](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
