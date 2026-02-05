---
title: About Google conversion value rules
---

# About Google conversion value rules

Search, Social, & Commerce automatically syncs the [conversion value rules](https://support.google.com/google-ads/answer/10518330) from your Google Ads accounts. Conversion value rules let you adjust the values of conversion events based on user information, including the device type, location, and audience segment. You can use rules for value-based bidding in search, display, shopping, and performance max campaigns with Google Smart Bidding. For campaigns with Maximize Conversions and Target ROAS bidding strategies, Google Ads algorithms will start preferring conversions with a higher value.

Campaign-level conversion value rules override account-level rules. When a conversion satisfies multiple conversion value rules, only one of the rules is applied. Usually, the most specific rule is applied, but see the [Google Ads documentation on priorities for the different rule condition types](https://support.google.com/google-ads/answer/10520348).

## The conversion value rules view and functionality

All rules created in the Google Ads interface are synced within 24 hours and are available in the Optimization > Conversion Value Rules view. Some accounts can manage their conversion value rules:

* In accounts for which conversions are tracked at the individual account or campaign level, you can create, edit, and change the status of your account-level and campaign-level rules.

  The accounts can be linked to Google Ads manager accounts, but they can't use cross-account conversions tracking (for which conversions are tracked across all accounts in the manager account).

* In accounts that use cross-account conversion tracking, your account-level and campaign-level rules are inherited from the manager account and are read-only.

## Conversion value rules with Search, Social, & Commerce portfolios

When the advertiser account is configured to upload Search, Social, & Commerce objectives to Google Ads, and you include a campaign that uses a conversion value rule in a portfolio with an objective, then Google Ads applies the conversion value rule to the original conversion value specified in the objective. As a result, conversion data in Advertising Search, Social, & Commerce will differ from the conversion data in Google Ads.

For example, suppose the objective uses a single conversion metric "Leads" and gives conversions from mobile devices a weight of 10 and conversions from non-mobile devices a weight of 10. Advertising Search, Social, & Commerce will count an event from either device type as one (1) conversion and credit the conversion value as 10. However, suppose a campaign in that portfolio uses a conversion value rule "If Device is Mobile, then multiply by 2." When a mobile Leads event is tracked for that campaign, Google Ad will also credit the conversion count as one (1) but the conversion value as (10 x 2) = 20.

To see more information about your rules, including the original conversion values before rules were applied, see the [conversion value rules report in Google Ads](https://support.google.com/google-ads/answer/10519848).

>[!MORELIKETHIS]
>
>* [Create a Google conversion value rule](create-google-conversion-value-rule.md)
>* [Edit a Google conversion value rule](edit-google-conversion-value-rule.md)
>* [Change the status of a Google conversion value rule](change-the-status-of-google-conversion-value-rule.md)
>* [Google conversion value rule settings](google-conversion-value-rule-settings.md)

