---
title: View tracking pixels for a segment
description: Learn how to view the tracking pixels for a custom or CCPA opt-out of sale segment.
feature: DSP Segments
exl-id: 3b67ab72-d7bb-45a0-b5ba-e4b811b7d2b3
TQID: https://experienceleague.adobe.com/jWneyyCriQcP299jQg-6Ggue0AObOfyehJwPvemYSfY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
    internal-label: DSP Segments
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# View tracking pixels for a segment

1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

1. Hold the cursor over the segment row and click **[!UICONTROL Get Pixel]**.

   * The page view tracking tag, which tracks desktop and mobile visitors to a webpage, is labeled "[!UICONTROL Desktop or mobile websites]." For segments that track [!DNL ID5] IDs, replace `ID5_PARTNER_ID` in the copied tag with the partner ID that [!DNL ID5] assigned to your organization when it signed an agreement with [!DNL ID5]. If you don't know your partner ID, contact your Adobe Account Team.

      Add the tag to the pages whose views you want to track.

   * (Custom segments only) The impression tracking tag, which tracks users exposed to an ad unit on desktop, mobile, or CTV devices, is labeled "[!UICONTROL Desktop or mobile ads]." Add the tag to the ads whose views you want to track; you can optionally add the tag to a placement to attach it by default to all ads associated with the placement.

Once a tracking tag is implemented, you can use the segment in the audience targets or exclusions for any placement.

>[!MORELIKETHIS]
>
>* [About audience management](audience-about.md)
>* [Create a custom segment](custom-segment-create.md)
>* [Edit segment information](segment-edit.md)
>* [Delete a segment](segment-delete.md)
>* [Share or stop sharing a segment](segment-share.md)
