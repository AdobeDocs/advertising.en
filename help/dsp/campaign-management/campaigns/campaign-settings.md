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

**[!UICONTROL Advertiser URL]:** The advertiser's official page. This field speeds your ad approval process with inventory partners.

**[!UICONTROL Timezone]:** (Read-only for existing campaigns) The time zone for reporting and bidding.

**[!UICONTROL Customer PO]:** (Optional) A customer purchase order for the insertion order/purchase order.

**[Campaign Dates]:** The campaign start and end dates.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** (Self-service accounts that are serviced by agencies using margins) Options for margin management:
 
* **[!UICONTROL Would you like to manage margins for this campaign?]:** Whether to manage margins for the campaign: *[!UICONTROL Yes]* or *[!UICONTROL No]* (the default). When you choose *[!UICONTROL Yes],* specify the additional settings. Once you enable margin management and save the campaign, you can't disable margin management.

* **[!UICONTROL How would you like to compute agency fees?]:** (Campaigns with margin management only) How to compute agency fees:

   * *[!UICONTROL Margin % of Total Budget]:* (the default) Computes fees as a percentage of the [!UICONTROL Gross Budget]. Specify the [!UICONTROL Agency Fee Type] (fixed or composite) and the [!UICONTROL Margin %] or [!UICONTROL Composite Margin %].

   * *[!UICONTROL Apply Markup % on top of individual cost components]:* Adds a specified percentage to your media cost, data and other costs, and/or [!DNL Adobe] tech fees. Specify the [!UICONTROL Markup %] and select the components on which to apply the markup.

* **[!UICONTROL Agency Fee Type]:** (Campaigns that use [!UICONTROL Margin % of Total Budget]) The type of agency fee.

   * *[!UICONTROL Fixed]:* (the default) Allows DSP to auto-calculate and cap spend based on a fixed percentage of the [!UICONTROL Gross Budget]. Specify the [!UICONTROL Margin %].

   * *[!UICONTROL Composite]:* Allows DSP to auto-calculate and cap spend based on a percentage of the [!UICONTROL Gross Budget], using the composite percentage of agency fees and [!DNL Adobe] tech fees. Specify the [!UICONTROL Composite Margin %].

* **[!UICONTROL Margin %]:** (Campaigns that use [!UICONTROL Margin % of Total Budget] with fixed margins) The default markup for each insertion order <!-- impression? -->, as a percentage. This amount is deducted from the [!UICONTROL Gross Budget] to define the net campaign budget. The margin isn't applied to the [!UICONTROL Estimated Tax Withholding] on the [!UICONTROL Gross Budget].

* **[!UICONTROL Composite Margin %]:** (Campaigns that use [!UICONTROL Margin % of Total Budget] with composite margins) The sum of agency fees and [!DNL Adobe] tech fees, as a percentage. This amount is deducted from the [!UICONTROL Gross Budget] to define the net campaign budget. The margin isn't applied to the [!UICONTROL Estimated Tax Withholding] on the [!UICONTROL Gross Budget].

* **[!UICONTROL Markup %]:** (Campaigns that use [!UICONTROL Apply Markup % on top of individual cost components]) The percentage to add to specified cost components.

* **[!UICONTROL Select cost components on which markup will be applied]:** (Campaigns that use [!UICONTROL Apply Markup % on top of individual cost components]) The cost components for which the [!UICONTROL Markup %] is applied. Select all applicable components: *[!UICONTROL Media cost]*, *[!UICONTROL Data and Other costs]*, and/or *[!UICONTROL Adobe tech fees]*.

**[!UICONTROL Gross Budget]:** (Campaigns with margin management only) The gross campaign budget, before the specified marginal adjustments are applied.

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

**[!UICONTROL Cross Device Level]:** (Read-only for existing campaigns created since 22 June 2020; not available for campaigns created before 22 June 2020) The level at which DSP targets ads and applies frequency caps: *Same Device* to target a device or *People* to target a person across all of their known devices. **Note:** Cross-device support isn't available for placements that target universal IDs.

**[!UICONTROL Device Graph]:** (Read-only for existing campaigns; campaigns with people-based cross-device targeting only) The device graph to use for cross-device targeting and frequency management:

* *[!UICONTROL LiveRamp - U.S. only]:* Available to all advertisers for cross-device targeting at $0.35 CPM for impressions that are delivered by using the [!DNL LiveRamp] device graph (that is, for devices not found within the targeted audience segments). You can set up cross-device targeting at the placement level.

    This option is also available to all advertisers, without any fees, for frequency management and attribution measurement.

    Cross-device support applies only for placements that target legacy IDs but not for placements that target universal IDs (including [!DNL LiveRamps]). Targeting, frequency management, and attribution for universal IDs is applied at the ID level only.

**[!UICONTROL Frequency Cap]:** (Optional) The number of times a unique device, universal ID, or person (depending on the specified [!UICONTROL Cross Device Level] and the placement's [!UICONTROL Targeting] setting) can be served ads from the campaign. Options include *[!UICONTROL Unlimited]* or a specific amount per day, week, or month.

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

#### Audience Verification

**[!UICONTROL Comscore Campaign Ratings]:** (Optional) Enables [!DNL Comscore] validated [!DNL Campaign Ratings] measurement and reporting of audience verification, using the specified settings. Additional fees apply.

* **[!UICONTROL Target Gender]:** The gender to target: *[!UICONTROL Both]* (the default), *[!UICONTROL Male]*, or *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** The age range to target. Use the left and right sliders to reduce the range as needed.

* **[!UICONTROL Target Country]:** (Optional) A country to target. [!DNL Comscore] measures impressions served in supported countries only.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Enables tracking for the placement-level [!UICONTROL Attention Score] metric (the weighted average number of [!DNL Adelaide] "[!DNL Attention Units]" across impressions). Metrics are available for all placement types except for [!DNL Roku] connected TV, VPAID-only pre-roll, and audio that's not a podcast. DSP automatically attaches a JavaScript tag to all associated creatives, and [!DNL Adelaide] tracks the exposure data and sends it to DSP daily. You can use the date to manually optimize your spending towards placement tactics with better attention scores.

The [!UICONTROL Attention Score] field is available in the [!UICONTROL Metrics] section of reports; within the [!UICONTROL Campaigns], [!UICONTROL Packages], and [!UICONTROL Placements] views; and on the [!UICONTROL Sites], [!UICONTROL Ads], and [!UICONTROL Inventory] tabs of the [placement details view](/help/dsp/campaign-management/reports/placement-details-view.md).

Using [!DNL Adelaide] segments for measurement incurs a CPM fee for each impression delivered from ads with [!DNL Adelaide] measurement tags. This fee is separate from fees for [placement-level attention targeting](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

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
