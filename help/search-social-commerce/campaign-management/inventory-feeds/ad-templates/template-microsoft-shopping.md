---
title: '[!DNL Microsoft® Ads] shopping ad template settings for inventory feeds'
description: Reference the settings for [!DNL Microsoft® Ads] shopping ad templates for inventory feeds.
exl-id: 64d0092a-bd63-48f4-8e15-f5585f7a022a
feature: Search Inventory Feeds
---
# [!DNL Microsoft® Ads] shopping ad template settings for inventory feeds

Use shopping ad templates to configure shopping ads.

>[!NOTE]
>
>* The following characters are reserved for designating column names and modifier names in the template, and are therefore prohibited as text in all attribute fields:  `[ ] < > `


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

<!-- **[!UICONTROL Campaign Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-only.md}}

<!-- **[!UICONTROL Campaign Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-method.md}}

**[!UICONTROL Campaign Tracking Template]:** (Optional for templates for client feed files) The campaign-level tracking template, which specifies all off-landing domain redirects and tracking parameters and embeds the final URL in a parameter. This value overrides the account-level setting, but tracking templates at more granular levels (with keyword as the most granular) override this value.

* For Adobe Advertising conversion tracking, which is applied when the campaign settings include &quot;[!UICONTROL EF Redirect]&quot; and &quot;[!UICONTROL Auto Upload],&quot; do one of the following":

  * (Recommended) Use the [tracking template format for Microsoft® shopping campaigns](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md). If the entire account is dedicated to shopping ads, you can instead define a tracking template at the account level.
  
  * If you instead include a value for each product in the feed using the "[!DNL bingads_redirect]" column (using the [correct format](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)), then enter the parameter `{lpurl}`. You can optionally add third-party redirects and tracking to the `{lpurl}` parameter.

* For third-party redirects and tracking, enter a value.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** The customer ID of the merchant account whose products are used for the campaign.

**[!UICONTROL Sales Country]:** The country in which the campaign's products are sold. Because products are associated
with target countries, this setting determines which products are advertised in the campaign.

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

**[!UICONTROL Campaign Priority]:** The priority with which the campaign is used when multiple campaigns advertise the
same product: *[!UICONTROL Low]* (the default for new campaigns), *[!UICONTROL Medium]*, or *[!UICONTROL High]*. When the same product is included in more than one campaign, the ad network uses
the campaign priority first to determine which campaign (and associated bid) is eligible for the ad auction. When all campaigns have the same priority, the campaign with the highest bid is eligible.

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Optional) An ad group-level tracking template, which specifies all off-landing domain redirects and tracking parameters and embeds the final URL in a parameter. This value overrides the account- and campaign-level settings, but tracking templates at more granular levels override this value.

For Adobe Advertising conversion tracking, you don't need to enter a value. The campaign-level value is enough.

For third-party redirects and tracking, enter a value.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** The default, all-inclusive product group, "[!UICONTROL All products]." You can't delete this parent product group, but it's automatically deleted when all lower tiers are missing from the feed.

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** (Units without child product groups; optional) The tracking template for the product
group, which specifies all off-landing domain redirects and tracking parameters and embeds the final URL in a [!DNL ValueTrack] parameter. This template overrides templates at higher levels.

For Adobe Advertising conversion tracking, you don't need to enter a value. The campaign-level value is enough.

For third-party redirects and tracking, enter a value.

**[!UICONTROL Initial Bid]:** The initial bid for each ad.

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
