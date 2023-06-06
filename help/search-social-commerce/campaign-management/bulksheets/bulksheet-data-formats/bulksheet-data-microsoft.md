---
title: Required bulksheet data for [!DNL Microsoft Advertising] accounts
description: Reference the required header fields and data fields in bulksheets for [!DNL Microsoft Advertising] accounts.
---
# Appendix - Required bulksheet data for [!DNL Microsoft Advertising] accounts

To create and update [!DNL Microsoft Advertising] campaign data in bulk, you can use Search, Social, & Commerce bulksheet files formatted specifically for [!DNL Microsoft Advertising] accounts. You can either a) [generate bulk sheet files for existing accounts](../bulksheet-download.md) in the required file format or b) create them manually (see "[Supported Bulksheet File Formats](bulksheet-file-formats.md)" for general information about the supported file formats).

{{$include /help/_includes/bulksheet-appendices-intro.md}}

## All available data fields

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Field | Description |
|----|----|
| Platform | (Included in generated bulksheets for information purposes) The ad platform. Required unless each row includes an &quot;AMO ID&quot; for the entity. |
| Acct Name | The unique name that identifies an ad network account. Required unless each row includes an &quot;AMO ID&quot; for the entity. |
| Campaign Name | The unique name that identifies a campaign for an account. The maximum length is 128 characters. |
| Campaign Budget | The daily or monthly campaign budget, with or without monetary symbols and punctuation. It can't be less than 0.05. |
| Channel Type | The type of channel that the campaign targets: <i>Audience</i>, <i>DynamicSearchAds</i>, <i>Search</i>, or <i>Shopping</i>. |
| Delivery Method | (Campaigns with daily budgets only) How quickly to show ads for the campaign each day:<ul><li><i>Standard (Distributed)</i> (the default for new campaigns): To spread your ad impressions across the day.</li><li><i>Accelerated:</i> To display your ads as often as possible until your budget is reached. As a result, your ads may not appear later in the day.</li></ul> |
| Campaign Priority | (Shopping campaigns only) The priority with which the campaign is used when multiple campaigns advertise the same product: <i>Low</i> (the default for new campaigns), <i>Medium</i>, or <i>High</i>.<br><br>When the same product is included in more than one campaign, the ad network uses the campaign priority first to determine which campaign (and associated bid) is eligible for the ad auction. When all of the campaigns have the same priority, the campaign with the highest bid is eligible. |
| Merchant ID | (Shopping campaigns and audience campaigns linked to a merchant feed only) The customer ID of the merchant account whose products are used for the campaign. |
| Sales Country | (Shopping campaigns only; read-only for existing campaigns) The country in which the campaign's products are sold. Because products are associated with target countries, this setting determines which products are advertised in the campaign. |
| Product Scope Filter | (Campaigns using the shopping network only) The products in your merchant account for which product ads can be created for the campaign. You can enter up to seven product dimension and attribute combinations on which to filter your products, using the format dimension=attribute. Separate multiple filters with a &quot;&gt;&gt;&quot; delimiter. For a list of available product dimensions, see &quot;[Shopping campaign product filters](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;<br><br> Example: &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> To delete the existing values, use the value `[delete]` (including the brackets). |
| DSA Domain Name | (Campaigns of type a) &quot;<i>DynamicSearchAds</i>&quot; or b) &quot;<i>Search</i>&quot; when the ExperimentId element isn't set) The domain name of the website to target for dynamic search ads. The maximum length is 2,048 characters. If the domain name includes `www`, it's trimmed and not used.<br><br>For existing campaigns, you can't edit the domain, but you must include it to update other properties. |
| DSA Domain Language | (Campaigns of type a) &quot;<i>DynamicSearchAds</i>&quot; or b) &quot;<i>Search</i>&quot; when the ExperimentId element isn't set) The language of the website pages to target for dynamic search ads. The supported domain languages are Dutch, English, French, German, Italian, Spanish, and Swedish.<br><br>For existing campaigns, you can't edit the language, but you must include it to update other properties. |
| Ad Group Name | The unique name that identifies an ad group. The maximum length is 128 characters. Trailing blank characters aren't saved (for example, &quot;Ad Group 1 &quot; is saved as &quot;Ad Group 1&quot;). |
| Ad Group Type | (Campaigns on the search network; read-only for existing ad groups) The ad group type: <i>Audience</i> (for audience campaigns only), <i>Search Dynamic</i> (for dynamic search ads only) and <i>Search Standard</i> (for responsive search ads and existing expanded text ads only). Some campaign types can include multiple ad group types. |
| Keyword | (Campaigns on the search network only) The keyword string. The maximum length is 50 characters.<br><br><b>Notes:</b><ul><li>To exclude a keyword at the ad group or campaign level, set the Match Type to `Negative`. If the row includes the ad group name, then the keyword is excluded for the ad group. If the row doesn't include the ad group name, the keyword is excluded for the entire campaign.</li><li>Changing a Microsoft Advertising keyword deletes the existing keyword and creates a new one with a new keyword ID. Changing the match type, however, doesn't delete the existing keyword.</li></ul> |
| Placement | Deprecated |
| Audience | The remarketing list for search ads (RLSA) target audience for the campaign or ad group. |
| Target Type | (RLSA targets only) The target type: <i>Inclusion</i> or <i>Exclusion</i>. |
| Auto Target Expression | Dynamic search targets for the ad group. For all targets, use &quot;All Web Pages.&quot;<br><br>To target up to three dynamic search criteria, use the format `<category>=<target>`, where &lt;category&gt; can include any of the categories below. Join multiple targets for an individual category with &quot;`[blank space] and [blank space]`&quot; and join multiple categories with &quot;`[blank space] and [blank space]`&quot;.<br><ul><li><i>Category:</i> To show dynamic search ads for indexed pages with a specific Google content category.</li><li><i>URL:</i> To show dynamic search ads for indexed pages with a specific URL, where the value may be included anywhere within the URL.</li><li><i>Page Title:</i> To show dynamic search ads for indexed pages with specific text in the page title.</li><li><i>Page Content:</i> To show dynamic search ads for indexed pages with specific content.</li></ul>Example: url=shoes.example.com and page title=footwear<br>Example: All Web Pages  |
| Location | A geographical location at which to place ads for the campaign or ad group; the values aren't case-sensitive. If you don't enter any values for the campaign or ad group, all locations are targeted. To target specific locations, enter the location using the Microsoft Advertising location code formats. To download a location list, log in to the Microsoft Advertising developer portal using your Microsoft Advertising advertising account credentials. <b> Note: To exclude a location, precede the location code with a minus sign (`-`), such as `-United States`. |
| Location Type | The location type, such as City, Country, MetroArea, PostalCode, and State. To download a location list, log in to the Microsoft Advertising developer portal using your Microsoft Advertising advertising account credentials. |
| Match Type | (Campaigns on the search network only) The keyword matching option(s). This may include the keyword matching option for a dynamic search target or product group. Values include : <i>Broad</i> (the default for new keywords), <i>Exact</i>, <i>Phrase</i>, <i>Content</i> (set automatically for keywords when the ad group targets the content network), <i>Negative</i> (to exclude a keyword on the content network), <i>Dynamic Ad Target</i> (the default for new dynamic search targets), <i>Product Group</i> (the default for new product groups), or <i>Negative Product Group</i> (to exclude a product group).  A value for either the match type or keyword ID is required to edit or delete a keyword with multiple match types.<br><br>For Broad Match Modifier, choose &quot;Broad&quot; and insert a `+` before any word within the keyword that's required (such as &quot;`+red +shoes`&quot; to require both &quot;red&quot; and &quot;shoes&quot;).<br><br>Changing the match type for a Microsoft Advertising keyword doesn't delete the existing keyword. |
| Max CPC | (Campaigns on the search network) The maximum cost per click (CPC), which is the highest amount to pay for an ad click based on the keyword, product group, or dynamic search target, with or without monetary symbols and punctuation.  For existing keywords and product groups records in optimized portfolios, updates are effective for only one day and are overwritten during the next optimization cycle. <b>Note:</b> You can't set bids for negative keywords. |
| Max Content CPC | (Read-only for CPC campaigns created before the content network deprecated in 2017 only ) The maximum content cost per click (CPC), which is the highest amount to pay for an ad click from a display network site, with or without monetary symbols and punctuation. |
| Audience Target Method | (Audience ad groups) Whether to:<ul><li><i>Target and Bid:</i> To show ads only to users associated with target audiences who also satisfy any other targets for the ad group.</li><li><i>Bid Only:</i>To show ads even to people who aren't associated with target audiences as long as they satisfy other ad group-level targets.</li></ul> You may increase the chances that ads are shown to specific audiences, however, by setting higher bids for those audiences. |
| Parent Product Groupings | The hierarchy of any parent product groups.<br><br>Example: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| Product Grouping | The product group (such as &quot;brand=acme&quot; or &quot;All Products&quot;).<br><br><b>Notes:</b><ul><li>When a specified product group doesn't exist in the Parent Product Groupings hierarchy, Search, Social, & Commerce creates any parts of the hierarchy that are needed.</li><li>Search, Social, & Commerce automatically creates an &quot;All Products&quot; group whenever you create an ad group in a Google Shopping campaign with a default bid set to the ad group default bid. Search, Social, & Commerce automatically creates an &quot;Everything Else&quot; group with the ad group default bid at each level of the product groups hierarchy. You can still explicitly create these default groups, and either exclude them or change their bids.</li><li>Each ad group can include up to eight tiers of product groups, including &quot;All Products&quot; and seven other tiers.</li></ul> |
| Partition Type | The partition type for the product group: <i>subdivision</i> (when it has child product groups) or <i>unit</i> (when it has no child product groups). |
| Ad Title, Ad Title 2-15 | (Expanded text ads, multimedia ads, responsive ads, and responsive search ads only) The headlines of an ad. The maximum length for each ad title field is 30 characters or 15 double-byte characters, including any dynamic text (such as the values of keywords, `{Param2}` and `{Param3}` dynamic substitution variables, and ad customizers).<br><br> For responsive search ads, insert an ad customizer using the following format, where "Default text" is an optional value to insert when your feed file doesn't include a valid value: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>For expanded text ads, Ad Title and Ad Title 2 are required, and Ad Title 3 is optional. Microsoft Advertising deprecated expanded text ads in August 2022, and you can now only report on and delete them.<br><br>For multimedia ads, responsive ads, and responsive search ads, Ad Title, Ad Title 2, and Ad Title 3 are required, and all other ad title fields are optional.<br><br>To delete the existing value for a non-required field, use the value `[delete]` (including the brackets).<br><br>For all ad types except for expanded text ads, changing the ad copy deletes the existing ad and creates a new ad with the same properties. |
| Ad Title 1-15 Position | (Responsive search ads only; optional) A position at which to pin the corresponding ad title: `[null]` (no value, which makes the ad title eligible for all positions), 1, 2, or 3. For example, if Ad Title Position has a value of 1, then Ad Title will appear only in Position 1. By default, all ad titles are null (have no values). To delete the existing value, use the value `[delete]` (including the brackets).<br><br><b>Note:</b> You can pin multiple ad titles to the same position. The ad network will use one of the ad titles pinned to the position. Titles pinned to position 3 may not be shown with the ad. |
| Description Line 1-4 | (Text ads, dynamic search ads, multimedia ads, responsive ads, responsive search ads, and enhanced campaign-level sitelinks only) The body of an ad or a sitelink.<br><br>For sitelinks, optionally use both Description Line 1 and Description Line 2 to include extra text that the ad network may display under the link text. Each description field can include up to 35 single-byte or 17 double-byte characters.<br><br>For ads, the maximum length for each description field is 90 characters or 45 double-byte characters, including any dynamic text (such as the values of keywords and ad customizers).<br><br>For responsive search ads, insert an ad customizer using the following format, where Default text is an optional value to insert when your feed file doesn't include a valid value: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>For text ads and dynamic search ads, Description Line 1 is required and Description Line 2 is optional.<br><br>For multimedia ads, responsive ads, and responsive search ads, Description Line 1 and Description Line 2 are required, and Description Line 3 and Description Line 4 are optional.<br><br>To delete the existing value, use the value `[delete]` (including the brackets).<br><br><b>Notes:</b><ul><li>(Standard text ads) The combined title and text must be at least three words.</li><li>(Expanded text ads) This field can optionally include the {Param2} and {Param3} dynamic substitution variables. If it does, the maximum length of the ad text is 300 single-byte or 150 double-byte characters. Microsoft Advertising deprecated expanded text ads in August 2022, and you can now only report on and delete them.</li><li>(Dynamic search ads) Dynamic substitution text isn't allowed.</li><li>For all ad types except expanded text ads, changing ad copy deletes the existing ad and creates a new one.</li></ul> |
| Description Line 1-4 Position | (Responsive search ads only; optional) A position at which to pin the corresponding description: `[null]` (no value, which makes the description eligible for all positions), 1, 2, or 3. For example, if Description 1 Position has a value of 1, then Description 1 will appear only in Position 1. By default, no descriptions are pinned to a position.<br><br>To delete the existing value, use the value `[delete]` (including the brackets).<br><br><b>Note:</b> You can pin multiple descriptions to the same position. The ad network will use one of the descriptions pinned to the position. Descriptions pinned to position 2 may not be shown with the ad. |
| Business Name | (Multimedia ads only) The business name, with a maximum of 25 characters. |
| Promotion Line | (Product Listing Ads only) A unique promotion line to be included with the product listing in search results (such as &quot;Free shipping now!). The maximum length is 45 characters.<br><br>The promotion line may appear in different locations relative to the ad (such as below the ad) depending on where the ad appears on the page. |
| Display URL | The URL that's included in the ad.<br><br>For expanded dynamic search ads, the ad network generates this value dynamically from the website domain, and you don't need to enter a value.<br><br>For expanded text ads and responsive search ads, you don't need to enter a value. The display URL is automatically extracted from the domain in the final URL. You optionally can customize the URL using the Path 1 and Path 2 fields.<br><br><b>Notes:</b><ul><li>(Accounts with final URLs) The domain names in the display URL and final URL must match.</li><li>Microsoft Advertising deprecated expanded text ads in August 2022, and you can now only report on and delete them.</li></ul> |
| Display Path 1 | (Expanded text ads, dynamic search ads, and responsive search ads only) Text that's added to the display URL that's automatically extracted from the final URL. Each path is preceded in the URL by a forward slash (/). A path can't contain forward slash (/) or newline (\n) characters. The maximum length for each path is 15 characters or 7 double-byte characters.<br><br>To insert an ad customizer, use the following formats, where "Default text" is an optional value to insert when your feed file doesn't include a valid value: `{CUSTOMIZER.Attribute name:Default text}`, such as `{CUSTOMIZER.Discount:10%}`<br><br>For example, if Display Path 1 is &quot;deals,&quot; then the display URL would be &lt;display URL&gt;/deals, such as www.example.com/deals.<br><br>Microsoft Advertising deprecated expanded text ads in August 2022, and you can now only report on and delete them. |
| Display Path 1 | (Expanded text ads, dynamic search ads, and responsive search ads only) An additional display path; see the entry for Display Path 1.<br><br>Example: If Display Path 1 is &quot;deals&quot; and Display Path 2 is &quot;local,&quot; then the display URL would be &lt;<i>display URL</i>&gt;/deals/local, such as www.example.com/deals/local. |
| Start Date | (Enhanced sitelinks only) The first date on which bids may be placed for the sitelink, in the advertiser's time zone and in one of the following formats: m/d/yyyy, m/d/yy, m-d-yyyy, or m-d-yy. The default for new enhanced sitelinks is the current day. <b>Note:</b> New enhanced sitelinks can be created only in campaigns with existing enhanced sitelinks or no sitelinks. |
| End Date | The last date on which the sitelink can appear with ads, in the advertiser's time zone and in one of the following formats: m/d/yyyy, m/d/yy, m-d-yyyy, or m-d-yy. For a new sitelink, the default is `[blank]` (that is, no end date). |
| Call To Action | The call to action to include in the ad. See the [API reference for a list of possible values](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction), but enter multi-word calls to action as multiple words (such as &quot;Bet Now&quot; instead of &quot;BetNow&quot;) in bulksheets. |
| Call To Action Language | The language for the call to action options. See the [API reference for a list of possible languages](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| Base URL/Final URL | The landing page URL to which search engine users are taken when they click your ad, including any append parameters configured for the campaign or account. Base/final URLs at the keyword level override those at the ad level and higher.<br><br>To delete the existing value, use the value `[delete]` (including the brackets). |
| Destination URL | (Included in generated bulksheets for information purposes; not posted to the search engine) For accounts with destination URLs, this is the URL that links an ad to a base URL/landing page on the advertiser's website (sometimes via another site that tracks the click and then redirects the user to the landing page). It includes any append parameters configured for the Search, Social, & Commerce campaign or account. If you generated tracking URLs, this is based on the tracking parameters in your account settings and campaign settings. If you appended search engine-specific parameters, they may be replaced with the equivalent parameters for Search, Social, & Commerce.<br><br>For accounts with final URLs, this column shows the same value as the Base URL/Final URL column. |
| Custom URL Param | Data to substitute for the `{custom_code}` dynamic variable when the variable is included in the tracking parameters for the search account or campaign settings. To insert the custom value in the tracking URL, you must upload the bulksheet file using the Generate Tracking URLs option. |
| Creative Type | The ad format: <i>Dynamic Search Ad</i>, <i>Expanded Text Ad</i>, <i>Expanded Dynamic Search Ad</i>, <i>Multimedia Ad</i>, <i>Product Ad</i> (shopping ads), or <i>Responsive Search Ad</i>, or <i>Text ad</i>. The default for new ads is <i>Text ad</i>. |
| Ad Group Start Date | The first date on which bids may be placed for the ad group, in the advertiser's time zone and in one of the following formats: m/d/yyyy, m/d/yy, m-d-yyyy, or m-d-yy. For a new ad group, the default is the current date. |
| Ad Group End Date | The last date on which bids may be placed for the ad group, in the advertiser's time zone and in one of the following formats: m/d/yyyy, m/d/yy, m-d-yyyy, or m-d-yy. For a new ad group, the default is [blank] (that is, no end date). |
| Tracking Template | (Optional) The tracking template, which specifies all off-landing domain redirects and tracking parameters and embeds the final URL in a parameter. The tracking template at the most granular level (with keyword as the most granular) overrides the values at all higher levels.<br><br>For Adobe Advertising conversion tracking, which is applied when the campaign settings include &quot;EF Redirect&quot; and &quot;Auto Upload,&quot; Search, Social, & Commerce automatically appends redirect and tracking code when you save the record.<br><br>For third-party redirects and tracking, enter a value.<br><br>For a list of parameters to indicate final URLs in tracking templates, see the Microsoft Advertising documentation.<br><br> To delete the existing value, use the value `[delete]` (including the brackets). |
| Landing Page Suffix | Any parameters to append to the end of final URLs to track information. Example: `param2=value1&param3=value2`<br><br>See "[Click-tracking formats for [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)."<br><br>Final URL suffixes at lower levels override the account-level suffix. For easier maintenance, use only the account-level suffix unless different tracking for individual account components is necessary. To configure a suffix at the ad group level or lower, use the Microsoft Advertising editor. |
| Search Network Status | Whether to place ads for the ad group on various elements of the Search Network:<ul><li><i>All:</i> To place ads on all Bing search networks and syndicated search partners.</li><li><i>OwnedAndOperatedOnly:</i>To place ads only on Bing and Yahoo! websites.</li><li><i>SyndicatedSearchOnly:</i> To place ads only on Bing and Yahoo! syndicated search partners.</li><li><i>Off:</i> To place ads on the Content Network only (not the Search Network).</li></ul> For new ad groups, the default is On. |
| Content Network Status | Deprecated |
| Languages | The target language for ads in the ad group: English, French, Finnish, German, Norwegian, Spanish, or Swedish. The default for new campaigns is English.<br><br>This setting determines the countries and regions in which your ad can be displayed. Make sure to choose a language compatible with the campaign's location targets. |
| Budget Type | Whether the budget is <i>Daily</i> (the default) or <i>Monthly</i>.<br><br>Note: If you assign the campaign to an optimized portfolio, this value is automatically set to Daily. |
| Device | A device type for which bid adjustments are made at the campaign or ad group level: <i>smartphone</i>, <i>tablet</i>, or <i>desktop</i>. |
| Bid Adjustment | The bid adjustment for a specified target type. For example, if the keyword-level bid is 1 USD and the bid adjustment for smartphones is 50%, then the smartphone bid is 1.50 USD. By default, all targets are bid at the keyword-level bid. Valid percentages can include:<ul><li>Smartphones and tablets: &ndash;100 (to not bid for the device type) and from &ndash;90 to 900</li><li>Desktop: from 0 to 900</li></ul> |
| Creative Preferred Devices | The device types on which you prefer to display the ad or sitelink: <i>All</i> (the default) or <i>Mobile</i>. When Mobile is specified, the network will try to display the ad or sitelink to mobile device users rather than desktop or tablet users. Otherwise, the network will display the ad or sitelink on any device type. <b>Note:</b> The network doesn't guarantee that it will display the ad on the preferred device type. |
| Param2 | The string to use as the substitution value if the keyword's base URL or the ad's title, description, or base URL contains the `{Param2}` dynamic substitution string. The maximum length is 70 characters, but be aware of the maximum length of the ad element in which you will use it (for example, Title 1 and Title 2 combined may be a maximum of 76 characters). To delete the existing value, use the value `[delete]` (including the brackets). |
| Param3 | The string to use as the substitution value if the keyword's base URL or the ad's title, description, or base URL contains the `{Param3}` dynamic substitution string. The maximum length is 70 characters, but be aware of the maximum length of the ad element in which you will use it (for example, Title 1 and Title 2 combined may be a maximum of 76 characters). To delete the existing value, use the value `[delete]` (including the brackets). |
| Link Name | The sitelink text. It must be unique within the campaign. If you specify Description1 and Description2, then the sitelink text can include up to 25 single-byte or 12 double-byte characters; otherwise, the sitelink text can include up to 35 single-byte or 17 double-byte characters.<br><br>Microsoft Advertising may display two, four, or six enhanced sitelinks with descriptions, or four or six sitelinks in a single row without descriptions, with an ad.<br><br>You can create new enhanced sitelinks only in campaigns with existing enhanced sitelinks or no sitelinks. |
| Campaign Status | The display status of the campaign: <i>Active</i>, <i>Paused</i>, or <i>Deleted</i> (existing campaigns only). The default for new campaigns is Active. To delete an active or paused campaign, enter the value `Deleted`. |
| Ad Group Status | The display status of the ad group: <i>Active</i>, <i>Paused</i>, or <i>Deleted</i> (existing ad groups only). The default for new ad groups is Active. To delete an active or paused ad group, enter the value `Deleted`. |
| Keyword Status | The display status of the keyword: <i>Active</i>, <i>Paused</i>, or <i>Deleted</i> (existing keywords only). The default for new keywords is Active. To delete an active or paused keyword, enter the value `Deleted`. <b>Note:</b> If you create tracking URLs for a keyword with multiple match types, then the keyword status for each match type must be the same. |
| Placement Status | Deprecated |
| Ad Status | The display status of the ad: <i>Active</i>, <i>Deleted</i> (existing ads only), <i>Disapproved</i> (not editable), or <i>Paused</i>. The default for new ads is Active. To delete an active or paused ad, enter the value `Deleted`. |
| Target Status | The status of a dynamic search target: <i>Active</i>, <i>Paused</i>, or <i>Deleted</i> (existing targets only). The default for new targets is Active. To delete an active or paused target, enter the value `Deleted`. |
| Sitelink Status | The display status of the sitelink: <i>Active</i> or <i>Deleted</i> (existing sitelinks only). The default for new sitelinks is Active. To delete an active sitelink, enter the value `Deleted`. |
| Location Status | The status of the location target: <i>Active</i> or <i>Deleted</i> (existing locations only). The default for new locations is Active. To delete an active location, enter the value `Deleted`. |
| Product Group Status | The display status of the product group: <i>Active</i> or <i>Deleted</i> (existing product groups only). The default for new product groups is Active. To delete an active product group, enter the value `Deleted`. |
| Device Target Status | The status of the campaign- or ad group-level device target: <i>Active</i> or <i>Deleted</i>. For new campaigns and ad groups, the default is Active. |
| RLSA Target Status | The status of the campaign- or ad group-level RLSA target or (Google Ads only) exclusion: <i>Active</i> or <i>Deleted</i> (existing targets only). The default for new targets or exclusions is Active. To delete an active target or exclusion, enter the value `Deleted`. |
| \[Advertiser-specific Label Classification\] | (Named for an advertiser-specific label classification, such as &quot;Color&quot; for a label classification called Color) A value for the specified classification that is associated with the entity. You can include only one value per classification per entity (such as &quot;red&quot; for the &quot;Color&quot; label classification for Campaign A). The maximum length is 100 characters, and the value can include ASCII and non-ASCII characters.<br><br>Label classifications and their label values are applied to all child components; new components that are added later are automatically associated with the label. Label classifications for product groups are applied to the unit (most granular) level.<br><br>Neither the classification name nor the classification value is case-sensitive. |
| Constraints | A constraint that's assigned to the entity. You can assign only one constraint per entity.<br><b>>Constraints are inherited by child entities, so you don't need to enter values for child entities unless you want to override the inherited values. |
| Campaign ID | The unique ID that identifies an existing campaign. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change the campaign name, unless the row includes an &quot;AMO ID&quot; for the campaign. |
| Ad Group ID | The unique ID that identifies an existing ad group. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change the campaign name, unless the row includes an &quot;AMO ID&quot; for the ad group. |
| Placement ID | Deprecated |
| Keyword ID | The unique ID that identifies an existing keyword. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change the keyword, unless the row includes a) sufficient property columns to identify the keyword or b) an &quot;AMO ID.&quot; |
| Ad ID | <p>The unique ID that identifies an existing ad. In CSV and TSV files, it must be preceded by a single quote (').[^1] For responsive search ads, either the Ad ID or AMO ID is required to edit or delete ad data. For all other entity types, the AMO ID is required only when you change the ad status, unless the row includes a) sufficient ad property columns to identify the ad or b) an &quot;AMO ID.&quot; However, if you include neither the Ad ID nor AMO ID, and the ad property columns match multiple ads, then the status for only one of the ads will change.</p><p><b>Note:</b> If you edit a) ad property columns except Status for an existing ad or b) any data for a responsive search ad, and you include neither the Ad ID nor AMO ID, then a new ad is created, and the existing ad isn't changed. </p> |
| Sitelink ID | The unique ID that identifies an existing sitelink. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change or delete the sitelink, unless the row includes a) sufficient property columns to identify the sitelink or b) an &quot;AMO ID.&quot; However, if you include neither Sitelink Ad ID nor AMO ID, and the property columns match multiple sitelinks, then the status for only one of the sitelinks will change.</p><p><b>Note:</b> If you edit sitelink property columns except Status for an existing sitelink, and you include neither the Sitelink ID nor AMO ID, then a new sitelink is created, and the existing sitelink isn't changed. |
| Product Group ID | The unique ID that identifies an existing product group. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change or delete the product group, unless the row includes a) sufficient property columns to identify the product group or b) an &quot;AMO ID.&quot; |
| Location ID | The unique Microsoft Advertising identifier for the location target. To download a location list, log in to the Microsoft Advertising developer portal using your Microsoft Advertising advertising account credentials. Required only when you change or delete the location target, unless the row includes an &quot;AMO ID&quot; for the target. |
| Target ID | The unique ID that identifies an existing auto target. Required only when you change or delete the auto target, unless the row includes an &quot;AMO ID&quot; for the target. |
| RLSA Target ID | The unique ID that identifies an existing campaign- or ad group-level RLSA target. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change or delete the target or exclusion, unless the row includes an &quot;AMO ID&quot; for the target. |
| AMO ID | (In generated bulksheets) An Adobe-generated unique identifier for a synced entity. For responsive search ads, the AMO ID is required to edit or delete ads unless you include the Ad ID. To edit data for all other entity types with an AMO ID, the AMO ID is required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |
| EF Error Message | (Included in generated bulksheets for information purposes) Placeholder for displaying error messages from the ad network regarding data in the row; error messages are included in EF Errors files. This value isn't posted to the ad network. |
| SE Error Message | (Included in generated bulksheets for information purposes) Placeholder for displaying error messages from the ad network regarding data in the row; error messages are included in SE Errors files. This value isn't posted to the ad network. |
| Exemption Request | (Included in generated bulksheets for information purposes) Placeholder for displaying the names and text of any Google advertising policies that an ad violates. |
| Retail Hash | (Included for information purposes in bulksheets generated using Advanced Campaign Management) An alphanumeric hash code (such as f9639f40cdf56524b541e5dacf55a991) that indicates the item was generated using the Advanced (ACM) view. |

<table style="table-layout:auto">

<!-- EDIT ALL -- Copied from Google page -->

<!-- 

## Fields required to create, edit, or delete each account component

### Campaign fields

Campaign Name
Campaign Budget
Campaign Status
Delivery Method
Device OS Targets (Google Adwords)
Device Targets
Languages
Mobile Carriers (Google Adwords)
Networks
Tracking Template
Channel Type
Campaign Priority
Merchant ID
Sales Country
Product Scope Filter
Audience Target Method
DSA Domain Name
DSA Domain Language
Landing Page Suffix
Label Classification

### Ad group fields

Campaign Name
Ad Group Name
Ad Group Type
Networks
Ad Group Status
Max CPC
Max Content CPC
Tracking Template
Audience Target Method
Label Classification


## Keyword fields

Campaign Name
Ad Group Name
Keyword Status
Max CPC
Tracking Template
URLs (Base URL/Final URL, Destination URL)
Exemption Request (Google Adwords)
First Page Bid
Keyword
Match Type
Param1
Param2
Quality Score
Custom URL Param
Label Classification


### Text/Product ad fields

Uses "Creative (except RSA)" row in Download Bulksheet dialog

### Dynamic search ad fields

Note: Create support not available

### Multimedia/Responsive ad fields

### Responsive search ad fields

Uses "Responsive Search Ad" row in Download Bulksheet dialog

### Dynamic search target (auto target) fields
Note: Create support not available

### Shopping product group fields

### Campaign-level sitelink fields

### Location Target fields

### Device Target fields

### RLSA Target

-->

>[!MORELIKETHIS]
>
>* [Appendix - Bulksheet errors](../bulksheet-errors.md)
>* [Operations you can perform in bulksheets](bulksheet-operations.md)
>* [Supported bulksheet file formats](bulksheet-file-formats.md)
>* [Download/Create a bulksheet file](../bulksheet-download.md)
>* [Click-tracking formats for [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Upload a bulksheet file or corrected error file](../bulksheet-upload.md)
