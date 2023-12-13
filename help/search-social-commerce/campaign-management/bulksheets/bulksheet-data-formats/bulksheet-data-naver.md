---
title: Required bulksheet data for [!DNL Naver] accounts
description: Reference the required header fields and data fields in bulksheets for [!DNL Naver] accounts.
exl-id: 1bfcdbb6-8026-4230-ab6b-b7c79b0d185a
feature: Search Bulksheets
---
# Appendix - Required bulksheet data for [!DNL Naver] accounts

Populate your [!DNL Naver] accounts in Search, Social, & Commerce by generating a bulksheet file within [!DNL Naver], and then uploading it to Search, Social, & Commerce.

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Ad Group Name,Keyword,Base URL,Destination URL,[Advertiser-specific Label Classification],Constraints,Campaign Status,Ad Group Status,Keyword Status,Campaign ID,Ad Group ID,Keyword ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## Available data fields

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Field | Campaign | Ad Group | Keyword | Description |
|----|----|----|----|----|
| [!UICONTROL Platform] | n/a | n/a | n/a | (Included in generated bulksheets for information purposes) The ad platform. Required unless each row includes an AMO ID for the entity. |
| [!UICONTROL Acct Name] | Required/Optional | Required/Optional | Required/Optional | The unique name that identifies an ad network account. Required unless each row includes an AMO ID for the entity. |
| [!UICONTROL Campaign Name] | Required | Required | Required | The unique name that identifies a campaign for an account. |
| [!UICONTROL Ad Group Name] | n/a | Required | Required | The unique name that identifies an ad group. |
| [!UICONTROL Keyword] | n/a | n/a | Required | The keyword string. |
| [!UICONTROL Base URL] | n/a | n/a | Optional | The landing page URL to which end users are taken when they click your ad, including any append parameters configured for the campaign or account.<br><br>Base/final URLs at the keyword level override URLs at the ad level and higher. |
| [!UICONTROL Destination URL] | n/a | n/a | n/a | (Included in generated bulksheets for information purposes; not posted to the ad network) For accounts with destination URLs, this value is the URL that links an ad to a base URL/landing page on the advertiser's website (sometimes via another site that tracks the click and then redirects the user to the landing page). It includes any append parameters configured for the Search, Social, & Commerce campaign or account. If you generated tracking URLs, this value is based on the tracking parameters in your account settings and campaign settings. If you appended ad network-specific parameters, they may be replaced with the equivalent parameters for Search, Social, & Commerce.<br><br>For accounts with final URLs, this column shows the same value as the [!UICONTROL Base URL/Final URL column]. |
| \[Advertiser-specific Label Classification\] | Optional | Optional | Optional | (Named for an advertiser-specific label classification, such as "Color" for a label classification called Color) A value for the specified classification that is associated with the entity. You can include only one value per  classification per entity (such as "red" for the "Color" label classification for Campaign A). The maximum length is 100 characters, and the value can include ASCII and non-ASCII characters.<br><br>Label classifications and their label values are applied to all child components; new components that are added later are automatically associated with the label. Label classifications for product groups are applied to the unit (most granular) level.<br><br>The classification name and the classification value aren't case-sensitive. |
| [!UICONTROL Constraints] | Optional | Optional | Optional | A constraint that's assigned to the entity. You can assign only one constraint per entity.<br><br>Constraints are inherited by child entities, so you don't need to enter values for child entities unless you want to override the inherited values. |
| [!UICONTROL Campaign Status] | Optional: Create or edit<br>Required: Delete | n/a | n/a | The display status of the campaign:  *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, or <i>[!UICONTROL Deleted]</i> (existing campaigns only). The default for new campaigns is <i>[!UICONTROL Active]</i>. To delete an active or paused campaign, enter the value "[!UICONTROL Deleted]". |
| [!UICONTROL Ad Group Status] | n/a | Optional: Create or edit<br>Required: Delete | n/a | The display status of the ad group:  *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, or <i>[!UICONTROL Deleted]</i> (existing ad groups only). The default for new ad groups is <i>[!UICONTROL Active]</i>. To delete an active or paused ad group, enter the value "[!UICONTROL Deleted]". |
| [!UICONTROL Keyword Status] | n/a | n/a | Optional:  Create or edit<br>Required: Delete | The display status of the keyword:  *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, or <i>[!UICONTROL Deleted]</i> (existing keywords only). The default for new keywords is <i>[!UICONTROL Active]</i>. To delete an active or paused keyword, enter the value "[!UICONTROL Deleted]". |
| [!UICONTROL Campaign ID] | n/a: Create<br>Required/Optional: Edit or delete | Optional | Optional | The unique ID that identifies an existing campaign. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change the campaign name, unless the row includes an AMO ID for the campaign. |
| [!UICONTROL Ad Group ID] | n/a | n/a: Create<br>Required/Optional: Edit or delete | Optional | The unique ID that identifies an existing ad group. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change the ad group name, unless the row includes an AMO ID for the ad group. |
| [!UICONTROL Keyword ID] | n/a | n/a | n/a: Create<br>Required/Optional: Edit<br>Required: Delete | The unique ID that identifies an existing keyword. In CSV and TSV files, it must be preceded by a single quote (').[^1] Required only when you change the keyword name, unless the row includes a) sufficient property columns to identify the keyword or b) an AMO ID. |
| [!UICONTROL AMO ID] | n/a: Create<br>Optional: Edit or delete | n/a: Create<br>Optional: Edit or delete | n/a: Create<br>Optional: Edit or delete | (In generated bulksheets) An [!DNL Adobe]-generated unique identifier for a synced entity. For responsive search ads, the AMO ID is required to edit or delete ads unless you include the [!UICONTROL Ad ID]. To edit data for all other entity types with an AMO ID, the AMO ID is required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |
| [!UICONTROL EF Error Message] | n/a | n/a | n/a | (Included in generated bulksheets for information purposes) Placeholder for displaying error messages from Search, Social, & Commerce regarding data in the row; error messages are included in [!UICONTROL EF Errors] files. This value isn't posted to the ad network. |
| [!UICONTROL SE Error Message] | n/a | n/a | n/a | (Included in generated bulksheets for information purposes) Placeholder for displaying error messages from the ad network regarding data in the row; error messages are included in [!UICONTROL SE Errors] files. This value isn't posted to the ad network. |

[^1]: Excel converts large numbers to scientific notation (such as 2.12E+09 for 2115585666) when it opens the file. To view digits in the standard notation, select any cell in the column and click inside the formula bar.

>[!MORELIKETHIS]
>
>* [Appendix - Bulksheet errors](../bulksheet-errors.md)
>* [Operations you can perform in bulksheets](bulksheet-operations.md)
>* [Supported bulksheet file formats](bulksheet-file-formats.md)
>* [Download/Create a bulksheet file](../bulksheet-download.md)
>* [Click-tracking formats for [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Upload a bulksheet file or corrected error file](../bulksheet-upload.md)
>* [Implement [!DNL Naver] tracking-only accounts](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
