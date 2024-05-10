---
title: Campaign Settings
description: See descriptions of the available campaign settings.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
---
# Campaign Settings

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** The campaign name.

**[!UICONTROL Advertiser]:** (Read-only for existing campaigns) The applicable advertiser (brand). Select an existing advertiser or create a new one.

**[!UICONTROL Advertiser URL]:** The advertiser’s official page. This field speeds your ad approval process with inventory partners.

**[!UICONTROL Timezone]:** (Read-only for existing campaigns) The time zone for reporting and bidding.

**[!UICONTROL Customer PO]:** (Optional) A customer purchase order for the insertion order/purchase order.

**[Campaign Dates]:** The campaign start and end dates.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Whether to manage margins for the campaign: *[!UICONTROL Yes]* or *[!UICONTROL No]* (the default).

When you choose *[!UICONTROL Yes],* specify the margin type and amount:

* **[!UICONTROL Margin Type]:** The type of margin. You can't change the margin type once you enable margin management and save the campaign.

   * *[!UICONTROL Fixed]:* (the default) Allows DSP to auto-calculate and cap spend based on a fixed margin percentage of the [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Allows you to manage margins down to the placement level by specifying a separate [!UICONTROL Budget Reserve %] and [!UICONTROL Gross Budget] for each package and placement in the campaign. DSP optimizes based on the financial efficiency of each placement, without guaranteeing a specific margin. Use this for insertion orders that consist of multiple line items for which you've agreed to deliver a fixed amount of units or unit types at a fixed rate.

* **[!UICONTROL Fixed Margin %]:** (Campaigns with fixed margins only) The default markup for each insertion order <!-- impression? -->, as a percentage. This amount is deducted from the [!UICONTROL Gross Budget] to define the net campaign budget.

* **[!UICONTROL Budget Reserve %]:** (Campaigns with fixed margins only; optional) Reserves a specified percentage of the [!UICONTROL Gross Budget] as a safeguard. This amount is deducted from the [!UICONTROL Gross Budget] to define the net campaign budget.

**[!UICONTROL Gross Budget]:** (Campaigns with margin management only) The gross campaign budget, before the specified marginal adjustments are applied.

You can optionally add an additional daily, weekly, or monthly gross budget:

1. Click **[!UICONTROL Add an additional Gross Budget]**.

1. Enter the **[!UICONTROL Gross Budget]** and select the budget interval: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* or *[!UICONTROL Monthly]*.

 The total net budget, which is the spending cap for the campaign, is automatically calculated based on the margin settings and is indicated below this value.

**[!UICONTROL Budget]:** (Campaigns without margin management) The overall campaign budget.

**[!UICONTROL Estimated Tax Withholding]:** Withholds a percentage of total spend across ad fees, ad serving fees, and/or data fees at the account level for country or local taxes. Rates are estimates for budgeting and pacing purposes, so invoiced tax rates may vary.

To estimate taxes to withhold:

1. Click **[!UICONTROL Update rates here]**.

1. Specify the **[!UICONTROL Estimated tax rate]**, as a percentage.

1. Select the check box next to each fee type for which to withhold taxes. The fee types include:

   * *[!UICONTROL Include estimated tax - ads fee]:* Applies to all Advertising DSP media spend, including taxes on campaign management fees.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Applies to all spend on Advertising DSP except for media and data. It excludes taxes for campaign management fees

   * *[!UICONTROL Include estimated tax - data fee]:* Applies to all data spend on Advertising DSP.

1. Click **[!UICONTROL Submit]**.

>[!NOTE]
>
>* In the U.S., states may vary in their inclusion of tax fees across ads, ad serving, and data. For organizations in other countries, include all three categories of tax fees to account for VAT.
>
>* You can also configure these values in the account's fee settings.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (Read-only for existing campaigns created since 22 June 2020; not available for campaigns created before 22 June 2020) The level at which DSP will target ads and apply frequency caps: *Same Device* to target a device or *People* to target a person across all of their known devices.

**[!UICONTROL Device Graph]:** (Read-only for existing campaigns; campaigns with people-based cross-device targeting only) The device graph to use for cross-device targeting and frequency management:

* *[!UICONTROL LiveRamp - U.S. only]:* Available to all advertisers for cross-device targeting at $0.35 CPM for impressions that are delivered by using the [!DNL LiveRamp] device graph (that is, for devices not found within the targeted audience segments). You can set up cross-device targeting at the placement level.

    This option is also available to all advertisers, without any fees, for frequency management and attribution measurement.

**[!UICONTROL Frequency Cap]:** (Optional) The number of times a unique device or person (depending on the specified [!UICONTROL Cross Device Level]) may be served ads from the campaign. Options include *[!UICONTROL Unlimited]* or a specific amount per day, week, or month.

>[!NOTE]
>
> You can set frequency caps at the campaign, package, and placement levels. DSP respects the strictest frequency cap in the campaign hierarchy.

**[!UICONTROL Packages]:** The [packages](/help/dsp/campaign-management/packages/package-about.md) to include in the campaign. Select existing packages and/or create packages to include. If you create packages, see descriptions about the [package settings](/help/dsp/campaign-management/packages/package-settings.md) for more information.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>The following settings enable only measurement and reporting capabilities. Performance optimization is executed only at the package and placement level.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Optional) Enables [!DNL IAS] measurement and reporting of viewability, fraud, brand safety, and audience verification, using the specified settings. Additional fees apply.

* **[!UICONTROL Measure On]:** The inventory on which to measure: *[!UICONTROL Display and VPAID video inventory]* (the default) or *[!UICONTROL Display, VPAID & VAST video inventory]*.

   >[!NOTE]
   >
   >Video viewability is measurable on VPAID inventory only.

* **[!UICONTROL IAS Account ID (AnID)]:** (Advertisers with their own [!DNL IAS] accounts; optional) The organization's [!DNL IAS] account ID, which [!DNL IAS] will bill directly for usage.

* **[!UICONTROL IAS Team ID]:** (Advertisers with their own [!DNL IAS] accounts; optional) The team ID for the organization's [!DNL IAS] account, which [!DNL IAS] will bill directly for usage. <!-- verify -->

**[!UICONTROL MOAT]:** (Optional) Enables [!DNL MOAT] measurement and reporting of viewability, fraud, brand safety, and audience verification. Additional fees apply.

#### Audience Verification

**[!UICONTROL Nielsen]:** (Optional) Enables [!DNL Nielsen] measurement and reporting of audience verification, using the specified settings. Additional fees apply.

* **[!UICONTROL Target Gender]:** The gender to target: *[!UICONTROL Both]* (the default), *[!UICONTROL Male]*, or *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** The age range to target. Use the left and right sliders to reduce the range as needed.

* **[!UICONTROL Target Country]:** (Optional) A country to target. [!DNL Nielsen] measures impressions served in supported countries only.

**[!UICONTROL comScore vCE]:** (Optional) Enables [!DNL Comscore validated Campaign Essentials (vCE)] measurement and reporting of audience verification, using the specified settings. Additional fees apply.

* **[!UICONTROL Target Gender]:** The gender to target: *[!UICONTROL Both]* (the default), *[!UICONTROL Male]*, or *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** The age range to target. Use the left and right sliders to reduce the range as needed.

* **[!UICONTROL Target Country]:** (Optional) A country to target. [!DNL Comscore] measures impressions served in supported countries only.

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Enables first-party measurement and reporting of viewability using the [!DNL IAB Open Video Viewability (OpenVV)] technology, based on the specified sensitivity level:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [About Campaign Management](campaign-about.md)
>* [Create a Campaign](campaign-create.md)
>* [Edit a Campaign](campaign-edit.md)
>* [View the Change Log for a Campaign](campaign-change-log.md)
