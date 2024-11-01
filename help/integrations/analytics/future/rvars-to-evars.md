---
title: XXX
description: Learn XXX
feature: Integration with Adobe Analytics
---
# XXXXX Paid Media rVar Migration for Analytics Data Connector

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

If you use reserved variables ([!DNL rVars]) to capture the [EF ID and AMO ID](ids.md) for your [!DNL Analytics for Advertising] integration, then you can prepare for a future integration between Adobe Advertising and [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview), which is Adobe’s next-generation [!DNL Analytics] solution, by copying your [!DNL rVars]<!-- , for which historical data isn't synced,--> into [!DNL eVars] as soon as possible. This will allow <!-- who --> to begin collecting historical data for your [!DNL rVars] as soon as you complete the task.

## Why .....

Customer Journey Analytics lets you sync data from Adobe Experience Platform into Adobe Analytics <!-- Leave out "Analytics? --> Analysis Workspace. Currently, [!DNL Analytics] <!-- or he [!DNL Analytics for Advertising] integration ? --> doesn't send historical data for [!DNL rVars] to Experience Platform, so historical data for [!DNL rVars] <!-- what exactly? --> isn't currently available within Customer Journey Analytics. Instead, XXXXXXXXXX <!-- what exactly? -->.

In 2025, your [!DNL Analytics for Advertising] integration will still require you to collect view-through data using [!DNL Analytics] tracking, but you'll be able to view your data in both [!DNL Analytics] (Analysis Workspace using data from [!DNL Analytics]) and Customer Journey Analytics (Analysis Workspace using data from Experience Platform). Once the feature is released, historical data for [!DNL rVars] will begin to collect for use in Customer Journey Analytics, but no data prior to the release date will exist. You can begin to collect data for your [!DNL rVars] sooner by creating a simple [[!DNL Analytics] processing rule](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules) <!-- Or a CJA processing rule? Or multiple rules? One rule per rVar, or one for all? -->to copy your [!DNL rVars] into [!DNL rVars] now. Once you create and implement<!-- implement? -->  the processing rule, you will begin to accrue historical data tracked by your [!DNL rVars].

## Copy your [!DNL rVars] into [!DNL rVars]












Sync Advertising data with CJA -- late 2024 to early 2025
-------------------------------------

Engineering's draft playbook:  https://wiki.corp.adobe.com/display/EfficientFrontier/Paid+Media+rVar+Migration+for+Analytics+Data+Connector+-+Playbook
Program Page:  https://wiki.corp.adobe.com/display/EfficientFrontier/CJA+Integration+Program+Page
Other Info: https://wiki.corp.adobe.com/pages/viewpage.action?pageId=3151723471

Release in late 2024 to early 2025, but clients can begin making rvar data available for it by creating an Analytics processing rule now to copy their rvars (for which historical data isn't synced) into evars.


The [!DNL Analytics for Advertising] integration uses two variables ([!DNL eVars] or [!DNL rVars] \[reserved [!DNL eVars]]\) to capture the [EF ID and AMO ID](ids.md).

FOR MARY TO DO once we remove from UI:

1. Create new topic.
2. Add info to A4A overview, and add cross-refs to other A4A topics.
3. Make sure that intro topic, and maybe https://experienceleague.adobe.com/en/docs/advertising, mention near the start that an A4A implementation is required for viewing advertising data in CJA as well as in Analytics.
4. Update "What's New" to include info.



