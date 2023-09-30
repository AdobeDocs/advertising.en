---
title: Download/Create a bulksheet file
description: Learn how to create bulksheet files by downloading account data for your ad networks.
exl-id: a3fcef52-3d36-462e-a975-c741d003326e
feature: Search Bulksheets
---
# Download/Create a bulksheet file

You can create bulksheets using custom settings for one or more accounts on one or more [supported ad networks](bulksheet-about.md#bulksheet-functionality-by-network). Bulksheets include data within Search, Social, & Commerce.

For synced campaigns, you can optionally sync with the ad network before downloading the data to ensure that recent data changes on the ad network side are included. For all ad networks, you can optionally generate new click-tracking URLs to include in the file.

>[!NOTE]
>
>You can also [create a bulksheet file based on the visible columns in a campaign management view](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md).

1. In the main menu, click **[!UICONTROL Search]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]**.

1. In the toolbar, click **[!UICONTROL Download Bulksheet]**.

1. Specify the [bulksheet settings](#bulksheet-download-settings):

1. On the **[!UICONTROL Selections]** tab, enter or select information in the fields.

1. (Optional) Click the **[!UICONTROL Rows and Columns]** tab, specify the account components and the component statuses for which to include rows in the bulksheet, and then specify the columns to include for each selected component.

   For a list of available bulksheet rows, see "[Bulksheet rows by ad network](#bulksheet-rows-by-ad-network)."

1. (Optional) Click the **[!UICONTROL Filters]** tab, and then indicate criteria for specific campaigns, ad groups, ads/creatives, keywords, placements, and other entities to include in the bulksheet:

   1. Select a parameter (entity name or ID; or any element of an ad, keyword, or placement), select an operator, and then enter the applicable value. For example, to return only ads with "shoes" in the headline for a [!DNL Google Ads] account, select *Headline*, select *[!UICONTROL contains]*, and then enter `shoes` in the input field.
   
   1. (To apply additional filters) For each additional filter, click **[!UICONTROL +Add Filter]**, select **[!UICONTROL AND]** or **[!UICONTROL OR]**, select an ad element or keyword and an operator, and then enter the applicable value.

1. Click **[!UICONTROL Download]**.

When the task begins, the window displays a notification but remains open so you can continue to create additional bulksheets if you want. Any specified filters and exclusions that are applicable to any new accounts that you select are retained. When the task begins, the file is listed in the Bulksheets view. When the file is created, you receive an email notification with a link to the file; depending on the amount of data being compiled, the notification may take several minutes or more. If the file generation fails, however, then an error file is listed in the Bulksheets view and you receive an email notification with a link to the error file.

## Bulksheet download settings {#bulksheet-download-settings}

| Tab | Parameter | Description |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | The accounts, campaigns, or ad groups to which to upload the data:<ul><li>To select an account and all of its campaigns and ad groups, select the check box next to the account name, and then click &gt;&gt; to move it to the [!UICONTROL Selected Filters] column.</li><li>To select individual campaigns or ad groups, click next to the account to expand it, (if necessary) click next the campaign to expand it, select the check box next to the campaign or ad group name, and then click &gt;&gt; to move it to the [!UICONTROL Selected Filters] column. For example, to get data only for Campaign 1 in Account 1, expand Account 1, select the check box next to Campaign 1, and then move it to the [!UICONTROL Selected Filters] column.</li></ul><b>Notes:</b><ul><li>A single bulksheet may apply to multiple accounts within multiple ad networks. Ad network-specific columns are labeled in bulksheets with the ad network name (such as &quot;Mobile Carriers (Google Ads)&quot;).</li><li>To see what type of component any item is, hold your cursor over it.</li><li>For campaigns, the first letter of the ad network name is in parentheses after the account name (such as &quot;Acme Realty (G)&quot; for a [!DNL Google Ads] account).</li><li>By default, only active and enabled accounts and their active components are listed. To view paused and deleted components, click ![Down arrow](/help/search-social-commerce/assets/arrow-down-expand.png "Down arrow") next to [!UICONTROL Show] and select **[!UICONTROL All]. |
| | [!UICONTROL Generate Tracking URLs] | (Optional) Includes tracking templates and landing page suffixes (for applicable ad networks) in accounts with tracking templates, or destination URLs with embedded tracking codes in accounts with destination URLs, for keywords, ads, placements, sitelinks, and [!DNL Google Ads] product groups in the bulksheet. By default, this option is selected.<br><br>When this option is selected, the URLs are generated according to the parameters in the [!UICONTROL Campaign Tracking] section of the account settings or campaign settings. By default, if tracking URLs already exist, they aren't regenerated unless new ones are needed (such as if the keyword match type, the ad text, or the account's tracking parameters have changed).<br><br><b>Notes:</b><ul><li>If the advertiser uses Adobe Advertising conversion tracking and the relevant account isn't configured to automatically generate and upload tracking URLs, then you must generate new tracking URLs when the base URLs have changed.</li><li>If you don't select this option, you can still generate tracking URLs later when you upload or post the file.</li></ul> |
| | [!UICONTROL Perform Pre-sync] | (Optional) Instructs Search, Social, & Commerce to synchronize its files with the specified campaigns to ensure that all data is the same. By default, this option isn't selected.<br><b>Note:</b> Search, Social, & Commerce automatically synchronizes with the ad network once a day, whenever it detects a new campaign on the ad network, and every time you change campaign data from within Search, Social, & Commerce. Select this option if you think that recent changes to campaign or account data were made directly in the ad network or using the ad network's desktop editor. Bulksheet creation takes longer when you select this option. |
| | [!UICONTROL Bulksheet Name] | The name of the new bulksheet, and the file type. By default, the file is created in tab-separated values format and is named one of the following:<ul><li>(for all accounts for the ad network) `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(for single accounts) `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(for multiple accounts) `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`.</li></ul>You can rename the file. The name can't include the following characters: `# % &amp; * | \ : &quot; &lt; &gt; . ? or /`.<br><br>Optionally, change the file type. The options include *[!UICONTROL .tsv]* (for tab-separated values), *[!UICONTROL .txt]* (for Unicode-compliant ASCII text), *[!UICONTROL .csv]* (for comma-separated values), or *[!UICONTROL .zip]* (for compressed ZIP format, which unzips to a TSV file).<br><br><b>Tip:</b> For bulksheets that include international characters, use TSV or TXT format. |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | The entities, and their corresponding statuses, to include in the bulksheet, with one data row per entry. For example, if you include active campaigns, then the bulksheet includes one row per active campaign. Only selected entities with the selected statuses are included. Defaults are pre-selected based on the specified ad network. By default, only active instances of the selected entities are included. For a list of available bulksheet rows, see &quot;[Bulksheet rows by ad network](#bulksheet-rows-by-ad-network).&quot;<br><br>To add or remove entities, select or clear the check boxes next to the entities, respectively. To add or remove statuses for an entity, click next to the status menu, and then select or clear the check boxes next to the entities, respectively. |
| | [!UICONTROL Cascading Status Hierarchy] | Filters the scope of child entities to those with the specified parent entity statuses, using an AND operation. For example, if you select "Active Campaign," "Active Adgroup," and "Active Keyword," then the bulksheet includes only active keywords in active ad groups in active campaigns.<br><br>If you don't select this option, then the parent status isn't considered, and the filter uses an OR operation. For example, if you select "Active Campaign," "Active Adgroup," and "Active Keyword," then the bulksheet includes all active campaigns; all active ad groups, regardless of the parent campaign status; and all active keywords, regardless of the parent campaign and ad group status. |
| | [!UICONTROL Bulksheet Columns] | The columns to include in the downloaded bulksheet file:<ul><li>*[!UICONTROL AMO ID]*: (Required if &quot;[!UICONTROL SE ID]&quot; isn't selected) Includes an [!DNL Adobe]-generated unique identifier for each entity/row. Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post it to the ad network. Later, you can edit data for the entity using the [!UICONTROL AMO ID] as the identifier, rather than the entity ID and parent entity IDs.</li><li>*[!UICONTROL SE ID]*: (Required if &quot;[!UICONTROL AMO ID]&quot; isn't selected) Includes the ad network's unique identifier for each included column and its parent entities. Later, if you edit data for any entity using the [!UICONTROL SE ID] as the identifier, then you must also include rows for the parent entities (including their [!UICONTROL SE ID] values).</li><li>*[!UICONTROL Platform]*: Includes a [!UICONTROL Platform column] at the beginning of each row to indicate the ad platform (such as &quot;Baidu&quot;).</li><li>*[!UICONTROL Acct Name]*: (Required if &quot;[!UICONTROL AMO ID]&quot; isn't selected) Includes the ad network account name for each entity/row.</li><li>\[Columns to include\]: To include all, none, or only selected columns relevant to each selected entity in the [!UICONTROL Bulksheet Rows] section. To see the individual columns relevant to an entity, click ![Right arrowhead](/help/search-social-commerce/assets/compressed-item.png "Right arrowhead") next to the entity name. By default, all relevant columns are included for each selected entity row. Deselect the check box next to any entity or next to any individual column to exclude it from the bulksheet.</li></ul><br><br><b>Tip:</b> Make sure that you include adequate columns to identify the item in each row of the bulksheet file. For example, say you include keyword rows per the [!UICONTROL Bulksheet Rows] selector but you exclude all keyword-related columns. The resulting bulksheet includes one row for each keyword instance. However, since no keyword-related columns are included &mdash; not even the AMO ID or SE ID &mdash; you can't identify which keyword instance pertains to a specific row, and you can't use the bulksheet to update data unless you manually add the appropriate ID column and values. |
| [!UICONTROL Filters] | | Criteria for specific campaigns, ad groups, ads/creatives, keywords, and/or placements to include in the bulksheet:<ol><li>Select a parameter (entity name or ID; or any element of a creative, keyword, or placement), select an operator, and then enter the applicable value.<br>For example, to return only ads with &quot;shoes&quot; in the headline for a [!DNL Google Ads] account, select *[!UICONTROL Headline]*, select *[!UICONTROL contains]*, and then enter `shoes` in the input field.</li><li>(To apply additional filters) For each additional filter, click **[!UICONTROL +Add Filter]**, select **[!UICONTROL AND]** or **[!UICONTROL OR]**, select an ad element or keyword and an operator, and then enter the applicable value.</li></ul> |

## Bulksheet rows by ad network {#bulksheet-rows-by-ad-network}

| Bulksheet Row | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft® Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | Yandex | Notes |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Yes | Yes | Yes | Yes | Yes | Yes | Yes | Yes | Yes | &mdash; |
| [!UICONTROL Adgroup] | Yes | Yes | Yes | Yes | Yes | Yes | Yes | Yes | Yes | &mdash; |
| [!UICONTROL Creative] *or* [!UICONTROL Creative (except RSA)] | Yes | Yes | Yes | &mdash; | &mdash; | Yes | Yes | Yes | Yes | ([!DNL Google  Ads]) Use for all ad types except for responsive search ads, which  are available in the [!UICONTROL Responsive Search Ad] row. |
| [!UICONTROL Responsive Search Ad] | &mdash; | Yes | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Keyword] | Yes | Yes | Yes | Yes | Yes | &mdash; | Yes | Yes | Yes | Use for non-negative keywords only. To see negative keywords created at the campaign or ad group level, use the [!UICONTROL Campaign Negative Keyword] or [!UICONTROL Adgroup Negative Keyword] row when available. |
| [!UICONTROL Promoted Pin] | &mdash; | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Placement] | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Auto Target] | &mdash; | Yes | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | Use for dynamic search targets for an ad group. |
| [!UICONTROL Shopping Product Group] | &mdash; | Yes | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Campaign Site Link] | &mdash; | Yes | Yes | &mdash; | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; |
| [!UICONTROL Campaign Negative Keyword] | Yes | Yes | Yes | &mdash; | &mdash; | &mdash; | Yes | Yes | &mdash; | Use for negative keywords created at the campaign or ad group level only. To see non-negative keywords, use the [!UICONTROL Keyword] row when available. |
| [!UICONTROL Campaign Negative Website] | &mdash; | Yes | Yes | &mdash; | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; |
| [!UICONTROL Adgroup Site Link] | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; |
| [!UICONTROL Creative Site Link] | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | Yes | &mdash; |
| [!UICONTROL Adgroup Negative Keyword] | Yes | Yes | Yes | &mdash; | &mdash; | &mdash; | Yes | Yes | &mdash; | &mdash; |
| [!UICONTROL Adgroup Negative Website] | &mdash; | Yes | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Campaign Location Target] | Yes | Yes | Yes | &mdash; | &mdash; | &mdash; | Yes | Yes | &mdash; | &mdash; |
| [!UICONTROL Adgroup Location Target] | &mdash; | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; |
| [!UICONTROL Campaign Device Target] | &mdash; | Yes | Yes | &mdash; | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; |
| [!UICONTROL Adgroup Device Target] | &mdash; | Yes | Yes | &mdash; | &mdash; | &mdash; | &mdash; | Yes | &mdash; | &mdash; |
| [!UICONTROL Campaign RLSA Target] | &mdash; | Yes | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Adgroup RLSA Target] | &mdash; | Yes | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Campaign RLSA Negative] | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |
| [!UICONTROL Adgroup RLSA Negative] | &mdash; | Yes | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; | &mdash; |

>[!MORELIKETHIS]
>
>* [About managing campaign data using bulksheets](bulksheet-about.md)
>* [Post bulksheets or corrected error files](bulksheet-post.md)
>* [Validate landing pages in bulksheet files](bulksheet-validate-landing-pages.md)
>* [Export a generated or uploaded bulksheet file](bulksheet-export.md)
