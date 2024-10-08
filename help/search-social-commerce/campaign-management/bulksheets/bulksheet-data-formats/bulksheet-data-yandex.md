---
title: Required bulksheet data for [!DNL Yandex] accounts
description: Reference the required header fields and data fields in bulksheets for [!DNL Yandex] accounts.
exl-id: bf5a22dd-75c2-486d-85fd-e042bdb87de3
feature: Search Bulksheets
---
# Appendix - Required bulksheet data for [!DNL Yandex] accounts

To create and update [!DNL Yandex] campaign data in bulk, you can use Search, Social, & Commerce bulksheet files formatted specifically for [!DNL Yandex] accounts. You can either a) [generate bulk sheet files for existing accounts](../bulksheet-download.md) in the required file format or b) create them manually (see "[Supported Bulksheet File Formats](bulksheet-file-formats.md)" for general information about the supported file formats).

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Campaign Start Date,Campaign Budget,Delivery Method,Ad Group Name,Ad Title,Ad Description,Base URL,Destination URL,SiteLink Title,SiteLink Base URL,SiteLink Destination URL,Keyword,Max CPC,Match Type,Search Network Status,Content Network Status,Negative Keywords (Yandex),Param1 (Yandex),Param2 (Yandex),Campaign Status,Ad Group Status,Ad Status,Keyword Status,SiteLink Status,Campaign ID,Ad Group ID, Ad ID,Keyword ID,AMO ID, [Advertiser-specific Label Classification],Constraints,EF Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## Available data fields

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

>[!TIP]
>
>The following table is wide. To expand your viewing area, you can temporarily hide the table of contents and the right pane by clicking ![Hide left pane](/help/dsp/assets/hide-left-pane.png "Hide left pane") at the top of the left pane and ![Hide right pane](/help/dsp/assets/hide-right-pane.png "Hide right pane") at the top of the right pane. You can also use the scrollbar at the bottom of the table to view the full contents.

| Field | Campaign | Ad Group | Keyword | Text Ad | Sitelink | Description |
|----|----|-----|-----|----|----|----|
| [!UICONTROL Platform] | n/a | n/a | n/a | n/a | n/a | (Included in generated bulksheets for information purposes) The ad platform. Required unless each row includes an AMO ID for the entity. |
| [!UICONTROL Acct Name] | Required/Optional | Required/Optional | Required/Optional | Required/Optional | Required/Optional | (Included in generated bulksheets for information purposes) The ad platform. Required unless each row includes an AMO ID for the entity. |
| [!UICONTROL Campaign Name] | Required | Required | Required | Required | Required | The unique name that identifies a campaign for an account. |
| [!UICONTROL Campaign Start Date] | Required: Create<br>Optional: Edit or delete | n/a | n/a | n/a | n/a | The first date on which bids may be placed for a campaign, in the advertiser's time zone and in one of the following formats: m/d/yyyy, m/d/yy, m-d-yyyy, or m-d-yy. The default for new campaigns is the current day. |
| [!UICONTROL Campaign Budget] | Required: Create<br>Optional: Edit or delete | n/a | n/a | n/a | n/a | A lifetime spending limit for the campaign, with or without monetary symbols and punctuation. |
| [!UICONTROL Delivery Method] | Required: Create<br>Optional: Edit or delete | n/a | n/a | n/a | n/a | How quickly to show ads for the campaign each day:<ul><li><i>[!UICONTROL Standard (Distributed)]</i> (the default for new campaigns): To spread your ad impressions across the day.</li><li><i>[!UICONTROL Accelerated]:</i> To display your ads as often as possible until your budget is reached. As a result, your ads may not appear later in the day.</li></ul> |
| [!UICONTROL Ad Group Name] | n/a | Required | Required | Required | n/a | The ad group. |
| [!UICONTROL Ad Title] | n/a | n/a | n/a | Required | n/a | The headline of the banner (ad). The maximum length is 33 characters, and a single word can't include more than 23 characters.<br><br><b>Note:</b> Changing the ad copy deletes the existing ad and creates a new one. |
| [!UICONTROL Ad Description] | n/a | n/a | n/a | Required | n/a | The body of the banner (ad). The maximum length is 75 characters, and a single word can't be more than 22 characters.<br><br><b>Note:</b> Changing the ad copy deletes the existing ad and creates a new one. |
| [!UICONTROL Base URL] | n/a | n/a | Optional | Required | n/a | The landing page URL to which end users are taken when they click your ad, including any append parameters configured for the campaign or account. The maximum length is 1024 characters, including the protocol.<br><br>Base/final URLs at the keyword level override URLs at the ad level and higher. |
| [!UICONTROL Destination URL] | n/a | n/a | n/a | n/a | n/a | (Included in generated bulksheets for information purposes; not posted to the ad network) For accounts with destination URLs, this value is the URL that links an ad to a base URL/landing page on the advertiser's website (sometimes via another site that tracks the click and then redirects the user to the landing page). It includes any append parameters configured for the Search, Social, & Commerce campaign or account. If you generated tracking URLs, this value is based on the tracking parameters in your account settings and campaign settings. If you appended ad network-specific parameters, they may be replaced with the equivalent parameters for Search, Social, & Commerce. |
| [!UICONTROL SiteLink Title] | n/a | n/a | n/a | n/a | Required | The sitelink text. For new sitelinks, include the campaign name within the sitelink row. For ad group-level or ad-level sitelinks, also include the ad group name or the ad title and text, respectively.<br><br><b>Note:</b> You can have up to four sitelinks. |
| [!UICONTROL SiteLink Base URL] | n/a | n/a | n/a | n/a | Required | The base URL for a sitelink; it must be the base URL for the banner. See &quot;[!UICONTROL Base URL].&quot; |
| [!UICONTROL SiteLink Destination URL] | n/a | n/a | n/a | n/a | n/a | The destination URL for a sitelink; it must be the destination URL for the banner. See &quot;[!UICONTROL Destination URL].&quot; |
| [!UICONTROL Keyword] | Optional / n/a | n/a | Required | n/a | n/a | The phrase (keyword string). An ad must have at least one phrase. Each keyword can have a maximum of seven words, excluding stop words.<br><br><b>Notes:</b><ul><li>To exclude a phrase at the campaign level, set the [!UICONTROL Match Type] to [!UICONTROL Negative].</li><li>Changing a phrase deletes the existing phrase and creates a new one.</li><li>Changing a [!DNL Yandex] keyword phrase or match type deletes the existing keyword phrase and creates a new one.</li></ul> |
| [!UICONTROL Max CPC] | n/a | Required: Create<br>Optional: Edit or delete | Optional | n/a | n/a | The maximum cost per click (CPC), which is the highest amount to pay for a banner (ad) click on the search network, with or without monetary symbols and punctuation. You can set values for ad groups and keywords. The default for a new keyword is inherited from the ad group level. |
| [!UICONTROL Match Type] | Optional / n/a | n/a | Optional: Create<br>Required/Optional: Edit or delete | n/a | n/a | The keyword matching option for the phrase: <i>[!UICONTROL Content]</i> or <i>[!UICONTROL Search]</i>. Define negative keywords using the &quot;[!UICONTROL Negative Keywords]&quot; column.<br><br><b>Note:</b> Changing a [!DNL Yandex] keyword phrase or match type deletes the existing keyword phrase and creates a new one. |
| [!UICONTROL Search Network Status] | Optional | n/a | n/a | n/a | n/a | Whether to place ads on the search network: <i>[!UICONTROL Yes]</i> (the default) or <i>[!UICONTROL No]</i>. |
| Content Network Status | Optional | n/a | n/a | n/a | n/a | Whether to place ads on the [!DNL Yandex] advertising (display) network: <i>[!UICONTROL Yes]</i> (the default) or <i>[!UICONTROL No]</i>. |
| [!UICONTROL Negative Keywords (Yandex)] | n/a | n/a | Optional | n/a | n/a | Negative keywords (phrases) that are shared by all phrases in an ad group, preceded by a minus sign (such as `-mykeyword`). If a negative keyword matches a keyword in a phrase, then the negative keyword isn't applied to the phrase. |
| [!UICONTROL Param1 (Yandex)] | n/a | n/a | Optional | n/a | n/a | Value of the `{param1}` substitution variable. It can include up to 255 bytes. To delete the existing value, use the value `[delete]` (including the brackets). |
| [!UICONTROL Param2 (Yandex)] | n/a | n/a | Optional | n/a | n/a | Value of the  `{param2}` substitution variable. It can include up to 255 bytes. To delete the existing value, use the value `[delete]` (including the brackets). |
| [!UICONTROL Campaign Status] | Optional: Create or edit<br>Required: Delete | n/a | n/a | n/a | n/a | The display status of the campaign: <i>[!UICONTROL active]</i>, <i>[!UICONTROL archived]</i>, <i>[!UICONTROL deleted]</i>, <i>[!UICONTROL disapproved]</i>, <i>[!UICONTROL pending]</i>, or <i>[!UICONTROL stop]</i> (paused). The default for new campaigns is <i>[!UICONTROL active]</i>.<br><br><b>Notes:</b><ul></li>If a campaign has ever been active, you can't delete it. Instead, archive it.</li><li>Campaigns may be automatically archived or removed in some situations.</li><li>You can't manually set the status to <i>[!UICONTROL disapproved]</i> or <i>[!UICONTROL pending]</i>, nor change those statuses.</li></ul> |
| [!UICONTROL Ad Group Status] | n/a | Optional: Create or edit<br>Required: Delete | n/a | n/a | n/a | The display status of the ad group: <i>[!UICONTROL active]</i>, <i>[!UICONTROL archived]</i>, <i>[!UICONTROL deleted]</i>, <i>[!UICONTROL disapproved]</i>, <i>[!UICONTROL pending]</i>, or <i>[!UICONTROL stop]</i> (paused). The default for new ad groups is <i>[!UICONTROL active]</i>.<br><br><b>Notes:</b><ul></li>If an ad group has ever been active, you can't delete it. Instead, archive it.</li><li>You can't manually set the status to <i>[!UICONTROL disapproved]</i> or <i>[!UICONTROL pending]</i>, nor change those statuses.</li></ul> |
| [!UICONTROL Ad Status] | n/a | n/a | n/a | Optional: Create or edit<br>Required: Delete | n/a | The display status of the banner (ad): <i>[!UICONTROL active]</i>, <i>[!UICONTROL archived]</i>, <i>[!UICONTROL deleted]</i>, <i>[!UICONTROL disapproved]</i>, <i>[!UICONTROL pending]</i>, or <i>[!UICONTROL stop]</i> (paused). The default for new banners is <i>[!UICONTROL active]</i>.<br><br><b>Note: You can't manually set the status to <i>[!UICONTROL disapproved]</i> or <i>[!UICONTROL pending]</i>, nor change those statuses. |
| [!UICONTROL Keyword Status] | n/a | n/a | Optional: Create or edit<br>Required: Delete | n/a | n/a | The display status of the phrase (keyword): <i>[!UICONTROL active]</i>. The default for new phrases is <i>[!UICONTROL active]</i>.<br><br><b>Note: You can't manually set the status to <i>[!UICONTROL disapproved]</i> or <i>[!UICONTROL pending]</i>, nor change those statuses. |
| [!UICONTROL SiteLink Status] | n/a | n/a | n/a | n/a | Optional: Create or edit<br>Required: Delete | The display status of the sitelink: <i>[*UICONTROL Active]</i> or <i>[*UICONTROL Paused]</i>. The default for new sitelinks is <i>[*UICONTROL Active]</i>. |
| [!UICONTROL Campaign ID] | n/a: Create<br>Required/Optional: Edit<br>Optional: Delete | Optional | Optional | Optional | Optional | The unique ID that identifies an existing campaign. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change the campaign name, unless the row includes an AMO ID for the campaign. |
| [!UICONTROL Ad Group ID] | n/a | n/a: Create<br>Required/Optional: Edit<br>Optional: Delete | Optional | Optional | n/a | The unique ID that identifies an existing ad group. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change the ad group name, unless the row includes an AMO ID for the ad group. |
| [!UICONTROL Ad ID] | n/a | n/a | n/a | n/a: Create<br>Required/Optional: Edit or delete | n/a | The unique ID that identifies an existing keyword. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change the keyword name, unless the row includes a) sufficient property columns to identify the keyword or b) an AMO ID. |
| [!UICONTROL Keyword ID] | n/a | n/a | n/a: Create<br>Required/Optional: Edit<br>Required: Delete | n/a | n/a | The unique ID that identifies an existing keyword. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change the keyword name, unless the row includes a) sufficient property columns to identify the keyword or b) an AMO ID. |
| [!UICONTROL AMO ID] | n/a | n/a | n/a | n/a | n/a | (In generated bulksheets) An [!DNL Adobe]-generated unique identifier for a synced entity. For responsive search ads, the AMO ID is required to edit or delete ads unless you include the [!UICONTROL Ad ID]. To edit data for all other entity types with an AMO ID, the AMO ID is required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |
| \[Advertiser-specific Label Classification\] | Optional | Optional | Optional | Optional | n/a | (Named for an advertiser-specific label classification, such as "Color" for a label classification called Color) A value for the specified classification that is associated with the entity. You can include only one value per classification per entity (such as "red" for the "Color" label classification for Campaign A). The maximum length is 100 characters, and the value can include ASCII and non-ASCII characters.<br><br>Label classifications and their label values are applied to all child components; new components that are added later are automatically associated with the label. Label classifications for product groups are applied to the unit (most granular) level.<br><br>The classification name and the classification value aren't case-sensitive. |
| [!UICONTROL Constraints] | Optional | Optional | Optional | n/a | n/a | A constraint that's assigned to the entity. You can assign only one constraint per entity.<br><br>Constraints are inherited by child entities, so you don't need to enter values for child entities unless you want to override the inherited values. |
| [!UICONTROL EF Error Message] | n/a | n/a | n/a | n/a | n/a | (Included in generated bulksheets for information purposes) Placeholder for displaying error messages from Search, Social, & Commerce regarding data in the row; error messages are included in [!UICONTROL EF Errors] files. This value isn't posted to the ad network. |

[^1]: Excel converts large numbers to scientific notation (such as 2.12E+09 for 2115585666) when it opens the file. To view digits in the standard notation, select any cell in the column and click inside the formula bar.

>[!MORELIKETHIS]
>
>* [Appendix - Bulksheet errors](../bulksheet-errors.md)
>* [Operations you can perform in bulksheets](bulksheet-operations.md)
>* [Supported bulksheet file formats](bulksheet-file-formats.md)
>* [Download/Create a bulksheet file](../bulksheet-download.md)
>* [Click-tracking formats for [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Upload a bulksheet file or corrected error file](../bulksheet-upload.md)
