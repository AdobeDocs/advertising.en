---
title: Generate an Adobe Advertising conversion-tracking tag
description: Learn how to create an Adobe Advertising conversion tag to track your conversion events.
exl-id: 617cd808-c4ba-4413-89e4-0f52cb44f44b
---
# Generate an Adobe Advertising conversion-tracking tag

*Advertisers with Adobe Advertising conversion tracking only*

Create a separate conversion tag for each set of metrics that you want to track, and provide the tags to the advertiser or agency with a list of webpages on which to insert each.

>[!NOTE]
>
>This feature doesn't add image tags or [!DNL JavaScript] tags to the advertiser's webpages. The tags must be added according to the advertiser's normal procedure for updating webpages.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Tools] > [!UICONTROL Conversion Tags]**.

1. Specify the [conversion tag settings](#conversion-tag-settings).

1. Generate the tag:
   
   * If the website uses HTTP, then click **[!UICONTROL Generate Conversion Tag]**.
   
   * If the website runs on a secure server (HTTPS), then click **[!UICONTROL Generate Secure Conversion Tag]**.

1. Copy the tag from the dialog box, and paste it into to the appropriate webpages as needed.

>[!NOTE]
>
>Each metric in the new conversion tag is automatically listed in [!UICONTROL Admin] > [!UICONTROL Conversions], even if it isn't implemented or the webpages it's on haven't received any clicks. This behavior is different from the behavior of metrics in tags created manually or elsewhere, which aren't listed in [!UICONTROL Admin] > [!UICONTROL Conversions] until one of the webpages it's on has received a click. In all cases, however, each metric is initially excluded from portfolio objectives, reports, and views until you explicitly make them available. Before you add the metrics to portfolio objectives, however, consider first making the metrics available and adding them to reports to verify when they receive clicks.

## Adobe Advertising conversion tag settings {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** The type of tag to create:

* *[!UICONTROL Image]:* To create an image tag to display a 1-pixel x 1-pixel transparent image (pixel), which is invisible to end users, on the webpage. The best practice is to use image tags only when the site has a policy against using JavaScript tags.

* *[!UICONTROL JavaScript]:* To create a JavaScript tag.

For more information about the differences between the tag types, see "[FAQs about Adobe Advertising conversion and page view tracking tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)."

**[!UICONTROL Tag Properties]:** One or more conversion metrics to be tracked when an end user views a page containing the conversion tag. To add a metric to the list, enter the metric name in the "[!UICONTROL Add new property]" field and click **[!UICONTROL Add]**.

When multiple metrics are tracked, they're joined by an ampersand (`&`) in the tag, such as `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Metrics added to this list aren't saved anywhere or integrated with the client's [!UICONTROL Conversions] list on the [!UICONTROL Admin] tab. However, metrics are added to the client's [!UICONTROL Conversions] list automatically once Adobe Advertising actually gathers data for a metric, which happens when the conversion tag is implemented on a page and an end user completes a transaction that opens that page.

**[!UICONTROL Include unique transaction IDs]:** (Optional) Includes a transaction ID property (`ev_transid=<transid>`) in the tag. The option is selected by default.

When you select this option, the advertiser must generate a unique value for `<transid>` (for example, an actual order ID) when the transaction is complete and pass it back to Adobe Advertising, such as `ev_transid=0123`. Adobe Advertising uses the transaction ID to eliminate duplicate transactions with the same transaction ID and property value. The transaction ID can't contain ampersand symbols (`&`), which are reserved as parameter separators. The transaction ID is included in [the [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), which you can use to validate data within Search, Social, & Commerce with the advertiser's data.

If the data doesn't include a unique ID per transaction, then Adobe Advertising still generates one based on transaction time.

>[!NOTE]
>
>If you send [transaction ID feeds](/help/search-social-commerce/tracking/feed-transaction-id.md) with conversion data for offline conversions, then you must submit the transaction ID (`ev_transid`) for the online part of the transaction in the feed data for offline parts of the transaction.

**[!UICONTROL Page is inside FB app]:** Obsolete

**[!UICONTROL Segment users]:** Obsolete

**[!UICONTROL JS Version]:** ([!DNL JavaScript] tags only) Which version of the [!DNL JavaScript] tag to create: *[!UICONTROL v2]* (the default) or *[!UICONTROL v3]*.

See "[FAQs about Adobe Advertising conversion and page view tracking tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)." for more information about the differences.
 
>[!MORELIKETHIS]
>
>* [About Adobe Advertising conversion-tracking tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [About the tools to create and decode tracking tags](tracking-tools-about.md)
>* [FAQs about conversion and page view tracking tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format of JavaScript conversion tracking tags version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format of JavaScript conversion tracking tags version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format of image conversion tracking tags](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [The Adobe Advertising JavaScript conversion mapping tag](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [About managing an advertiser's conversion metrics](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
