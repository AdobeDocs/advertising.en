---
title: Convert User IDs from [!DNL Tealium] to Universal IDs
description: Learn how to enable DSP to ingest your [!DNL Tealium] first-party segments.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
---
# Convert User IDs from [!DNL Tealium] to Universal IDs

*Beta feature*

Use the DSP integration with the [!DNL Tealium] customer data platform to convert your organization's first-party hashed email addresses to universal IDs for targeted advertising. The process uses the [!DNL Amazon Web Services] (AWS) firehose connector. Follow these steps to share data from Tealium with DSP:

1. (To convert email addresses to [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Set up tracking to enable [!DNL Analytics] measurement](#analytics-tracking).

1. [Create an audience source in DSP](#source-create).

1. [Prepare and share segment-mapping data](#map-data). 

1. [Create connectors in [!DNL Tealium] to share segment data](#tealium-connector).

1. [Duplicate the existing connector in [!DNL Tealium] to continue to share segments](#duplicate-connector).

1. [Compare the number of universal IDs with the number of hashed email addresses](#compare-id-count).

## Step 1: Set up tracking for [!DNL Analytics] measurement {#analytics-tracking}

*Advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

To convert email addresses to [!DNL RampIDs] or [!DNL ID5] IDs, you must do the following:

1. (If you haven't already done so) Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
1. Register with the universal ID partner and deploy universal ID-specific code on your webpages to match conversions from the IDs on desktop and mobile web browsers (but not mobile apps) to view-throughs:
   
   * **For [!DNL RampIDs]:** You must deploy an additional JavaScript tag on your webpages to match conversions from the IDs on desktop and mobile web browsers (but not mobile apps) to view-throughs. Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag from [!DNL LiveRamp] Authentication Traffic Solutions. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

## Step 2: Create an audience source in DSP {#source-create}

1. [Create an audience source](source-manage.md) to import audiences to your DSP account or an advertiser account. You can choose to convert your user identifiers to any of the [available universal ID formats](source-about.md).

   The source settings will include an auto-generated source key, which you'll use to prepare the segment-mapping data.

1. After you create the audience source, share the source code key with the [!DNL Tealium] user.

## Step 3: Prepare and share segment-mapping data {#map-data}

The advertiser must prepare and share segment-mapping data.

1. The advertiser must prepare the data within [!DNL Tealium]:
   
   1. Hash the email IDs for the advertiser's audience using the SHA-256 algorithm.

   1. Map the column containing hashed email IDs to the attribute of the type of Visitor ID.

   1. Create the audience with the `Tealium_visitor_id` attribute. Apply the right enrichment to trigger the audience. See the [[!DNL Tealium] documentation on visitor ID attributes](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).
   
1. The advertiser must give segment-mapping data to the Adobe Account Team to create the segments in DSP. Use the following column names and values in a comma-separated values file:

   * **External Segment Key:** The external segment key, which you'll later specify in the action settings for the connector in [!DNL Tealium]. The recommended naming convention is "`<DSP source key>_<Tealium segment name>`," such as "57bf424dc10_coffee-drinkers." For the DSP source key, use the [!UICONTROL Source Key] from the DSP audience source settings.
   
   * **Segment Name:** The segment name.
   
   * **Segment Description:** The purpose or rule of the segment, or both.
   
   * **Parent ID:** Keep blank
   
   * **Video CPM:** 0
   
   * **Display CPM:** 0
   
   * **Segment Window:** The segment time-to-live.

## Step 4: Create connectors in [!DNL Tealium] to share segment data {#tealium-connector}

For each segment that you want to share, create a separate connector for each action that triggers data changes. For example, to share two segments that each have two triggers, create four connectors.

1. The Adobe Account Team provides the advertiser with AWS firehose connector credentials.

1. In [!DNL Tealium], [add a connector](https://docs.tealium.com/server-side/connectors/add/), using the following options:

   1. Select the [!DNL AWS Firehose] connector.

   1. In the source settings:
   
      1. Select the audience segment to share.

      1. Set up a trigger:

         * For the first connector for the segment, select the trigger `Joined Audience`. This ensures that data is shared with DSP whenever a user joins a segment.

         * For the second connector for the segment, select the trigger `Left Audience`. This connector is used to handle all opt-outs and users who leave the segment in DSP.

   1. In the configuration settings, specify the AWS firehose connector. If you haven't yet added the firehose connector for DSP, then add a firehose connector using the following information:

      * **Name:** The name of the connector.
      
      * **Access Key:** The access key provided by the Adobe Account Team.
      
      * **Secret Key:** The secret key provided by the Adobe Account Team.
      
      * **Region:** US East North Virginia (us-east-1)
     
   1. In the action settings, do the following:
   
      1. Create a "Send Customer Data to Delivery Stream (Advanced)" action to add data to the segment, using the following information:
      
         * **Action Name:** The name of the action.
         
         * **Action Type:** Send Customer Data to Delivery Stream (Advanced)
         
         * **Delivery Stream:** Tealium_CDP_Connector
         
         * **Message Data:**  Do the following:
         
           1. Choose one attribute for the segment:
           
              * For the Hashed_Email attribute, name the custom message `hashed_email`.
              
              * For the Cookies attribute, name the custom message `cookies`.
                
           1. In the option to create a custom field, in the [!DNL Source Key] field, enter the [!UICONTROL External Segment Key] that was included in the [segment-mapping data](#map-data) in the previous procedure.
           
              DSP will use this key to populate your segment.
                
           1. (Recommended) Create an update action to keep the segment fresh.
   
## Step 5: Duplicate the existing connector in [!DNL Tealium] to continue to share segments {#duplicate-connector}

You can have only one connector per segment and one segment per connector.

1. In [!DNL Tealium], duplicate the segment for which you want to create another segment, and rename the new segment.

1. In [!DNL Tealium], duplicate [the connector you created](#tealium-connector) in the previous procedure, and rename the new connector from "`<original name>-copy`" to the new segment name.

## Step 6: Compare the number of universal IDs with the number of hashed email addresses {#compare-id-count}

The segments should be available in DSP within 24 hours. After DSP receives the segment data, the audience count should be visible within nine (9) hours.

Verify in your audience library (which is available when you create or edit an audience from [!UICONTROL Audiences] > [!UICONTROL All Audiences] or within placement settings) that the segment is populating, and compare the number of universal IDs with the number of original hashed email addresses. For information about acceptable ID translation rates and why the segment counts can vary, see "[Data Variances Between Email IDs and Universal IDs](#universal-ids-data-variances)."

Segments are refreshed every 24 hours. However, inclusion in a segment expires after 30 days by default or after a customer-specified expiration period. Refresh your segments by re-pushing them from [!DNL Tealium] prior to the expiration. To request a custom segment expiration, contact your Adobe Account Team.

## Troubleshooting

To troubleshoot translation rate and user count issues, see "[Support for Activating Universal IDs](/help/dsp/audiences/universal-ids.md)."

To troubleshooting issues with the conversion procedure, contact your Adobe Account Team or `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [About First-Party Audience Sources](/help/dsp/audiences/sources/source-about.md)
>* [Manage Audience Sources to Activate Universal ID Audiences](source-manage.md)
>* [Support for Activating Universal IDs](/help/dsp/audiences/universal-ids.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
