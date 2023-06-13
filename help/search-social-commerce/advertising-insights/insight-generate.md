---
title: Generate an [!DNL Advertising Insight]
description: Learn how to create an [!DNL Advertising Insight].
exl-id: 242095c9-25f0-4954-b1a8-5ea3db312afd
---
# Generate an [!DNL Advertising Insight]

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Advertising Insights]**.

2. Click the insight that you want to generate.

3. Specify the insight settings:

   1. (Some reports; optional) Specify the date ranges for the insight.

   2. (Most insights) Select the portfolio to analyze.

      In general, all optimized and active portfolios that contain active campaigns are available. For some insights, you can filter the portfolio list to include **[!UICONTROL Only Optimized Portfolios]**.
      
      For [!UICONTROL Day of Week] insights, only portfolios that have enough spend, and that also spent to target in the last two days, are available.

   3. ([!UICONTROL Event Path Beta] insight only) Do the following:

      1. Select the **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* (to upload a [!UICONTROL Channel Assist Report] or [!UICONTROL Campaign Assist Report] and classify the user events into distinct groups for analysis) or *[!UICONTROL Analyze classified events]* (to upload event groups and use them to generate the insight).

      1. Click **[!UICONTROL Select]** to locate a file in XLSX and ZIP (compressed XLSX) format, and then click **[!UICONTROL Upload]**.

   4. ([!UICONTROL Google Account Audit] insight only) Do the following:

      1. Enter the **[!UICONTROL Advertiser Name]** and **[!UICONTROL Account Name]**.
      
      1. Select the **[!UICONTROL Account Currency]**, **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* or *[!UICONTROL United Kingdom]*), and the **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*, *[!UICONTROL French]*, or *[!UICONTROL German]*).
      
      1. Click **[!UICONTROL Select]** to locate campaign, keyword, and change history reports downloaded for the account from the [!DNL Google Ads] web user interface and a bulksheet file downloaded for the account from the [!DNL Google Ads Editor] application. Then click **[!UICONTROL Upload]**.

         All files must be in CSV, TSV, TXT, or ZIP (compressed CSV, TSV, or TXT) format.

   5. ([!UICONTROL Location Target Performance] insight only; optional) To aggregate the data daily rather than as a summary, select the **[!UICONTROL Time Aggregation]** of *[!UICONTROL Daily]*.

   6. ([!UICONTROL Normalized Sim (Combined)] insight only) Do the following:

      1. In the **[!UICONTROL Step]** field, specify the number of target spend levels, or steps, to include in the insight. The value can be between three (3) and 100.

      1. In the **[!UICONTROL Type]** field, select the simulation type:

         * *[!UICONTROL Optimized Multi-portfolio]*: Generates a single simulation across multiple portfolios with the same objective and currency.

         * *[!UICONTROL Individual Normalized]*: Generates an individual simulation for each portfolio selected. The portfolios may have different objectives and currencies.

   7. ([!UICONTROL Portfolio Launch] insight only; optional) To specify a launch date in the future, specify a date in the **[!UICONTROL Optional Date]** field.

   8. ([!UICONTROL Quality Score] insight only) Select the applicable ad network.

   9. ([!UICONTROL Query Cross Matching] insight only) In the **[!UICONTROL Google Accounts]** menu, select the account.

4. Click **[!UICONTROL Generate Insight]**.

   You'll receive notification when the job is completed or fails based on your [configured notification settings](/help/search-social-commerce/notifications/notification-edit.md) for [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [About [!UICONTROL Advertising Insights]](insight-about.md)
>* [View or save an [!DNL Advertising Insight]](insight-view-save.md)
>* [Delete an [!DNL Advertising Insight]](insight-delete.md)
