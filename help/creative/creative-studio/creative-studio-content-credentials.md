---
title: Content credentials in Creative Studio
description: Learn how content credentials are automatically attached to content that's generated or edited with generative AI in Creative Studio.
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

# Content credentials in [!UICONTROL Creative Studio]

[!UICONTROL Creative Studio] automatically attaches content credentials to content that's generated or edited with generative AI, so that the provenance of your ad content is recorded as durable, invisible metadata. The credentials follow the standard of the [Coalition for Content Provenance and Authenticity](https://c2pa.org/) (C2PA).

<!--

The existing page is about Creative Cloud, not DX. Should I provide a reference WRT Firefly, or is the in-screen link that's shown in the chatbot adequate?

For more information about content credentials at [!DNL Adobe], see "Partner Models in Adobe products."

-->

## Which actions attach content credentials

Content credentials are automatically attached at the following points in a [!UICONTROL Creative Studio] session:

* **Generation:** When you use the [[!UICONTROL Ad Variations Generator]](/help/creative/creative-studio/creative-studio-manage-standard-ads.md#generate-ad-variations) to generate new background images<!--, headlines, subheadlines, CTAs, or body copy --> for standard ads. <!-- ??? --><!-- Does a credential attach per asset or per variation? -->

* **Editing:** When you use the AI chat interface to modify existing content for standard ads<!-- I don't think this is possible: or dynamically-generated ads-->. Editing an asset that already carries a credential causes the existing [!DNL Creative Studio] credential to be resigned to include the new action. Examples:

  * Cropping an image without a Creative Studio content credential adds a credential.

  * Cropping a generated image without applying any non-AI edits (such as text overlays or drawing), so that the updated image is considered fully generated, re-signs the credential to include the original image as a `parentOf` ingredient and a `c2pa.cropped` action.

<!-- CONFIRM: does editing an asset that already carries a credential update the existing credential, or attach an additional one? -->

>[!NOTE]
>
>[!DNL Creative Studio] preserves any existing credentials that are already attached to uploaded files, including credentials created from Adobe GenStudio and Adobe Experience Manager. When an uploaded file is edited using generative AI, [!DNL Creative Studio] attaches a new credential in addition to the existing credential.

<!-- VERIFY THAT. Describe how the provenance chain looks for the resulting creative — does it list each contributing generative AI model, or just the immediate Creative Studio generation step?] -->

<!-- Do I need this? Seems repetitive:

## Common scenarios

* "I asked the [!UICONTROL Ad Variations Generator] to create a new ad concept, including images, from a text prompt → [PLACEHOLDER: describe what's attached]."

* "I used the AI chat interface to modify an existing image → [PLACEHOLDER]."

* "I attached an asset from my library to an AI chat message and the AI incorporated it into a generated variation → [PLACEHOLDER]."

-->


## Content types and scope

** I THINK THIS IS ONLY FOR IMAGES, NOT TEXT?**

| Content type | Supported elements | AI service that generates the content | Model that generates the credential |
| --- | --- | --- | --- |
| Images | Background image files | Adobe Firefly | Google Gemini Flash |
| Text | Headlines, subheadlines, CTAs, and body copy. | Anthropic Claude | Anthropic Claude |

<!-- CONFIRM whether text content carries its own credential or is covered under the image/creative-level credential.-->

## When does the credential include, and when it created?

For each GenAI generation or alteration, the following are included in the credential. If an asset is altered multiple times, then each operation appears in the credential.

* Timestamp (date + time)
* Model name + version (Adobe Firefly / gemini-flash for images<!-- ; Anthropic claude-sonnet-4-5 for text -->)
* Unique identifier (UUID per operation)

The credential is signed with the full provenance chain when a user downloads an asset or it is sent to be served in an ad.

<!--

[Is there a panel, inspect view, or properties view where a customer can see an attached credential? Describe using a real example, e.g. "Here's what the attached credential looks like after generating an image."]

[Screenshot: the content credentials panel / inspect view populated with real details]
-->

<!-- I think this is already covered:

## What happens as the asset moves

[PLACEHOLDER — describe what's preserved when a Creative Studio asset is:]

* [Saved to a creative library]
* [Downloaded/exported]
* [Attached to a bundle or ad experience and served through Advertising Creative]
* [Received into Creative Studio from an Adobe upstream app or a partner model, and how existing content credentials are updated when that content is then edited with generative AI in Creative Studio]

[Note any format or workflow where behavior differs — for example, whether the credential is preserved differently for standard ads vs. dynamic, catalog-driven creatives.]
 -->


<!--
## Additional resources

[PLACEHOLDER — customer-facing links, e.g. general content credentials / Adobe generative AI transparency resources.]
-->

>[!MORELIKETHIS]
>
>* [About Creative Studio](/help/creative/creative-studio/creative-studio-about.md)
