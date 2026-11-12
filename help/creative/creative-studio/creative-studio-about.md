---
title: About Creative Studio in Advertising Creative
description: Learn how to use Creative Studio to build AI-assisted ad content in Adobe Advertising Creative.
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
# About [!UICONTROL Creative Studio] in [!DNL Advertising Creative]

[!UICONTROL Creative Studio] is an AI-assisted environment where you can build, resize, and refine display ads across multiple formats in a single session. You interact with the AI through a natural-language chat interface to generate and modify ad content &mdash; no manual design work is required for content fields.

## Workspace overview

[!UICONTROL Creative Studio] is organized into three tabs:

**[!UICONTROL Creatives]** &mdash; The starting point for ad creation. Shows your existing creatives generated from Creative Studio, organized into collapsible creative libraries. From here you can generate standard display ads from templates, build dynamic display creatives from catalog data, and manage existing creatives (edit, generate ad variations, preview, duplicate, download, delete, QA, and review change logs). See "[Manage standard ads in Creative Studio](creative-studio-manage-standard-ads.md)" and "[Manage dynamic ads in Creative Studio](creative-studio-manage-dynamic-ads.md)."

**[!UICONTROL Templates]** &mdash; Shows all display and video ad templates available to your account, with filtering by source (All, System Templates, User Templates), status, and ad format. You can preview, favorite, label, download, and delete templates, or start an ad generation session directly from an existing display ad template. See "[Manage templates in Creative Studio](creative-studio-manage-templates.md)."

**[!UICONTROL Assets]** &mdash; Stores images, video, and audio files used in templates and available to attach to AI chat messages during ad generation sessions. You can search, filter, upload, download, and delete assets. See [Manage assets in Creative Studio](creative-studio-manage-assets.md).

## Key capabilities

* **Create and manage ad templates:**

  * **Generate from text using AI:** [Generate display ad templates from a text prompt](creative-studio-manage-templates.md#template-generate-from-text), optionally including a brand profile and an image. Review multiple results, then open a template in the editor to customize and save a new copy.

  * **Generate from an image using AI:** [Convert an existing static display ad image into an editable template](creative-studio-manage-templates.md#template-generate-from-image). Select an image ad from a Creative Library, review the generated template, and request changes using natural language. Open the template editor to make manual changes and save the template.

  * **Create display and video ad templates:** Create and manage both display ad templates and video ad templates. When creating a template, choose **[!UICONTROL Display Ad Template]** or **[!UICONTROL Video Ad Template]** to match your campaign format.

  * **Import HTML5 templates:** Import existing HTML5 ad templates by uploading them as ZIP files. The **[!UICONTROL Import Templates]** dialog lets you assign an advertiser and template name before importing.

  * **Organize templates:** Mark templates as favorites, apply labels, and filter by status, format, or source to keep your template library organized.

* **Create ads:**

  * **Generate standard ad content using AI:** Use the **[!UICONTROL Ad Variations Generator]** to generate ad concepts and variations through a natural-language chat interface. The AI assistant can generate headlines, subheadlines, CTAs, body copy, and background image variations, and can create new size templates in the same session. Up to 10 concepts can be active per session.

  * **Build dynamic creatives using feeds:** For dynamic ad campaigns, connect a product or content catalog to generate ads at scale, then use the AI agent to filter, preview, and quality-check catalog-generated ad combinations.

* **Customize ad content and formats:**

  * **Apply brand guidelines:** When your [brand profile](/help/creative/brands/brand-manage.md) is applied, the AI uses your brand's logos, color palettes, voice guidelines, image standards, and channel guidelines to keep generated content on-brand.

  * **Attach library assets:** Attach images and other assets directly to AI chat messages by selecting from your asset library, keeping visual context available during content generation.

  * **Resize ads:** Resize ads to IAB standard dimensions in a single step. The AI automatically adjusts content placement and sizing for each format, and canvas controls (zoom in/out, fit to screen, replay animations) help you review each size.

## Ad creation workflows

<!-- Add links to the other workflows!!!!! -->

| Workflow | When to use |
| --- | --- |
| [Generate standard ads from a template](creative-studio-manage-standard-ads.md) | Select a display or video template and use the [!UICONTROL Ad Variations Generator] to create AI-generated content variations. Best when a template already exists and you want AI-assisted content generation. |
| [Manage dynamic creatives](creative-studio-manage-dynamic-ads.md) | Connect a product or content catalog to a template, map catalog fields to template elements, then use the AI agent to preview and QA all generated ad combinations. Best for large-scale, catalog-driven campaigns. |
| [Generate a template from text](creative-studio-manage-templates.md#template-generate-from-text) | Describe a display ad template, optionally select a brand profile and an image, and choose from AI-generated results. Best when you want a new template without an existing ad design. |
| [Generate a template from an image](creative-studio-manage-templates.md#template-generate-from-image) | (Beta feature) Convert an existing static display ad image from a Creative Library into an editable template, request changes using natural language, and edit and save the template. Best when you want to use an existing image ad as the starting design. |
| Build a new template | Start from a blank canvas to create a display or video template. Best when no existing template meets your needs. |
| Upload HTML5 templates | Import one or more HTML5 ad templates packaged as ZIP files. Best when you have production-ready HTML5 creatives built outside of [!DNL Advertising Creative]. |

## Standard ads vs. dynamic ads

[!UICONTROL Creative Studio] supports two ad content models that determine how the AI agent behaves:

**Standard ads** &mdash; You supply or generate all ad content. The AI agent can generate, modify, or replace any content field (headlines, CTAs, images, colors, copy tone) within the constraints of the template layout. Completed standard ads are saved to a creative library by selecting an advertiser and library, with an option to attach them to bundles. Standard ads are best for custom-messaging campaigns.

**Dynamic ads** &mdash; Content is driven by a product or content catalog. A four-step guided workflow walks you through selecting a template, mapping catalog fields to template elements, and configuring the ad set. After setup, the AI agent shifts to a QA and preview role: it can filter ads by catalog fields, flag quality issues (character limits, content overflow, broken images, compliance), and analyze combinations across the catalog &mdash; but it can't modify catalog-sourced content directly. To change dynamic ad content, update the source catalog.

>[!MORELIKETHIS]
>
>* [Manage standard ads in Creative Studio](creative-studio-manage-standard-ads.md)
>* [Manage dynamic creatives in Creative Studio](creative-studio-manage-dynamic-ads.md)
>* [Manage templates in Creative Studio](creative-studio-manage-templates.md)
>* [Manage assets in Creative Studio](creative-studio-manage-assets.md)
>* [Manage brand profiles in Advertising Creative](/help/creative/brands/brand-manage.md)
>* [C2PA metadata in [!UICONTROL Creative Studio]](/help/creative/creative-studio/creative-studio-content-credentials.md)
