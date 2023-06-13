---
title: Manage ads
description: Learn how to create and manage ads.
exl-id: 9108bbfd-61e7-49fa-90ba-4eb276eb0897
---
# Manage ads

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], and [!DNL Yandex] accounts only*

You can create, edit, and change the status of ads from the [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads] view.

## Create an ad

>[!NOTE]
>
>You don't need to create product ads for shopping campaigns; the ad network creates them automatically. For [!DNL Microsoft Advertising] shopping campaigns, however, you can optionally define promotion lines to include in ads.

>[!TIP]
>
>To create many ads at once, use the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Ads]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network, the account, the campaign, the ad group, and the ad type, and then click **[!UICONTROL Continue]**.
   
   For more information about the different ad types, see "[About ads](ad-about.md)."

1. Enter the [[!DNL Baidu] text ad](ad-settings-baidu-text.md), [[!DNL Google Ads] call-only ad](ad-settings-google-call.md), [[!DNL Google Ads] expanded dynamic search ad](ad-settings-google-dsa.md) (now called just "dynamic search ad" in Google Ads), [[!DNL Google Ads] responsive search ad](ad-settings-google-rsa.md), [[!DNL Microsoft Advertising] expanded dynamic search ad](ad-settings-microsoft-dsa.md), [[!DNL Microsoft Advertising] multimedia ad](ad-settings-microsoft-multimedia.md), [[!DNL Microsoft Advertising] product ad](ad-settings-microsoft-product.md), [[!DNL Microsoft Advertising] responsive (audience) ad](ad-settings-microsoft-responsive.md), [[!DNL Microsoft Advertising] responsive search ad](ad-settings-microsoft-rsa.md), or [[!DNL Yandex] text ad](ad-settings-yandex-text.md) settings.
   
   >[!NOTE]
   >
   >(Campaigns with Adobe Advertising conversion tracking) If the account or campaign settings specify tracking only at the keyword level, then Search, Social, & Commerce doesn't generate tracking for ads.

1. Click **[!UICONTROL Post]**.

1. (Shopping ads in campaigns with Adobe Advertising conversion tracking; optional) To track clicks on the ad, [generate a tracking URL using the Tracking URLs tool](/help/search-social-commerce/tools/click-tracking-url-generate.md), and manually add it to the account, campaign, or product group settings.

## Edit ad settings

>[!NOTE]
>
>* The following ad types are *mutable*, which means that you can change the ad copy or image and retain the same ad ID: all [!DNL Google Ads] ad types except for dynamic search ads, and [!DNL Microsoft Advertising] expanded text ads.
>* All other supported ads are *non-mutable*, which means that changing the ad copy or image deletes the existing ad and creates a new one. Performance for the new ad may be volatile for a couple of weeks while Search, Social, & Commerce gathers enough data to optimize bids.
>* You can't edit the content of a product ad, except for the promotion line for [!DNL Microsoft Advertising] product ads. You can, however, pause or delete an ad.

>[!TIP]
>
>To edit large amounts of data at once, use the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Ads]**.

1. Do either of the following:
   
   * (To edit settings for a single ad) Hold the cursor over the ad preview and click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").
   
   * (To edit settings for one or more ads) Do the following:
     
     1. Select the check box next to each row.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."
     
     1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Edit the [[!DNL Baidu] text ad](ad-settings-baidu-text.md), [[!DNL Google Ads] call-only ad](ad-settings-google-call.md), [[!DNL Google Ads] expanded dynamic search ad](ad-settings-google-dsa.md) (now called just "dynamic search ad" in Google Ads), [[!DNL Google Ads] responsive search ad](ad-settings-google-rsa.md), [[!DNL Microsoft Advertising] expanded dynamic search ad](ad-settings-microsoft-dsa.md), [[!DNL Microsoft Advertising] multimedia ad](ad-settings-microsoft-multimedia.md), [[!DNL Microsoft Advertising] product ad](ad-settings-microsoft-product.md), [[!DNL Microsoft Advertising] responsive (audience) ad](ad-settings-microsoft-responsive.md), [[!DNL Microsoft Advertising] responsive search ad](ad-settings-microsoft-rsa.md), or [[!DNL Yandex] text ad](ad-settings-yandex-text.md) settings.

   For multiple ads, you can edit only the fields that are common to all of the selected ads, and your changes are applied to all of the selected ads. For some alphanumeric fields, you can change existing values to a specified value, replace an existing string with a specified string, add a specified prefix to the beginning of each value, or append a suffix to the end of each value. For some monetary fields, you can change existing values to a specified value or either increase or decrease the amount by a specified percentage or monetary amount, with a limit.

1. Save the data:

   * (Single ads) Click **[!UICONTROL Post]**.
   
   * (Multiple ads) Click **[!UICONTROL Post Now]**.

## Change the status of ads

You can pause an active ad to disable bidding on it. You can later resume bidding by changing the status back to active.

You also can delete any active or paused search ad. Deleted ads are deleted from the ad network. They're still visible, but you can't change them.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Ads]**.

1. (Optional) Filter the list to include specific ads.

1. Select the check box next to each ad whose status you want to change.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar, click the status button:

   * To activate the rows, click ![Activate](/help/search-social-commerce/assets/activate.png "Activate").
   
   * To pause the rows, click ![Pause](/help/search-social-commerce/assets/pause.png "Pause").
   
   * To delete the rows, click ![More](/help/search-social-commerce/assets/more.png "More") and select **[!UICONTROL Delete]**. In the confirmation message, click **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [About ads](ad-about.md)
>* [[!DNL Baidu] text ad settings](ad-settings-baidu-text.md)
>* [[!DNL Google Ads] call-only ad settings](ad-settings-google-call.md)
>* [[!DNL Google Ads] expanded dynamic search ad settings](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] responsive search ad settings](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising] expanded dynamic search ad settings](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] multimedia ad settings](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] product ad settings](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] responsive (audience) ad settings](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising] responsive search ad settings](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex] text ad settings](ad-settings-yandex-text.md)
