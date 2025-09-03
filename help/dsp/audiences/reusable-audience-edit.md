---
title: Edit a Reusable Audience
description: Learn how to edit a reusable audience.
feature: DSP Audiences
exl-id: 4de6b9a4-2907-474d-92bf-83686a1f0b31
---
# Edit a Reusable Audience

When you edit an audience that is used in any placements or other reusable audiences, the changes are immediately applied to those placements and audiences.<!-- verify -->

>[!NOTE]
>
>(Advertisers for whom DSP converts hashed email IDs to LiveRamp RampID segments) First-party RampID segments that aren't attached to an active, scheduled, or paused placement are paused. The segment is noted in the segment list as "Auto paused."

1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL All audiences]**.

1. Hold the cursor over the audience row and click **[!UICONTROL Edit]**.

1. Edit the audience settings in any of the following ways:

    >[!NOTE]
    >
    >If you edit the audience segment logic, detailed [audience size data](audience-about.md) is updated in the right panel.

   * (Optional) To edit the **[!UICONTROL Audience Name]** click ![Edit](/help/dsp/assets/edit.png) next to the audience name, enter a unique audience name, and then click **[!UICONTROL Apply]**.

   * (Optional) To manually edit the segment logic, using segments available on the [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments], and [!UICONTROL Saved Audiences] tabs](audience-settings.md), do the following.

     * To add a segment to an existing segment group:

      1. Click the segment group in the right panel.

      1. (Optional) Change the group logic to *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, or *[!UICONTROL Exclude All]*, as needed.

         *[!UICONTROL Exclude All]* isn't available to the first segment group. For an audience that includes only exclusions, build this audience as *[!UICONTROL Include Any]* and then, within a placement, select that audience from the Excluded Audiences menu.

      1. Locate the new segment in the left panel, and select the check box next to the segment name.

         The segment group is automatically updated with the new segment.

    * To add a new segment group:

      1. Click **[!UICONTROL + New Group]** in the right panel.

      1. (Optional) Change the logic between the previous group and the new group to *[!UICONTROL And]* or *[!UICONTROL Or]*, as needed.

      1. Locate the segments for the new group in the left panel, and select the check boxes next to the segment names.

      1. (Optional) Change the group logic to *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, or *[!UICONTROL Exclude All]*, as needed.

   * To use segment logic from an existing audience:

     1. Copy the segment logic from the existing audience in any of the following ways:

        * In the All Audiences view, hold the cursor over the audience row, and then click **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

        * In the settings for the existing audience, at the top of the segment logic panel, click **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

        * In a text editor, manually create the segment logic using alphanumeric segment IDs and [Boolean syntax](audience-segment-logic-syntax.md), and copy it to your clipboard.

     1. Click **[!UICONTROL paste in an audience rule to begin building]**, paste the existing segment logic into the input field, and then click **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >If the audience already includes any segment logic, pasting in new segment logic overwrites the existing logic.

1. Click **[!UICONTROL Save]**.

1. In the confirmation message, click **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [About Audience Management](audience-about.md)
>* [Create a Reusable Audience](reusable-audience-create.md)
>* [Duplicate a Reusable Audience](reusable-audience-duplicate.md)
>* [View Details About a Reusable Audience](reusable-audience-view-details.md)
>* [Share a Reusable Audience](reusable-audience-share.md)
>* [Export a Reusable Audience](reusable-audience-export.md)
>* [Copy the Segment Key for a Reusable Audience to the Clipboard](reusable-audience-clipboard.md)
>* [Delete a Reusable Audience](reusable-audience-delete.md)
>* [Audience Settings](audience-settings.md)
>* [Syntax for Audience Segment Logic](audience-segment-logic-syntax.md)
>* [Available Third-party Data Providers](third-party-data-providers.md)
