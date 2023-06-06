---
title: Download data from a campaign management view
description: Learn how to download data from most campaign management views.
---
# Download data from a campaign management view

You can download data from the [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] views except for the [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences], and [!UICONTROL Extensions] views. You can download either:

* A report in [!DNL XLSM] (macro-enabled [!DNL Microsoft® Excel] spreadsheet) format. If you select specific rows in the view, then the report includes one row for each selected row. If you don't select any rows, then one row is created for each row in the view.

* A bulksheet file in TXT format that includes all relevant child entities. If you select rows for entities on multiple ad networks, then one file is created for each relevant ad network. If you don't select any rows, then one file is created for each ad network represented in the view. Bulksheet files generated for different ad networks include different data columns.

  If you generate data for multiple campaigns and the combined data consists of over 500,000 rows, then the data is further split by campaign into two or more files, as necessary, named `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt`, and so on.

  Each bulksheet file in the [!UICONTROL Downloads] panel is also listed on the [!UICONTROL Bulksheets] view. When the file is created, you receive an email notification with a link from which you can download the file; depending on the amount of data being compiled, the notification may take several minutes or more. If, however, the file generation fails, then an error file is listed on the Bulksheets view, and you receive an email notification with a link to the error file. Deleting a bulksheet file from either the [!UICONTROL Download] panel or the [!UICONTROL Bulksheets] tab deletes it from both locations.

1. (Optional) Select individual rows to include in the file.

   Otherwise, all data in the view is included.

1. On the right of the toolbar, click ![Report Download](/help/search-social-commerce/assets/download.png "Report Download").

1. Click ![Create](/help/search-social-commerce/assets/add.png "Create") **[!UICONTROL Create]**, optionally add the file name, and then click either **[!UICONTROL Report]** or **[!UICONTROL Bulksheet]**.

1. (Optional) Once the report job is complete, click ![Report Download](/help/search-social-commerce/assets/download.png "Report Download") to view the [!UICONTROL Available Reports] panel, and then download or delete the report:

   * To open or save the file according to your browser's normal procedure, click ![Download spreadsheet](/help/search-social-commerce/assets/download-spreadsheet.png "Download spreadsheet").
   
     For more information about your browser procedure, see your browser’s online help.

   * To delete the file, click ![Delete](/help/search-social-commerce/assets/delete.png "Delete").
  
>[!MORELIKETHIS]
>
>[Delete a performance data report or bulksheet file from the [!UICONTROL Downloads] menu](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
