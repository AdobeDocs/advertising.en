---
title: Settings for non-targeted experiences
description: See descriptions of all settings for ad experiences without decision tree targeting.
feature: Creative Experiences
exl-id: aeeca035-8ae2-4173-827a-b8690d228549
---
# Settings for non-targeted experiences

*Closed beta*

## [!UICONTROL Experience basics] section

**[!UICONTROL Advertiser]:** (Read-only for existing experiences) The advertiser that will bid on the creatives included in the experience. Once you save the experience, you can't change the advertiser.

**[!UICONTROL Experience Name]:** A unique name for the experience. **Tip:** Use a name that will be easy to find when you use the experience as an ad in Advertising DSP or other DSP.

**[!UICONTROL Creative Library]:** (Read-only for existing experiences) A single creative library to use for the experience. Once you save the experience, you can't change the library.

## [!UICONTROL Default creatives] section

**\[Default creatives specified\]:** The default image creatives to use when a browser can't display creatives assigned to the experience, such as when the browser isn't JavaScript-enabled or the ad server can't personalize the ad because of delays. Include one image creative per ad size for which the experience applies. Your choices determine the creative sizes that can be used for the experience. <!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. -->

For experiences without decision tree targeting, you can override the default creatives with creatives of the same size within [!UICONTROL Tag Manager].<!-- verify -->

* To add a default creative with different dimensions, click **[!UICONTROL + Add Sizes]**, select the check box next to each creative to add from the right pane, and then click **[!UICONTROL Add Creatives]**.

* To delete a default creative, hold the cursor over the creative thumbnail and click ![Delete](/help/creative/assets/delete.png "Delete").

* To delete all default creatives, click ![Delete](/help/creative/assets/delete.png "Delete") **[!UICONTROL Delete all]**.

* To show or hide the Creatives pane on the right, click ![Show/Hide](/help/creative/assets/hide-show-creatives.png "Show/Hide") in the upper right of the right pane.

## [!UICONTROL Targeting] section

**[!UICONTROL Targeting]:** (Read-only for existing experiences) Not applicable when you don't want to enable targeting using a decision tree; keep this option disabled.

**[!UICONTROL Dynamic ads]:** (Read-only for existing experiences) Indicates the experience includes dynamic ads. **Note:** An experience can include either all standard ads or all dynamic ads.

**[!UICONTROL Language Targeting]:** (Experiences with standard ads only; optional; read-only for existing experiences) Checks the user's browser language settings and displays a creative in the specified language when a creative in that language is available. When a creative in the browser-specified language isn't available, the [!UICONTROL Preferred language] setting is used instead. Once you save the experience, you can't change this setting. 

**[!UICONTROL Preferred language]:** (Experiences with standard ads only; read-only for existing experiences) The language for all ads created from the experience, except when [!UICONTROL Language Targeting] is enabled. Once you save the experience, you can't change this setting.

## [!UICONTROL Advanced] section

**Data Pass:** (Experiences with dynamic ads only; optional) To target users based on specific key-value pairs that the DSP, publisher, or partner passes in real time on impression. You can specify up to five data pass keys (parameters).<!-- May move this to just within the decision tree. -->

When you later create an ad experience tag for a specific creative size, each key that's specified in this field is appended as a macro in the tag. You must enter the value for each key-value pair within the tag before you implement the tag as an ad in your DSP.

**Radius:** (Experiences with dynamic ads only; optional) A radius from a United States zip code specified in the feed file to target; select a radius from 0 miles to 200 miles. The feed file used to create the dynamic ads for the experience must include a [!UICONTROL ZIP] column<!-- or a user-named column mapped to a ZIP column --> with a value for each product row in the file. For example, for a radius of 10 miles, an ad for a product available in 95110 can be displayed to users within 10 miles of 95110.

**RT Pixel:** (Experiences with dynamic ads only; optional) A [!UICONTROL Creative] retargeting pixel to potentially target. When you set up targeting within the decision tree, you can include one level of RT pixel target nodes and specify the pixel to target for each node as well as and the required values for the pixel's attributes that must be present in order to show the creatives in the assigned creative bundles. If you don't specify a pixel in this field, you can still specify one within the decision tree.<!-- From R: "the RT Pixel should be via the content selection in the Dynamic ad setup" -- clarify. I do see "Datapass" (oneword) in the dynamic ad settings, but I'm not sure how that setting and this experience-level one work together. -->

**[!UICONTROL Label]:** <!-- should be "Labels" --> (Optional) Any [!DNL Creative]-specific labels to apply to the experience. You can filter experiences by label in the Experiences<!-- sic --> view.

* To select existing labels, click ![Down](/help/creative/assets/chevron-down.png "Down"), and select the check box next to each label to apply.

* To search for existing labels, begin entering a text string within the label name.

* To create a new label to apply, open the list, click **+ Add Label**, enter a new label name in the [!UICONTROL Label] field, and then click **Create**.

* To remove a label, deselect the check box next to the label name.

**[!UICONTROL Impression Tracking URL]:** (Optional) A third-party impression-tracking URL to append to the landing page URL for any ad created from the experience. You can include up to five URLs. To add an additional URL, click ![icon](/help/creative/assets/create.png) **[!UICONTROL Add More] and enter the URL.

Once you enter a URL, all [available macros](/help/creative/creative-macros.md) and the data with which they're substituted are listed further down the page. To insert one of the macros in the URL, hold the cursor over the macro description and click ![Copy to clipboard](/help/creative/assets/copy-to-clipboard.png "Copy to clipboard"), and then paste the macro wherever you want it in the URL field.

>[!NOTE]
>
>* [!DNL Creative] automatically prefixes its own impression-tracking tags to the landing page URL.
>* You can override this URL for any creative in the experience.
>* You also can enter third-party JavaScript impression-tracking code in the [!UICONTROL Client JS] field

**[!UICONTROL Click Tracking URL]:** (Optional) (Optional) A third-party click-tracking URL to append to the landing page URL. You can include up to five URLs. To add an additional URL, click ![icon](/help/creative/assets/create.png) **[!UICONTROL Add More]** and enter the URL.

Once you enter a URL, all [available macros](/help/creative/creative-macros.md) and the data with which they're substituted are listed further down the page. To insert one of the macros in the URL, hold the cursor over the macro description and click ![Copy to clipboard](/help/creative/assets/copy-to-clipboard.png "Copy to clipboard"), and then paste the macro wherever you want it in the URL field.

>[!NOTE]
>
>* [!DNL Creative] automatically prefixes its own impression-tracking tags to the landing page URL.
>* You can override this URL for any creative <!-- creative bundle for targeted experiences -->in the experience.

**[!UICONTROL Client JS]:** (Optional) Any of the following:

* (When the advertiser uses an OBA compliance vendor for the ads) JavaScript code pointing to the ad overlay that allows users to opt out of online behavioral targeting (OBA).

* Any third-party, JavaScript impression tracking code to append to the landing page. **Note:** You also can enter a third-party impression-tracking URL in the [!UICONTROL Impression Tracking URL] field.

>[!MORELIKETHIS]
>
>* [Create an experience without decision tree targeting](experience-create-no-targeting.md)
>* [Edit an experience without decision tree targeting](experience-edit-no-targeting.md)
>* [Available macros for tracking URLs](/help/creative/creative-macros.md)
>* [Manually create an ad tag for an applicable creative size](experience-tag-create-manually.md)
>* [Assign creatives to an ad tag for experiences without targeting](experience-tag-assign-creatives.md)
>* [Customize the tracking URLs for an experience without targeting](experience-tracking-urls-no-targeting.md)
>* [Customize creative optimization and scheduling for an experience without targeting](experience-optimization-scheduling-no-targeting.md)
