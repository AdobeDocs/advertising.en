# Ad Descriptions field in RSA ad settings

**[!UICONTROL Ad Descriptions]:** At least two, and up to four, ad descriptions, with optional position pins. The ad network displays ads with up to two descriptions; enter at least two. The maximum length for each description is 90 characters, including any dynamic text (such as the values of keywords and ad customizers).

To insert an ad customizer, use the following formats, where `Default text` is an optional value to insert when your feed file doesn't include a valid value:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

To pin a description to a specific position, select the pin option (such as "[!UICONTROL Pinned at position 1]"). At least one description must be available for each position. If you pin multiple descriptions to the same position, then the final ad always includes one of those descriptions in the specified position. Descriptions pinned to position 2 may not be shown with the ad.

To add an additional description, click **[!UICONTROL + Add]**.
