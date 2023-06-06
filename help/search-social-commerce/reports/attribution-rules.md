---
title: How attribution rules are calculated
description: Learn how Adobe Advertising calculates each type of attribution rule.
---
# How attribution rules are calculated for Adobe Advertising

*Advertisers with Adobe Advertising conversion tracking only*

<!-- Verify statements about cross-device events -->

The advertiser-level attribution rule is used to attribute conversion data &mdash; potentially across multiple ad channels &mdash; in a series of events that lead to a conversion.

In reports, default and custom views for Advertising Search, Social, & Commerce (Search, Social, & Commerce), and (some user roles) portfolio-level simulations for Search, Social, & Commerce, the selected rule is used only for the view, report, or simulation data. The various attribution rules are applied as follows.

>[!NOTE]
>
>* Attribution rules apply to clicks on paid ads in any channel and to impressions on display and social ads. They don't apply to impressions for paid search ads, which can't be tracked at the event level.
>* Adobe Advertising always stores the following events for each Web surfer before a conversion:  a) the first paid click; b) up to 10 clicks for each channel (search, social, or display), including the first click; and c) up to 10 display impressions. <!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
* In Advertising DSP and Advertising Creative, cross-device definitions consider only the event path from the attribution rule selected.<!-- cross-device attribution via LiveRamp only -->
* In reports and management views, the number of decimal places shown for a value depends on the currency, but Adobe Advertising stores more precise values.
 
## Last Event (the default)

Attributes the conversion to the last paid click in the series within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) or, if no paid clicks occurred, to the last impression within the advertiser's [impression lookback window](/help/search-social-commerce/glossary.md#i-j).

When the conversion is preceded only by impressions, then the conversion is considered a *view-through*, which is weighted either according to the advertiser's [view-through weight setting](/help/search-social-commerce/glossary.md#uv) or &mdash; as specified &mdash; according to the view-through valuation method specified in the report, view, or custom simulation parameters.

![Last event attribution percentages](/help/search-social-commerce/assets/attribution-percent-last-event.png "Last event attribution percentages")

<!-- start examples as collapsible content -->

+++Examples of event calculations

### Example with all clicks

Event path: Click1, Click2, Click3, Conversion of 120 USD
 
The conversion is attributed to Click 3 in the amount of 120 USD.

### Example with both impressions and clicks

**Note:** Impressions are applicable only from display and social ads.

Event path: Impression 1, Click 1, Impression 2, Conversion of 120 USD

The conversion is attributed to Click 1 in the amount of 120 USD.

### Example with all impressions

**Note:** Only impressions for display and social ads are applicable.

Event path: Impression 1, Impression 2, Impression 3, Conversion of 120 USD
 
The conversion is attributed to Impression 3. Because the conversion is a view-through, the view-through valuation method selected in the "Conversion Attribution" section of the report settings is applied:

* If the report parameter specifies a weighted view-through weight, then that weight is applied to the view-through. For example, if the advertiser's view-through weight is 40%, then 120 USD x 40% = 48 USD, so 48 USD is attributed to Impression 3.

* If the report parameter specifies using raw values for view-throughs, then no view-through weight is applied to the view-through, and the full 120 USD is attributed to Impression 3.

+++

<!-- end examples as collapsible content -->

## First Event

Attributes the conversion to the first paid click in the series within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) or, if no paid clicks occurred, to the first impression within the advertiser's [impression lookback window](/help/search-social-commerce/glossary.md#i-j). This rule is available for events across single devices only.

When the conversion is preceded only by impressions, the conversion is considered a *view-through*, which is weighted either according to the advertiser's [view-through weight setting](/help/search-social-commerce/glossary.md#uv) or &mdash; as specified &mdash; according to the view-through valuation method specified in the report, view, or custom simulation parameters.

![First event attribution percentages](/help/search-social-commerce/assets/attribution-percent-first-event.png "First event attribution percentages")

<!-- start examples as collapsible content -->

+++Examples of event calculations

### Example with all clicks

Event path: Click 1, Click 2, Click 3, Conversion of 120 USD

The conversion is attributed to Click 1 in the amount of 120 USD.

### Example with both impressions and clicks

**Note:** Impressions are applicable only from display and social ads.

Event path: Impression 1, Click 1, Impression 2, Conversion of 120 USD

The conversion is attributed to Click 1 in the amount of 120 USD.

### Example with all impressions

**Note:** Only impressions for display and social ads are applicable.

Event path: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

The conversion is attributed to Impression 1. Because the conversion is a view-through, the view-through valuation method selected in the "(Display Campaigns) Conversion
Attribution" section of the report settings is applied:

* If the report parameter specifies a weighted view-through weight, then that weight is applied to the view-through. For example, if the advertiser's view-through weight is 40%, then 120 x 40% = 48 USD, so 48 USD is attributed to Impression 1.

* If the report parameter specifies using raw values for view-throughs, then no view-through weight is applied to the view-through, and the full 120 USD is attributed to Impression 1.

+++

<!-- end examples as collapsible content -->

## Weight First Event More

Attributes the conversion to all events in the series that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j), but gives the most weight to the first event and successively less weight to the following events.This rule is available for events across single devices only.

When the conversion is preceded only by impressions, the conversion is considered a *view-through*, which is weighted either according to the advertiser's [view-through weight setting](/help/search-social-commerce/glossary.md#uv) or &mdash; as specified &mdash; according to the view-through valuation method specified in the report, view, or custom simulation parameters.

When the conversion path includes both paid clicks and impressions, the impressions are treated differently by different Adobe Advertising products:

* In Search, Social, & Commerce, the [impression override weight](/help/search-social-commerce/glossary.md#i-j) &mdash; which is specified in the advertiser's impression override weight setting and in report, view, or custom simulation parameters &mdash; is first applied to the impressions.

* In DSP, the impressions are ignored, and only clicks are weighted. DSP doesn't take impression override weights into consideration for attribution.

![Weight first event more attribution percentages](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "Weight first event more attribution percentages")

<!-- start examples as collapsible content -->

+++Examples of event calculations

### Example with all clicks

Event path: Click 1, Click 2, Click 3, Conversion of 120 USD

Attribution: Click 1 = 60 USD, Click 2 = 40 USD, Click 3 = 20 USD (120 USD total)

### Examples with both impressions and clicks

**Note:** Impressions are applicable only from display and social ads.

Event path: Impression 1, Click 1, Impression 2, Click 2, Conversion of 120 USD

#### (Search, Social, & Commerce only) Using the default "Impression Override Weight" of 10%

Because the event series included both impressions and clicks, the impression override weight applies to the impressions.

Attribution: Impression 1 = 8 USD, Click 1 = 72 USD, Impression 2 = 4 USD, Click 2 = 36 USD (120 USD total)

#### Using (DSP only) no Impression Override Weight or (Search, Social, & Commerce only) an "Impression Override Weight" of 0%

Because the event series included both impressions and clicks, the impressions are ignored.

Attribution: Impression 1 = 0 USD, Click 1 = 80 USD, Impression 2 = 0 USD, Click 2 = 40 USD (120 USD total)

### Example with all impressions

**Note:** Only impressions for display ads are applicable.

Event path: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

Because the conversion is a view-through, the view-through valuation method &mdash; rather than the impression override weight &mdash; is applied to determine the value of each impression:

* If the report parameter specified a weighted view-through weight, then that weight is applied to the impression values. For example, if the view-through weight is 40%, then Impression 1 = 24 USD, Impression 2 = 16 USD, Impression 3 = 8 USD (48 USD total)

* If the report parameter specifies using raw values for view-throughs, then no view-through weight is applied to the impression, and the full 120 USD is divided between the three impressions: Impression 1 = 60 USD, Impression 2 = 40 USD, Impression 3 = 20 USD (120 USD total)

+++

<!-- end examples as collapsible content -->

## Even Distribution

>[!NOTE]
>
>This rule is available for events across single devices only.

Attributes the conversion equally to each event in the series that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j).

When the conversion is preceded only by impressions, the conversion is considered a *view-through*, which is weighted either according to the advertiser's [view-through weight setting](/help/search-social-commerce/glossary.md#uv) or &mdash; as specified &mdash; according to the view-through valuation method specified in the report, view, or custom simulation parameters.

When the conversion path includes both paid clicks and impressions, the impressions are treated differently by different Adobe Advertising products:

* In Search, Social, & Commerce, the [impression override weight](/help/search-social-commerce/glossary.md#i-j) &mdash; which is specified in the advertiser's impression override weight setting and in report, view, or custom simulation parameters &mdash; is first applied to the impressions.

* In DSP, the impressions are ignored, and only clicks are weighted. DSP doesn't take impression override weights into consideration for attribution.

![Even attribution percentages](/help/search-social-commerce/assets/attribution-percent-even.png "Even attribution percentages")

<!-- Add in
Examples of event calculations

<!-- start examples as collapsible content -->

+++Examples of event calculations

### Example with all clicks

Event path: Click 1, Click 2, Click 3, onversion of 120 USD

No impressions led to the conversion, so the impression override weight isn't applicable, and the conversion is divided equally between the three clicks:

Attribution: Click 1 = 40 USD, Click 2 = 40 USD, Click 3 = 40 USD (120 USD total)

### Examples with both impressions and clicks

**Note:** Impressions are applicable only from display and social ads.

Event path: Impression 1, Click 1, Impression 2, Click 2, Conversion of 120 USD

#### (Search, Social, & Commerce only) Using the default "Impression Override Weight" of 10%

Because the event series included both impressions and clicks, the impression override weight applies to the impressions.

Attribution: Impression 1 = 6 USD, Click 1 = 54 USD, Impression 2 = 6 USD, Click 2 = 54 USD (120 USD total)

#### Using (Adobe Advertising DSP only) no Impression Override Weight or (Search, Social, & Commerce only) an "Impression Override Weight" of 0%

Because the event series included both impressions and clicks, the impressions are ignored.

Attribution: Impression 1 = 0 USD, Click 1 = 60 USD, Impression 2 = 0 USD, Click 2 = 60 USD (120 USD total)

## Example with all impressions

**Note:** Only impressions for display ads are applicable.

Event path: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

Because the conversion is a view-through, the view-through valuation method &mdash; rather than the impression override weight &mdash; is applied to determine the value of each impression:

* If the report parameter specified a weighted view-through weight, then that weight is applied to the impression values. For example, if the view-through weight is 40%, then Impression 1 = 16 USD, Impression 2 = 16 USD, Impression 3 = 16 USD (48 USD total)

* If the report parameter specifies using raw values for view-throughs, then no view-through weight is applied to the impression, and the full 120 USD is divided between the three impressions: Impression 1 = 40 USD, Impression 2 = 40 USD, Impression 3 = 40 USD (120 USD total)

+++

<!-- end examples as collapsible content -->

## Weight Last Event More

Attributes the conversion to all events in the series that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j), but gives the most weight to the last event and successively less weight to the preceding events.

When the conversion is preceded only by impressions, the conversion is considered a *view-through*, which is weighted either according to the advertiser's [view-through weight setting](/help/search-social-commerce/glossary.md#uv) or &mdash; as specified &mdash; according to the view-through valuation method specified in the report, view, or custom simulation parameters.

When the conversion path includes both paid clicks and impressions, the impressions are treated differently by different Adobe Advertising products:

* In Search, Social, & Commerce, the [impression override weight](/help/search-social-commerce/glossary.md#i-j) &mdash; which is specified in the advertiser's impression override weight setting and in report, view, or custom simulation parameters &mdash; is first applied to the impressions.

* In DSP, the impressions are ignored, and only clicks are weighted. DSP doesn't take impression override weights into consideration for attribution.

![Weight last event more attribution percentages](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "Weight last event more attribution percentages")

<!-- start examples as collapsible content -->

+++Examples of event calculations

### Example with all clicks

Event path: Click 1, Click 2, Click 3, Conversion of 120 USD

Attribution: Click 3 = 60 USD, Click 2 = 40 USD, Click 1 = 20 USD (120 USD total)

### Examples with both impressions and clicks

**Note:** Impressions are applicable only from display and social ads.

Event path: Impression 1, Click 1, Impression 2, Click 2, Conversion of 120 USD

#### (Search, Social, & Commerce only) Using the default "Impression Override Weight" of 10%

Because the event series included both impressions and clicks, the impression override weight applies to the impressions.

Attribution: Impression 1 = 4 USD, Click 1 = 36 USD, Impression 2 = 8 USD, Click 2 = 72 USD (120 USD total)

#### Using (DSP only) no Impression Override Weight or (Search, Social, & Commerce only) an "Impression Override Weight" of 0%

Because the event series included both impressions and clicks, the impressions are ignored.

Attribution: Impression 1 = 0 USD, Click 1 = 40 USD, Impression 2 = 0 USD, Click 2 = 80 USD (120 USD total)

### Example with all impressions

**Note:** Impressions are applicable only from display and social ads.
 
Event path: Impression 1, Impression 2, Impression 3,Conversion of 120 USD

Because the conversion is a view-through, the view-through valuation method &mdash; rather than the impression override weight &mdash; is applied to determine the value of each impression:

* If the report parameter specified a weighted view-through weight, then that weight is applied to the impression values. For example, if the view-through weight is 40%, then multiply each value in the "Example with all clicks" by 40%: Impression 3 = 24 USD, Impression 2 = 16 USD, Impression 1 = 8 USD (48 USD total)

* If the report parameter specifies using raw values for view-throughs, then the full 120 USD is divided between the impressions: Impression 3 = 60 USD, Impression 2 = 40 USD, Impression 1 = 20 USD (120 USD total)

+++

<!-- end examples as collapsible content -->

## U-shaped

Attributes the conversion to all events in the series that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j), but gives the most weight to the first event and last events, with successively less weight to the events in the middle of the conversion path.

When the conversion is preceded only by impressions, the conversion is considered a *view-through*, which is weighted either according to the advertiser's [view-through weight setting](/help/search-social-commerce/glossary.md#uv) or &mdash; as specified &mdash; according to the view-through valuation method specified in the report, view, or custom simulation parameters.

When the conversion path includes both paid clicks and impressions, the impressions are treated differently by different Adobe Advertising products:

* In Search, Social, & Commerce, the [impression override weight](/help/search-social-commerce/glossary.md#i-j) &mdash; which is specified in the advertiser's impression override weight setting and in report, view, or custom simulation parameters &mdash; is first applied to the impressions.

* In DSP, the impressions are ignored, and only clicks are weighted. DSP doesn't take impression override weights into consideration for attribution.

![U-shaped attribution percentages](/help/search-social-commerce/assets/attribution-percent-u-shaped-event.png "U-shaped event attribution percentages")

<!-- start examples as collapsible content -->

+++Examples of event calculations

### Example with all clicks

Event path: Click 1, Click 2, Click 3, Click 4, Conversion of 120 USD

Attribution: Click 1 = 36 USD, Click 2 = 24 USD, Click 3 = 24 USD, Click 4 = 36 USD (120 USD total)

### Examples with both impressions and clicks

**Note:** Impressions are applicable only from display and social ads.

Event path: Impression 1, Click 1, Impression 2, Click 2, Conversion of 120 USD

#### (Search, Social, & Commerce only) Using the default "Impression Override Weight" of 10%

Because the event series included both impressions and clicks, the impression override weight applies to the impressions.

Attribution: Impression 1 = 6 USD, Click 1 = 54 USD, Impression 2 = 6 USD, Click 2 = 54 USD (120 USD total)

#### Using (DSP only) no impression override weight or (Search, Social, & Commerce only) an "Impression Override Weight" of 0%

Because the event series included both impressions and clicks, the impressions are ignored.

Attribution: Impression 1 = 0 USD, Click 1 = 60 USD, Impression 2 = 0 USD, Click 2 = 60 USD (120 USD total)

### Example with all impressions

**Note:** Only impressions for display ads are applicable.

Event path: Impression 1, Impression 2, Impression 3, Impression 4, Conversion of 120 USD

Because the conversion is a view-through, the view-through valuation method &mdash; rather than the impression override weight &mdash; is applied to determine the value of each impression:

* If the report parameter specified a weighted view-through weight, then that weight is applied to the impression values. For example, if the view-through weight is 40%, then Click 1 = 14.40 USD, Click 2 = 9.60 USD, Click 3 = 9.60 USD, Click 4 = 14.40 USD (48 USD total)

* If the report parameter specifies using raw values for view-throughs, then the full 120 USD is divided between the impressions: Click 1 = 36 USD, Click 2 = 24 USD, Click 3 = 24 USD, Click 4 = 36 USD (120 USD total)

+++

<!-- end examples as collapsible content -->
