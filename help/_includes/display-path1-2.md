# Display Path 1 and Display Path 2 fields in some ad settings

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Optional) Text that's added to the display URL that's automatically extracted from the final URL. Each path is preceded in the URL by a forward slash (`/`). A path can't contain forward slash (`/`) or newline (`\n`) characters. The maximum length for each path is 15 characters or 7 double-byte characters.

To insert an ad customizer, use the following formats, where `Default text` is an optional value to insert when your feed file doesn't include a valid value:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

For example, if [!UICONTROL Display Path 1] is "deals" and [!UICONTROL Display Path 2] is "local," then the display URL would be `<display URL>/deals/local`, such as www.example.com/deals/local.
