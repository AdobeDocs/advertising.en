---
title: Manage modifiers
description: Learn how to configure and manage modifiers for your ad templates for inventory data feeds.
exl-id: ade1472d-10e3-454e-8095-c579b48cfc01
---
# Managing modifiers

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (delete actions only), and [!DNL Yandex] accounts only*

Modifiers are adjectives or adverbs that can be added to or removed from a sentence without changing the basic sentence structure. You can create groups of modifiers to use as variables in various data fields in feed data templates. By including modifiers in account structure (campaign and ad group) fields, keywords, base URLs, and ads, you create one value for each associated modifier value. For example, if you use a modifier group variable in an ad headline, and the modifier group includes three modifiers ("cheap," "discount," and "affordable"), then three separate ads are created for each data row in the data feed &mdash; one for each modifier. Similarly, if you include a modifier group with multiple values in the base URL for an ad group, then one set of keywords is created for each of the resulting base URLs.

Each modifier group can include as many modifiers as you want. Each template can use only one modifier group.

## Create a modifier group

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**.

1. In the toolbar above the data table, click **[!UICONTROL Modifiers]**.

1. Above the list of modifier groups, click **[!UICONTROL Create]**.

1. Specify the modifier group settings:

   **[!UICONTROL Name]:** The name of the modifier group.
   
   **[!UICONTROL Modifiers]:** The modifier values for the group (one per line).

1. Click **[!UICONTROL Save]**.

## Edit a Modifier Group

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**.

1. In the toolbar above the data table, click **[!UICONTROL Modifiers]**.

1. In the list of modifier groups, click the modifier group name.

1. Edit the modifier group settings:

   **[!UICONTROL Name]:** The name of the modifier group.
   
   **[!UICONTROL Modifiers]:** The modifier values for the group (one per line).

1. Click **[!UICONTROL Save]**.

## Delete Modifier Groups

>[!IMPORTANT]
>
>When you delete a modifier group, remove all variables for that modifier group (denoted as `<modifier_group_name>`) from the fields of existing templates. If you try to propagate data through a template using variables for modifiers that don't exist, the job fail1.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**.

1. In the toolbar above the data table, click **[!UICONTROL Modifiers]**.

1. Select the check box next to each modifier group that you want to delete.

1. Above the list of modifier groups, click **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Yes]**.

1. (If necessary) [Remove references to the modifier](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) from all applicable templates.

>[!MORELIKETHIS]
>
>* [About inventory feeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Manage ad templates](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
