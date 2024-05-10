---
title: Manage audience targets for campaigns and ad groups
description: Learn how to configure and manage audience targets for your [!DNL Google Ads] and [!DNL Microsoft Advertising] campaigns and ad groups.
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
---
# Manage audience targets for your [!DNL Google Ads] and [!DNL Microsoft Advertising] campaigns and ad groups

*[!DNL Google Ads] and [!DNL Microsoft Advertising] only*

[!DNL Google Ads] campaigns and ad groups, and [!DNL Microsoft Advertising] ad groups, can target specific audiences from the same ad network. The ad network determines how large an audience must be to be targetable.

>[!NOTE]
>
>Exclusions always override inclusions/targets.

You can configure audience targets, edit the bid modifiers for audience targets, and change the status of audience targets.

## Configure audience targets

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Audiences] > [!UICONTROL Targets]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network and the account name, and then click **[!UICONTROL Continue]**.

1. Configure the audience targets for specific campaigns and ad groups:

   1. Select the applicable audiences for the specified ad network.
   
      You can optionally search for audiences that contain a specific text string with a minimum of three characters. For any matching audience, click **[!UICONTROL Include]** to select it.
      
      [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

   1. Specify the targets:
   
      1. (Optional) To expand a campaign its child ad groups, click the campaign name.
      
      1. (Optional) To filter a campaign list or ad group list by a text string included in the name, click ![Filter](/help/search-social-commerce/assets/filter.png "Filter") , either enter or paste the text string into the input field, and then press the **[!UICONTROL Enter]** key.
      
      1. Specify each campaign and ad group target for the specified ad network by clicking the adjacent empty circle so that a blue checkmark (![Select](/help/search-social-commerce/assets/include.png "Select")) appears.
      
      You can't configure a target for both a parent campaign and a child ad group (which automatically uses the target).

1. Click **[!UICONTROL Post]**.

1. (Optional) Set a bid adjustment for the target in one of the following ways from the [!UICONTROL Targets] view:

   * Click in the **[!UICONTROL Bid Adjustment]** column and enter a value.
   
   * Select the check box next to the target row. In the toolbar , click ![Edit](/help/search-social-commerce/assets/edit.png "Edit"), enter the bid modifier, and then click **[!UICONTROL Post]**.

   Values can include:
   
   * *0%:* To not adjust bids for ads for this audience.
   
   * /[*Other values from -90% to 900%*/]: To increase or decrease the bid for ads for this audience. For example, if the  keyword-level bid is 1 USD and the bid adjustment for a specific audience target is 50%, then the bid for that audience increases to 1.50 USD.

## Edit the bid modifier for audience targets

You can change the bid modifier and status of audience targets for all audience types except for in-market audiences.

>[!NOTE]
>
>Search, Social, & Commerce automatically optimizes the bid modifier when the parent campaign uses the CPC bid strategy and is in a portfolio configured to auto-optimize bid adjustment values for audience targets.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Audiences] > [!UICONTROL Targets]**.

1. Do either of the following:

   * To edit a bid modifier for one target, click in the **[!UICONTROL Bid Adjustment]** column and edit the bid adjustment.

   * To edit a bid modifier for one more targets, do the following:

     1. Select the check box next to each target to edit.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

     1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

     1. Edit the **[!UICONTROL Bid Modifier]** and/or **[!UICONTROL Status]** fields.
     
         For the [!UICONTROL Bid Modifier] field, you have options to change existing values to a specified value or to either increase or decrease the amount by a specified percentage or monetary amount, with a limit.

         For a set value, the value can include:
         
         * *0%:* To not adjust bids for ads for this audience.
         
         * /[*Other values from -90% to 900%*/]: To increase or decrease the bid for ads for this audience. For example, if the  keyword-level bid is 1 USD and the bid adjustment for a specific audience target is 50%, then the bid for that audience increases to 1.50 USD.
         
         For multiple targets, your changes are applied to all of the selected targets.

     1. (Optional) Click **[!UICONTROL Additional Details]** and optionally enter a project name and description.
     
     1. Click **[!UICONTROL Post]**.
  
## Change the status of audience targets

You can pause an active audience target to disable bidding on it. You can later resume bidding by changing the status back to active.

You can also delete an active or paused search audience target.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Audiences] > [!UICONTROL Targets]**.

1. (Optional) Filter the list to include specific audience targets.

1. Select the check box next to each audience target whose status you want to change.
     
   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar, click the status button:

   * To activate the rows, click ![Activate](/help/search-social-commerce/assets/activate.png "Activate").
   
   * To pause the rows, click ![Pause](/help/search-social-commerce/assets/pause.png "Pause").
   
   * To delete the rows, click ![More actions](/help/search-social-commerce/assets/more.png "More actions") and select **[!UICONTROL Delete]**. In the confirmation message, click **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [About audiences](audience-about.md)
>* [Manage audience exclusions for campaigns and ad groups](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
