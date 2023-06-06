# Ad Titles field in RSA ad settings

**[!UICONTROL Ad Titles]:** At least three, and up to fifteen, ad titles (headlines), with optional position pins. The ad network displays ads with up to three headlines; enter at least three. The maximum length for each title is 30 characters, including any dynamic
text (such as the values of keywords and ad customizers).

To insert an ad customizer, use the following formats, where `Default text` is an optional value to insert when your feed file doesn't include a valid value:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

To pin a title to a specific position, select the pin option (such as "[!UICONTROL Pinned at position 1]"). At least one title must be available for each position. If you pin multiple titles to the same position, then the final ad always includes one of those titles in the specified position. Titles pinned to position 3 may not be shown with the ad.

To add an additional title, click **[!UICONTROL + Add]**.
