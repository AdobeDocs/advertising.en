---
title: Manage shared sitelink extensions
description: Learn how to create and manage shared sitelinks and associate them with accounts, campaigns, and ad groups.
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
# Manage shared sitelink extensions

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts only*

A sitelink is an extra text link in a text ad listing. Use sitelinks to take users directly to specific pages on your site. The ad network determines which sitelinks to display based on their relevance to the ad.

You can optionally include descriptive text for each sitelink. The ad network may also display copy from existing ads in the account when it's highly relevant to the sitelink. [!DNL Google Ads] may show 2-6 sitelinks in a desktop ad and up to four in a mobile ad. [!DNL Microsoft Advertising] may show two, four, or six sitelinks with descriptions or 4-6 without descriptions.

You create shared sitelink text and settings at the account level for a [synchronized ad network account](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md). Sitelinks in the library aren't used with ads until you associate them with account entities.

## About the [!UICONTROL Sitelinks] and [!UICONTROL Associations] views {#sitelink-view-about}

In **[!UICONTROL Library] > [!UICONTROL Extensions]**, the **[!UICONTROL Sitelinks]** tab lists your account-level shared sitelinks. The **[!UICONTROL Associations]** tab lists the associations between extensions and account entities.

Viewing these tabs requires the [!UICONTROL View Extensions] permission. Creating, editing, and deleting sitelinks, and creating or deleting associations, requires the [!UICONTROL Edit Extensions] permission.

See the ad network help for the maximum number of extensions per [Google Ads account](https://support.google.com/google-ads/answer/6372658) and per [Microsoft Advertising account](https://help.ads.microsoft.com/#apex/3/en/52001).

### Available actions

* [Create a shared sitelink](#sitelink-create)

* [Edit shared sitelink settings](#sitelink-edit)

* [Delete shared sitelinks](#sitelink-delete)

* [Associate shared sitelinks with accounts, campaigns, and ad groups](#sitelink-associate)

* [Delete extension associations](ad-extension-association-delete.md)

* [Copy all data in selected rows to your clipboard](#copy-to-clipboard)

## Create a shared sitelink {#sitelink-create}

1. In the main menu, click **[!UICONTROL Library] > [!UICONTROL Extensions]**, and then click the **[!UICONTROL Sitelinks]** tab.

1. Click **[!UICONTROL Create Sitelink]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Enter the [shared sitelink settings](#shared-sitelink-settings).

1. Click **[!UICONTROL Review and Save]**.

1. Review the settings. To change a setting, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

After you create the sitelink, [associate it with an account, campaign, or ad group](#sitelink-associate).

## Edit shared sitelink settings {#sitelink-edit}

You can edit one shared sitelink at a time. You can't change its start date after creating it.

1. In the main menu, click **[!UICONTROL Library] > [!UICONTROL Extensions]**, and then click the **[!UICONTROL Sitelinks]** tab.

1. Select the check box next to one sitelink.

1. In the bulk actions toolbar, click **[!UICONTROL Edit]**.

1. Edit the [shared sitelink settings](#shared-sitelink-settings).

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Update]**.

You can also edit a sitelink's **[!UICONTROL Base URL]** or **[!UICONTROL Tracking Template]** directly in the data table by clicking its value.

## Delete shared sitelinks {#sitelink-delete}

1. In the main menu, click **[!UICONTROL Library] > [!UICONTROL Extensions]**, and then click the **[!UICONTROL Sitelinks]** tab.

1. Select the check box next to each shared sitelink to delete.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

To remove an association without deleting the shared sitelink from the library, [delete the association](ad-extension-association-delete.md) instead.

## Associate shared sitelinks with accounts, campaigns, and ad groups {#sitelink-associate}

You can assign shared sitelinks for use on the search network:

* For [!DNL Google Ads], assign sitelinks to accounts, campaigns, or ad groups.

* For [!DNL Microsoft Advertising], assign sitelinks to campaigns. To assign them to accounts or ad groups, use the [!DNL Microsoft Advertising] ad manager.

You can assign up to 20 sitelinks per account, campaign, or ad group. Keep at least six active sitelinks available for desktop and mobile coverage.

1. In the main menu, click **[!UICONTROL Library] > [!UICONTROL Extensions]**, and then click the **[!UICONTROL Associations]** tab.

1. Click **[!UICONTROL Create Association] > [!UICONTROL Sitelink Association]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select the shared sitelinks to associate from the account's library.

1. Select the account entities to which the sitelinks are assigned:

   * Select each applicable account, campaign, or ad group.

   * To view an account's campaigns or a campaign's ad groups, expand the account or campaign.

   * Use the list's search controls to find specific entities.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

## Copy all data in selected rows to your clipboard {#copy-to-clipboard}

Copy the visible information in selected rows, according to the applied filters and columns visible in the view. The information is saved as tab-separated values (TSV).

1. Select the check box next to each row whose data you want to copy.

1. In the bulk actions toolbar, click **[!UICONTROL Copy]**.

## Shared sitelink settings {#shared-sitelink-settings}

For additional policies and reasons for sitelink disapproval, see the [Google Ads sitelink requirements](https://support.google.com/adspolicy/answer/1054210) and [Microsoft Advertising sitelink requirements](https://help.ads.microsoft.com/#apex/ads/en/ext60206).

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** The text to appear for the link. It can include up to 25 single-byte or 12 double-byte characters. The link text must be unique within the account or campaign.

>[!NOTE]
>
>([!DNL Google Ads]) Existing text of 35 characters is displayed in ads on desktops and tablets but not on mobile devices.

**[!UICONTROL Status]:** The display status of the sitelink: **[!UICONTROL Active]** or **[!UICONTROL Deleted]** for existing sitelinks. New sitelinks are active by default.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Extra text that the ad network may display under the link text. To include a description, enter both fields. Each can include up to 35 single-byte or 17 double-byte characters.

**[!UICONTROL Start Date]:** (Optional; creation only) The first date on which the sitelink may be displayed. The default is the current day. To specify a future date, enter it in MM/DD/YYYY format or use the date picker. The start date is read-only for existing sitelinks.

**[!UICONTROL End Date]:** (Optional) The last date on which the sitelink may be displayed. By default, the sitelink may be displayed indefinitely. To specify an end date, enter it in MM/DD/YYYY format or use the date picker.

**[!UICONTROL Mobile Preference]:** (Optional) Allows the network to try to display the extension to mobile device users rather than desktop or tablet users. By default, this option isn't enabled, and the extension can appear on any device type. The network doesn't guarantee that it will display the extension on the preferred device type.

### [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

**[!UICONTROL Tracking Template]:** (Optional) The tracking URL, including off-landing domain redirects and tracking parameters, with the final landing page URL embedded in a parameter. For example, `https://www.trackingservice.example.com/?url={lpurl}&source={network}&id=5`.

In this view, values entered for [!UICONTROL Base URL] and [!UICONTROL Tracking Template] must start with `http://` or `https://` and can't contain spaces.

* When the campaign settings include **[!UICONTROL EF Redirect]** and **[!UICONTROL Auto Upload]**, Search, Social, & Commerce automatically prefixes its own redirect and tracking code when you save the record.

* For parameters that embed the final URL, see the [Microsoft Advertising documentation](https://help.ads.microsoft.com/#apex/3/en/56799) or the "Tracking template only" parameters in the [Google Ads ValueTrack documentation](https://support.google.com/google-ads/answer/6305348).

* You can include URL parameters and campaign-level custom parameters, separated by ampersands (`&`), and third-party redirects and tracking.

* The tracking template at the most granular level overrides templates at higher levels.

>[!NOTE]
>
>* For accounts with final URLs, the base URL may contain redirects within the landing page domain or subdomain, but not outside the landing page domain. The ad network extracts the domain to create the display URL.
>* ([!DNL Google Ads]) Each sitelink in a campaign or ad group must have a unique landing page with approximately 80% unique content. Don't use links to multiple anchors on the same page as separate sitelink landing pages.
>* ([!DNL Google Ads]) Updating a tracking template at the sitelink or keyword level resubmits the relevant ads for review. Updating it at the account, campaign, or ad group level doesn't resubmit the ads.
>* ([!DNL Microsoft Advertising]) You can update tracking templates at any level without resubmitting ads for approval.
>* ([!DNL Google Ads]) Avoid macros, which aren't substituted for clicks from sources that enable parallel tracking. If macros are required, your Adobe Account Team should work with Customer Support or the implementation team to add them.

## Performance data for sitelinks {#sitelink-performance}

Search, Social, & Commerce maps clicks on an ad extension and the resulting conversions to the keyword associated with the ad in which the extension appears. Extension-level cost and click data isn't available in Search, Social, & Commerce.

In the [!UICONTROL Transaction Report], a [!UICONTROL Link Type] value of `sl:<Sitelink text>`, such as `sl:See Current Offers`, identifies a transaction from a sitelink rather than the ad itself. See "[Transaction Report](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)."

You can view extension-level cost and click data in the ad network's interface.

>[!MORELIKETHIS]
>
>* [Manage Google Ads shared callout extensions](callout-extension-manage.md)
>* [Delete ad extension associations](ad-extension-association-delete.md)
