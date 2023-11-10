---
title: '[!DNL Microsoft® Advertising] campaign settings'
description: Reference the settings for [!DNL Microsoft® Advertising] campaigns.
exl-id: c6d86fb8-48b0-40fd-bcfc-c4afdccd5283
feature: Search Campaign Management
---
# [!DNL Microsoft® Advertising] campaign settings

## \[Campaign Creation screen\]

**[!UICONTROL Campaign Type]:** (Available during campaign creation only) Where to place ads, and which ad types
the campaign may contain:

* *[!UICONTROL Search]:* Shows text ads on the search network.

* *[!UICONTROL Shopping Network]:* Shows product ads &mdash; for your products in your [!DNL Microsoft® Merchant Center] product catalog &mdash; on the shopping network.

* *[!UICONTROL Audience]:* Shows native/display ads on the [!DNL Microsoft® Audience Network]. You can either a) automatically generate feed-based ads by linking the campaign to a merchant center store in the [!UICONTROL Shopping Settings] section or b) create responsive ads with text assets and uploaded images. Both options require you to create ad groups with user targeting.

* *[!UICONTROL Shopping Campaigns for Brands]:* (Beta feature) Promotes your products through linked retailers across the search and audience networks. You can create child ad groups and product groups (apps to promote), and optional product ads for the campaign; [!DNL Microsoft® Advertising] automatically creates ads for the product groups.

* *[!UICONTROL Microsoft® Store Ads Campaign]:* (Beta feature) Promotes your apps and games that are available in the [!DNL Microsoft® Store]. You can create child ad groups, product groups, and optional product ads for the campaign; [!DNL Microsoft® Advertising] automatically creates ads for the product groups.

* *[!UICONTROL Audience Video]:* (Beta feature) Shows video ads on the audience network.

* *[!UICONTROL Audience Video]:* (Beta feature) Shows connected TV (CTV) video ads on the audience network.

* *[!UICONTROL Performance Max]:* (Beta feature) Shows multiple ad types across all networks. Assign asset groups separately within the [!DNL Microsoft® Advertising] ad editor.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** A campaign name that is unique within the account. The maximum length is 128 characters.

**[!UICONTROL Status]:** The display status of the campaign: *Active* or *Paused*. The default for new ad campaigns is *Active*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** The bid strategy for the campaign:

* *[!UICONTROL CPV]* (Audience CTV video campaigns only) Uses the cost-per-view (CPV) model. <!-- Campaigns with this bid strategy aren't optimized when they're included in portfolios. -->

* *[!UICONTROL Enhanced CPC]:* (Campaigns on the audience, search, and shopping networks) Uses the ad network's enhanced cost-per-click (eCPC) model, which allows the ad network to automatically change the cost-per-click (CPC) bid for each auction in an attempt to maximize conversions, using conversions specified within the ad network (not in Search, Social, & Commerce), while trying to keep your average CPC below your maximum CPC. 

  When you add a campaign with eCPC to an optimized Search, Social, & Commerce portfolio, Search, Social, & Commerce optimizes the base bids and &mdash; when the "[!UICONTROL Auto adjust campaign budget limits]" option is enabled &mdash; the campaign budget. The ad network optimizes all bid adjustments and may change the Search, Social, & Commerce-generated bids at the time of the user query based on proprietary data and insights. **Caution:** Use eCPC campaigns in portfolios only when the total conversions tracked on the ad network align with the portfolio objective.

* *[!UICONTROL Manual CPC]*: (Shopping campaigns for brands; [!DNL Microsoft Store Ads] campaigns; deprecated by [!DNL Microsoft® Advertising] in 2021 for other campaign types) Uses the cost-per-click (CPC) model. For some ad types, you can optionally allow the ad network to change bids for the campaign:

  * **[!UICONTROL Enable Enhanced CPC]** (disabled by default): This is the same as using the "[!UICONTROL Enhanced CPC]" option.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] campaigns) Uses the cost per acquisition (CPA) model.

* *[!UICONTROL Manual CPM]* (Audience campaigns and audience video campaigns only) Uses the cost-per-thousand-impressions (CPM) model, for which you specify what you want to spend per 1,000 viewed impressions. Campaigns with this bid strategy aren't optimized when they're included in portfolios.

* *[!UICONTROL Maximize Clicks]:* (Search and shopping campaigns) The ad network &mdash; not Search, Social, & Commerce &mdash; optimizes bids to maximize clicks. Optionally, enter a **[!UICONTROL Max CPC]** (cost per click) to ensure that the ad network doesn't pay more than a specific amount for each click. **Caution:** When you add a campaign with this strategy to a portfolio, bids are driven by click weight, not by the portfolio objective.

* *[!UICONTROL Maximize Conversion Value]:* (Search and shopping/smart shopping networks, performance max campaigns) The ad network &mdash; not Search, Social, & Commerce  &mdash; optimizes bids to maximize conversion value. Optionally enter a **[!UICONTROL Target Return on Ad Spend]** (ROAS) as a percent. **Note:** Use this option for campaigns in hybrid portfolios but not standard portfolios.

* *[!UICONTROL Maximize Conversions]:* (Campaigns on the search network <!-- future: and audience network -->, performance max campaigns) The ad network &mdash; not Search, Social, & Commerce &mdash; optimizes bids to maximize conversions. Optionally enter a **[!UICONTROL Target CPC]** (cost per click)<!-- future: ; for audience campaigns, you can also enter an optional [!UICONTROL Target CPA] (cost per acquisition) -->. **Note:** Use this option for campaigns in hybrid portfolios but not standard portfolios.

* *[!UICONTROL Target CPA]:* (Campaigns on the search network) The ad network &mdash; not Search, Social, & Commerce &mdash; optimizes bids based on an optional **[!UICONTROL Target CPA]** (cost per acquisition), which is the 30-day average amount you want to pay for an acquisition (conversion). **Note:** Use this option for campaigns in hybrid portfolios (but not standard portfolios) with any spend strategy except [!UICONTROL Weekly] or [!UICONTROL Google Target CPA].

  Average position and CPC bid data aren't available for campaigns with this bid strategy.

* *[!UICONTROL Target Impression Share]:* (Campaigns on the search network) The ad network &mdash; not Search, Social, & Commerce &mdash; optimizes bids to achieve a target impression share and ad position. Optionally, enter a **[!UICONTROL Target Impression Share]** as a percent, the **[!UICONTROL Target Ad Position]**, and a **[!UICONTROL Max CPC]** (cost per click). **Note:** This option isn't supported in hybrid portfolios.

* *[!UICONTROL Target Return on Ad Spend]:*  (Campaigns on the search and shopping networks) The ad network &mdash; not Search, Social, & Commerce &mdash; optimizes bids based on your **[!UICONTROL Target ROAS]** (return on ad spend), specified as a percentage. Optionally, enter a **[!UICONTROL Max CPC]** (cost per click) to ensure that the ad network doesn't pay more than a specific amount for each click. **Note:** Use this option for campaigns in hybrid portfolios (but not standard portfolios) with any spend strategy except [!UICONTROL Weekly] or [!UICONTROL Google Target ROAS].

  Average position and CPC bid data aren't available for campaigns with this bid strategy.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Shopping campaigns only; read-only for existing campaigns) The country in which
the campaign's products are sold. Because products are associated with target countries, this setting determines which products are advertised in the campaign.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft® Merchant Center]:** (Audience campaigns only; optional) Links the campaign with a specific merchant center store for automated feed-based ads rather than responsive ads. When you select this option, specify the [!UICONTROL Merchant ID] and [!UICONTROL Products]. You need to create ad groups for the campaign, but you don't need to create ads.

Once you link the campaign to a store and save the settings, you can't change this option.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}


**[!UICONTROL Products]:** (Audience campaigns linked to a merchant center store only) The products to advertise. By default, *[!UICONTROL All products]* is selected. To advertise only products with specific attributes, select *[!UICONTROL Filter products]* and specify up to seven product dimension-and-attribute combinations on which to filter your products. All specified values must be applicable for ads to appear for the product. For example, to show ads for Acme pet supplies, you might create the filters `Custom Label 1=animals`, `Category=pet supplies`, and `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campaigns on the display/native network only; optional) Sites on the display network on which you don't want your ads to be displayed. Enter a valid URL, such as www.example.com. To specify multiple strings, separate them with commas or enter them on separate lines.

For information about availability, see Microsoft® Advertising help to "[Prevent ads from appearing on specific websites](https://help.ads.microsoft.com/#apex/bae/en/14061/0)."

## [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (For [!UICONTROL EF Redirect] only) Not implemented

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Whether to *[!UICONTROL Use account conversion goals for this campaign]* (the default) or *[!UICONTROL Use campaign specific conversion goals]*. If you choose to specify conversion goals for the campaign, then select the goals from the list of all available goals. **Note:** Goals are synchronized daily, so goals created in the previous 24 hours may not be listed. To update the list, [manually synchronize the ad network data](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

If the campaign is part of a portfolio, then use the same conversion goals as the portfolio's objective. Using different conversion goals may impact portfolio performance.

>[!MORELIKETHIS]
>
>* [Manage campaigns](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
