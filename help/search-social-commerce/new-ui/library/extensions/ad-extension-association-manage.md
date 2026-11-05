---
title: Manage ad extension associations
description: Learn how to associate shared sitelinks and callouts with account entities, delete associations, and copy association data to your clipboard.
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
# Manage ad extension associations

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts only*

An association links an ad extension to an account entity so that the extension can be used with its ads. You can create associations for shared sitelinks and callouts and delete existing associations, including sitelink, callout, location, and phone extension associations supported by the ad network.

Deleting a shared sitelink or callout association removes the association with the selected entity; it doesn't delete the shared extension from the library. To delete the shared extension instead, use the **[!UICONTROL Sitelinks]** or **[!UICONTROL Callouts]** tab.

Viewing associations requires the [!UICONTROL View Extensions] permission. Creating or deleting associations requires the [!UICONTROL Edit Extensions] permission.

## Associate shared sitelinks with accounts, campaigns, and ad groups {#sitelink-associate}

You can assign shared sitelinks for use on the search network:

* For [!DNL Google Ads], assign sitelinks to accounts, campaigns, or ad groups.

* For [!DNL Microsoft Advertising], assign sitelinks to campaigns. To assign them to accounts or ad groups, use the [!DNL Microsoft Advertising] ad manager.

You can assign up to 20 sitelinks per account, campaign, or ad group. Keep at least six active sitelinks available for desktop and mobile coverage.

1. In the main menu, click **[!UICONTROL Library] > [!UICONTROL Extensions]**, and then click the **[!UICONTROL Associations]** tab.

1. Click **[!UICONTROL Create Association] > [!UICONTROL Sitelink Association]**.

1. In the **[!UICONTROL Basic Settings]** section, select the ad network and account.

1. In the **[!UICONTROL Sitelinks]** section, select the shared sitelinks to associate from the account's library.

1. In the **[!UICONTROL Assignment]** section, select the account entities to which the sitelinks are assigned:

  * Select each applicable account, campaign, or ad group.

  * To view an account's campaigns or a campaign's ad groups, expand the account or campaign.

  * Use the list's search controls to find specific entities.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

## Associate shared callouts with campaigns and ad groups {#callout-associate}

*[!DNL Google Ads] accounts only*

You can associate shared callouts with [supported Google Ads campaigns and ad groups](/help/search-social-commerce/introduction/supported-inventory.md) on the search network. Assign at least two callouts to each campaign or ad group.

1. In the main menu, click **[!UICONTROL Library] > [!UICONTROL Extensions]**, and then click the **[!UICONTROL Associations]** tab.

1. Click **[!UICONTROL Create Association] > [!UICONTROL Callout Association]**.

1. In the **[!UICONTROL Basic Settings]** section, select [!DNL Google Ads] and the account.

1. In the **[!UICONTROL Callouts]** section, select the shared callouts to associate from the account's library.

1. In the **[!UICONTROL Assignment]** section, select the campaigns or ad groups to which the callouts are assigned:

  * Select each applicable campaign or ad group.

  * To view a campaign's ad groups, expand the campaign.

  * Use the list's search controls to find specific campaigns or ad groups.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

## Delete associations {#association-delete}

1. In the main menu, click **[!UICONTROL Library] > [!UICONTROL Extensions]**, and then click the **[!UICONTROL Associations]** tab.

1. (Optional) Filter the list to include specific extensions, campaigns, or ad groups.

1. Select the check box next to each association to delete.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click ![Delete](/help/search-social-commerce/assets/delete-new.png "Delete").

1. In the confirmation message, click **[!UICONTROL Confirm]**.

## Copy all data in selected rows to your clipboard {#copy-to-clipboard}

Copy the visible information in selected rows, according to the applied filters and columns visible in the view. The information is saved as tab-separated values (TSV).

1. Select the check box next to each row whose data you want to copy.

1. In the bulk actions toolbar, click **[!UICONTROL Copy]**.

>[!MORELIKETHIS]
>
>* [Manage shared sitelink extensions](sitelink-extension-manage.md)
>* [Manage Google Ads shared callout extensions](callout-extension-manage.md)
