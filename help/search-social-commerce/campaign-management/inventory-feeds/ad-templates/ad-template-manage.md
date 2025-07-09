---
title: Manage ad templates for inventory feeds
description: Learn about managing ad templates through which your inventory data can be processed to manage account structure and deliver dynamic ads.
exl-id: b0e540cf-8735-4812-9df5-58f488a25ba5
feature: Search Inventory Feeds
---
# Manage ad templates for inventory feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (delete actions only), and [!DNL Yandex] accounts only*

Before or after you upload data, you can create search-engine specific ad templates through which your data can be processed. You can create templates for text ads and expanded/extended text ads, [!DNL Google Ads] and [!DNL Microsoft Advertising] responsive search ads, and for [!DNL Google Ads] and [!DNL Microsoft Advertising] shopping ads.

You can associate each template with one feed file, [!DNL Google Merchant Center] account, or [!DNL Microsoft Merchant Center] account, and you can associate multiple templates with the same feed file or account. An ad template can include variables, which are substituted with actual data columns from an uploaded file or an account. In most cases, the variables also can include [a modifier group](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) you set up in Search, Social, & Commerce to create multiple ads, keywords, campaigns, or ad groups for each applicable row in the data file. The template options allow you to either create new account structure (campaigns, ad groups, keywords) for the ads or map the ads to the existing account structure.

In addition to creating new templates from scratch, you can optionally create new templates by cloning existing ones and edit existing templates.

Once you create a template and associate it with a data feed file or a merchant center account, you can propagate the data in the file through the template to create campaign data and account structure, optionally creating a bulksheet file for review or for immediate posting to the ad network.

Any template can be activated, paused, or deleted. Feed data can be automatically propagated only through active templates. However, you can manually propagate data through a paused template.

## Create, clone, or edit a feed template

Create separate templates for text and expanded/extended text ads, responsive search ads, [!DNL Google Ads] shopping ads, and [!DNL Microsoft Advertising] shopping ads.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**, which opens to the [!UICONTROL Templates] tab.

1. Do one of the following:

   * To create a template from scratch, click **[!UICONTROL Create/Clone]** in the toolbar above the data table, and then select the applicable ad network.

   * To clone an existing template:

     1. Select the check box next to the template that you want to copy.

     1. In the toolbar above the data table, click **[!UICONTROL Create/Clone]**, and then select the applicable ad network.
   
   * (To edit an existing template) Next to the template name, click ![View/edit settings](/help/search-social-commerce/assets/settings.png "View/edit settings").

1. Specify the settings for the [text ad template](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md), [[!DNL Google Ads] shopping ad template](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md), or [[!DNL Microsoft Advertising] shopping ad template](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md):

   1. At the top of the template settings window, specify the template name and the applicable account.

      When you clone an existing template, rename the new template so that the ads that are created from the new template aren't associated with ads that are created from the source template.

   1. (Optional) In the left column, specify the product feed file or merchant center account whose data will be propagated through the template:

      * (For product feed files) To select a previously-uploaded file, click ![Down arrow](/help/search-social-commerce/assets/arrow-down-dropdown.png "Down arrow") and select a file from the list of available feed files. To upload a new file, specify the file either by entering the full path and file name or by clicking **[!UICONTROL Browse]** to locate the file on your device or network, and then click **[!UICONTROL Upload]**.
      
      * (For a synced merchant center account) Select the account name.

      The columns for the selected file or account are displayed.

   1. On the **[!UICONTROL Account Structure]** tab, specify the account structure settings.

   1. (Text ads only) Click the **[!UICONTROL Keywords]** tab, and specify the keyword settings.
   
   1. (Text and responsive search ads only) Click the **[!UICONTROL Ads]** tab, and do any of the following:
   
      >[!NOTE]
      >
      >* You can include up to four ad variation templates per standard text ad template, five ad variation templates per expanded/extended text ad template, and three ad variation templates per responsive search ad template.
      >* Each ad group can include up to three enabled responsive search ads.
      >* You can't edit existing standard text ad variations, and existing templates no longer generate standard text ads.
      >* If you change an ad variation template, then existing ads may be deleted and new ones may be created when you propagate data through the template, [depending on the ad type and ad network](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md).

      * To add an ad variation, do the following:
      
        1. Click **[!UICONTROL Add Ad Variation]** to create a text ad, **[!UICONTROL Add ETA Variation]** to create an expanded/extended text ad, or **[!UICONTROL Add RSA Variation]** to create a responsive text ad.
      
           Once you specify the ad type, you can create only that ad type with the template.
         
        1. Specify the ad settings.
      
           For responsive search ads, you can include 3-15 headlines and 2-4 descriptions.

        1. (Optional) To pre-fill all alternate ad copy fields with text from the original ad copy fields, select the check box next to **[!UICONTROL Prefill]**.
        
        1. (Optional) To add another set of ad copy to an ad, which may be used if any of the lines in the original ad copy exceed the maximum length once any dynamic parameters are substituted with data during propagation, click **[!UICONTROL Add Alternate]**, and then add the alternate values.

           >[!NOTE]
           >
           >* If the [!UICONTROL Prefill] option is selected, then the alternate fields are pre-filled with the original fields, and you can edit them as needed.
           >* Only the ad copy fields that exceed the maximum length are replaced with the alternate value. For example, if only an original headline or title is too long, then the generated ad variation uses the alternate headline or title and the original descriptions(s). Therefore make sure that the alternate ad copy makes sense when combined with the original ad copy.
           >* If the original ad copy meets the search engine's length requirements, then the alternate ad copy is discarded.
           >* You can specify up to four alternates for each ad copy field.

        * To edit an ad variation, do the following:
         
          1. Edit the ad settings.
          
             For responsive search ads, you can include 3-15 headlines and 2-4 descriptions.
             
          1. (Optional) To pre-fill all alternate ad copy fields with text from the original ad copy fields, select the check box next to **[!UICONTROL Prefill]**.
          
          1. (Optional) To add another set of ad copy to an ad, which may be used if any of the lines in the original ad copy exceed the maximum length once any dynamic parameters are substituted with data during propagation, click **[!UICONTROL Add Alternate]**, and then add the alternate values.

             >[!NOTE]
             >
             >* If the [!UICONTROL Prefill] option is selected, then the alternate fields are pre-filled with the original fields, and you can edit them as needed.
             >* Only the ad copy fields that exceed the maximum length are replaced with the alternate value. For example, if only an original headline or title is too long, then the generated ad variation uses the alternate headline or title and the original descriptions(s). Therefore make sure that the alternate ad copy makes sense when combined with the original ad copy.
             >* If the original ad copy meets the search engine's length requirements, then the alternate ad copy is discarded.
             >* You can specify up to four alternates for each ad copy field.

        * To remove an ad variation, click **[!UICONTROL Remove ETA Variation]** (for expanded/extended text ads) or **[!UICONTROL Remove RSA Variation]** (for responsive search ads) next to the ad variation, as applicable.

   1. (Shopping templates only) Click the **[!UICONTROL Product Groups]** tab, and then specify information about the product groups that you want to target.
   
   1. (Optional) Click the **[!UICONTROL Feed Filters]** tab, and then specify which rows in the feed file to propagate.
   
   1. (Optional) Click the **[!UICONTROL Label Classifications tab]**, and then specify the label classification values to assign to the different campaign components that are created:
   
      1. Click the check box next to **[!DNL \[Component\] Label Classifications]**.
      
      1. For each label classification to assign to the component, do the following:

         1. Click **[!UICONTROL Add Label Classification]**.
         
         1. Select the label classification, and then either select an existing value or enter a new value.

1. Save the template:

   * To simply save the template, click **[!UICONTROL Save]**, and then click **[!UICONTROL Save]** again.
   
   * To save the template and propagate the specified data file through it, click **[!UICONTROL Save]**, and then click **[!UICONTROL Save & Propagate]**.

## Change the status of feed templates

You can activate any paused data feed template or pause any active data feed template.

>[!NOTE]
>
>You can manually propagate data through a paused template, but data isn't automatically propagated through it.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**, which opens to the [!UICONTROL Templates] tab.

1. Select the check box next to each template whose status you want to change.

1. In the toolbar above the data table, click **[!UICONTROL Change Status]**, and then click **[!UICONTROL Activate]** or **[!UICONTROL Pause]**.

## Delete feed templates

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**, which opens to the [!UICONTROL Templates] tab.

1. Select the check box next to each template that you want to delete.

1. In the toolbar above the data table, click **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [About automating ad management using inventory feeds](../inventory-feeds-about.md)
>* [Text ad and responsive search ad template settings](template-text-rsa.md)
>* [[!DNL Google Ads] shopping ad template settings](template-google-shopping.md)
>* [[!DNL Microsoft Advertising] shopping ad template settings](template-microsoft-shopping.md)
>* [Propagate feed data through templates](../feed-data-propagate.md)
