---
title: 
description: 
---
# About uploading account data for reporting and simulations

<!-- As of Aug. 2024, this will remain in closed beta for quite some time. Not even selling it yet. --
>
<!-- File name??? -->

<!-- Move all related files into one page? -->

If you use online ad networks for which Search, Social, & Commerce doesn't provide API support, you can upload campaign content and offline cost, click, and conversion data for an account for reporting and performance simulations. Advertisers with an [[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md) can view the data within Adobe Analytics.

This feature is available for ad networks that follow the standard three-tiered campaign structure (campaign, ad group or ad set, and bid unit (ad or keyword)). For Adobe DSP, the feature is available for packages and the placements assigned to a package, but not for campaigns nor placements with placement-level pacing.




ontaining  dimensions(metadata), click and revenue data to the platform. Once uploaded files is processed, customer will have the ability to utilise functionalities such as reporting, simulation and analytics


Out-of-the-box support is available for the following networks:<!-- But what if you want to use something else? Is that possible currently? -->

* Adobe DSP <!-- Is any data upload required, or just an initial setup of an S3 bucket and/or something else, and then DSP sends the data automatically? If so, then I may need to reframe this whole chapter accordingly. -->
* [!DNL Apple Search Ads]
* [!DNL LinkedIn Ads]
* [!DNL Reddit Ads]
* [!DNL TikTok Ads]

<!-- What happened to Snapchat Ads?  -->

Search, Social, & Commerce click tracking and Adobe Advertising conversion tracking aren't supported with this feature.

## Functionality available within Search, Social, & Commerce

* Tracking and reporting:

  * Read-only campaign components down to the bid unit level within campaign management views.

  * Performance data down to the ad group level <!-- verify the entity level --> within campaign management views and custom reports. Advertisers with [!DNL Adobe Analytics for Advertising]) additionally get performance data down to the ad group level <!-- verify the entity level --> within the Adobe Analytics report suites specified for the advertiser.<!-- Verify if the data types are limited -- cost, click, display impression, revenue? -->

* Performance XXX<!-- ??? -->

  * Performance simulations when you add the campaigns to a portfolio.<!-- How does this even work? Do they need to be in standard or hybrid portfolios, with active or optimized status, and can you mix these campaigns with API-synced campaigns? If so, do we just ignore these campaigns and optimize the others? -->

    Search, Social, & Commerce doesn't optimize anything for these types of campaigns.

<!-- What about
Budget recommendations (spend recommendations) across ad networks [search engines + Meta]. - Meta is API-synced now, so 
 -->


## Workflow for setting up offline accounts

<!-- subtitle wording? -->

1. [Set up a dummy account record](/help/search-social-commerce/campaign-management/accounts/data-upload-account-manage.md).

1. Create a data file for a single account in <!-- what file format? -->, including the status at the day level for campaigns, ad groups, and ads.

  The data must follow the data requirements for the ad network, so the data fields for each entity may vary by ad network. You can download a template for the account by XXXXXX.<!-- add instructions -- next to manual upload option in upload window -->

2. <!-- For all ad networks (excluding DSP), --> Upload the initial data for a single account in either of the following ways:

* Upload a file manually from your device or network.

* Upload the data to a Search, Social, & Commerce-assigned folder in an [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3]) bucket.


<!-- Advertising DSP:  If in beta, then will see packages in portfolio list. Will be GA sooner than other networks. Can ask Diptarka about this. -->

1. Continue to upload new data files daily.

1. Once you've uploaded data for 30 days, you can optionally add the campaigns to XXX <!--how should we refer to them? --> portfolios and generate simulations.

You can view a log of each data upload to see its status. In addition, if you initiate an upload but the upload isn't completely successful, then you receive an error notification via [Notification Center](/help/search-social-commerce/notifications/notification-about.md), based on your notification settings.<!-- Originally, I'd thought that we created an error bulksheet, but I'm not sure that that happens. >

<!-- Data validation, and any troubleshooting? -->

## Required and optional data<!-- include this here, in the procedures, or as a separate file if there's much info and it applies to both upload procedures? -->

The data must follow the data requirements for the ad network. 
The data fields for each entity may vary by ad network.

>[!MORELIKETHIS]
>
>* [About uploading account data for reporting and simulations](data-upload-accounts-about.md)
>* [Upload account data to an [!DNL Amazon] [!DNL S3] bucket](upload-data-from-s3-bucket.md)
>* [Upload account data manually](upload-data-manually.md)
>* [View a log of uploaded account data files](upload-log.md)
>* [Manage ad network accounts for data uploads](/help/search-social-commerce/campaign-management/accounts/data-upload-account-manage.md)
