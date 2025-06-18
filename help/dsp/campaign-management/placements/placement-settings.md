---
title: Placement Settings
description: See descriptions of the available placement settings.
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
---
# Placement Settings 

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** The placement name.

>[!TIP]
>Use a naming convention that makes sense for your situation. One suggested naming convention is "*\<Campaign Name\>: \<Ad Unit\>: \<Duration\>: \<Targeting\>*."

**[!UICONTROL Status]:** The placement status: *[!UICONTROL Active]* (the default) or *[!UICONTROL Paused]*.

>[!TIP]
>The best practice is to pause the placement until you're ready to launch it.

**[!UICONTROL Details]:** (Read-only) The applicable ad type, the account that is creating or created the placement, and the parent campaign. To see more details, click **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Opens a list of existing placement templates. To auto-populate targeting settings from a template:

1. Do either of the following:

   * To reuse all target from a template, select the check box next to the template name.

   * To reuse individual target types from a template, expand the template name and select the check box next to the target types you want to reuse.

1. Click **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Video ad formats only) The ad duration and/or ad specifications, which are used to calculate the Forecast projection on the right. The fields vary by ad type.

**[!UICONTROL Environment]:** (Universal Video ad format only) The device environments (Desktop, Mobile, Connected TV) to include as targets in the placement. Specify at least one.

In custom reports, the placement-level dimension “Device Environment” indicates the targeted environment.

**[!UICONTROL Placement tags]:** (Optional) Keywords or nicknames to help you locate this placement.

## Goals

**[!UICONTROL Package]:** (Optional) A package to which the placement is assigned. Click ![Edit](/help/dsp/assets/edit.png) to select an existing package or create a package. When you assign the placement to a package, the [!UICONTROL Goals] section is updated with the flight dates, delivery goal, and budget from the package.

**[!UICONTROL Flight Dates]:** The start date and end date for the placement. Approved ads are eligible to run during the flight when the placement is active and assigned to an active package or campaign.

The dates for the package (when applicable) or campaign are auto-populated by default.

>[!NOTE]
>
>* The flight dates must be included within the campaign flight dates and the package flight dates.

### Placements Assigned to Packages with Package-level Pacing

**[!UICONTROL Placement Funding]:** How to budget for the placement:

* *[!UICONTROL Optimize based on performance]:* Controls the budget at the package level.
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* Allows you to set a minimum and/or a maximum placement budget. Specify at least one type of budget:

  * *[!UICONTROL Maximum Budget]*: Enter a value and the duration (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

  * *[!UICONTROL Minimum Budget]*: The minimum budget as a percentage of the package budget. When an interval cap is specified, the minimum budget value is always calculated as a percentage of the interval cap. Otherwise, it's calculated as a percentage of the package budget.

**[!UICONTROL Max Bid]:** The maximum to pay for 1000 impressions.

**[!UICONTROL Placement Pre-bid Filters]:** Up to five KPI thresholds (such as a minimum viewability metric or click-through rate) that must be met for bidding to occur. You can use pre-bid filters as optimization tactics, but understand that each rule may limit the opportunities on which this placement can bid. To add or edit filters:

1. Click ![Edit](/help/dsp/assets/edit.png).
1. Do either of the following:
   * To add a filter:
      1. Click **[!UICONTROL Add Filter]**.
      1. Next to **[!UICONTROL Only bid if]**, select a metric, and then enter a value.
   * To remove a filter, click **[!UICONTROL X]** in the filter row.
1. Click **[!UICONTROL Save]**.

 See descriptions of each pre-bid filter at "[Placement-level Pre-Bid Filters and How to Use Them](/help/dsp/optimization/optimization-pre-bid-filters.md)."

### All Other Placements

**[!UICONTROL Budget Goal]:** The gross budget cap and the budget interval (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Placements in campaigns with margin management only) The gross budget cap and the budget interval (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:**  The optimization goal for the package. See descriptions of each optimization goal at "[Optimization Goals and How to Use Them](/help/dsp/optimization/optimization-goals.md)".

**[!UICONTROL Target Goal]:** The target goal, which is used to track performance.

>[!NOTE]
>
>This field is only a benchmark and isn't used for decisioning.

**[!UICONTROL Pace on]:** The basis for pacing:

* **[!UICONTROL Budget goal]:** (Default) This option delivers as many impressions as possible within the allocated budget.

* **[!UICONTROL Impressions]:** This option delivers impressions until a specified quantity is reached within a specified interval. When you select this option, specify the number of impressions and the interval: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* or *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** The maximum to pay for 1000 impressions.

**[!UICONTROL Flight pacing]:** (Placements with placement-level pacing only) How to pace ad delivery:

* *[!UICONTROL Even]:* (The default) Paces delivery uniformly throughout each flight, with a target of 50% of the delivery in the first half of the flight.

* *[!UICONTROL Slightly Ahead]:* (The default) Accelerates delivery so that it's 55-65% complete halfway through the flight duration.

* *[!UICONTROL Frontload]:* Accelerates delivery so that it is 65-75% complete halfway through the flight.

* *[!UICONTROL Aggressive Frontload]:* Accelerates delivery so that it is 75-85% complete halfway through the flight.

**[!UICONTROL Intraday pacing]:** (Placements with placement-level pacing only) How to pace ad delivery across each day within the flight:

* *[!UICONTROL Even]:* (The default) Scales delivery based on inventory availability. Generally, more ads are delivered per hour in the daytime, when auction volume is higher, and fewer ads are delivered in the mornings and evenings.

* *[!UICONTROL ASAP]:* (The default) Accelerates delivery to twice the speed of *Even*.

   >[!CAUTION]
   >
   >This option can negatively affect performance. Use it only when you are fully prioritizing delivery and spend over performance optimization.

**[!UICONTROL Placement Pre-bid Filters]:** (Optional) Up to five filters that must be met for bidding to occur. You can use pre-bid filters as optimization tactics, but keep in mind that each rule may limit the opportunities on which this placement can bid. To add or edit filters:

1. Click ![Edit](/help/dsp/assets/edit.png).
1. Do either of the following:
   * To add a filter:
      1. Click **[!UICONTROL Add Filter]**.
      1. Next to **[!UICONTROL Only bid if]**, select a metric, and then enter a value.
   * To remove a filter, click **[!UICONTROL X]** in the filter row.
1. Click **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Optional) Specific locations in which to include or exclude ads in the placement. If you don't specify any locations, all locations are targeted.

>[!NOTE]
>
>City and DMA locations aren't available for Roku placements.

To specify locations:

1. Click ![Edit](/help/dsp/assets/edit.png).
1. Do any of the following:
   * To include or exclude a Country, State, City, DMA, Federal Legislative District, or State Legislative District:
      1. Select the location type in the left column.
      1. (As needed) Click a location to expand it.
      1. Next to the location, click *[!UICONTROL Include]* to include it as a target or *[!UICONTROL Exclude]* to exclude it as a target.
   * To search for a postal code and include or exclude all selected results:
      1. Click **[!UICONTROL Search Postal Code]**.
      1. Select the country.
      1. Enter the city name, and then click ![Edit](/help/dsp/assets/search.png).
      1. Click the correct search result.
      1. Click *[!UICONTROL Include All]* to include all locations as targets or *[!UICONTROL Exclude All]* to exclude all locations as targets.
   * To enter or paste postal codes, and include or exclude them all:
      1. Click **[!UICONTROL Paste Postal Code]**.
      1. Select the country.
      1. Enter or paste up to 1000 postal codes.
         Include one postal code per line, or enter multiple values separated by commas or tabs.
      1. Click *[!UICONTROL Include All]* to include all locations as targets or *[!UICONTROL Exclude All]* to exclude all locations as targets.
   * To remove a location from the [!UICONTROL Included] or [!UICONTROL Excluded] list, click **[!UICONTROL X]** next to the location in the right column.
1. Click **[!UICONTROL Done]**.

>[!NOTE]
>
>* Not all countries have State, City, or Postal Code locations.
>* DMA (designated market area), Federal Legislative Districts, and State Legislative Districts are available for U.S. locations only.

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Inventory sources to include or exclude as targets. For most placement types, all inventory types, and all sources for each type, are included by default. For [!DNL Roku] placements, you must specify the inventory type and sources. You can choose from the following types of inventory:

* [!UICONTROL Public]: (All placement types except for Roku) All open exchange inventory to which DSP has access. You can include and exclude public inventory.

    You can view the list by source or by feed. When you view the list by feed, you can search by feed name, feed key, or a selected characteristic tag.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: Your existing private deals (or existing private [!DNL Roku] deals for [!DNL Roku] placements) with publishers that you've set up in DSP, and your existing [private deal lists](/help/dsp/inventory/lists-deals-manage.md). You can include, but not exclude, public inventory.

    From the [!UICONTROL Deals] tab, you can search the list by keyword, key, deal ID, or custom tag. From the [!UICONTROL Deal Lists] tab, you can search the list by deal list name or deal list ID.

    * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Optional) Overrides the bid price algorithm to bid at least the fixed and floor prices for deals.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: All [premium, non-guaranteed [!UICONTROL On Demand] inventory](/help/dsp/inventory/on-demand-inventory-about.md) (or [!UICONTROL On Demand] [!DNL Roku] deals for [!DNL Roku] placements) to which you've subscribed in [!DNL DSP]. You can include and exclude [!UICONTROL On Demand] inventory.

    You can view the list by source or by feed. When you view the list by feed, you can search by feed name, feed key, or a selected publisher region, category tag, or characteristic tag.

    * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Optional) Overrides the bid price algorithm to bid at least the fixed and floor prices for deals.

To specify inventory targeting:

* To exclude an inventory type, clear the check box next to the name.
* To target an inventory type:
   1. Select the check box next to the inventory type name.
   1. (Optional) Change the sources to include:
      1. Click ![Edit](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] and [!UICONTROL On Demand] inventory) Click **[!UICONTROL View by Source]** or **[!UICONTROL View by Feed]** to change how the sources are listed.
      1. (When applicable) Filter the inventory as needed.
      1. Specify the sources to include and exclude:
         * For [!UICONTROL Public] or [!UICONTROL On Demand] inventory:
           * To include a source, click **[!UICONTROL Include]** next to the source name.
           * To exclude a source, click **[!UICONTROL Exclude]** next to the source name.
         * For [!UICONTROL Private] inventory:
           * On the [!UICONTROL Deals] tab:
             * To include all inventory in a deal, click **[!UICONTROL Include all]** next to the deal name.
             * To include an individual inventory source, expand the deal name, and then click the check box next to the source name.
           * On the [!UICONTROL Deal Lists] tab, click the check box next to the deal list name.
   1. (Optional) To download a CSV file with the targeting information to your browser's Downloads location, click **[!UICONTROL Save & Export]**.
   1. Click **[!UICONTROL Save]**.

>[!TIP]
>
>If you subscribed to [!UICONTROL On Demand] inventory but can't locate the publishers or deals to target, then check the status of the deals. For more information about statuses, see [About [!DNL On Demand] Premium Inventory](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Video targeting]:**  Target (but not exclude) inventory by inventory attributes. When you target multiple values for the same video attribute, any of the selected attributes can be targeted (for example either \[Player size = large OR Player size = HD\]). When you target multiple attributes, each of the specified attributes must be present (for example, \[Duration = 30-60 min] AND \[Player size = large OR Player size = HD\]).

* **[!UICONTROL Player size]:** Target (but not exclude) inventory by player size. The setting applies to preroll placements, mobile standard preroll placements, and universal video placements for desktop and mobile environments. By default, all sizes are targeted. To narrow down the targets, select specific target sizes and/or *Unknown*.

* **[!UICONTROL Playback mode]:** Target (but not exclude) inventory by how playback is initiated. The setting applies to preroll placements, mobile standard preroll placements, and universal video placements for desktop and mobile environments. By default, all modes are targeted. To narrow down the targets, select specific target modes and/or *Unknown*.

* **[!UICONTROL Skippability]:** Target (but not exclude) inventory according to whether or not it’s skippable. The setting applies to all VAST/VPAID placements, including preroll, mobile standard preroll, connected TV, and universal video placements. By default, all options are targeted. To narrow down the targets, select specific targets and/or *Unknown*.

**[!UICONTROL Position targeting]:** Target (but not exclude) inventory by ad position. The setting applies to all VAST/VPAID placements, including preroll, mobile standard preroll, connected TV, and universal video placements. By default, all positions are targeted. To narrow down the targets, select specific target positions and/or *Unknown*.

## [!UICONTROL Site and App Targeting]

**[!UICONTROL Traffic type]:** The types of traffic to target. Options include **[!UICONTROL Websites]** and **[!UICONTROL Apps]**.

**[!UICONTROL Tier]:** (Available when **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*) The quality of the traffic to target. Tiers 1-3 are all brand safe and have been approved by the DSP mapping team.

* *[!UICONTROL Tier 1]:* Premium sites and applications that are nationally recognizable.

* *[!UICONTROL Tier 2]:* Targets Tier 1 as well as quality sites and applications that are less widely known than Tier 1.

* *[!UICONTROL Tier 3]:* Targets Tiers 1-2 plus legitimate and brand-safe sites and applications that cater to a niche audience. Use Tier 3 for reach or data targeting buys.

* *[!UICONTROL All Sites or Apps]:* Targets Tiers 1-3 and new inventory that has not been screened or categorized, which you can use for reach.

>[!NOTE]
>
>Inventory is specific to the ad units in the placement.

>[!TIP]
>
>For performance campaigns, the best practice is to select *[!UICONTROL All Sites]*.

**[!UICONTROL Site or App Categories]:** (Optional; available when **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*) Site categories within the selected site tiers to either include or exclude (but not both) as targets. Choose from vertical site lists that DSP has mapped based on subject:

1. Click ![Edit](/help/dsp/assets/edit.png).
1. Specify the site categories to either include or exclude:
   * To include site categories:
      1. Click **[!UICONTROL Include categories]**.
      1. Select the check box next to each category to target.
   * To exclude site categories:
      1. Click **[!UICONTROL Exclude categories]**.
      1. Select the check box next to each category to exclude.
1. (Optional) To download a CSV file with the targeting information to your browser's Downloads location, click **[!UICONTROL Export]**.
1. Click **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites or Apps]:** (Optional; available when **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*) Sites to exclude. You can either search for and select sites, or enter or paste domain names:

1. Click ![Edit](/help/dsp/assets/edit.png).
1. Specify the sites:
   * To search for a site:
      1. Click **[!UICONTROL Search]**.
      1. Enter a keyword, select a site tier, and/or select a site category.
      1. In the search results, select the sites to exclude:
         * To exclude an individual site, select the adjacent check box.
         * (When more than 50 results are available) To exclude the first 50 results, click **[!UICONTROL Exclude these 50]**. To exclude all search results, click **[!UICONTROL Exclude these \<*NN*\>]**.
   * To enter domain names:
      1. Click **[!UICONTROL Paste]**.
      1. Enter one or more domain names on separate lines.
      1. Click **[!UICONTROL Exclude All]**.
1. Click **[!UICONTROL Done]** when you're finished.

>[!NOTE]
>
>* Account-level and advertiser-level blocked site lists are also applied, in addition to the DSP [globally blocked site list](/help/dsp/introduction/features/brand-safety-media-quality.md), which includes sites deemed unsafe for ads.
>* Blocked site lists always override targeted site lists. If a placement both excludes and includes the same target for an ad, then the target is excluded.

**[!UICONTROL Language]:** (Optional) A single language to target.

**[!UICONTROL Site or App List Preview]:** (Read-only) All targeted and blocked sites for the placement.

You can optionally export the list of targeted and blocked sites as a comma-separated values (CSV) file. To export the list, click **[!UICONTROL Export full site list]**, and then open or save the file according to your browser's normal procedure.

**[!UICONTROL Allow unscreened sites]:** (Standard display placements only) Enables ad delivery on non-audited sites. When the placement targets private inventory, this option may deliver ads on blocked sites.

**[!UICONTROL Paste list of targeted sites]:** Allows you to target specific sites only. When you enable this option, the other site targeting options are disabled.

**[!UICONTROL Sites]:** (Available when **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL On]*) Sites to target. You can either search for and select sites, or enter or paste domain names:

1. Click ![Edit](/help/dsp/assets/edit.png).
1. Specify the sites:
   * To search for a site:
      1. Click **[!UICONTROL Search]**.
      1. Enter a keyword, select a site tier, and/or select a site category.
      1. In the search results, select the sites to include:
         * To exclude an individual site, select the adjacent check box.
         * (When more than 50 results are available) To include the first 50 results, click **[!UICONTROL Include these 50]**. To include all search results, click **[!UICONTROL Include these \<*NN*\>]**.
   * To enter domain names:
      1. click **[!UICONTROL Paste]**.
      1. Enter one or more domain names on separate lines.
      1. Click **[!UICONTROL Include All]**.
1. Click **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Any audience targets for the placement, including [third-party segments, first-party segments, Adobe segments, custom segments, and saved audiences](/help/dsp/audiences/audience-settings.md). The total and active deduplicated audience size across all selected segments and saved audiences is also displayed. You can select an existing audience, create an audience that you can reuse later, or select specific audience segments:

* To select an existing audience, click ![Select](/help/dsp/assets/chevron-down.png) next to [!UICONTROL Included Audiences], and then select the audience.
* To create an audience, click ![Select](/help/dsp/assets/chevron-down.png) next to [!UICONTROL Included Audiences], and then select **[!UICONTROL + Create Audience]**. For instructions, see [Create a Reusable Audience](/help/dsp/audiences/reusable-audience-create.md), beginning with Step 3.
* To select specific audience segments, click **[!UICONTROL Select segments for this placement only]**. Select the segment logic; for instructions, see Step 6 in "[Create a Reusable Audience](/help/dsp/audiences/reusable-audience-create.md)." When you're done, click **Save**.

**[!UICONTROL Excluded Audiences]:** Any audiences to exclude for the placement, including audiences with [third-party segments, first-party segments, Adobe segments, custom segments, and saved audiences](/help/dsp/audiences/audience-settings.md). The total and active deduplicated audience size across all excluded audiences is also displayed. You can select an existing audience or create a new audience that you can reuse later:

* To select an existing audience, click ![Select](/help/dsp/assets/chevron-down.png) next to [!UICONTROL Excluded Audiences], and then select the audience.

* To create an audience, click ![Select](/help/dsp/assets/chevron-down.png) next to [!UICONTROL Excluded Audiences], and then select **+ Create Audience**. For instructions, see [Create a Reusable Audience](/help/dsp/audiences/reusable-audience-create.md), beginning with Step 3.

**[!UICONTROL Targeting]:** The types of user IDs to target. You can't change this setting after the placement is live (that is, after the flight has begun).

When you select both legacy IDs and universal IDs, bidding preference is given to universal IDs.

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*: (The default) Targets users based on their cookies, mobile advertising IDs, or connected TV (CTV) IDs. IDs are selected based on the browser, in-app, or CTV inventory. 

* *[!UICONTROL Universal ID Beta]*: Targets user privacy-focused IDs; select one ID type. The available options are determined by the selected geographical targets in the [!UICONTROL Geo-Targeting] section. Use with [[!DNL RampID] segments imported directly to DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md), [segments for which DSP converts your PII to universal IDs](/help/dsp/audiences/sources/source-about.md), or [custom segments that tracks universal IDs](/help/dsp/audiences/custom-segment-create.md).

  * *[!UICONTROL ID5]*: Targets [!DNL ID5] IDs created probabilistically from email addresses and other signals.<!-- What countries/geos are these available for? Everywhere?--> ID5 IDs are available for no fee. **Note:** Third-party segments from [!DNL Eyeota] may include ID5 IDs.

  * *[!UICONTROL RampID]*: Targets [!DNL LiveRamp] [!DNL RampIDs] of users logged into your site using their email addresses.<!-- Verify --> [!DNL RampIDs] are available for users in North America, Australia, and New Zealand.
  
  * *[!UICONTROL Unified ID2.0]*: Targets [!DNL Unified ID2.0] (UID2) IDs of users logged into your site using their email addresses.<!-- Verify -->[!DNL UID2 IDs] aren't available for users in the European Economic Area and some additional countries. See the [list of prohibited countries](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  **[!UICONTROL Terms of service]**: The terms of service agreement for using universal IDs. You or another user in the DSP account must accept the terms once before you can convert data to a new ID type. For customers with managed service contracts, your Adobe Account Team will get your consent and accept the terms on your organization's behalf. To read the terms, click **>**. To accept the terms, scroll to the bottom of the terms and click **[!UICONTROL Accept]**.
  
**[!UICONTROL Cross Device Targeting]:** (Available when the [campaign is configured for people-based cross-device targeting](/help/dsp/campaign-management/campaigns/campaign-settings.md), you target legacy IDs only (not universal IDs), and you select at least one segment or audience. Allows you to extend your targeting across all of a person's known devices (per the device graph specified in the campaign settings), even devices that aren't in the specified segments. Fees may apply depending on the graph specified for the campaign. Device graph data is available only in North America.

**[!UICONTROL Placement Cap]:** (Optional) The number of times a unique device, universal ID, or person (depending on the specified [!UICONTROL Cross Device Level] for the campaign and the placement's [!UICONTROL Targeting] setting) can be served ads from the placement. Options include *[!UICONTROL Unlimited]* or a specific amount per day, week, or month.

>[!NOTE]
>
> You can set frequency caps at the campaign, package, and placement levels. DSP respects the strictest frequency cap in the campaign hierarchy.

**[!UICONTROL Secondary Cap]:** (Optional; available when you include a numeric [!UICONTROL Placement Cap]) An additional limitation within the bounds of the primary placement cap. Select the number of impressions and the time period (such as 3 per 12 hours).

**[!UICONTROL Day Parting]:** (Optional) Specific days of the week and time of day in which ads may run. To specify dayparting intervals:

1. Click ![Edit](/help/dsp/assets/edit.png).
1. Select the applicable time zone.
1. Specify the intervals:
   * To select a preset interval, click one of the interval buttons. Options include *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]*, or *[!UICONTROL Prime]* (primetime).
   * To manually select an interval, click inside a cell and optionally drag to select the interval.
1. Click **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Optional; available to advertisers configured with [!DNL Proximic by Comscore] segments) Specific segment names or IDs from [!DNL Proximic by Comscore] to include as targets. Additional fees may apply for this feature. To activate this feature and set up topic segments, contact your Adobe Account Team.

To specify topic targeting:

1. Click ![Edit](/help/dsp/assets/edit.png).
1. Specify the segments to target:
   1. In the left column, select the partner: (*[!UICONTROL Comscore]*.
   1. In the input field, enter the segment names or segment IDs.
1. (Optional) To download a CSV file with the topic information to your browser's Downloads location, click **[!UICONTROL Export]**.
1. Click **[!UICONTROL Save]**.

>[!TIP]
>
>* Topic targeting limits the inventory on which the placement can bid, so use topic targeting for only a small percentage of your overall buy.
>
>* Set up any negative targeting within the segment on [!DNL Proximic by Comscore].

**[!UICONTROL Device Targeting]:** (Optional) Specific device information, including device types, manufacturers, operating systems, browsers, and connectivity types, to include and exclude as targets. The types vary by placement type. To specify device targeting:

1. Click ![Edit](/help/dsp/assets/edit.png).
1. Specify the device details to include and exclude:
   1. In the left column, select the category.
   1. Specify targeting:
      * To include a value, click **[!UICONTROL Include]** next to the value name.
      * To exclude a value, click **[!UICONTROL Exclude]** next to the value name.
1. (Optional) To download a CSV file with the device targeting information to your browser's Downloads location, click **[!UICONTROL Export]**.
1. Click **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Optional) Specific internet service providers (ISPs) to either include or exclude (but not both) as targets. To specify ISP targeting:

1. Click ![Edit](/help/dsp/assets/edit.png).
1. Specify the ISPs to include or exclude:
   * To include ISPs:
      1. Click **[!UICONTROL Include ISPs]**.
      1. (Optional) Filter the list by keyword.
      1. Select the check box next to each ISP to target.
   * To exclude ISPs:
      1. Click **[!UICONTROL Exclude ISPs]**.
      1. (Optional) Filter the list by keyword.
      1. Select the check box next to each ISP to exclude.
1. (Optional) To download a CSV file with the ISP targeting information to your browser's Downloads location, click **[!UICONTROL Export]**.
1. Click **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Quality]

**[!UICONTROL DoubleVerify ABS segment ID]:** (Optional; [!DNL DoubleVerify] customers only; available for desktop pre-roll, standard and click-to-play display, and native display and video placements only; not supported for [default programmatic guaranteed placements for deals](/help/dsp/inventory/programmatic-guaranteed-about.md)) A [!DNL DoubleVerify Authentic Brand Safety] segment ID associated with the organization's [!DNL DoubleVerify] account to use for the placement. Specifying an ID blocks impressions post-bid using the custom brand safety rules configured for the specified segment ID. DSP bills your account for usage for the segment ID.

The ID must begin with "51" and consist of eight digits. By default, if a segment ID is specified in the advertiser account settings, then the advertiser-level ID is entered, but you can change the ID to use a different segment or delete the ID to disable the feature.

**[!UICONTROL Contextual filtering]:** (Applicable for desktop and mobile web display, native, and video ads) Types of [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39] contextual filters to apply. The advertiser-level defaults are selected for new placements, but you can change the settings:

<!-- Looks like we didn't rename this:
**[!UICONTROL Brand Safety categories]:** Types of [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39] brand safety category filters to apply. The advertiser-level defaults are selected for new placements, but you can change the settings:
-->

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Optional) One or more types of inventory context to block by default. Additional fees may apply.

* [!UICONTROL Peer 39]:

   * **Target sites that are:** (Optional) One or more types of inventory attributes to target by default. Additional fees may apply.

* [!UICONTROL ComScore]:

   * **Block sites that are:** (Optional) One or more types of inventory attributes to block by default. Additional fees may apply.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Optional) The degree of adult content for which to block ads by default: *[!UICONTROL Do Not Block]* (the default), *[!UICONTROL Standard]*, or *[!UICONTROL Strict]*. Additional fees may apply.

   * **[!UICONTROL Alcohol Content]:** (Optional) The degree of alcohol content for which to block ads by default: *[!UICONTROL Do Not Block]* (the default), *[!UICONTROL Standard]*, or *[!UICONTROL Strict]*. Additional fees may apply.

**[!UICONTROL Pre-bid fraud blocking]:** Types of sites to block based on fraudulent traffic and suspicious activities measured through [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39]. The advertiser-level defaults are selected for new placements, but you can change the settings:

* [!UICONTROL DoubleVerify]: (Applicable for desktop and mobile web display, native, video, and standard connected TV ads)

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** By default, blocks all 100% invalid traffic, including traffic on hijacked devices, for new placements. Additional fees may apply.

   * **[!UICONTROL Also block sites with]:** (Optional) An additional level of fraud and invalid traffic that causes DSP to block ads by default:  *[!UICONTROL None]* (the default, which doesn't block additional traffic), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*, or *[!UICONTROL >25% Average Fraud/IVT levels]*. Additional fees may apply.

* [!UICONTROL Peer 39]: (Applicable for desktop and mobile web display, native, and video ads)

   * **[!UICONTROL Block sites that are]:** (Optional) One or more types of fraud that cause DSP to block ads by default: *[!UICONTROL Fraud]* (which blocks all sites with fraud), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*, and/or *[!UICONTROL Fraud: Zero Ads]*. Additional fees may apply.

* [!UICONTROL Integral Ad Science]: (Applicable for desktop and mobile web display, native, and video ads)

   * **[!UICONTROL Block sites that are]:** (Optional) A type of suspicious website or app activity that causes DSP to block ads by default: *[!UICONTROL None]* (the default, which doesn't block ads based on suspicious activity), *[!UICONTROL Suspicious Activity - High Risk]*, or *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Additional fees may apply.

**[!UICONTROL Pre-bid viewability]:** (Applicable for desktop and mobile web display, native, and video ads) Which pre-bid viewability filters by [!DNL DoubleVerify], and [!DNL Integral Ad Science] to apply for the placement. The advertiser-level defaults are selected for new placements, but you can change the settings. Additional fees may apply.

**[!UICONTROL Ads.txt filtering]:** (Applicable for desktop and mobile web display, native, video, and audio ads) Which level of [Ads.txt](https://iabtechlab.com/ads-txt-about/) pre-bid filtering to use by applying each publisher's Authorized Digital Sellers list. The advertiser-level default is selected for new placements, but you can change the settings:

* *[!UICONTROL Opt out of ads.txt (default)]*: To buy inventory from all sellers.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: To prioritize buying inventory from a domain's authorized direct sellers and resellers.
* *[!UICONTROL Ads.txt sellers only]*: To buy inventory only from a domain's authorized direct sellers and resellers.
* *[!UICONTROL Ads.txt sellers only]*: To buy inventory only from a domain's authorized direct sellers.

**[!UICONTROL Attention Targeting]:** (Applicable for desktop and mobile web display, video, and standard connected TV ads) Targets [!DNL Adelaide] pre-bid segments with a specific attention level (high, medium, or low) based on the specified site, format, and ad size. The segments are updated weekly. **Note:** Using [!DNL Adelaide] segments for targeting incurs a CPM fee for each impression delivered with [!DNL Adelaide] attention targeting; this fee is separate from fees for [attention measurement](/help/dsp/campaign-management/campaigns/campaign-settings.md). For interactive pre-roll placements, you're charged only for VAST impressions.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] placements) Third-party tracking vendors approved by [!DNL Roku] include [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], and [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (Optional) Third-party event-tracking pixels to attach by default to all new ads in the placement. To specify event pixels:

1. Click ![Edit](/help/dsp/assets/edit.png).
1. Do any of the following:
   * To select an existing pixel, select the check box in the pixel row.
   * To create a pixel:
      1. Click **[!UICONTROL Create]**.
      1. Enter the following information:
         * **[!UICONTROL Pixel name]:** The pixel name; the maximum length is 500 characters. Use a name that helps you easily identify the pixel.
         * **[!UICONTROL Pixel event fires on]:** The event that triggers the pixel to fire. The available events vary by ad type.
         * **[!UICONTROL Pixel type]:** Whether the pixel is an *[!UICONTROL IMG URL]* (1x1 pixel image file), *[!UICONTROL HTML]*, or *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** The URL of the pixel image.
      1. Click **[!UICONTROL Create and attach]**.
   1. Click **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Optional) Conversion tracking pixels to attach by default to all new ads in the placement. To specify conversion pixels:

1. Click ![Edit](/help/dsp/assets/edit.png).
1. Do any of the following:
   * To select an existing pixel, select the check box in the pixel row.
   * To create a pixel:
      1. Click **[!UICONTROL Create]**.
      1. Enter the following information:
         * **[!UICONTROL Conversion pixel name]:** The pixel name; the maximum length is 500 characters. Use a name that helps you easily identify the pixel.
         * **[!UICONTROL Conversion category]:** The type of conversion.
         * **[!UICONTROL Impression conversion window]:** The number of days after an ad impression occurs in which the impression can be attributed to a conversion. The default is 30 days.
         * **[!UICONTROL Click conversion window]:** The number of days after an ad click occurs in which the click can be attributed to a conversion. The default is 30 days.
         * **[!UICONTROL Notes]:** (Optional) A description or other information about the pixel.
      1. Click **[!UICONTROL Create and attach]**.
      1. Implement the conversion pixel on the relevant webpages:
         1. In the main menu, go to **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. In the pixel row, click **[!UICONTROL edit]**.
         1. Copy the value(s) in the [!UICONTROL HTML Tag] and [!UICONTROL Flash Tag] fields, as needed, to provide to the advertiser or website contact.

            The advertiser's IT department or other group may need to schedule, or be informed about, the tag deployment.
   1. Click **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Optional) A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions. The package-level default is automatically applied for new placements, when applicable, unless you enter a different value.

>[!NOTE]
>
>Billable fees are reflected in the [!UICONTROL Net CPM] metric.

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Create a Placement](placement-create.md)
>* [Edit Placements](placement-edit.md)
>* [Manage Bid Multipliers for Placements](placement-manage-bid-multipliers.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Keyboard Shortcuts](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [FAQs About Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
