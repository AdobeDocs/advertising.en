---
title: Post bulksheets or corrected error files
description: Learn how to post bulksheet files to your ad networks. 
---
# Post bulksheets or corrected error files

You can post existing bulksheet files or corrected error files to the relevant accounts for [supported ad networks](bulksheet-about.md#bulksheet-functionality-by-network). If the file is in ZIP format, you don't need to unzip it first.

Bulksheet files and error files are automatically deleted 30 days after they're uploaded or generated.

>[!NOTE]
>You can also post a bulksheet file or error file when you upload the file.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Bulksheets]**.

1. Select the check box next to each file to post.

1. In the toolbar above the data table, click **[!UICONTROL Post]**.

1. In the dialog box, enter or select information in the [[!UICONTROL Post Bulksheet] settings](#bulksheet-post-settings), and then click **[!UICONTROL Post]**.

   The same settings apply to all files you post.

When the task begins, the status and scheduled post date for the row are changed in the [!UICONTROL Bulksheets] view. When the file is posted, an email notification is sent with a link to the file. Depending on the amount of data compiled, the email notification may take several minutes or more. If any of the data can't be posted, however, then an error file is listed on the [!UICONTROL Bulksheets] view, and an email notification is sent with a link to the error file.

>[!NOTE]
>
>* Large amounts of data take longer to be posted. You can follow the progress of the file in the [!UICONTROL Progress] column in the [!UICONTROL Bulksheets] view.
>* All posted data is subject to the network's editorial process.
* Before the bulksheet file is posted, you can cancel the posting.

## Post settings for bulksheets and corrected error files {#bulksheet-post-settings}

| Parameter | Description |
|----|----|
| [!UICONTROL Account (Search Engine)] | The ad network account for which the data is posted. If you post multiple files simultaneously or one file that applies to multiple accounts, the value is <i>Multiple Accounts Selected</i>.<br><br>The first letter of the ad network name is in parentheses after the account name (such as "Acme Realty (G)" for a [!DNL Google Ads] account). |
| [!UICONTROL Scheduling] | When to post the file to the specified ad network:<ul><li><i>[!UICONTROL Post to ad network now]</i> (the default): Begins posting the data immediately.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Begins posting the data on the specified date and time; the default is tomorrow at 02:00 (2 a.m.). To change the date, enter a date in the format DD/MM/YYYY or D/M/YYYY or click ![Calendar](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md "Calendar") to open the calendar and [select a date](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). To change the time, enter the time in the format HH/MM or H/M or select a time (in 15-minute intervals) from the list.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Whether to include tracking templates and landing page suffixes (for applicable ad networks) in accounts with tracking templates, or destination URLs with embedded tracking codes in accounts with destination URLs, for all keywords, ads, placements, sitelinks, and [!DNL Google Ads] product groups in the posting: <i>[!UICONTROL Yes]</i> (the default) or <i>[!UICONTROL No]</i>. It doesn't matter if the bid units are in a portfolio.<br><br>If you select <i>[!UICONTROL Yes]</i>, then the URLs are generated according to the parameters in the [!UICONTROL Tracking Methods] section of the relevant account settings or campaign settings. By default, if tracking URLs exist, they aren't regenerated unless new ones are needed (such as if the keyword match type, the ad text, or the tracking parameters for the relevant accounts have changed).<br><br>If you select <i>[!UICONTROL No]</i>, then you can still generate tracking URLs later by manually posting the uploaded file.<br><br><b>Note:</b> If the advertiser uses Adobe Advertising conversion tracking and the base URL has changed, you must generate new tracking URLs unless the account is configured to automatically generate and upload tracking URLs. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Allows budget changes to campaigns in optimized portfolios based on posted data. By default, this option isn't selected. If you select this option, any specified campaign budget changes are applicable until the optimization capability determines that the budget should be reallocated (usually at the next bid cycle).<br><br><b>Note:</b> Any budget changes resulting from the posted data for campaigns in non-optimized portfolios occur when the file is posted. Changes appear in the campaign management views the next day. |
| [!UICONTROL Enable bidding on ads within portfolios] | When the included campaign components are in an optimized portfolio, this feature overrides the optimization strategy and allows bid changes based on the data in the bulksheet until a specified end date. If you select this option, specify an end date between 1-7 days away in the **[!UICONTROL Hold bulksheet bids until]** field. |

>[!MORELIKETHIS]
>
>* [About managing campaign data using bulksheets](bulksheet-about.md)
>* [Download/Create a bulksheet file](bulksheet-download.md)
>* [Upload bulksheets or corrected error files](bulksheet-upload.md)
>* [Validate landing pages in bulksheet files](bulksheet-validate-landing-pages.md)
>* [Export a generated or uploaded bulksheet file](bulksheet-export.md)
