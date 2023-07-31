---
title: Bulksheet data for [!DNL Yahoo! Display Network] accounts
description: Reference the header fields and data fields in downloaded bulksheets for [!DNL Yahoo! Display Network] accounts.
exl-id: 233a7e1f-328b-4ff8-9e38-66c3185414b6
feature: Search Bulksheets
---
# Appendix - Bulksheet data for [!DNL Yahoo! Display Network] accounts

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

You can download data for [!DNL Yahoo! Display Network] accounts in bulk but can't upload or post bulksheets to the ad network.

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

The following example shows data in comma-delimited values. If you're using tab-separated values, then the data looks different.

Platform,Acct Name,Campaign Name,Ad Group Name,Ad Name, Ad Title,Description Line 1,Description Line 2,Base URL/Final URL,Destination URL,[Advertiser-specific Label Classification],Bid Rules,Constraints,Campaign Status,Ad Group Status,Ad Status,Campaign ID,Ad Group ID,Ad ID,AMO ID,EF Error Message

-->

## Available data fields

| Field | Campaign | Ad Group | Ad | Description |
|----|----|----|----|----|
| [!UICONTROL Platform] | n/a | n/a | n/a | (Included in generated bulksheets for information purposes) The ad platform. |
| [!UICONTROL Acct  Name] | If included | If included | If included | The unique name that identifies an ad network account. |
| [!UICONTROL Campaign Name] | If included | If included | If included | The unique name that identifies a campaign for an account. |
| [!UICONTROL Ad Group Name] | n/a | If included | If included | The unique name that identifies an ad group. |
| [!UICONTROL Ad Name] | n/a | n/a | If included | The unique name that identifies the ad within an ad group. The maximum length is 50 characters. |
| [!UICONTROL Ad Title] | n/a | n/a | If included | The headline of an ad. |
| [!UICONTROL Description Line 1] | n/a | n/a | If included | The first line of the body of an ad. |
| [!UICONTROL Description Line 2] | n/a | n/a | If included | The second line of the body of an ad. |
| [!UICONTROL Base URL/Final URL] | n/a | n/a | If included | The landing page URL to which end users are taken when they click your ad, including any append parameters configured for the campaign or account. Base/final URLs at the keyword level override URLs at the ad level and higher. |
| [!UICONTROL Destination URL] | n/a | n/a | n/a | (Included in generated bulksheets for information purposes; not posted to the ad network) For accounts with destination URLs, this value is the URL that links an ad to a base URL/landing page on the advertiser's website (sometimes via another site that tracks the click and then redirects the user to the landing page). It includes any append parameters configured for the Search, Social, & Commerce campaign or account. If you generated tracking URLs, this value is based on the tracking parameters in your account settings and campaign settings. If you appended ad network-specific parameters, then they may be replaced with the equivalent parameters for Search, Social, & Commerce. |
| \[Advertiser-specific Label Classification\] | If included | If included | If included | (Named for an advertiser-specific label classification, such as &quot;Color&quot; for a label classification called Color) A value for the specified classification that is associated with the entity. |
| [!UICONTROL Constraints] | If included | If included | n/a | A constraint that's assigned to the entity. |
| [!UICONTROL Campaign Status] | If included | n/a | n/a | The display status of the campaign: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, or <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | n/a | If included | n/a | The display status of the ad group: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, or <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Keyword Status] | n/a | n/a | If included | The display status of the keyword: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, or <i>[!UICONTROL Deleted]</i> (existing keywords only). |
| [!UICONTROL Campaign ID] | If included | If included | If included | The unique ID that identifies an existing campaign. |
| [!UICONTROL Ad Group ID] | n/a | If included | If included | The unique ID that identifies an existing ad group. |
| [!UICONTROL Keyword ID] | n/a | n/a | If included | The unique ID that identifies an existing keyword. |
| [!UICONTROL AMO ID] | n/a | n/a | n/a | (In generated bulksheets) An Adobe-generated unique identifier for a synced entity. |
| [!UICONTROL EF Error Message] | n/a | n/a | n/a | (Included in generated bulksheets for information purposes) Placeholder for displaying error messages from Search, Social, & Commerce regarding data in the row; error messages are included in [!UICONTROL EF Errors] files. |

>[!MORELIKETHIS]
>
>* [Download/Create a bulksheet file](../bulksheet-download.md)
