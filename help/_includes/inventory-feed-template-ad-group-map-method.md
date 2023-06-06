# Text ad template - Ad Group Map Method

**[!UICONTROL Map Method]:** (When [!UICONTROL Map Only] is enabled for ad groups; all ad networks except [!DNL Yandex]) The method by which new keywords and ads are mapped to existing ad groups:

* *[!UICONTROL Contains Anywhere]:* Adds data to an existing ad group whose name includes the specified string, if it exists.

* *[!UICONTROL Contains Exactly]:* Adds data to an existing ad group whose name includes the specified string, if it exists.

* *[!UICONTROL Exactly Matches]* (the default): Adds data to an existing ad group with the same name, if it exists.

When no match is found, all data for the ad group is ignored. If the ad group data in the feed doesn't include campaign data, then the ad group is mapped to an ad group with the same name in any campaign, if one exists. If multiple ad group matches are found, then the keywords and ads are mapped to all of them.
