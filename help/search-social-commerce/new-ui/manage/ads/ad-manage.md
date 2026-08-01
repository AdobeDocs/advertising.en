---
title: Manage ads
description: Learn how to create and manage ads, including the available ad types.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Manage ads

*Beta feature*

*[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising], [!DNL Yandex], and existing [!DNL Baidu] accounts only*

An ad belongs to an ad group and contains the content that's displayed to users &mdash; such as the headline, description, image, or other creative elements &mdash; depending on the ad network and ad type.

Once you [make an ad network account accessible via an API connection](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) and Search, Social, & Commerce has synchronized the account data with the ad network, you can create ads for a [supported campaign type](/help/search-social-commerce/introduction/supported-inventory.md). You also can edit and change the status of ads.

For details about the functionality available for each ad network, see "[Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md)."

## About the [!UICONTROL Ads] view {#ad-view-about}

The [!UICONTROL Manage] > [!UICONTROL Ads] view lists all ads in the filtered view for the selected advertiser account.

### Available actions

* [Create an ad](#ad-create)

* [Rename an ad from within the row](#ad-rename)

* [Edit ad settings](#ad-edit)

* [Change the status of, or delete, an ad](#ad-status)

* [Manage data view reports from the [!UICONTROL Ads] view](#ad-reports)

## Available ad types {#ad-types}

You can create and manage supported ad types for ad groups within a synchronized ad network account:

* **Text ads or expanded text ads** for an ad group in a campaign that targets the search network. Text ads may include optional tracking parameters that override the ad group- or campaign-level parameters. Depending on the ad network, you may be able to create either expanded/extended text ads or standard text ads.

* Cross-device, native **audience ads** for [!DNL Microsoft Advertising] campaigns on the [!DNL Microsoft Audience Network]. You have two options for audience ads, based on the campaign settings:

  * If the campaign is linked to a merchant center store, then let the ad network automatically generate feed-based ads for the campaign, using the store's product information. You don't need to create feed-based ads for the campaign, but you must create ad groups with user targeting.

  * If the campaign isn't linked to a merchant center account, then create image-based audience ads using the responsive ad format, which includes multiple text and image assets. The ad network assembles the ads using the most effective combinations of ad elements and displays them on sites like [!DNL MSN], [!DNL Outlook.com], and [!DNL Microsoft Edge].

* **Call-only ads** for [!DNL Google Ads] campaigns on the search network. Call-only ads are text ads that include a telephone number. You optionally can use a [!DNL Google Ads]-assigned forwarding number for advanced call reporting.

  >[!NOTE]
  >
  >You can't currently create or edit call-only ads. You can view, change the status of, or delete an existing call-only ad.

* **Expanded dynamic search ads** (now called just "dynamic search ads" on the ad networks) for [!DNL Google Ads] and [!DNL Microsoft Advertising] dynamic search ad groups in search campaigns. Dynamic search ads use content from your website, instead of keywords, to decide when to show your ads. The ad network dynamically generates the headline, chooses the landing page URL and display URL, and automatically generates the final URL.

  For more information about dynamic search ads, see the [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/2471185) and [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Multimedia ads** for [!DNL Microsoft Advertising] search campaigns. Multimedia ads are large image ads that are shown in prominent mainline and sidebar positions, and only one multimedia ad is displayed per page. They can include multiple text and image assets, like responsive ads, and the ad network assembles the ads using the most effective combinations of ad elements. Multimedia ads don't replace your text ad placements.

* Promotion lines for **[!DNL Microsoft Advertising] product (shopping) ads** on the shopping network. Shopping ads use products in your existing [!DNL Microsoft Merchant Center] product feed, instead of keywords, to decide how and where to show your ads. The ad copy and landing page URLs are generated automatically from your product information in the feed, but you can optionally set up promotion lines to include for the ad group.

  For more information about product ads, see the [Microsoft Advertising documentation](https://help.ads.microsoft.com/#apex/3/en/51082).

* **Responsive search ads** for [!DNL Google Ads] and [!DNL Microsoft Advertising] campaigns on the search network. The ad network dynamically assembles text-based responsive search ads from a set of ad titles and descriptions, favoring combinations that perform well together. The ad includes up to three headlines, two descriptions, and a customizable URL from the base URL and optional path1 and path2 fields. You can optionally pin ad titles and descriptions to specific positions.

  >[!NOTE]
  >
  >[!DNL Google Ads] doesn't provide data outside of its native editors about the text combinations that were displayed as ads. For more information about reporting for each text combination, see the [Google Ads documentation](https://support.google.com/google-ads/answer/7684791).

### Ad-level performance data

Ad-level data is available for most ad types.

However, it isn't available for [!DNL Google Ads] dynamic search ad (DSA), performance max, smart shopping, and [!DNL YouTube] campaigns. Expect discrepancies between the total ad-level data for a campaign and the total data for the campaign.

| Ad Network/Campaign/Ad Type | Data Availability |
|---|---|
| [!DNL Google Ads] dynamic search ad (DSA) | Campaign, ad group |
| [!DNL Google Ads] performance max | Campaign |
| [!DNL Google Ads] shopping, smart shopping | Campaign, ad group |
| [!DNL Google Ads] [!DNL YouTube] | Campaign, ad group |

## Create an ad {#ad-create}

<!-- Verify that this note is still applicable -->

>[!NOTE]
>
>* You don't need to create product ads for shopping campaigns; the ad network creates them automatically. For [!DNL Microsoft Advertising] shopping campaigns, however, you can optionally define promotion lines to include in ads.
>* You can't create [!DNL Google Ads] call-only ads.

>[!TIP]
>
>To create a large number of ads at once, use [campaign bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ads]**.

1. Click **[!UICONTROL Create Ads]**.

1. In the **[!UICONTROL Basic Settings]** step, select the network, the account, the campaign, the ad group, and the ad type.

   For more information about the available ad types, see "[Available ad types](#ad-types)."

1. Specify the remaining settings for a [Baidu text ad](ad-settings-baidu-text.md), [Google Ads expanded dynamic search ad](ad-settings-google-dsa.md) (called just "dynamic search ad" in Google Ads), [Google Ads responsive search ad](ad-settings-google-rsa.md), [Microsoft Advertising expanded dynamic search ad](ad-settings-microsoft-dsa.md), [Microsoft Advertising multimedia ad](ad-settings-microsoft-multimedia.md), [Microsoft Advertising product ad](ad-settings-microsoft-product.md), [Microsoft Advertising responsive (audience) ad](ad-settings-microsoft-responsive.md), [Microsoft Advertising responsive search ad](ad-settings-microsoft-rsa.md), or [Yandex text ad](ad-settings-yandex-text.md) settings.

   >[!NOTE]
   >
   >(Campaigns with Adobe Advertising conversion tracking) If the account or campaign settings specify tracking only at the keyword level, then Search, Social, & Commerce doesn't generate tracking for ads.

1. Click **[!UICONTROL Review and Save]**.

1. If necessary, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit") **[!UICONTROL Edit]** and change the ad settings.

1. Click **[!UICONTROL Create]**.

1. <!-- Add link to where to generate this once available to users-->(Shopping ads in campaigns with Adobe Advertising conversion tracking; optional) To track clicks on the ad, manually add a tracking URL to the account, campaign, or product group settings.

## Rename an ad {#ad-rename}

Quickly rename an ad without opening the full ad settings.

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ads]**.

1. Hold the cursor over the ad row and click **[!UICONTROL ...] > [!UICONTROL Rename]**.

1. Edit the name, and then click **[!UICONTROL Apply]**.

## Edit ad settings {#ad-edit}

>[!NOTE]
>
>* The following ad types are *mutable*, which means that you can change the ad copy or image and retain the same ad ID: all [!DNL Google Ads] ad types except for dynamic search ads, and [!DNL Microsoft Advertising] expanded text ads.
>* All other supported ads are *non-mutable*, which means that changing the ad copy or image deletes the existing ad and creates a new one. Performance for the new ad may be volatile for a couple of weeks while Search, Social, & Commerce gathers enough data for optimization.
>* You can't edit the content of a product ad, except for the promotion line for [!DNL Microsoft Advertising] product ads. You can, however, pause or delete an ad.
>* You can't edit [!DNL Google Ads] call-only ads. You can, however, pause or delete one.
>* You can edit only one ad at a time.

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ads]**.

1. Select the check box next to the ad.

1. In the bulk actions toolbar, click **[!UICONTROL Edit]**.

1. Edit the remaining settings for a [Baidu text ad](ad-settings-baidu-text.md), [Google Ads expanded dynamic search ad](ad-settings-google-dsa.md) (now called just "dynamic search ad" in Google Ads), [Google Ads responsive search ad](ad-settings-google-rsa.md), [Microsoft Advertising expanded dynamic search ad](ad-settings-microsoft-dsa.md), [Microsoft Advertising multimedia ad](ad-settings-microsoft-multimedia.md), [Microsoft Advertising product ad](ad-settings-microsoft-product.md), [Microsoft Advertising responsive (audience) ad](ad-settings-microsoft-responsive.md), [Microsoft Advertising responsive search ad](ad-settings-microsoft-rsa.md), or [Yandex text ad](ad-settings-yandex-text.md) settings.

1. Click **[!UICONTROL Review and Save]**.

1. If necessary, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit") **[!UICONTROL Edit]** and change the ad settings.

1. Click **[!UICONTROL Update]**.

## Change the status of an ad {#ad-status}

Quickly change the status of an ad without opening the full ad settings.

You can pause any active ad on a supported ad network to disable bidding on it. You can later resume bidding by changing the status back to active.

You also can delete any active or paused ad. Deleted ads are deleted from the ad network. They're still visible when you include them in the data filter, but you can't change them.

### Activate or pause an ad

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ads]**.

1. Select the check box for the ad row.

1. In the bulk actions toolbar, change the status:

   * To activate a paused ad, click **[!UICONTROL Activate]**.

   * To pause an active ad, click **[!UICONTROL Pause]**.

### Delete an ad

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ads]**.

1. Select the check box for the ad row.

1. In the bulk actions toolbar, click **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

## Manage data view reports from the [!UICONTROL Ads] view {#ad-reports}

Generate a report that includes the data rows for one or more ads in the [!UICONTROL Ads] view, and then download the report as a Microsoft Excel worksheet file (XLXS format). The report includes all visible columns in the view.

You can delete any generated report.

See also "[(Legacy UI) Download data from a campaign management view](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)" and "[(Legacy UI) Delete a performance data report or bulksheet file from the [!UICONTROL Downloads] menu](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)."

### Generate a report with the filtered data rows

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ads]**.

1. Specify the ads whose data you want to download:

   * To download data for specific ads, select the check boxes next to the ads.

   * To download data for all ads, you don't need to select any check boxes. All ads are included by default.

1. In the toolbar above the data table, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report") **[!UICONTROL Reports]**.

1. In the [!UICONTROL Grid Reports] settings, enter a unique report name, and then click **[!UICONTROL Generate]**.

   By default, the file is named "ad_YYYYMMDD_NNNN," where "NNNN" is the sequential job number (such as "ad_20250402_1326).

   The file is added to the [!UICONTROL Recently Generated] list.

1. (Optional) To download the file once it's completed, click ![Download](/help/search-social-commerce/assets/download.png "Download") next to the file name.

   The file is downloaded according to your browser's normal procedure.

### Download a completed report

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ads]**.

1. In the toolbar above the data table, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report") **[!UICONTROL Reports]**.

1. In the [!UICONTROL Recently Generated] list in the [!UICONTROL Grid Reports] dialog, click ![Download](/help/search-social-commerce/assets/download.png "Download") next to the file name.

   The file is downloaded according to your browser's normal procedure.

### Delete a completed report

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Ads]**.

1. In the toolbar above the data table, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report") **[!UICONTROL Reports]**.

1. In the [!UICONTROL Recently Generated] list in the [!UICONTROL Grid Reports] dialog, click ![Delete](/help/search-social-commerce/assets/delete-new.png "Delete") next to the file name.

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] text ad settings](ad-settings-baidu-text.md)
>* [[!DNL Google Ads] expanded dynamic search ad settings](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] responsive search ad settings](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising] expanded dynamic search ad settings](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] multimedia ad settings](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] product ad settings](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] responsive (audience) ad settings](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising] responsive search ad settings](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex] text ad settings](ad-settings-yandex-text.md)
