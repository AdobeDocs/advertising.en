---
title: Required bulksheet data for [!DNL Google Ads] accounts
description: Reference the required header fields and data fields in bulksheets for [!DNL Google Ads] accounts.
exl-id: 756b77fe-f95d-469f-9ae0-7424c2fad0b1
feature: Search Bulksheets
---
# Appendix - Required bulksheet data for [!DNL Google Ads] accounts

To create and update [!DNL Google Ads] campaign data in bulk, you can use Search, Social, & Commerce bulksheet files formatted specifically for [!DNL Google Ads] accounts. You can either a) [generate bulk sheet files for existing accounts](../bulksheet-download.md) in the required file format or b) create them manually (see "[Supported Bulksheet File Formats](bulksheet-file-formats.md)" for general information about the supported file formats).

Each bulksheet must include the header fields and corresponding data fields required for the [specific operations you want to perform](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (such as creating an ad). When a field isn't required, you can omit it from the header and data rows. All custom columns are deleted when you upload the bulk sheet file.

Following are a table of all available data fields and additional tables indicating which fields are required to add, edit, or delete data for individual entities (such as campaigns and keywords).

## All available data fields {#bulksheet-fields-all-google}

The following table describes all available data fields.

For the data fields relevant for account entities, see "[Fields required to create, edit, or delete each account component](#bulksheet-fields-per-component-google)."

>[!NOTE]
>
>* The values in all text columns are case-sensitive.
>* When you create a new record and don't include values for all required data fields, then some of those fields are assigned the specified default values.
>* For fields that aren't specified below, the default value for the ad network is used.
>* For a list of available bulksheet rows in the [!UICONTROL Download Bulksheet] dialog, see "[Bulksheet rows by ad network](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network)."

| Field | Description |
| ---- | ---- |
| [!UICONTROL Platform] | (Included in generated bulksheets for information purposes) The ad platform. Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity.|
| [!UICONTROL Acct Name] | The unique name that identifies an ad network account. Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | The unique name that identifies a campaign for an account. |
| [!UICONTROL Campaign Budget] | A daily spending limit for the campaign, with or without monetary symbols and punctuation. This value overrides but can't exceed the account budget. |
| [!UICONTROL Delivery Method] | <p>How quickly to show ads for the campaign each day:</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> (the default for new campaigns): To spread your ad impressions across the day.</p></li><li><p><i>[!UICONTROL Accelerated]:</i> (Deprecated in October 2019) To display your ads as often as possible until your budget is reached. As a result, your ads may not appear later in the day.</p></li></ul> |
| [!UICONTROL Channel Type] | <p>The channels on which to place ads. Specify one or more options:</p><ul><li><p><i>[!UICONTROL Search]</i> (the default for new campaigns): To place ads on the [!DNL Google Ads] search network (including [!DNL Google Ads] search and search partner websites) and optionally also on the [!DNL Google Ads] display network. <b>Note:</b> Campaigns that target both the search network and the display network can't be added to a portfolio for bid optimization.</p></li><li><p><i>[!UICONTROL Display]</i>: To place ads only on the [!DNL Google Ads] display network.</p></li><li><p><i>[!UICONTROL Shopping]</i>: To place shopping ads on [!DNL Google Ads] shopping  network (in select countries) and the [!DNL Google Ads] search network (including [!DNL Google Ads] search and search partner websites). To create shopping ads, you must have products in a [!DNL Google Merchant Center] account and [allow Search, Social, & Commerce to download data from the account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). See &quot;[Implement [!DNL Google Ads] shopping campaigns](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)&quot; for more information about the process of creating shopping ads.</p></li></ul> |
| [!UICONTROL Networks] | <p>Where to place ads. Specify one or more options:</p><ul><li><p><i>[!UICONTROL Google Search]</i>: Sponsored search listings on the Google Search Network only.</p></li><li><p><i>[!UICONTROL Search Partners]</i>: Sponsored search listings on Google's search partners.</p></li><li><p><i>[!UICONTROL Content]</i>: To place bids for display network listings.</p></li><li><p><i>[!UICONTROL All]</i> (the default for new campaigns): Targets Google Search, Search Partners, and Content.</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>(Search Network only; applicable to expanded dynamic search ads only) The root domain (such as example.com) or subdomain (such as shoes.example.com) of the website whose content that the ad network uses to target your dynamic search ads.<br><br><b>Notes:</b></p><ul><li><p>Expanded dynamic search ads target website content, rather than keywords.</p></li><li><p>Your domain must be indexed by the ad network's organic search index to be targeted.</p></li><li><p>If you don't specify a domain, then you must create dynamic search targets, which target either all of your website pages or a subset of them, for each ad group.</p></li></ul> |
| [!UICONTROL DSA Domain Language] | (Search Network only; applicable to expanded dynamic search ads only) The language for the specified website domain. <b>Note:</b> If the domain contains pages in multiple languages and you want to target all of them, create a separate campaign for each language. |
| [!UICONTROL GDN Custom Bid Level] | (Campaigns that target the display network only) How to bid: by <i>[!UICONTROL Ad Group]</i> (the default), <i>[!UICONTROL Keyword]</i>, <i>[!UICONTROL Placement]</i> (website), or <i>[!UICONTROL None]</i> (to reset the existing value). Other dimensions (<i>Age</i>, <i>Gender</i>, <i>Interest and List</i>, <i>Topic</i>, and <i>Vertical</i>) are available from the [!DNL Google Ads] interface. If you've used the [!DNL Google Ads] interface to configure bidding by another dimension, that value is shown, but you can't select or enter those dimensions here.</p><p><b>Note:</b></p><ul><li><p>When you bid by keyword, create tracking templates at the keyword level. Similarly, when you bid by placement, create tracking templates at the placement level. For all other dimensions, create tracking templates at the ad level.</p></li><li><p>When you bid by an unsupported dimension (Age, Gender, Interest and List, or Topic), Search, Social, & Commerce doesn't optimize bids for the dimension, and all attribution is applied to the ad group.</p></li><li><p>Ads on the search network always use keyword bids.</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>(Shopping campaigns only) The priority with which the campaign is used when multiple campaigns advertise the same product:  <i>[!UICONTROL Low]</i> (the default for new campaigns), <i>[!UICONTROL Medium]</i>, or <i>[!UICONTROL High]</i>.</p><p>When the same product is included in more than one campaign, the ad network uses the campaign priority first to determine which campaign (and associated bid) is eligible for the ad auction. When all campaigns have the same priority, the campaign with the highest bid is eligible. |
| [!UICONTROL Merchant ID] | (Shopping campaigns and audience campaigns linked to a merchant feed only) The customer ID of the merchant account whose products are used for the campaign. |  |
| [!UICONTROL Sales Country] | (Shopping campaigns only; read-only for existing campaigns) The country in which the campaign's products are sold. Because products are associated with target countries, this setting determines which products are advertised in the campaign. |
| [!UICONTROL Product Scope Filter] | (Campaigns using the [!DNL Google Ads] shopping network only) The products in your [!DNL Google Merchant Center] account for which shopping ads can be created for the campaign. You can enter up to seven product dimension and attribute combinations on which to filter your products, using the format dimension=attribute. Separate multiple filters with a &quot;&gt;&gt;&quot; delimiter. For a list of available product dimensions, see &quot;[Shopping campaign product filters](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;</p><p>Example: &quot;CategoryL1=animals&gt;&gt;CategoryL2=pet supplies&gt;&gt;Brand=Acme Pet Supplies&quot;</p><p>To delete the existing values, use the value <code>[delete]</code> (including the brackets).</p> |
| [!UICONTROL Languages] | <p>(Search and Display networks only) The target languages for ads in the campaign.</p><p>If you don't enter a value for either this field or the [!UICONTROL Geo Targeting] field for a new campaign, the currency specified for the account determines the default languages, except that campaigns with currencies that aren't mapped to specific languages (for example, EUR) are targeted to all languages. If you don't enter a value for this field but enter a value in the [!UICONTROL Geo Targeting] field for a new campaign, this defaults to <i>[!UICONTROL All]</i>. If you leave this field blank for an existing campaign, the existing value is retained.</p><p>To target all languages, enter <span style="font-style: italic;"><i[!UICONTROL >All]</i></span>. To target specific languages, enter values separated by semi-colons using either <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] language names</a> (such as <i>English;Japanese</i>, which are substituted with the correct numeric codes) or numeric codes (such as <i>1000;1005</i>). The values aren't case-sensitive.</p> |
| [!UICONTROL Location] | A geographical location at which to place ads, or for which to exclude ads, for the campaign. If you don't enter any values for either this field or the Languages field for a new campaign, then the currency specified for the account determines the default locations, except that campaigns with currencies that aren't mapped to specific locations (for example, EUR) are targeted to all locations. If you don't enter a value for this field but enter a value in the [!UICONTROL Languages] field for a new campaign, then this defaults to <i>[!UICONTROL All]</i>. If you leave this field blank for an existing campaign, then the existing value is retained.</p><p>To target a specific location, use one of [[!DNL Google Ads] location names](https://developers.google.com/adwords/api/docs/appendix/geotargeting) (which are substituted with the correct numeric code) or location codes:</p><ul><li><p>Countries/territories: Enter the country/territory names (such as <i>United States;Japan</i>) or the numeric codes (such as <i>2840;2392</i>).</p></li><li><p>States/provinces/regions: Enter the state/province/region names with the related country/territory abbreviations (such as <i>Tokyo, JP;New York, US</i>) or the numeric codes (such <i>20636;21167</i>).</p></li><li><p>Non-U.S. cities: Enter the city name, state/province/region name, and country/territory abbreviations (such as <i>Adachi, Tokyo, JP;Kita, Tokyo, JP</i>), or the numeric codes (such as <i>1028850;1009293</i>)</p></li><li><p>US metro areas: Enter the city names, state names, and country abbreviations (such as <i>Buffalo NY, US;New York NY, US</i>) or the numeric codes (such as <i>514;501</i>).</p></li></ul><p>To exclude a location, precede the location name or code with a minus sign (`-`), such as <i>-Japan</i>.</p><p><b>Note:</b> The values aren't case-sensitive.</p> |
| [!UICONTROL Location Type] | (When you include a Location) The [location type](https://developers.google.com/google-ads/api/data/geotargets).|
| [!UICONTROL Device] | A device type for which bid adjustments are made at the campaign or ad group level: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i>, or <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | <p>(When you include a [!UICONTROL Location], [!UICONTROL Device], or [!UICONTROL RLSA] target) Whether to adjust bids for ads in a specific location, on a specific device type, or with a specific audience target:</p><ul><li><p>To use the keyword-level bid (0% difference), enter 0. For new targets, you can also leave this blank.</p></li><li><p>To use a different bid for this target, enter the percentage by which to increase or decrease bids.</p></li><ul><li><p>For location and RLSA targets, valid percentages include from -90 to 900.</p></li><li><p>For device bid adjustments, valid percentages include:</p></li><ul><li><p>(Campaigns)-100 (to not bid for ads on the device type) or from -90 to 900.</p></li><li><p>(Ad groups) -100 for smartphones and tablets (to not bid for the device type), and from -90 to 900 for all device types.</p></li></ul></ul><li><p>(Existing campaigns and ad groups) To use the existing bid adjustment, leave this blank.</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | (Included in generated bulksheets for information purposes) The read-only bid adjustment that Adobe recommends for campaign-level location target or an RLSA. It's calculated only when the campaign is in a portfolio with an objective that uses weighted conversion metrics (not the [!UICONTROL Maximize Clicks] objective), and the campaign contains at least two location targets or RLSAs with at least five clicks or 5 USD in cost over the last 90 days.</p><p>If you want to manually edit a location target or RLSA to use the recommended value, wait at least two weeks after you create the location target or RLSA to allow for sufficient data collection, and don't change the value more than once a week. |
| [!UICONTROL Device Targets] | <p>(Legacy campaign types only) The devices on which the ad may be shown: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Smartphones]</i>, or <i>[!UICONTROL Tablets]</i>. For new campaigns, the default is <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | (Legacy campaign types only; applicable when the Device Targets include &quot;Smartphones&quot; or &quot;Tablets&quot;) The operating systems on which the ad may be shown: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Android]</i>, <i>[!UICONTROL iOS]</i>, or <i>[!UICONTROL Palm]</i>. For new campaigns, the default is <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>(Legacy campaign types only; applicable when the [!UICONTROL Device Targets] include &quot;[!UICONTROL All]&quot; or &quot;[!UICONTROL Smartphones]&quot;) Mobile carriers to which the smartphones may be connected: <i>[!UICONTROL All]</i>, or one or more carriers indicated by &lt;c<i>carrier code</i>&gt;,&lt;<i>country code</i>&gt; (such as T-Mobile,US) using the list of <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">available carriers and codes for [!DNL Google Ads]</a>. Separate multiple carriers with semi-colons (such as T-Mobile,US;T-Mobile,GB). For new campaigns, the default is <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Ad Group Name] | <p>The unique name that identifies an ad group. The maximum length is 255 characters; trailing blank characters aren't saved (for example, &quot;Ad Group 1 &quot; is saved as &quot;Ad Group 1&quot;). This field isn't applicable for campaign-level sitelinks or campaign-level device targets.</p> |
| [!UICONTROL Ad Group Type] | <p>The ad group type: <i>[!UICONTROL Discovery]</i> (for discovery campaigns only), <i>[!UICONTROL Display]</i> (for display campaigns), <i>[!UICONTROL Search Dynamic]</i> (for expanded dynamic search ads), <i>[!UICONTROL Search Standard]</i> (for search ads), <i>[!UICONTROL Shopping Product]</i> (for shopping product ads), <i>[!UICONTROL Shopping Showcase]</i> (creation and editing not supported), or <i>[!UICONTROL Unknown]</i>.</p> |
| [!UICONTROL Max CPC] | <p>(CPC campaigns only) The maximum cost per click (CPC), which is the highest amount to pay for an ad click on the ad network, with or without monetary symbols and punctuation. You can set values for ad groups and keywords, product groups, and dynamic search targets. The default for a new keyword is inherited from the ad group level. For product groups, you can set values for the lowest product group tier; the default for a new tier is inherited from the parent tier.</p><p>For existing product groups and dynamic search targets in optimized portfolios, updates are effective for only one day and are overwritten during the next optimization cycle.</p> |
| [!UICONTROL Max Content CPC] | <p>(CPC campaigns only) The maximum content cost per click (CPC), which is the highest amount to pay for an ad click from a display network site, with or without monetary symbols and punctuation. You can set and edit values at the ad group level in campaigns that aren't placement-targeted.</p> |
| [!UICONTROL Audience Target Method] | <p>(Campaigns on only the search network, and existing, read-only [!DNL Gmail] campaigns on the display network) Whether to:</p><ul><li><p><i>[!UICONTROL Target and Bid]</i>: To show ads only to users associated with target audiences who also satisfy any other targets for the ad group.</p></li><li><p><i>[!UICONTROL Bid Only]</i>: To show ads even to people who aren't associated with target audiences as long as they satisfy other ad group-level targets.</p><p>You may increase the chances that ads are shown to specific audiences, however, by setting higher bids for those audiences.</p></li></ul> |
| [!UICONTROL Keyword] | The keyword string. The maximum length is 80 characters and no more than 10 words, and it can include only letters, digits, and the following special characters: space `# $ & _ - " [ ] ' + . / :`</p><p><b>Note:</b></p><ul><li><p>To exclude a keyword at the ad group or campaign level, set the [!UICONTROL Match Type] to <i>[!UICONTROL Negative]</i>. If the row includes the ad group name, the keyword is excluded for the ad group. If the row doesn't include the ad group name, the keyword is excluded for the entire campaign.</p></li><li><p>Changing a [!DNL Google Ads] keyword or match type deletes the existing keyword and creates a new one.</p></li></ul> |
| [!UICONTROL Placement] | (Campaigns using content match only) A placement in the display network on which your ads may be displayed. Specify one of the following:</p><ul><li><p>Web site: Enter a valid URL. It can be a top-level domain, first-level subdomain, or domain with a single directory name. The URL can't include a question mark (?). Examples:<code><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</code></p></li><li><p>An ad position on a specific page: Use the format `<URL> >> <location,sublocation>` (such as `finance.google.com >> Company pages,Top right`).</p></li><li><p>A topic category: Use the syntax `<category::<category> > <subcategory>` and so on (such as `category::Industries > Energy & Utilities > Oil & Gas`).</p></li></ul><p><b>Note:</b> To exclude a placement at the ad group or campaign level, set the [!UICONTROL Match Type] to <i>[!UICONTROL Negative]</i>. If the row includes the ad group name, the placement is excluded for the ad group. If the row doesn't include the ad group name, the placement is excluded for the entire campaign.</p> |
| [!UICONTROL Auto Target Expression] | <p>(Required when the campaign setting to &quot;[!UICONTROL Use my website contents to target my ads]&quot; isn't enabled; optional otherwise) Dynamic search targets for the ad group.</p><p>For all targets, use an asterisk (*).</p><p>To target up to three dynamic search criteria, use the format `<category>=<target>`, where `<category>` can include any of the categories below. Join multiple targets for an individual category with &quot;\[blank space\] and \[blank space\]&quot; and join multiple categories with &quot;[blank space] and [blank space]&quot;.</p><ul><li><p><i>[!UICONTROL Category]</i>: To show expanded dynamic search ads for indexed pages with a specific [!DNL Google Ads] content category.</p></li><li><p><i>[!UICONTROL URL]</i>: To show expanded dynamic search ads for indexed pages with a specific URL, where the value may be included anywhere within the URL.</p></li><li><p><i>[!UICONTROL Page Title]</i>: To show expanded dynamic search ads for indexed pages with specific text in the page title.</p></li><li><p><i>[!UICONTROL Page Content]</i>: To show expanded dynamic search ads for indexed pages with specific content.</p></li></ul><p>Example: url=shoes.example.com and page title=footwear</p> |
| [!UICONTROL Parent Product Groupings] | The hierarchy of any parent product groups.<br><br>Example: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>The product group (such as &quot;brand=acme&quot; or &quot;All Products&quot;).</p><p><b>Note:</b></p><ul><li><p>When a specified product group doesn't exist in the [!UICONTROL Parent Product Groupings] hierarchy, Search, Social, & Commerce creates any parts of the hierarchy that are needed.</p></li><li><p>Search, Social, & Commerce automatically creates an &quot;[!UICONTROL All Products]&quot; group when you create an ad group in a [!DNL Google Ads] Shopping campaign with a default bid set to the ad group default bid. Search, Social, & Commerce automatically creates an &quot;[!UICONTROL Everything Else]&quot; group with the ad group default bid at each level of the product group hierarchy. You can still explicitly create these default groups, and either exclude them or change their bids.</p></li><li><p>Each ad group can include up to eight tiers of product groups, including &quot;[!UICONTROL All Products]&quot; and seven other tiers.</p></li></ul> |
| [!UICONTROL Partition Type] | The partition type for the product group: <i>subdivision</i> (when it has child product groups) or <i>unit</i> (when it has no child product groups). |
| [!UICONTROL Match Type] | <p>For dynamic search target or product groups: The keyword matching option for the dynamic search target or product group: <i>[!UICONTROL Dynamic Ad Target]</i> (the default for new dynamic search targets), <i>[!UICONTROL Product Group]</i> (the default for new product groups) or <i>[!UICONTROL Negative Product Group]</i> (to exclude a product group).</p><p>For keywords: The keyword matching option for the keyword: <i>[!UICONTROL Broad]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Exact]</i>, or <i>[!UICONTROL Negative]</i> (to exclude a keyword or a placement on the display network); product groups that are used with shopping ads have a match type of <i>[!UICONTROL Product Group]</i>. If you use <i>[!UICONTROL Negative]</i>, you must also include the match type to be excluded (for example, &quot;Negative Phrase&quot;).</p><p>For new keywords, the default is <i>[!UICONTROL Broad]</i>. A value for either the match type or keyword ID is required only to edit a keyword with multiple match types.</p><p><b>Note:</b></p><ul><li><p>Match types aren't applicable to expanded dynamic search ads, which don't use keywords.</p></li><li><p>Changing the match type for a [!DNL Google Ads] keyword deletes the existing keyword and creates a new one.</p></li><li><p>For Broad Match Modifier, choose &quot;Broad&quot; and insert a + before any word within the keyword for which close variants are required (such as &quot;+red +shoes&quot; to require close variants of both &quot;red&quot; and &quot;shoes&quot;). <b>Note:</b> Broad match modifiers now have the same matching behavior as phrase match for some languages, and you haven't been able to create new broad match modifier keywords since July 2021. See [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/7042511) for more information.</p> |
| [!UICONTROL First Page Bid] | (Included in generated bulksheets for information purposes) The bid required to place an ad on the first page of the search results. This value isn't posted to the ad network. |
| [!UICONTROL Quality Score] | (Included in generated bulksheets for information purposes) The current quality score that the search engine has assigned to the keyword. This value isn't posted to the ad network.) |
| [!UICONTROL Creative Preferred Devices] | (Text ads, expanded dynamic search ads, and enhanced sitelinks; optional) The device types on which you prefer to display the ad: <i>[!UICONTROL All]</i> (the default) or <i>[!UICONTROL Mobile]</i>. When <i>[!UICONTROL Mobile]</i> is specified, the network tries to display the ad to mobile device users rather than desktop or tablet users. Otherwise, the network displays the ad on any device type.</p><p><b>Note:</b></p><ul><li><p>Only administrator and [!DNL Adobe] account manager users can edit this setting.</p></li><li><p>The network doesn't guarantee that it will display the ad on the preferred device type.</p></li><li><p>New enhanced sitelinks can be created only in campaigns with existing enhanced sitelinks or no sitelinks.</p></li></ul> |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | (Expanded text ads and responsive search ads only) The headlines of an ad, each separated by a vertical pipe (&vert;). The maximum length for each ad title field is 30 characters or 15 double-byte characters, including any dynamic text (such as the values of keywords and ad customizers).</p><p>For responsive search ads, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2], and [!UICONTROL Ad Title 3] are required, and all other ad title fields are optional. To delete the existing value for a non-required field, use the value <code>[delete]</code> (including the brackets).</p><p>For responsive search ads, insert an ad customizer using the following format: <code>{CUSTOMIZER.AdCustomizerName:DefaultText}</code>, such as <code>{CUSTOMIZER.Discount:10%}</code></p><p>You can't create or edit, but you can delete, expanded text ads, which [!DNL Google Ads] deprecated in June 2022. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>(Responsive search ads only; optional) A position at which to pin the corresponding ad title: `[null]` (no value, which makes the ad title eligible for all positions), <i>1</i>, <i>2</i>, or <i>3</i>. For example, if [!UICONTROL Ad Title Position] has a value of 1, then Ad Title appears only in Position 1. By default, all ad titles are null (have no values).</p><p>To delete the existing value, use the value <code>[delete]</code> (including the brackets).</p><p><b>Note:</b> You can pin multiple ad titles to the same position. The ad network uses one of the ad titles pinned to the position. Titles pinned to position 3 may not be shown with the ad.</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>(Expanded dynamic search ads, expanded text ads, and responsive search ads only) The body of an ad. The maximum length for each description field is 90 characters or 45 double-byte characters, including any dynamic text (such as the values of keywords and ad customizers).</p><p>For responsive search ads, insert an ad customizer using the following format: `{CUSTOMIZER.AdCustomizerName:DefaultText}`, such as `{CUSTOMIZER.Discount:10%}`</p><p>For expanded dynamic search ads, use [!UICONTROL Description Line 1] and [!UICONTROL Description Line 2] only. <b>Note:</b> For this ad type, changing ad copy deletes the existing ad and creates a new one.</p><p>You can't create or edit, but you can delete, expanded text ads, which [!DNL Google Ads] deprecated in June 2022.</p><p>For responsive search ads, [!UICONTROL Description Line 1] and [!UICONTROL Description Line 2] are required, and [!UICONTROL Description Line 3] and [!UICONTROL Description Line 4] are optional. To delete the existing value, use the value <code>[delete]</code> (including the brackets).</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Responsive search ads only; optional) A position at which to pin the corresponding description: `[null]` (no value, which makes the description eligible for all positions), <i>1</i>, <i>2</i>, or <i>3</i>. For example, if [!UICONTROL Description 1 Position] has a value of 1, then [!UICONTROL Description 1] appears only in Position 1. By default, no descriptions are pinned to a position.</p><p>To delete the existing value, use the value `[delete]` (including the brackets).</p><p><b>Note:</b> You can pin multiple descriptions to the same position. The ad network uses one of the descriptions pinned to the position. Descriptions pinned to position 2 may not be shown with the ad. |
| [!UICONTROL Display URL] | The URL that's included in the ad.<br><br>For expanded dynamic search ads, [!DNL Google Ads] generates this value dynamically from the website domain, and you don't need to enter a value.<br><br>For responsive search ads, you don't need to enter a value. The display URL is automatically extracted from the domain in the final URL. You optionally can customize the URL using the Path 1 and Path 2 fields.<br><br>You can't create or edit, but you can delete, expanded text ads, which [!DNL Google Ads] deprecated in June 2022.<br><br><b>Note:</b> (Accounts with final URLs) The domain names in the display URL and final URL must match.</p> |
| [!UICONTROL Display Path 1] | <p>(Expanded text ads<span> and responsive search ads</span> only)</p><p>(Optional) Text that is added to the display URL that is automatically extracted from the final URL. It's preceded in the URL by a forward slash (/). A path can't contain forward slash (/) or newline (\n) characters. The maximum length is 15 characters or 7 double-byte characters.</p><p>To insert an ad customizer, use the following formats, where `Default text` is an optional value to insert when your feed file doesn't include a valid value:< `{CUSTOMIZER.AdCustomizerName:Default text}`, such as `{CUSTOMIZER.Discount:10%}`</p><p>For example, if [!UICONTROL Display Path 1] is &quot;deals,&quot; then the display URL is &lt;<i>display URL</i>&gt;/deals, such as www.example.com/deals.</p><p>You can't create or edit, but you can delete, expanded text ads, which [!DNL Google Ads] deprecated in June 2022.</p> |
| [!UICONTROL Display Path 2] | A second display path; see the entry for [!UICONTROL Display Path 1].<br><br>Example: If [!UICONTROL Display Path 1] is &quot;deals&quot; and [!UICONTROL Display Path 2] is &quot;local,&quot; then the display URL is &lt;<i>display URL</i>&gt;/deals/local, such as www.example.com/deals/local.</p><p>You can't create or edit, but you can delete, expanded text ads, which [!DNL Google Ads] deprecated in June 2022.</p> |
| [!UICONTROL Promotion Line] | (Product listing ads only) An optional promotion line to be included with the product listing in search results. The maximum length is 45 characters.</p><p>The promotion line may appear in different locations relative to the ad (such as below the ad) depending on where the ad appears on the page. |
| [!UICONTROL Link Name] | <p>The sitelink text. It can include up to 25 characters.</p><p>For new sitelinks, you must include the campaign name within the sitelink row. For ad group-level sitelinks, you must also include the ad group name.</p><p><b>Note:</b> Existing text of 35 characters are still displayed in ads on desktops and tablets but not on mobile devices.</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | (Existing app install ads only) The operating system on which the mobile application runs: <i>Android&trade;</i> or <i>ios</i>. |
| [!UICONTROL Mobile App ID (Google Adwords)] | (Existing app install ads only) <p>The application ID or package name. |
| [!UICONTROL Mobile App Name (Google Adwords)] | (Existing app install ads only) The name of the application. |
| [!UICONTROL Start Date] | <p>(Enhanced sitelinks only) The first date on which bids may be placed for the sitelink, in the advertiser's time zone and in one of the following formats: <i>m/d/yyyy</i>, <i>m/d/yy</i>, <i>m-d-yyyy</i>, or <i>m-d-yy</i>. The default for new enhanced sitelinks is the current day.</p><p><b>Note:</b> New enhanced sitelinks can be created only in campaigns with existing enhanced sitelinks or no sitelinks.</p> |
| [!UICONTROL End Date] | <p>(Enhanced sitelinks only) The last date on which bids may be placed for the sitelink, in the advertiser's time zone and in one of the following formats: &#160;<i>m/d/yyyy</i>, <i>m/d/yy</i>, <i>m-d-yyyy</i>, or <i>m-d-yy</i>. The default is none (no end date).</p><p><b>Note:</b> New enhanced sitelinks can be created only in campaigns with existing enhanced sitelinks or no sitelinks.</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | (Existing app install ads only)</p><p>(Optional) Prevents [!DNL Google Ads] from displaying the ad to tablet users. Values can include <i>yes</i> and <i>no</i>. |
| [!UICONTROL Landing Page Suffix] | Any parameters to append to the end of final URLs to track information. Example: `param2=value1&param3=value2`<br><br>See "[Click-tracking formats for [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)."<br><br>Final URL suffixes at lower levels override the account-level suffix. For easier maintenance, use only the account-level suffix unless different tracking for individual account components is necessary. To configure a suffix at the ad group level or lower, use the [!DNL Google Ads] editor. |
| [!UICONTROL Tracking Template] | The tracking template, which specifies all off-landing domain redirects and tracking parameters and embeds the final URL in a [!DNL ValueTrack] parameter. The tracking template at the most granular level (with keyword as the most granular) overrides the values at all higher levels.<br><br>For Adobe Advertising conversion tracking, which is applied when the campaign settings include "[!UICONTROL EF Redirect]" and "[!UICONTROL Auto Upload]," Search, Social, & Commerce automatically appends its own redirect and tracking code when you save the record.<br><br>For third-party redirects and tracking, enter a value. For a list of [!DNL ValueTrack] parameters to indicate final URLs in tracking templates, see the &quot;Tracking template only&quot; parameters in the section on &quot;Available [!DNL ValueTrack] Parameters&quot; in the [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/2375447).<br><br>To delete the existing value, use the value `[delete]` (including the brackets). |
| [!UICONTROL Base URL/Final URL] | The landing page URL to which search engine users are taken when they click your ad, including any append parameters configured for the campaign or account. Base/final URLs at the keyword level override those at the ad level and higher.<br><br>To delete the existing value, use the value `[delete]` (including the brackets). |
| [!UICONTROL Destination URL] | (Included in generated bulksheets for information purposes; not posted to the search engine) For accounts with destination URLs, this is the URL that links an ad to a base URL/landing page on the advertiser's website (sometimes via another site that tracks the click and then redirects the user to the landing page). It includes any append parameters configured for the Search, Social, & Commerce campaign or account. If you generated tracking URLs, this is based on the tracking parameters in your account settings and campaign settings. If you appended search engine-specific parameters, they may be replaced with the equivalent parameters for Search, Social, & Commerce.<br><br>For accounts with final URLs, this column shows the same value as the Base URL/Final URL column. |
| [!UICONTROL Custom URL Param] | Data to substitute for the `{custom_code}` dynamic variable when the variable is included in the tracking parameters for the search account or campaign settings. To insert the custom value in the tracking URL, you must upload the bulksheet file using the Generate Tracking URLs option. |
| [!UICONTROL Creative Type] | The ad format: <i>[!UICONTROL Text ad]</i>, <i>[!UICONTROL Expanded text ad]</i>, <i>[!UICONTROL Dynamic search ad]</i> (deprecated ad type), <i>[!UICONTROL Expanded Dynamic Search ad]</i>, <[!UICONTROL i>Display ad]</i>, <i>[!UICONTROL App Install ad]</i> (deprecated), <i>[!UICONTROL Image]</i>, <i>[!UICONTROL Product ad<]/i> (shopping ads), or <i>[!UICONTROL Responsive search ad]</i>. The default for new ads is <i>[!UICONTROL Text ad]</i>.<br><br>Required to create or edit the status of a product ad. |
| [!UICONTROL Param1] | <p>The numeric value of the `{param1}` ad parameter, which can be included in the ad copy or display URL for any ad in the bulksheet file. The maximum length is 25 characters, and you may include the following nun-numeric characters:</p><ul><li><p>The value can be preceded or appended with a currency symbol or code. For example, `£2.000,00` and `2000GBP` are valid.</p></li><li><p>The value can include a comma (`,`) or period (`.`) as a separator, with an optional period (`.`) or comma (`,`) for fractional values. For example, `1,000.00` and `2.000,10` are valid.</p></li><li><p>The value can be prefixed or appended with a percent sign (`%`), plus sign (`+`), or minus sign (`- `). For example, `20%`, `208+`, and `-42.32` are valid.</p></li><li><p>Two numbers can be embedded with a forward slash. For example, `4/1` and `0.95/0.45` are valid.</p></li></ul><p>To delete the existing value, use the value `[delete]` (including the brackets).</p> |
| [!UICONTROL Param2] | The numeric value of the `{param2}` ad parameter, which can be included in the ad copy or display URL for any ad in the bulksheet file. See the entry for Param1 for more information.|
| [!UICONTROL Audience] | The remarketing list for search ads (RLSA) target audience or excluded audience for the campaign or ad group. Specify whether it's a target or exclusion in the &quot;Target Type&quot; field. |
| [!UICONTROL Target Type] | (When an Audience is specified) Whether the specified audience is an <i>Inclusion</i> (target) or <i>Exclusion</i>. |
| [!UICONTROL Campaign Status] | The display status of the campaign: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i> (not editable), or <i>[!UICONTROL Deleted]</i> (existing campaigns only). The default for new campaigns is <i>[!UICONTROL Active]</i>. To delete an active or paused campaign, enter the value <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | The display status of the ad group: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, or <i>[!UICONTROL Deleted]</i> (existing ad groups only). The default for new ad groups is [!UICONTROL Active]. To delete an active or paused ad group, enter the value `Deleted`. |
| [!UICONTROL Keyword Status] | The display status of the keyword: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, or <i>[!UICONTROL Deleted]</i> (existing keywords only). The default for new keywords is [!UICONTROL Active]. To delete an active or paused keyword, enter the value <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | The display status of the ad: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (existing ads only), <i>[!UICONTROL Disapproved]</i> (not editable), or <i>[!UICONTROL Paused]</i>. The default for new ads is [!UICONTROL Active]. To delete an active or paused ad, enter the value <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Placement Status] | The status of the website placement: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, or <i>[!UICONTROL Deleted]</i> (existing ads only). The default for new websites is <i>Active.</i> To delete an active or paused placement, enter the value <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Target Status] | The status of a dynamic search target: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, or <i>[!UICONTROL Deleted]</i> (existing targets only). The default for new targets is <i>Active.</i> To delete an active or paused target, enter the value <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Product Group Status] | The display status of the product group: <i>[!UICONTROL Active]</i> <span>or</span> <i>[!UICONTROL Deleted]</i> (existing product groups only). The default for new product groups is <i>[!UICONTROL Active]</i>. To delete an active product group, enter the value <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Sitelink Status] | The display status of the sitelink: <i>Active or Deleted</i> (existing sitelinks only). The default for new sitelinks is <i>[!UICONTROL Active]</i>. To delete an active sitelink, enter the value <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Location Status] | The status of the location target: <i>[!UICONTROL Active]</i> or <i>[!UICONTROL Deleted]</i> (existing locations only). The default for new locations is [!UICONTROL Active]. To delete an active location, enter the value <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL RLSA Target Status] | The status of the campaign- or ad group-level RLSA target or exclusion: <i>[!UICONTROL Active]</i> or [!UICONTROL Deleted]</i> (existing targets only). The default for new targets or exclusions is <i>[!UICONTROL Active]</i>. To delete an active target or exclusion, enter the value <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Device Target Status] | <p>The status of the campaign- or ad group-level device target: <i>[!UICONTROL Active]</i> or <i>[!UICONTROL Deleted]</i>. For new campaigns and ad groups, the default is <i>[!UICONTROL Active]</i>.</p> |
| \[Advertiser-specific Label Classification\] | (Named for an advertiser-specific label classification, such as &quot;Color&quot; for a label classification called Color) A value for the specified classification that is associated with the entity. You can include only one value per classification per entity (such as &quot;red&quot; for the &quot;Color&quot; label classification for Campaign A). The maximum length is 100 characters, and the value can include ASCII and non-ASCII characters.<br><br>Label classifications and their label values are applied to all child components; new components that are added later are automatically associated with the label. Label classifications for product groups are applied to the unit (most granular) level.<br><br>Neither the classification name nor the classification value is case-sensitive. |
| [!UICONTROL Constraints] | A constraint that's assigned to the entity. You can assign only one constraint per entity.<br><b>>Constraints are inherited by child entities, so you don't need to enter values for child entities unless you want to override the inherited values. |
| [!UICONTROL Campaign ID] | The unique ID that identifies an existing campaign. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change the campaign name, unless the row includes an &quot;[!UICONTROL AMO ID]&quot; for the campaign. |
| [!UICONTROL Ad Group ID] | The unique ID that identifies an existing ad group. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change the campaign name, unless the row includes an &quot;[!UICONTROL AMO ID]&quot; for the ad group. |
| [!UICONTROL Keyword ID] | The unique ID that identifies an existing keyword. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change the keyword, unless the row includes a) sufficient property columns to identify the keyword or b) an &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>The unique ID that identifies an existing ad. In CSV and TSV files, it must be preceded by a single quote (').[^1] For responsive search ads, either the Ad ID or AMO ID is required to edit or delete ad data. For all other entity types, the Ad ID is required only when you change the ad status, unless the row includes a) sufficient ad property columns to identify the ad or b) an &quot;[!UICONTROL AMO ID]&quot;.&quot; However, if you include neither the [!UICONTROL Ad ID] nor [!UICONTROL AMO ID], and the ad property columns match multiple ads, then the status for only one of the ads changes.</p><p><b>Note:</b> If you edit a) ad property columns except Status for an existing ad or b) any data for a responsive search ad, and you include neither the [!UICONTROL Ad ID] nor [!UICONTROL AMO ID], then a new ad is created, and the existing ad isn't changed.</p> |
| [!UICONTROL Placement ID] | The unique ID that identifies a website placement. Required only when you change or delete the placement, unless the row includes a) sufficient property columns to identify the placement or b) an &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Target ID] | The unique ID that identifies an existing auto target. Required only when you change or delete the auto target, unless the row includes an &quot;[!UICONTROL AMO ID]&quot; for the target. |
| [!UICONTROL Product Group ID] | The unique ID that identifies an existing product group. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change or delete the product group, unless the row includes a) sufficient property columns to identify the product group or b) an &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Sitelink ID] | The unique ID that identifies an existing sitelink. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change or delete the sitelink, unless the row includes a) sufficient property columns to identify the sitelink or b) an &quot;[!UICONTROL AMO ID]&quot;.&quot; However, if you include neither [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID], and the property columns match multiple sitelinks, then the status for only one of the sitelinks changes.</p><p><b>Note:</b> If you edit sitelink property columns except Status for an existing sitelink, and you include neither the [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID], then a new sitelink is created, and the existing sitelink isn't changed. |
| [!UICONTROL RLSA Target ID] | The unique ID that identifies an existing campaign- or ad group-level RLSA target or exclusion. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change or delete the target or exclusion, unless the row includes an &quot;[!UICONTROL AMO ID]&quot; for the target. |
| [!UICONTROL Device Target ID] | <p>The unique ID that identifies an existing campaign-level or ad group-level device target or exclusion. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change or delete the target, unless the row includes an &quot;[!UICONTROL AMO ID]&quot; for the target.</p> |
| [!UICONTROL AMO ID] | (In generated bulksheets) An Adobe-generated unique identifier for a synced entity. For responsive search ads, the AMO ID is required to edit or delete ads unless you include the Ad ID. To edit data for all other entity types with an AMO ID, the AMO ID is required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |
| [!UICONTROL EF Error Message] | (Included in generated bulksheets for information purposes) Placeholder for displaying error messages from the ad network regarding data in the row; error messages are included in [!UICONTROL EF Errors] files. This value isn't posted to the ad network. |
| [!UICONTROL SE Error Message] | (Included in generated bulksheets for information purposes) Placeholder for displaying error messages from the ad network regarding data in the row; error messages are included in [!UICONTROL SE Errors] files. This value isn't posted to the ad network. |
| [!UICONTROL Exemption Request] | (Included in generated bulksheets for information purposes) Placeholder for displaying the names and text of any [!DNL Google Ads] advertising policies that an ad violates. |
| [!UICONTROL Retail Hash] | (Included for information purposes in bulksheets generated using Advanced Campaign Management) An alphanumeric hash code (such as f9639f40cdf56524b541e5dacf55a991) that indicates the item was generated using the Advanced (ACM) view. |

[^1]: [!DNL Excel] converts large numbers to scientific notation (such as 2.12E+09 for 2115585666) when it opens the file. To view digits in the standard notation, select any cell in the column and click inside the formula bar.

## Fields required to create, edit, or delete each account component {#bulksheet-fields-per-component-google}

The following sections include the fields relevant to specific account entities.

>[!NOTE]
>
>When a field isn't applicable to an action, any value entered in the field is ignored.

### Campaign fields

For a description of each data field, see "[All available data fields](#bulksheet-fields-all-google)."

| Field | Required? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | Required |
| [!UICONTROL Campaign Budget] | Required to create a campaign. |
| [!UICONTROL Delivery Method] | Required to create a campaign. |
| [!UICONTROL Channel Type] | Required to create a campaign. |
| [!UICONTROL Networks] | Required to create a campaign. |
| [!UICONTROL DSA Domain Name] | Required to create a campaign with dynamic search ads on the search network. |
| [!UICONTROL DSA Domain Language] | Required to create a campaign with dynamic search ads on the search network. |
| [!UICONTROL Campaign Priority] | Required to create a shopping campaign. |
| [!UICONTROL Merchant ID] | Required to create a shopping campaign. |
| [!UICONTROL Sales Country] | Required to create a shopping campaign. |
| [!UICONTROL Product Scope Filter] | (Shopping campaigns) Optional |
| [!UICONTROL Languages] | Optional |
| [!UICONTROL Device Targets] | Optional |
| [!UICONTROL Device Targets (Google Adwords)] | Optional |
| [!UICONTROL Mobile Carriers (Google Adwords)] | Optional |
| [!UICONTROL Audience Target Method] | n/a |
| [!UICONTROL Landing Page Suffix] | Optional |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Campaign Status] | Required only to delete a campaign. |
| \[Advertiser-specific Label Classification\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Required only when you change the campaign name, unless the row includes an &quot;[!UICONTROL AMO ID]&quot; for the campaign. |
| [!UICONTROL AMO ID] | Required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |

### Ad group fields

For a description of each data field, see "[All available data fields](#bulksheet-fields-all-google)."

| Field | Required? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | Required |
| [!UICONTROL Networks] | n/a |
| [!UICONTROL GDN Custom Bid Level] | Optional |
| [!UICONTROL Ad Group Name] | Required  |
| [!UICONTROL Ad Group Type] | Required to create an ad group. |
| [!UICONTROL Max CPC] | Optional |
| [!UICONTROL Max Content CPC] | Optional |
| [!UICONTROL Audience Target Method] | Required |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Ad Group Status] | Required only to delete an ad group. |
| \[Advertiser-specific Label Classification\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Ad Group ID] | Required only when you change the ad group name, unless the row includes an &quot;[!UICONTROL AMO ID]&quot; for the ad group. |
| [!UICONTROL AMO ID] | Required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |

### Keyword fields

For a description of each data field, see "[All available data fields](#bulksheet-fields-all-google)."

| Field | Required? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | Required |
| [!UICONTROL Ad Group Name] | Required  |
| [!UICONTROL Max CPC] | Optional |
| [!UICONTROL Keyword] | Required |
| [!UICONTROL Match Type] | A value for either the match type or keyword ID is required to edit or delete a keyword with multiple match types. |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Base URL/Final URL] | Optional |
| [!UICONTROL Custom URL Param] | Optional |
| [!UICONTROL Param1] | Optional |
| [!UICONTROL Param2] | Optional |
| [!UICONTROL Keyword Status] | Required only to delete a keyword. |
| \[Advertiser-specific Label Classification\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Keyword ID] | Required only when you edit or delete the keyword, unless the row includes a&#41; sufficient property columns to identify the keyword or b&#41; an "[!UICONTROL AMO ID]." |
| [!UICONTROL AMO ID] | Required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |

### Placement fields

For a description of each data field, see "[All available data fields](#bulksheet-fields-all-google)."

| Field | Required? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | Required |
| [!UICONTROL Ad Group Name] | Required  |
| [!UICONTROL Max Placement CPC (Google Adwords)] | Optional |
| [!UICONTROL Max Placement CPM (Google Adwords)] | Optional |
| [!UICONTROL Placement] | Required |
| [!UICONTROL Match Type] | Required |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Base URL/Final URL] | Optional |
| [!UICONTROL Custom URL Param] | Optional |
| [!UICONTROL Placement Status] | Required only to delete a placement. |
| \[Advertiser-specific Label Classification\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Placement ID] | Required only when you edit or delete the placement, unless the row includes a&#41; sufficient property columns to identify the placement or b&#41; an "[!UICONTROL AMO ID]." |
| [!UICONTROL AMO ID] | Required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |

### Expanded dynamic search ad

This ad type is now called "dynamic search ad" in [!DNL Google Ads]. For more information about creating dynamic search ads, see "[Implement [!DNL Google Ads] dynamic search ads](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-dynamic-search-ads.html)."

For this ad type, use the "[!UICONTROL Creative (except RSA)]" row in the [!UICONTROL Download Bulksheet] dialog.

For a description of each data field, see "[All available data fields](#bulksheet-fields-all-google)."

| Field | Required? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | Required |
| [!UICONTROL Ad Group Name] | Required  |
| [!UICONTROL Creative Preferred Devices] | Optional |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Required to create an ad or edit the description. <b>Note:</b> For this ad type, changing ad copy deletes the existing ad and creates a new one. |
| [!UICONTROL Display URL] | Required |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Creative Type] | Required to create or edit the status of a product ad. |
| [!UICONTROL Ad Status] | Required to delete an ad. |
| \[Advertiser-specific Label Classification\] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Ad ID] | Required only when you change the ad status, unless the row includes a) sufficient ad property columns to identify the ad or b) an "[!UICONTROL AMO ID]." However, if you include neither the [!UICONTROL Ad ID] nor [!UICONTROL AMO ID], and the ad property columns match multiple ads, then the status for only one of the ads changes. |
| [!UICONTROL AMO ID] | Required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |

### Product listing/shopping ad fields

For more information about creating shopping ads, see "[Implement [!DNL Google Ads] shopping campaigns](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-shopping-campaigns.html)."

For this ad type, use the "[!UICONTROL Creative (except RSA)]" row in the [!UICONTROL Download Bulksheet] dialog.

For a description of each data field, see "[All available data fields](#bulksheet-fields-all-google)."

| Field | Required? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | Required |
| [!UICONTROL Ad Group Name] | Required  |
| [!UICONTROL Promotion Line] | Optional |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Base URL/Final URL] | Optional |
| [!UICONTROL Custom URL Param] | Optional |
| [!UICONTROL Creative Type] | Required to create or edit the status of a product ad. |
| [!UICONTROL Ad Status] | Required to delete an ad. |
| \[Advertiser-specific Label Classification\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Ad ID] | Required only when you change the ad status, unless the row includes a) sufficient ad property columns to identify the ad or b) an "[!UICONTROL AMO ID]." However, if you include neither the [!UICONTROL Ad ID] nor [!UICONTROL AMO ID], and the ad property columns match multiple ads, then the status for only one of the ads changes. |
| [!UICONTROL AMO ID] | Required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |

### Responsive search ad fields 

For this ad type, use the "[!UICONTROL Responsive Search Ad]" row in the [!UICONTROL Download Bulksheet] dialog.

For a description of each data field, see "[All available data fields](#bulksheet-fields-all-google)."

| Field | Required? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | Required |
| [!UICONTROL Ad Group Name] | Required  | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | For responsive search ads, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2], and [!UICONTROL Ad Title 3] are required to create an ad, and all other ad title fields are optional. To delete the existing value for a non-required field, use the value `[delete]` (including the brackets). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Optional |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | For responsive search ads, [!UICONTROL Description Line 1] and [!UICONTROL Description Line 2] are required to create an ad, and [!UICONTROL Description Line 3] and [!UICONTROL Description Line 4] are optional. To delete the existing value, use the value `[delete]` (including the brackets). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Optional |
| [!UICONTROL Display Path 1] | Optional |
| [!UICONTROL Display Path 2] | Optional |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Base URL/Final URL] | Required to create an ad. |
| [!UICONTROL Custom URL Param] | Optional |
| [!UICONTROL Creative Type] | Optional |
| [!UICONTROL Ad Status] | Required to delete an ad. |
| \[Advertiser-specific Label Classification\] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Ad ID] | Required to edit or delete ads unless the row includes an "[!UICONTROL AMO ID]." |
| [!UICONTROL AMO ID] | Required to edit or delete ads unless you include the Ad ID. | 

### Text ad fields

For this ad type, use the "[!UICONTROL Creative (except RSA)]" row in the [!UICONTROL Download Bulksheet] dialog.

For a description of each data field, see "[All available data fields](#bulksheet-fields-all-google)."

>[!NOTE]
>
>Expanded text ads were deprecated in June 2022. You can only delete existing text ads.

| Field | Required? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | Required |
| [!UICONTROL Ad Group Name] | Required  |
| [!UICONTROL Creative Preferred Devices] | Read-only |
| [!UICONTROL Ad Title], Ad Title 2-3 | Read-only |
[!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Read-only |
| [!UICONTROL Display URL] | Read-only |
| [!UICONTROL Display Path 1] | Read-only |
| [!UICONTROL Display Path 2] | Read-only |
| [!UICONTROL Tracking Template] | Read-only |
| [!UICONTROL Base URL/Final URL] | Read-only |
| [!UICONTROL Custom URL Param] | Read-only |
| [!UICONTROL Creative Type] | Optional |
| [!UICONTROL Ad Status] | Required |
| \[Advertiser-specific Label Classification\] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Ad ID] | Required only when you change the ad status, unless the row includes a) sufficient ad property columns to identify the ad or b) an "[!UICONTROL AMO ID]." However, if you include neither the [!UICONTROL Ad ID] nor [!UICONTROL AMO ID], and the ad property columns match multiple ads, then the status for only one of the ads changes. |
| [!UICONTROL AMO ID] | Required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |

### Dynamic search target (auto target) fields

For a description of each data field, see "[All available data fields](#bulksheet-fields-all-google)."

| Field | Required? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | Required |
| [!UICONTROL Ad Group Name] | Required  |
| [!UICONTROL Max CPC] | Optional |
| [!UICONTROL Auto Target Expression] | Required only when the campaign setting to "[!UICONTROL Use my website contents to target my ads]" isn't enabled. |
| [!UICONTROL Match Type] | Optional |
| [!UICONTROL Target Status] | Required to delete a target |
| \[Advertiser-specific Label Classification\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Target ID] | Required only when you change or delete the auto target, unless the row includes an "[!UICONTROL AMO ID]" for the target. |
| [!UICONTROL AMO ID] | Required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |

### Shopping product group fields

For a description of each data field, see "[All available data fields](#bulksheet-fields-all-google)."

| Field | Required? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | Required |
| [!UICONTROL Ad Group Name] | Required  |
| [!UICONTROL Max CPC] | Required to create a product group. |
| [!UICONTROL Parent Product Groupings] | Required |
| [!UICONTROL Product Grouping] | Required |
| [!UICONTROL Partition Type] | Required to create a product group. |
| [!UICONTROL Match Type] | Optional |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Base URL/Final URL] | Required |
| [!UICONTROL Product Group Status] | Required only to delete a product group. |
| \[Advertiser-specific Label Classification\] | Optional |
| [!UICONTROL Constraints] | Optional |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Product Group ID] | Required only when you change or delete the product group, unless the row includes a) sufficient property columns to identify the product group or b) an "[!UICONTROL AMO ID]." |
| [!UICONTROL AMO ID] | Required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |

### Campaign-level and ad group-level sitelink fields

For a description of each data field, see "[All available data fields](#bulksheet-fields-all-google)."

| Field | Required? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | Required |
| [!UICONTROL Ad Group Name] | Required for ad group-level sitelinks. Not applicable for campaign-level sitelinks. |
| [!UICONTROL Creative Preferred Devices] | Optional |
| [!UICONTROL Link Name] | Required |
| [!UICONTROL Start Date] | Optional |
| [!UICONTROL End Date] | Optional |
| [!UICONTROL Tracking Template] | Optional |
| [!UICONTROL Base URL/Final URL] | Required |
| [!UICONTROL Sitelink Status] | Required only to delete a sitelink. |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional |
| [!UICONTROL Sitelink ID] | Required only when you change or delete the sitelink, unless the row includes a) sufficient property columns to identify the sitelink or b) an "[!UICONTROL AMO ID]." However, if you include neither [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]  and the property columns match multiple sitelinks, then the status for only one of the sitelinks changes.<br><br><b>Note:</b> If you edit sitelink property columns except [!UICONTROL Status] for an existing sitelink, and you don't include either the [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID], then a new sitelink is created, and the existing sitelink isn't changed. |
| [!UICONTROL AMO ID] | Required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |

### Location target 

For a description of each data field, see "[All available data fields](#bulksheet-fields-all-google)."

| Field | Required? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | Required |
| [!UICONTROL Location] | Required |
| [!UICONTROL Location Type] | Optional |
| [!UICONTROL Bid Adjustment] | Optional |
| [!UICONTROL Location Status] | Required only to delete a location target. |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL AMO ID] | Required to edit or delete the data unless you include the [!UICONTROL Campaign ID].<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |

### Campaign-level and ad group-level device target fields

For a description of each data field, see "[All available data fields](#bulksheet-fields-all-google)."

| Field | Required? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | Required |
| [!UICONTROL Device] | Required to create or edit a device target. |
| [!UICONTROL Bid Adjustment] | Optional |
| [!UICONTROL Ad Group Name] | Required for ad group-level device targets. Not applicable for campaign-level device targets. |
| [!UICONTROL Device Target Status] | Required only to delete a device target. |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional; applicable only for ad group-level device targets. |
| [!UICONTROL Device Target ID] | Required only when you change or delete the target, unless the row includes an "[!UICONTROL AMO ID]" for the target. |
| [!UICONTROL AMO ID] | Required to edit or delete the data unless you include the Device Target ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |

### Campaign-level and ad group-level RLSA target/exclusion fields

For a description of each data field, see "[All available data fields](#bulksheet-fields-all-google)."

| Field | Required? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Required unless each row includes an &quot;[!UICONTROL AMO ID]&quot; for the entity. |
| [!UICONTROL Campaign Name] | Required |
| [!UICONTROL Bid Adjustment] | Optional |
| [!UICONTROL Ad Group Name] | Required for ad group-level targets and exclusions. Not applicable for campaign-level targets and exclusions. |
| [!UICONTROL Audience] | Required to create a new target or exclusion. |
| [!UICONTROL Target Type] | Required to create a new target or exclusion. |
| [!UICONTROL RLSA Target Status] | Required only to delete a target or exclusion. |
| [!UICONTROL Campaign ID] | Optional |
| [!UICONTROL Ad Group ID] | Optional; applicable only for ad group-level targets and exclusions. |
| [!UICONTROL RLSA Target ID] | Required only when you change or delete the target, unless the row includes an "[!UICONTROL AMO ID]" for the target. |
| [!UICONTROL AMO ID] | Required to edit or delete the data unless you include the RLSA Target ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |

>[!MORELIKETHIS]
>
>* [Appendix - Bulksheet errors](../bulksheet-errors.md)
>* [Operations you can perform in bulksheets](bulksheet-operations.md)
>* [Supported bulksheet file formats](bulksheet-file-formats.md)
>* [Download/Create a bulksheet file](../bulksheet-download.md)
>* [Click-tracking formats for [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Upload a bulksheet file or corrected error file](../bulksheet-upload.md)
