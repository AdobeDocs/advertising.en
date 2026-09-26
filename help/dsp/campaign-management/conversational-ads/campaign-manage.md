---
title: Manage [!DNL ChatGPT] conversational ad campaigns
description: Learn how to create and manage [!DNL ChatGPT] campaigns, ad groups, and conversational ads, a beta feature that places ads inside AI assistant conversations.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Manage [!DNL ChatGPT] conversational ad campaigns

*Beta feature*

Manage [!DNL ChatGPT] campaigns, ad groups, and ads within a [conversational ads account](account-manage.md).

## About the [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns] view {#campaign-views-about}

The [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns] view includes three tabs: [!UICONTROL Campaigns], [!UICONTROL Ad Groups], and [!UICONTROL Ads]. Each tab lists the campaigns, ad groups, or ads for the selected account, along with performance data for the selected date range.

### Available actions

* [Create](#campaign-create) or [edit](#campaign-edit) a campaign

* [Create](#ad-group-create) or [edit](#ad-group-edit) an ad group for an existing campaign

* [Create](#ad-create) or [edit](#ad-edit) an ad for an existing ad group

* [Activate or pause a campaign, ad group, or ad](#pause-activate)

* [Archive a campaign, ad group, or ad](#archive)

* [Navigate between campaigns, ad groups, and ads](#drill-down)

## Campaigns

### Create a [!DNL ChatGPT] conversational ad campaign {#campaign-create}

When you create a campaign, you can optionally create its first ad group and ad. Each step creates that entity as soon as you click **[!UICONTROL Next]**, so you can't go back to a previous step&mdash;if you need to change something afterward, edit it once the wizard is closed.

1. In the main menu, click **[!UICONTROL Conversational Ads Beta]**.

1. In the submenu, click the **[!UICONTROL Campaigns]** tab.

1. In the upper right, select an advertiser and a [!DNL ChatGPT] account.

1. In the upper right, click **[!UICONTROL Create] > [!UICONTROL Campaign]**.

1. Specify the [campaign settings](#campaign-settings).

1. Click **[!UICONTROL Next]** to save the campaign settings.

1. Do any of the following:

   * If you don't want to create an ad group for the campaign, then click **[!UICONTROL Close]**.

     >[!TIP]
     >
     >To create an ad group or ad later, see "[Create an ad group](#ad-group-create)" or "[Create an ad](#ad-create)."

   * (Optional) Create an ad group:
   
     1. Specify the [ad group settings](#ad-group-settings).
     
     1. Click **[!UICONTROL Next]** to save the ad group settings.

     1. (Optional) If you don't want to create an ad for the campaign, then click **[!UICONTROL Close]**.

   * (Optional after you've created an ad group) Create an ad:

     1. Specify the [ad settings](#ad-settings).
     
     1. Click **[!UICONTROL Create ad]**.

### Edit [!DNL ChatGPT] conversational ad campaign settings {#campaign-edit}

1. In the main menu, click **[!UICONTROL Conversational Ads Beta]**.

1. In the submenu on the left, click **[!UICONTROL Campaigns]**.

1. In the upper right, select an advertiser and a [!DNL ChatGPT] account.

1. (If necessary) Above the data table, click the **[!UICONTROL Campaigns]** tab.

1. Hold the cursor over the row and click **[!UICONTROL ...] > [!UICONTROL Edit]**.

1. Edit any of the [campaign settings](#campaign-settings), [ad group settings](#ad-group-settings), and [ad settings](#ad-settings).

1. Click **[!UICONTROL Save]**.

### [!DNL ChatGPT] conversational ad campaign settings {#campaign-settings}

**[!UICONTROL Campaign name]:** A unique name for the campaign. The name must include at least three characters.

**[!UICONTROL Campaign type]:** (Read-only) *Standard* is the only available type.

**[!UICONTROL Objective]:** The metric on which to focus the campaign: *Reach* or *Clicks*. The objective determines the bid type for the campaign's ad groups.

**[!UICONTROL Locations]:** (Optional) One or more specific locations to target. To target all locations, leave this setting empty. To specify a specific location, enter at least two letters that appear anywhere within the name, and then click the name within the search results.

**[!UICONTROL Budget type]:** *Daily budget* or *Lifetime budget*.

**[!UICONTROL Budget]:** The budget for the specified budget type. The value must be greater than zero (0).

**[!UICONTROL Start date]:** The date the campaign starts, in the account's timezone.

**[!UICONTROL Set an end date]:** (Optional) Allows you to specify an end date for the campaign. When you select this option, specify the **[!UICONTROL End date]**.

## Ad groups

### Create a [!DNL ChatGPT] ad group for an existing campaign {#ad-group-create}

1. In the main menu, click **[!UICONTROL Conversational Ads Beta]**.

1. In the submenu, click the **[!UICONTROL Campaigns]** tab.

1. In the upper right, select an advertiser and a [!DNL ChatGPT] account.

1. In the upper right, click **[!UICONTROL Create] > [!UICONTROL Ad Group]**.

1. Specify the [ad group settings](#ad-group-settings), including the parent campaign.

1. Click **[!UICONTROL Create ad group]**.

## Edit a [!DNL ChatGPT] ad group {#ad-group-edit}

1. In the main menu, click **[!UICONTROL Conversational Ads Beta]**.

1. In the submenu on the left, click **[!UICONTROL Campaigns]**.

1. In the upper right, select an advertiser and a [!DNL ChatGPT] account.

1. Above the data table, click the **[!UICONTROL Ad Groups]** tab.

1. Hold the cursor over the row and click **[!UICONTROL ...] > [!UICONTROL Edit]**.

1. Edit the [ad group](#ad-group-settings) settings.

1. Click **[!UICONTROL Save]**.

### [!DNL ChatGPT] ad group settings {#ad-group-settings}

**[!UICONTROL Parent campaign]:** (Ad groups for existing campaigns only) The campaign to which the ad group belongs.

**[!UICONTROL Ad group name]:** A unique name for the ad group. The name must include at least three characters.

**[!UICONTROL Maximum CPC bid]** or **[!UICONTROL Maximum CPM bid]:** The maximum amount you'll pay for each click or for 1,000 impressions. The value must be greater than zero (0). The campaign's objective determines the bid field: *Clicks* campaigns show **[!UICONTROL Maximum CPC bid]**, and *Reach* campaigns show **[!UICONTROL Maximum CPM bid]**.

>[!TIP]
>
>Higher bids may win more auctions.

**[!UICONTROL Context hints]:** (Optional) A description of the conversations, topics, or keywords for which your products or services are relevant. These hints guide matching but aren't exact-match targeting rules.

## Ads

### Create a [!DNL ChatGPT] ad for an existing ad group {#ad-create}

1. In the main menu, click **[!UICONTROL Conversational Ads Beta]**.

1. In the submenu, click the **[!UICONTROL Campaigns]** tab.

1. In the upper right, select an advertiser and a [!DNL ChatGPT] account.

1. In the upper right, click **[!UICONTROL Create] > [!UICONTROL Ad]**.

1. Specify the [ad settings](#ad-settings), including the parent campaign and ad group.

1. Click **[!UICONTROL Create ad]**.

## Edit a [!DNL ChatGPT] ad {#ad-edit}

1. In the main menu, click **[!UICONTROL Conversational Ads Beta]**.

1. In the submenu on the left, click **[!UICONTROL Campaigns]**.

1. In the upper right, select an advertiser and a [!DNL ChatGPT] account.

1. Above the data table, click the **[!UICONTROL Ads]** tab.

1. Hold the cursor over the row and click **[!UICONTROL ...] > [!UICONTROL Edit]**.

1. Edit the [ad](#ad-settings) settings.

1. Click **[!UICONTROL Save]**.

### [!DNL ChatGPT] ad settings {#ad-settings}

**[!UICONTROL Parent campaign]** and **[!UICONTROL Parent ad group]:** (Ads in existing ad groups only) The campaign and ad group to which the ad belongs.

**[!UICONTROL Ad name]:** A unique name for the ad. The name must include at least three characters.

**[!UICONTROL Ad URL (Link)]:** The landing page URL, starting with `http://` or `https://`.

**[!UICONTROL Title (headline)]:** The ad headline. The title must be between 3-50 characters. **Note:** The title may be truncated in some placement types.

**[!UICONTROL Description]:** The body text of the ad. The description must be between 3-100 characters.

**[!UICONTROL Ad image]:** A JPG or PNG image to include in the ad. To upload an image, click (new ads) **[!UICONTROL Upload image (PNG/JPG)]** or **[!UICONTROL Change image]**, and then locate and select a file on your device or network.

**[!UICONTROL Preview]:** A preview of the ad, based on the ad settings.

## Activate or pause a [!DNL ChatGPT] campaign, ad group, or ad {#pause-activate}

1. In the main menu, click **[!UICONTROL Conversational Ads Beta]**.

1. In the submenu on the left, click **[!UICONTROL Campaigns]**.

1. In the upper right, select an advertiser and a [!DNL ChatGPT] account.

1. On the **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, or **[!UICONTROL Ads]** tab, find the row.

1. In the **[!UICONTROL Active]** column, do one of the following:

   * To activate a paused item, turn on the toggle (to the right).

   * To pause an active item, turn off the toggle (to the left).

## Archive a [!DNL ChatGPT] campaign, ad group, or ad {#archive}

Archiving permanently removes the campaign, ad group, or ad from the [!UICONTROL Conversational Ads] views.

1. In the main menu, click **[!UICONTROL Conversational Ads Beta]**.

1. In the submenu on the left, click **[!UICONTROL Campaigns]**.

1. In the upper right, select an advertiser and a [!DNL ChatGPT] account.

1. On the **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, or **[!UICONTROL Ads]** tab, hold the cursor over the row and click **[!UICONTROL ...] > [!UICONTROL Archive]**.

## Navigate between [!DNL ChatGPT] campaigns, ad groups, and ads {#drill-down}

* Click a campaign row to view only its ad groups on the **[!UICONTROL Ad Groups]** tab, or click an ad group row to view only its ads on the **[!UICONTROL Ads]** tab.

To remove the filter and see all rows in the view, click **X** in the filter above the data table.

>[!MORELIKETHIS]
>
>* [Manage conversational ad accounts](account-manage.md)
