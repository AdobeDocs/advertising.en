---
title: About managing campaign data using bulksheets
description: Learn about bulksheet functionality available by ad network, the bulksheet workflow, and error handling.
exl-id: 207cc08b-8650-4243-b9fd-1c920b81c1f9
---
# About managing campaign data using bulksheets

A bulksheet is a file that contains campaign data in a specific format and can be used to quickly create or modify campaign and ad group structure data and text ads. You can generate (download) bulksheets with data for one or more accounts, for specific campaigns and ad groups, or even for specific text ads, placements, and product groups. You can use bulksheets to manage large data sets or to make small changes. Each ad network requires different columns of information.

You can generate bulksheets with as much data as you want &mdash; or optionally create them manually and upload them (see the chapter on "Required/Included Data in Bulksheets").

Once you create a bulksheet, you can identify any broken landing pages that need to be corrected, or additional data to add or edit. You can then edit the file and upload it to Search, Social, & Commerce, optionally scheduling it to be posted to the relevant ad network immediately or later. You can also post an available bulksheet either immediately or later.

You can optionally upload bulksheet files to a specified FTP account for retrieval and automatic posting. The directory is scanned every hour, and new files are posted to the search network in the order in which they're received.

All bulksheets, landing page validation error files, and other error files are automatically deleted 30 days after they are created unless you delete them earlier.

## Functionality by Ad Network

* **Download, upload, and post:**  [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft® Advertising], and [!DNL Yandex] accounts

* **Download and upload only:** [!DNL Naver] accounts

  You can upload [!DNL Naver] data for use within Search, Social, & Commerce but can't post it to the ad network. You can also download your existing (unsynchronized) data.

* **Download data only:**  [!DNL Pinterest], [!DNL Yahoo Native], and [!DNL Yahoo! Display Network] accounts

  You can download your existing (unsynchronized) data.

## Overview of using bulksheets

The standard steps in using bulksheets for synchronized accounts are as follows:

<!-- insert image
  [EDIT/RECREATE FILE to replace "search engine"]
-->

1. [Download data for one or more accounts, campaigns, or ad groups into a bulksheet file](bulksheet-download.md). Optionally, you can manually populate an ad network-specific bulksheet and upload the file.

1. [Validate the landing pages](bulksheet-validate-landing-pages.md) in the base (final) URLs or destination URLs in the file.

1. When you need to add data or make corrections:

   1. [Export the file](bulksheet-export.md) to your desktop and edit it in [!DNL Microsoft® Excel].
   
   1. [Manually upload the edited file](bulksheet-upload.md) to Search, Social, & Commerce, or [upload the file to a specified FTP account](bulksheet-ftp-account.md) for automatic posting.

1. (For files uploaded manually) [Post the file](bulksheet-post.md) to the ad network either as you upload it or later.

1. (If necessary) Download any new error files, correct the rows, and repost the file.

## Managing errors in uploading and posting campaign data

Search, Social, & Commerce uploads and posts as many rows of data as it can from a campaign bulk sheet, including the tracking URLs it generates when required.

When errors occur during bulksheet operation, one of the following two types of error files is generated:

* **[!UICONTROL EF Errors]:**  When a file or individual rows in the file can't be uploaded or processed, an error file called `<uploaded file name>_ef_errors.<extension used for the bulksheet>` is created. If the problem is with individual rows, then those rows are included, with an explanation of each error so that it can be corrected.

* **[!UICONTROL SE Errors]:**  When a file is posted but the ad network doesn't accept some or all of the data, an error file called `<uploaded file name>_se_errors.<extension used for the bulksheet>` is created. When some but not all rows were accepted, the error file shows the rows that weren't posted and an explanation of each error so it can be corrected. The error messages are shown in the last three columns of each row.

>[!NOTE]
>
>If you post any [!DNL Google Ads] ads that violate the ad network's advertising policies but may be eligible for exemptions, then those ads are automatically reposted with exemption requests. If the exemption request fails, then information about the violation is included in the error file.

You can download either type of error file, make corrections directly in the rows, and then reupload and post the file.

Error files are automatically deleted after 30 days unless you delete them earlier.

## Information about each file

All downloaded data files, uploaded files, and error files are available from [!UICONTROL Search] > [!UICONTROL Bulksheets].

Information for each file includes the current task status and the percent of the task that's completed, the date it was created, (when applicable) the date it was or will be posted to the specified ad network, the scheduled deletion date, and the login name of the user who initiated the task.

>[!MORELIKETHIS]
>
>* [Download/Create a bulksheet file](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
>* [Upload a bulksheet or corrected error file](bulksheet-upload.md)
>* [Post bulksheets or corrected error files](bulksheet-post.md)
>* [Export a generated or uploaded bulksheet file](bulksheet-export.md)
