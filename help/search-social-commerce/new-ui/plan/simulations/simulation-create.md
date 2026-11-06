---
title: Run or rerun a custom simulation
description: Learn how to run or rerun a custom simulation for a portfolio.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 0ee62d04-fdc4-445c-90fb-71d5a40a9ed0
TQID: 'https://experienceleague.adobe.com/DlSJEcKXOxVz6UXVpAjQqaiwDTakgJ4SS6rsQUxkQIE'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# Run or rerun a custom simulation

*Beta feature*

You can generate a custom simulation for an [optimized or active](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#portfolio-status) portfolio. You can also select a simulation in the list to run a new simulation for the same portfolio, or rerun simulations with their existing settings.

Creating a custom simulation requires the [!UICONTROL Create Simulation] permission. Selecting a portfolio requires the [!UICONTROL View Portfolios] permission.

<!-- You can't run sims for portfolios with legacy keyword-level optimization when they include smart bidding campaigns. Clarify all exceptions so users don't find out via error messages. -->

[!UICONTROL Admin] and [!UICONTROL Account Manager] users can see simulations created by other users. All other users can see only the custom simulations they create.

## Create a new simulation {#simulation-create}

You can start from the [!UICONTROL Simulations] view or [run a custom simulation from the [!UICONTROL Portfolios] view](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#run-simulation).

1. In the main menu, click **[!UICONTROL Plan] > [!UICONTROL Simulations]**.

1. Clear any selected simulation rows, and then click **[!UICONTROL Run Simulation]**.

1. Select the portfolio:

   1. Click **[!UICONTROL Select Portfolio]**.

   1. Select the portfolio.

      To search for portfolios that include a specific text string, begin entering the text string within the search field. Values aren't case-sensitive.

   1. Click **[!UICONTROL Proceed]**.

1. Specify the [custom simulation settings](#custom-simulation-settings):

   1. (Optional) To change the portfolio used for the simulation, click **[!UICONTROL Change Portfolio]** next to the portfolio name, select the portfolio, and then click **[!UICONTROL Proceed]**.
   
   1. On the [!UICONTROL Basic Settings] tab:
   
      1. Enter a unique **[!UICONTROL Simulation Name]**.
      
      1. (Optional) Change the basic parameters for the simulation.
   
   1. (Optional) On the [!UICONTROL Advanced Settings] tab, change the advanced parameters for the simulation.

   The existing parameters for the selected portfolio are specified by default. Changing the values will show you the results that different parameters would produce without changing the portfolio's existing parameters.

1. Click **[!UICONTROL Next]**.

1. Review the settings, and edit settings as needed.

1. Click **[!UICONTROL Submit & Run]**.

The request is submitted, and the [!UICONTROL Simulations] view opens. When the simulation report is available, you and any other email recipients specified receive a notification with a download link. You can also [download the simulation from the [!UICONTROL Simulations] view](simulation-download.md).

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## Rerun a simulation with the existing settings {#rerun-a-simulation-with-the-existing-settings}

You can rerun up to 10 simulations at a time with their existing settings. Simulations with a status of [!UICONTROL Queued] or [!UICONTROL In Progress] can't be rerun. If your selection includes these simulations, they are skipped, and the remaining simulations are submitted.

1. In the main menu, click **[!UICONTROL Plan] > [!UICONTROL Simulations]**.

1. Select the check boxes next to the simulations you want to rerun.

1. In the toolbar above the data table or in the bulk actions toolbar, click **[!UICONTROL Re-Run Simulation]**.

The request is submitted, and the view refreshes.

## Run a new simulation for a portfolio in the list {#edit-the-settings-for-an-existing-simulation-and-rerun-it}

Selecting a simulation before you click [!UICONTROL Run Simulation] selects its portfolio for a new simulation. The form uses the portfolio's current settings, not the selected simulation's settings. This action doesn't edit the existing simulation.

1. In the main menu, click **[!UICONTROL Plan] > [!UICONTROL Simulations]**.

1. Select the check box next to a simulation for the portfolio you want to use.

   If you select multiple simulations, they must all use the same portfolio. The portfolio must be active or optimized.

1. Above the data table, click **[!UICONTROL Run Simulation]**.

1. Specify the [custom simulation settings](#custom-simulation-settings), including a unique **[!UICONTROL Simulation Name]**. Change the parameters on the **[!UICONTROL Basic Settings]** and **[!UICONTROL Advanced Settings]** tabs as needed.

1. Click **[!UICONTROL Next]**.

1. Review the settings, and edit settings as needed.

1. Click **[!UICONTROL Submit & Run]**.

The request is submitted, and the [!UICONTROL Simulations] view opens. You can [download the simulation](simulation-download.md) after it completes successfully.

## Custom simulation settings {#custom-simulation-settings}

For more information about the custom simulation settings, see the Optimization Guide, which is available from within Search, Social, & Commerce.

>[!MORELIKETHIS]
>
>* [About simulations](simulation-about.md)
>* [View simulation details](simulation-view.md)
>* [Download simulations](simulation-download.md)
