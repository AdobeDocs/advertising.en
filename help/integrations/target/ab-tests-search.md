---
title: Configure A/B Tests for Adobe Advertising Search, Social, & Commerce Ads in Adobe Target
description: Learn how to set up an A/B test in [!DNL Target] for your [!DNL Google Ads] and [!DNL Microsoft Advertising] ads in Search, Social, & Commerce.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
---
# Configure A/B Tests in Adobe Target for Advertising Search, Social, & Commerce Ads

*Advertisers with Advertising Search, Social, & Commerce only*

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts only*

Adobe Advertising and Adobe Target make it easy to set up landing page experience A/B tests for digital advertising traffic [!DNL Google Ads] and [!DNL Microsoft Advertising] to:

* Improve conversion rates (CVR) and acquisition efficiency measures (such as CPA, CPL, and CAC).

* Deliver a more personalized landing page experience that's relevant to the ad (for example, matching the image/video creative, copy, keyword, or other advertising signal to the landing page).

You can also combine the native [[!DNL Analytics] for Advertising](/help/integrations/analytics/overview.md) and [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integration reporting dimensions that are integrated into Adobe Analytics to measure and visualize your test data with [!DNL Analytics] metrics and success events.

See the following sections for the prerequisites, instructions to set up A/B tests in [!DNL Target] for click-through traffic from ads in Search, Social, & Commerce, and tips on how to measure and visualize your tests in [!DNL Analytics].

## Prerequisites

### Required Products

* Search, Social, & Commerce
* [!DNL Target]

### Recommended Products and Integrations

* [!DNL Analytics]

* [[!DNL Analytics] for Advertising](/help/integrations/analytics/overview.md) integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integration

## Step 1: Create an A/B Test Activity in [!DNL Target] for Search, Social, & Commerce

The following instructions highlight information pertaining to the Search, Social, & Commerce use case.

1. [Log in to Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Create an A/B test](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. In the **[!UICONTROL Enter Activity URL]** field, enter the landing page URL for the test.

   1. In the **[!UICONTROL Goal]** field, enter the success metric for the test.

       >[!NOTE]
       >
       >Make sure that [!DNL Analytics] is enabled as a data source within [!DNL Target], and that the correct report suite is selected.

   1. Set the **[!UICONTROL Priority]** to `High` or `999` to prevent conflicts when users in the test segment receive an incorrect on-site experience.


   1. Within **[!UICONTROL Reporting Settings]**, select the **[!UICONTROL Company Name]** and **[!UICONTROL Report Suite]** connected to your Search, Social, & Commerce account.

       For additional reporting tips, see "[Reporting best practices and troubleshooting](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)."

   1. In the **[!UICONTROL Date Range]** field, enter the appropriate start and end dates for the test.

   1. Select **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. In the **[!UICONTROL Value]** field, enter the [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID], or [!UICONTROL Network Ad ID] for the relevant ad network entity in Search, Social, & Commerce. This allows you to use the [!DNL Target] query string parameters for click-through audiences for the entity.
   
      You can find the ID by [adding the relevant ID column to the entity view](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] column in the [!UICONTROL Accounts] view](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] column in the [!UICONTROL Accounts] view")

      Work with your Adobe Account Team if you need assistance.

   1. For the **[!UICONTROL Traffic Allocation Method]**, select **[!UICONTROL Manual (Default)]** and split the audience 50/50.
   
   1. Save the activity. 

1. Use [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) to make design changes to the A/B test landing page template.

   * Experience A: Don't edit because it's the default/control landing page experience without personalization.

   * Experience B: Use the [!DNL Target] user interface to customize the landing page template based on the assets included in the test (such as headlines, copy, button placement, and creatives).

   >[!NOTE]
   >
   >For example creative test use cases, contact your Adobe Account Team.

## Step 2: Set up Your [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

[!DNL Analytics for Target] (A4T) is a cross-solution integration that lets advertisers create [!DNL Target] activities based on [!DNL Analytics] conversion metrics and audience segments and then measure the results using [!DNL Analytics] as the reporting source. All reporting and segmentation for that activity is based on [!DNL Analytics] data collection.

For more information about [!DNL Analytics for Target], including a link to implementation instructions, see "[Adobe Analytics as the reporting source for Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)".

### Set up the [!DNL Analytics for Target] Panel

In Analysis Workspace, configure the [!DNL Analytics for Target panel] to analyze your [!DNL Target] activities and experiences. Keep in mind the following important pointers and information about your reports.

#### Metrics

* Create a panel within the workspace specific to the Adobe Advertising account, campaign, or ad group<!-- only applicable entities? --> for which the test was run. Use summary visualizations to show Adobe Advertising metrics in the same report as the [!DNL Target] test performance.

* Prioritize using on-site metrics (such as visits and conversions) to measure performance.

* Understand that aggregated media metrics from Adobe Advertising (such as impressions, clicks, and costs) can't be matched to [!DNL Target] metrics.

#### Dimensions

The following dimensions pertain to [!DNL Analytics for Target]:

* **Target Activities**: Name of the A/B Test

* **Target Experiences**: Names of landing page experiences used within the activity

* **Target Activity** > **Experience**: The activity name and experience name in the same row

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
* [A/B Test Overview](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Describes A/B test activities, which you can use with Search, Social, & Commerce ads.
* [Overview of Analytics for Advertising](/help/integrations/analytics/overview.md) - Introduces Analytics for Advertising, which allows you to track click-through and view-through site interactions in your Analytics instances.

>[!MORELIKETHIS]
>
>* [Configure A/B Tests in Adobe Target for Advertising DSP Ads](ab-tests-dsp.md)
