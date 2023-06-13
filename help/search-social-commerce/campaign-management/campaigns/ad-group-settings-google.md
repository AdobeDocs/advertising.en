---
title: '[!DNL Google Ads] ad group settings'
description: Reference the settings for [!DNL Google Ads] ad groups.
exl-id: 00aaa936-796f-4e22-9bee-4bb5121cd887
---
# [!DNL Google Ads] ad group settings

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** An ad group name that is unique within the campaign. The maximum length is 255 double-byte characters.

**[!UICONTROL Status]:** The display status of the ad group: *Active* or *Paused*. The default for new ad groups is *Active*.

**[!UICONTROL Ad Group Type]:** (Expanded dynamic search ad campaigns only) The type of ad group:

* *[!UICONTROL Search Standard]* (the default): For standard ads.

* *[!UICONTROL Search Dynamic]:* For dynamic search ads.

**[!UICONTROL Ad Rotation Mode]:** How often [!DNL Google Ads] delivers your active ads in relation to one another within the ad group:

* *[!UICONTROL Optimize]:* Google Ads favors ads that it expects to perform better than other ads in the ad group. These ads enter the ad auction more often, and over time a single ad is favored. This may be inconsistent with your business and optimization objectives.

* *[!UICONTROL Rotate forever]:*   Each of your ads enters the ad auction a more even number of times, which allows Search, Social, & Commerce to score your ads not only on click-through rate but also on conversions.

* *[!UICONTROL Use campaign setting]*(the default for new ad groups): Uses the existing campaign-level ad rotation setting. **Note:** The campaign-level setting isn't visible in Search, Social, & Commerce.

If the campaign uses a Smart Bidding bid strategy (such as [!UICONTROL Target CPA], [!UICONTROL Target ROAS], or [!UICONTROL Enhanced CPC]), then [!DNL Google Ads] automatically sets the option to "[!UICONTROL Optimize]."

**[!UICONTROL Custom Bid Level]:** (Campaigns that target the display network only) How to bid: by *[!UICONTROL Ad Group]* (the default), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Interests & Remarketing in Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (website), *[!UICONTROL Unknown]*, or *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* When you bid by keyword, create tracking templates at the keyword level. Similarly, when you bid by placement, create tracking templates at the placement level. For all other dimensions, create tracking templates at the ad level.
>* When you bid by Age, Gender, Interest and List, or Vertical for campaigns in portfolios, the optimization capability doesn't optimize bids for the dimension. Also, all attribution is applied to the ad group.
>* Ads on the search network always use keyword bids.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (Campaigns with [!UICONTROL Target CPA] bidding; optional) The target cost per acquisition (CPA) for the ad group. This value overrides the campaign-level target.

**[!UICONTROL Target ROAS]:** (Campaigns with [!UICONTROL Target ROAS] bidding; optional) The target return on ad spend (ROAS) for the ad group, as a percentage. This value overrides the campaign-level target.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Campaigns on only the search network, and existing, read-only [!DNL Gmail] campaigns on the display network) Whether to:

* *[!UICONTROL Target and Bid]:* To show ads only to users associated with target audiences who also satisfy any other targets for the ad group.

* *[!UICONTROL Bid Only]:* To show ads even to people who aren't associated with target audiences as long as they satisfy other ad group-level targets. You can increase the chances that ads are shown to specific audiences, however, by setting higher bids for those audiences.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

>[!MORELIKETHIS]
>
>* [Manage ad groups](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
