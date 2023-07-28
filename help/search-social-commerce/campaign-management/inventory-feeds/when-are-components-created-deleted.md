---
title: When are account components created or deleted by inventory feeds?
description: Learn which situations create and delete account components when you post inventory feeds.
exl-id: 93b31996-15dd-4215-ae9d-39327910f712
feature: Search Inventory Feeds
---
# When are account components created or deleted by inventory feeds?

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (delete actions only), and [!DNL Yandex] accounts only*

When an inventory feed file is propagated through a template, account components are created and deleted as follows.

>[!NOTE]
>
>Duplicate ads are never created within an ad group.

| Scenario | Example | Action |
|----|----|----|
| Feed data includes a new value for a column used in a campaign name, ad group name, keyword, or product group. | Previous files:<br>Campaign=Hats<br>Campaign=Gloves<br><br>New file:<br>Campaign=Shoes | A new campaign, ad group, keyword, or product group is created if it doesn't exist on the ad network. |
| Feed data contains a new value for a column used in an ad. | Previous file: An ad included price=20<br><br>New file: For the same ad, price=10 | When the ad copy for [!DNL Microsoft® Advertising] expanded text ads, [!DNL Yahoo! Japan ads], or [!DNL Yandex] ads is changed, the existing ad is deleted and a new one is created.<br><br>When ad copy is changed for other ad types or when the applicable column is used for a [!DNL Google Ads] ad parameter ({param1} or {param2}) in an ad, then the existing ad is updated. |
| The template settings for the campaign, ad group, keyword, or product group changed since the last propagation. | Previous setting:Keyword=[Keyword]<br><br>New setting: Keyword=&lt;Color&gt;[Keyword] | A new campaign, ad group, keyword, or product group is created if it doesn't exist on the ad network. |
| The template settings for an ad changed since the last propagation. | Previous setting: Ad description=&quot;Buy [category] now.&quot;<br><br>New setting: Ad description=&quot;Buy [brand] now.&quot; | When the ad copy for [!DNL Microsoft® Advertising] expanded text ads, [!DNL Yahoo! Japan ads], or [!DNL Yandex] ads is changed, the existing ad is deleted and a new one is created.<br><br>When ad copy is changed for other ad types or when the change reflects a change in the column used for a single [!DNL Google Ads] ad parameter ({param1} or {param2}) in an ad, then the existing ad is updated. |
| New feed data doesn't include a row for an existing campaign or ad group. | n/a | The existing campaigns and ad groups remain as-is. |
| New feed data doesn't include a row for an existing ad group, ad, keyword, or product group. | n/a | The existing ad group, ad, keyword, or product group remains as-is, is paused, or is deleted, according to the [feed data settings](feed-settings-manage.md#feed-data-settings). |
| New feed data for an existing parent product group doesn't include rows for its existing child product groups. | n/a | The existing parent product group remains as-is or is deleted, according to the [feed data settings](feed-settings-manage.md#feed-data-settings). <b>Note:</b> If the feed data settings are configured to pause missing line items, then the parent product group is still deleted because you can't pause product groups. |
| New feed data includes a row for an ad group, ad, keyword, or product group that was a) in previous data but b) was omitted since then and was paused according to the [feed data settings](feed-settings-manage.md#feed-data-settings). | n/a | The existing ad group, ad, keyword, or product group is reactivated, without losing any history or the quality score. |
| New feed data includes a row for an ad group, ad, keyword, or product group that was a) in previous data but b) was omitted since then and was deleted according to the [feed data settings](feed-settings-manage.md#feed-data-settings). | n/a | A new ad group, ad, keyword, or product group is created. |
| You've disabled the campaign- or ad group-level option to &quot;[!UICONTROL Delete negative keywords when omitted from list].&quot; | The negative keywords list includes &quot;coupe&quot; and &quot;sports car.&quot;<br><br>The ad group already includes the negative keyword &quot;SUV.&quot; | Any existing negative keywords that aren't on the list remain as-is. |
| You've enabled the campaign- or ad group-level option to &quot;[!UICONTROL Delete negative keywords when omitted from list],&quot; and negative keywords that aren't on the list exist. | The negative keywords list includes &quot;coupe&quot; and &quot;sports car.&quot;<br><br>The ad group already includes the negative keyword &quot;SUV.&quot; | Any unspecified negative keywords previously created using the template are deleted when a feed file is propagated through the template. However, any unspecified negative keywords created using other means (such as in plain bulksheets, the [!UICONTROL Campaigns] views, or in the ad network's ad editor) remain as-is. | | The scheduled end date for the components of a posted feed file occurs. | n/a | The existing campaigns remain as-is. The existing ad groups, ads, and keywords remain as-is, are paused, or are deleted, according to the [feed data settings](feed-settings-manage.md#feed-data-settings). |
| The stock level of an item dips below a minimum specified in the [feed data settings](feed-settings-manage.md#feed-data-settings). | Previous file: stock=10<br><br>New file: stock=0 | The existing campaigns remain as-is. The existing ad groups, ads, keywords, and product groups are either paused or deleted, according to the [feed data settings](feed-settings-manage.md#feed-data-settings). |
| The stock level of an item goes back above a minimum specified in the [feed data settings](feed-settings-manage.md#feed-data-settings). | Previous file: stock=0<br><br> New file: stock=10 | When the existing ads, keywords, or product groups are paused, they're reactivated, without losing any history or the quality score. When no ads, keywords, or product groups exist (for example, if they were deleted previously because the stock level was below the minimum), new ones are created. |

>[!MORELIKETHIS]
>
>* [About automating ad management using inventory feeds](inventory-feeds-about.md)
