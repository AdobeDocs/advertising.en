---
title: (New UI) Replicate Google Ads campaigns in Microsoft Advertising
description: Learn how to export your synced campaigns in a Google Ads account directly into a synced Microsoft Advertising account.
feature: Search Campaign Management
---
# (New UI) Replicate [!DNL Google Ads] campaigns in [!DNL Microsoft Advertising]

*Beta feature*

You can export your synced campaigns in a [!DNL Google Ads] account directly into a synced [!DNL Microsoft Advertising] account as enhanced CPC (eCPC) campaigns. The existing bids and campaign budgets are scaled. Existing Search, Social, & Commerce tracking isn't imported.

You can replicate the following types of campaigns and their campaign structure:

* [!DNL Google Ads] search and display campaigns into [!DNL Microsoft Advertising] search and display campaigns.

* [!DNL Google Display Network] campaigns, including ad images, into [!DNL Microsoft Advertising] audience campaigns on the Microsoft Audience Network.

  If you want to replicate shopping feed-based display campaigns, then first replicate your [!DNL Google Merchant Center] product offers to [!DNL Microsoft Merchant Center]. When you replicate the campaigns, select the [!DNL Microsoft Merchant Center] store in the import options to link the store to your feed-based audience campaigns.

* [!DNL Google Ads] performance max campaigns, including local inventory ads, into [!DNL Microsoft Advertising] performance max campaigns.

You can choose to update the campaigns once; daily, weekly, or monthly; or according to [!DNL Microsoft Advertising]'s recommended schedule. You can optionally configure notifications every time an import job runs or when errors or changes occur. Once you import your campaigns into [!DNL Microsoft Advertising], you can check the status of your import job, review any error logs, manually run an import job, and edit, pause, enable, or delete your import schedule.

Not all campaign information is replicated, and you may need to add some information to your [!DNL Microsoft Advertising] campaigns. For more information about what data is imported, see [!DNL Microsoft Advertising] help on "[What gets imported from [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851){target="_blank"}." Because Search, Social, & Commerce tracking isn't imported, you should also add tracking within the [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), or [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) settings.

## Replicate [!DNL Google Ads] campaigns

>[!NOTE]
>
>If you want to replicate shopping feed-based display campaigns, first [replicate your [!DNL Google Merchant Center] product offers in [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870){target="_blank"}. When you replicate the campaigns, select the [!DNL Microsoft Merchant Center] store in the import options to link the store to your feed-based audience campaigns.

See [what's imported from [!DNL Google Ads] campaigns](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. Click **[!UICONTROL Import Campaigns]**.

1. Specify the [import settings](#campaign-import-settings).

1. Cick **[!UICONTROL Review and Save]** in the upper right.

1. Review your selections in the summary and click **[!UICONTROL Start Import]**.

1. (Optional) Add Search, Social, & Commerce tracking within the [account](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), or [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) settings.

## Edit schedule settings for a campaign import job

See [what's imported from [!DNL Google Ads] campaigns](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. On the **[!UICONTROL List of Import Jobs]** tab, click the name of the import job, and then click **[!UICONTROL Edit]**.

1. In the **[!UICONTROL Set schedule]** step, specify the [schedule settings](#campaign-import-settings).

1. Click **[!UICONTROL Save]**.

## View your campaign import jobs

You can list all import jobs, including the source [!DNL Google Ads] account, the target [!DNL Microsoft Advertising] account, the import time or schedule, and the user who created the job. When you run an import job multiple times, including during regularly scheduled imports, each occurrence is listed as a separate job.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

   The view opens to the **[!UICONTROL List of Import Jobs]** tab by default.

## Run a campaign import job

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. On the **[!UICONTROL List of Import Jobs]** tab, select the check box next to the import job, and then click **[!UICONTROL Run Now]**.

## View logs for your campaign import jobs {#campaign-import-log}

You can list all completed or failed import jobs, including the start time, the source [!DNL Google Ads] account, the target [!DNL Microsoft Advertising] account, the user who created the job, the number of successful and failed operations, and any email addresses that received notifications for each job. You can view further details about the changes to the target [!DNL Microsoft Advertising] account that occurred for each job, including the number of items added, synced, deleted, and that produced errors for each entity level (such as campaign or keyword) in the account.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. Click the **[!UICONTROL Import Logs]** tab.

1. (Optional) To view details for any import job, click the value in the [!UICONTROL Summary] column.

## Campaign import job settings {#campaign-import-settings}

### [!UICONTROL Select Accounts] tab

**[!UICONTROL Import Name]:** A name to identify the import job.

**[!UICONTROL Source Google Ads account]:** The synced [!DNL Google Ads] account from which campaign data is exported.

**[!UICONTROL Target Microsoft Ads account]:** The synced [!DNL Microsoft Advertising] account into which campaign data is imported.

**[!UICONTROL Credential ID]:** An ID that [!DNL Microsoft Advertising] uses to represent your [!DNL Google Ads] credentials. Auto-generation of [!DNL Microsoft Advertising] credentials for import is unavailable because of [!DNL Microsoft Advertising] limitations. Contact your Adobe Account Team, and they'll generate the credentials and give you the ID.

### [!UICONTROL Select Campaigns & Ad Groups] tab

**\[Data to import\]:** The data to import:

* *[!UICONTROL Import all new and existing campaigns]:* To import data for all campaigns that already exist and campaigns that don't exist in [!DNL Microsoft Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* To select specific campaigns and ad groups.

  * To expand a campaign into its child ad groups, click **[!UICONTROL >]** after the campaign name.

  * To select a campaign or ad group, select the item so that a checkmark appears.

  * To remove a campaign or ad group, deselect the item or click ![Delete](/help/search-social-commerce/assets/delete-new.png "Delete") in the [!UICONTROL Selection] column.

### [!UICONTROL Customize Your Import] tab

**[!UICONTROL Choose specific import options]:** Allows you to specify what to import, bids and budgets, and other options.

**[!UICONTROL What to import]:** Defines the items to import. Options to import item categories are selected by default, with all item types selected. To include only specific item types, click **[!UICONTROL Show advanced options]** and change the item types to include. You can also optionally associate a UET tag ID with any remarketing list or audience that hasn't previously been imported into [!DNL Microsoft Advertising].

**[!UICONTROL Bids and budgets]:** Defines which bid and budget settings to import, update, and customize, including options to increase or decrease bids and budgets by a specified percentage for [!DNL Microsoft Advertising].

**[!UICONTROL Other options]:** Defines how to handle imported landing page URLs, tracking templates, and other campaign, ad, and targeting options, including options to find and replace text and insert suffixes.

### [!UICONTROL Set Schedule] tab

**[!UICONTROL When]:** When to import the specified campaigns: *Auto* (to let [!DNL Microsoft Advertising] set a schedule to best optimize your campaigns), *[!UICONTROL Now]* (to run the job when you post the job settings), *[!UICONTROL Once]* at a specified time, *[!UICONTROL Daily]* at a specified time, *[!UICONTROL Weekly]* at a specified time, or *[!UICONTROL Monthly]* at a specified time.

**[!UICONTROL Receive email notifications]:** Whether and when to send email notifications about import jobs to the addresses in the [!UICONTROL Send reports to] field: *[!UICONTROL No emails]*, *[!UICONTROL Only if there are changes or errors]* (the default), *[!UICONTROL Only if there are errors]*, or *[!UICONTROL Every time this import runs]*.

**[!UICONTROL Send reports to]:** Email addresses to receive notifications about import jobs. Separate multiple addresses with commas (`,`).

>[!MORELIKETHIS]
>
>* [Manage ad network accounts](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
