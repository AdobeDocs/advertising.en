---
title: Targeted experience settings
description: See descriptions of all settings for targeted ad experiences.
feature: Creative Experiences
exl-id: cb6fd855-6534-4eac-b34b-323073d186be
---
# Targeted ad experience settings

*Closed beta*

## [!UICONTROL Experience basics] section

**[!UICONTROL Advertiser]:** (Read-only for existing experiences) The advertiser that will bid on the creative and target combinations included in the experience. Once you save the experience, you can't change the advertiser.

**[!UICONTROL Experience Name]:** A unique name for the experience. **Tip:** Use a name that you can easily find when you use the experience as an ad in Advertising DSP or other DSP.

**[!UICONTROL Creative Library]:** (Read-only for existing experiences) A single creative library to use for the experience. Once you save the experience, you can't change the library.

## [!UICONTROL Default creatives] section

**\[Default creatives specified\]:** The default image creatives to use when a browser can't display creatives assigned to the experience, such as when the browser isn't JavaScript-enabled or the ad server can't personalize the ad because of delays. Include one image creative per ad size for which the experience applies. Your choices determine the creative sizes that can be used for the experience.<!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. This feels a little wonky in that there isn't a distinct/obvious "Creative Sizes" setting to reference. -->

For experiences with decision tree targeting, you can override the default creatives with creative bundles that contain creatives of the same size from within the decision tree.<!-- verify -->

* To add a default creative with different dimensions, click **[!UICONTROL + Add Sizes]**, select the check box next to each creative to add from the right pane, and then click **[!UICONTROL Add Creatives]**.

* To delete a default creative, hold the cursor over the creative thumbnail and click ![Delete](/help/creative/assets/delete.png "Delete").

* To delete all default creatives, click ![Delete](/help/creative/assets/delete.png "Delete") **[!UICONTROL Delete all]**.

* To show or hide the Creatives pane on the right, click ![Show/Hide](/help/creative/assets/hide-show-creatives.png "Show/Hide") in the upper right of the right pane.

## [!UICONTROL Targeting] section

**[!UICONTROL Targeting]:** (Read-only for existing experiences) Enables creative targeting using a decision tree and automatic tag creation. Once you save the experience, you can't change this setting.

**[!UICONTROL Dynamic ads]:** (Read-only for existing experiences) Indicates that the experience includes dynamic ads. **Note:** An experience can include either all standard ads or all dynamic ads. Once you save the experience, you can't change this setting.

**[!UICONTROL Language Targeting]:** (Experiences with standard ads only; optional; read-only for existing experiences) Checks the user's browser language settings and displays a creative in the specified language when a creative in that language is available. When a creative in the browser-specified language isn't available, the [!UICONTROL Preferred language] setting is used instead.

Once you save the experience, you can't change this setting.

**[!UICONTROL Preferred language]:** (Experiences with standard ads only; read-only for existing experiences) The language for all ads created from the experience, except when [!UICONTROL Language Targeting] is enabled. Once you save the experience, you can't change this setting.

## [!UICONTROL Advanced] section

**Data Pass:** (Read-only for existing experiences; optional) To target users based on specific key-value pairs that the DSP, publisher, or partner passes in real time on impression (such as SKU=01234567890123 or Cart=empty). You can specify up to five default data pass keys (parameters). When you set up targeting within the decision tree, you can include one level of data pass target nodes, optionally customize the keys, and specify the values to target for each node. If you don't specify any keys in this field when you create the experience, you can still specify them within the decision tree.

Each key is appended as a macro in the ad experience tag, which you can generate to implement as an ad in your DSP.

**Radius:** (Experiences with dynamic ads only; optional) A radius from a United States zip code specified in the feed file to target; select a radius from 0 miles to 200 miles. The feed file used to create the dynamic ads for the experience must include a [!UICONTROL ZIP] column<!-- or a user-named column mapped to a ZIP column --> with a value for each product row in the file. For example, for a radius of 10 miles, an ad for a product available in 95110 can be displayed to users within 10 miles of 95110 (determined by the user's IP address).

**RT Pixel:** (Read-only for existing experiences; optional) A [!UICONTROL Creative] retargeting pixel to potentially target. When you set up targeting within the decision tree, you can include one level of RT pixel target nodes. For each node, you'll specify the pixel to target and the values for the pixel's attributes that are required to show the creatives in the assigned creative bundles. If you don't specify a pixel in this field when you create the experience, you can still specify one within the decision tree.<!-- May move this to just within the decision tree. -->

**Label:**<!-- should be "Labels" --> (Optional) Any [!DNL Creative]-specific labels to apply to the experience. You can filter experiences by label in the Experiences view and include the [!UICONTROL Experience Label] dimension in the [!UICONTROL Custom Creative Report].

* To select existing labels, click ![Down](/help/creative/assets/chevron-down.png "Down"), and select the check box next to each label to apply.

* To search for existing labels, begin entering a text string within the label name.

* To create a new label to apply, open the list, click **+ Add Label**, enter a new label name in the [!UICONTROL Label] field, and then click **Create**.

* To remove a label, deselect the check box next to the label name.

**Impression Tracking URL:** (Optional) A third-party impression-tracking URL to append to the landing page URL for any ad created from the experience. You can include up to five URLs. To add an additional URL, click ![icon](/help/creative/assets/create.png) **[!UICONTROL Add More] and enter the URL.

Once you enter a URL, all [available macros](/help/creative/creative-macros.md) and the data with which they're substituted are listed further down the page. To insert one of the macros in the URL, hold the cursor over the macro description and click ![Copy to clipboard](/help/creative/assets/copy-to-clipboard.png "Copy to clipboard"), and then paste the macro wherever you want it in the URL field.

>[!NOTE]
>
>* [!DNL Creative] automatically prefixes its own impression-tracking tags to the landing page URL.
>* You can [override this URL for any creative in the experience](experience-tracking-urls-targeting.md).
>* You can also enter third-party JavaScript impression-tracking code in the [!UICONTROL Client JS] field

**Click Tracking URL:** (Optional) (Optional) A third-party click-tracking URL to append to the landing page URL. You can include up to five URLs. To add an additional URL, click ![icon](/help/creative/assets/create.png) **[!UICONTROL Add More] and enter the URL.

Once you enter a URL, all [available macros](/help/creative/creative-macros.md) and the data with which they're substituted are listed further down the page. To insert one of the macros in the URL, hold the cursor over the macro description and click ![Copy to clipboard](/help/creative/assets/copy-to-clipboard.png "Copy to clipboard"), and then paste the macro wherever you want it in the URL field.

>[!NOTE]
>
>* [!DNL Creative] automatically prefixes its own impression-tracking tags to the landing page URL.
>* You can [override this URL for any creative in the experience](experience-tracking-urls-targeting.md).

**Client JS:** (Optional) Any of the following:

* (When the advertiser uses an OBA compliance vendor for the ads) JavaScript code pointing to the ad overlay that allows users to opt out of online behavioral targeting (OBA).

* Any third-party, JavaScript impression tracking code to append to the landing page. **Note:** You can also enter a third-party impression-tracking URL in the [!UICONTROL Impression Tracking URL] field.

>[!MORELIKETHIS]
>
>* [Create an experience with decision tree targeting](experience-create-targeting.md)
>* [Edit an experience with decision tree targeting](experience-edit-targeting.md)
>* [Available macros for tracking URLs](/help/creative/creative-macros.md)
