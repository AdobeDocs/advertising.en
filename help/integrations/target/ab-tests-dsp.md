---
title: Configure A/B Tests for Adobe Advertising DSP Ads in Adobe Target
description: Learn how to set up an A/B test in [!DNL Target] for your DSP ads.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
---
# Configure A/B Tests in Adobe Target for Advertising DSP Ads

*Advertisers with Advertising DSP only*

Adobe Advertising and Adobe Target make it even easier for marketers to deliver a personalized and connected experience across paid media and on-site messaging. By sharing signals between the products, you can:

* Decrease site fall-through rates by linking customers’ ad exposure from DSP campaigns to their on-site experiences.

* Establish A/B testing by mirroring on-site experiences with advertising messaging using Adobe Audience Manager exposure data and click-to-feed [!DNL Target] audiences.

* Measure the impact of unified messaging on an on-site objective lift with simple visualizations in Adobe Analytics for [!DNL Target].

See the following sections for the prerequisites and for instructions to set up click-through and view-through tracking, implement signal sharing between DSP and [!DNL Target] and set up an A/B test activity, and set up [!DNL Analytics] Analysis Workspace to view the test data.

If you have additional questions, contact adcloud_support@adobe.com.

## Prerequisites

This use case requires the following products and integrations:

* [!DNL Target]

* [[!DNL Analytics] for Advertising](/help/integrations/analytics/overview.md) integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integration

* Audience Manager (required for view-through testing only)

## Step 1: Set up the Click-through Framework {#click-through-framework}

![Click-through framework](/help/integrations/assets/target-ct-framework.png)

When you add DSP macros to a click-through URL (the URL displayed when a user clicks an ad and reaches the landing page), DSP automatically captures the placement key by including `${TM_PLACEMENT_ID}` in the click-through URL. This macro captures the alphanumeric placement key and not the numeric placement ID.

![Click-through URL appended to the landing page URL](/help/integrations/assets/target-ct-url.jpg)

### (DSP Only) Add DSP Macros to Your Click-through URLS

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Within [!DNL Flashtalking] or Google Campaign Manager 360, manually update the click-through URL for each ad to include the macros required to capture AMO ID variables. The AMO ID variables are used to send click data to Adobe Analytics and to share placement keys for A/B testing. See the following pages for instructions:

* [Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md). **Note:** This procedure isn't necessary if your organization has a direct partnership with [!DNL Flashtalking] and you use data-pass macros to track the `s_kwcid` and `ef_id` tracking parameters per the [!DNL Flashtalking] support documentation at [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros).

* [Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md)

Contact your Adobe Account Team to retrieve the required placement key and finalize the setup, and to make sure that each click-through URL is populated with the placement key.

## Step 2: Set up the View-through Framework Using Audience Manager {#view-through-framework}

![View-through framework](/help/integrations/assets/targetr-vt-framework.png) 

By adding an Audience Manager impression event pixel in your ad tags and placement settings, you can create a test segment for additional view-through testing opportunities.

1. Implement an Audience Manager impression event pixel in your ad tags and DSP placement settings.

   For instructions, see "[Collect Media Exposure Data from Advertising DSP Campaigns](/help/integrations/audience-manager/media-data-integration/collect.md)."

   Make sure you add [DSP macros](/help/dsp/campaign-management/macros.md) to capture all data you want the impression event pixel to pass back, including `${TM_PLACEMENT_ID_NUM}` for the numeric placement ID.

   >[!NOTE]
   >
   >Click-tracking URLs include the `${TM_PLACEMENT_ID}` macro for the alphanumeric placement key, instead of `${TM_PLACEMENT_ID_NUM}` for the numeric placement ID.

1. Configure an Audience Manager segment from the DSP impression data:

   1. Verify that segment data is available:

      1. [Search for the signal](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) for the [key-value pair](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) that determines at what level the segment users are grouped.
      
          Use a [supported key](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) with a value that corresponds to a macro that you added to the Audience Manager impression event pixel.
          
          For example, to group users for a particular placement, use the `d_placement` key. For the value, use an actual numeric placement ID (such as 2501853) that's captured by the DSP macro `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->
          
          If the search results show user counts for the key-value pair, which indicates that the pixel was placed correctly and data is flowing, then continue to the next step.

   1. [Create a rule-based trait](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) for segment creation in Audience Manager.

      * Name the trait so that it’s easily identifiable within test activities. Store the trait in whichever folder you prefer.
      
      * Select `Ad Cloud` as the **[!UICONTROL Data Source]**.
      
      * For the trait expression, use `d_event` as the **[!UICONTROL Key]** and `imp` as the **[!UICONTROL Value]**.

   1. [Set up a test segment](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) for the new trait in Audience Manager, selecting `Ad Cloud` as the **[!UICONTROL Data Source]**.

       Audience Manager automatically splits the segment into a control group that receives the standard landing page experience and a test group that received a personalized onsite experience.

## Step 3: Set Up an A/B Test Activity in [!DNL Target] for DSP

The following instructions highlight information pertaining to the DSP use case.

1. [Sign in to Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Create an A/B test](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. In the **[!UICONTROL Enter Activity URL]** field, enter the landing page URL for the test.

       >[!NOTE]
       >
       >You can use multiple URLs to test view-through site entry. For more information, see "[Multipage Activity](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html)." You can easily identify top entries by page URL by creating a [Site Entry report](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports) in Analytics.

   1. In the **[!UICONTROL Goal]** field, enter the success metric for the test.

       >[!NOTE]
       >
       >Make sure that [!DNL Analytics] is enabled as a data source within [!DNL Target], and that the correct report suite is selected.

   1. Set the **[!UICONTROL Priority]** to `High` or `999` to prevent conflicts when users in the test segment receive an incorrect on-site experience.

   1. Within **[!UICONTROL Reporting Settings]**, select the **[!UICONTROL Company Name]** and **[!UICONTROL Report Suite]** connected to your DSP account.

       For additional reporting tips, see "[Reporting best practices and troubleshooting](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)."

   1. In the **[!UICONTROL Date Range]** field, enter the appropriate start and end dates for the test.

   1. Add audiences to the activity:

      1. Choose the [segment that you previously created in Audience Manager to test view-through audiences](#view-through-framework).

      1. Select **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**, and enter the DSP placement key in the **[!UICONTROL Value]** field to use the Target query string parameters for click-through audiences.

   1. For the **[!UICONTROL Traffic Allocation Method]**, select **[!UICONTROL Manual (Default)]** and split the audience 50/50.

   1. Save the activity. 

1. Use [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) to make design changes to the A/B test landing page template.

   * Experience A: Don't edit because it's the default/control landing page experience without personalization.

   * Experience B: Use the [!DNL Target] user interface to customize the landing page template based on the assets included in the test (such as headlines, copy, button placement, and creatives).

   >[!NOTE]
   >
   >For example creative test use cases, contact your Adobe Account Team.

## Step 4: Set up Your [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) is a cross-solution integration that lets advertisers create [!DNL Target] activities based on [!DNL Analytics] conversion metrics and audience segments and then measure the results using [!DNL Analytics] as the reporting source. All reporting and segmentation for that activity is based on [!DNL Analytics] data collection.

For more information about [!DNL Analytics for Target], including a link to implementation instructions, see "[Adobe Analytics as the reporting source for Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)".

### Set up the [!DNL Analytics for Target] Panel

In Analysis Workspace, configure the [!DNL Analytics for Target panel] to analyze your [!DNL Target] activities and experiences. Keep in mind the following important pointers and information about your reports.

#### Metrics

* Create a panel within the workspace specific to the Adobe Advertising campaign, package, or placement for which the test was run. Use summary visualizations to show Adobe Advertising metrics in the same report as the [!DNL Target] test performance.

* Prioritize using on-site metrics (such as visits and conversions) to measure performance.

* Understand that aggregated media metrics from Adobe Advertising (such as impressions, clicks, and costs) can't be matched to [!DNL Target] metrics.

#### Dimensions

The following dimensions pertain to [!DNL Analytics for Target]:

* **[!UICONTROL Target Activities]**: Name of the A/B Test

* **[!UICONTROL Target Experiences]**: Names of landing page experiences used within the activity

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**: The activity name and experience name in the same row

### Troubleshooting Analytics for [!DNL Target] Data

Within Analysis Workspace, if you notice that activity and experiences data is minimal or not populating, then do the following:

* Verify that the same [!UICONTROL Supplemental Data ID] (SDID) is used for both [!DNL Target] and [!DNL Analytics]. You can verify the SDID values by using the [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) on the landing page to which the campaign is driving users.

  [Supplemental Data ID (SDID) values in Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* On the same landing page, verify that a) the [!UICONTROL Hostname] shown in the Adobe Debugger under [!UICONTROL Solutions] > [!UICONTROL Target] matches b) the [!UICONTROL Tracking Server] shown in [!DNL Target] for the activity (under [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] requires an [!DNL Analytics] tracking server to be sent in calls from [!DNL Target] to the [!DNL Modstats] data collection server for Analytics.<!-- just "to Analytics?"-->

  [Hostname value in Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

  [Tracking Server value in Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Further Reading

* [Integrate Target with Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Explains how to set up [!DNL Target] reporting in Analysis Workspace.
* [A/B Test Overview](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Describes A/B test activities, which you can use with DSP ads.
* [Experiences and offers](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Explains [!DNL Target] tools to determine the on-site content to which DSP test users are exposed.
* [Signals, Traits, and Segments](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Defines some of the Audience Manager tools that can help with DSP view-through testing.
* [Overview of Analytics for Advertising](/help/integrations/analytics/overview.md) - Introduces Analytics for Advertising, which allows you to track click-through and view-through site interactions in your Analytics instances.

>[!MORELIKETHIS]
>
>* [Configure A/B Tests in Adobe Target for Advertising Search, Social, & Commerce Ads](ab-tests-search.md)
