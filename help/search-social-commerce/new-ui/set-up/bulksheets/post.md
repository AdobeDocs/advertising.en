---
title: (New UI) Post bulksheets or corrected error files
description: Learn how to post bulksheet files to your ad networks in the new Search, Social, & Commerce UI.
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
# (New UI) Post bulksheets or corrected error files

You can post existing bulksheet files or corrected error files to the relevant accounts for [supported ad networks](about.md#bulksheet-functionality-by-network). If the file is in ZIP format, you don't need to unzip it first.

Bulksheet files and error files are automatically deleted 30 days after they're uploaded or generated.

>[!NOTE]
>
>You can also post a bulksheet file or error file when you upload the file.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Select the check box next to each file to post.

1. In the bulk actions toolbar, click **[!UICONTROL Post]**.

1. Enter or select information in the [[!UICONTROL Post Bulksheet] settings](#bulksheet-post-settings), and then click **[!UICONTROL Post]**.

   The same settings apply to all files you post.

When the task begins, the status and scheduled post date for the row are updated in the [!UICONTROL Bulksheets] view. When email notifications for bulksheets are [enabled within [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications/notification-manage.md), then an email notification with a link to the file is sent when the file is posted. Depending on the amount of data compiled, the email notification may take several minutes or more. If any of the data can't be posted, then an error file is listed in the [!UICONTROL Bulksheets] view, and an email notification is sent with a link to the error file.

>[!NOTE]
>
>* Large amounts of data take longer to be posted. You can follow the progress of the file in the [!UICONTROL Progress] column in the [!UICONTROL Bulksheets] view.
>* All posted data is subject to the network's editorial process.
>* Before the bulksheet file is posted, you can cancel the posting.

## Post settings for bulksheets and corrected error files {#bulksheet-post-settings}

| Parameter | Description |
|----|----|
| [!UICONTROL Account (Search Engine)] | The ad network account for which the data is posted. If you post multiple files simultaneously or one file that applies to multiple accounts, the value is *Multiple Accounts Selected*.<br><br>The first letter of the ad network name is in parentheses after the account name (such as "Acme Realty (G)" for a [!DNL Google Ads] account). |
| [!UICONTROL Scheduling] | When to post the file to the specified ad network:<ul><li>*[!UICONTROL Post to ad network now]* (the default): Begins posting the data immediately.</li><li>*[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:* Begins posting the data on the specified date and time; the default is tomorrow at 02:00 (2 a.m.). To change the date, enter a date in the format DD/MM/YYYY or click the calendar icon to open the calendar and select a date. To change the time, select a time (in 15-minute intervals) from the list.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Whether to include tracking templates and landing page suffixes (for applicable ad networks) in accounts with tracking templates, or destination URLs with embedded tracking codes in accounts with destination URLs, for all keywords, ads, placements, sitelinks, and [!DNL Google Ads] product groups in the posting: *[!UICONTROL Yes]* (the default) or *[!UICONTROL No]*. It doesn't matter if the bid units are in a portfolio.<br><br>If you select *[!UICONTROL Yes]*, then the URLs are generated according to the parameters in the [!UICONTROL Tracking Methods] section of the relevant account settings or campaign settings. By default, if tracking URLs exist, they aren't regenerated unless new ones are needed (such as if the keyword match type, the ad text, or the tracking parameters for the relevant accounts have changed).<br><br>If you select *[!UICONTROL No]*, then you can still generate tracking URLs later by manually posting the uploaded file.<br><br>**Note:** If the advertiser uses Adobe Advertising conversion tracking and the base URL has changed, you must generate new tracking URLs unless the account is configured to automatically generate and upload tracking URLs. |
| [!UICONTROL Replace Media Optimizer Tracking] | (Available when [!UICONTROL Generate Tracking URLs] is *[!UICONTROL Yes]*) Replaces any existing Adobe Advertising tracking in the uploaded file's URLs with newly generated tracking. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Allows budget changes to campaigns in optimized portfolios based on posted data. By default, this option isn't selected. If you select this option, any specified campaign budget changes are applicable until the optimization capability determines that the budget should be reallocated (usually at the next bid cycle).<br><br>**Note:** Any budget changes resulting from the posted data for campaigns in non-optimized portfolios occur when the file is posted. Changes appear in the campaign management views the next day. |
| [!UICONTROL Enable bidding on ads within portfolios] | When the included campaign components are in an optimized portfolio, this feature overrides the optimization strategy and allows bid changes based on the data in the bulksheet until a specified end date. If you select this option, specify an end date between 1-7 days away in the **[!UICONTROL Hold bulksheet bids until]** field. |

>[!MORELIKETHIS]
>
>* [(New UI) About managing campaign data using bulksheets](about.md)
>* [(New UI) Download/Create a bulksheet file](download.md)
>* [(New UI) Upload a bulksheet or corrected error file](upload.md)
>* [(New UI) Validate landing pages in bulksheet files](validate-landing-pages.md)
>* [(New UI) Delete uploaded bulksheets and error files](delete.md)
