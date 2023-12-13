---
title: About automating ad management using inventory feeds
description: Learn about advanced campaign management, which allows you to automatically manage account structure and deliver dynamic ads based on data about your product or service inventory.
exl-id: 46e78f32-96ef-4a23-bbe3-f18b84309463
feature: Search Inventory Feeds
---
# About automating ad management using inventory feeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (delete actions only), and [!DNL Yandex] accounts only*

The [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] view for advanced campaign management allows you to automatically create and update ad network account structure and deliver dynamic ads based on data about your product or service inventory. You can upload new files with product data daily or as often as you like, or link directly to a [!DNL Google] or [!DNL Microsoft®] merchant center account. Use the feature to:

* Build new campaigns from ordered data sources.

* Dynamically update text and responsive search ads, [!DNL Google Ads] shopping ads, or [!DNL Microsoft® Advertising] shopping ads whenever new data is processed, using dynamic variables for changeable data elements (such as the price or quantity). Each time you change the data, the existing ads are deleted and new ones are created.

* Automatically pause or remove ad groups, keywords, and ads when stock dips below a specific level, according to a specified end date, or when an existing component is omitted from feed data.

To set up your ads, create inventory feed templates containing variables (placeholders), and then substitute the variables with actual data columns from an uploaded file or a [Google or Microsoft® merchant center account that is synced](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). The variables can also include modifier groups you set up in a file or individual rows in the file to create multiple ads, keywords, campaigns, or ad groups for each applicable row in the data file. For example, if you use a modifier group variable in an ad headline, and the modifier group includes two modifiers ("for cheap," and "at a discount"), then two separate ads are created for each product &mdash; one for each modifier. For [!DNL Google Ads] and [!DNL Microsoft® Advertising] dynamic search ads, you can also include values for ad customizers.

| [!UICONTROL Ad Variation] Section of Template | Modifiers in Search, Social, & Commerce | Feed Contents | Resulting Ads |
|----|----|----|----|
| Title: Buy high-end \{<i>Product Category</i>\} &lt;<i>CheapList</i>&gt;.<br><br>Description 1: Huge inventory of \{<i>Product Name</i>\}.<br><br>Description 2: Available at \{<i>Discount Percentage</i>\}% discount. | Values for modifier group &quot;CheapList&quot;:<br><br>&quot;for cheap&quot;<br><br>&quot;at a discount&quot; | Product Category,Product Name,Discount Percentage<br>electronics,iPods,10<br><br>apparel,Shirts,15<br><br><b>Note:</b> You can separate values with either commas or tabs. | <u>Buy high-end electronics for cheap.</u><br>Huge inventory of tablets. Available at 10% discount.<br><br><u>Buy high-end electronics at a discount.</u><br>Huge inventory of tablets. Available at 10% discount.<br><br><u>Buy high-end apparel for cheap.</u><br>Huge inventory of shirts. Available at 15% discount.<br><br><u>Buy high-end apparel at a discount.</u><br>Huge inventory of shirts. Available at 15% discount. |

Once you generate the ads, you can optionally review them and then post them to the ad network.

>[!NOTE]
>To create or edit campaign data in bulk using spreadsheet files, see "[About managing campaign data using bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)."

## Workflow for managing campaign data using inventory feeds

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
>* [When are account components created or deleted by inventory feeds?](when-are-components-created-deleted.md)
