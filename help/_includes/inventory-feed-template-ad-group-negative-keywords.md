# Text ad template - Ad Group Level Negative Keywords settings

**[!UICONTROL Delete negative keywords when omitted from list]:** (All ad networks except Yandex; optional) Deletes existing ad group-level negative keywords previously created using the template that aren't specified in the lists below. **Note:** Negative keywords created using other means (such as in plain bulksheets, the [!UICONTROL Campaigns] views, or in the ad network's ad editor) are never removed using the template.

**[!UICONTROL Apply these negatives]:** (All ad networks except [!DNL Yandex]; optional) Any static ad group-level negative keywords to add. To specify multiple keywords or multiple match types for the same keyword, enter them on separate lines. Use the following syntax, without a minus sign:

* Negative broad match: `keyword` (not supported by [!DNL Microsoft Advertising])
* Negative phrase match: `"keyword"`
* Negative exact match: `[keyword]`

The customary syntax for phrase and exact match types is used in the bulksheet that's generated when you propagate feed data through the template. **Note:** You can't see the negative keywords in the [!UICONTROL Keywords] tab or in the [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] view.
