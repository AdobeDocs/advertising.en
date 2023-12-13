---
title: Validate landing pages in bulksheet files
description: Learn how to validate the destination URLs in a single-account bulksheet file.
exl-id: 191cb1bc-54a9-4c6c-a29c-f3cbae08e0d8
feature: Search Bulksheets
---
# Validate landing pages in bulksheet files

*Accounts with destination URLs only*

You can validate the landing pages in all destination URLs in a single-account bulksheet file. You can specify any phrases and URLs that indicate an invalid page and optionally report landing page redirects as errors. Search, Social, & Commerce checks for your specified conditions and for missing landing pages (which result in HTTP 404, or "Not Found" errors).

When it finds errors, Search, Social, & Commerce creates a bulksheet error file that includes all rows in the original bulksheet and error messages for all rows with invalid landing page. The errors are noted in the [!UICONTROL EF Errors] column. The file name convention is `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

You can later download the file, correct the errors and upload the corrected file, and then post the corrected file to the ad network account.

>[!NOTE]
>
>* This feature doesn't validate values in the Base URL/Final URL column.
>* You can post bulksheet files while they are being validated, or even if errors are found.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Bulksheets]**.

1. Select the check box next to each file to validate.

1. In the toolbar above the data table, click **[!UICONTROL Validate URLs]**.

1. In the dialog box, enter information in the fields, and then click **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** Text in the body of a landing page that indicates the page is invalid. To specify multiple values, enter them on separate lines.
   
   **[!UICONTROL Enter invalid landing pages(one per line):]** The URLs of pages that are invalid as landing pages. To specify multiple values, enter them on separate lines.
   
   **[!UICONTROL User Agent:]** How the landing page validation agent is identified to the web server on which the landing page resides. The default is default, which attributes views by the agent to an anonymous [!DNL Mozilla Firefox] user. If the web server blocks requests from anonymous [!DNL Mozilla Firefox] users, then enter the name of a different agent. For example, for [!DNL Googlebot], enter `Googlebot/2.1;+http://www.google.com/bot.html`.
   
   **[!UICONTROL Report redirects as errors]:** When a landing page redirects to another page (for example, if the landing page is missing and the site displays a substitute page), the [!UICONTROL ER Errors] column in the landing page error file indicates the URL to which the landing page is redirected.

When the task begins, a new row is added to the [!UICONTROL Bulksheets view]. When the file is created, an email notification is sent with a link to the file. Depending on the amount of data compiled, the email notification may take several minutes or more. You can download the file to edit it and then reupload it for posting, or you can post the file as-is. If the file generation fails, however, then an error file is listed on the [!UICONTROL Bulksheet Management] page, and an email notification is sent with a link to the error file.

>[!NOTE]
>
>* Large files take longer to validate.
>* Bulksheet files for multiple campaigns can contain up to 500,000 data rows. If you generate data for multiple campaigns and the combined data consists of over 500,000 rows, then the data is split by campaign into two or more files named `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`, and so on.

>[!MORELIKETHIS]
>
>* [About managing campaign data using bulksheets](bulksheet-about.md)
>* [Delete uploaded bulksheets and error files](bulksheet-delete.md)
>* [Post bulksheets or corrected error files](bulksheet-post.md)
>* [Stop a bulksheet job in progress](bulksheet-stop-job.md)
>* [Upload a bulksheet or corrected error file](bulksheet-upload.md)
>* [Export a generated or uploaded bulksheet file](bulksheet-export.md)
