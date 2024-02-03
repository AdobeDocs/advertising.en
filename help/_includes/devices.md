# Devices field in GGL and MS campaign and ad group settings

**[!UICONTROL Devices]:** (Optional; not available for [!DNL Google Ads] performance max campaigns or [!DNL Microsoft Advertising] video or CTV video ads) Configure bid adjustments for different device types, as percentages of the keyword-level bid. For example, if the keyword-level bid is 1 USD and the bid adjustment for smartphones is 50%, then the smartphone bid is 1.50 USD. By default, no values are entered (bid adjustment=0), and all devices are bid at the keyword-level bid.

For [!DNL Google Ads], valid percentages can include -100 for smartphones and tablets (to not bid for the device type), and from -90 to 900 for all device types.

For [!DNL Microsoft Advertising], valid percentages can include:

* Smartphones and tablets: -100 (to not bid for the device type) and from -90 to 900
* Desktop: from 0 to 900

>[!NOTE]
>* The ad group-level settings override the campaign-level settings. However, if you exclude a device at the campaign level, then you can't override the exclusion at the ad group level.
>* If you assign this campaign to a standard optimized portfolio, then Search, Social, & Commerce automatically determines the base keyword-level bid to help the portfolio meet its objective. The ad network then adjusts the bid as specified for different device types.
>* (For all campaigns/ad groups except for [!DNL Microsoft Advertising] ad groups in the audience network) If you assign this campaign to a standard optimized portfolio that's configured to "[!UICONTROL Auto-optimize Bid Adjustment Values]," then the optimization capability changes the specified device bid adjustments at the ad group level, as long as the ideal value that it calculates falls within the minimum and maximum values specified in the portfolio settings and the ad group doesn't exclude bidding for the device type.
