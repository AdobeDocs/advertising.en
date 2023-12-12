---
title: "Workflow for Using the DSP Integration with [!DNL Tealium]"
description: "Learn how to enable DSP to ingest your [!DNL Tealium] first-party segments."
feature: DSP Audiences
---
# Workflow for Using the DSP Integration with [!DNL Tealium]

<!-- for What's New:

<I didn't see "Amazon Kinesis" anywhere in product requirements -- just AWS (parent) generically. Also, verify if must use RampIDs in particular or if there's a choice in the Audience > Source settings

| <release date> | [!UICONTROL Audiences] | Advertisers can now share their first-party data from the [!DNL Tealium] customer data platform (CDP) with DSP using the [!DNL Amazon Kinesis] streaming data platform. You can then target your DSP placements to the segments using [!DNL RampIDs]. Within placement settings for [!UICONTROL Audience Targeting], the shared segments are available in the [!UICONTROL First Party Segments] list. | Contact your Adobe Account Team. |

--><!-- Look up Kinesis -->

You can share your organization's first-party data from the [!DNL Tealium] customer data platform using the [!DNL Amazon Web Services] (AWS) firehose connector. There are four steps to share data from Tealium with DSP:

1. [Create an audience source in DSP](#source-create). 

1. [Prepare and share segment-mapping data](#map-data). 

1. [Create connectors in [!DNL Tealium] to share segment data](#tealium-connector).

1. [Duplicate the existing connector in [!DNL Tealium] to continue to share segments](#duplicate-connector).

## Step 1: Create an audience source in DSP {#source-create}

* [Create an audience source](source-create.md) to import audiences to your DSP account or an advertiser account, and share the source code key with the [!DNL Tealium] user.

## Step 2: Prepare and share segment-mapping data {#map-data}

1. The advertiser must prepare and share segment-mapping data:

   1. The advertiser must prepare the data within [!DNL Tealium]:
   
      1. The email IDs for the advertiser's audience must be hashed using the SHA-256 algorithm.

      1. The column containing hashed email IDs must be mapped to the attribute of the type of Visitor ID.

      1. The audience must be created with the `Tealium_visitor_id` attribute. The right enrichment must be applied to trigger the audience. See the [[!DNL Tealium] documentation on visitor ID attributes](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).
   
   1. The advertiser must give segment-mapping data to the Adobe Account Team to create the segments in DSP. Use the following column names and values in a comma-separated values file:<!-- are a couple of fields missing? -->

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
                
           1. In the option to create a custom field, in the Source Key field, enter the External Segment Key that was included in the segment-mapping data in [Step 2](#map-data). <!-- Is the field named "external_segment_key"?  If not, what is the field name? -->
           
              DSP will use this key to populate your segment.
                
           1. (Recommended) Create an update action to keep the segment fresh. <!-- This was listed under triggers, but I don't see a setting in the Source UI, so is it in the Actions UI? -->
   
## Step 4: Duplicate the existing connector in [!DNL Tealium] to continue to share segments {#duplicate-connector}

<!-- why?  because can have only one segment per connector and need multiple connectors -->

1. In [!DNL Tealium], duplicate the connector you created in Step 3.

   The duplicated connector is named "`<original name>-copy`."

1. Rename the new connector to the new segment name.

>[!MORELIKETHIS]
>
>* [About Activating Authenticated Segments from Audience Sources](/help/dsp/audiences/sources/source-about.md)
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [Workflow for Using the DSP Integration with [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)

<!--
>* [Workflow for Using the DSP Integration with [!DNL ActionIQ]](/help/dsp/audiences/sources/source-actioniq.md)
-->

<!-- relevant? You can optionally use Ramp IDs, so maybe this is relevant/necessary for some use cases?
>* [Activate Authenticated Segments from Durable ID Partners](source-durable-id.md)
-->
