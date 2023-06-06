---
title: About automating ad management using inventory feeds
description: Learn about advanced campaign management, which allows you to automatically manage account structure and deliver dynamic ads based on data about your product or service inventory.
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

>[!MORELIKETHIS]
>
>* [Workflow for managing campaign data using inventory feeds](inventory-feeds-workflow.md)
>* [When are account components created or deleted by inventory feeds?](when-are-components-created-deleted.md)
