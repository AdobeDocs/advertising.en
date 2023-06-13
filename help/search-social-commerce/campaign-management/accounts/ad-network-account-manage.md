---
title: Manage ad network accounts
description: Learn how to set up and manage account details for an ad network account.
---
# Manage ad network accounts

Following are instructions for creating and editing ad network account details, refreshing the [!DNL oAuth] token for an account, and disabling accounts.

## Create ad network account details {#create-account}

*Agency account manager, Adobe account manager, and administrator user roles only*

To enable syncing or tracking of an account, you must create a corresponding account record containing the account access credentials and tracking options and with the status *active*. For details about the functionality available for each ad network, see "[Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md)."

>[!NOTE]
>
>To create an actual account on the ad network, go to the ad network's website.

1. In the main menu, click **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. In the submenu, click **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Specify the [account settings](#account-settings):

   1. Click the name of the ad network, and then click **[!UICONTROL Next]**.

   1. In the **[!UICONTROL Account Details]** section, enter the account details.

      For ad networks that use the login authorization type "[!UICONTROL oAuth]," allow Search, Social, & Commerce to access the account using the [OAuth authorization protocol](https://oauth.net/2/):

      1. Enter the **[!UICONTROL Login]** value for the account, optionally enter the password, and then click **[!UICONTROL Authenticate]**.

         The best practice is to use the login for API access to the account. Enter the password when you want to encrypt and save it, so that the Adobe Account Team can refresh tokens as needed.

      1. (If you're not logged in to the advertiser's account) Log in to the advertiser's ad account. The best practice is to use the credentials for API access to the account.

      1. In the request for permission/access screen, click the button to confirm permission.

      1. Copy the authentication string in the pop-up window that opens, and paste the string into the **[!UICONTROL oAuth Token]** field.

      1. Specify the remaining account details.

   1. Click **[!UICONTROL Set Account Tracking]**, and enter the tracking settings.

1. Click **[!UICONTROL Post]**.

   Recent cost and click data for all campaigns in the account is available within Search, Social, & Commerce in about 24 hours. By default, data is available for the last 5-10 days, depending on the ad network. When necessary, however, the project launch team may retrieve data for up to the last 60 days.

## Edit ad network account details {#edit-account}

*Agency account manager, Adobe account manager, and administrator user roles only*

If account credentials change, you want to change the default tracking parameters across an account, or you want to enable or disable activity on an account, then edit the account details.

>[!NOTE]
>
>To edit an actual account on the ad network, go to the ad network's website.

1. In the main menu, click **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. In the submenu, click **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Hold the cursor over the account name, click ![More](/help/search-social-commerce/assets/more-filters.png "More"), and then select **[!UICONTROL Edit]**.

1. Edit the [account settings](#account-settings):

   1. (Optional) Edit the account details.

   1. (Optional) Click **[!UICONTROL Set Account Tracking]**, and edit the tracking settings.

1. Click **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >Search, Social, & Commerce must synchronize the new account data with that on the ad network. This happens automatically once a day, or more often when Search, Social, & Commerce detects changes on the ad network.

## Refresh oAuth access tokens for search accounts {#refresh-oauth-tokens}

*Agency account manager, Adobe account manager, and administrator user roles only*

If Search, Social, & Commerce accesses the account using the [OAuth authorization protocol](https://oauth.net/2/) and the account credentials change, or if additional access is required to support new features in Search, Social, & Commerce, then you must get a new access token for the account.

Your Adobe Account Team will inform you if new features require a new token.

1. (If you're logged in to another account for the same ad network in the same browser application) Log out of any account other than the advertiser's.

1. In the main menu, click **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. In the submenu, click **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Hold the cursor over the account name, click ![More](/help/search-social-commerce/assets/more-filters.png "More"), and then select **[!UICONTROL Edit]**.

1. Get a new access token:

   1. Click **[!UICONTROL Get oAuth Token]**.

   1. (If you're not logged in to the advertiser's account) Log in to the advertiser's ad account. The best practice is to use the credentials for API access to the account.

   1. In the request for permission/access screen, click the button to confirm permission.

   1. Copy the authentication string in the pop-up window that opens, and paste the string into the **[!UICONTROL oAuth Token]** field.

1. Click **[!UICONTROL Post]**.

## Enable or disable ad network accounts {#enable-disable-account}

*Agency account manager, Adobe account manager, and administrator user roles only*

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios.When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. In the submenu, click **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (To change the status for a single account) Hold the cursor over the account name, click ![More](/help/search-social-commerce/assets/more-filters.png "More"), and then select **[!UICONTROL Edit]**. Change the **[!UICONTROL Status]** to *Enabled* or *Disabled*, and then click **[!UICONTROL Post]**.

   * (To change the status for one or more accounts) Do the following:

      1. Select the check box next to each account.

         For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

      1. In the toolbar above the data table, click ![Activate icon](/help/search-social-commerce/assets/activate.png "Activate icon") to enable the account or ![Disable icon](/help/search-social-commerce/assets/disable.png "Disable icon") to disable the account.

## Ad network account settings {#account-settings}

>[!NOTE]
>
>Only agency account manager, [!DNL Adobe] account manager, and administrator users can configure account settings.

### Account Details

**[!UICONTROL SE Account ID]:** (All accounts except for [!DNL Naver] and [!DNL Yandex] accounts; editable for new accounts only) The account ID assigned by the ad network. 

>[!NOTE]
>
>Ad network manager accounts aren't supported here. To identify a manager account for [!DNL Microsoft Advertising] or [!DNL Yandex], use the Master Account ID or MCC Account field, respectively. To [set up credentials for a [!DNL Google Ads] manager account](/help/search-social-commerce/admin/manager-accounts.md), go to [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** The name to be displayed for the account within Search, Social, & Commerce. 

>[!NOTE]
>
>If you have a Search, Social, & Commerce-Adobe Analytics integration and change the name of the search account, then notify your Adobe Account Team so they can update the mapping.

**[!UICONTROL Login Details]: \[Login Type\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] only) Whether to authorize logins to the account using:

* *[!UICONTROL oAuth]* (the default): To use the [[!DNL OAuth] authorization protocol](https://oauth.net/2/).

* *[!UICONTROL Password]:* To use the client's password.

For [!DNL Microsoft Advertising] accounts, only [!DNL oAuth]-authorized logins can be used.

**[!UICONTROL Login Details]: [!UICONTROL Login]:** (All ad networks except [!DNL Naver]) The login name or ID to enable API access to the account.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] [!DNL oAuth]-enabled and all other networks except for [!DNL Baidu], [!DNL Meta], and [!DNL Yandex]) The account's token to authorize logins using the [[!DNL OAuth] authorization protocol](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** (All ad networks except [!DNL Naver]) The password for the account. For password-enabled accounts on [!DNL Baidu], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], and [!DNL Yandex], this field is required. For [!DNL oAuth]-enabled accounts, this field is optional; use it when you want to encrypt and save the password so that the account manager can refresh tokens as needed.

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** ([!DNL Baidu] and [!DNL Yandex] accounts only) The access key for the developer account to be used.

**[!UICONTROL Currency]:** The abbreviation for the currency used for the account. This field is editable for new [!DNL Naver] accounts. For all other search networks, the value is filled automatically with the currency configured for the account on the ad network once you save the record.

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] and [!DNL Microsoft Advertising] accounts only; optional) Any parameters to append to the end of final URLs to track information; include all parameters that your business must track.

Example: `param1=value1&param2=value2`

Accounts that use Adobe Advertising click tracking must include the ad network's click identifier (`msclkid` for [!DNL Microsoft Advertising]; `gclid` for Google) in the suffix. Accounts with an Adobe Analytics integration must use the `s_kwcid` parameter. If the account has a server-side s\_kwcid implementation, then the parameter is added automatically when a user clicks an ad; otherwise, you must manually add it here. See the [required suffix formats for [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) and [required suffix formats for [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* This field isn't updated by the [!UICONTROL Auto Upload] tracking setting.
>* Final URL suffixes at lower levels override the account-level suffix. For easier maintenance, use only the account-level suffix unless different tracking for individual account components is necessary. To configure a suffix at the ad group level or lower, use the ad network's editor.

**Time Zone:** (All ad networks except for [!DNL Baidu] and [!DNL Yahoo! Display Network]) The advertiser's time zone. This field is editable and optional for new [!DNL Naver] accounts. For all other search networks, the value is filled automatically with the time zone configured for the advertiser's Search, Social, & Commerce account once you save the record.

**Status:** The account status within Search, Social, & Commerce:

* *Enabled:* Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios.
* *Disabled:* Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is paused. You can later re-activate the account to resume activity with the account.

**Tracking Template** - ([!DNL Google Ads], [!DNL Microsoft Advertising], and [!DNL Yahoo! Japan Ads] accounts only; optional) The default tracking template for the account, which specifies all off-landing domain redirects and tracking parameters and also embeds the final/landing page URL in a parameter. Example: `{lpurl}?source={network}&id=5` or `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` to include a redirect.

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

**[!UICONTROL Master Account ID]:** ([!DNL Microsoft Advertising] accounts only) The ID for an agency/management account associated with the account.

**[!UICONTROL MCC Account]:** ([!DNL Yandex] accounts only; optional) An agency/management account associated with the account. To remove an existing association, select "[!UICONTROL No MCC Account]."

**[!UICONTROL Application ID]:** ([!DNL Yandex] accounts only) The developer token to use for the account. The same token is used for all [!DNL Yandex] accounts.

**[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] accounts with the Shared Account setting disabled only; optional) The numeric ID for the campaign that will be used to pay for all ad campaigns in the account.

**[!UICONTROL Finance Token]:** ([!DNL Yandex] accounts with the Shared Account setting disabled only; optional) The developer token to use for finance-related API calls, such as for reallocating money from the wallet between the advertiser's campaigns as necessary for portfolio optimization.

### Account Tracking

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (For [!UICONTROL EF Redirect] only) Not implemented

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S\_kwcid Format** - (Existing [!DNL Google Ads] accounts for advertisers with an Adobe Advertising-Adobe Analytics integration and for which the s\_kwcid hasn't already been migrated)

This account uses the legacy format for the s\_kwcid tracking code, which allows Adobe Advertising to share data about the account with Adobe Analytics. The [latest format](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md) includes parameters for campaign ID and ad group ID, which are necessary to accurately report at the campaign and ad group levels for [!DNL Google Ads] performance max campaigns and drafts and experiments campaigns in Analytics:

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`
  
If this account needs to report at the campaign and ad group levels, then click the [!UICONTROL Edit] (pencil) icon and then **[!UICONTROL Migrate to new s\_kwcid format]** to change to the new format. For accounts that don't include these campaign types, migrating to the new format is optional but recommended.
  
For full instructions, see "[Update the s\_kwcid tracking code for a [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-skwcid-google.md)."

**Report Suite Names** - (For EF Redirect with token only; advertisers with an Adobe Advertising-Adobe Analytics integration; optional) One or more Analytics report suites to which Search, Social, & Commerce sends data it collects from the ad network, including entity classifications and click data for the account. This feature is available only to supported ad networks. 

For the data to appear in the report suites, either (a) the server-side s\_kwcid must be configured for the account or (b) the advertiser-level setting to "[!UICONTROL Enable tracking for SAINT feeds]" must be enabled. In addition, the advertiser's Analytics account must be configured to receive data from Search, Social, & Commerce. For more information, contact your Adobe Account Manager.

>[!MORELIKETHIS]
>
>* [About ad network accounts](ad-network-account-about.md)
>* [Manage merchant center accounts](merchant-account-manage.md)
>* [Update the s\_kwcid tracking code for a [!DNL Google Ads] account](update-skwcid-google.md)
