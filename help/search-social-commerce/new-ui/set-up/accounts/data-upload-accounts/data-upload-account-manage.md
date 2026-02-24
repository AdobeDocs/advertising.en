---
title: Configure ad network accounts for data upload
description: Learn how to set up and manage account details for an ad network account.
feature: Search Campaign Management
---
# Manage ad network accounts for data uploads

<!-- Edit all, including title and metadata -->

Following are instructions for managing account details for ad network accounts for which you'll upload the account data.

For details about the functionality available for each ad network, see "[Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md)."

>[!NOTE]
>
>For instructions about managing account details for an ad network account that Search, Social, & Commerce syncs using the ad network's API, see "[Manage ad network accounts via API connection](ad-network-account-manage)" instead.

## Create account details {#create-account}

<!-- WORDING???? To enable syncing or tracking of an account, you must create a corresponding account record containing the account access credentials and tracking options and with the status *enabled*. -->

1. Click **[!UICONTROL Create Account]**.

1. Click the name of the ad network, and then click **[!UICONTROL Next]**.

1. Specify the [account settings](#account-settings):

   1. On the **[!UICONTROL Account Details]** tab, edit the account details.

   1. (Advertisers with [!DNL Adobe Analytics for Advertising](/help/integrations/analytics/overview.md)) Click the **[!UICONTROL Set up Adobe Analytics]** tab, and edit the [!DNL Analytics] reporting suites to use for tracking and reporting campaign activity.

   1. (Optional) On the **[!UICONTROL Upload File]** tab, upload data files for the account.

1. Click **[!UICONTROL Save]**.

## Edit account details {#edit-account}

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Select the account in either of the following ways:

   * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the floating toolbar.

   * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.

1. Edit the [account settings](#account-settings-upload):

   1. (Optional) On the **[!UICONTROL Account Details]** tab, edit the account details.

   1. (Optional; advertisers with [!DNL Adobe Analytics for Advertising](/help/integrations/analytics/overview.md)) Click the **[!UICONTROL Set up Adobe Analytics]** tab, and edit the [!DNL Analytics] reporting suites to use for tracking and reporting campaign activity.

   1. (Optional) On the **[!UICONTROL Upload File]** tab, upload data files for the account.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Click **[!UICONTROL Save]**.

<!-- What happens for these account types?

## Enable or disable ad network accounts {#enable-disable-account}

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios. When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):

     * (To enable the account) Select the check box next to the account name, and then click **[!UICONTROL Activate]** in the floating toolbar.

     * (To disable the account) Select the check box next to the account name, and then click **[!UICONTROL Pause]** in the floating toolbar.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the floating toolbar.
        
     1. On the **[!UICONTROL Account Details]** tab, turn off **[!UICONTROL Account enabled]**.

     1. Click **[!UICONTROL Save]**.

-->

## Account settings {#account-settings-upload}

### Account Details tab

**[!UICONTROL Account Name]:** The name to be displayed for the account within Search, Social, & Commerce. 

>[!NOTE]
>
>If you have a Search, Social, & Commerce-Adobe Analytics integration and change the name of the search account, then notify your Adobe Account Team so they can update the mapping.

**[!UICONTROL Network Account ID]:** The account ID assigned by the ad network. This ID is used for reporting only. Search, Social, & Commerce won't connect directly to the ad network account.

**[!UICONTROL Currency]:** (Read-only for existing accounts) The abbreviation for the currency used for the account.

**[!UICONTROL Time Zone]:** (Read-only for existing accounts) The advertiser's time zone.

<!-- Naming here is wrong and misleading -->**[!UICONTROL Account Synchronization and Management] > [!UICONTROL Account Enabled]:** <!-- Verify what exactly happens here --> Search, Social, & Commerce allows data uploads.

## Setup Analytics tab

**Adobe Analytics Report Suite:** (Advertisers with an [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md); optional) One or more Analytics report suites to which Search, Social, & Commerce sends data it collects from the ad network, including entity classifications and click data for the account. This feature is available only to supported ad networks.

For the data to appear in the report suites, either (a) the server-side AMO ID feature must be configured for the account or (b) the advertiser-level setting to "[!UICONTROL Enable Advertising reporting in Analytics]" must be enabled. In addition, the advertiser's [!DNL Analytics] account must be configured to receive data from Search, Social, & Commerce. For more information, contact your Adobe Account Team.

### Upload File tab

(Optional) Upload data files for the account.
