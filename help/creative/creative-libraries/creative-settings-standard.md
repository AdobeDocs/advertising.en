---
title: Creative settings
description: Learn about xxxx.
feature: Creative Standard Creatives
exl-id: 8eb66310-4860-4ca0-9678-a9e33639c529
---
# Creative settings

*Closed beta*

The settings vary by creative type.

When you edit multiple creatives at the same time:

* You can edit the settings for each creative at the same time or individually. By default, all creatives you chose are selected, and any settings you specify apply to all selected creatives. To edit settings for specific creatives, deselect each inapplicable creative before editing the fields; repeat for additional creatives if necessary.

* Some settings are applied to all selected creatives.

## Flexible HTML5 creative settings {#creative-settings-flexible-html5}

### Details tab

**Creative Name:** The name of the creative. The template name or uploaded file name is used by default, but you can change the name. For multiple creatives, you can edit the individual creative names. **Tip:** Include the ad size in the creative name, and Use a name that you can easily find when you include the creative in an experience.

**Language:** The default language for each ad with which you associate the creatives. When you upload or edit multiple creatives, the same value is applied to each selected creative.

**Creative Size:** (Read-only for existing creatives) The dimensions of the creative. If any images included in the creative are larger than the specified size, they're resized accordingly.

**[!UICONTROL Click Tags]:** The variables that allow click-tracking redirects from the included banner ads. The variable names and corresponding landing page URLs are populated from the uploaded creative unit, but you can change the default URLs. For multiple creatives, you can edit the individual click tags.

<!-- I don't see this as of 1/30. I do see the option to create one custom LP per creative (for any creative type), not one per click tag for flexible HTML5 creatives.
>[!NOTE]
>
>When you include the creative in an experience, you can replace the default value for any of the click tags with a custom landing page URL to generate a derivation of the base creative.
-->

**Label:** (Optional) Any labels to apply to all selected creatives. You can filter creatives by label in various views within [!DNL Creative].

* To select existing labels, click ![Down](/help/creative/assets/chevron-down.png "Down"), and select the check box next to each label to apply.

* To search for existing labels, begin entering a text string within the label name.

* To create a new label to apply to the creatives, open the list, click **+ Add Label**, enter a new label name in the [!UICONTROL Label] field, and then click **Create**.

* To remove a label, deselect the check box next to the label name.

### Attributes tab

**\[All default content attributes applicable to the creative\]:** The default attribute names and values are populated from the flexible creative unit, but you can optionally change the values.

>[!NOTE]
>
>You can also replace the default value for any of the creative attributes with a custom value when you include the creative in an experience. Editing the attributes within an experience creates a variation of the parent creative.

For information about attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."

### Template tab

*Existing creatives only*

The flexible HTML5 template file for the creative.

You can optionally replace the existing template with a new template that has a different layout but the same set of attribute names as the original template. The new template must be in ZIP format with a maximum of 2 MB. When the creative is in a bundle, all experiences that use the bundle subsequently use the layout from the new template.

When you update the template for a parent creative with child variations, the variations are updated with any changes to the template layout, but the attribute values for the variation aren't changed.

To replace the existing ad template:

1. Click **Update Template**.

1. Click **Proceed**.

1. Specify a ZIP file in either of the following ways:

   * Drag and drop a file on your device or network into the box.
      
   * Click **[!UICONTROL select a file]** to locate the file on your device or network.

   See the [flexible ad specifications](#flexible-ad-spec).

1. Edit the new [flexible HTML ad settings](#flexible-ad-settings) as needed.

1. Click **[!UICONTROL Edit]**

## HTML5 creative settings {#creative-settings-html5}

## Details tab

For new creatives, the following settings aren't on a named tab.

**Creative Name:** The name of the creative. For a new creative, the file name is used by default, but you can change the name. For multiple creatives, you can edit the individual creative names. **Tip:** Include the ad size in the creative name, and Use a name that you can easily find when you include the creative in an experience.

**Language:** The default language for each ad with which you associate the creatives. When you upload or edit multiple creatives, the same value is applied to each selected creative.

**Creative Size:** (Read-only for existing creatives) The dimensions of the creative. If any images included in the creative are larger than the specified size, they're resized accordingly.

**[!UICONTROL Click Tags]:** (Static HTML5 creatives only) The variables that allow click-tracking redirects from the included banner ads. The variable names and corresponding landing page URLs are populated from the uploaded creative unit, but you can change the default URLs. For multiple creatives, you can edit the individual click tags.

>[!NOTE]
>
>When you include the creative in an experience, you can replace the default value for any of the click tags with a custom landing page URL to generate a derivation of the base creative.

**Landing Page URL:** (Simple HTML5 creatives with one landing page only) The URL of the default landing page for each ad with which you associate the creatives. It must be a valid URL beginning with http:// or https://. It may include third-party tracking parameters or [[!DNL Creative] macros](/help/creative/creative-macros.md) for your own use.

When you include a creative in a bundle and assign the bundle to an experience, you can optionally change the landing page URL, as well as add impression- and click-tracking URLs and JavaScript, for each creative in the bundle. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Label:** (Optional) Any labels to apply to all selected creatives. You can filter creatives by label in various views within [!DNL Creative].

* To select existing labels, click ![Down](/help/creative/assets/chevron-down.png "Down"), and select the check box next to each label to apply.

* To search for existing labels, begin entering a text string within the label name.

* To create a new label to apply to the creatives, open the list, click **+ Add Label**, enter a new label name in the [!UICONTROL Label] field, and then click **Create**.

* To remove a label, deselect the check box next to the label name.

### Template tab

*Existing static HTML5 creatives only*

The HTML5 template file for the creative.

You can optionally replace the existing template with a new template that has a different layout but the same set of attribute names as the original template. The new template must be in ZIP format with a maximum of 2 MB. When the creative is in a bundle, all experiences that use the bundle subsequently use the layout from the new template.

When you update the template for a parent creative with child variations, the variations are updated with any changes to the template layout, but the attribute values for the variation aren't changed.

To replace the existing ad template:

1. Click **Update Template**.

1. Click **Proceed**.

1. Specify a ZIP file in either of the following ways:

   * Drag and drop a file on your device or network into the box.
      
   * Click **[!UICONTROL select a file]** to locate the file on your device or network.

   See the [HTML ad specifications](html5-creative-specification.md).

1. Edit the new [HTML5 ad settings](#creative-settings-html5) as needed.

1. Click **[!UICONTROL Edit]**

## Image creative settings {#creative-settings-image}

**Creative Name:** The name of the creative. For a new creative, the file name is used by default, but you can change the name. For multiple images, you can edit the individual creative names. **Tip:** Use a name that you can easily find when you include the creative in an experience.

**Language:** The default language for each ad with which you associate the creatives. The same value applies to all selected images. When you include the creatives in an experience, you can optionally customize language preferences for the experience.

**Creative Size:** (Read-only) The dimensions of the uploaded images.

**Landing Page URL:** The URL of the default landing page for each ad with which you associate the creatives. The landing page URL must be a valid URL beginning with http:// or https://. It may include third-party tracking parameters or [[!DNL Creative] macros](/help/creative/creative-macros.md) for your own use. The same value applies to all selected images.

When you include a creative in a bundle and then assign the bundle to an experience, you can optionally change the landing page URL, as well as add impression- and click-tracking URLs and JavaScript, for each creative in the bundle. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Label:** (Optional) Any labels to apply to all selected creatives. You can filter creatives by label in various views within [!DNL Creative].

* To select existing labels, click ![Down](/help/creative/assets/chevron-down.png "Down"), and select the check box next to each label to apply.

* To search for existing labels, begin entering a text string within the label name.

* To create a new label to apply to the creatives, open the list, click **+ Add Label**, enter a new label name in the [!UICONTROL Label] field, and then click **Create**.

* To remove a label, deselect the check box next to the label name.

## Third-party creative settings {#creative-settings-third-party}

**JavaScriptCode:** A JavaScript tag (and optionally an alternate tag for browsers that don't support JavaScript) that points to the creative on the third-party ad server. The script can vary by ad server. When you edit multiple creatives, the same value is applied to each selected creative.

All [available macros](/help/creative/creative-macros.md) and the data with which they're substituted are listed below the input field. To insert one of the macros in the tag, hold the cursor over the macro description and click ![Copy to clipboard](/help/creative/assets/copy-to-clipboard.png "Copy to clipboard"), and then paste the image wherever you want it within the tag.

When you include this creative in an experience that you implement as an ad from a DSP, the DSP uses the information in this tag to display the ad and to track impressions and clicks on it. The DSP then pushes the tag to the ad exchange. When the ad is displayed and clicked, the ad server, the DSP, and [!DNL Creative] track the events.

**[!UICONTROL Advertiser]:** (Read-only) The advertiser to which the library is available.

**Creative Name:** The name of the creative. **Tip:** Use a name that you can easily find when you include the creative in an experience.

**Creative Size:** (Read-only for existing ads) The dimensions of the creative. For new creatives, select from a list of standard ad sizes.
u
**Language:** The default language for each ad with which you associate the creatives.

**Landing Page URL:** The landing page URL used to validate each ad with which you associate the creatives. The third-party ad server determines the actual landing page for each ad.

**Label:** (Optional) Any labels to apply to all selected creatives. You can filter creatives by label in various views within [!DNL Creative].

* To select existing labels, click ![Down](/help/creative/assets/chevron-down.png "Down"), and select the check box next to each label to apply.

* To search for existing labels, begin entering a text string within the label name.

* To create a new label to apply to the creatives, open the list, click **+ Add Label**, enter a new label name in the [!UICONTROL Label] field, and then click **Create**.

* To remove a label, deselect the check box next to the label name.

>[!MORELIKETHIS]
>
>* [Add standard creatives to a creative library](/help/creative/creative-libraries/creative-add-standard.md)
>* [Edit standard creatives](/help/creative/creative-libraries/creative-edit-standard.md)
>* [Available macros for tracking URLs](/help/creative/creative-macros.md)
