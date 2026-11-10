---
title: Run and download simulations from the [!UICONTROL Portfolios] view
description: Learn how to run a custom simulation and download weekly simulations from the Portfolios view.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
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
---
# Run and download simulations from the [!UICONTROL Portfolios] view

*Beta feature*

You can run a custom simulation for a single [optimized or active](portfolio-about.md#portfolio-status) portfolio and download automated weekly simulations for up to 100 portfolios from the [!UICONTROL Portfolios] view.

Running a custom simulation requires the [!UICONTROL Create Simulation] permission. Downloading weekly simulations requires the [!UICONTROL View Simulation] permission.

>[!NOTE]
>
>You can also [create or rerun a custom simulation from the [!UICONTROL Simulations] view](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md).

## Run a custom simulation {#run-simulation}

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Portfolios]**.

1. Do either of the following:

   * Hold the cursor over the portfolio row. Next to the portfolio name, click **[!UICONTROL ...]** > **[!UICONTROL Run Simulation]**.

   * Select the check box next to the portfolio. In the bulk actions toolbar, click **[!UICONTROL More] > [!UICONTROL Run Simulation]**.

1. Specify the [custom simulation settings](#custom-simulation-settings):

   1. On the **[!UICONTROL Basic Settings]** tab, enter a unique **[!UICONTROL Simulation Name]** and change the basic parameters as needed.

   1. (Optional) On the **[!UICONTROL Advanced Settings]** tab, change the advanced parameters.

   The selected portfolio's current settings are used as defaults. Changing simulation settings doesn't change the portfolio's settings.

1. Click **[!UICONTROL Next]**.

1. Review the settings and make changes as needed. 

1. Click **[!UICONTROL Submit & Run]**.

The request is submitted, and the [!UICONTROL Simulations] view opens. You can [download the simulation](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md) after it completes successfully.

## Download weekly simulations {#download-simulations}

You can download weekly simulations for one run date at a time as a [!DNL Microsoft Excel] workbook (XLSX file). Only active and optimized portfolios with available simulation reports for that date are included.

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Portfolios]**.

1. Select the check box next to each portfolio whose weekly simulation you want to download. Select up to 100 portfolios.

1. In the bulk actions toolbar, click **[!UICONTROL More] > [!UICONTROL Download Simulation]**.

1. In **[!UICONTROL Weekly Simulation]**, select a run date.

   The most recent available date is selected by default. If reports aren't available for some selected portfolios, the dialog shows how many portfolios will be excluded. Select another date if needed. You can't download a report when no selected portfolios have an available simulation for that date.

1. Click the download button, whose label includes the number of portfolios with available reports (for example, **[!UICONTROL Download 2 portfolios]**).

   The file is downloaded according to your browser's normal procedure. The completion message indicates how many portfolios were included.

To download custom simulations or select individual weekly simulations, use the [[!UICONTROL Simulations] view](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md).

## Custom simulation settings {#custom-simulation-settings}

For more information about the custom simulation settings, see the Optimization Guide, which is available from within Search, Social, & Commerce.

>[!MORELIKETHIS]
>
>* [(New UI) View portfolio performance details](portfolio-details.md)
>* [About portfolios](portfolio-about.md)
>* [Run or rerun a custom simulation](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md)
>* [Download simulations](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md)
