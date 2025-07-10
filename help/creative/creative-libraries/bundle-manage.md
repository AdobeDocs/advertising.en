---
title: Manage creative bundles
description: Learn about xxxx.
feature: Creative Bundles
exl-id: a9ed4e8f-db93-46d5-9231-2b3bb0aa072a
---
# Manage creative bundles

*Closed beta*

<!--
**I'll probably split this up into multiple pages since the creative-related topics are separate**
-->

Bundles are groups of creatives that you can add to an experience as one unit. After you create a bundle container, you can attach creatives to the bundle. Standard display bundles can contain only standard display ads, standard video bundles can contain only standard video ads, and dynamic display bundles can contain only dynamic display ads. You can override the landing pages, impression-tracking tags, and click-tracking tags for all creatives within a bundle that's assigned to an experience from within the experience decision tree, without affecting the base creatives.

[!DNL Creative] rotates through the creatives in the bundle as specified for each experience to which the bundle is assigned. You can optionally allow [!DNL Creative] to optimize the ad elements for any experience based on performance using algorithmic ad rotation, which is powered by Adobe Sensei.

To enable the optimization of ad elements across bundles in an ad experience, each bundle can include only one of each \[creative size + language\] combination. For example, if a bundle includes one 250x250 creative with a default language of "French," then you can't add a second 250x250 creative with a default language of "French." If you have multiple creatives of the same size in the same language, then add them separately to the experience.

Creatives that are attached to bundles are still available as individual creatives. You can add a single creative to multiple bundles. If you edit any settings for a creative that's attached to a bundle, then the changes are propagated to the bundle. However, any custom landing pages, impression-tracking tags, and click-tracking tags configured for the creative within an experience are always used for the experience.

<!-- multiselect only to duplicate and delete -->

## Create a bundle for a creative library

You can attach a creative to multiple bundles.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. In the upper right, click **[!UICONTROL Create]** > **[!UICONTROL Bundles]** > **[!UICONTROL Bundle]**.

1. Enter a unique **[!UICONTROL Bundle Name]** and the **[!UICONTROL Bundle Type]:** *Standard Display* (for standard display creatives), *Dynamic Display* (for dynamic display creatives), *Standard Video* (for standard video creatives).

1. Click **[!UICONTROL Create]**.

## List the creatives in a bundle

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle card or row to view all creatives in the bundle.

## Duplicate bundles

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Select the bundles to duplicate:

   * To duplicate a single bundle:
   
     * In card view, click **[!UICONTROL ...]** next to the bundle name, and then click **[!UICONTROL Duplicate]**.
     
     * In table view, hold the cursor over the row and click **[!UICONTROL Duplicate]**.

   * To duplicate one or more bundles, select the check box for each bundle that you want to duplicate. In the bulk actions toolbar, click **[!UICONTROL Duplicate].**
   
     To select all rows, select the global check box in the upper left.

   The new bundles are named `<original name> (copy) # 1` (or the next number in the sequence). For example, if you make two duplicates of "Test bundle," then the duplicates are named "Test bundle (copy) # 1" and "Test bundle (copy) # 2."

## Edit a bundle name

Changes to a bundle name are propagated across all associated experiences.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Select the bundle:

   * In card view, click **[!UICONTROL ...]** next to the library name, and then click **[!UICONTROL Edit]**.
     
   * In table view, hold the cursor over the row and click **[!UICONTROL Edit]**.

1. Edit the **[!UICONTROL Bundle Name]**.

   The [!UICONTROL Bundle Name] must be unique.

1. Click **[!UICONTROL Update]**.<!-- inconsistent with "Edit" for creative libraries and creatives -->

## Attach creatives to a bundle

You can attach existing standard display creatives to a standard display bundle, standard video creatives to standard video bundles, and dynamic display creatives to a dynamic bundle. Attaching a creative to a bundle makes the creative available in all experiences to which the bundle is assigned. Each bundle can include only one of each \[creative size + language\] combination.

>[!NOTE]
>
>You can also [attach creatives to bundles from the Standard Ads and Dynamic Ads views](creative-attach-detach-bundles.md).

### Attach creatives to a bundle from the Bundles list

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Select the bundle:

   * In card view, click **[!UICONTROL ...]** next to the bundle name, and then click **[!UICONTROL Attach Creatives]**.
     
   * In table view, hold the cursor over the row and click **[!UICONTROL Attach Creatives]**.

   Each creative that's eligible for the bundle type is listed in the right frame. Creatives that are already attached to the bundle are listed but not selectable.

1. (Optional) Switch between the default table view and a card view of the available bundles by clicking ![Card view](/help/creative/assets/card-view-button.png "Card view") to open the card view or ![Table/list view](/help/creative/assets/table-view-button.png "Table view") to return to the table view.

1. In the right frame, select the check box next to each creative to attach to the bundle, and then click **[!UICONTROL Attach Creative to Bundle]**.

### Attach creatives to a bundle from the bundle's creative list 

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle card or row to view all creatives in the bundle.

1. In the upper right, click **[!UICONTROL Attach Creatives]**.

1. In the right panel, select the check box for each creative you want to attach.
   
1. Click **[!UICONTROL Attach Creatives to Bundle]**.

## Detach creatives from a bundle {#bundle-detach-creatives}

Detaching a creative from a bundle removes the association between the two, so that the creative is no longer used for experiences that target the bundle.

Detaching a creative from the bundle doesn't delete the creative from the Creatives tab in your creative library.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle card or row to view all creatives in the bundle.

1. Select the creatives to detach from the bundle:

   * To detach a single creative:
   
     * In card view, click **[!UICONTROL ...]** next to the creative name, and then click **[!UICONTROL Detach]**.
     
     * In table view, hold the cursor over the row and click **[!UICONTROL Detach]**.

   * To detach one or more creatives, select the check box for each creative you want to detach. In the bulk actions toolbar, click **[!UICONTROL Detach]**.
   
     To select all rows, select the global check box in the upper left.

## Preview a single creative in a bundle

You can preview a creative as viewers will see it, including hyperlinks.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle card or row to view all creatives in the bundle.

1. Select the creative:

   * In card view, click **[!UICONTROL ...]** next to the creative name, and then click **[!UICONTROL Preview]**.
   
   * In table view, hold the cursor over the row and click **[!UICONTROL Preview]**.

1. (Optional) To resize the image within the screen, select an option in the **[!UICONTROL Zoom]** list, from 10% to 100% of the image size.

<!-- Not there as of 1/22/24:  1. (Flexible HTML5 creatives; optional) To show all frames for the creative, select **Show frames**. -->

1. (Optional) To open the landing page for the creative, click the creative.

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Optional) To download the creative, click ![Download](/help/creative/assets/download.png "Download").

   The file is downloaded according to your browser's normal procedure.

## Preview all creatives in a bundle

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Select the bundle:

   * In card view, click **[!UICONTROL ...]** next to the bundle name, and then click **[!UICONTROL Preview]**.
   
   * In table view, hold the cursor over the row and click **[!UICONTROL Preview]**.

1. (Optional) To filter the creatives by language, select an option in the **[!UICONTROL Language]** list, and then click **[!UICONTROL Preview]** in the upper right of the preview.

1. (Optional) To filter the creatives by size, select an option in the **[!UICONTROL Size]** list, and then click **[!UICONTROL Preview]** in the upper right of the preview.

1. (Optional) To resize the images within the screen, select an option in the **[!UICONTROL Zoom]** list, from 10% to 100% of the image size.

1. (Optional) To open the landing page for a creative, click the creative.

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Optional) To share a demo URL so that other people without a login to [!DNL Creative] can preview the creatives:

   1. Click ![Share](/help/creative/assets/share.png "Share") in the upper right of the preview.
   
   1. In the [!UICONTROL Share Demo URL] dialog, click **[!UICONTROL Copy]** to copy the URL to your clipboard so that you can share it with someone else.

<!-- Not there as of 1/22/25:

## Edit the landing page and tracking tags for the creatives in a standard creative bundle

*Standard creative bundles only*

[Verify and edit all this, including the command names and where they're available. This is supposed to be a single and bulk action from within the right frame when you've open bundle details for a single bundle -- not from the Bundles table view.]

This procedure customizes the landing page, impression-tracking tags, and click-tracking tags for the creatives only within the context of the bundle. It doesn't change the settings for the base creative in [!UICONTROL Creative Libraries].

The custom URL and tags are applied to a creative when the bundle is assigned to an experience and the creative is served for the experience.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle name.

1. In the right pane, XXXXXXXXXXXX.

1. 

1. Edit any of the following settings: **[!UICONTROL Landing Page]**, **[!UICONTROL Click Tags]**, **[!UICONTROL Impression Tags]**.[Verify, and is can you do this for only one creative or is multiselect available?]

1.

 -->

## Delete bundles

You can delete bundles that aren't assigned to a [live](/help/creative/experiences/experience-about.md#experience-statuses-experience-statuses) experience. If a bundle is assigned to a live experience, then [remove the bundle from the decision tree](/help/creative/experiences/experience-target-node-delete.md) for the experience before you continue.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Select the bundles to delete:

   * To delete a single bundle:
   
     * In card view, click **[!UICONTROL ...]** next to the bundle name, and then click **[!UICONTROL Delete]**.
     
     * In table view, hold the cursor over the row and click **[!UICONTROL Delete]**.

   * To delete one or more bundles, select the check box for each bundle you want to delete. In the bulk actions toolbar, click **[!UICONTROL Delete].**
   
     To select all rows, select the global check box in the upper left.

1. In the confirmation message, click **[!UICONTROL Delete].**

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Assign and unassign creative bundles to a final node in an experience](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Preview a creative](/help/creative/creative-libraries/creative-preview.md)
>* [Add standard creatives to a creative library](/help/creative/creative-libraries/creative-add-standard.md)
>* [Manage creative libraries](/help/creative/creative-libraries/creative-library-manage.md)
>* [About your creative libraries](/help/creative/creative-libraries/creative-libraries-about.md)
