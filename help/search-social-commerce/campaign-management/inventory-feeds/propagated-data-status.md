---
title: Statuses of data generated from feeds
description: Learn about the statuses for data generated from inventory data feeds.
exl-id: 8e5e7649-a16b-4634-896a-7c216185b367
feature: Search Inventory Feeds
---
# Statuses of data generated from feeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (delete actions only), and [!DNL Yandex] accounts only*

Each component can have one of the following statuses:

* *[!UICONTROL New]:* The component doesn't exist on the ad network and wasn't posted to the ad network, and you can still edit its settings if necessary by clicking the component name. When you're ready to post the data, click **[!UICONTROL Post to SE]** and specify the data to submit.

* *[!UICONTROL Posted]:* (Campaigns and ad groups only) The campaign or ad group was partially posted to the ad network, but some components weren't posted because of errors. The validation status of each keyword and ad shows what information needs to be corrected. You can edit the component's settings if necessary by clicking the component name.

* *[!UICONTROL Active]:* The component is already active on the ad network, and you can't edit its settings here. Active components may include subcomponents that are [!UICONTROL New], which can be posted if the data is valid.

* *[!UICONTROL Paused]:* The component is already paused on the ad network, and you can't edit its settings here. Paused components may include subcomponents that are [!UICONTROL New], which can be posted if the data is valid.

* *[!UICONTROL Deleted]:* The component was already deleted on the ad network, and you can't edit its settings here. Deleted components may include subcomponents that are [!UICONTROL New], which can be posted if the data is valid.

>[!MORELIKETHIS]
>
>* [About inventory feeds](inventory-feeds-about.md)
>* [View data generated from feeds](propagated-data-view.md)
>* [Edit data generated from feeds](propagated-data-edit.md)
>* [Post campaign data generated from feeds to ad networks](propagated-data-post.md)
>* [Stop a posting job for inventory feed data](stop-job.md)
