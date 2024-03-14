---
title: Workflow for Using the DSP Integration with [!DNL Tealium]
description: Learn how to enable DSP to ingest your [!DNL Tealium] first-party segments.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
---
# Workflow for Using the DSP Integration with [!DNL Tealium]

Use the DSP integration with the [!DNL Tealium] customer data platform to convert your organization's first-party hashed email IDs to universal IDs for targeted advertising. The process uses the [!DNL Amazon Web Services] (AWS) firehose connector. There are four steps to share data from Tealium with DSP:

1. [Create an audience source in DSP](#source-create).

1. [Prepare and share segment-mapping data](#map-data). 

1. [Create connectors in [!DNL Tealium] to share segment data](#tealium-connector).

1. [Duplicate the existing connector in [!DNL Tealium] to continue to share segments](#duplicate-connector).

The segments should be available in DSP within 24 hours.

## Step 1: Create an audience source in DSP {#source-create}

1. [Create an audience source](source-create.md) to import audiences to your DSP account or an advertiser account, specifying the [universal ID formats](source-about.md) to which you want to convert your user identifiers.

1. After you create the audience source, share the source code key with the [!DNL Tealium] user.

## Step 2: Prepare and share segment-mapping data {#map-data}

1. The advertiser must prepare and share segment-mapping data:

   1. The advertiser must prepare the data within [!DNL Tealium]:
   
      1. The email IDs for the advertiser's audience must be hashed using the SHA-256 algorithm.

      1. The column containing hashed email IDs must be mapped to the attribute of the type of Visitor ID.

      1. The audience must be created with the `Tealium_visitor_id` attribute. The right enrichment must be applied to trigger the audience. See the [[!DNL Tealium] documentation on visitor ID attributes](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).
   
   1. The advertiser must give segment-mapping data to the Adobe Account Team to create the segments in DSP. Use the following column names and values in a comma-separated values file:

      * **External Segment Key:** The external segment key, which you'll later specify in the action settings for the connector in [!DNL Tealium]. The recommended naming convention is "`<DSP source key>_<Tealium segment name>`," such as "57bf424dc10_coffee-drinkers."
      
      * **Segment Name:** The segment name.
      
      * **Segment Description:** The purpose or rule of the segment, or both.
      
      * **Parent ID:** Keep blank
      
      * **Video CPM:** 0

      * **Display CPM:** 0

      * **Segment Window:** The segment time-to-live.

## Step 3: Create connectors in [!DNL Tealium] to share segment data {#tealium-connector}

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
                
           1. In the option to create a custom field, in the [!DNL Source Key] field, enter the [!UICONTROL External Segment Key] that was included in the segment-mapping data in [Step 2](#map-data).
           
              DSP will use this key to populate your segment.
                
           1. (Recommended) Create an update action to keep the segment fresh.
   
## Step 4: Duplicate the existing connector in [!DNL Tealium] to continue to share segments {#duplicate-connector}

You can have only one connector per segment and one segment per connector.

1. In [!DNL Tealium], duplicate the segment for which you want to create another segment, and rename the new segment.

1. In [!DNL Tealium], duplicate the connector you created in [Step 3](#tealium-connector), and rename the new connector from "`<original name>-copy`" to the new segment name.

>[!MORELIKETHIS]
>
>* [About Activating Authenticated Segments from Audience Sources](/help/dsp/audiences/sources/source-about.md)
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [Workflow for Using the DSP Integration with [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
