# Adobe Advertising EF IDs

The EF ID is a unique token that Adobe Advertising uses to associate activity with an online click or ad exposure at the individual browser or device level. EF IDs act primarily as keys for sending [!DNL Analytics] data and Customer Journey Analytics data to Adobe Advertising for reporting and bid optimization within Adobe Advertising.

For [!DNL Analytics], the EF ID is stored in [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) or [!DNL rVar] (reserved [!DNL eVar]) dimension (Adobe Advertising EF ID).

For Customer Journey Analytics, the EF ID is stored in the `trackingIdentities` property of the `conversionDetails` object, which is part of the [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension].
