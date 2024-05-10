---
title: Create negative keywords
description: Learn how to create negative keywords for search campaigns and ad groups.
exl-id: afe786bf-eda8-4590-b471-3fb696c420de
feature: Search Campaign Management
---
# Create negative keywords

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], and existing [!DNL Baidu] accounts only*

You can create negative keywords for a search ad group or campaign that targets the search or display/native network. Negative keywords don't trigger ads.

>[!NOTE]
>You can also create and edit negative keywords in the [ad group settings](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) and [campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>To create many negative keywords at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Keywords] > [!UICONTROL Negatives]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create"), and then click **[!UICONTROL Campaign]** to create campaign-level negative keywords or **[!UICONTROL Ad Group]** to create ad group-level negative keywords.

1. Select the ad network, the account, the campaign, and (when relevant) the ad group, and then click **[!UICONTROL Continue]**.

1. Enter the negative keywords. Use the following syntax, without a minus sign (`-`):

   * Negative broad match: `keyword` (not supported by [!DNL Microsoft Advertising])
   
   * Negative phrase match: `"keyword"`
   
   * Negative exact match: `[keyword]`

   Separate multiple values with commas, or enter them on separate lines. You can enter or paste up to 2000 negative keywords in one operation. See also the following requirements and restrictions:
   
   * Maximum character lengths: [!DNL Baidu]: 30 single-byte or 15 double-byte; [!DNL Microsoft Advertising]: 100 single-byte or 50 double-byte; [!DNL Google Ads] and [!DNL Yahoo! Japan Ads]: 80 single-byte or 40 double-byte.
   
   * [!DNL Baidu] allows only one match type per keyword per ad group. For example, Ad Group 1 can't include both `"keyword"` and `[keyword]`.
   
   * [!DNL Google Ads]: Each keyword can consist no more than 10 words and can include only letters, digits, and the following special characters: space `# $ & _ - " [ ] ' + . / :`
   
   * [!DNL Yandex]: Each keyword can have a maximum of seven words, excluding stop words. Each [!DNL Yandex ad group] can include a maximum of 200 keywords.

1. Click **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [About keywords](keyword-about.md)
>* [Manage biddable keywords](keyword-manage.md)
>* [Change the status of keywords and negative keywords](keyword-status-edit.md)
