---
title: Manage assets in Creative Studio
description: Learn how to upload, browse, and manage assets in the Creative Studio Assets tab in Adobe Advertising Creative.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Manage assets in [!UICONTROL Creative Studio]

*Beta feature*

Upload images, video, audio, and font assets to reference in ad templates and attach to AI agent chat messages during ad generation sessions.

## The [!UICONTROL Creative Studio] > [!UICONTROL Assets] view

The **[!UICONTROL Assets]** tab lists your existing assets in a card view.

### Available actions

<!--  * [Browse and search assets](#assets-search) -->

* [Upload assets](#assets-upload)

* [Rename an asset](#assets-rename)

* [Download an asset](#assets-download)

* [Delete an asset](#assets-delete)

<!--

Should be in "Common Tasks" chapter

## Browse and search assets {#assets-search}

* Use the **[!UICONTROL Search assets]** field to find assets by name. Enter at least three characters to trigger a search; shorter queries don't filter results.
* Click **[!UICONTROL Filter]** to filter the asset library by type or other attributes.

-->

##  Supported asset types

   <!-- Verified 2026-07-09 against creative-api TemplateMediaValidator.java (IMAGE_EXTENSIONS, VIDEO_EXTENSIONS, AUDIO_EXTENSIONS), which backs the /v1/creative/template-medias upload/initiate endpoint used by this tab. The Assets tab file input has no client-side accept restriction (TemplateBrowser.tsx) and relies entirely on this backend validator, so it is authoritative. -->

   | Type | Supported formats | Maximum file size |
   | --- | --- | --- |
   | Images | JPG/JPEG, PNG, GIF, WebP, SVG | 10 MB |
   | Video | MP4, MOV, AVI, WebM | 512 MB |
   | Audio | MP3, WAV, AAC, OGG | 50 MB |
   | Fonts | TTF, OTF, WOFF, WOFF2 | 5 MB |

## Upload assets {#assets-upload}

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Assets]** tab.

1. Click **[!UICONTROL Upload Assets]**.

1. Select one or more files from your computer or network.

   Empty files and unsupported file types are rejected with an error notification.

   The asset name is saved as the uploaded filename without its extension. Spaces and non-ASCII characters in the filename are replaced with underscores (for example, uploading `My Logo.png` creates an asset named `My_Logo`). You can rename the asset afterward.

## Edit an asset name {#asset-rename}

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Assets]** tab.

1. Hold the cursor over the asset card and click **[!UICONTROL ...]** > **[!UICONTROL Edit name]**.

1. Update the asset name.

   Asset names can be up to 512 characters.

1. Click **[!UICONTROL Update]**.

## Download an asset {#asset-download}

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Assets]** tab.

1. Hold the cursor over the asset card and click **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   The asset downloads according to your browser's normal procedure.

## Delete an asset {#asset-delete}

>[!NOTE]
>
>You can't reactivate a deleted asset.

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Assets]** tab.

1. Hold the cursor over the asset card and click **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [About Creative Studio in Advertising Creative](creative-studio-about.md)
>* [Manage templates in Creative Studio](creative-studio-manage-templates.md)
>* [Generate standard ads in Creative Studio](creative-studio-manage-standard-ads.md)
