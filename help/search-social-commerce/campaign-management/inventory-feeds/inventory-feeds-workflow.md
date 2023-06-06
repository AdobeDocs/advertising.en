---
title: About automating ad management using inventory feeds
description: Learn about the workflow to automatically manage account structure and deliver dynamic ads based on data about your product or service inventory.
---
# Workflow for managing campaign data using inventory feeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (delete actions only), and [!DNL Yandex] accounts only*

Initially, test at least one feed file or account, and then you can fully automate the process or continue to control it at each step:

1. (Optional) Contact your Adobe Account Team to set up an FTP directory for depositing data files.

   If you use the FTP directory, then the feed service checks for new files every two hours.

   Otherwise, you can manually upload files in the [!UICONTROL Advanced (ACM)] view.

1. Set [parameters for processing feed data](feed-settings-manage.md#feed-data-settings).

   If you're using FTP, don't automatically post data to the ad networks initially. After you verify the output from your first file and are satisfied with the results, you can change the settings.

1. Upload a data file to the FTP directory, [manually upload a data file](feed-files-manage.md) in the [!UICONTROL Advanced (ACM) view], or [enable access to a Google or Microsoft® merchant center account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). 

  To manually upload files, you can wait until you create a template that uses the data file.

1. (Optional) Create groups of [modifiers](modifiers-manage.md) to use as variables in various data fields in feed data templates.

1. [Create one or more templates](ad-templates/ad-template-manage.md) that use the data columns to create campaigns, ad groups, keywords, and/or ad copies for a specific ad network account.

1. [Propagate feed data through the templates](feed-data-propagate.md), which substitutes the column names in the template with data in the file or account. Depending on the template options, Search, Social, & Commerce either creates new account structure (campaigns, ad groups, keywords) for the ads using default settings or maps the ads to the existing account structure.

1. (Optional) [Preview the output](propagated-data-view.md) in the [!UICONTROL Advanced (ACM)] views, and optionally view a summary of the data changes on the [!UICONTROL Propagations] tab.

1. [Post the data](propagated-data-post.md) to the relevant ad network accounts.

1. (If you use FTP or a merchant center account to upload your data; optional) After you validate the output from the first feed file, [edit the parameters](feed-settings-manage.md#feed-data-settings) to automatically propagate subsequent data through the associated templates and post it to the relevant ad networks.

1. (When you have new data files) As necessary, upload new files, propagate the data through templates, and post the data to the relevant ad network. You can optionally propagate and post the data in one step.

>[!MORELIKETHIS]
>
>* [About automating ad management using inventory feeds](inventory-feeds-about.md)
>* [When are account components created or deleted by inventory feeds?](when-are-components-created-deleted.md)
