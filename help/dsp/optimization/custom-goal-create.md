---
title: Create a Custom Goal
description: Create a Custom Goal
feature: DSP Optimization
exl-id: 81b0acfa-085d-495b-9516-576b952b1307
---
# Create a Custom Goal

 You can create custom goals as *objectives* within [!DNL Advertising Search, Social, & Commerce].

To create a custom goal, the DSP account must be linked to a [!DNL Search, Social, & Commerce] account with the same Adobe Experience Cloud organization ID, from within the [!DNL Search, Social, & Commerce] client settings. If your DSP account isn't linked to a [!DNL Search, Social, & Commerce] account, contact your Adobe Account Team.

>[!TIP]
>
>See the [best practices for creating custom goals](custom-goal-best-practices.md) for tips on how to configure your custom goals.

1. Log in to [!DNL Advertising Search, Social, & Commerce] at (users in North America) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) or (all other users) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Make sure the metrics that you want to include in your goal have been tracked, are available in the product, and include a display name:
    1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions]**.
    1. Locate the metric, and make sure that **[!UICONTROL Show in UI and Reports]** is enabled for the metric.
    1. If the metric doesn't have a value in the **[!UICONTROL Display Name]** column, click in the cell, enter the display name, and then click **[!UICONTROL Apply].**
1. Create the custom goal as an *objective*:
    1. In the main menu, click **[!UICONTROL Search]** > **[!UICONTROL Optimization] > [!UICONTROL Objectives]**.
    1. In the toolbar, click **[!UICONTROL Create objective].**
    1. Enter the objective settings:
        1. In the **[!UICONTROL Change Objective Name]** field, enter the objective name.

           The objective name will be shown in the [!UICONTROL Custom Goals] list in the DSP package settings.

        1. Associate properties with the objective:

           >[!NOTE]
           >
           > All conversion metrics tracked for the advertiser are listed by default in the [!UICONTROL Available Properties] list.

            * To import a CSV file with conversion metrics and their weights, click **[!UICONTROL Import]** and locate the file to import.

               The imported conversion metrics must already exist for the advertiser; the names aren't case-sensitive.

               The imported conversion metrics replace any existing properties specified.

            * To manually specify the first conversion metric with the default weight (1), select from a list of all conversion metrics tracked for the advertiser.

            * To manually add another conversion metric with the default weight (1), click **[!UICONTROL +]** .

               >[!TIP]
               >
               > To search for a metric in the list, enter a string from anywhere within the metric name.

            * To manually add multiple conversion metrics, click **[!UICONTROL Add Multiple Properties].** For each conversion metric you want to add, click the metric name in the [!UICONTROL Available Properties] column and drag it into the [!UICONTROL Added Properties] column. When you're finished adding metrics, click **[!UICONTROL Add]**.

               >[!TIP]
               >
               >* To search for a metric in the list, enter a string from anywhere within the metric name in the input field.
               >* To filter the list to exclude metrics that are excluded in reports, select the option **[!UICONTROL Hide properties excluded from reports].**

            * (When the objective contains multiple conversion metrics) To change the weight of a metric relative to the other metrics in the objective, enter values in the **[!UICONTROL Weight]** field(s).

        1. At the bottom of the settings, click **[!UICONTROL Save]**.

Once you create an objective, you can assign it to a DSP package as a custom goal when the optimization goal ends with "[!UICONTROL - Custom Goal]" (such as "[!UICONTROL Highest ROAS - Custom Goal]").

>[!TIP]
>
>For optimum performance, the combined metrics in the custom goal (objective) must total at least ten conversions per day. When they don't, the best practice is to add additional supporting conversion metrics, such as product pages or application starts, to the objective. See [Best Practices for Building a Custom Goal](custom-goal-best-practices.md) for guidelines.

>[!MORELIKETHIS]
>
>* [About Custom Goals](custom-goal-about.md)
>* [Best Practices for Building a Custom Goal](custom-goal-best-practices.md)
>* [Optimization Goals and How to Use Them](optimization-goals.md)
>* [Package Settings](/help/dsp/campaign-management/packages/package-settings.md)
> * [How DSP Optimizes Your Campaigns](optimization-how-dsp-optimizes-campaigns.md)
