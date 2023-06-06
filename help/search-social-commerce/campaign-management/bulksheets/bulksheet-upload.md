---
title: Upload a bulksheet or corrected error file
description: Learn how to manually upload a bulksheet file or corrected landing page validation error file. 
---
# Upload a bulksheet or corrected error file

You can upload bulksheet files, corrected landing page validation error files, and other corrected error files from your device or network for [supported ad networks](bulksheet-about.md#bulksheet-functionality-by-network). Any custom columns in the file are deleted when you upload the file.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Bulksheets]**.

1. In the toolbar above the data table, click **[!UICONTROL Upload Bulksheet]**.

1. Enter or select information in the [[!UICONTROL Upload Bulksheet] settings](#bulksheet-upload-settings).

1. Click **[!UICONTROL Apply]**.

When the task begins, the file is listed in the [!UICONTROL Bulksheets] view. When the file is complete, an email notification is sent with a link to the file. Depending on the amount of data compiled, the email notification may take several minutes or more. If the file generation fails, however, then an error file is listed on the [!UICONTROL Bulksheets] view, and an email notification is sent with a link to the error file.

>[!NOTE]
>
>If you post the bulksheet data to the ad network, you can follow the progress of the file in the [!UICONTROL Progress] column in the [!UICONTROL Bulksheets] view. Large amounts of data take longer to be posted.

## Upload settings for bulksheets and corrected error files {#bulksheet-upload-settings}

| Parameter | Description |
|----|----|
| [!UICONTROL File to Upload] | The file to upload. Specify the file either by entering the full path and file name or by clicking <b>[!UICONTROL Browse]</b> to locate the file on your device or network.<br><br>Bulksheet files can be up to 2.5 GB (about 2.5 million rows) and must have one of the following file extensions: <i>[!UICONTROL .tsv]</i> (for tab-separated values), <i>[!UICONTROL .txt]</i> (for Unicode-compliant ASCII text), <i>[!UICONTROL .csv]</i> (for comma-separated values), or <i>[!UICONTROL .zip]</i> (for compressed ZIP format, which unzips to a TSV file). The file name can't include the following characters: `# % &amp; * | \ : &quot; &lt; &gt; . ? /`<br><br><b>Tip:</b> For data that includes international characters, use files in TSV or TXT format. |
| [!UICONTROL Single Account] | Whether the file applies to one account: <i>[!UICONTROL Yes]</i> (for one account) or <i>[!UICONTROL No]</i>(for multiple accounts). |
| [!UICONTROL Account (Search Engine)] | (When the file applies to a single account) The account to which to upload the data. |
| [!UICONTROL Search Engine] | (When the file applies to multiple accounts) The ad network to which to upload the data. |
| [!UICONTROL Scheduling] | When or if to post the file to the specified ad network:<ul><li><i>[!UICONTROL Post to ad network now]</i> (the default): Begins posting the data immediately.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Begins posting the data on the specified date and time; the default is tomorrow at 02:00 (2 a.m.). To change the date, enter a date in the format DD/MM/YYYY or D/M/YYYY or click ![Calendar](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md "Calendar") to open the calendar and [select a date](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). To change the time, enter the time in the format HH/MM or H/M or select a time (in 15-minute intervals) from the list.</li><li><i>[!UICONTROL Preview only]:</i> To upload the file to Search, Social, & Commerce without posting the data to the ad network; you can still post the file later. When the bulksheet file is more than 10 MB but smaller than 2 GB, the file is in ZIP format; you don't need to unzip the file to post it.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Whether to include tracking templates and landing page suffixes (for applicable ad networks) in accounts with tracking templates, or destination URLs with embedded tracking codes in accounts with destination URLs, for all keywords, ads, placements, sitelinks, and [!DNL Google Ads] product groups in the posting: <i>[!UICONTROL Yes]</i> (the default) or <i>[!UICONTROL No]</i>. It doesn't matter if the bid units are in a portfolio.<br><br>If you select <i>[!UICONTROL Yes]</i>, then the URLs are generated according to the parameters in the [!UICONTROL Tracking Methods] section of the relevant account settings or campaign settings. By default, if tracking URLs exist, they aren't regenerated unless new ones are needed (such as if the keyword match type, the ad text, or the tracking parameters for the relevant accounts have changed).<br><br>If you select <i>[!UICONTROL No]</i>, then you can still generate tracking URLs later by manually posting the uploaded file.<br><br><b>Note:</b> If the advertiser uses Adobe Advertising conversion tracking and the base URL has changed, you must generate new tracking URLs unless the account is configured to automatically generate and upload tracking URLs. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Allows budget changes to campaigns in optimized portfolios based on posted data. By default, this option isn't selected. If you select this option, any specified campaign budget changes are applicable until the optimization capability determines that the budget should be reallocated (usually at the next bid cycle).<br><br><b>Note:</b> Any budget changes resulting from the posted data for campaigns in non-optimized portfolios occur when the file is posted. Changes appear in the campaign management views the next day. |
| [!UICONTROL Enable bidding on ads within portfolios] | When the included campaign components are in an optimized portfolio, this feature overrides the optimization strategy and allows bid changes based on the data in the bulksheet until a specified end date. If you select this option, specify an end date between 1-7 days away in the **[!UICONTROL Hold bulksheet bids until]** field. |

>[!MORELIKETHIS]
>
>* [About managing campaign data using bulksheets](bulksheet-about.md)
>* [Download/Create a bulksheet file](bulksheet-download.md)
>* [Post bulksheets or corrected error files](bulksheet-post.md)
>* [Validate landing pages in bulksheet files](bulksheet-validate-landing-pages.md)
>* [Export a generated or uploaded bulksheet file](bulksheet-export.md)
