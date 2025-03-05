---
title: About Adobe Advertising Creative
description: Learn about [!DNL Creative].
feature: Creative Introduction
---
# About Adobe Advertising Creative 2.0

*Closed beta*

<!-- verify all and rewrite to include new stuff -->

As part of Adobe Advertising, Advertising Creative is a self-service platform for automating real-time, personalized ad experiences and optionally optimizing your ads at the creative element level.

## Custom creative libraries of reusable creatives

Your Creative Libraries allow you to manage the creatives you'll use in your ad experiences. You can create multiple libraries, each with individual creatives and creative groups (called *bundles*). You'll add creative bundles to your ad experiences.

## Rules-based experiences

With [!DNL Creative], you can build out stories using a rules-based decision tree model &mdash; unfolding a choreographed string of ads that are customized in real time based on what you know about your audience, and that follow your customers even when they move to different websites<!-- verify if that's true without Adobe CDP -->. For example, the stories can change based on customer behavior, geography, demographics, retargeting, position in the customer journey, and more.

### Implementation of experiences as ads

Once you create an experience, you can generate a JavaScript or iframe tag for the experience and implement the tag as a third-party ad in Advertising DSP or any other DSP.<!-- Add any more info about integration with DSP? -->

<!-- Maybe add a subsection "Audience targeting options" with info about types of creative-level REtargeting and placement-level targeting within your DSP.  Need to clarify if any placement-level targeting might contradict/override creative-level targeting, or if they're completely different.

Advertiser should be able to target all segments which are available in DSP for targeting
-->

### Optimization of ad elements

You can optionally allow [!DNL Creative] to optimize the ad elements for any experience based on performance &mdash; whether or not you define specific audience targets &mdash; using optimized, weighted ad rotation, which is powered by Adobe Sensei.

## Retargeting pixels

You can create retargeting pixels to use as targets for creatives within an ad experience. The targets show ads only to users with specified attributes who previously visited specific webpages.

## Impression, click, and conversion tracking

[!DNL Creative] automatically tracks all impressions and clicks for ads served from an experience. You can also optionally add third-party impression-tracking and click-tracking URLs to creatives in Creative Libraries, as well as custom tracking URLs in an experience.

[!DNL Creative] also tracks conversions from served ads created from your ad experiences.<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optoinal?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## Performance reporting

You can view detailed, experience-level performance reports within Creatives > Experiences.

You can also create Custom Creative reports at Reports > Custom Reports to monitor experience-level performance across your experiences. If you use your [!DNL Creative] experiences as ads within DSP campaigns, then performance data for those ads is available in additional custom reports, just like data for your other DSP ads. <!-- Verify that [!DNL Creative] users have access to ALL other reports, and if I can completely duplicate the report help for both help sets. -->

You can optionally deliver your custom reports to specified [report destinations](/help/dsp/reports/report-destinations/report-destination-about.md).

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [About your creative libraries](/help/creative/creative-libraries/creative-libraries-about.md)
>* [About experiences in Advertising Creative](/help/creative/experiences/experience-about.md)
