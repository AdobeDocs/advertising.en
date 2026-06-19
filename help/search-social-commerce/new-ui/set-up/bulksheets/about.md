---
title: (New UI) About managing campaign data using bulksheets
description: Learn about bulksheet functionality available by ad network, the bulksheet workflow, and error handling in the new Search, Social, & Commerce UI.
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
# (New UI) About managing campaign data using bulksheets

A bulksheet is a file that contains campaign data in a specific format and can be used to quickly create or modify campaign and ad group structure data and text ads. You can generate (download) bulksheets with data for one or more accounts, for specific campaigns and ad groups, or even for specific text ads, placements, and product groups. You can use bulksheets to manage large data sets or to make small changes. Each ad network requires different columns of information.

You can generate bulksheets with as much data as you want &mdash; or optionally create them manually and upload them. See "[Required and included data in bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-file-formats.md)" for file format requirements, and "[Operations you can perform in bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md)" for supported operations by ad network.

Once you create a bulksheet, you can identify any broken landing pages that need to be corrected, or additional data to add or edit. You can then edit the file and upload it to Search, Social, & Commerce, optionally scheduling it to be posted to the relevant ad network immediately or later. You can also post an available bulksheet either immediately or later.

All bulksheets, landing page validation error files, and other error files are automatically deleted 30 days after they are created unless you delete them earlier.

## Functionality by ad network {#bulksheet-functionality-by-network}

* **Download, upload, and post:**  [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising], and [!DNL Yandex] accounts

* **Download and upload only:** [!DNL Naver] accounts

  You can upload [!DNL Naver] data for use within Search, Social, & Commerce but can't post it to the ad network. You can also download your existing (unsynchronized) data.

* **Download data only:**  [!DNL Pinterest], [!DNL Yahoo DSP], [!DNL Yahoo Native] accounts

  You can download your existing (unsynchronized) data.

## Overview of using bulksheets

The standard steps for using bulksheets with synchronized accounts are as follows:

1. [Download data for one or more accounts, campaigns, or ad groups into a bulksheet file](download.md). Optionally, you can manually populate an ad network-specific bulksheet and upload the file.

1. [Validate the landing pages](validate-landing-pages.md) in the base (final) URLs or destination URLs in the file.

1. When you need to add data or make corrections:

   1. Export the file to your desktop and edit it in [!DNL Microsoft Excel].

   1. [Manually upload the edited file](upload.md) to Search, Social, & Commerce.

1. (For files uploaded manually) [Post the file](post.md) to the ad network either as you upload it or later.

1. (If necessary) Download any new error files, correct the rows, and repost the file.

## Managing errors in uploading and posting campaign data

Search, Social, & Commerce uploads and posts as many rows of data as it can from a campaign bulksheet, including the tracking URLs it generates when required.

When errors occur during a bulksheet operation, one of the following two types of error files is generated:

* **[!UICONTROL EF Errors]:** When a file or individual rows in the file can't be uploaded or processed, an error file called `<uploaded file name>_ef_errors.<extension used for the bulksheet>` is created. If the problem is with individual rows, then those rows are included, with an explanation of each error so that it can be corrected.

* **[!UICONTROL SE Errors]:** When a file is posted but the ad network doesn't accept some or all of the data, an error file called `<uploaded file name>_se_errors.<extension used for the bulksheet>` is created. When some but not all rows were accepted, the error file shows the rows that weren't posted and an explanation of each error so it can be corrected. The error messages are shown in the last three columns of each row.

>[!NOTE]
>
>If you post any [!DNL Google Ads] ads that violate the ad network's advertising policies but may be eligible for exemptions, those ads are automatically reposted with exemption requests. If the exemption request fails, then information about the violation is included in the error file.

You can download either type of error file, make corrections directly in the rows, and then reupload and post the file.

Error files are automatically deleted after 30 days unless you delete them earlier.

## Information about each file

All downloaded data files, uploaded files, and error files are available from [!UICONTROL Setup] \> [!UICONTROL Bulksheets].

Information for each file includes the current task status and the percent of the task that's completed, the date it was created, (when applicable) the date it was or will be posted to the specified ad network, the scheduled deletion date, and the login name of the user who initiated the task.

>[!MORELIKETHIS]
>
>* [(New UI) Download/Create a bulksheet file](download.md)
>* [(New UI) Upload a bulksheet or corrected error file](upload.md)
>* [(New UI) Post bulksheets or corrected error files](post.md)
>* [(New UI) Validate landing pages in bulksheet files](validate-landing-pages.md)
>* [(New UI) Delete uploaded bulksheets and error files](delete.md)
>* [(New UI) Stop a bulksheet job in progress](stop-job.md)
