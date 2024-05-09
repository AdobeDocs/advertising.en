---
title: Placement-level Pre-Bid Filters and How to Use Them
description: Reference the available placement-level pre-bid filters and see how to use them.
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
---
# Placement-level Pre-Bid Filters and How to Use Them

| Pre-Bid Filter | Description | When to Use This Filter|
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Sets a minimum prediction threshold for the probability that an auction may result in a click-through. For example, if you set the threshold to 0.1%, then you bid on auctions only when the predicted probability of a click is greater than or equal to 0.1%.<br><br><b>Note:</b> Filters are applied before optimization goals. As a result, very strict filters can prevent spend. | Use when you have a minimum KPI goal for click-through rate (CTR) and don't want to spend your budget when the CTR is below the threshold. This filter can be quite restrictive, so it's important to set realistic goals. Depending on other restrictions on the placement, a goal of .03-.07% is generally a good starting point. You can optimize this at the site level as needed to help improve metrics.<br><br>If your goal is to achieve a minimum CTR and the best possible CPM, then the recommended setup is to combine a [!UICONTROL Click Through Rate] filter with the optimization goal "[!UICONTROL Lowest CPM]." If your goal is a maximum CPM with no real benefit for overachieving, and a minimum CTR, then pairing a [!UICONTROL Click Through Rate] filter with the optimization goal "[!UICONTROL Always Max Bid + Highest CTR]" may be more appropriate. |
| [!UICONTROL 100% Completion Rate] | Sets a required minimum completion rate that must be met before you bid on an impression. | Use this filter when the campaign's main goal is completion rates. Factor in other targeting parameters, but 65% is the recommended starting percentage. |
| [!UICONTROL Player Size - Adobe] | Sets a required minimum player size, using data from DSP. You'll bid on an impression when the [!UICONTROL Player Size] threshold is met. | Use to ensure you're delivering on full-episode player inventory using data from DSP. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Sets a required minimum player size, using data from [!DNL Moat] or [!DNL Integral Ad Science] ([!DNL IAS]). You'll bid on an impression when the [!UICONTROL Player Size] threshold is met. | Use to ensure you're delivering on full-episode player inventory using platform-wide [!DNL Moat] or [!DNL IAS] data.<br><br><b>Note:</b> Use this filter only when the campaign is configured to use [!DNL Moat] or [!DNL IAS] data. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Sets a required minimum viewability percentage, using DSP viewability numbers and measurements. You'll bid on an impression when the specified threshold is met.<br><br><b>Notes:</b><ul><li>If the campaign's [!UICONTROL Viewability Sensitivity] setting is "[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)],” then the [!DNL Media Rating Council] (MRC) viewability measurement standard is used for the campaign. If the [!UICONTROL Viewability Sensitivity] setting is “[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)],” then the [!DNL GroupM] viewability measurement standard is used for the campaign.</li><li>Adobe measurement definitions differ from third-party definitions, so there may be slight discrepancies with third-party data.</li></ul> | The best practice is to match the optimization goal and any pre-bid filter settings with the campaign's [!UICONTROL Viewability Sensitivity] setting. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [How DSP Optimizes Your Campaigns](optimization-how-dsp-optimizes-campaigns.md)
>* [Package Settings](/help/dsp/campaign-management/packages/package-settings.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Campaign Settings](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Optimization Goals and How to Use Them](optimization-goals.md)
