---
title: About experiences in Advertising Creative
description: Learn how to configure personalized ad experiences and optimize ad elements based on performance.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
---
# About experiences in Advertising Creative 2.0

*Closed beta*

[!DNL Advertising Creative 2.0] provides two different ad experience structures for the ads in a creative library<!-- can use a single library only -->:

* **Experiences with decision tree targeting:** [!DNL Creative] allows you to configure personalized ad experiences throughout the customer journey using a decision tree model. You can customize all ad elements &mdash; images, headlines, offers, and landing pages &mdash; based on the target audience.

  For example, you could specify the same creative bundle for people in Chicago and New York City who are in a specific Adobe Analytics audience segment but send people in Chicago to different landing pages than New Yorkers. You could also specify a different bundle for people in the segment who live anywhere except Chicago and New York City, and a third bundle for other people who aren't in the segment.

  Targeting options include:

    * Your first-party audience segments from Adobe Audience Manager, Adobe Analytics, and Advertising Cloud DSP
    
    * Specific geographical locations, including countries, states, DMAs within the United States, cities, and zip codes
    
    * Viewers for which specific key-value pairs (data pass targets) are passed from the DSP, publisher, or partner
    
    * [!DNL Creative] retargeting pixels and specified attribute values
    
    * Specific device types, operating systems, and browsers

  Once you create a target audience branch in the decision tree, you can pair the target audience with potential creatives by assigning creative bundles to the branch. For each experience, you can customize optimization and scheduling for the creative bundles and change the default landing pages and tracking URLs<!-- later: and any flexible attributes --> for individual creatives in each bundle.

* **Experiences without decision tree targeting:** [!DNL Creative] optimizes the ad elements for the ad experience without narrowing the audience. For each experience, you specify start and end dates and some default settings, but much of the workflow isn't directly within the experience. Instead of adding creatives directly to the experience, you use [!UICONTROL Tag Manager] to create an ad tag for each ad size for the experience and then add creatives to it, configure creative optimization and scheduling, and customize the landing pages and tracking URLs<!-- later: and any flexible attributes -->.

## Ad optimization

<!-- MORE -->
[!DNL Creative] optimizes the ad elements for any experience based on performance. For experiences that are targeted to specific audiences, ads can be optimized based on the performance of the individual ad elements for the target audience sets. For experiences without specific audience targets, the ad elements are optimized based purely on the performance of the individual ad elements.

## Implementing and managing experiences

Once you create a live experience (with all required ad elements), you can [generate a JavaScript or iframe tag for the entire experience](experience-tag-export.md). You can upload the experience tag as an ad to a campaign in Adobe Advertising DSP or implement it as an ad in a third-party DSP. [!DNL Creative] serves first-party ads and triggers third-party ads for the experience based on the targeting and ad rotation options as well as the available ad inventory.

## Performance data for your experiences

The following performance data is available:

* When you enable the [!UICONTROL Metrics] option in the [!UICONTROL Creative] > [!UICONTROL Experiences] view, each experience card or row indicates the number of impressions and clicks that the experience received.

  ![Metrics option](/help/creative/assets/metrics-option.png "Metrics option")

  <!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

  <!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. --> 

* You can [view detailed performance data for any experience](experience-performance-details.md) from the [!UICONTROL Experiences] view.

* To monitor performance across your experiences, create a [Custom Creative Report](/help/creative/report-custom-creative.md).

## Experience statuses {#experience-statuses}

The status of an experience is set automatically, except for *Deleted,* which you set manually.

| Status | Description |
| ------ | ----------- |
| [!UICONTROL Live] | The experience includes all the required elements, so you can generate an experience tag to implement as an ad in a DSP. A live experience may be scheduled to start in the future. |
| [!UICONTROL Draft] | All branches of the experience aren't assigned creatives, so the experience is incomplete, and you can't generate an experience tag. |
| [!UICONTROL Processing] | A previously-live experience was edited but is now incomplete. You can't generate an experience tag for it. **Note:** If you already implemented an experience tag for the experience, then the previously-live version can still be served. If you later complete the experience &mdash; making it live again &mdash; then the new version can be served using the existing tag implementation. |
| [!UICONTROL Deleted] | The experience was deleted from [!DNL Creative] and is no longer visible in the [!UICONTROL Experiences] views. | 

>[!NOTE]
>
>You can change the status of an ad within a DSP without affecting the experience status in [!DNL Creative].

## The [!UICONTROL Experiences] view

The [!UICONTROL Experiences] view shows all of your targeted and non-targeted experiences. You can see the experience names, status, start and end dates, number and dimensions of the assigned creatives or creative bundles, and whether the experience includes dynamic ads. When you enable the [!UICONTROL Metrics] option in the [!UICONTROL Experiences] view, each experience card or row indicates the number of impressions and clicks that the experience received.

You can create and manage your experiences, create and rename ad experience tags, and export the tags in JavaScript and iframe formats for implementation on your DSPs. Advertisers with Advertising DSP can optionally upload ad tags directly to an Advertising DSP campaign.

### Available actions

The following are key actions available. For a full list, see the table of contents for the Creatives > Experiences chapter.

* [Download data within the view](experience-download-view.md)

* [Create](/help/creative/experiences/experience-create-targeting.md) and [edit](/help/creative/experiences/experience-edit-targeting.md) an experience with targeting

* [Create](/help/creative/experiences/experience-create-no-targeting.md), [edit](/help/creative/experiences/experience-edit-no-targeting.md), and [manually create an ad tag](/help/creative/experiences/experience-tag-create-manually.md) for an experience without targeting

* [Clone](experience-clone.md) an experience

* [Preview](experience-preview.md) an experience

* [Share a demo URL](experience-share-demo-url.md) for an experience

* [Export ad tags for an experience](experience-tag-export.md), including optionally uploading ad tags directly to an Advertising DSP campaign

* [Delete](experience-delete.md) an experience

>[!MORELIKETHIS]
>
>* [Create an experience with decision tree targeting](experience-create-targeting.md)
>* [Create an experience without targeting](experience-create-no-targeting.md)
