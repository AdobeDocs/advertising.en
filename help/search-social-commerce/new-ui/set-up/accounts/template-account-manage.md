---
title: (New UI) Manage [!DNL Naver] accounts for tracking only
description: Learn how to set up and manage account details in the new UI for a [!DNL Naver] account.
feature: Search Campaign Management
---
# (New UI) Manage [!DNL Naver] accounts for tracking only

*Beta feature*

Following are instructions for managing [[!DNL Naver] accounts](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) to track, report on, and visualize performance for the ads that you buy directly from the ad network. Search, Social, & Commerce doesn't synchronize data with the ad network, provide automated bidding, nor provide any type of optimization or simulations.

For details about the functionality available, see "[Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md)."

## Create ad network account details {#create-account}

To enable tracking of an account, you must create a corresponding account record containing the account access credentials and with the status *enabled*.

>[!NOTE]
>
>To create an actual account on the ad network, go to the ad network's website.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Click **[!UICONTROL Create Account]**.

1. Click the name of the ad network, and then click **[!UICONTROL Next]**.

1. Specify the [account settings](#account-settings-naver):

   1. On the **[!UICONTROL Enter Account Details]** tab, specify the general account settings.

   1. (Advertisers with an [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md)) Click the **[!UICONTROL Set up Adobe Analytics]** tab, and select all [!DNL Analytics] reporting suites to use for tracking and reporting campaign activity.

1. Click **[!UICONTROL Save]**.

## Edit ad network account details {#edit-account}

To change the account name, change the account status, or change the [!DNL Analytics] report suites to use for tracking and reporting, edit the account details.

>[!NOTE]
>
>To edit an actual account on the ad network, go to the ad network's website.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Select the account in either of the following ways:

   * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

   * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.

1. Edit the [account settings](#account-settings-api):

   1. (Optional) On the **[!UICONTROL Account Details]** tab, edit the account details.

   1. (Optional; advertisers with an [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md)) Click the **[!UICONTROL Set up Adobe Analytics]** tab, and edit the [!DNL Analytics] reporting suites to use for tracking and reporting campaign activity.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Click **[!UICONTROL Save]**.

<!-- What does this do?

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

-->

## Ad network account settings {#account-settings-api}

### [!UICONTROL Account Details] tab

#### [!UICONTROL Enter Account Details]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** The name to be displayed for the account within Search, Social, & Commerce. 

>[!NOTE]
>
>If you have a Search, Social, & Commerce-Adobe Analytics integration and change the name of the search account, then ask your Adobe Account Team to update the mapping.

**[!UICONTROL Network Account ID]:** The account ID assigned by the ad network. 

**[!UICONTROL Currency]:** The abbreviation for the currency used for the account.

**[!UICONTROL Time Zone]:** The advertiser's time zone.

**[!UICONTROL Account Synchronization and Management] > [!UICONTROL Account Enabled]:** Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios.

## [!UICONTROL Setup Analytics] tab

**[!UICONTROL Adobe Analytics Report Suite]:** (Advertisers with an [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md); optional) One or more Analytics report suites to which Search, Social, & Commerce sends data you upload for the ad network, including entity classifications and click data for the account.

For the data to appear in the report suites, either (a) the server-side AMO ID feature must be configured for the account or (b) the advertiser-level setting to "[!UICONTROL Enable Advertising reporting in Analytics]" must be enabled. In addition, the advertiser's [!DNL Analytics] account must be configured to receive data from Search, Social, & Commerce. For more information, contact your Adobe Account Team.

>[!MORELIKETHIS]
>
>* [Implement [!DNL Naver] tracking-only accounts](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [About ad network accounts](/help/search-social-commerce/new-ui/set-up/accounts/ad-network-account-about.md)
