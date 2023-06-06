# Text ad template - Campaign Level Negative Keywords settings

**[!UICONTROL Delete negative keywords when omitted from list]:** (All ad networks except Yandex; optional) Deletes existing campaign-level negative keywords previously created using the template that aren't specified in the lists below. **Note:** Negative keywords created using other means (such as in plain bulksheets, the [!UICONTROL Campaigns] views, or in the ad network's ad editor) are never removed using the template.

**[!UICONTROL Set negative keywords by campaign name condition]:** (All ad networks except Yandex; optional) Allows you to specify negative keywords for campaigns whose name includes a specified string. When you select this option, you can add up to three campaign name strings and corresponding keywords.

For each string, click **[!UICONTROL Add (Up to 3)]** and enter the following information:

* **[!UICONTROL If campaign name contains]:**  A text string to look for anywhere within the campaign name. The query is case-sensitive (for example, "[!DNL Car]" matches the campaign name "[!DNL Car Parts]" but not "[!DNL INTERIOR CAR ACCESSORIES]").

* **[!UICONTROL Apply these negatives]:**  Any static campaign-level negative keywords to add for campaigns whose name includes the specified string. To specify multiple keywords or multiple match types for the same keyword, enter them on separate lines. Use the following syntax, without a minus sign:

  * Negative broad match: `keyword` (not supported by [!DNL Microsoft Advertising])
  * Negative phrase match: `"keyword"`
  * Negative exact match: `[keyword]`

The customary syntax for phrase and exact match types is used in the bulksheet that's generated when you propagate feed data through the template. **Note:** You can't see the negative keywords in the [!UICONTROL Keywords] tab or in the [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] view.

**[!UICONTROL All other campaigns: Apply these negatives]:** (All ad networks except [!DNL Yandex]; optional) Any static campaign-level negative keywords to add for campaigns whose name doesn't match a specified string. To specify multiple keywords or multiple match types for the same keyword, enter them on separate lines. Use the following syntax, without a minus sign:

* Negative broad match: `keyword` (not supported by [!DNL Microsoft Advertising])
* Negative phrase match: `"keyword"`
* Negative exact match: `[keyword]`

The customary syntax for phrase and exact match types is used in the bulksheet that's generated when you propagate feed data through the template. **Note:** You can't see the negative keywords in the [!UICONTROL Keywords] tab or in the [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] view.
