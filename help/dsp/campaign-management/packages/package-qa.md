---
title: Review and Edit Package Settings Using Spreadsheets
description: Learn how to review and edit key package settings using spreadsheets.
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
---
# Review and Edit Package Settings Using Spreadsheets

You can download the settings for one or more packages in XLSX ([!DNL Microsoft Excel] spreadsheet) format for review. The spreadsheet includes a separate tab with flight information.

To update multiple settings at once, you can do either of the following:

* Make changes to select fields, save the file, and upload the edited file back to DSP.

* To make changes to additional packages, and to settings for any placement or ad, download a blank template file that includes tabs for each type of campaign component, enter or paste new or updated settings into the template file, and then upload the populated template to make the changes. For instructions, see "[XXXXXXXXXXXXXXX]()."

Editable fields include most settings that are normally editable.

>[!TIP]
>
>To quickly edit more fields for one or more packages, see "[Edit Packages](/help/dsp/campaign-management/packages/package-edit.md)."

## Download Settings for All Packages in a Campaign

When you download settings for all packages in a campaign, the spreadsheet includes separate tabs for the package settings and for the flight information. You can optionally include settings for the placements and ads that are associated with the packages; additional tabs are included for placement and ad settings.

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Download QA Excel]**.

1. In the [!UICONTROL QA Excel Download] dialog box, deselect any campaign components whose settings you want to exclude from the downloaded file, and then click **[!UICONTROL Download]**.

  By default, settings for all placements and ads associated with the packages are selected.
  
  A notification message indicates when the file is available to download.
  
1. To download the file, do either of the following:
  
   * In the notification message, click **[!UICONTROL Download].**
   
   * In the right of the top menu bar, click ![Jobs](/help/dsp/assets/downloads.png). Click **[!UICONTROL Download]** next to the job.
   
     The file is saved to the browser's Downloads folder. See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns.

>[!NOTE]
>
>You can't edit and re-upload campaign-level QA files. To make changes to the campaign component settings in these files, download a separate settings template file (setup file), enter or paste rows from the QA file into the template and save the file, and then upload the populated template file.

## Download Settings for One or More Packages

When you download settings for specific packages, the spreadsheet includes separate tabs for the package settings and for the flight information.

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the submenu, click **[!UICONTROL Packages]**.

1. In the bulk actions toolbar, click **[!UICONTROL ...]** > **[!UICONTROL Setup Excel]**.

   A notification message indicates when the file is available to download.

1. To download the file, do either of the following:

   * In the notification message, click **[!UICONTROL Download].**
   
   * In the right of the top menu bar, click ![Jobs](/help/dsp/assets/downloads.png). Click **[!UICONTROL Download]** next to the job.
   
     The file is saved to the browser's Downloads folder. See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns.

## Download a Settings Template {#download-template}

Download a blank template file that includes tabs for each type of campaign component. You can later add rows to any tab on the template and [upload the edited file](##upload-package-settings) to make changes. 

1. Click the name of the campaign.

1.  In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Download Setup Excel]**.

   The file is saved to the browser's Downloads folder. See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns.

## Upload Package Settings {#upload-package-settings}

You can upload settings for your packages, including the placements and ads associated with the packages, in a populated template file, but not in an edited settings file.

1. [Download a settings template](#download-template), enter or paste package, placement, and/or ad settings on the relevant tabs of the template, and then save the file to your device or network.

   Editable fields include most settings that are normally editable. See the available settings below.

1. Click the name of the campaign.

1.  In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Upload Setup Excel]**.

1. In the [!UICONTROL Upload Setup Excel] dialog:

    1. Either drag and drop a file into the box, or click inside the box to select a file from your device or network.

    1. Click **[!UICONTROL Upload]**.

1. (Optional) To verify that the updates were processed, click ![Jobs](/help/dsp/assets/downloads.png) in the right of the top menu bar.

<!--  EDIT AND ADD BACK LATER

## Upload Settings for One or More Packages

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the submenu, click **[!UICONTROL Packages]**.

1.  Select the check box next to each package whose settings you want to upload.

1. In the bulk actions toolbar, click **[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**.

1. In the [!UICONTROL Edit in Excel] dialog:

    1. Either drag and drop a file into the box, or click inside the box to select a file from your device or network.

    1. Click **[!UICONTROL Upload]**.

1. (Optional) To verify that the updates were processed, click ![Jobs](/help/dsp/assets/downloads.png) in the right of the top menu bar.

-->

## Package Setting Columns in Downloaded/Uploaded Spreadsheets{#qa-sheet-columns-packages}

>[!TIP]
>
> In a downloaded spreadsheet, all editable columns are highlighted in blue.

### [!UICONTROL Package] Tab

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | The name of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Status] | The package status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Description] | An optional description of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | An optional description of the third-party fee rate, if applicable. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | The start date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | The end date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | At which level to pace and cap placements in the package: *[!UICONTROL Package]* or *[!UICONTROL Placement]*. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | The package budget. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | An optional budget interval cap. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | The interval for the optional budget interval cap: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | The objective of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | The target value of the goal. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only)A [custom goal](/help/dsp/optimization/custom-goal.md) that includes the revenue or conversion events used to calculate the CPA or ROAS metric. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Optional; packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only) The final conversion event or revenue event/sale amount to use for computing the return on ad spend or the cost per acquisition. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Packages with custom optimization goals only) The purpose of the package, which helps determine how to optimize the package: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]*, or *[!UICONTROL Other]* . | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Packages with custom optimization goals only) The package ID for another package whose historic data is used as input for optimizing the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Packages with custom optimization goals only) Another package whose historic data is used as input for optimizing the package. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Whether the package is pacing towards the *[!UICONTROL budget]* or *[!UICONTROL primary_goal]* (for impressions). | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (When you pace the package on impressions) The target number of impressions during the specified time interval. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (When you pace the package on impressions) The time interval for the target number of impressions. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the package: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the package: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | The primary frequency cap for the package during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the primary [!UICONTROL Frequency Cap] applies. For example, if the primary cap is 12 impressions per month, then the value here would be `12`. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the package during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Whether or not to create non-even pacing flights for the package*T* (true) or *F* (false). Once you enable custom flighting and save the package, you can't disable custom flighting nor edit the package start date. | &mdash; |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Available only when the [!UICONTROL Activate Custom Flighting] option is enabled) Whether or not to automatically add any remaining budget from the previous flight to the existing budget for the next flight: *T* (true) or *F* (false). | Yes |
| [!UICONTROL Error] | [!UICONTROL Error] | Any relevant errors. | &mdash; |

### [!UICONTROL Package_Flights] Tab {#qa-sheet-columns-package-flights}

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | The numeric ID of the flight. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] |The first date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | The final date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | The target spend goal for the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Existing packages without the "[!UICONTROL Automatically rollover remaining flight budget to next flight]" option enabled) An amount of potentially unspent budget to add to the next flight. | Yes |

>[!MORELIKETHIS]
>
>* [Edit Packages](/help/dsp/campaign-management/packages/package-edit.md)
>* [Package Settings](/help/dsp/campaign-management/packages/package-settings.md)
