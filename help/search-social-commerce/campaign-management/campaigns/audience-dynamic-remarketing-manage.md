---
title: Manage [!DNL Microsoft Advertising] dynamic remarketing audiences
description: Learn how to create and manage [!DNL Microsoft Advertising] dynamic remarketing audiences.
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
---
# Manage [!DNL Microsoft Advertising] dynamic remarketing audiences

*[!DNL Microsoft Advertising] accounts only*

You can create a [!DNL Microsoft Advertising] dynamic remarketing audience when you use the search engine's JavaScript conversion- and audience-tracking tag on your webpages. Each audience is created using a specified tag that's included in the webpages whose users comprise the audience. You can create multiple audiences with the same tracking tag. You can also change the name and data source for existing audiences, or delete existing audiences.

Dynamic remarketing audiences have the Audience Type "[!UICONTROL Dynamic Remarketing] \<Visitor Type\>" (such as "Dynamic Remarketing Past Buyers").

For more information about dynamic remarketing and how to implement the required JavaScript tag, see the [[!DNL Microsoft Advertising] documentation on dynamic remarketing](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Create a dynamic remarketing audience

>[!NOTE]
>
>For [!DNL Microsoft Advertising] accounts, the JavaScript tag must include the [product ID and page type parameters](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. Identify the name of the [!DNL Microsoft Advertising] universal event tracking (UET) tag that's included in the webpages from which the audience will be created.

   You'll need the tag name in a later step.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Audiences] > [!UICONTROL Library]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network and the account name, and then click **[!UICONTROL Continue]**.

1. Specify the audience information:

   1. In the **[!UICONTROL Data Source]** menu, select **[!UICONTROL Dynamic Remarketing List]**.
   
   1. Enter the **[!UICONTROL Audience Name]**.
   
   1. From a list of all available tags for the search engine account, select the name of the [!DNL Microsoft Advertising] UET tag that's included in the webpages whose users comprise the audience.
   
   1. Select the visitor type for the audience, which is based on visitor actions on the relevant webpages: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*, or *[!UICONTROL Shopping Cart Abandoners]*.
   
   1. Specify the number of **[!UICONTROL Membership Days]**, which is the number of days a user's cookie stays in the audience. Values can range from one (1) to 180.
      
      Use the length of time for which you expect your ad to be relevant to the user.

1. Click **[!UICONTROL Post]**.

>[!NOTE]
>
>Your [!DNL Microsoft Advertising] dynamic remarketing lists are eligible for targeting once they include at least 300 users.

## Edit a dynamic remarketing audience

You can change the name and data source for a [!DNL Microsoft Advertising] dynamic remarketing audience. You can't edit the value of the [!UICONTROL Membership Days] setting.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Audiences] > [!UICONTROL Library]**.

1. Select the check box next to the audience to edit.

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Edit the audience information:

   1. In the **[!UICONTROL Data Source]** section, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

   1. (Optional) Change the **[!UICONTROL Audience Name]**.

   1. (Optional) From a list of all available tags for the ad network account, change the name of the [!DNL Microsoft Advertising] UET tag that's included in the webpages whose users comprise the audience.

   1. (Optional) Change the visitor type for the audience, which is based on visitor actions on the relevant webpages: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*, or *[!UICONTROL Shopping Cart Abandoners]*.

   1. Click **[!UICONTROL Post]**.

## Delete a dynamic remarketing audience

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Audiences] > [!UICONTROL Library]**.

1. (Optional) Filter the list to include specific audiences.

1. Select the check box next to each audience to delete.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the confirmation message, click **[!UICONTROL Delete]**.
 
>[!MORELIKETHIS]
>
>* [About audiences](audience-about.md)
>* [Create [!DNL Google Ads] customer match audiences from [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [Create a [!DNL Google Ads] customer match audience from an Adobe Campaign email list](google-audience-from-campaign-email-list.md)
>* [Manage customer match audiences using customer data lists](audience-from-customer-data-list.md)
