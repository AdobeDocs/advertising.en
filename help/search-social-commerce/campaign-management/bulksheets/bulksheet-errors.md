---
title: Bulksheet errors
description: Reference potential reasons for each bulksheet error. 
---
# Bulksheet errors

Search, Social, & Commerce generates two types of error files during bulksheet operations:

* **SE Errors:** When a file is posted but the ad network doesn't accept all of the data, an error file called `<uploaded file name>_se_errors.<extension used for the bulksheet>` is created. When some but not all rows were accepted, the error file shows the rows that weren't posted and an explanation of each error so you can correct it. The errors are included in the "[!UICONTROL SE Error Message]" column.

 >[!NOTE]
 >
 >If you post any [!DNL Google Ads] ads that violate the ad network's advertising policies but may be eligible for exemptions, then those ads are automatically reposted with exemption requests. If the exemption request fails, then information about the violation is included in the error file.

* **EF Errors:** When the bulksheet operation can't upload or process a file or individual rows in the file, it creates an error file called `<uploaded file name>_ef_errors.<extension used for the bulksheet>`. If the problem is with individual rows, then those rows are included,
with an explanation of each error so you can correct it. The errors are included in the "[!UICONTROL EF Error Message]" column.

## [!UICONTROL SE Error] messages

Errors in the [!UICONTROL SE Error] column come directly from the ad network.

## [!UICONTROL EF Error] messages

The following errors may be included in the [!UICONTROL EF Error] column in EF Errors files.

### Download/Create errors

| Category | Message | Description |
|----|----|----|
| General | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | The operation failed completely because of an uncategorized or unhandled error. If the problem persists, contact your Adobe Account Team to investigate the cause. |
| | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | Search, Social, & Commerce couldn't sync with the ad network before creating the bulksheet, so no bulksheet was created. If the problem persists, contact your Adobe Account Team. |

### Upload errors

| Category | Message | Description |
|----|----|----|
| General | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | The operation failed completely. If the problem persists, contact your Adobe Account Team. |
| All entities | [!UICONTROL Invalid Fields.] \[invalid fields and error\] | The specified data is missing or invalid. |
|  | [!UICONTROL Invalid Reference Given] | The entity's ID on the ad network, or a parent entity's ID (such as the account ID), doesn't correspond to an entity in Search, Social, & Commerce. This can occur when you edited the ID in the bulksheet. |
|  | [!UICONTROL &lt;Entity&gt; is deleted or expired] | The entity is expired or was deleted, and you can't change its properties. The entity may be deleted when someone manually edited the status. |
|  | [!UICONTROL &lt;Entity&gt; status should be Active or Paused] | (New entities) A new entity can be only &quot;Active&quot; or &quot;Paused.&quot; |
|  | [!UICONTROL Duplicate Entries are present] | Multiple rows are included for the same entity, with different attributes in each row. Consolidate the changes into one row. |
|  | [!UICONTROL Invalid AMO ID given] | The AMO ID for the row doesn't exist. This can occur if you edited the ID in the bulksheet. |
|  | [!UICONTROL Invalid row given] | The row doesn't include enough information to determine the entity type. Edit the row to include all required fields for the entity type. |
| Accounts | [!UICONTROL Provide Valid Account Details] | (Bulksheets for multiple accounts) Account identifiers aren't included in all rows. Enter values for either of the following combinations of columns for each row: a) &quot;[!UICONTROL AMO ID]&quot; or b) &quot;[!UICONTROL Account Name]&quot; and &quot;[!UICONTROL Platform].&quot; |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed]  | Search, Social, & Commerce doesn't have access to the ad network account, so you can't create or edit campaign data. Make sure that the credentials for the search account are correct and that the account is enabled. |
| Campaign | [!UICONTROL Invalid Shopping Country specified] | (Shopping campaigns) The value in the &quot;[!UICONTROL Sales Country]&quot; field is invalid. See a list of valid countries [for [!DNL Google Ads]](https://support.google.com/merchants/answer/160637#countrytable) and [for [!DNL Microsoft® Advertising]](https://help.ads.microsoft.com/#apex/3/en/51083). |
| All campaign components | [!UICONTROL Campaign creation failed] | The parent campaign wasn't created, so this entity wasn't created. Make sure that all parent entities contain all required fields. |
| Ad group | [!UICONTROL Campaign Row missing] | The specified parent campaign doesn't exist, so the ad group wasn't created. Create the parent campaign in a new row. |
|  | [!UICONTROL New adgroup has both keywords and placement] | An ad group can contain either keywords or placements, but not both. Create separate ad groups for keywords and placements. |
|  | [!UICONTROL No corresponding keyword for Adgroup] | ([!DNL Yandex]) The ad group wasn't created because it doesn't include at least one keyword. |
|  | [!UICONTROL No corresponding creative for Adgroup] | ([!DNL Yandex]) The ad group wasn't created because it doesn't include at least one ad. |
|  | [!UICONTROL Creative Row Missing] | ([!DNL Yandex]) The ad group wasn't created because it doesn't include at least one ad. |
| All ad group components | [!UICONTROL Adgroup creation failed] | The parent ad group wasn't created, so this entity couldn't be created. This could be because of an error in the ad group fields or because the parent campaign failed. Make sure that all parent entities contain all required fields. |
|  | [!UICONTROL Adgroup Row Missing] | The specified parent ad group doesn't exist, so the entity couldn't be created. Create the parent ad group in a new row. |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | The &quot;[!UICONTROL Tracking Template]&quot; field is only for accounts that use final/advanced URLs. Remove the value until you have migrated the account to use final/advanced URLs. |
| Ad | [!UICONTROL Cannot modify attributes other than status code and url for &lt;ad type&gt;] | (Ad types other than text, expanded text, product, app install, and dynamic search) You can edit only the status and URL for this ad type. |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | Each ad group can include up to 50 ads, and this bulksheet includes more than 50. Reduce the number of ads. |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | The ad is in an expired or deleted parent entity, so you can't edit it. |
| Keyword | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | The parent campaign or ad group is deleted or expired, so you can't change the entity. |
| Placement | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | The parent campaign or ad group is deleted or expired, so you can't change the entity. |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | (Google Ads) You can bid on placements only in campaigns on the search network only or on the content network only, but not on campaigns that target both search and content networks. |
| Shopping product group | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | Each level of product group must include an &quot;[!UICONTROL Everything Else]&quot; group. You can't manually delete an &quot;[!UICONTROL Everything Else]&quot; group; it's automatically deleted when you delete all other product groups at the same level. |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | The parent campaign or ad group is deleted or expired, so you can't change the entity. |
| Sitelink | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | ([!DNL Yandex] only) The message is inaccurate; each campaign can include up to four (not 10) sitelinks, and this bulksheet includes more than four. Remove some sitelinks. |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | The parent campaign is expired or deleted, so you can't edit the sitelink. |
|  | [!UICONTROL Creative creation failed] | ([!DNL Yandex]) The sitelink couldn't be created because the ad wasn't created. |
| Location target | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | The parent campaign or ad group is deleted or expired, so you can't edit the location targets. |
| Exclusions | [!UICONTROL Other than status is modified] | You can edit only the status of an exclusion (&quot;[!UICONTROL Active]&quot; or &quot;[!UICONTROL Deleted]&quot;). |
| Google remarketing list targets/audiences | [!UICONTROL Invalid Audience given] | ([!DNL Google Ads] campaigns only) The RLSA target doesn't correspond to an existing RLSA (audience). Correct the values in the &quot;[!UICONTROL Audience]&quot; and &quot;[!UICONTROL RLSA Target]&quot; columns. |

### Post errors

The following errors occur in EF Errors files only. Most posting errors come from the ad network and are included in an SE Errors file.

| Category | Message | Description |
|----|----|----|
| General | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | The operation failed completely. If the problem persists, contact your Adobe Account Team. |
| All entities | [!UICONTROL Entity] is posted to ad network | The entity was posted to the ad network, but it wasn't synced to Search, Social, & Commerce at the same time, so the entity data isn't immediately available in Search, Social, & Commerce. The sync process is automatically triggered now.<br><br>When large amounts of data are synced, the data may not be available in Search, Social, & Commerce for several hours or more. |
| | [!UICONTROL Skipping &lt;ENTITY&gt; creation since &lt;PARENT ENTITY&gt; creation failed.] | The parent entity couldn't be created, so this child entity wasn't created. |

>[!MORELIKETHIS]
>
>* [About managing campaign data using bulksheets](bulksheet-about.md)
>* [Download/Create a bulksheet file](bulksheet-download.md)
>* [Validate landing pages in bulksheet files](bulksheet-validate-landing-pages.md)
>* [Upload a bulksheet file or corrected error file](bulksheet-upload.md)
>* [Post bulksheets or corrected error files](bulksheet-post.md)
