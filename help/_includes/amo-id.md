# Adobe Advertising AMO IDs

## Adobe Advertising AMO IDs {#amo-id}

The AMO ID tracks each unique ad combination at a less granular level and is used for [!DNL Analytics] and Customer Journey Analytics data classification and ingestion of advertising metrics (such as impressions, clicks, and cost) from Adobe Advertising.

For [!DNL Analytics], the AMO ID is stored in an [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) or rVar dimension (AMO ID).

For Customer Journey Analytics, the AMO ID is stored in the `trackingCode` property of the `conversionDetails` object, which is part of the [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension].

The AMO ID is also called the `s_kwcid`, which is sometimes pronounced as "[!DNL squid]."
