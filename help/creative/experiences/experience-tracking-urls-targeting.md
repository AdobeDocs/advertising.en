---
title: Customize the tracking URLs for an experience
description: Learn how to customize the tracking URLs for each creative in an experience with decision tree targeting.
feature: Creative Experiences
exl-id: ba3b15b4-116e-4caa-8ce1-4d2e488a6362
TQID: 'https://experienceleague.adobe.com/LjeF7eYU8V93W28VbV-D6NNWWwdKqywOP2BwzDwQAgo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# Customize the tracking URLs for creatives in an experience with decision tree targeting

*Target nodes with existing creatives only*

For experiences with decision tree targeting, you can create up to five custom impression-tracking URLs and five custom click-tracking URLs for each individual creative used for the experience. When the landing page override is available, you can also specify one custom landing page URL. You can customize the tracking URLs from within either decision tree editor.

The custom URLs are used only for ads created from the experience and aren't saved in the base creative settings in [!UICONTROL Creative Libraries].

The landing page override is available for standard experiences and for nodes using default creatives. For assigned dynamic bundles, landing pages are determined by the feed, and the landing page tab isn't shown.

## Using the AI-driven editor (Beta) {#ai-editor}

While you're [creating](experience-create-targeting.md#ai-editor) or [editing](experience-edit-targeting.md#ai-editor) the experience, use the canvas controls:

1. On the creative leaf node below the target node, click **[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**.

1. Select the **[!UICONTROL Click Tracking URLs]**, **[!UICONTROL Impression Tracking URLs]**, or (when available) **[!UICONTROL Landing URL]** tab.

   Creatives are grouped by bundle. The default creative sizes for the experience determine the available creative sizes.

1. Expand the creative you want to edit, and do any of the following:

   * To add or edit a custom URL, enter the URL in the input field.

   * To add another custom tracking URL, click **[!UICONTROL Add URL]**, and enter the URL in the input field.

   * To remove a custom URL, click **[!UICONTROL Delete URL]**.

   Click outside an edited field, and correct any validation errors before saving.

1. Click **[!UICONTROL Save]** in the dialog to update the working tree.

1. [Save the experience](#save) from the tree header.

## Using the manual editor {#manual-editor}

[Open the manual editor](experience-edit-targeting.md#experience-open) before following these steps.

1. On the creative leaf node below the target node, click **[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**.

1. Select the **[!UICONTROL Click Tracking URLs]**, **[!UICONTROL Impression Tracking URLs]**, or (when available) **[!UICONTROL Landing URLs]** tab.

   The tabs list the creatives in the assigned bundles. The default creative sizes for the experience determine the available creative sizes.<!-- There's no distinct "Creative Sizes" setting. -->

1. Expand the creative you want to edit, and do any of the following:

   * To add or edit a custom URL, enter the URL in the input field.

   * To add another custom tracking URL, click **[!UICONTROL +]**, and enter the URL in the input field.

   * To remove a custom URL, hold the cursor over the creative row, and click ![Delete](/help/creative/assets/delete.png "Delete").

1. Click **[!UICONTROL Save]** in the dialog to update the working tree.

1. [Save the experience](#save) from the tree header.

## Save the experience {#save}

The following steps apply to both editors. Saving the tracking URL dialog alone doesn't save or publish the experience.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Assign and unassign creative bundles to a final node in an experience](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Customize the tracking URLs for an experience without decision tree targeting](experience-tracking-urls-no-targeting.md)
