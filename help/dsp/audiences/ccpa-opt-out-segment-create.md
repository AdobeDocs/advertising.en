---
title: Create and Implement a CCPA Opt-out-of-Sale Segment
description: Learn how to create and implement a segment to track users IDs from consumer opt-out-of-sale requests.
feature: CCPA, DSP Segments
exl-id: aebe0c5b-382f-4e4a-b145-c32f32d216ca
---
# Create and Implement a CCPA Opt-out-of-Sale Segment

You can create a segment to track users IDs from consumer opt-out-of-sale requests on your website, per the California Consumer Privacy Act (CCPA). Users remain in CCPA opt-out-of-sale segments indefinitely.

Once the segment pixel tag is implemented, Adobe Advertising will begin to collect a pool of IDs on the advertiser’s behalf.

>[!NOTE]
>
>* For information about how to communicate CCPA opt-out-of-sale requests to Adobe Advertising using the Adobe Experience Platform Privacy Service API, see [https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa-opt-out-of-sale.html).
>* To track users who visit webpages for purposes not related to tracking CCPA opt-out-of-sale events, as well as users exposed to ads from desktop, mobile, and CTV devices, create a [custom segment](/help/dsp/audiences/custom-segment-create.md).

1. Create the segment:

    1. In the main menu, click **Audiences > Segments**.

    1. Above the data table, click **[!UICONTROL Create]**.

    1. Enter a unique **[!UICONTROL Segment Name]**.

       Recommended segment name: “<*Your Advertiser Name*> – CCPA Opt Out of Sale” (such as "Acme - CCPA Opt Out of Sale")

    1. For the [!UICONTROL Segment Type], select **[!UICONTROL CCPA Opt-out of sale]**.

    1. Click **[!UICONTROL Save]**.

1. Copy and implement a pixel tag to track the segment:

    1. Return to **[!UICONTROL Audiences] > [!UICONTROL Segments]**.

    1. In the segment row, hold the cursor over the new segment and click **[!UICONTROL Get pixel]**.

    1. Copy the image pixel (beginning with `<img src="https://rtd-tm.everesttech.net"`) to collect user IDs of desktop and mobile visitors to a webpage.

    1. Provide the tag to the advertiser or website contact for deployment using the mechanism that the company uses to track CCPA opt-out-of-sale requests (such as using a Consent Management Platform).

        The advertiser's IT department or other group may need to schedule, or be informed about, the tag deployment.

        Once the pixel is implemented, Adobe Advertising will begin to collect a pool of IDs on the advertiser’s behalf.

        Although implementation choice and logic is up to the advertiser, here’s an example of how an advertiser could fire the pixel:

        1. A consumer lands on the advertiser's homepage.
        1. The consumer finds and clicks on the advertiser’s “CCPA opt out of sale” button.
        1. The consumer is presented with a list of service providers with which the advertiser works.
        1. The consumer checks the box to opt out of selling data to Adobe Advertising.

           This action triggers the pixel to fire and to collect the consumer’s cookie ID within the specified “[!UICONTROL CCPA Opt-out of sale]” segment.

>[!MORELIKETHIS]
>
>* [Adobe Advertising Support for the California Consumer Privacy Act: Consumer Opt-out Support](/help/privacy/ccpa-opt-out-of-sale.md)
>* [About [!UICONTROL CCPA Opt-out-of-Sale] Segments and Reports](ccpa-opt-out-about.md)
>* [Retrieve Consumer Opt-Out-of-Sale Reports](ccpa-opt-out-segment-report-retrieve.md)
>* [Create and Implement a Custom Segment](custom-segment-create.md)
>* [About Audience Management](audience-about.md)
