---
title: Manage inventory data feed files
description: Learn how to configure the settings that control how feed data is processed.
exl-id: 73d372de-2673-4190-94cf-2f07f4ce2493
feature: Search Inventory Feeds
---
# Manage inventory data feed files

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (delete actions only), and [!DNL Yandex] accounts only*

If you submit your own feed data, then you must upload files containing your product data to dynamically create campaign structure, ads, and keywords, based on your product data. You can then associate them with ad network-specific ad templates and process the data through the templates, eventually posting the data to the relevant ad networks. You can associate multiple templates with a feed file, but each template can be associated with only one feed file.

>[!NOTE]
>
>Don't upload files if you're using data directly from a merchant center account.

You can upload and process data feed files in either of the following ways:

* **Automatically using FTP:** You can upload files directly to an FTP directory; the feed service checks for new files every two hours. After you upload a file for the first time, you can associate it with an ad network-specific template. Later, all files you upload with the same name are automatically associated with the same template. Depending on how you [configure the feed data settings](feed-settings-manage.md), Search, Social, & Commerce may automatically propagate the feed data through all applicable templates and optionally post the resulting campaign and ad data to the relevant ad networks.

  To set up an FTP directory for depositing and automatically processing data files, contact your Adobe Account Team.

* **Manual Processing:** You can manually [upload feed files](#feed-file-upload) from the [!UICONTROL Advanced] (ACM) view. After you associate a feed file with one or more ad network-specific [templates](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md), you can generate campaign and ad data by [propagating the feed data through the templates](feed-data-propagate.md) according to the [feed data settings](feed-settings-manage.md). You can optionally preview the generated data within campaign hierarchy views, generate a bulksheet file for review, or generate a bulksheet file for immediate posting to the ad network. If you don't post the data immediately, then you can [preview it](propagated-data-view.md) and [post it](propagated-data-post.md) later. You can later [replace the existing feed file with a new file](#feed-file-replace) without losing any existing template associations.

## Feed file requirements

No specific data fields are required in an individual file, but the following are required for each file:

* The first line in the file must contain column names (also called *headers*), which correspond to the dynamic parameters in the associated templates. The remaining lines must include data that correspond to the column names. Each data line (row) must pertain to only one account component, such as one campaign or one ad. The values on all lines must be separated by either tabs or commas. See the [CSV example file](#example-csv-feed-file) and [TSV example file](#example-tsv-feed-file) below.

*  The file can be any size but must have one of the following file extensions: `.tsv` (for tab-separated values), `.txt` (for [!DNL Unicode]-compliant ASCII text), `.csv` (for comma-separated values), or `.zip` (for a single file in compressed ZIP format, which unzips to a TSV file).

* The file name is case-sensitive and can't include the following characters: `# % & * | \ : " < > . ? /`

* If you deposit files in an FTP directory, then you must use the same file name for each version of the file.

* ([!DNL Google Ads] templates only) If your template uses the Param2 or Param2 ad parameter in text ads, then the corresponding data fields in the feed file must include numeric data, with no monetary symbols.

* To update existing account components, include the name of the existing campaign (and its components, if relevant). If the existing structure isn't specified, then new components are created.

### Example of a comma-separated feed file {#example-csv-feed-file}

```
Product Category,Product Name,Discount Percentage
electronics,iPods,10
apparel,Shirts,15
shoes,Clarks,20
```

### Example of a tab-separated feed file {#example-tsv-feed-file}

```
Product Category<TAB>Product Name<TAB>Discount Percentage
electronics<TAB>iPods<TAB>10
apparel<TAB>Shirts<TAB>15
shoes<TAB>Clarks<TAB>20
```

## Best practices

* For data that includes international characters, use files in TSV or TXT format.

* To achieve a repeatable process with limited manual review or editing, set up feed files and their account structure data as follows:

  * Include columns and rows that contain sufficient data to create account structure or map to the existing account structure. Ideally, use an existing account structure that is closely tied to the product taxonomy and to which the feed data is easily mapped.
  
  * Include descriptions that are short enough to use in ad copy.
  
  * Use consistent data patterns and naming conventions across product rows.
  
  * Remove all preceding spaces and trailing spaces.
  
  * Remove any garbled characters.

## View or download a feed file

You can open or download any feed file that was uploaded manually or using FTP.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**, which opens to the [!UICONTROL Templates] tab.

1. Locate the feed file:

1. In the templates list, locate a template that uses the feed file.

1. In the toolbar above the data table, click **[!UICONTROL Feeds]** to open a list of all feed files.

1. Click the feed file name.

1. Open or save the file according to your browser's normal procedure.

  For more information, see your browser’s online help.

## Manually upload a feed file {#feed-file-upload}

>[!NOTE]
> If you associate a template with a manually uploaded file, but then you upload via FTP another file with the same name, file extension, and grammatical case, then the FTP file is used when you propagate the data through the template. For example, myfile.csv replaces myfile.csv, but Myfile.CSV doesn't.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**, which opens to the [!UICONTROL Templates] tab.

1. In the toolbar above the data table, click **[!UICONTROL Feeds]**.

1. Above the data table, click **[!UICONTROL Upload]**.

1. Specify the file to upload either by entering the full path and file name or by clicking **[!UICONTROL Browse]** to locate the file on your device or network.

1. Click **[!UICONTROL Upload].

All fields in the file are validated. You can't post items with invalid field lengths later until you correct the values. All column names in the file become available in templates as dynamic parameters.

## Replace a feed file {#feed-file-replace}

When you replace a feed file &mdash; even if the new file has a different file name or extension &mdash; all existing template associations remain. The new file is used when you propagate data through all templates that were originally associated with the previous file.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**, which opens to the [!UICONTROL Templates] tab.

1. Do either of the following:

   * In the [!UICONTROL Feed] column for any applicable template, click ![More options](/help/search-social-commerce/assets/options.png "More options") and select **[!UICONTROL Re-upload]**.

   * In the toolbar above the data table, click **[!UICONTROL Feeds]**. In the feed file list, select the check box next to the existing file name. Above the data table, click **[!UICONTROL Upload]**.

   >[!NOTE]
   >
   >The source of the feed file ("[!UICONTROL FTP]" or "&mdash" for manually uploaded files) is included in the [!UICONTROL Source] column.

1. Specify the file to upload either by entering the full path and file name or by clicking **[!UICONTROL Browse]** to locate the file on your device or network.

  Even if the new file has a different file name or extension, the existing file is overwritten with the new file.

1. Click **[!UICONTROL Re-Upload]**.

All fields in the file are validated. You can't post items with invalid field lengths later until you correct the values. All column names in the file become available in templates as dynamic parameters.

## Delete feed files

You can delete any feed file that's been uploaded manually or via FTP. When you delete a feed file, it's no longer associated with any templates.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**, which opens to the [!UICONTROL Templates] tab.

1. In the toolbar above the data table, click **[!UICONTROL Feeds]**.

1. Select the check box next to each file that you want to delete.

1. Above the data table, click **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [About inventory feeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propagate feed data through templates](feed-data-propagate.md)
>* [View data generated from feeds](propagated-data-view.md)
>* [Edit data generated from feeds](propagated-data-edit.md)
>* [Post campaign data generated from feeds to ad networks](propagated-data-post.md)
>* [Stop a posting job for inventory feed data](stop-job.md)
>* [Statuses of data generated from feeds](propagated-data-status.md)
