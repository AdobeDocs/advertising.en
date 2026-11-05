---
title: Manage Google Ads shared callout extensions
description: Learn how to create, edit, and delete Google Ads shared callout extensions.
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
# Manage [!DNL Google Ads] shared callout extensions

*[!DNL Google Ads] accounts only*

A callout extension is informational text about a product, service, or promotion that your site offers, displayed with a text ad. The ad network may show 2-4 callouts with an ad.

You create shared callout text and settings at the account level for a [synchronized Google Ads account](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md). Callouts in the library aren't used with ads until you associate them with a supported campaign or ad group on the search network.

To make your ads eligible to appear with callouts, assign at least two callouts per campaign or ad group. Callouts at the ad group level override callouts at the campaign level.

## About the [!UICONTROL Callouts] and [!UICONTROL Associations] views {#callout-view-about}

In **[!UICONTROL Library] > [!UICONTROL Extensions]**, the **[!UICONTROL Callouts]** tab lists your account-level shared callouts. The **[!UICONTROL Associations]** tab lists the associations between extensions and account entities.

Viewing these tabs requires the [!UICONTROL View Extensions] permission. Creating, editing, and deleting callouts, and creating or deleting associations, requires the [!UICONTROL Edit Extensions] permission.

See the [Google Ads documentation on account limits](https://support.google.com/google-ads/answer/6372658) for the maximum number of extensions per account.

### Available actions

* [Create a shared callout](#callout-create)

* [Edit shared callout settings](#callout-edit)

* [Delete shared callouts](#callout-delete)

* [Associate shared callouts with campaigns and ad groups](ad-extension-association-manage.md#callout-associate)

* [Delete extension associations](ad-extension-association-manage.md#association-delete)

* [Copy all data in selected rows to your clipboard](#copy-to-clipboard)

## Create a shared callout {#callout-create}

1. In the main menu, click **[!UICONTROL Library] > [!UICONTROL Extensions]**, and then click the **[!UICONTROL Callouts]** tab.

1. Click **[!UICONTROL Create Callout]**.

1. In **[!UICONTROL Basic Settings]**, select [!DNL Google Ads] and the account.

1. Enter the [shared callout settings](#shared-callout-settings).

1. Click **[!UICONTROL Review and Save]**.

1. Review the settings. To change a setting, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

After you create the callout, [associate it with a campaign or ad group](ad-extension-association-manage.md#callout-associate).

## Edit shared callout settings {#callout-edit}

You can edit one shared callout at a time. You can't change its start date after creating it.

1. In the main menu, click **[!UICONTROL Library] > [!UICONTROL Extensions]**, and then click the **[!UICONTROL Callouts]** tab.

1. Select the check box next to one callout.

1. In the bulk actions toolbar, click **[!UICONTROL Edit]**.

1. Edit the [shared callout settings](#shared-callout-settings).

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Update]**.

## Delete shared callouts {#callout-delete}

1. In the main menu, click **[!UICONTROL Library] > [!UICONTROL Extensions]**, and then click the **[!UICONTROL Callouts]** tab.

1. Select the check box next to each shared callout to delete.

   For information on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

To remove an association without deleting the shared callout from the library, [delete the association](ad-extension-association-manage.md#association-delete) instead.

## Copy all data in selected rows to your clipboard {#copy-to-clipboard}

Copy the visible information in selected rows, according to the applied filters and columns visible in the view. The information is saved as tab-separated values (TSV).

1. Select the check box next to each row whose data you want to copy.

1. In the bulk actions toolbar, click **[!UICONTROL Copy]**.

## Shared callout settings {#shared-callout-settings}

For additional policies and reasons for callout disapproval, see the [Google Ads callout requirements](https://support.google.com/adspolicy/answer/1054212).

**[!UICONTROL Callout Text]:** The text to appear. It can include up to 25 single-byte or 12 double-byte characters. It can't include exclamation marks or punctuation at the beginning of the text.

**[!UICONTROL Start Date]:** (Optional; creation only) The first date on which the callout may be displayed. The default is the current day. To specify a future date, enter it in MM/DD/YYYY format or use the date picker. The start date is read-only for existing callouts.

**[!UICONTROL End Date]:** (Optional) The last date on which the callout may be displayed. By default, the callout may be displayed indefinitely. To specify an end date, enter it in MM/DD/YYYY format or use the date picker.

**[!UICONTROL Mobile Preference]:** (Optional) Allows [!DNL Google Ads] to try to display the extension to mobile device users rather than desktop or tablet users. Otherwise, the extension can appear on any device type. [!DNL Google Ads] doesn't guarantee that it will display the extension on the preferred device type.

## Performance data for callouts {#callout-performance}

Search, Social, & Commerce maps clicks on an ad extension and the resulting conversions to the keyword associated with the ad in which the extension appears. Extension-level cost and click data aren't available in Search, Social, & Commerce.

You can view extension-level cost and click data in the [!DNL Google Ads] interface.

>[!MORELIKETHIS]
>
>* [Manage shared sitelink extensions](sitelink-extension-manage.md)
>* [Manage ad extension associations](ad-extension-association-manage.md)
