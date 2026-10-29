---
title: Manage audience exclusions for campaigns and ad groups
description: Learn about Google Ads and Microsoft Advertising audience exclusions, including how to delete Google Ads exclusions.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Manage audience exclusions for campaigns and ad groups

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts only*

An audience exclusion prevents ads in a campaign or ad group from being shown to users in a specific [audience](audience-manage.md).

For [!DNL Google Ads] accounts, you can exclude any audience type. For [!DNL Microsoft Advertising] accounts, you can exclude only dynamic remarketing audiences.

>[!NOTE]
>
>Exclusions always override [audience targets](audience-targets-manage.md).

## About the [!UICONTROL Exclusions] view {#audience-exclusions-view-about}

The [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Exclusions] view lists the audience exclusions in the filtered view for the selected advertiser.

Viewing the data requires the [!UICONTROL View Audiences] permission. Selecting rows and deleting supported exclusions requires the [!UICONTROL Edit Audience Exclusions] permission.

### Available actions

<!--
Restricted to internal beta users:

* [Configure audience exclusions](#audience-exclusions-create)
-->

* [Delete audience exclusions](#audience-exclusions-delete)

* [Copy all data in selected rows to your clipboard](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience exclusion creation.

## Configure audience exclusions {#audience-exclusions-create}

Creating exclusions requires the [!UICONTROL Edit Audience Exclusions] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Exclusions]** tab.

1. Click **[!UICONTROL Create Exclusion]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups from which to exclude the audiences:

   * Select each applicable campaign or ad group for exclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.
-->

## Delete audience exclusions {#audience-exclusions-delete}

*[!DNL Google Ads] exclusions only*

You can delete one or more [!DNL Google Ads] audience exclusions. Deleting [!DNL Microsoft Advertising] exclusions isn't supported in this view.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Exclusions]** tab.

1. (Optional) Filter the list to include specific audience exclusions.

1. Select the check box next to each [!DNL Google Ads] exclusion to delete. Don't include exclusions from another ad network in the selection.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

## Copy all data in selected rows to your clipboard {#copy-to-clipboard}

Copy the visible information in selected rows, according to the applied filters and columns visible in the view. The information is saved as tab-separated values (TSV).

1. Select the check box next to each row whose data you want to copy.

1. In the bulk actions toolbar, click **[!UICONTROL Copy]**.

>[!MORELIKETHIS]
>
>* [Manage audiences](audience-manage.md)
>* [Manage audience targets for campaigns and ad groups](audience-targets-manage.md)
