---
title: (New UI) Download/Create a bulksheet file
description: Learn how to create bulksheet files by downloading account data for your ad networks in the new Search, Social, & Commerce UI.
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
# (New UI) Download/Create a bulksheet file

You can create bulksheets using custom settings for one or more accounts on one or more [supported ad networks](about.md#bulksheet-functionality-by-network). Bulksheets include data within Search, Social, & Commerce.

For synced campaigns, you can optionally sync with the ad network before downloading the data to ensure that recent data changes on the ad network side are included. For all ad networks, you can optionally generate new click-tracking URLs to include in the file.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. In the toolbar, click **[!UICONTROL Bulk Operations]** \> **[!UICONTROL Download Bulksheet]**.

1. Specify the [bulksheet settings](#bulksheet-settings):

   1. On the **[!UICONTROL Selections]** tab, select the accounts, campaigns, or ad groups to include and configure the bulksheet options.

   1. (Optional) Click the **[!UICONTROL Rows and Columns]** tab, specify the account components and the component statuses for which to include rows in the bulksheet, and then specify the columns to include for each selected component.

      For a list of available bulksheet rows, see "[Bulksheet rows by ad network](#bulksheet-rows-by-ad-network)."

   1. (Optional) Click the **[!UICONTROL Filters]** tab, and then specify criteria for the specific campaigns, ad groups, ads/creatives, keywords, placements, and other entities to include in the bulksheet.

1. Click **[!UICONTROL Download]**.

When the task begins, the window displays a notification but remains open so you can continue to create additional bulksheets if needed. When the file is created, you receive an email notification with a link to the file; depending on the amount of data being compiled, the notification may take several minutes or more. If the file generation fails, an error file is listed in the Bulksheets view and you receive an email notification with a link to the error file.

## Bulksheet settings {#bulksheet-settings}

### Selections tab {#bulksheet-selections-settings}

**\[Account, campaign, and ad group selection\]**

Expand the network and account hierarchy, and then select the check box next to each account, campaign, or ad group whose data to include in the bulksheet:

* To include all campaigns and ad groups for an account, select the check box next to the account name.

* To include specific campaigns, expand the account, and then select the check box next to each campaign to include. To include specific ad groups, further expand a campaign and select the check box next to each ad group.

>[!NOTE]
>
>* A single bulksheet can apply to multiple accounts within multiple ad networks. Ad network-specific columns are labeled in bulksheets with the ad network name (such as "Mobile Carriers (Google Ads)").
>* To see the type of component an item is, hold your cursor over it.
>* By default, only active and enabled accounts and their active components are listed.

**[!UICONTROL Generate Tracking URLs]:** (Optional) Includes tracking templates and landing page suffixes (for applicable ad networks) in accounts with tracking templates, or destination URLs with embedded tracking codes in accounts with destination URLs, for keywords, ads, placements, sitelinks, and [!DNL Google Ads] product groups in the bulksheet. By default, this option is selected.

When this option is selected, the URLs are generated according to the parameters in the [!UICONTROL Campaign Tracking] section of the account settings or campaign settings. By default, if tracking URLs already exist, they aren't regenerated unless new ones are needed (such as if the keyword match type, the ad text, or the account's tracking parameters have changed).

>[!NOTE]
>
>* If the advertiser uses Adobe Advertising conversion tracking and the relevant account isn't configured to automatically generate and upload tracking URLs, then you must generate new tracking URLs when the base URLs have changed.
>* If you don't select this option, you can still generate tracking URLs later when you upload or post the file.

**[!UICONTROL Perform pre-sync]:** (Optional) Instructs Search, Social, & Commerce to synchronize its files with the specified campaigns to ensure that all data is the same. By default, this option isn't selected.

>[!NOTE]
>
>Search, Social, & Commerce automatically synchronizes with the ad network once a day, whenever it detects a new campaign on the ad network, and every time you change campaign data from within Search, Social, & Commerce. Select this option if you think that recent changes to campaign or account data were made directly in the ad network or using the ad network's desktop editor. Bulksheet creation takes longer when you select this option.

**[!UICONTROL Bulksheet Name]:** The name of the new bulksheet and the file type. By default, the file is created in tab-separated values format and is named one of the following:

* (For all accounts for an ad network) `<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* (For a single account) `<account name>_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* (For multiple accounts) `MultipleAccounts_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`

You can rename the file. The name can't include the following characters: `# % & * | \ : " < > . ? /`

Optionally, change the file type. The options include *[!UICONTROL .tsv]* (for tab-separated values), *[!UICONTROL .txt (unicode)]* (for Unicode-compliant ASCII text), *[!UICONTROL .csv]* (for comma-separated values), or *[!UICONTROL .zip]* (for compressed ZIP format, which unzips to a TSV file).

>[!TIP]
>
>For bulksheets that include international characters, use TSV or TXT format.

### Rows and Columns tab {#bulksheet-rows-columns-settings}

**[!UICONTROL Bulksheet Rows]:** The entities, and their corresponding statuses, to include as data rows in the bulksheet, with one row per entry. For example, if you include active campaigns, the bulksheet includes one row per active campaign. Only selected entities with the selected statuses are included. Defaults are pre-selected based on the specified ad network. By default, only active instances of the selected entities are included.

To add or remove entities, select or clear the check boxes next to the entities. To add or remove statuses for an entity, click the status menu next to the entity, and then select or clear the check boxes for the applicable statuses.

For a list of available rows by ad network, see "[Bulksheet rows by ad network](#bulksheet-rows-by-ad-network)."

**[!UICONTROL Cascading Status Hierarchy]:** Filters child entities to those with the specified parent entity statuses, using an AND operation. For example, if you select "Active Campaign," "Active Adgroup," and "Active Keyword," then the bulksheet includes only active keywords in active ad groups in active campaigns.

If you don't select this option, then the parent status isn't considered, and the filter uses an OR operation. For example, if you select "Active Campaign," "Active Adgroup," and "Active Keyword," then the bulksheet includes all active campaigns; all active ad groups regardless of the parent campaign status; and all active keywords regardless of the parent campaign and ad group status.

**[!UICONTROL Bulksheet Columns]:** The columns to include in the downloaded bulksheet file:

* *[!UICONTROL AMO ID]:* (Required if "[!UICONTROL SE ID]" isn't selected) Includes an [!DNL Adobe]-generated unique identifier for each entity/row. Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post it to the ad network. Later, you can edit data for the entity using the [!UICONTROL AMO ID] as the identifier, rather than the entity ID and parent entity IDs.

* *[!UICONTROL SE ID]:* (Required if "[!UICONTROL AMO ID]" isn't selected) Includes the ad network's unique identifier for each included column and its parent entities. Later, if you edit data for any entity using the [!UICONTROL SE ID] as the identifier, then you must also include rows for the parent entities (including their [!UICONTROL SE ID] values).

* *[!UICONTROL Platform]:* Includes a [!UICONTROL Platform] column at the beginning of each row to indicate the ad platform (such as "Baidu").

* *[!UICONTROL Acct Name]:* (Required if "[!UICONTROL AMO ID]" isn't selected) Includes the ad network account name for each entity/row.

* \[Entity-specific columns\]: To include all, none, or only selected columns relevant to each entity selected in [!UICONTROL Bulksheet Rows], click ![Right arrowhead](/help/search-social-commerce/assets/compressed-item.png "Right arrowhead") next to the entity name to expand it, and then select or clear the check boxes for individual columns. By default, all relevant columns are included for each selected entity row.

>[!TIP]
>
>Make sure you include adequate columns to identify the item in each row of the bulksheet file. For example, if you include keyword rows per the [!UICONTROL Bulksheet Rows] selector but exclude all keyword-related columns, the resulting bulksheet includes one row for each keyword instance with no way to identify which keyword instance belongs to a specific row. In this case, you can't use the bulksheet to update data unless you manually add the appropriate ID column and values.

### Filters tab {#bulksheet-filters-settings}

Criteria for specific campaigns, ad groups, ads/creatives, keywords, and/or placements to include in the bulksheet:

1. Select a parameter (entity name or ID; or any element of a creative, keyword, or placement), select an operator, and then enter the applicable value.

   For example, to return only ads with "shoes" in the headline for a [!DNL Google Ads] account, select *[!UICONTROL Headline]*, select *[!UICONTROL contains]*, and then enter `shoes` in the input field.

1. (To apply additional filters) For each additional filter, click **[!UICONTROL +Add Filter]**, select **[!UICONTROL AND]** or **[!UICONTROL OR]**, select an ad element or keyword and an operator, and then enter the applicable value.

## Bulksheet rows by ad network {#bulksheet-rows-by-ad-network}

| Bulksheet Row | [!DNL Baidu] | [!DNL Google Ads] | [!DNL LY Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo Native] | [!DNL Yandex] | Notes |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Yes | Yes | Yes | Yes | Yes | Yes | Yes | Yes | Yes | &mdash; |
| [!UICONTROL Adgroup] | Yes | Yes | Yes | Yes | Yes | Yes | Yes | Yes | Yes | &mdash; |
| [!UICONTROL Creative] *or* [!UICONTROL Creative (except RSA)] | Yes | Yes | Yes | Yes | &mdash; | &mdash; | Yes | Yes | Yes | ([!DNL Google Ads]) Use for all ad types except responsive search ads, which are available in the [!UICONTROL Responsive Search Ad] row. |
| [!UICONTROL Responsive Search Ad] | &mdash; | Yes | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Keyword] | Yes | Yes | Yes | Yes | Yes | Yes | &mdash; | Yes | Yes | Use for non-negative keywords only. To see negative keywords created at the campaign or ad group level, use the [!UICONTROL Campaign Negative Keyword] or [!UICONTROL Adgroup Negative Keyword] row when available. |
| [!UICONTROL Promoted Pin] | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Placement] | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Auto Target] | &mdash; | Yes | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | Use for dynamic search targets for an ad group. |
| [!UICONTROL Shopping Product Group] | &mdash; | Yes | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Campaign Site Link] | &mdash; | Yes | &mdash; | Yes | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; |
| [!UICONTROL Campaign Negative Keyword] | Yes | Yes | Yes | Yes | &mdash; | &mdash; | &mdash; | Yes | &mdash; | Use for negative keywords created at the campaign or ad group level only. To see non-negative keywords, use the [!UICONTROL Keyword] row when available. |
| [!UICONTROL Campaign Negative Website] | &mdash; | Yes | &mdash; | Yes | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; |
| [!UICONTROL Adgroup Site Link] | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; |
| [!UICONTROL Creative Site Link] | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | Yes | &mdash; |
| [!UICONTROL Adgroup Negative Keyword] | Yes | Yes | Yes | Yes | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; |
| [!UICONTROL Adgroup Negative Website] | &mdash; | Yes | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Campaign Location Target] | Yes | Yes | Yes | Yes | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; |
| [!UICONTROL Adgroup Location Target] | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; |
| [!UICONTROL Campaign Device Target] | &mdash; | Yes | &mdash; | Yes | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; |
| [!UICONTROL Adgroup Device Target] | &mdash; | Yes | &mdash; | Yes | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; |
| [!UICONTROL Campaign RLSA Target] | &mdash; | Yes | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Adgroup RLSA Target] | &mdash; | Yes | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Campaign RLSA Negative] | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Adgroup RLSA Negative] | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |

For details about the required and optional columns for each ad network, see the ad network-specific bulksheet data format articles:

* [Required and optional bulksheet data for [!DNL Baidu] accounts](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)
* [Required and optional bulksheet data for [!DNL Google Ads] accounts](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)
* [Required and optional bulksheet data for [!DNL LY Ads] accounts](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)
* [Required and optional bulksheet data for [!DNL Microsoft Advertising] accounts](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)
* [Required and optional bulksheet data for [!DNL Naver] accounts](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
* [Required and optional bulksheet data for [!DNL Yahoo! Display Network] accounts](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)
* [Required and optional bulksheet data for [!DNL Yandex] accounts](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md)

>[!MORELIKETHIS]
>
>* [(New UI) About managing campaign data using bulksheets](about.md)
>* [(New UI) Upload a bulksheet or corrected error file](upload.md)
>* [(New UI) Post bulksheets or corrected error files](post.md)
>* [(New UI) Validate landing pages in bulksheet files](validate-landing-pages.md)
