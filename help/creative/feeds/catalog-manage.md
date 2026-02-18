---
title: Manage feed catalogs
description: Learn how to manage feed catalogs.
feature: Creative Dynamic Creatives
exl-id: d3ee20ba-5359-4dbe-bc76-269dc800843c
---
# Manage feed catalogs

Processed feed catalogs are sets of potential ad variations created from a specified feed file and a specified feed template. Dynamic HTML5 and video ads, but not static HTML5 ads, require a catalog to create dynamic ads.

Before you can create ad variations and [add dynamic ads to a creative library](/help/creative/creative-libraries/creative-add-dynamic.md), process the catalog. You can later update the feed file and reprocess the catalog to create a new set of ad variations.<!-- I should list somewhere what happens when you add, update, or remove: I don't think we rewrite existing ads in the creative library, but only add to them. -->

Each feed file can process up to 500 rows with video assets.

## Create a catalog {#feed-catalog-create}

>[!NOTE]
>
>You can also directly upload a catalog when you [add dynamic creatives to a creative library](/help/creative/creative-libraries/creative-add-dynamic.md). Any catalogs you create there become available within the [!UICONTROL Catalogs] view for future use.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Catalog]** tab.

1. In the upper right, click  **[!UICONTROL Create]** >  **[!UICONTROL Template]**.

1. Specify the [catalog settings](#catalog-settings) as needed.

1. Click **[!UICONTROL Next]**.

1. Review the potential ad variations that can be created for the catalog.

1. Click **[!UICONTROL Save]**.

## Edit a catalog

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Catalog]** tab.

1. Hold the cursor over the template row and click **[!UICONTROL Edit]**.

1. Edit the [catalog settings](#catalog-settings) as needed.

1. Review the potential ad variations that can be created for the catalog.

1. Click **[!UICONTROL Save]**.

## Process a catalog {#feed-catalog-process}

Processing a catalog makes the ad variations available to create dynamic HTML5 ads.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Catalog]** tab.

1. Hold the cursor over the template row and click **[!UICONTROL Run Now]**.

## Pause an active catalog

Pause a catalog to make it inactive.<!-- Can you Activate it again? -->

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template row and click **[!UICONTROL Pause]**.

<!-- Verify if this is available:  1. In the confirmation message, click **[!UICONTROL Pause]**. -->

## Activate a paused catalog

<!-- Verify if this is available. -->

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template row and click **[!UICONTROL Activate]**.

## Archive a catalog

Archive a catalog to delete it.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template row and click **[!UICONTROL Archive]**.

1. In the confirmation message, click **[!UICONTROL Archive]**.

## Catalog settings {#catalog-settings}

**[!UICONTROL Advertiser]:** The advertiser who can use the catalog.

**[!UICONTROL Asset]:** The feed file to use as input for the catalog.

**[!UICONTROL Catalog Name]:** A unique catalog name for the specified advertiser. By default, the feed file name is used, including the file extension, which is the best practice for identification.<!-- must it have a file extension? -->

**[!UICONTROL Template]:** The feed template to use for mapping fields in the specified asset/feed file to fields on the Advertising Creative backend.

>[!MORELIKETHIS]
>
>* [Track the status of catalog processing jobs](/help/creative/feeds/job-status-track.md)
>* [Workflows for dynamic ads](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Manage asset files](/help/creative/feeds/asset-manage.md)
>* [Manage feed templates](/help/creative/feeds/feed-template-manage.md)
>* [Manage dynamic ad templates](/help/creative/ad-templates/ad-template-manage.md)
>* [Add dynamic creatives to a creative library](/help/creative/creative-libraries/creative-add-dynamic.md)
