---
title: Manage [!DNL Google Ads] dynamic search targets
description: Learn how to create and manage [!DNL Google Ads] dynamic search targets.
exl-id: 85b1455a-dda1-4bb9-b4be-d6e0a837fd9d
feature: Search Campaign Management
---
# Manage [!DNL Google Ads] dynamic search targets

*[!DNL Google Ads] accounts only*

You can create, edit, and change the status of dynamic search targets for campaigns that use the search network.

>[!NOTE]
>
>You can create and edit large amounts of target data at once by uploading [bulksheet files](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) and posting them to the ad network.

## Create a [!DNL Google Ads] dynamic search target

You can create dynamic search targets to define pages in your websites (that is, the domains used in your ads' display URLs) whose content is used to target your dynamic search ads in the same ad group.

You can target all criteria or up to three individual criteria.

>[!NOTE]
>
>To best track performance, create an "[!UICONTROL All Targets]" target for only one ad group per campaign.

>[!TIP]
>
>To create many account components at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network, the account, the campaign, and the ad group, and then click **[!UICONTROL Continue]**.

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

1. Click **[!UICONTROL Post]**.

## Edit [!DNL Google Ads] dynamic search target settings

You can edit the status or maximum bid for a [!DNL Google Ads] dynamic search target. You can't change the criteria that are targeted.

>[!TIP]
>
>To edit large amounts of data at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each row to edit.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

   For multiple targets, your changes are applied to all of the selected targets. For the [!UICONTROL Bid field], you have options to change existing values to a specified value or to either increase or decrease the amount by a specified percentage or monetary amount, with a limit.

1. Save the data:

   * (Single targets) Click **[!UICONTROL Post]**.
   
   * (Multiple ad groups) Click **[!UICONTROL Post Now]**.

## Change the status of [!DNL Google Ads] dynamic search targets

You can pause any active dynamic search target in a supported campaign type to stop using them for dynamic search ads in the same ad group. You can later use them as targets by changing the ad status back to active.

You can also delete any dynamic target.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. (Optional) Filter the list to include specific dynamic targets.

1. Do either of the following:
   
   * To change the status of one dynamic target, click in the **[!UICONTROL Status]** column and change the status.
   
   * To delete one or more dynamic targets, do the following:
   
     1.  Select the check box next to each dynamic target you want to delete.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."
     
     1. In the toolbar, click ![More](/help/search-social-commerce/assets/more.png "More") and select **[!UICONTROL Delete]**.
     
     1. In the confirmation message, click **[!UICONTROL Delete]**.

## [!DNL Google Ads] dynamic search target settings {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Required when you don't specify a website domain and language in the campaign's [!UICONTROL DSA Options] section; read-only for existing targets) Dynamic search targets for the ad group:

* *[!UICONTROL All Targets]* (the default): Targets all indexed pages.

* *\[Specific Targets\]:* Targets up to three criteria for the indexed pages. When you select this, you must specify the criteria by specifying information categories and specific values for which to target ads (for example, "URL contains shoes.example.com"). To specify more than one criteria, click **[!UICONTROL + And]**. Target criteria include:

  * *[!UICONTROL Category]:* To show ads for indexed pages with a specific [!DNL Google Ads] content category.

  * *[!UICONTROL URL]:* To show ads for indexed pages with a specific URL, where the value may be included anywhere within the URL.

  * *[!UICONTROL Page Title]:* To show ads for indexed pages with specific text in the page title.

  * *[!UICONTROL Page Content]:* To show ads for indexed pages with specific content.

**Status:** The status of the target settings:

* *[!UICONTROL Active]* (the default): Enables bidding.

* *[!UICONTROL Paused]:* Disables bidding.

* *[!UICONTROL Deleted]* (existing targets only): Deletes the target settings.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** The maximum cost per click (CPC) for an ad or cost per 1000 impressions (CPM) for an ad, as applicable for the ad network and campaign pricing model. This value overrides the ad group-level value.

>[!NOTE]
>
>If the target is in an optimized portfolio, then the specified CPC bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations.
 
>[!MORELIKETHIS]
>
>* [About [!DNL Google Ads] dynamic search targets](dynamic-search-target-about.md)
