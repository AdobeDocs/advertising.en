---
title: (New UI) Manage ad network accounts
description: Learn how to set up and manage account details in the new UI for an ad network synced via the ad network API.
feature: Search Campaign Management
---
# (New UI) Manage ad network accounts via API connection

<!-- Besides just logging into an account, do you have to make any other choices once you're logged in (such as to give speciic permissions to SSC?  And what about oAuth tokens -- do we still use them? -->

*Beta feature*

<!-- Move out info about Naver into a separate page -->

Following are instructions for managing ad network accounts that Search, Social, & Commerce syncs using the ad network's API.

<!-- Move out info about Naver into a separate page -->

For details about the functionality available for each ad network, see "[Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md)."

## Create ad network account details {#create-account}

To enable syncing of an account, you must create a corresponding account record containing the account access credentials and tracking options and with the status *enabled*.

>[!NOTE]
>
>To create an actual account on the ad network, go to the ad network's website.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Click **[!UICONTROL Create Account]**.

1. Click the name of the ad network, and then click **[!UICONTROL Next]**.

1. (All ad networks except for [!DNL Yandex]) Log in to the ad network using the advertiser's credentials. Select the option "Account tracking for this account." Then, in the upper right, click **[!UICONTROL Next]**. 

1. Specify the [account settings](#account-settings-api):

   1. On the **[!UICONTROL Select Accounts]** tab, specify the general account settings. For [!DNL Yandex] accounts, specify the account credentials.

   1. Click the **[!UICONTROL Setup Tracking]** tab, and enter the tracking settings.

   1. (Advertisers with an [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md)) Click the **[!UICONTROL Set up Adobe Analytics]** tab, and select all [!DNL Analytics] reporting suites to use for tracking and reporting campaign activity.

1. Click **[!UICONTROL Save]**.

   Recent cost and click data for all campaigns in the account is updated within Search, Social, & Commerce hourly. By default, data is available for the last 5-10 days, depending on the ad network. When necessary, however, the project launch team may retrieve data for up to the last 60 days.

## Edit ad network account details {#edit-account}

To re-authenticate the account settings to refresh the connection or update permissions, enable or disable activity on an account, change the default tracking parameters across an account, or change the [!DNL Analytics] report suites to use for tracking and reporting, then edit the account details.

>[!NOTE]
>
>To edit an actual account on the ad network, go to the ad network's website.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Select the account in either of the following ways:

   * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

   * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.

1. Edit the [account settings](#account-settings-api):

   1. (Optional) On the **[!UICONTROL Account Details]** tab, edit the account details.

   1. (Optional) Click the **[!UICONTROL Setup Tracking]** tab, and edit the tracking settings.

   1. (Optional; advertisers with an [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md)) Click the **[!UICONTROL Set up Adobe Analytics]** tab, and edit the [!DNL Analytics] reporting suites to use for tracking and reporting campaign activity.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Click **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Search, Social, & Commerce must synchronize the new account data with that on the ad network. This happens automatically once a day, or more often when Search, Social, & Commerce detects changes on the ad network.

## Re-authenticate an ad network account {#reauthenticate}

To refresh the ad network connection or update permissions for the account, re-authenticate the account.

1. (If you're logged in to another account for the same ad network in the same browser application) Log out of any account other than the advertiser's.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

<!-- For Bing and Yandex, the right-click menu includes "Re authenticate." Clarify why just those types -->

1. Select the account in either of the following ways:

   * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

   * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.

1. On the **[!UICONTROL Account Details]** tab, click **[!UICONTROL Re authenticate]** and log in to the ad network using the advertiser's credentials.

1. Click **[!UICONTROL Save]**.

## Enable or disable ad network accounts {#enable-disable-account}

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios. When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):

     * (To enable the account) Select the check box next to the account name, and then click **[!UICONTROL Activate]** in the bulk actions toolbar.

     * (To disable the account) Select the check box next to the account name, and then click **[!UICONTROL Pause]** in the bulk actions toolbar.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.
        
     1. On the **[!UICONTROL Account Details]** tab, turn off **[!UICONTROL Account enabled]**.

     1. Click **[!UICONTROL Save]**.

## Ad network account settings {#account-settings-api}

The account settings vary by ad network. You may not see all settings below.

<!-- When you're creating new accounts only; not sure that you'll have anything to do here once you've authenticated

### Authenticate tab

-->

### [!UICONTROL Select Accounts]/[!UICONTROL Account Details] tab

**[!UICONTROL Account Name]:** The name to be displayed for the account within Search, Social, & Commerce. 

>[!NOTE]
>
>If you have a Search, Social, & Commerce-Adobe Analytics integration and change the name of the search account, then ask your Adobe Account Team to update the mapping.

**[!DNL [Ad Network] Accounts]:** (Visible while you're creating an account) The ad network account to sync. 

**[Login Details]:** (Yandex accounts only) The account credentials to use:

* **[!UICONTROL Login]:** The login name or ID to enable API access to the account.

* **[!UICONTROL Password]:** The password for the account.

* **[!UICONTROL Access Key]:** The access key for the developer account to be used.

* **[!UICONTROL Application ID]:** The developer token to use for the account. The same token is used for all [!DNL Yandex] accounts.

* **[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] accounts with the Shared Account setting disabled only; optional) The numeric ID for the campaign used to pay for all ad campaigns in the account.

* **[!UICONTROL Finance Token]:** ([!DNL Yandex] accounts with the Shared Account setting disabled only; optional) The developer token to use for finance-related API calls, such as for reallocating money from the wallet between the advertiser's campaigns as necessary for portfolio optimization.

**[!UICONTROL Network Account ID]:** (All ad networks except for [!DNL Yandex] The account ID assigned by the ad network. 

>[!NOTE]
>
>Ad network manager accounts aren't supported here. To identify a manager account for [!DNL Microsoft Advertising], use the Master Account ID or MCC Account field, respectively. To [set up credentials for a [!DNL Google Ads] manager account](/help/search-social-commerce/admin/manager-accounts.md), go to [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Currency]:** (Read-only) The abbreviation for the currency used for the account. This value is filled automatically with the currency configured for the account on the ad network once you save the record.

**[!UICONTROL Time Zone]:** The advertiser's time zone. This value is filled automatically with the time zone configured for the advertiser's Search, Social, & Commerce account once you save the record.

**[!UICONTROL Login]:** (Read-only) The user account used to log into the account.

**[!UICONTROL Account Synchronization and Management] > [!UICONTROL Account Enabled]:** Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios.

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

**Account Tracking URL**: ([!DNL Google Ads], [!DNL Microsoft Advertising], and [!DNL Yahoo! Japan Ads] accounts only; optional) The default tracking template for the account, which specifies all off-landing domain redirects and tracking parameters and also embeds the final/landing page URL in a parameter. Example: `{lpurl}?source={network}&id=5` or `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` to include a redirect.

* To embed the final URL:

  * ([!DNL Google Ads] and [!DNL Microsoft Advertising] only) For a list of parameters to indicate final URLs in tracking templates, see the ([!DNL Microsoft Advertising] only) [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) or ([!DNL Google Ads] only) the "Tracking template only" parameters in the section on "Available [!DNL ValueTrack] Parameters" in the [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

  * ([!DNL Yahoo! Japan Ads] only) Use the parameter `!{lpurl}` to indicate the landing page URL.

* You can optionally include URL parameters and any custom parameters defined for the campaign, separated by ampersands (&), such as `{lpurl}?matchtype={matchtype}&device={device}`.

* You can optionally add third-party redirects and tracking.

* When the campaign settings include "[!UICONTROL EF Redirect]" and "[!UICONTROL Auto Upload]," Search, Social, & Commerce automatically prefixes its own redirect and tracking code when you save the record.

>[!NOTE]
>
>* For [!DNL Google Ads], avoid using macros, which aren't substituted for clicks from sources that enable parallel tracking. If the advertiser must use macros, the Adobe Account Team should work with Customer Support or the implementation team to add them.
>* The tracking template at the most granular level overrides the values at all higher levels. For example, if both the account settings and the keyword settings include a value, then the keyword value is applied.
>* If you update a tracking template at the ad, sitelink, or keyword level, then the relevant ads are resubmitted for review. You can update your tracking templates at the account, campaign, or ad group levels without resubmitting your ads for approval.

## [!UICONTROL Setup Analytics] tab

**[!UICONTROL Adobe Analytics Report Suite]:** (Advertisers with an [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md); optional) One or more Analytics report suites to which Search, Social, & Commerce sends data it collects from the ad network, including entity classifications and click data for the account. This feature is available only to supported ad networks.

For the data to appear in the report suites, either (a) the server-side AMO ID feature must be configured for the account or (b) the advertiser-level setting to "[!UICONTROL Enable Advertising reporting in Analytics]" must be enabled. In addition, the advertiser's [!DNL Analytics] account must be configured to receive data from Search, Social, & Commerce. For more information, contact your Adobe Account Team.

>[!MORELIKETHIS]
>
>* [About ad network accounts](ad-network-account-about.md)
>* [Manage merchant center accounts](merchant-account-manage.md)
>* [Update the s_kwcid tracking code for a [!DNL Google Ads] account](update-amo-id-google.md)
