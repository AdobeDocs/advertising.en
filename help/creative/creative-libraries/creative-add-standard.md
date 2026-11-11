---
title: Add standard creatives to a creative library
description: Learn how to add standard (non-dynamic) creatives to a creative library.
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
TQID: 'https://experienceleague.adobe.com/mgUcE-E6LAIFFU8S5WrUceCQ6ZMSGF9tFkqEfnuKKSQ'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d06c1576-7039-4934-b256-7366e138fbb6
    internal-label: Creative Standard Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Add standard creatives to a creative library

Add standard creatives to your [creative libraries](creative-library-manage.md) to use with standard [ad experiences](/help/creative/experiences/experience-about.md). 

>[!NOTE]
>
> You can include individual creatives directly within ad experiences that don't have defined user targets. You can also group your creatives in [bundles](bundle-manage.md), which you can include in targeted ad experiences.

## Add flexible HTML ads to a creative library {#flexible-creative-add}

You can do either of the following: 

* Upload your own flexible creatives in ZIP files.

* Use any of the predefined flexible creative templates uploaded to your account as a starting point for your own flexible creative.

### Upload your own flexible creatives {#flexible-creative-upload}

You can upload multiple flexible creative units. Flexible creatives must be in ZIP format and can be up to 2 MB. For file requirements, see the [HTML5 creative specification](html5-creative-specification.md).

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Flexible]**.

1. Click **[!UICONTROL Upload New]**.

1. Specify ZIP files in either of the following ways:

   * Drag and drop files on your device or network into the box.
      
   * Click **[!UICONTROL Select a file]** to locate the files on your device or network.

   See the [flexible ad specifications](#flexible-ad-spec).

1. Add or remove flexible creative files:

   * To add a file, click ![Add](/help/creative/assets/create.png "Add") in the upper left and locate the file on your device or network.

   * To remove a file, deselect the check box next to it.

1. (Optional) To preview a creative, click ![Preview](/help/creative/assets/preview.png "Preview") above the image.

1. Specify the [flexible HTML5 ad settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5).

   By default, all creatives you just uploaded are selected. Any settings with only one value apply to all selected creatives; for some settings, you can specify individual values. To enter settings for specific creatives, deselect the check box next to each inapplicable creative.

1. Click **[!UICONTROL Create]**

### Add flexible creatives using a template {#flexible-creative-use-template}

You can use any of the flexible creative templates uploaded to your account to build ads of a predefined size. Once you select a template to use, you'll edit the click tags and attributes.

<!--
Replace last sentence with this if we add the template download feature back:  You can either a\) select a template to use, and then edit the click tags and attributes; or b\) [download a template as a ZIP file](#download-flexible-creative-template), edit the contents offline to build your own creative, and then [upload the edited file as a new creative](flexible-creative-upload).
-->

<!--
 Not currently an option:
You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads.

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."
-->

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Flexible]**.

1. Click **[!UICONTROL Browse System Flexible Templates]**.

1. (Optional) To preview the template, click **[!UICONTROL ...]** next to the template name, and then click **[!UICONTROL Preview]**.

   You can optionally download the template: click **[!UICONTROL ...]** next to the template name, and then click **[!UICONTROL Download]**.

1. Next to the template name, click **[!UICONTROL ...]** and then **[!UICONTROL Use Selected]**.

1. Edit the [flexible HTML5 creative settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) to specify the language and include your own click tags, images, and other attributes.

   The maximum file size of the creative, once it's zipped, is 2 MB.<!-- Still true? -->

1. Add or remove your own flexible creative files:

   * To add a file from your device or network, click ![Add](/help/creative/assets/create.png "Add") in the upper left and locate the file. Select the check box next to the creative, and deselect the check box next to the other creatives, and edit the [flexible HTML5 creative settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) to specify the language and include your own click tags, images, and other attributes.

   * To remove a file, deselect the check box next to it.

1. (Optional) To preview a creative, click ![Preview](/help/creative/assets/preview.png "Preview") above the image.

1. Click **[!UICONTROL Create]**.

## Add a standard display creative to a creative library

Standard display creatives include image and HTML5 creatives, including creatives imported from Adobe Experience Manager and Adobe GenStudio for Performance Marketing.

* Image creatives can be in GIF, JPEG, JPG, or PNG format. The maximum file size is two (2) MB. See the [supported creative sizes](/help/creative/creative-libraries/creative-sizes.md).

* You can add multiple Experience Manager assets, multiple GenStudio experiences, or multiple local HTML5 creatives of a single type (simple or static) at a time. For HTML5 creatives, see the [HTML5 ad specification](/help/creative/creative-libraries/html5-creative-specification.md).

<!--
 Add in when we add this feature back:
You can optionally download a sample HTML5 creative as a ZIP file, edit the contents to build your own creative, and then add the edited file as a new creative.
-->

>[!NOTE]
>
>You can also [add flexible HTML5 creatives](#flexible-creative-add), which are HTML5 creatives with all their attributes as standard HTML tags that you can edit directly within [!DNL Creative].

### From the new UI

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Open the library in either of the following ways:

   * Click the library name.
   
   * Next to the library name, click **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Upload]** > **[!UICONTROL Display]**.

1. Specify the creatives:

   * For local image or HTML5 assets, do either of the following:

     * Drag and drop files on your device or network into the box.
   
     * Click **[!UICONTROL Select a file]** to locate files on your device or network.

   * For approved images in an [Experience Manager library connected to your DSP account](/help/creative/creative-libraries/aem-assets-configure.md), do the following:

     1. Click **[!UICONTROL AEM Asset Library]**.

     1. (If you're not already signed in to your Experience Manager account) Sign in to your Experience Manager account.

     1. Locate and select the files in your [!UICONTROL Assets] or [!UICONTROL Collections] views, and then click **[!UICONTROL Select]** in the upper right.

        <!-- If the existing asset has multiple quality options, [!DNL Creative] downloads the primary asset, or the asset with the highest resolution within some upper limit [verify what it is and how this works]. [If an asset is part of an image set, ... primary asset in the image set. -->

   * For GenStudio experiences, do the following:

     1. Click **[!UICONTROL GenStudio Library]**.

     1. (If you're not already signed in to your GenStudio account) Sign in to your GenStudio account.

        Your display ad experiences are displayed by default. Optionally filter your experiences by campaign or other attributes as needed.

     1. Locate and select the display ad experiences, and then click **[!UICONTROL Select]** in the upper right.

      Each creative variant in a selected experience is imported as a separate HTML5 creative.

1. Add or remove creatives:

   * To add an image, click ![Add](/help/creative/assets/create.png "Add") in the upper left and locate the file on your device or network.

   * To remove an image, deselect the check box next to it.

1. Specify the [HTML5 creative settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5) or [image creative settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image).

   By default, all creatives or GenStudio experiences you just uploaded are selected, and any settings you specify apply to all selected items. Any settings with only one value apply to all selected items. To enter settings for specific creatives or GenStudio experiences, deselect each inapplicable creative or experience.

1. Click **[!UICONTROL Save Creative]**.

### From the legacy UI

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click **[!UICONTROL Switch to classic UI]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Standard Display]**.

1. Specify the creatives:

   * For local image or HTML5 assets, do either of the following:

     * Drag and drop files on your device or network into the box.
   
     * Click **[!UICONTROL Select a file]** to locate files on your device or network.

   * For approved images in an [Experience Manager library connected to your DSP account](/help/creative/creative-libraries/aem-assets-configure.md), do the following:

     1. Click **[!UICONTROL AEM Asset Library]**.

     1. (If you're not already signed in to your Experience Manager account) Sign in to your Experience Manager account.

     1. Locate and select the files in your [!UICONTROL Assets] or [!UICONTROL Collections] views, and then click **[!UICONTROL Select]** in the upper right.

        <!-- If the existing asset has multiple quality options, [!DNL Creative] downloads the primary asset, or the asset with the highest resolution within some upper limit [verify what it is and how this works]. [If an asset is part of an image set, ... primary asset in the image set. -->

   * For GenStudio experiences, do the following:

     1. Click **[!UICONTROL GenStudio Library]**.

     1. (If you're not already signed in to your GenStudio account) Sign in to your GenStudio account.

        Your display ad experiences are displayed by default. Optionally filter your experiences by campaign or other attributes as needed.

     1. Locate and select the display ad experiences, and then click **[!UICONTROL Select]** in the upper right.

      Each creative variant in a selected experience is imported as a separate HTML5 creative.

1. Add or remove creatives:

   * To add an image, click ![Add](/help/creative/assets/create.png "Add") in the upper left and locate the file on your device or network.

   * To remove an image, deselect the check box next to it.

1. Specify the [HTML5 creative settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5) or [image creative settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image).

   By default, all creatives or GenStudio experiences you just uploaded are selected, and any settings you specify apply to all selected items. Any settings with only one value apply to all selected items. To enter settings for specific creatives or GenStudio experiences, deselect each inapplicable creative or experience.

1. Click **[!UICONTROL Create]**.

## Add third-party creatives to a creative library {#creative-add-third-party}

[!DNL Creative] supports ad tags for display creatives hosted on third-party ad servers. In the new UI, you can import one or more creatives from a trafficking sheet. The legacy UI supports entering a tag for a single creative.

### From the new UI

#### Prepare your trafficking sheet {#third-party-sheet-requirements}

* Use an Excel (`.xlsx` or `.xls`), CSV, or TSV file no larger than 10 MB, with no more than 500 creatives.

* For Excel files, put the creatives on the first worksheet. Only the first worksheet is imported. Password-protected files aren't supported.

* Use a [!DNL Flashtalking] or [!DNL Google Campaign Manager 360] export, or prepare a generic sheet. The sheet must match the ad server layout you select when you upload it.

* Include a creative name, size, and ad tag for each creative. Names can contain up to 255 characters. Specify dimensions in a single size column (such as `300x250`) or in separate width and height columns in vendor exports. Use [supported creative sizes](creative-sizes.md).

* For a generic sheet, use the column headers `Creative Name`, `Size`, and `Ad Tag`. You can download a CSV template from the upload dialog. Replace its example row with your own creative data.

>[!IMPORTANT]
>
>* Bulk upload supports display tags only. Video and VAST tags aren't supported.
>* Bulk upload stores ad tags as supplied; it doesn't insert tracking macros or rewrite tracking URLs during import. Include any required [tracking macros](/help/creative/creative-macros.md) in your tags before you upload the sheet.

#### Upload and review the creatives {#third-party-bulk-upload}

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Open the library in either of the following ways:

   * Click the library name.
   
   * Next to the library name, click **[!UICONTROL ...]** > **[!UICONTROL Open]**.
        
1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Add new]** > **[!UICONTROL Upload]** > **[!UICONTROL 3rd Party]**.

   The **[!UICONTROL Bulk upload third-party tags]** dialog opens.

1. Select the **[!UICONTROL Ad server]** that matches your sheet:

   * **[!UICONTROL Flashtalking]**

   * **[!UICONTROL Google CM360]**

   * **[!UICONTROL Generic]**

   You must select an ad server before you can upload a file. The selected ad server applies to every creative in the sheet; it isn't detected from individual tags.

1. (Optional) To prepare a generic sheet, click **[!UICONTROL Download CSV template]**, replace the example data with your own creatives, and save the file.

1. Specify the sheet in either of the following ways:

   * Drag and drop the file into the upload box.

   * Click **[!UICONTROL select a file]** to locate the file on your device or network.

   The sheet is uploaded and analyzed. If its layout doesn't match the selected ad server, then correct the sheet or select the matching ad server, and upload the file again.

1. In **[!UICONTROL Review third-party creatives]**, review the **[!UICONTROL Creative name]**, **[!UICONTROL Size]**, **[!UICONTROL Type]**, **[!UICONTROL Language]**, and **[!UICONTROL Status]** for each row.

   * If the sheet includes multiple tag formats, select the tab for the tag column you want to import. The selected format applies to all rows, and rows with no tag in that column aren't shown. Changing tabs resets the selection to all importable rows for that format.

   * All importable rows are selected by default. Deselect the check box next to any creative you don't want to import.

   * (Optional) Change the **[!UICONTROL Language]** for individual creatives. The default is English.

   * Rows with an **[!UICONTROL Error]** status can't be selected or imported. You can import the valid rows, or click **[!UICONTROL Cancel]**, correct the source sheet, and upload it again. Correct missing names, dimensions, or tags, and remove video tags or any characters flagged as unsupported.

1. Click **[!UICONTROL Import <N> creatives]**, where `<N>` is the number of selected creatives. For a single creative, click **[!UICONTROL Import 1 creative]**.

   The dialog closes, and a notification confirms that the import has started. The creatives appear in the library after processing completes.

To track the import, click ![Job Manager](/help/creative/assets/job-manager.png "Job Manager) (**[!UICONTROL Job Manager]**) in the upper right of any page. If any rows fail during processing, click **[!UICONTROL Download failed rows]** for the import job, correct the downloaded sheet, and upload it again.

### From the legacy UI

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click **[!UICONTROL Switch to classic UI]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.
     
1. Click the library name.
     
1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL 3rd Party]**.

1. Specify the JavaScript tag and other settings for the creative in the [third-party creative settings](#creative-settings-third-party).

   You can copy and paste any of the [available macros](/help/creative/creative-macros.md) into the JavaScript tag.

1. Click **[!UICONTROL Create]**.

## Upload a video creative to a creative library

See the [video creative specifications](/help/creative/creative-libraries/creative-libraries-about.md#creative-video-specs) and the [supported creative sizes](/help/creative/creative-libraries/creative-sizes.md).

### From the new UI

You can upload one video at a time.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Open the library in either of the following ways:

   * Click the library name.
   
   * Next to the library name, click **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Upload]** > **[!UICONTROL Video]**.

1. Specify the video file in either of the following ways:

   * Drag and drop a file on your device or network into the box.
   
   * Click **[!UICONTROL Select a file]** to locate a file on your device or network.

1. Specify the [video creative settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-video).

1. Click **[!UICONTROL Save Creative]**.

### From the legacy UI

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click **[!UICONTROL Switch to classic UI]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Video]**.

1. Specify the video files in either of the following ways:

   * Drag and drop files on your device or network into the box.
   
   * Click **[!UICONTROL Select a file]** to locate files on your device or network.

1. Specify the [video creative settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-video).

   By default, the creative you just uploaded is selected, and any settings you specify apply to the selected creative.<!-- By default, all creatives you just uploaded are selected, and any settings you specify apply to all selected creatives. Any settings with only one value apply to all selected creatives. To enter settings for specific creatives, deselect each inapplicable creative. -->

1. Click **[!UICONTROL Create]**

>[!MORELIKETHIS]
>
>* [Edit standard creatives](/help/creative/creative-libraries/creative-edit-standard.md)
>* [Standard creative settings](/help/creative/creative-libraries/creative-settings-standard.md)
>* [View the change log for a creative](/help/creative/creative-libraries/creative-view-change-log.md)
>* [Available macros for tracking URLs](/help/creative/creative-macros.md)
>* [Supported creative sizes](/help/creative/creative-libraries/creative-sizes.md)
>* [Preview a creative](/help/creative/creative-libraries/creative-preview.md)
>* [Attach and detach creatives from bundles](/help/creative/creative-libraries/creative-attach-detach-bundles.md)
>* [About your creative libraries](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Manage creative libraries](/help/creative/creative-libraries/creative-library-manage.md)
