---
title: (New UI) Manage ad network accounts
description: Learn how to set up and manage account details in the new UI for an ad network synced via the ad network API.
feature: Search Campaign Management
exl-id: a50b2943-7568-401c-be5b-ff6f62629488
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
---
# (New UI) Manage ad network accounts via API connection

Following are instructions for managing ad network accounts that Search, Social, & Commerce syncs using the ad network's API, including authenticating accounts, refreshing connections, and checking authentication and access status.

To create, edit, or re-authenticate accounts, you must have permission to edit accounts.

For details about the functionality available for each ad network, see "[Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md)."

## About the [!UICONTROL Accounts] view {#account-view-about}

The [!UICONTROL Manage] > [!UICONTROL Accounts] view lists all ad network accounts in the filtered view for the selected advertiser account. Click an account name to open the [!UICONTROL Campaigns] view filtered for that account.

### Account authentication and access status {#authentication-status}

Authentication and access details vary by ad network and by the information available for the account. An enabled or successfully authenticated account can still have missing permissions.

The following columns show account status, authentication, and access details:

* **[!UICONTROL Status]:** The account's operational status, which is separate from its authentication and permissions. An enabled account can sync data with the ad network and use supported account management and optimization features. A disabled account stops activity within Search, Social, & Commerce. The account status display uses a green indicator for **[!UICONTROL Enabled]**, a red indicator for **[!UICONTROL Disabled]**, and an amber indicator for **[!UICONTROL Pending]**. You can [enable or disable accounts](#enable-disable-account) from the view or the account settings.

* **[!UICONTROL Authenticated]:** Whether the account is authenticated:

  * **[!UICONTROL Yes]:** The account is authenticated.

  * **[!UICONTROL No]:** The account isn't authenticated. When an authentication error is available, hold the cursor over the red warning icon to view the error.

  * **[!UICONTROL Not Applicable]:** Authentication doesn't apply because you upload data for the account rather than connect through an API.

  * **[!UICONTROL Expiring in N days]**, **[!UICONTROL Expiring today]**, or **[!UICONTROL Expired]:** A token-expiration warning replaces **[!UICONTROL Yes]** when expiration information is available and the token expires in 14 days or fewer or has already expired. Click the warning icon to view the account's access details and [re-authenticate](#reauthenticate).

* **[!UICONTROL Manager Account for Cross-Account Conversions]:** ([!DNL Google Ads] accounts only) The ID of the associated manager account used for cross-account conversion uploads. When an error is available for the manager account, a warning icon appears next to the ID. Hold the cursor over the icon to view the error. The manager account's credentials are separate from the ad network account's credentials. To add or refresh manager account credentials, use **[!UICONTROL Setup]** > **[!UICONTROL Manager Accounts]**. See "[Manage manager accounts](/help/search-social-commerce/new-ui/set-up/manager-account-manage.md)."

* **[!UICONTROL Access Level]:** The reported account access level, such as **[!UICONTROL Full]**, **[!UICONTROL Limited]**, or **[!UICONTROL None]**, or **[!UICONTROL Not Applicable]** when no access-level value is available.

  When permissions are missing, click the warning icon to view the account's access details. The **[!UICONTROL Access]** section lists permissions as **[!UICONTROL Granted]** or **[!UICONTROL Missing]**. When impact details are available, the **[!UICONTROL Not working]** section lists the affected functionality. To [re-authenticate](#reauthenticate) and update permissions, click **[!UICONTROL Update Access]**.

### Available actions

The available actions depend on your permissions and the account type.

* [Create ad network account details](#create-account)

* [Edit ad network account details](#edit-account)

* [Re-authenticate an ad network account](#reauthenticate)

* [Enable or disable ad network accounts](#enable-disable-account)

* [Sync account data with the ad network](sync-api-accounts.md)

* [View a performance graph in the [!UICONTROL Accounts] view](#account-performance-graph)

* [Manage data view reports from the [!UICONTROL Accounts] view](#account-reports)

## Create ad network account details {#create-account}

To enable syncing of an account, you must create a corresponding account record containing the account access credentials and tracking options and with the status *enabled*.

>[!NOTE]
>
>To create an actual account on the ad network, go to the ad network's website.

1. In the main menu, click **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Click **[!UICONTROL Create Account]**.

1. Click the name of the ad network to open account setup.

1. (All ad networks except for [!DNL ChatGPT Ads] and [!DNL Yandex]) On the **[!UICONTROL Authenticate]** tab, complete sign-in in the popup window using the advertiser's credentials and grant the requested account access.

   The setup screen updates automatically and displays **[!UICONTROL Authentication Successful]** when authentication succeeds. If you need to reopen the login window, click **[!UICONTROL Open login again]**. If your browser blocks the window, edit your browser settings to allow popups for the site.

   For [!DNL Meta Ads], a warning identifies any missing permissions and their impact. Successful authentication doesn't necessarily mean that all requested permissions were granted.

   Click **[!UICONTROL Next]** to continue.

1. Specify the [account settings](#account-settings-api) on each available tab. For accounts authenticated in a popup, select the account to sync from **[!UICONTROL Linked Ad Accounts]** on the **[!UICONTROL Select Accounts]** tab.

1. Click **[!UICONTROL Save]**.

   Recent cost and click data for all campaigns in the account is updated within Search, Social, & Commerce hourly. By default, data is available for the last 5-10 days, depending on the ad network. When necessary, however, the project launch team may retrieve data for up to the last 60 days.

## Edit ad network account details {#edit-account}

To enable or disable activity on an account, change the default tracking parameters across an account, or change the [!DNL Analytics] report suites to use for tracking and reporting, edit the account details. To refresh the connection or update permissions, you can [re-authenticate the account](#reauthenticate) from the account settings or the [!UICONTROL Accounts] view.

>[!NOTE]
>
>To edit an actual account on the ad network, go to the ad network's website.

1. In the main menu, click **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Select the account in either of the following ways:

   * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

   * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.

1. Edit the [account settings](#account-settings-api) on the available tabs.

1. Click **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Search, Social, & Commerce must synchronize the new account data with that on the ad network. This happens automatically once a day, or more often when Search, Social, & Commerce detects changes on the ad network.

## Re-authenticate an ad network account {#reauthenticate}

*For accounts that use popup authentication; not applicable to [!DNL ChatGPT Ads] or [!DNL Yandex] accounts*

To refresh the ad network connection or update permissions for the account, re-authenticate the account.

1. (If you're logged in to another account for the same ad network in the same browser application) Log out of any account other than the advertiser's.

1. In the main menu, click **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Open authentication in one of the following ways:

   * (When the account's **[!UICONTROL Authenticated]** value is **[!UICONTROL No]**) Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Re authenticate]**, when available.

   * (When a token-expiration warning is displayed) Click the warning icon in the **[!UICONTROL Authenticated]** column, and then click **[!UICONTROL Reauthenticate]**.

   * (When permissions are missing) Click the warning icon in the **[!UICONTROL Access Level]** column, and then click **[!UICONTROL Update Access]**.

   * (From the account settings) Select the check box next to the account name and click **[!UICONTROL Edit]** in the bulk actions toolbar, or hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**. On the **[!UICONTROL Account Details]** tab, in **[!UICONTROL Account Authentication]**, click **[!UICONTROL Re authenticate]**.

1. Complete sign-in in the popup window using the advertiser's credentials and grant the requested account access.

   The new access token is saved automatically when re-authentication succeeds. If you also change other account settings, click **[!UICONTROL Save]** to save those changes.

   For [!DNL Meta Ads], an information message identifies any permissions that are still missing after successful re-authentication. Review the [access details](#authentication-status) to identify the affected functionality.

## Enable or disable ad network accounts {#enable-disable-account}

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios. When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):

     * (To enable the account) Select the check box next to the account name, and then click **[!UICONTROL Enable]** in the bulk actions toolbar.

     * (To disable the account) Select the check box next to the account name, and then click **[!UICONTROL Disable]** in the bulk actions toolbar.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.
        
     1. On the **[!UICONTROL Account Details]** tab, turn on **[!UICONTROL Account Enabled]** to enable the account, or turn it off to disable the account.

     1. Click **[!UICONTROL Save]**.

## View a performance graph in the [!UICONTROL Accounts] view {#account-performance-graph}

Open and configure a performance graph with up to three metrics totalled across accounts in the filtered view for the specified date range and currency.

### View a performance graph

1. In the main menu, click **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Specify the date range and apply any filters for the accounts whose performance you want to view.

1. Above the data table, click ![Charts](/help/search-social-commerce/assets/charts.png "Charts").

1. (Optional) Use **[!UICONTROL Currency]** and **[!UICONTROL Metrics]** to specify the currency and up to three metrics to include in the chart.

### Hide a visible performance graph

* Above the data table, click ![Charts](/help/search-social-commerce/assets/charts.png "Charts").

## Manage data view reports from the [!UICONTROL Accounts] view {#account-reports}

Generate a report that includes the data rows for one or more accounts in the [!UICONTROL Accounts] view, and then download the report as a Microsoft Excel worksheet file (XLSX format). The report includes the visible columns in the view for the specified date range.

You can delete completed reports and reports that failed to generate.

### Generate a report with the filtered data rows

1. In the main menu, click **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Specify the date range and apply any filters for the data you want to download.

1. Specify the accounts whose data you want to download:

   * To download data for specific accounts, select the check boxes next to the accounts.

   * To download data for all accounts in the filtered view, leave all check boxes cleared.

1. In the toolbar above the data table, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report") **[!UICONTROL Reports]**.

1. In the [!UICONTROL Grid Reports] dialog, keep the default **[!UICONTROL Report Name]** or enter another name, and then click **[!UICONTROL Generate]**.

   The report is added to the **[!UICONTROL Recently Generated]** list.

1. (Optional) To download the file once it's completed, click ![Download](/help/search-social-commerce/assets/download.png "Download") next to the file name.

   The file is downloaded according to your browser's normal procedure.

### Download a completed report

1. In the main menu, click **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. In the toolbar above the data table, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report") **[!UICONTROL Reports]**.

1. In the **[!UICONTROL Recently Generated]** list in the [!UICONTROL Grid Reports] dialog, click ![Download](/help/search-social-commerce/assets/download.png "Download") next to the file name.

   The file is downloaded according to your browser's normal procedure.

### Delete a report

1. In the main menu, click **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. In the toolbar above the data table, click ![Download Report](/help/search-social-commerce/assets/download.png "Download Report") **[!UICONTROL Reports]**.

1. In the **[!UICONTROL Recently Generated]** list in the [!UICONTROL Grid Reports] dialog, click ![Delete](/help/search-social-commerce/assets/delete-new.png "Delete") next to the name of a completed report or a report that failed to generate.

1. Confirm the deletion.

## Ad network account settings {#account-settings-api}

The account settings vary by ad network. You may not see all settings below.

### [!UICONTROL Authenticate] tab

(Visible while you're creating an account that uses popup authentication) Connect to the ad network using the advertiser's credentials. The tab displays the connection status and includes **[!UICONTROL Open login again]** to reopen the login popup.

### [!UICONTROL Select Accounts]/[!UICONTROL Account Details] tab

**[!UICONTROL Account Name]:** The name to be displayed for the account within Search, Social, & Commerce.

>[!NOTE]
>
>If you have a Search, Social, & Commerce-Adobe Analytics integration and change the name of the search account, then ask your Adobe Account Team to update the mapping.

**[!UICONTROL Linked Ad Accounts]:** (Visible while you're creating an account that uses popup authentication) The ad network account to sync. Choose from the ad accounts linked to your network login.

**[Login Details]:** ([!DNL Yandex] accounts only) The account credentials to use:

* **[!UICONTROL Login]:** The login name or ID to enable API access to the account.

* **[!UICONTROL Password]:** The password for the account.

* **[!UICONTROL Access Key]:** The access key for the developer account to be used.

* **[!UICONTROL Application ID]:** The developer token to use for the account. The same token is used for all [!DNL Yandex] accounts.

* **[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] accounts with the Shared Account setting disabled only; optional) The numeric ID for the campaign used to pay for all ad campaigns in the account.

* **[!UICONTROL Finance Token]:** ([!DNL Yandex] accounts with the Shared Account setting disabled only; optional) The developer token to use for finance-related API calls, such as for reallocating money from the wallet between the advertiser's campaigns as necessary for portfolio optimization.

**[!UICONTROL Currency]:** (Read-only) The abbreviation for the currency used for the account. This value is filled automatically with the currency configured for the account on the ad network once you save the record.

**[!UICONTROL Time Zone]:** The advertiser's time zone. This value is filled automatically with the time zone configured for the advertiser's Search, Social, & Commerce account once you save the record.

**[!UICONTROL Login]:** (Read-only) The user account used to log into the account.

**[!UICONTROL Account Synchronization and Management] > [!UICONTROL Account Enabled]:** Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios.

**[!UICONTROL Account Authentication] > [!UICONTROL Re authenticate]:** (Visible while you're editing an account that uses popup authentication) Refreshes the connection or updates account permissions. The new access token is saved automatically when re-authentication succeeds.

## [!UICONTROL Setup Tracking] tab

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** Whether or not to enable tracking use the Adobe Advertising conversion tracking service. This method generates unique click-tracking IDs and redirects users to the Adobe Advertising server for tracking purposes before sending them to the client's landing page. This method has default tracking options that you optionally can customize, and you also can specify parameters to append to each URL.

To enable this feature, turn on **[Enable Tracking]**.

>[!NOTE]
>
>* If you change this setting, then you must regenerate tracking URLs for the account.
>* Campaign-level tracking options override account-level settings.

**[!UICONTROL Tracking Type]:** (When Search, Social, & Commerce tracking is enabled) The method of redirecting end users to the final URL or destination URL. The selected option is applicable to all bid units in the account or campaign. The default account-level setting is inherited from the advertiser's tracking settings, and the default campaign-level setting is inherited from the account settings.

* *[!UICONTROL Standard]:* To just redirect the end user to the specified URL.

* *[!UICONTROL Token]:* To redirect the end user to the URL and also record the Search, Social, & Commerce ID for the click (`ef_id`) as a query string parameter, which is used as a token. Choose this option if you will report offline transactions, want Search, Social, & Commerce to exchange data with Adobe Analytics, or want to track all conversions that occur within [!DNL Apple Safari] browsers.

>[!NOTE]
>
>* If you switch from [!UICONTROL Standard] to [!UICONTROL Token], or vice versa, then you must regenerate tracking URLs for the account.
>* You can override the account-level setting at the campaign level.

**[!UICONTROL Auto Update]:** (When Search, Social, & Commerce tracking is enabled) Standardizes your tracking URLs for compatibility across browsers and servers. Search, Social, & Commerce automatically uploads the following to the ad network during the next synchronization: (a) Search, Social, & Commerce tracking parameters for tracking templates and the same parameters appended to the final URLs or (b) new destination URLs embedded with Search, Social, & Commerce tracking code. For advertisers with an [Adobe Advertising-Adobe Analytics integration](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) and a server-side AMO ID (s_kwcid) configuration, the upload also includes [AMO ID parameters](/help/integrations/analytics/ids.md#amo-id) for your [!DNL Google Ads] and [!DNL Microsoft Advertising] accounts. The default account-level setting is inherited from the advertiser's tracking settings. You can override the account-level setting at the campaign level. 
  
Tracking URLs are updated daily only for entities that are out of sync (that is, new entities that were added and existing entities whose properties have changed). Therefore, if you change this setting from disabled to enabled for an existing advertiser/account/campaign, then tracking URLs aren't updated for existing entities that are already in sync. To add tracking to the URLs of existing, in-sync entities, contact your Adobe Account Team and request a one-time, manual sync process. The automatic upload process will handle future changes.

**[!UICONTROL URL Encoding]:** (When Search, Social, & Commerce tracking is enabled; accounts with destination URLs only) Encodes the base URL within the end user's browser address bar (such as `%3D` instead of `=`):

**[!UICONTROL Tracking Level]:** (When Search, Social, & Commerce tracking is enabled; available at the account and campaign levels; not applicable to ad networks that are enabled for parallel tracking) The level at which clicks and revenue should be tracked by adding a redirect (when relevant) and append parameters to the relevant URLs:
  
* *[!UICONTROL Keyword]:* To track data at only the keyword level. Not available for [!DNL Yandex].  

* *[!UICONTROL Ad]:* To track data at only the ad level. Not available for [!DNL Naver].
  
* *[!UICONTROL Keyword and Ad]:* To track data at both the keyword and ad levels. Not available for [!DNL Naver] and [!DNL Yandex].

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] and [!DNL Microsoft Advertising] accounts only; optional) Any parameters to append to the end of final URLs to track information; include all parameters that your business must track.

Example: `param1=value1&param2=value2`

Accounts that use Adobe Advertising click tracking must include the ad network's click identifier (`msclkid` for [!DNL Microsoft Advertising]; `gclid` for Google) in the suffix. Accounts with an Adobe Analytics integration must use the AMO ID parameter (beginning with `s_kwcid`). If the account has a server-side AMO ID implementation, then the parameter is added automatically when a user clicks an ad; otherwise, you must manually add it here. See the [required suffix formats for [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) and [required suffix formats for [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* This field isn't updated by the [!UICONTROL Auto Update] tracking setting.
>* Final URL suffixes at lower levels override the account-level suffix. For easier maintenance, use only the account-level suffix unless different tracking for individual account components is necessary. To configure a suffix at the ad group level or lower, use the ad network's editor.

**Account Tracking URL**: ([!DNL Google Ads], [!DNL LY Ads], and [!DNL Microsoft Advertising] accounts only; optional) The default tracking template for the account, which specifies all off-landing domain redirects and tracking parameters and also embeds the final/landing page URL in a parameter. Example: `{lpurl}?source={network}&id=5` or `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` to include a redirect.

* To embed the final URL:

  * ([!DNL Google Ads] and [!DNL Microsoft Advertising] only) For a list of parameters to indicate final URLs in tracking templates, see the ([!DNL Microsoft Advertising] only) [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) or ([!DNL Google Ads] only) the "Tracking template only" parameters in the section on "Available [!DNL ValueTrack] Parameters" in the [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

  * ([!DNL LY Ads] only) Use the parameter `!{lpurl}` to indicate the landing page URL.

* You can optionally include URL parameters and any custom parameters defined for the campaign, separated by ampersands (&), such as `{lpurl}?matchtype={matchtype}&device={device}`.

* You can optionally add third-party redirects and tracking.

* When the campaign settings include "[!UICONTROL EF Redirect]" and "[!UICONTROL Auto Upload]," Search, Social, & Commerce automatically prefixes its own redirect and tracking code when you save the record.

>[!NOTE]
>
>* For [!DNL Google Ads], avoid using macros, which aren't substituted for clicks from sources that enable parallel tracking. If the advertiser must use macros, the Adobe Account Team should work with Customer Support or the implementation team to add them.
>* The tracking template at the most granular level overrides the values at all higher levels. For example, if both the account settings and the keyword settings include a value, then the keyword value is applied.
>* If you update a tracking template at the ad, sitelink, or keyword level, then the relevant ads are resubmitted for review. You can update your tracking templates at the account, campaign, or ad group levels without resubmitting your ads for approval.

## [!UICONTROL Set up Adobe Analytics] tab

These settings are available for advertisers with an [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md).

**[!UICONTROL Adobe Analytics Report Suite]:** (Optional) One or more Analytics report suites to which Search, Social, & Commerce sends data it collects from the ad network, including entity classifications and click data for the account. This feature is available only to supported ad networks.<!-- What are the repercussions of changing the suites? Timing of updated data? -->

For the data to appear in the report suites, either (a) the server-side AMO ID feature must be configured for the account or (b) the advertiser-level setting to "[!UICONTROL Enable Advertising reporting in Analytics]" must be enabled. In addition, the advertiser's [!DNL Analytics] account must be configured to receive data from Search, Social, & Commerce. For more information, contact your Adobe Account Team.

**[!UICONTROL Adobe Analytics Conversion Reporting]: [!UICONTROL Enable conversion reporting in Adobe Analytics]:** ([!DNL Meta Ads] accounts; optional) Appends the [AMO ID (s_kwcid) tracking parameter](/help/search-social-commerce/tracking/amo-id-tracking-parameter.md) to all ads in the campaign. The parameter enables Adobe Analytics to associate conversions with Meta Ads campaigns in the specified report suite, along with the entity classifications and click data.

>[!MORELIKETHIS]
>
>* [About ad network accounts](../ad-network-account-about.md)
>* [Manage merchant center accounts](/help/search-social-commerce/new-ui/set-up/manager-account-manage.md)
>* [Update the s_kwcid tracking code for a [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
