---
title: "[!DNL OpenAI Ads] campaign settings"
description: Reference the settings for [!DNL OpenAI Ads] campaigns.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
---
# [!DNL OpenAI Ads] campaign settings

<!-- EDIT ALL AS NEEDED -->

<!-- Can create, edit, and delete. Possibly not all of the other procedures available to campaigns on the other SEs. -->

## [!UICONTROL Basic Settings] tab

*New campaigns only*

**[!UICONTROL Network]:** The ad network.

**[!UICONTROL Account]:** The ad network account.

<!-- VERIFY -->**[!UICONTROL Campaign Type]:** Where to place ads: the only option is *[!UICONTROL Standard]* to display ads in [!DNL ChatGPT].

## [!UICONTROL Campaign Details] tab

**[!UICONTROL Campaign Name]:** A campaign name that's unique within the account.

**[!UICONTROL Status]:** The display status of the campaign: *Active* or *Paused*. The default for new ad campaigns is *Active*.

<!-- I don't see Conversions, which is required for the "Conversion events" field that appears below. Verify the options here. Reach=CPM, Clicks=CPC -->**[!UICONTROL Objective]:** The campaign objective: *Reach* or *Clicks*.

**[!UICONTROL Location Targets]:** Specific user geographical locations to include as targets. By default, all locations are targeted. You can include (but not exclude) users in any combination of locations.

* To target all locations, don't select any locations.

* To include a location and its child locations, click the adjacent circle.

* To expand a location into its subcomponents (such as the regions, territories, or cities), click the location name.

* To search for a location, enter or paste at least the first three characters of the location in the input field.

**[!UICONTROL Budget Type]:** The type of campaign budget: *Daily budget* or *Lifetime*.

**[!UICONTROL Budget]:** The budget for the specified campaign type.

<!-- Should this be here? I don't see the Conversions objectives (conversion-optimized cost-per-click campaigns) available above, and it's required for this field -->**[!UICONTROL Conversion events]:** (Campaigns with the objective "[!UICONTROL Conversions]" ) The conversion events 

>[!MORELIKETHIS]
>
>* [Manage campaigns](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
