---
title: Replicate [!DNL Google Ads] campaigns in [!DNL Microsoft® Advertising]
description: Learn how to export your synced campaigns in a [!DNL Google Ads] account directly into a synced [!DNL Microsoft® Advertising] account.
exl-id: 1bb0d915-bf33-4c50-88a5-268d4de5ccff
---
# Replicate [!DNL Google Ads] campaigns in [!DNL Microsoft® Advertising]

You can export your synced campaigns in a [!DNL Google Ads] account directly into a synced [!DNL Microsoft® Advertising] account as enhanced CPC (eCPC) campaigns. The existing bids and campaign budgets are scaled. Existing Search, Social, & Commerce tracking isn't imported.

You can replicate the following types of campaigns and their campaign structure:

* [!DNL Google Ads] search and display campaigns into [!DNL Microsoft® Advertising] search and display campaigns.

* [!DNL Google Display Network] campaigns, including ad images, into [!DNL Microsoft® Advertising] audience campaigns on the Microsoft® Audience Network.

  If you want to replicate shopping feed-based display campaigns, then first replicate your [!DNL Google Merchant Center] product offers to [!DNL Microsoft® Merchant Center]. When you replicate the campaigns, select the [!DNL Microsoft® Merchant Center] store in the Import Options to link the store to your feed-based audience campaigns.

* [!DNL Google Ads] performance max campaigns, including local inventory ads, into [!DNL Microsoft® Advertising] smart shopping campaigns.

You can choose to update the campaigns once; daily weekly, or monthly; or according to [!DNL Microsoft® Advertising]'s recommended schedule. You can optionally configure notifications every time an import job runs or when errors or changes occur. Once you import your campaigns into [!DNL Microsoft® Advertising], you can check the status of your import job, review any error logs, manually run an import job, and edit, pause, enable, or delete your import schedule.

Not all campaign information is replicated, and you may need to add some information to your [!DNL Microsoft® Advertising] campaigns. For more information about what data is imported, see [!DNL Microsoft® Advertising] help on "[What gets imported from [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851)." Because Search, Social, & Commerce tracking isn't imported, you should also add tracking within the [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), or [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) settings. 

## Replicate [!DNL Google Ads] campaigns

>[!NOTE]
>
>If you want to replicate shopping feed-based display campaigns, first [replicate your [!DNL Google Merchant Center] product offers in [!DNL Microsoft® Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). When you replicate the campaigns, select the [!DNL Microsoft® Merchant Center] store in the import options to link the store to your feed-based audience campaigns. 

See [what's imported from [!DNL Google Ads] campaigns](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Get an import credential ID from [!DNL Microsoft® Advertising] to represent your [!DNL Google Ads] credentials.

   Auto-generation of [!DNL Microsoft® Advertising] credentials for import is unavailable because of [!DNL Microsoft® Advertising] API limitations. Contact Adobe technical support or your Adobe Account Team, and they'll generate the credentials and give you the ID.

   You must have the ID to configure the import job.

1. In the Search, Social, & Commerce main menu, click **[!UICONTROL Search] > [!UICONTROL Tools] > [!UICONTROL Import Campaigns]**.

1. Click **[!UICONTROL +Import]**.

1. Specify the [import settings](#campaign-import-settings):

   1. In the **[!UICONTROL Select accounts]** section, select the source and destination accounts and the credential ID that [!DNL Microsoft® Advertising] requires.

   1. In the **[!UICONTROL Select campaigns & ad groups]** section, specify the campaigns and ad groups to import.

   1. In the **[!UICONTROL Customize your import]** section, specify the item types to import.

   1. In the **[!UICONTROL Set schedule]** section, specify when to run the import job.

1. Click **[!UICONTROL Post]**.

1. (Optional) Add Search, Social, & Commerce tracking within the [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), or [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) settings.

## Edit details for a campaign import job

See [what's imported from [!DNL Google Ads] campaigns](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Tools] > [!UICONTROL Import Campaigns]**.

1. Select the check box next to the import job, and then click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Edit the [import settings](#campaign-import-settings).

   1. In the **[!UICONTROL Select accounts]** section, select the source and destination accounts and the credential ID that [!DNL Microsoft® Advertising] requires.

   1. In the **[!UICONTROL Select campaigns & ad groups]** section, specify the campaigns and ad groups to import.

   1. In the **[!UICONTROL Customize your import]** section, specify the item types to import.

   1. In the **[!UICONTROL Set schedule]** section, specify when to run the import job.

1. Click **[!UICONTROL Post]**.

## View your campaign import jobs

You can list all import jobs, including the source [!DNL Google Ads] account, the target [!DNL Microsoft® Advertising] account, the import time or schedule, and the user who created the job. When you run an import job multiple times, including during regularly scheduled imports, each occurrence is listed as a separate job.

* Do either of the following:
  
  * In the main menu, click **[!UICONTROL Search] > [!UICONTROL Tools] > [!UICONTROL Import Campaigns]**.
    
    By default, the view opens to the [!UICONTROL List of Import Jobs] tab.

  * From the [[!UICONTROL Import Logs] tab](#campaign-import-log), click the **[!UICONTROL List of Import Jobs]** tab. 

## Run a campaign import job

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Tools] > [!UICONTROL Import Campaigns]**.

1. Select the check box next to the import job.

1. Click ![Run now](/help/search-social-commerce/assets/run.png "Run now").
 
## View logs for your campaign import jobs {#campaign-import-log}

You can list all completed or failed import jobs, including the start time, the source [!DNL Google Ads] account, the target [!DNL Microsoft® Advertising] account, the user who created the job, the number of successful and failed operations, and any email addresses that received notifications for each job. You can view further details about the changes to the target [!DNL Microsoft® Advertising] account that occurred for each job, including the number of items added, synced, deleted, and that produced errors for each entity level (such as campaign or keyword) in the account.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Tools] > [!UICONTROL Import Campaigns]**.

1. Click the **[!UICONTROL Import Logs]** tab.

1. (Optional) To view details for any import job, click the value in the [!UICONTROL Summary] column.

## Campaign import job settings {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** The synced [!DNL Google Ads] account from which campaign data is exported.

**[!UICONTROL Credential ID]:** An ID that [!DNL Microsoft® Advertising] uses to represent your [!DNL Google Ads] credentials.

Auto-generation of [!DNL Microsoft® Advertising] credentials for import is unavailable because of [!DNL Microsoft® Advertising] limitations. Contact Adobe technical support or your Adobe Account Team, and they'll generate the credentials and give you the ID.

**[!UICONTROL Target Microsoft® Ads account]:** The synced [!DNL Microsoft® Advertising] account into which campaign data is imported.

### [!UICONTROL Select campaigns & ad groups]

**\[Data to import\]:** Specify the data to import:

* *[!UICONTROL Import all new and existing campaigns]:* To import data for all campaigns that already  exist and campaigns that don't exist in [!DNL Microsoft® Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* To select specific campaigns and ad groups.
  
  * To expand a campaign into its child ad groups, click **[!UICONTROL >]** after the campaign name.
  
  * To select a campaign or ad group, select the item so that a checkmark appears.
  
  * To remove a campaign or ad group:
    
    * In the [!UICONTROL Campaigns] or [!UICONTROL Adgroups] column, deselect the campaign or ad group so that the checkmark disappears.
    
    * In the [!UICONTROL Selected] column, click ![Delete](/help/search-social-commerce/assets/delete.png "Delete").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Allows you to specify what to import, bids and budgets, and other options.

**[!UICONTROL What to import]:** Defines the items to import. Options to import item categories are selected by default, with all items types selected. To include only specific item types, click **[!UICONTROL Show advanced options]** and change the item types to include.

**[!UICONTROL Bids and budgets]:** Defines which bid and budget settings to import, update, and customize.

**[!UICONTROL Other options]:** Defines how to handle imported landing page URLs, tracking templates, and other campaign, ad, and targeting options.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** The name of the import job.

**[!UICONTROL When]:** When to import the specified campaigns: *Auto* (to let [!DNL Microsoft® Advertising] set a schedule to best optimize your campaigns), *[!UICONTROL Now]* (to run the job when you post the job settings), *[!UICONTROL Once]* at a specified time, *[!UICONTROL Daily]* at a specified time, *[!UICONTROL Weekly]* at a specified time, or *[!UICONTROL Monthly]* at a specified time.

**[!UICONTROL Receive email notifications]:** If and when to send email notifications about import jobs to the email addresses in the Send reports to field.

**[!UICONTROL Send reports to]:** Email addresses to receive notifications about import jobs. Separate multiple addresses with commas (`,`).
