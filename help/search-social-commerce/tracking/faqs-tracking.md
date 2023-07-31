---
title: FAQs about tracking
description: Learn answers to common questions about tracking, including troubleshooting issues.
exl-id: f559b977-dd44-4d29-b49e-c41c6fb783d1
feature: Search Tracking
---
# FAQs about tracking

## Tracking features

+++Can I track campaigns that Adobe Advertising doesn't manage?

Yes. If Search, Social, & Commerce is syncing one of your ad network accounts, then it tracks the ad network's click data for all [supported campaign types](/help/search-social-commerce/introduction/supported-inventory.md) in that account. It also tracks conversion data if you've added the Search, Social, & Commerce redirect to your ad and/or keyword destination URLs or tracking templates and implemented conversion tracking in your conversion pages. Clarify with your Adobe Account Team which campaigns you want Search, Social, & Commerce to simply track and which you want them to manage.
+++

+++How do I get multi-event attribution?

For advertisers who use Search, Social, & Commerce or Adobe Analytics conversion tracking tags, Adobe Advertising provides multiple options for attributing conversion data across a series of events that lead to a conversion. An advertiser-level setting determines how to attribute conversion data across events, even when they occur across multiple ad channels, as long as the channels allows impression tracking at the event level. By default, conversions are attributed to the last (most recent) event, but the setting can be configured differently, such as to attribute conversions to the first event or to weight all events evenly. Changing the attribution rule affects how future bids are calculated.

Advertisers who provide all conversion data in a feed file must attribute the conversion to the related transaction events themselves.

>[!NOTE]
>
>In campaign management and portfolio management views, reports, and (available to some users) custom simulations, you can change the rule used to attribute conversion data within the views and report results, without affecting how future bids are calculated.

+++

+++How does Adobe Advertising identify duplicate transactions?

Duplicate transactions may occur when a user refreshes the confirmation page after completing a transaction. Adobe Advertising uses the `ev_transid` attribute to eliminate duplicate transactions with the same transaction ID and property value.

The following is Adobe Advertising's de-duplication logic:

* **When a client sends a value for the `ev_transid` attribute:** Subsequent pixel requests are considered duplicates of the previous one if the following are all the same: the `ev_transid`; the tracking ID for the same keyword, ad, or placement; and the value for a specific conversion metric.

  For example, if multiple loan applications have the same application ID and loan amount for the same keyword on a specific ad network, then they're considered duplicates, and only the first loan application is counted.

* **When a client doesn't send a value for the `ev_transid` attribute:** Subsequent transactions are considered duplicates of the previous one if they share a tracking ID for the same keyword, ad, or placement; and the same value for a specific conversion metric.

  For example, if multiple loan applications have the same keyword ID and loan amount, then they are considered duplicates, and only the first loan application is counted.
+++

## Types of tracking implementation

+++I want to stop using the Adobe Advertising conversion tracking service for one or more campaigns or accounts. How can I quickly remove the tracking code from the tracking URLs?

First, consult with your Adobe Account Team to understand the implications of removing tracking URLs.

In the account or campaign, change the tracking method to "[!UICONTROL No EF Redirect]." Then create a bulksheet using the "[!UICONTROL Generate Tracking URLs]" option, and post it to the ad network. All existing tracking URLs or destination URLs are replaced.
+++

## Data questions

+++How do I know which conversion metric is from a data feed or is tracked by the Adobe Advertising conversion tracking tag?

In a [!UICONTROL Transaction Report], you can tell if an included conversion metric was tracked by the Adobe Advertising conversion tracking pixel if you include the custom column "[!UICONTROL Tracking URL]." Tracking URLs with the Adobe Advertising tracking pixel begin with `http://pixel.everesttech.net`.
+++

+++What are orphan transactions?

Orphan transactions are transaction events that can't be associated with a specific keyword or ad. Adobe Advertising attributes transaction/revenue to a keyword or ad by matching the tracking IDs received with the revenue event to the unique tracking ID in the keyword's or ad's tracking URL.

When an Adobe Account Team suspects that orphan transactions are to blame for a drop in revenue, the Customer Care team checks for orphans and, if it finds any, investigates the issue.

Orphans occur in the following situations.

**Pixel implementations**

Orphan transactions almost never occur for pixel implementations. However, pixel orphans have occurred when:

* The click data isn't available for the conversion's click date. In this case, the data is mapped back when Search, Social, & Commerce gets the click data from the ad network.

* The click logs aren't processed before the conversion logs.

**Feed implementations**

* The tracking ID sent in the feed is from an account that Search, Social, & Commerce doesn’t know about.

* The account is out of sync, or errors occurred during the sync process.

* The tracking ID was added and removed from the ad network while Search, Social, & Commerce was out of sync with the ad network, so Search, Social, & Commerce has no information about the ID. This issue continues to cause orphan revenue if there is a delay in receiving revenue.

* The client sent a tracking ID that's formatted incorrectly in the feed and doesn't match the tracking ID in the URL. This usually occurs because of a formatting issue or when tracking IDs are abbreviated in the feed.

* In the configuration file, the regular expression that's used to extract the tracking ID from the URLs is incorrect or outdated. Sometimes the advertiser changes the tracking ID in the URL or adopts an entirely new tracking system, which requires the Search, Social, & Commerce implementation team to update the regular expression. In such cases, a major portion of the revenue is orphaned.

**Feed implementations using a transaction ID**

No online transactions are available before the dates for which data is available in the offline feed.

**Feed implementations using a token (ef_id)**

Search, Social, & Commerce can't find a corresponding click on its server or on the ad network. This may be because the click data isn't available for the conversion's click date or (rarely) because the click logs weren't processed before the conversion logs. When Search, Social, & Commerce receives the click data from the ad network or the click logs are processed, the data is mapped to the conversion.
+++

## Revenue tracking issues

+++How do I fix old/incorrect data from a feed file?

Contact Customer Care with the corrected data file.
+++

+++Multiple keywords have the same tracking URLs.

**Implications**

For feed implementations with multiple tracking IDs, data is reported against multiple keywords. For other implementations, conversions may be attributed to the wrong keyword because the system assigns a conversion arbitrarily to one of the keywords.

**Possible Cause**

The URL for a new keyword or ad was copied from another keyword or ad.

This shouldn't happen with display or social ads.

**Possible Solution or Work-around**

* If you manage your own keywords and ads, then create a bulksheet file with the correct URLs for the duplicate URLs and post it to the appropriate account using the **[!UICONTROL Generate Tracking URLs]** option, which regenerates URLs for all keywords and ads.

* If an Adobe Account Team manages your keywords, then ask them to create new URLs for the duplicate URLs.
+++
