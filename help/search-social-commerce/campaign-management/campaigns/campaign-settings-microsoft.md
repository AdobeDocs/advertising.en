---
title: '[!DNL Microsoft® Advertising] campaign settings'
description: Reference the settings for [!DNL Microsoft® Advertising] campaigns.
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
---
# [!DNL Microsoft® Advertising] campaign settings

## \[Campaign Creation screen\]

**[!UICONTROL Campaign Type]:** (Available during campaign creation only) Where to place ads, and which ad types
the campaign may contain:

* *[!UICONTROL Search]:* Shows text ads on the search network.

* *[!UICONTROL Shopping Network]:* Shows product ads &mdash; for your products in your [!DNL Microsoft® Merchant Center] product catalog &mdash; on the shopping network.

* *[!UICONTROL Audience]:* Shows native/display ads on the [!DNL Microsoft® Audience Network]. You can either a) automatically generate feed-based ads by linking the campaign to a merchant center store in the [!UICONTROL Shopping Settings] section or b) create responsive ads with text assets and uploaded images. Both options require you to create ad groups with user targeting.

* *[!UICONTROL Shopping Campaigns for Brands]:* (Beta feature) Promotes your products through linked retailers across the search and audience networks. You can create child ad groups and product groups (apps to promote), and optional product ads for the campaign; [!DNL Microsoft® Advertising] automatically creates ads for the product groups. For shopping campaigns for brands, use the bid strategy [!UICONTROL Manual CPC]; for shopping promotions for brands, use the bid strategy [!UICONTROL Cost per Sale].

* *[!UICONTROL Microsoft® Store Ads Campaign]:* (Beta feature) Promotes your apps and games that are available in the [!DNL Microsoft® Store]. You can create child ad groups, product groups, and optional product ads for the campaign; [!DNL Microsoft® Advertising] automatically creates ads for the product groups.

* *[!UICONTROL Audience CTV Video]:* (Beta feature) Shows connected TV (CTV) video ads on the audience network.

* *[!UICONTROL Audience Video]:* (Beta feature) Shows standard video ads on the audience network.

* *[!UICONTROL Performance Max]:* (Beta feature) Shows multiple ad types across all networks using [!DNL Microsoft Advertising] smart bidding. Within the campaign settings, you must specify one or more asset groups, which include images, logos, headlines, descriptions, an optional call to action, and audience signals. The ad network automatically combines the assets to serve ads based on the channel.

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

* *[!UICONTROL Cost per Sale]:* (Shopping campaigns only) The ad network &mdash; not Search, Social, & Commerce &mdash; optimizes bids based on the **[!UICONTROL Target CPS]** (cost per sale). You pay only when a click on your product ad results in a sale within 24 hours. **Note:** Use this option for campaigns in hybrid portfolios but not standard portfolios.<!-- Verify all -->

  Once you save a shopping campaign for brands with this bid strategy, you can't change the bid strategy. For other shopping campaign types, this strategy is available only for new campaigns.

* *[!UICONTROL CPV]* (Audience CTV video campaigns only) Uses the cost-per-view (CPV) model. <!-- Campaigns with this bid strategy aren't optimized when they're included in portfolios. -->

* *[!UICONTROL Enhanced CPC]:* (Campaigns on the audience, search, and shopping networks) Uses the ad network's enhanced cost-per-click (eCPC) model, which allows the ad network to automatically change the cost-per-click (CPC) bid for each auction in an attempt to maximize conversions, using conversions specified within the ad network (not in Search, Social, & Commerce), while trying to keep your average CPC below your maximum CPC. 

  When you add a campaign with eCPC to an optimized Search, Social, & Commerce portfolio, Search, Social, & Commerce optimizes the base bids and &mdash; when the "[!UICONTROL Auto adjust campaign budget limits]" option is enabled &mdash; the campaign budget. The ad network optimizes all bid adjustments and may change the Search, Social, & Commerce-generated bids at the time of the user query based on proprietary data and insights. **Caution:** Use eCPC campaigns in portfolios only when the total conversions tracked on the ad network align with the portfolio objective.

* *[!UICONTROL Manual CPC]*: (Shopping campaigns for brands; [!DNL Microsoft Store Ads] campaigns; deprecated by [!DNL Microsoft® Advertising] in 2021 for other campaign types) Uses the cost-per-click (CPC) model. For some ad types, you can optionally allow the ad network to change bids for the campaign:

  * **[!UICONTROL Enable Enhanced CPC]** (disabled by default): This is the same as using the "[!UICONTROL Enhanced CPC]" option.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] campaigns) Uses the cost per acquisition (CPA) model.

* *[!UICONTROL Manual CPM]* (Audience campaigns and audience video campaigns only) Uses the cost-per-thousand-impressions (CPM) model, for which you specify what you want to spend per 1,000 viewed impressions. Campaigns with this bid strategy aren't optimized when they're included in portfolios.

* *[!UICONTROL Maximize Clicks]:* (Search and shopping campaigns) The ad network &mdash; not Search, Social, & Commerce &mdash; optimizes bids to maximize clicks. Optionally, enter a **[!UICONTROL Max CPC]** (cost per click) to ensure that the ad network doesn't pay more than a specific amount for each click. **Caution:** When you add a campaign with this strategy to a portfolio, bids are driven by click weight, not by the portfolio objective.

* *[!UICONTROL Maximize Conversion Value]:* (Search and shopping/smart shopping networks, performance max campaigns) The ad network &mdash; not Search, Social, & Commerce  &mdash; optimizes bids to maximize conversion value. Optionally enter a **[!UICONTROL Target Return on Ad Spend]** (ROAS) as a percent. **Note:** Use this option for campaigns in hybrid portfolios but not standard portfolios.

* *[!UICONTROL Maximize Conversions]:* (Performance max campaigns and campaigns on the search network or audience network (but not audience videos or connected TV)) The ad network &mdash; not Search, Social, & Commerce &mdash; optimizes bids to maximize conversions. Optionally enter a **[!UICONTROL Target CPC]** (cost per click). For audience campaigns, you can also enter an optional **[!UICONTROL Target CPA]** (cost per acquisition). **Note:** Use this option for campaigns in hybrid portfolios but not standard portfolios.

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

**[!UICONTROL Languages]:** (Performance max campaigns only) The language of the ad, which should match the language of the sites on which your ad will appear. [!DNL Microsoft Advertising] determines a user's language from various signals, including the user's query, the publisher's country, and the user's language setting.

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

## [!UICONTROL Asset Groups] (per asset group)

**[!UICONTROL Asset Group Name]:** The name of the asset folder (asset group).

**[!UICONTROL Asset Group Status]:** The status of the asset group: *[!UICONTROL Active]* or *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** The final URL for all ads created from the asset group.

**[!UICONTROL Images]:** Up to 20 images for the ad, including at least one square image and one landscape image. See the [[!DNL Microsoft Advertising] image guidelines](https://help.ads.microsoft.com/#apex/ads/en/60204/0). You can either upload images or select them from your [!UICONTROL Asset Library] &mdash; but not both in the same operation.

* To upload images:

  1. On the [!UICONTROL Upload from Device] tab, click **[!UICONTROL +]** and select images from your device or network.

  1. For each image:

     1. Select the aspect ratio.
   
     1. Drag and position the crop box as necessary to select the viewable part of the image, and resize the viewable part of the image as necessary when possible.

     1. (Optional) Select additional aspect ratios, and optionally reposition and resize the image as necessary for each selected aspect ratio.
   
        One asset is created for each selected aspect ratio.

     1. Click **[!UICONTROL Proceed]**.

  1. When you're finished specifying images, click **[!UICONTROL Upload]**.

* To select images from your [!UICONTROL Asset Library], click **[!UICONTROL Asset Library]** and select the images.

**[!UICONTROL Logos]:** At least one logo. You can include up to five. See the [[!DNL Microsoft Advertising] asset guidelines](https://help.ads.microsoft.com/#apex/ads/en/60204/0). You can either upload images or select them from your [!UICONTROL Asset Library] &mdash; but not both in the same operation.

* To upload images:

  1. On the [!UICONTROL Upload from Device] tab, click **[!UICONTROL +]** and select images from your device or network.

  1. For each image:

     1. Select the aspect ratio.
   
     1. Drag and position the crop box as necessary to select the viewable part of the image, and resize the viewable part of the image as necessary when possible.

     1. (Optional) Select additional aspect ratios, and optionally reposition and resize the image as necessary for each selected aspect ratio.
   
        One asset is created for each selected aspect ratio.

     1. Click **[!UICONTROL Proceed]**.

  1. When you're finished specifying images, click **[!UICONTROL Upload]**.

* To select images from your [!UICONTROL Asset Library], click **[!UICONTROL Asset Library]** and select the images.
  
**[!UICONTROL Headlines]:** At least three, and up to 15, short headlines with a maximum of 30 characters each. You can either enter text or select assets from your [!UICONTROL Asset Library] &mdash; but not both in the same operation.

* To enter text:

  1. On the [!UICONTROL Enter Text] tab, enter the text.
  
  1. (Optional) To add another text string, click **[!UICONTROL + Add]** and enter the string.

* To select assets from your [!UICONTROL Asset Library], click **[!UICONTROL Asset Library]** and select the assets.

**[!UICONTROL Long Headlines]:** At least one, and up to five, long headlines with a maximum of 90 characters each. You can either enter text or select assets from your [!UICONTROL Asset Library] &mdash; but not both in the same operation.

* To enter text:

  1. On the [!UICONTROL Enter Text] tab, enter the text.
  
  1. (Optional) To add another text string, click **[!UICONTROL + Add]** and enter the string.

* To select assets from your [!UICONTROL Asset Library], click **[!UICONTROL Asset Library]** and select the assets.

**[!UICONTROL Descriptions]:** At least two, and up to five, descriptions with a maximum of 90 characters each. You can either enter text or select assets from your [!UICONTROL Asset Library] &mdash; but not both in the same operation.

* To enter text:

  1. On the [!UICONTROL Enter Text] tab, enter the text.
  
  1. (Optional) To add another text string, click **[!UICONTROL + Add]** and enter the string.

* To select assets from your [!UICONTROL Asset Library], click **[!UICONTROL Asset Library]** and select the assets.

**[!UICONTROL Call to Action]:** The call to action to include in the ad. By default, *[!UICONTROL Act Now]* is selected.

**[!UICONTROL Business Name]:** The business name, with a maximum of 25 characters. It can't contain scripts, HTML, or other markup language.

**[!UICONTROL Audience Signal]:** (Optional) [!DNL Microsoft Advertising] audiences to use as audience signals for the campaign. [!DNL Microsoft Advertising] machine learning models use the audiences to find similar web surfers to target and may also show ads to audiences that aren’t specified as signals to help you meet your performance goals. Choose audiences that are most likely to convert.

>[!NOTE]
>Audience signals are different from [ad group-level audience targets](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:** Allows you to specify another asset group.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Whether to *[!UICONTROL Use account conversion goals for this campaign]* (the default) or *[!UICONTROL Use campaign specific conversion goals]*. If you choose to specify conversion goals for the campaign, then select the goals from the list of all available goals. **Note:** Goals are synchronized daily, so goals created in the previous 24 hours may not be listed. To update the list, [manually synchronize the ad network data](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

If the campaign is part of a portfolio, then use the same conversion goals as the portfolio's objective. Using different conversion goals may impact portfolio performance.

>[!MORELIKETHIS]
>
>* [Manage campaigns](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
