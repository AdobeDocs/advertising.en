---
title: (New UI) Validate landing pages in bulksheet files
description: Learn how to validate the destination URLs in a single-account bulksheet file in the new Search, Social, & Commerce UI.
feature: Search Bulksheets
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: e58024d1-d6da-420c-80af-6be211808316
    internal-label: Bulksheets
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# (New UI) Validate landing pages in bulksheet files

*Accounts with destination URLs only*

You can validate the landing pages in all destination URLs in a single-account bulksheet file. You can specify any phrases and URLs that indicate an invalid page and optionally report landing page redirects as errors. Search, Social, & Commerce checks for your specified conditions and for missing landing pages (which result in HTTP 404, or "Not Found" errors).

When it finds errors, Search, Social, & Commerce creates a bulksheet error file that includes all rows in the original bulksheet and error messages for all rows with invalid landing pages. The errors are noted in the [!UICONTROL EF Errors] column. The file name convention is `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

You can later download the file, correct the errors and upload the corrected file, and then post the corrected file to the ad network account.

>[!NOTE]
>
>* This feature doesn't validate values in the Base URL/Final URL column.
>* You can post bulksheet files while they are being validated, or even if errors are found.

>[!IMPORTANT]
>
>Support for non-ASCII characters in landing page validation has been temporarily suspended. If your landing page URLs contain non-ASCII characters, contact technical support for assistance.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Select the check box next to each file to validate.

   >[!NOTE]
   >
   >You can validate only single-account EF bulksheets that aren't currently in progress. If you select a multi-account bulksheet or a bulksheet that's currently being processed, those files are excluded.

1. In the action bar, click **[!UICONTROL Validate URLs]**.

1. In the dialog, enter information in the fields, and then click **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page (one per line):]** Text in the body of a landing page that indicates the page is invalid. To specify multiple values, enter them on separate lines.

   **[!UICONTROL Enter invalid landing pages (one per line):]** The URLs of pages that are invalid as landing pages. To specify multiple values, enter them on separate lines.

   **[!UICONTROL User Agent:]** How the landing page validation agent is identified to the web server on which the landing page resides. The default is `default`, which attributes views by the agent to an anonymous [!DNL Mozilla Firefox] user. If the web server blocks requests from anonymous [!DNL Mozilla Firefox] users, then enter the name of a different agent. For example, for [!DNL Googlebot], enter `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]:** When a landing page redirects to another page (for example, if the landing page is missing and the site displays a substitute page), the [!UICONTROL EF Errors] column in the landing page error file indicates the URL to which the landing page is redirected.

When the task begins, a new row is added to the [!UICONTROL Bulksheets] view. When email notifications for bulksheets are [enabled within [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md), then an email notification with a link to the file is sent when the file is created. Depending on the amount of data compiled, the email notification may take several minutes or more. You can download the file to edit it and then reupload it for posting, or you can post the file as-is.

>[!NOTE]
>
>* Large files take longer to validate.
>* Bulksheet files for multiple campaigns can contain up to 500,000 data rows. If you generate data for multiple campaigns and the combined data consists of more than 500,000 rows, then the data is split by campaign into two or more files named `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`, and so on.

>[!MORELIKETHIS]
>
>* [(New UI) About managing campaign data using bulksheets](about.md)
>* [(New UI) Upload a bulksheet or corrected error file](upload.md)
>* [(New UI) Post bulksheets or corrected error files](post.md)
>* [(New UI) Delete uploaded bulksheets and error files](delete.md)
>* [(New UI) Stop a bulksheet job in progress](stop-job.md)
