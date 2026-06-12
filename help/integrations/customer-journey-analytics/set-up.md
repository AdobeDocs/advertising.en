---
title: Set up data collection, data transfer, and reporting
description: Learn how to set up data collection, data transfer, and reporting.
feature: Integration with Adobe Customer Journey Analytics
exl-id: a955e2b0-ea1b-4b5c-937b-f8c66603cd36
TQID: https://experienceleague.adobe.com/u6xL6FuW-TwqAkse3VTS3zcyt-10Cv-ADTZLJTiWWT8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
---
# Set up data collection, data transfer, and reporting

*Advertisers with Advertising DSP and [!DNL Advertising Search, Social, & Commerce]*

*Advertisers without [!DNL Analytics for Advertising] only*

The following tasks are required to natively exchange data between Adobe Advertising and Customer Journey Analytics using the [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html). Data transfer and attribution begin after the launch; no historical data is included.

1. (Your organization's web analyst; optional) [Collect historical data for AMO IDs and EF IDs](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}.

   This step is applicable only for advertisers with [!DNL Analytics for Advertising].

2. (Your organization's site administrator for Adobe Experience Platform) [Set up data collection in Experience Platform and implement conversion tracking tags](#data-collection).

3. (Your organization's site administrator for Customer Journey Analytics) [Create a connection to your Experience Platform datasets in Customer Journey Analytics](#dataset-connection).

4. (Your organization's web analyst) [Set up data views in Customer Journey Analytics](#cja-data-views).

5. (Your organization's web analyst) [Set up reports and visualizations in Customer Journey Analytics Workspace](#cja-reports).

The following sections include the detailed procedures, which include the tasks and settings required for the integration but do not explain all features available within the workflows. See the linked resources for full information.

## Set up data collection in Adobe Experience Platform and on your website {#data-collection}

The following tasks are required to set up data collection in Experience Platform and implement conversion tracking tags. Your organization's site administrator for Experience Platform can perform these tasks, but your organization's IT department may need to help with deploying tracking tags.

### Collect and send data from Adobe Advertising to Experience Platform Edge Network as a dataset

This procedure includes creating a schema. You can optionally edit an existing schema instead; in that case, you don't need to create a dataset or datastream.

1. In Experience Platform, [define a manual schema](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) for the data you want to collect using the Experience Data Model (XDM).

   * In the [!UICONTROL Schema Details], select **[!UICONTROL Experience Event]** as the base class for the schema to capture site events. Name your schema and click **[!UICONTROL Finish]**.
   
   * In the left panel, add the field group [Adobe Advertising Cloud ExperienceEvent Full Extension](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension) to add fields specific to Adobe Advertising. At a minimum, include the conversionDetails object with the `trackingCode` and `trackingIdentities` properties, which include the [AMO ID and EF ID](ids.md). The other fields are optional.
   
   * (Optional) Add additional field groups as needed to connect additional data fields to Adobe Advertising data.

   **Note:** You can create multiple schemas, but you can use only one schema per dataset and per datastream, which you'll create in the following steps.

1. [Create a dataset](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create) based on the schema to store and manage the collection of event data. This will be your *event dataset*. If you're editing an existing schema with a dataset, then you can skip this step.

   * Choose the option to **[!UICONTROL Create dataset from schema]** and select your schema.
   
     Based on your event dataset, Adobe Advertising creates two additional datasets: 1\) a *summary dataset* with the related summary data (such as clicks and impressions) and 2\) a *lookup dataset* (with dimensions/classification metadata, such as Adobe Advertising campaign name). Data for the datasets is populated in Experience Platform daily.

   >[!TIP]
   >
   >Create a dummy event dataset first to validate data flow before using a production dataset.
 
1. [Create a datastream](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) to specify where to send data from your website or app and how to handle the incoming data.

   * For the [!UICONTROL Mapping schema] setting, select your schema.
   
   * Add and enable the services `Adobe Advertising` and `Adobe Experience Platform` to the datastream.
   
     The [!UICONTROL Adobe Advertising] service enables ad exposures to be associated with the payload, and the [!UICONTROL Adobe Experience Platform] enables the Edge Network to store the dataset and to route it to Adobe Advertising.

   * For the [!UICONTROL Event dataset] setting, select your event dataset.
   
     Each datastream can insert data into only one dataset.

### Send your organization's website data to your Experience Platform datastream

Use the Adobe Experience Platform Web SDK extension in Adobe Tags to send your organization's website data to your Experience Platform datastream.

>[!NOTE]
>
>Only Adobe Tags are supported. Support isn't available for standalone Experience Platform Web SDK (`alloy.js`) or third-party tag managers.

1. Use Experience Platform [tags](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) (formerly known as [!DNL Launch]) to generate a JavaScript tag to send your organization's website data to the datastream.
   
   * Create a tag property, which is the container for the tag configuration.
   
   * For your property, [install the extension "Adobe Experience Platform Web SDK"](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) from the extensions catalog.
   
     This extension sends data from your web properties to Adobe CX Enterprise via the Experience Platform Edge Network.
     
     Don't use the Adobe Advertising extension.

   * Create a [custom Web SDK build](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build):
   
     * In the [!UICONTROL Custom build components] section, enable the **Advertising** component.
     
       This component includes all JavaScript code needed for Adobe Advertising in the tag and is required for both Advertising DSP and Advertising Search, Social, & Commerce customers. The component also adds an "Advertising" setting in tag rules (which are optional) to define how advertising data is used for attribution measurement.
       
       You can optionally enable additional components as needed.
       
     * In the [!UICONTROL SDK Instances] section:
     
       * In the [!UICONTROL Datastreams] settings, select the datastream to use for each of your web environments (production, staging, development).
       
       * (Organizations with Adobe Advertising DSP only) In the [[!UICONTROL Adobe Advertising] settings](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising), enable **[!UICONTROL Adobe Advertising DSP]** to permit view-through tracking and specify the advertisers for which to enable view-through tracking. You can optionally collect IDs from universal IDs by adding your organization's ID5 partner ID and/or the path to your organization's [!DNL LiveRamp RampID] JavaScript code (ats.js).

         If your advertisers aren't listed, then enter the advertiser ID for each advertiser. If needed, ask your Adobe Account Team for the IDs.

       * Save the build.
        
   * (Optional) [Create rules](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) as needed to determine when Web SDK should send data to the Edge Network.
   
     * For `[sendEvent](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/actions/send-event)` actions, use the [[!UICONTROL Advertising] setting](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising) to define how advertising data is used for attribution measurement. This setting is helpful when the rule includes a sequence of multiple actions and is available only when you've selected the "[!UICONTROL Advertising]" component for the custom build component.
   
   * Create [data elements](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) as needed to map variables on your website to the structure of the XDM schema you created previously.

1. [Publish the tag](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) to a test environment in which you can iterate on the development of tags.
      
1. [Check the activity for each of your three datasets](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets) to validate delivery.
 
1. [Publish the tag to your live production environment](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

   Your organization's IT department or other group may need to schedule, or be informed about, the tag deployment.

## Create a connection to your Experience Platform datasets in Customer Journey Analytics {#dataset-connection}

Follow these steps to pull Adobe Advertising data from your Experience Platform datasets into Customer Journey Analytics. Your organization's site administrator for Customer Journey Analytics can perform these tasks.

You can also optionally edit an existing connection with the same information.

1. In Customer Journey Analytics, [create or edit a connection](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) that includes your Experience Platform datasets and schema.

   <!-- **Note:** You must send data for all DSP and Search, Social, & Commerce accounts to a single Experience Platform instance and sandbox.  -->

   * Confirm that the correct sandbox is selected.

   * Calculate the average number of daily events (under 1 million for most organizations).

   * Add your Experience Platform event metrics dataset (type: `Event`), your<!-- Adobe Advertising --> event summary metrics dataset  (type: `Event`), and your<!-- Adobe Advertising --> dimensions (classifications/metadata) dataset (type: `Lookup`).

     Your team created the event dataset, and Adobe Advertising created the summary and dimensions datasets based on your event dataset.
     
     You can optionally include additional datasets as needed.

   * Configure the dataset settings:

     * For the [!UICONTROL Event Dataset] settings:

       * **[!UICONTROL Person ID]:** `Identity Map`
       
       * **[!UICONTROL Use primary identity namespace]:** Enable setting

       * **[!UICONTROL Data Source Type]:** `Web Data > Others` <!-- I don't see "Others" in the screen shot example -->
  
       * **[!UICONTROL Import all new data]:** Enable the setting
   
     * For the [!UICONTROL Lookup Dataset] settings, map the dimensions dataset to the events dataset:

       * **[!UICONTROL Key]** (the field to use as the key for the dimensions dataset): `Tracking Code` (which is same as the `trackingCode` field in the schema).
      
       * **[!UICONTROL Matching key]** (the field to use as the matching key for the events dataset): `Tracking Code (Event datasets)`.<!-- verify this Later, you'll also map the events dataset to the summary dataset when you set up your data view(#cja-data-views).  -->
  
       * **[!UICONTROL Import all new data]:** Enable the setting

     * For the [!UICONTROL Metrics Dataset] settings:

       * **[!UICONTROL Person ID]:** `Identity Map`
       
       * **[!UICONTROL Timestamp]:** Confirm the value
  
       * **[!UICONTROL Import all new data]:** Enable the setting

1. Within three hours, verify that the data is available in Customer Journey Analytics.

   1. In Customer Journey Analytics, go to **[!UICONTROL Connections]** and select your connection.

   2. In the list of data sets displayed, verify that the "[!UICONTROL Number of Records]" report shows that data was added.

## Set up data views in Customer Journey Analytics {#cja-data-views}

In Customer Journey Analytics, create one or more data views to define the metrics and dimensions for reporting. A web analyst can perform these tasks.

1. In Customer Journey Analytics, [create a data view](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview).

1. Configure the view to include the following information.

   * If you have an Adobe Analytics account, use the [!UICONTROL Time Zone] for your [!DNL Analytics] account in the [!UICONTROL Calendar] section of the [!UICONTROL Configure] tab.
   
   * On the [!UICONTROL Components] tab:
   
     * Add your lookup dataset (with dimensions/classification data), event dataset (with your event-level data), and summary dataset (with your other metrics, such as clicks).
     
     * Choose metrics from your event dataset and your lookup dataset to include in the data view.

     * Search for "[!UICONTROL Tracking Code]" (which is part of the event dataset with schema path `_experience.adcloud.conversionDetails.trackingCode`). <!-- and do what with it? Add it? Or is that what you --> Set **[!UICONTROL Persistence]** to *[!UICONTROL Most Recent]*.

<!--

Seems to not be necessary now:


       You already joined these two datasets in the connection that you created in the [last procedure](#dataset-connection).
     
     *  Join the events dataset to the summary dataset, which isn't yet joined to anything:
     
       * For each dimension with summary data that you want to be available in Customer Journey Analytics, [create a derived field](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/derived-fields).

         For example, to view summary data for campaigns, create a derived field for the dimension `Adobe Advertising Campaign`.
         
         You'll link the two datasets using the matching key `trackingCode` (which is the schema field for the Adobe Advertising ID).
       
         * In the [!UICONTROL Lookup] section of the derived rule builder:
         
           * For the **[!UICONTROL Value]** field, select "[!UICONTROL Tracking Code]" from the metrics summary dataset.

           * For the **[!UICONTROL Lookup dataset]** field, select the dimensions dataset (such as "Adobe Advertising Classification").

           * For the **[!UICONTROL Matching Key]** field, select "[!UICONTROL Tracking Code]" from the classification dataset.

           * For the **[!UICONTROL Values to return]** field, select the dimension (such as "[!UICONTROL Adobe Advertising Campaign]")" from the classification dataset.
         
         The derived field name is appended with "(DF)", such as `Adobe Advertising Campaign(DF)`. 
         
       * For each derived field:
       
         * In the [!UICONTROL Included components] section, add the derived field.
         
           Two names are now listed for the same dimension (for example, "Adobe Advertising Campaign(DF)" (the derived field) and "Adobe Advertising Campaign" (the field in the summary dataset)).

         * Select the dimension in the summary dataset (such as "Adobe Advertising Campaign") and edit the settings for the dataset.

           The settings open on the right.

           * In the the Summary Data Group section, select the option to **[!UICONTROL Create grouping]**.

           * For the **[!UICONTROL Dimension]** field, select the derived field (which is appended with "(DF)," such as "Adobe Advertising Campaign(DF)").
         
           * Select the option to **[!UICONTROL Hide in reporting]**, which hides the derived field name in Workspace.

-->

## Set up reports and visualizations in Customer Journey Analytics Workspace {#cja-reports}

In Customer Journey Analytics Workspace, follow these steps to configure reports and visualizations. A web analyst can perform these tasks.

1. [Create a project](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) in Workspace to build reports and visualizations based on the dimensions and metrics configured within the data view.

  You can classify both summary metrics and event data using the same dimension in one freeform table.

1. (If you have data from [!DNL Google Ads] or [!DNL Microsoft Advertising]) Create a report of publisher-tracked conversions using fields for ad network-specific metrics, which are grouped as `googleConversions` and `microsoftConversions`.

>[!TIP]
>
>Summary events typically add a small amount of extra data to reports, such as a few extra events, one extra session per day, or one extra person per report. These additions are negligible compared to standard web events. However, you can filter out this additional summary event data by excluding data for the dummy Person ID `00000000-0000-0000-0000-000000000000`.
>![Example of excluding data using a Person ID](/help/integrations/assets/cja-report-with-person-id.png "Example of excluding data using a Person ID")

![How your datasets may appear in Customer Journey Analytics](/help/integrations/assets/cja-report-example.png "How your datasets may appear in Customer Journey Analytics")

>[!MORELIKETHIS]
>
>* [Overview](overview.md)
>* [Prerequisites](prerequisites.md)
>* [Adobe Advertising IDs used by [!DNL Customer Journey Analytics]](ids.md)
>* [Adobe Advertising metrics and dimensions in Customer Journey Analytics](advertising-data-in-cja.md)
>* [Collect historical data for AMO IDs and EF IDs for use in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Customer Journey Analytics Guide](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [User guide for Adobe Analytics users](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
