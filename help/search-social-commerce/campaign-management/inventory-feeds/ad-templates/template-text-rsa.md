---
title: Text ad and responsive search ad template settings for inventory feeds
description: Reference the settings for text ad and responsive search ad templates for inventory feeds.
---
# Text ad and responsive search ad template settings for inventory feeds


*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (delete actions only), and [!DNL Yandex] accounts only*

>[!NOTE]
>
>* The following characters are reserved for designating column names and modifier names in the template, and are therefore prohibited as text in all attribute fields:  `[ ] < > `
>* In [!DNL Yandex templates], you can use the dynamic parameters `{param1}` and `{param2}` only in URLs, and you can't use dynamic price insertion in ad descriptions.

## \[Above all tabs\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[Left panel\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

**[!UICONTROL Map Only]:** (Optional) Maps all new ad groups (not available for [!DNL Yandex]), keywords, and ads to existing campaigns, rather than creating campaigns. If you enable this option, select the mapping method.

Using [!UICONTROL Map Only] at the campaign level requires an existing account structure  that's closely tied to the product taxonomy and easily maps to the data feed.

**[!UICONTROL Map Method]:** (When [!UICONTROL Map Only] is enabled for the campaign) The method by which new ad groups (not available for [!DNL Yandex]), keywords, and ads are mapped to existing campaigns:

* *[!UICONTROL Contains Anywhere]:* Adds data to an existing campaign whose name includes the specified string, if it exists.

* *[!UICONTROL Contains Exactly]:* Adds data to an existing campaign whose name includes the specified string, if it exists.

* *[!UICONTROL Exactly Matches]* (the default): Adds data to an existing campaign with the same name, if it exists.

When no match is found, all data for the campaign is ignored. If multiple campaign matches are found, then the keywords and ads are mapped to all of them.

**[!UICONTROL Campaign Tracking Template]:** (Accounts with final/advanced URLs only; optional) The campaign-level tracking template, which specifies all off-landing domain redirects and tracking parameters and embeds the final URL in a parameter. This value overrides the account-level setting, but tracking templates at more granular levels (with keyword as the most granular) override this value.

* For Adobe Advertising conversion tracking, which is applied when the campaign settings include &quot;[!UICONTROL EF Redirect]&quot; and &quot;[!UICONTROL Auto Upload],&quot; Search, Social, & Commerce automatically appends redirect and tracking code when you save the record.

* To embed the final URL:

  * ([!DNL Google Ads] and [!DNL Microsoft® Advertising] only) For a list of parameters to indicate final URLs in tracking templates, see the ([!DNL Microsoft® Advertising] only) [[!DNL Microsoft® Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799/2) or ([!DNL Google Ads] only) the "Tracking template only" parameters in the section on "Available [!DNL ValueTrack] Parameters" in the [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

  * ([!DNL Yahoo! Japan Ads] only) Use the parameter `!{unescapedurl}` to indicate the landing page URL.

  * You can optionally include URL parameters and any custom parameters defined for the campaign, separated by ampersands (&), such as `{lpurl}?matchtype={matchtype}&device={device}`.

* For third-party redirects and tracking, enter a value.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]:** (In [!DNL Google Ads] and [!DNL Yandex] campaign settings) The networks on which to place ads:

* *[!UICONTROL Search]:* To place bids for sponsored search listings.

  ([!DNL Google Ads] campaigns) To include bids on listings for [!DNL Google Ads] search partners, select the check box next to **[!UICONTROL Search partners]**.

* *[!UICONTROL Content]:* To place bids for placements on content (display) network listings. **Note:** You can't create placements using the template. When you select this option, create placements for each ad group and specify which pages on the display network to target for each ad group using either <!-- insert link --> bulksheets or the <!-- insert links --> ad group and placement settings in the [!UICONTROL Search] &gt; [!UICONTROL Campaigns] views.

**[!UICONTROL Languages]:** ([!DNL Google Ads] search and display networks only) One or more target languages for ads in the campaign.

[!DNL Google Ads] determines a user's language from the user's [!DNL Google] language setting or the language of the search query, the current page, or recently viewed pages on the [!DNL Google Display Network].

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Accounts with final/advanced URLs only) The ad group-level tracking template, which specifies all off-landing domain redirects and tracking parameters and embeds the final URL in a parameter.

For Adobe Advertising conversion tracking, which is applied when the campaign settings include "[!UICONTROL EF Redirect]" and "[!UICONTROL Auto Upload]," Search, Social, & Commerce automatically appends redirect and tracking code when you save the record.

For third-party redirects and tracking, enter a value. To indicate the landing page URL:

* For Yahoo! Japan Ads accounts, use the parameter {lpurl}.

* For parameters available for Microsoft® Advertising and Google Ads accounts, see the [[!DNL Microsoft® Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) or the &quot;Tracking template only&quot;parameters in the section on &quot;Available [!DNL ValueTrack] Parameters&quot; in the [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

This value overrides the account- and campaign-level settings, but tracking templates at more granular levels (with keyword as the most granular) override this value.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]:** Keywords for the specified ad group (or campaign for [!DNL Yandex] accounts), which can consist of any combination of static text, columns in the specified file, and modifiers. Column names and modifiers are substituted with actual data when the specified feed file is propagated through the template.

To insert a column name or modifier group as a dynamic parameter, click in the input field, and then click a column name in the column list or a [modifier name](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) in the Modifiers list. To specify multiple keywords or multiple match types for the same keyword, enter them on separate lines. To specify the keyword match type, use the following match type syntax around the column name:

* For [!DNL Google Ads], [!DNL Microsoft® Advertising], and [!DNL Yahoo! Japan Ads] templates:

  * For dynamic parameters: Broad Match = `[keyword]`, Broad Match Modifier for the first term in the [!UICONTROL Keyword] column (such as +blue suede shoes) = `+[keyword]`, Broad Match Modifier for each term in the Keyword column (such as +blue +suede +shoes) = `+[keyword]+`, Phrase Match = `"[keyword]"`, Exact Match = `[[keyword]]`

  * For static keywords: Broad Match = `keyword`, Broad Match Modifier = `+keyword`, or Phrase Match = `"keyword"`
  
    You can't enter static keywords with exact match and standard match syntax here because they're surrounded by brackets (`[]`), like dynamic parameters are.

* For [!DNL Yandex] templates:

  * For dynamic parameters: Insert the column name, such as `[keyword]`. To indicate match type, use the [[!DNL Yandex]-specific syntax](https://yandex.com/support/direct/keywords/symbols-and-operators.html). **Note:** For broad match terms, use the following syntax: Broad Match Modifier for the first term in the Keyword column (such as +blue suede shoes) = `+[keyword]`, Broad Match Modifier for each term in the Keyword column (such as +blue +suede +shoes) = `+[keyword]+`
  
  * For static keywords: Only search keywords are supported. Use the [[!DNL Yandex]-specific syntax](https://yandex.com/support/direct/keywords/symbols-and-operators.html) for the keyword. Brackets (`[]`) to indicate word order aren't supported.

>[!NOTE]
>
>* You can manually include multiple modifier values in the Keywords field by enclosing comma-separated values within parentheses either before or after a keyword parameter (but not in both places). For example, `(cheap, discount, affordable)[product]` produces three separate ads for each product.
>* If you don't specify a match type, then the default match type &quot;broad&quot; is used.
>* Negative matches aren't supported.
>* Google broad match modifiers now have the same matching behavior as phrase match for some languages, and you can't create new broad match modifier keywords. See the [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/10286719) for more information.

**[!UICONTROL Map Only]:** Adds any new ads to ad groups (or to campaigns for [!DNL Yandex] accounts) in which the specified keywords are found, rather than creating new keywords. To enable this option, select the check box. When this option is enabled, any Param 1 and Param 2 variables in the specified keywords don't apply because the keywords exist.

**[!UICONTROL Keyword Final URL]:** (Accounts with final/advanced URLs; optional) The landing page URL to which ad network users are taken when they click your ad. It must include the same domain as the display URL, and any parameters in the final URL must match the parameters in the landing page URL after the ad click. It may contain redirects within the landing page domain or subdomain but no redirects outside the landing page domain.

If you use a [!DNL Google Merchant Center] feed and include this value in the &quot;[!DNL Link]&quot; column, then insert that column in this field.

>[!NOTE]
>
>* If you generate tracking URLs when you post data propagated through the template, tracking parameters are appended to this value based on the account tracking settings.
>* ([!DNL Google Ads] accounts) Avoid using macros, which aren't substituted for clicks from sources that enable parallel tracking. If the advertiser must use macros, then the Adobe Account Team should work with Customer Support or the implementation team to add them.

**[!UICONTROL Keyword Tracking Template]:** (Accounts with final/advanced URLs; optional) The tracking template, which specifies all off-landing domain redirects and tracking parameters and embeds the final URL in a parameter. The tracking template at the most granular level (with keyword as the most granular) override values at all other levels.

* For Adobe Advertising conversion tracking, which is applied when the campaign settings include "[!UICONTROL EF Redirect]" and "[!UICONTROL Auto Upload]," Search, Social, & Commerce automatically appends redirect and tracking code when you save the record.

* You can optionally enter third-party redirects and tracking.

* To indicate the landing page URL:

  * ([!DNL Google Ads] and [!DNL Microsoft® Advertising] only) For a list of parameters to indicate final URLs in tracking templates, see the ([!DNL Microsoft® Advertising] only) [[!DNL Microsoft® Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) or ([!DNL Google Ads] only) the "Tracking template only" parameters in the section on "Available [!DNL ValueTrack] Parameters" in the [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).
  
  * ([!DNL Yahoo! Japan Ads] only) Use the parameter `!{lpurl}` to indicate the landing page URL.

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2] \[[!DNL Google Ads] templates\]:** ([!DNL Google Ads] templates only) The column in the specified file that represents the [!DNL Google Ads] `{param1}` or `{param2}` variable, which you can include in the ad copy or display URL for any ad created from the template. To insert the dynamic parameter, click in the input field, and then click a column name in the column list. The column name is substituted with the actual data when the feed file is propagated through the template.

If you use either parameter, you have an option to only apply the parameter to new keywords or to also update the values of existing keywords that weren't created from the template:

* **[!UICONTROL Do Not Apply to Existing Keywords]** (the default): Simply inserts the value of the parameter for new keywords that are created using the template.
  
* **[!UICONTROL Apply to Existing Keywords: Constant]:** In addition to creating new keywords from the feed, Search, Social, & Commerce also updates the value of the parameter for all existing keywords in the ad group that weren't created using the template. Enter a single numeric value that is used for all of those keywords. The template must contain at least one keyword.
  
* **[!UICONTROL Apply to Existing Keywords: Min]:** In addition to creating new keywords from the feed, Search, Social, & Commerce also updates the value of the parameter for all existing keywords in the ad group that weren't created using the template as long as the feed file contains numeric values for the parameter, with up to one decimal point but without commas, currency symbols or codes, or any other characters. The minimum value for the parameter in the feed file is used for all existing keywords. For example, if the feed file has [!UICONTROL Param1] values of 21500 and 22000, then the [!UICONTROL Param1] values for the existing keywords are changed to 21500. The template must contain at least one keyword. **Tip:** Use this option only when you have tightly themed ad groups so that it makes sense for keywords to have the same value.

The data fields in the feed file may have a maximum of 25 characters and may consist of only numeric data with the following non-numeric characters:

* (When you use the &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot; parameter) Up to one decimal point only.
  
* (When you don't use the &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot; parameter):
  
  * The value can be preceded or appended with a currency symbol or code. For example, £2.000,00 and 2000GBP are valid.

  * The value can include a comma (,) or period (.) as a separator, with an optional period (.) or comma (,) for fractional values. For example, 1,000.00 and 2.000,10 are valid.

  * The value can be prefixed or appended with a percent sign (%), plus sign (+), or minus sign (-). For example, 20%, 208+, and -42.32 are valid.

  * Two numbers can be embedded with a forward slash. For example, 4/1 and 0.95/0.45 are valid.

**[!UICONTROL Param 2] \[[!DNL Microsoft® Advertising] templates\]:** ([!DNL Microsoft® Advertising] templates only) The string to use as the substitution value in an ad if the title, text, display URL, or final URL contains the `{Param2}` dynamic substitution string. The maximum length is 70 characters, but be aware of the maximum length of the ad element in which you use it (for example, an ad title may include up to 25 characters).

**[!UICONTROL Param 3]:** ([!DNL Microsoft® Advertising] templates only) The string to use as the substitution value in an ad if the title, text, display URL, or final URL contains the `{Param3}` dynamic substitution string. The maximum length is 70 characters, but be aware of the maximum length of the ad element in which you use it (for example, an ad title may include up to 25 characters).

**[!UICONTROL Initial Bid (&lt;Match Type or Ad Type&gt;)]:** The initial bid for each keyword with the specified match type or ad type.

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** ([!DNL Google Ads] and [!DNL Microsoft® Advertising] campaigns only) The type of ads: *[!UICONTROL Expanded Search Ads]* or *[!UICONTROL Responsive Search Ads]*.

**[!UICONTROL Prefill]:** (Optional) Prefills all alternate ad copy fields with text from the original ad copy fields.

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** (Responsive search ads only) The ad position at which the title/headline must be included (such as &quot;[!UICONTROL Pinned at position 1]&quot;). The default is [!UICONTROL Unpinned].

At least one title must be available for each position. If you pin multiple titles to the same position, then the final ad always includes one of those titles in the specified position. Titles pinned to position 3 may not be shown with the ad.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]**, **[!UICONTROL Headline 3]:** (Responsive search ads only) The ad titles (headlines). Each ad variation must include at least three, and up to 15, ad titles. The ad network displays ads with up to three headlines. The maximum length for each title is 30 characters, including any dynamic text (such as the values of keywords and ad customizers).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** (Existing Microsoft® Advertising standard text ads only; read-only) The title, or first line, of an ad. Microsoft® Advertising has deprecated the creation and editing of standard text ads.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]:** ([!DNL Google Ads] and [!DNL Yahoo! Japan Ads] expanded/extended text ad templates only) The headline of an ad. The maximum length for each line (after any dynamic parameters are replaced) is 30 characters or 15 double-byte characters.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** ([!DNL Google Ads] expanded text ad templates only; optional) A third headline for an ad. The maximum length (after any dynamic parameters are replaced) is 30 characters or 15 double-byte characters.

**[!UICONTROL Title]:** ([!DNL Yandex] only) The title, or first line, of an ad. The maximum is 33 characters.

**[!UICONTROL Title Part 1]**, **[!UICONTROL Title Part 2]:** (Microsoft® Advertising expanded text ads only) The headline of an ad. The maximum length for each line (after any dynamic parameters are replaced) is 30 characters or 15 double-byte characters.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** (Microsoft® Advertising expanded text ads only) The body of an ad. The maximum length (after any dynamic parameters are replaced) is 80 characters or 40 double-byte characters (such as Chinese, Japanese, and Korean).

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:** The body of the ad.

* (Google Ads expanded text ad templates) The maximum length (after any dynamic parameters are replaced) is 90 characters or 45 double-byte characters. 

* (Yahoo! Japan Ads templates) The maximum length (after any dynamic parameters are replaced) is 80 characters or 40 double-byte characters.

* (Yandex templates) The maximum length (after any dynamic parameters are replaced) is 75 characters, and a single word can't be more than 22 characters.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** (Responsive search ads only) The ad position at which the description must be included (such as &quot;[!UICONTROL Pinned at position 1]&quot;). The default is [!UICONTROL Unpinned]. At least one description must be available for each position.

If you pin multiple descriptions to the same position, then the final ad always includes one of those descriptions in the specified position. Descriptions pinned to position 2 may not be shown with the ad.

**[!UICONTROL Description 1]**, **[!UICONTROL Description 2]:** (Responsive search ads only) The ad descriptions. Each ad variation must include at least two, and up to four, ad descriptions. The ad network displays ads with up to two descriptions; enter at least two. The maximum length for each description is 90 characters, including any dynamic text (such as the values of keywords and ad customizers).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** (Google expanded text ad templates only; optional) A second line of the ad. The maximum length (after any dynamic parameters are replaced) is 90 characters or 45 double-byte characters.

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Expanded text and responsive search ads only; optional) One or two URL paths to include consecutively after the base URL. They should describe the product or service in the ad in more detail. For example, if you add a [!UICONTROL Display Path 1] of &quot;Shoes&quot; and [!UICONTROL Display Path 2] of &quot;Outdoor&quot; to the base URL www.example.com, the URL is www.example.com/Shoes/Outdoor. The maximum length (after any dynamic parameters are replaced) for each field is 15 characters or 7 double-byte characters.

For responsive search ads, insert an ad customizer using the following formats, where `Default text` is an optional value to insert when your feed file doesn't include a valid value:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, such as `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft® Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, such as `{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]:** (Existing [!DNL Microsoft® Advertising] and [!DNL Yahoo! Japan Ads] standard text ads only; read-only) The URL displayed in an ad.

[!DNL Microsoft® Advertising] and [!DNL Yahoo! Japan Ads] have deprecated the creation and editing of standard text ads.

**[!UICONTROL Base URL]:** (Accounts with destination URLs only) The page to which users are taken. It can include third-party redirection and tracking code. If you use the Adobe Advertising conversion tracking service, and the campaign settings include using the [!UICONTROL EF Redirect] and adding tracking at the ad level, then Search, Social, & Commerce automatically adds its own redirection and tracking code to the ad.

To insert a column name or modifier group as a dynamic parameter, click in the input field, and then click a column name in the column list or a [modifier name](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) in the [!UICONTROL Modifiers] list.

**[!UICONTROL Final URL]:** (Accounts with final/advanced URLs) The landing page URL to which users are taken when they click your ad. It must include the same domain as the display URL, and any parameters in the final URL must match the parameters in the landing page URL after the ad click. It may contain redirects within the landing page domain or subdomain but no redirects outside the landing page domain.

If you use a [!DNL Google Merchant] Center feed and include this value in the &quot;[!UICONTROL Link]&quot; column, then insert that column in this field.

>[!NOTE]
>
>* If you generate tracking URLs when you post data propagated through the template, then tracking parameters are appended to this value based on the account tracking settings.
>* ([!DNL Google Ads] accounts ) Avoid using macros, which aren't substituted for clicks from sources that enable parallel tracking. If the advertiser must use macros, the Adobe Account Team should work with Customer Support or the implementation team to add them.

**[!UICONTROL Tracking Template]:** (Accounts with final/advanced URLs; optional) The tracking template, which specifies all off-landing domain redirects and tracking parameters and embeds the final URL in a parameter. The tracking template at the most granular level (with keyword as the most granular) override values at all other levels.

For Adobe Advertising conversion tracking, which is applied when the campaign settings include &quot;[!UICONTROL EF Redirect]&quot; and &quot;[!UICONTROL Auto Upload],&quot; Search, Social, & Commerce automatically appends redirect and tracking code when you save the record.

For third-party redirects and tracking, enter a value. To indicate the landing page URL:

* For Yahoo! Japan Ads accounts, use the parameter {lpurl}.

* For parameters available for Microsoft® Advertising and Google Ads accounts, see the [[!DNL Microsoft® Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) or the &quot;Tracking template only&quot;parameters in the section on &quot;Available [!DNL ValueTrack] Parameters&quot; in the [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

**\[Alternate ad fields below the original ad fields\]:** (Optional) An alternate set of ad copy for an ad, which may be used if any of the lines in the original ad copy exceed the maximum length allowed once any dynamic parameters are filled in with data during propagation.

>[!NOTE]
>
>* If the [!UICONTROL Prefill] option is selected, then the alternate fields are pre-filled with the original fields, and you can edit them as needed.
>* Only the ad copy fields that exceed the maximum length are replaced with the alternate value. For example, if only an original headline or title is too long, then the generated ad variation uses the alternate headline or title and the original descriptions. Therefore make sure that the alternate ad copy makes sense when combined with the original ad copy.
>* If the original ad copy meets the search engine's length requirements, then the alternate ad copy is discarded.

**\[Component\] [!UICONTROL Ad Label Classifications] &gt; \[Label Classification and Value\]:** (Optional) Values for up to five existing label classifications to assign to the ad variations that are created or edited using the template. For each campaign component to which you want to assign label classifications:

1. Click the check box.

1. Configure the label classification values for the ad variation template:

   * For each label classification and value to assign to the component, do the following:
   
     1. Click **[!UICONTROL Add Label Classification]**.
     
     1. Select the existing label classification, and then either select an existing value or enter a new value.
     
        The maximum length for each value is 100 characters, and it can include ASCII and non-ASCII characters.
        
        To insert a column name as a dynamic parameter for a label classification value, click in the input field (the second field), and then click a column name in the column list.
        
        You can include only one value per classification per campaign component. For example, a campaign can have Color=Red but not Color=Red and Color=Blue.
        
        * To change an existing label classification value, select or enter a new value.
        
        * To remove an existing label classification value, click **[!UICONTROL X]** next to the value.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [About automating ad management using inventory feeds](../inventory-feeds-about.md)
>* [Managing modifiers](../modifiers-manage.md)
>* [Managing inventory data feed files](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Propagate feed data through templates](../feed-data-propagate.md)
>* [Post campaign data from inventory feeds to ad networks](../propagated-data-post.md)
