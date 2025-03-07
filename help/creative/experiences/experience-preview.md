---
title: Preview an experience
description: Learn how to preview the creatives in an ad experience.
feature: Creative Experiences
exl-id: 2ac8f580-7d3d-4de6-ba14-5d72b30188d7
---
# Preview an experience

*Closed beta*

You can preview the creatives with a specific ad size that target viewers will see for an experience, including all hyperlinks. For experiences with decision tree targeting, you can preview a single creative, the creatives for a particular branch (target type), or all creatives in the experience. For experiences without decision tree targeting, you can preview a single creative. <!-- verify -->

* When you preview all creatives for the experience or a particular branch, all applicable creatives are shown.

* When you preview a single creative and multiple creatives fit the criteria, the creative you see each time you refresh the preview is based on the ad rotation settings for the experience:

  * For algorithmic ad rotation, the creative is selected based on the optimization goal.

  * For weighted ad rotation, the creative is selected based on the specified weights (such as an 80% chance that Creative A is shown and a 20% chance that Creative B is shown) each time.

  * For scheduled ad rotation, the first creative in the schedule is shown. You can keep refreshing the preview to continue through the sequence.<!-- Refresh isn't there as of 2/3 -->

## Preview creatives in an experience with decision tree targeting

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific experiences.

1. Do one of the following:

   * In card view, click **[!UICONTROL ...]** next to the experience name, and then click **[!UICONTROL Preview]**.
   
   * In table view, hold the cursor over the row, click **[!UICONTROL More]**, and then click **[!UICONTROL Preview]**.

1. Select which creatives to preview:

   * To preview a single creative:
   
      1. Click **[!UICONTROL Creative]**.
      
      1. Select the ad size.

      1. In the [!UICONTROL Decision Tree Targeting] section, select the creative target.

   * To preview the creatives for a particular branch:
   
     1. Click **[!UICONTROL Particular branch]**.
     
     1. Select the ad size.
  
     <!-- I don't see this as of 2/3:
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

     1. Select the creative target.

   * To preview all creatives in the experience, click **[!UICONTROL Entire Tree]**.

     <!-- I don't see this as of 2/3:
     1. Click **[!UICONTROL Entire Tree]**.
     1. Select the ad size.
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

1. (Optional) To include the name of the creative, the creative type and size, the landing page URL or click URLs, and flexible attributes below each creative, select **[!UICONTROL Display Creative Metadata]**.

1. Click **[!UICONTROL Preview]**.

1. (Preview by creative only; optional) In the toolbar, click **[!UICONTROL Refresh]** to preview any additional creatives that may be shown, according to the ad rotation settings.<!-- I don't see this as of 2/3 -->

1. (Optional) To copy a demo URL of the experience to share with other people without a login to [!DNL Creative]:

   1. In the upper right of the preview, click ![Share](/help/creative/assets/share.png "Share").
   
   1. In the [!UICONTROL Share Demo URL] dialog, click **[!UICONTROL Copy]** to copy the URL to your clipboard so that you can share it with someone else.


## Preview creatives in an experience without decision tree targeting

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific experiences.

1. Do one of the following:

   * In card view, click **[!UICONTROL ...]** next to the experience name, and then click **[!UICONTROL Preview]**.
   
   * In table view, hold the cursor over the row, click **[!UICONTROL More]**, and then click **[!UICONTROL Preview]**.

1. (Optional) Limit the list of creatives by selecting a specific creative size.

   By default, creatives of all sizes are listed.

1. Click the name of an ad tag to expand the row and preview the creative.

1. (Optional) To copy a demo URL of the experience to share with other people without a login to [!DNL Creative]:

   1. In the upper right of the preview, click ![Share](/help/creative/assets/share.png "Share").
   
   1. In the [!UICONTROL Share Demo URL] dialog, click **[!UICONTROL Copy]** to copy the URL to your clipboard so that you can share it with someone else.

>[!MORELIKETHIS]
>
>* [Create an experience with decision tree targeting](experience-create-targeting.md)
>* [Create an experience without decision tree targeting](/help/creative/experiences/experience-create-no-targeting.md)
