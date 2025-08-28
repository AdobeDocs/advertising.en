---
title: Prerequisites for integrating Adobe Advertising with Customer Journey Analytics
description: Prerequisites for integrating Adobe Advertising with Customer Journey Analytics
feature: Integration with Adobe Customer Journey Analytics
exl-id: 4bd14178-5003-4da6-9034-d070c57f0e9b
---
# Prerequisites for integrating Adobe Advertising with Customer Journey Analytics

*Advertisers with Advertising DSP and [!DNL Advertising Search, Social, & Commerce]*

* Advertisers with both [!DNL Analytics for Advertising] and Customer Journey Analytics:

  * Adobe Customer Journey Analytics<!-- any specific version? -->

  * [All other prerequisites for [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md). 

* Advertisers with Customer Journey Analytics but not [!DNL Analytics for Advertising]:

  * Adobe Experience Platform Web SDK library: `alloy.js`
    
    The [!DNL Org ID] used for Web SDK and for the Adobe Advertising advertiser account must be the same. You can find this ID on the [Summary tab of the Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).
    
    ![Experience Cloud Debugger Summary screen](/help/integrations/assets/a4adc-debugger-summary.png)
    
    You'll need support from your Experience Platform site administrator to create an Experience Platform datastream and XDM schema.

  * Adobe Customer Journey Analytics<!-- any specific version? -->

    You'll need support from your internal web analyst to set up a connection to your dataset and configure reporting.

>[!TIP]
>
>To improve data fidelity, use the most recent version of each library.

>[!MORELIKETHIS]
>
>* [Overview](overview.md)
>* (Adobe Analytics users) [Collect Historical Data for AMO IDs and EF IDs for Use in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
