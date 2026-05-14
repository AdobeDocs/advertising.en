---
title: Run or rerun a custom simulation
description: Learn how to run or rerun a custom simulation for a portfolio.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 0ee62d04-fdc4-445c-90fb-71d5a40a9ed0
TQID: https://experienceleague.adobe.com/DlSJEcKXOxVz6UXVpAjQqaiwDTakgJ4SS6rsQUxkQIE
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
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

You can generate a custom simulation for an [optimized or active](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) portfolio. You also can either change the parameters of an existing simulation and regenerate the simulation or rerun an existing simulation with the existing parameters.

<!-- You can't run sims for portfolios with legacy keyword-level optimization when they include smart bidding campaigns. Clarify all exceptions so users don't find out via error messages. -->

[!UICONTROL Admin] and [!UICONTROL Account Manager] users can see simulations created by other users. All other users can see only the custom simulations they create.

## Create a new simulation 

1. Do either of the following:

  * From the [!UICONTROL Simulations] view:

    1. In the main menu, click **[!UICONTROL Plan] > [!UICONTROL Simulations]**.

    1. Above the data table, click **[!UICONTROL Run Simulation]**.

    1. Select the portfolio:
    
       1. Click **[!UICONTROL Select Portfolio]**.
       
       1. Select the portfolio.
       
          To search for portfolios that include a specific text string, begin entering the text string within the search field. Values aren't case-sensitive.
       
       1. Click **[!UICONTROL Proceed]**.

  * From the [!UICONTROL Portfolios] view:

    1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Portfolios]**.

    1. Hold the cursor over the portfolio row. Next to the portfolio name, click **[!UICONTROL ...]** > **[!UICONTROL Run Simulation]**.

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

When the simulation report is available, you and any other email recipients specified receive a notification with a link to download the data in a ZIP file that contains one workbook (XLSX file).

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## Edit the settings for an existing simulation and rerun it

1. In the main menu, click **[!UICONTROL Plan] > [!UICONTROL Simulations]**.

1. Select the check box next to the simulation to regenerate.

1. Above the data table, click **[!UICONTROL Run Simulation]**.

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

When the simulation report is available, you and any other email recipients specified receive a notification with a link to download the data in a ZIP file that contains one workbook (XLSX file).

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## Rerun a simulation with the existing settings

You can rerun simulations that aren't currently queued.

1. In the main menu, click **[!UICONTROL Plan] > [!UICONTROL Simulations]**.

1. Select the check boxes next to the simulations you want to rerun.

1. In the toolbar above the data table, click ![Rerun](/help/search-social-commerce/assets/rerun.png "Rerun").

## Custom simulation settings {#custom-simulation-settings}

For more information about the custom simulation settings, see the Optimization Guide, which is available from within Search, Social, & Commerce.

>[!MORELIKETHIS]
>
>* [About simulations](simulation-about.md)
>* [View simulation details](simulation-view.md)
>* [Download simulations](simulation-download.md)
