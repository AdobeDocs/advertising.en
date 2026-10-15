---
title: Generate an ad template from an image using AI
description: Learn how to use AI in Creative Studio to convert an existing static display ad image into an editable ad template.
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
# Generate an ad template from an image using AI

*Beta feature*

Use AI in [!UICONTROL Creative Studio] to convert an existing static display ad image into an editable display ad template. Review the generated template, request changes using natural language, and open the template editor to make manual changes and save the template.

## Before you begin

You need an existing static image ad in a Creative Library. This workflow selects ads from your libraries; it doesn't upload a new image directly in the generation dialog.

## Generate and review the template {#template-generate}

1. In the main menu, click **[!UICONTROL Creative Studio]**.

1. Click the **[!UICONTROL Templates]** tab.

1. (Optional) Select an advertiser from the advertiser list at the top of the page to view that advertiser's libraries.

1. In the **[!UICONTROL Use AI to Generate a New Display Ad Template]** card, click **[!UICONTROL Generate]**.

1. In the **[!UICONTROL Generate New Ad Template]** dialog, select **[!UICONTROL Generate from Existing Standard Ad Image]** if it isn't already selected.

1. Select the library containing the image ad from the **[!UICONTROL Ad Library]** list.

1. Hold the cursor over the image ad card and click **[!UICONTROL Use this Standard Ad]**.

   Generation begins automatically, using the selected ad's width and height.

1. Wait for generation to finish, then review the template preview and the **[!UICONTROL Layers]** panel, when available.

   Check the text, images, and layout before using the template. The layers shown here are for review; make manual changes in the template editor.

1. (Optional) Request changes to the generated template:

   1. In the **[!UICONTROL Ask the AI for any changes]** field, describe the changes you want. For example, enter `Change the headline to "Limited Time Offer" and the button text to "Shop Now"`.

   1. Click **[!UICONTROL Regenerate]**.

   1. Review the updated preview. Repeat as needed.

1. When you're ready to continue, click **[!UICONTROL Use this Ad Template]**.

   The generated template opens in the display template editor.

## Edit and save the template {#template-save}

1. In the template editor, review the generated elements and make any remaining changes using the [template editor controls](creative-studio-manage-templates.md#template-controls).

1. Click **[!UICONTROL Save]**.

1. In the **[!UICONTROL Update Template]** dialog, enter or update the **[!UICONTROL Template name]**, select the **[!UICONTROL Advertiser]**, and optionally add tags.

1. Click **[!UICONTROL Update]** to save the template and return to the **[!UICONTROL Templates]** view.

   To save a separate copy instead, click **[!UICONTROL Save As New]**.

You can then use the template to [generate ad variations](creative-studio-manage-templates.md#ad-variations-generate).

## If you can't generate a template {#troubleshooting}

* **No libraries or image ads are listed:** Check the selected advertiser and **[!UICONTROL Ad Library]**. If the library has no standard ad images, select another library containing an existing static image ad.

* **Generation fails or the image can't be converted:** Review the displayed message, click **[!UICONTROL Back to library]**, and select an image ad to try again.

>[!MORELIKETHIS]
>
>* [Manage ad templates in Creative Studio](creative-studio-manage-templates.md)
>* [Manage standard ads in Creative Studio](creative-studio-manage-standard-ads.md)