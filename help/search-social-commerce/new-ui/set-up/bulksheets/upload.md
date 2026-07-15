---
title: (New UI) Upload a bulksheet or corrected error file
description: Learn how to manually upload a bulksheet file or corrected landing page validation error file in the new Search, Social, & Commerce UI.
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
# (New UI) Upload a bulksheet or corrected error file

You can upload bulksheet files, corrected landing page validation error files, and other corrected error files from your device or network for [supported ad networks](about.md#bulksheet-functionality-by-network). Any custom columns in the file are deleted when you upload the file.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. In the toolbar, click **[!UICONTROL Bulk Operations]** \> **[!UICONTROL Upload Bulksheet]**.

1. Enter or select information in the [[!UICONTROL Upload Bulksheet] settings](#bulksheet-upload-settings).

1. Click **[!UICONTROL Upload]**.

When the task begins, the file is listed in the [!UICONTROL Bulksheets] view. When email notifications for bulksheets are [enabled within [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md), then an email notification is sent with a link to the file when the job is complete. Depending on the amount of data compiled, the email notification may take several minutes or more. If the file generation fails, then an error file is listed in the [!UICONTROL Bulksheets] view and an email notification is sent with a link to the error file.

>[!NOTE]
>
>If you post the bulksheet data to the ad network, you can follow the progress of the file in the [!UICONTROL Progress] column in the [!UICONTROL Bulksheets] view. Large amounts of data take longer to be posted.

## Upload settings for bulksheets and corrected error files {#bulksheet-upload-settings}

| Parameter | Description |
|----|----|
| [!UICONTROL File to Upload] | The file to upload. Specify the file either by clicking **[!UICONTROL Choose File]** to locate the file on your device or network.<br><br>Bulksheet files can be up to 2.5 GB (about 2.5 million rows) and must have one of the following file extensions: *[!UICONTROL .tsv]* (for tab-separated values), *[!UICONTROL .txt]* (for Unicode-compliant ASCII text), *[!UICONTROL .csv]* (for comma-separated values), or *[!UICONTROL .zip]* (for compressed ZIP format, which unzips to a TSV file). The file name can't include the following characters: `# % & * \| \ : " < > . ? /`<br><br>**Tip:** For data that includes international characters, use files in TSV or TXT format. |
| [!UICONTROL Single Account] | Whether the file applies to one account: *[!UICONTROL Yes]* (for one account) or *[!UICONTROL No]* (for multiple accounts). |
| [!UICONTROL Account (Search Engine)] | (When the file applies to a single account) The account to which to upload the data. |
| [!UICONTROL Search Engine] | (When the file applies to multiple accounts) The ad network to which to upload the data.<br><br>**Note:** Bid changes for keywords in optimized portfolios aren't supported with multiple-account bulksheets. |
| [!UICONTROL Scheduling] | When or if to post the file to the specified ad network:<ul><li>*[!UICONTROL Post to search engine now]* (the default): Begins posting the data immediately.</li><li>*[!UICONTROL Post to search engine on \[specified date\] \[specified time\]]:* Begins posting the data on the specified date and time; the default is tomorrow at 02:00 (2 a.m.). To change the date, enter a date in the format DD/MM/YYYY or click the calendar icon to open the calendar and select a date. To change the time, select a time (in 15-minute intervals) from the list.</li><li>*[!UICONTROL Preview only]:* Uploads the file to Search, Social, & Commerce without posting the data to the ad network; you can still post the file later. When the bulksheet file is more than 10 MB but smaller than 2 GB, the file is in ZIP format; you don't need to unzip the file to post it.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Whether to include tracking templates and landing page suffixes (for applicable ad networks) in accounts with tracking templates, or destination URLs with embedded tracking codes in accounts with destination URLs, for all keywords, ads, placements, sitelinks, and [!DNL Google Ads] product groups in the posting: *[!UICONTROL Yes]* (the default) or *[!UICONTROL No]*. It doesn't matter if the bid units are in a portfolio.<br><br>If you select *[!UICONTROL Yes]*, then the URLs are generated according to the parameters in the [!UICONTROL Tracking Methods] section of the relevant account settings or campaign settings. By default, if tracking URLs exist, they aren't regenerated unless new ones are needed (such as if the keyword match type, the ad text, or the tracking parameters for the relevant accounts have changed).<br><br>If you select *[!UICONTROL No]*, then you can still generate tracking URLs later by manually posting the uploaded file.<br><br>**Note:** If the advertiser uses Adobe Advertising conversion tracking and the base URL has changed, you must generate new tracking URLs unless the account is configured to automatically generate and upload tracking URLs. |
| [!UICONTROL Replace Media Optimizer Tracking] | (Available when [!UICONTROL Generate Tracking URLs] is *[!UICONTROL Yes]*) Replaces any existing Adobe Advertising tracking in the uploaded file's URLs with newly generated tracking. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Allows budget changes to campaigns in optimized portfolios based on posted data. By default, this option isn't selected. If you select this option, any specified campaign budget changes are applicable until the optimization capability determines that the budget should be reallocated (usually at the next bid cycle).<br><br>**Note:** Any budget changes resulting from the posted data for campaigns in non-optimized portfolios occur when the file is posted. Changes appear in the campaign management views the next day. |
| [!UICONTROL Enable bidding on ads within portfolios] | When the included campaign components are in an optimized portfolio, this feature overrides the optimization strategy and allows bid changes based on the data in the bulksheet until a specified end date. If you select this option, then specify an end date between 1-7 days away in the **[!UICONTROL Hold bulksheet bids until]** field. |

>[!MORELIKETHIS]
>
>* [(New UI) About managing campaign data using bulksheets](about.md)
>* [(New UI) Download/Create a bulksheet file](download.md)
>* [(New UI) Post bulksheets or corrected error files](post.md)
>* [(New UI) Validate landing pages in bulksheet files](validate-landing-pages.md)
