---
title: '[!DNL Google Ads] campaign settings'
description: Reference the settings for [!DNL Google Ads] campaigns.
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
---
# [!DNL Google Ads] campaign settings

## \[Campaign Creation screen\]

**[!UICONTROL Campaign Type]:** (Available during campaign creation only) Where to place ads, and which ad types
the campaign may contain:

* *[!UICONTROL Search Network Only]:* Shows ads on the search network, which includes [!DNL Google] search results and, optionally, search partner sites. You must specify keywords for each ad group.

* *[!UICONTROL Search with Display Select]:* Shows ads on the search network (which includes [!DNL Google] search results and, optionally, search partner sites) and potentially shows ads on display network sites. On the display network, [!DNL Google Ads] displays your ads selectively using automated bidding, regardless of the campaign's bid strategy. For search ads, specify keywords for each ad group; for display ads, specify placements and optionally specify keywords for each ad group.

* *[!UICONTROL Shopping Network]:* Shows product ads, which [!DNL Google] generates automatically based on your products in [!DNL Google Merchant Center] on [!DNL Google Shopping], the area next to [!DNL Google] search results (separate from text ads), and (optionally) search partner websites. For each ad group in the campaign, you can specify product groups to advertise.

* *[!UICONTROL Display Network Only]:* Shows ads on the display network. For each ad group, you must specify placements and can optionally specify keywords.

* *[!UICONTROL Performance Max]:* (Beta feature) Shows and optimizes conversions for your ads across channels using [!DNL Google Ads] smart bidding. Within the campaign settings, you must specify one or more asset groups, which include images, logos, headlines, descriptions, optional videos, and audience signals. [!DNL Google Ads] automatically combines the assets to serve ads based on the channel (such as [!DNL YouTube], [!DNL Gmail], or [!DNL Search]).

  **Notes:**
  
  * Only required settings are available. For optional settings, log in to the [!DNL Google Ads] editor.
  
  * Links to [!DNL Google Merchant Center] product feeds aren't supported.
  
  * Support for listing groups isn't available. To manage and view data for listing groups, log in to the [!DNL Google Ads] editor.

  * Hybrid optimization is supported. Bid strategy targets and campaign budgets are set at the campaign level.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** A campaign name that is unique within the account.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**(Existing, read-only Gmail campaigns only) Whether to:

* *[!UICONTROL Target and Bid]* To show ads only to users associated with target audiences who also satisfy any other targets for the ad group.

* *[!UICONTROL Bid Only]:*  To show ads even to people who aren't associated with target audiences as long as they satisfy other ad group-level targets. You may increase the chances that ads are shown to specific audiences, however, by setting higher bids for those audiences.

**[!UICONTROL Status]:** The display status of the campaign: *Active* or *Paused*. The default for new ad campaigns is *Active*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Campaigns that target the search network only, including shopping campaigns) Shows
your ads on the ad network's search partner networks. By default, this option is *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** The bid strategy for the campaign:

* *[!UICONTROL Enhanced CPC]:* (Not available for performance max or existing, read-only [!DNL Gmail] campaigns) Uses the ad network's enhanced cost-per-click (eCPC) model, which allows the ad network to automatically change the cost-per-click (CPC) bid for each auction in an attempt to maximize conversions, using conversion(s) specified within the ad network (not in Search, Social, & Commerce), while trying to keep your average CPC below your maximum CPC. 

When you add a campaign with eCPC to an optimized Search, Social, & Commerce portfolio, Search, Social, & Commerce optimizes the base bids and &mdash; when the "[!UICONTROL Auto adjust campaign budget limits]" option is enabled &mdash; the campaign budget. The ad network optimizes all bid adjustments and may change the Search, Social, & Commerce-generated bids at the time of the user query based on proprietary data and insights. **Caution:** Use eCPC campaigns in portfolios only when the total conversions tracked on the ad network align with the portfolio objective. <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* (the default): (Not available for performance max campaigns) Uses the cost-per-click (CPC) model. You can optionally allow the ad network to change bids for the campaign:

  * **[!UICONTROL Enable Enhanced CPC]** (disabled by default): This is the same as using the "[!UICONTROL Enhanced CPC]" option.

* *[!UICONTROL Maximize Clicks]:* (Search, display, and shopping campaigns) The ad network &mdash; not Search, Social, & Commerce &mdash; optimizes bids to maximize clicks. Optionally, enter a **[!UICONTROL Max CPC]** (cost per click) to ensure that the ad network doesn't pay more than a specific amount for each click. **Caution:** When you add a campaign with this strategy to a portfolio, bids are driven by click weight, not by the portfolio objective.

* *[!UICONTROL Maximize Conversion Value]:* (Search, performance max, and smart shopping campaigns) The ad network &mdash; not Search, Social, & Commerce  &mdash;optimizes bids to maximize conversion value. Optionally enter a **[!UICONTROL Target Return on Ad Spend]** (ROAS) as a percentage. **Note:** Use this option for campaigns in hybrid portfolios but not standard portfolios.

* *[!UICONTROL Maximize Conversions]:* (Search, display, and performance max campaigns) The ad network &mdash; not Search, Social, & Commerce &mdash; optimizes bids to maximize conversions. Optionally enter a **[!UICONTROL Target CPA]** (cost per acquisition). **Note:** Use this option for campaigns in hybrid portfolios but not standard portfolios.

* *[!UICONTROL Target CPA]:* (Display campaigns; existing search campaigns) The ad network &mdash; not Search, Social, & Commerce &mdash; optimizes bids based on an optional **[!UICONTROL Target CPA]** (cost per acquisition), which is the 30-day average amount you want to pay for an acquisition (conversion). **Note:** Use this option for campaigns in hybrid portfolios (but not standard portfolios) with any spend strategy except [!UICONTROL Weekly] or [!UICONTROL Google Target CPA].

  Average position and CPC bid data aren't available for campaigns with this bid strategy.

  For new search campaigns, [!DNL Google Ads] has replaced this bid strategy with the [!UICONTROL Maximize Conversions] strategy using a [!UICONTROL Target CPA] value. For existing search campaigns with this strategy, you can edit only the target value, and doing so changes the strategy to the [!UICONTROL Maximize Conversions] strategy using the specified [!UICONTROL Target CPA] value.

* *[!UICONTROL Target Impression Share]:* (Search campaigns) The ad network &mdash; not Search, Social, & Commerce &mdash; optimizes bids to achieve a target impression share and ad position. Optionally, enter a **[!UICONTROL Target Impression Share]** as a percentage, the **[!UICONTROL Target Ad Position]**, and a **[!UICONTROL Max CPC]** (cost per click). **Note:** This option isn't supported in portfolios.

* *[!UICONTROL Target Return on Ad Spend]:*  (Display and shopping campaigns; existing search campaigns) The ad network &mdash; not Search, Social, & Commerce &mdash; optimizes bids based on a specified **[!UICONTROL Target ROAS]** (return on ad spend), specified as a percentage. **Note:** Use this option for campaigns in hybrid portfolios (but not standard portfolios) with any spend strategy except [!UICONTROL Weekly] or [!UICONTROL Google Target ROAS].

  Average position and CPC bid data aren't available for campaigns with this bid strategy.

  For new search campaigns, [!DNL Google Ads] has replaced this bid strategy with the [!UICONTROL Maximize Conversion Value] strategy using a [!UICONTROL Target Return on Ad Spend value]. For existing search campaigns with this strategy, you can edit only the target value, and doing so changes the strategy to the [!UICONTROL Maximize Conversion Value] strategy using the specified [!UICONTROL Target Return on Ad Spend] value.

* *[!UICONTROL Viewable CPM]:* (Existing, read-only [!DNL Gmail] campaigns only) The ad network &mdash; not Search, Social, & Commerce &mdash; bids only on ads that are measured as viewable. **Note:** Optimization for this strategy isn't supported in any type of portfolio.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Shopping campaigns only; read-only for existing campaigns) The country in which
the campaign's products are sold. Because products are associated with target countries, this setting determines which products are advertised in the campaign.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Shopping campaigns only; advertisers already participating in the local shopping program with [!DNL Google Merchant Center] stores in the US, UK, DE, FR, JP and AU; optional) Allows [!DNL Google Ads] to automatically add your local inventory information to your shopping ads on Google.com. 

**Tip:** If you use this setting, don't exclude local ads in the [!UICONTROL Inventory Filter] setting.

**Note:** Local inventory ads require two additional feeds to [!DNL Google Merchant Center] &mdash; one with your local product data and another with your local product inventory. See the [!DNL Google Ads] documentation for more information about [local shopping ads](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Search and display networks only) One or more target languages for ads in the campaign.

[!DNL Google Ads] determines a user's language from the user's [!DNL Google] language setting or the language of the search query, the current page, or recently viewed pages on the [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** Specific user geographical locations to include or exclude as targets. By default, all locations are targeted. You can include and exclude users in any combination of locations. Exclusions always override inclusions.

* To target all locations, don't select any locations.

* To target or exclude specific locations:

  * (Countries, states, metropolitan regions, or cities) Click **[!UICONTROL Location Target]** (![Location Target](/help/search-social-commerce/assets/location-target.png "Location Target")) and locate the locations to include and exclude:

    * To include a location and its child locations, click the circle next to it once so that a blue checkmark (![Include](/help/search-social-commerce/assets/include.png "Include")) appears.
    
    * To exclude a location, click the circle next to it twice so that a red checkmark (![Exclude](/help/search-social-commerce/assets/exclude.png "Exclude")) appears.
    
    * To expand a location into its subcomponents (such as the states, metropolitan regions, or cities in the U.S.), click the location name.
    
    * To search for a location, enter or paste at least the first three characters of the location in the input field. In the search results, click **[!UICONTROL Include]** next to a location to include or **[!UICONTROL Exclude]** next to a location to exclude.

  * (Locations near an address; included targets only) Click **[!UICONTROL Radius Target]** (![Radius Target](/help/search-social-commerce/assets/radius-target.png "Radius Target")), and then click **[!UICONTROL Address]**. Enter the address and the radius in miles or kilometers around the address to target, and then click **[!UICONTROL Add]**.
  
  * (Locations near geographic coordinates; included targets only) Click **[!UICONTROL Radius Target]** (![Radius Target](/help/search-social-commerce/assets/radius-target.png "Radius Target")), and then click **[!UICONTROL Coordinate]**. Enter the latitude and longitude and the radius in miles or kilometers around the location to target, and then click **[!UICONTROL Add]**.

* (To add a bid adjustment for an included target location) Enter a bid adjustment value:

* 0%: To not adjust bids for ads in this location.

* \[Other values from -90% to 300%\]: To increase or decrease the bid for ads in this location.

**Note:**

* Search, Social, & Commerce doesn't provide auto-adjusted bid adjustments for the following location targets because of limitations in the data that [!DNL Google Ads] provides for mapping surfer locations to location targets:

  * Radius targets.
  
  * Some locations below the state/province/region/county/prefecture level for which [!DNL Google Ads] doesn't send a parent location in the surfer's URL, including airports and U.S. congressional districts.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Display network only) Specific mobile carriers to target; the carriers are sorted
by country. If you don't select any, all are targeted.

**[!UICONTROL Mobile Carriers]:** (Display network only) Specific operating systems to target. If you don't select any, all are targeted.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

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

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

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

**[!UICONTROL Asset Group Name]:** The name of the asset group. Links to [!DNL Google Merchant Center] product feeds aren't supported.

**[!UICONTROL Asset Group Status]:** The status of the asset group: *[!UICONTROL Active]* or *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** The final URL for all ads created from the asset group. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Up to 15 images for the ad, including the following sizes: 1) at least three square images, 2) at least three landscape images, and 3) at least one portrait image. See the [[!DNL Google Ads] image specifications](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). You can either upload images or select them from your [!UICONTROL Asset Library] &mdash; but not both in the same operation.

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

**[!UICONTROL Logos]:** At least one square (1:1) logo and one landscape (4:1) logo. You can include up to five of each size. See the [[!DNL Google Ads] logo specifications](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). You can either upload images or select them from your [!UICONTROL Asset Library] &mdash; but not both in the same operation.

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

**[!UICONTROL Videos]:** (Optional) At least one, and up to five, [!DNL YouTube] videos that are at least 10 seconds long. You can either enter URLs or select them from your [!UICONTROL Asset Library] &mdash; but not both in the same operation.

* To enter URLs:

  1. On the [!UICONTROL Enter Video Url] tab, enter an URL.
  
  1. (Optional) To add another URL, click **[!UICONTROL + Add]** and enter the URL.

* To select videos from your [!UICONTROL Asset Library], click **[!UICONTROL Asset Library]** and select the videos.
  
**[!UICONTROL Headlines]:** At least three, and up to five, short headlines with a maximum of 30 characters each. At least one headline must be at least 15 characters or less. If the campaign-level option to enable final URL expansion is set within [!DNL Google Ads], then [!DNL Google Ads] replaces this value with a custom headline based on the landing page content.

 You can either enter text or select assets from your [!UICONTROL Asset Library] &mdash; but not both in the same operation.

* To enter text:

  1. On the [!UICONTROL Enter Text] tab, enter the text.
  
  1. (Optional) To add another text string, click **[!UICONTROL + Add]** and enter the string.

* To select assets from your [!UICONTROL Asset Library], click **[!UICONTROL Asset Library]** and select the assets.

**[!UICONTROL Long Headlines]:** At least one, and up to five, long headlines with a maximum of 90 characters each. You can either enter text or select assets from your [!UICONTROL Asset Library] &mdash; but not both in the same operation.

* To enter text:

  1. On the [!UICONTROL Enter Text] tab, enter the text.
  
  1. (Optional) To add another text string, click **[!UICONTROL + Add]** and enter the string.

* To select assets from your [!UICONTROL Asset Library], click **[!UICONTROL Asset Library]** and select the assets.

**[!UICONTROL Descriptions]:** At least two, and up to four, descriptions with a maximum of 90 characters each. At least one description must be at least 30 characters or less. You can either enter text or select assets from your [!UICONTROL Asset Library] &mdash; but not both in the same operation.

* To enter text:

  1. On the [!UICONTROL Enter Text] tab, enter the text.
  
  1. (Optional) To add another text string, click **[!UICONTROL + Add]** and enter the string.

* To select assets from your [!UICONTROL Asset Library], click **[!UICONTROL Asset Library]** and select the assets.

**[!UICONTROL Call to Action]:** The call to action to include in the ad. By default, *[!UICONTROL Automated]* is selected, and [!DNL Google Ads] selects the call to action. You can optionally choose a different action.

**[!UICONTROL Business Name]:** The business name, with a maximum of 25 characters.

**[!UICONTROL Audience Signal]:** (Optional) [!DNL Google Ads] audiences to use as audience signals for the campaign. [!DNL Google Ads] machine learning models use the audiences to find similar web surfers to target and may also show ads to audiences that aren't specified as signals to help you meet your performance goals. Choose audiences that are most likely to convert.

>[!NOTE]
>Audience signals are different from [campaign-level and ad group-level audience targets](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Add new asset group]:** Allows you to specify another asset group.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Whether to *[!UICONTROL Use account conversion goals for this campaign]* (the default) or *[!UICONTROL Use campaign specific conversion goals]*. If you choose to specify conversion goals for the campaign, then select standard goals and/or create a custom goal for the campaign.

Goals are synchronized daily, so existing goals created in the previous 24 hours may not be listed. To update the list, [manually synchronize the ad network data](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

To create a custom conversion goal, click **[!UICONTROL + Add custom goal]**, enter the custom goal name, select the [conversion actions](https://support.google.com/google-ads/answer/6032150) to include in the custom goal, and then click **[!UICONTROL Save]**. **Note:** Each campaign can have only one custom goal.

>[!TIP]
>
>If the campaign is part of a hybrid portfolio, then use the same conversion goals as the portfolio's objective. Using different conversion goals may impact portfolio performance.

>[!MORELIKETHIS]
>
>* [Manage campaigns](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)

