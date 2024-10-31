---
title: XXX
description: Learn XXX
feature: Integration with Adobe Analytics
---
# Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*
 


Paid Media rVar Migration for Analytics Data Connector - Playbook

To view your Adobe Advertising data in 
an A4A implementation is required for viewing advertising data in CJA as well as in Analytics


There is Analytics Data Connector available for exporting data from Adobe Analytics to AEP. This then would be easily available in CJA to use. This includes events/lists/props/eVars etc. However this doesn't include rVar as of today. Many integrations(including Adobe Advertising) uses rVar mechanism to capture data in Adobe Analytics.

Adobe Advertising uses rVar integration in ~40% of the reportsuites ( ~15% of Adobe Advertising Clients ) to store data for "AMO ID" and "AMO EF ID" critical for Ad Tracking and Optimization.

This playbook provides details about how can we leverage existing Adobe Analytics Integration with rVar to integrate for Adobe Advertising.




Sync Advertising data with CJA -- late 2024 to early 2025
-------------------------------------

Engineering's draft playbook:  https://wiki.corp.adobe.com/display/EfficientFrontier/Paid+Media+rVar+Migration+for+Analytics+Data+Connector+-+Playbook
Program Page:  https://wiki.corp.adobe.com/display/EfficientFrontier/CJA+Integration+Program+Page
Other Info: https://wiki.corp.adobe.com/pages/viewpage.action?pageId=3151723471

Release in late 2024 to early 2025, but clients can begin making rvar data available for it by creating an Analytics processing rule now to copy their rvars (for which historical data isn't synced) into evars.




FOR MARY TO DO once we remove from UI:

1. Create new topic.
2. Add info to A4A overview, and add cross-refs to other A4A topics.
3. Make sure that intro topic, and maybe https://experienceleague.adobe.com/en/docs/advertising, mention near the start that an A4A implementation is required for viewing advertising data in CJA as well as in Analytics.
4. Update "What's New" to include info.



