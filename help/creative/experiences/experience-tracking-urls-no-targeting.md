---
title: Customize the tracking URLs for an experience without targeting
description: Learn how to customize the tracking URLs for each creative in an experience without decision tree targeting.
feature: Creative Experiences
exl-id: 03a10285-c0df-4bc3-92c7-c1c2ea3f8129
---
# Customize the tracking URLs for an experience without decision tree targeting

*Closed beta*

For experiences without decision tree targeting, you can create up to five custom impression-tracking URLs, five custom click-tracking URLs, and one custom landing page URL for each individual creative used for the ad experience tag. You can customize the tracking URLs from within [!UICONTROL Tag Manager].

The custom URLs are used only for ads created from the ad experience tag and aren't saved in the base creative settings in [!UICONTROL Creative Libraries].

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Do one of the following:

   * In card view, click **[!UICONTROL ...]** next to the experience name, and then click **[!UICONTROL Tag Manager]**.
     
   * In table view, hold the cursor over the row, click **[!UICONTROL More]**, and then click **[!UICONTROL Tag Manager]**

1. (If a tag for the ad size doesn't exist) Create a tag for the applicable creative size.

   You can create one or more tag for each creative size used for the experience.

   1. In the upper right, click **[!UICONTROL Create Tag]**.

   1. Enter a unique **[!UICONTROL Tag name]** and select the **[!UICONTROL Tag size]**.

      The sizes of the default image creatives for the experience determine the available sizes.

   1. Click **[!UICONTROL Create]**.

1. Hold the cursor over the row for the applicable ad tag and click ![Edit tracking URLs](/help/creative/assets/edit-gray.png "Edit tracking URLs") **[!UICONTROL Tracking URLs]**. <!-- For targeted experiences, this is "EDIT Tracking URLs" --><!-- Tag Manager has only a list view, but no card view, as of 2/2. >

   The [!UICONTROL Click Tracking URLs], [!UICONTROL Impression Tracking URLs], and [!UICONTROL Landing URLs] tabs list the names of all creatives in the applicable sizes in the assigned bundles. The sizes of the default image creatives for the experience determine the available sizes.<!-- There's no distinct "Creative Sizes" setting. -->

1. On the **[!UICONTROL Click Tracking URLs]**, **[!UICONTROL Impression Tracking URLs]**, and **[!UICONTROL Landing URLs]** tabs, do the following for each creative as needed:

   1. Expand the row for the creative.

   1. Do any of the following:
   
      * To add or edit a custom URL, enter the URL in the input field.
      
      * To add another custom URL, click **[!UICONTROL +]** and enter the URL in the input field.

      * To remove a custom URL, hold the cursor over the creative row and click ![Delete](/help/creative/assets/delete.png "Delete").

      You can include up to five custom impression-tracking URLs, five custom click-tracking URLs, and one custom landing page URL.

1. Click **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Assign creatives to an ad tag for experiences without targeting](experience-tag-assign-creatives.md)
>* [Customize the tracking URLs for an experience with decision tree targeting](experience-tracking-urls-targeting.md)
