---
title: View Tracking Pixels for a Segment
description: Learn how to view the tracking pixels for a custom or CCPA opt-out of sale segment.
feature: DSP Segments
exl-id: 3b67ab72-d7bb-45a0-b5ba-e4b811b7d2b3
---
# View Tracking Pixels for a Segment

1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

1. Hold the cursor over the segment row and click **[!UICONTROL Get Pixel]**.

   * The page view tracking tag, which tracks desktop and mobile visitors to a webpage, is labeled "[!UICONTROL Desktop or mobile websites]." For segments that track [!DNL ID5] IDs, replace `ID5_PARTNER_ID` in the copied tag with the partner ID that [!DNL ID5] assigned to your organization when it signed an agreement with [!DNL ID5]. If you don't know your partner ID, contact your Adobe Account Team.

      Add the tag to the pages whose views you want to track.

   * (Custom segments only) The impression tracking tag, which tracks users exposed to an ad unit on desktop, mobile, or CTV devices, is labeled "[!UICONTROL Desktop or mobile ads]." Add the tag to the ads whose views you want to track; you can optionally add the tag to a placement to attach it by default to all ads associated with the placement.

Once a tracking tag is implemented, you can use the segment in the audience targets or exclusions for any placement.

>[!MORELIKETHIS]
>
>* [About Audience Management](audience-about.md)
>* [Create a Custom Segment](custom-segment-create.md)
>* [Edit Segment Information](segment-edit.md)
>* [Delete a Segment](segment-delete.md)
>* [Share or Stop Sharing a Segment](segment-share.md)
