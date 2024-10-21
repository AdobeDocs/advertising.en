---
title: Glossary
description: See definitions of key terms.
exl-id: 87ce61b5-8340-4a6b-bd98-89ef73b2a9d8
feature: Search Introduction
---
# Glossary {#glossary}

## A-B {#a-b}

**ad group:** A set of ads and their related keywords, placements, and product groups for a campaign.

**ad variation:** Any ad within an ad group or ad strategy.

**[AMO ID](/help/integrations/analytics/ids.md#amo-id):** A tracking code that allows Adobe Advertising to share data about campaigns with Adobe Analytics. It begins with `s_kwcid=`.

**bid unit:** A Search, Social, & Commerce term for a unit on which bids are placed.

* For CPC campaigns, this is a keyword and its match type for a search or content campaign, a unit-level product group (the lowest level of subdivision) for a shopping campaign, or a dynamic search target for a dynamic search ad campaign. When the same keyword and match type combination, the same product group, or the same dynamic search target occurs within multiple ad groups in a single campaign, all instances are considered the same bid unit and thus have the same bid.

* For campaigns with the [!DNL Maximize Clicks], [!DNL Maximize Conversion Value], [!DNL Maximize Conversions], [!DNL Target Cost Per Acquisition], or [!DNL Target Return on Ad Spend] spend strategies, each campaign is a bid unit.

* For campaigns on [!DNL Yahoo! Display Network], which doesn't use keywords, all ads within an ad group have the same bid and are considered the same bid unit.

**bid unit constraint:** See "constraint."

## C-D {#c-d}

**campaign:** A set of ad groups in a single ad account that share a budget, time span, targeting, and other settings. **Note:** [!DNL Baidu] doesn't have the concept of campaigns, but Search, Social, & Commerce creates pseudo-campaigns for each set of related ad groups in existing [!DNL Baidu] accounts that are synched within Search, Social, & Commerce.

**case-sensitive field:** A case-sensitive field or query treats uppercase letters (such as C) differently than lowercase letters (such as c). For example, Car is treated as a different value than car.

**click:** A single user click on or within an online ad.

**click lookback window:** An advertiser-level setting that specifies the number of days after a paid click in an event series occurs in which the click can be attributed to a conversion.

**click time:** The time at which an end user with a unique IP address first clicks an ad in the ad network.

**click-through rate:** (CTR) The number of clicks divided by the number of impressions on an ad. Ads that are most relevant to the search query have the highest click-through rates.

**click-tracking URL:** A tracking template or a destination URL with embedded code to track clicks on a keyword, ad variation, or placement.

**constraint:** (Advertisers with portfolios; applicable for bid units in standard portfolios only) A rule for bidding on a specific keyword or ad. It overrides any portfolio-level limits and the recommended bidding strategy.

**conversion:** The completion of an action after an end user clicks an ad, usually captured as a metric. Examples include registrations and purchases, and they can represent counts or monetary amounts. A conversion can consist of one or more transaction events, but the terms "conversion" and "transaction" are often used interchangeably.

**conversion tracking:** Conversion tracking uses cookies to track a) clicks on an advertiser's ads on the ad networks and b) the resulting transactions on the advertiser's website.

**cost accuracy:** (Advertisers with portfolios) The actual spend for a portfolio divided by the forecasted spend. [Model accuracy reports](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indicate the accuracy of the cost models that are used for optimization, and the [[!UICONTROL Model Accuracy]insight](/help/search-social-commerce/advertising-insights/insight-about.md) includes more details, in addition to recommendations to improve model accuracy.

**cost model:** (Advertisers with portfolios) Search, Social, & Commerce technology that predicts cost volume, the bid required to win each position or placement, and the CPC (search) or CPM (display) for each bid unit using historical data and mathematical forecasting techniques.

**cost model coverage:** (Advertisers with portfolios) The number and/or percentage of bid units in CPC or eCPC campaigns that have received at least one impression in the last seven days so that the optimization capability can build cost models. Not all bid units have cost models; the bid units with cost models count toward the cost model coverage.

**cost model half-life:** (Advertisers with portfolios) The number of days before the current date for which the cost data is considered more recent and therefore more relevant for cost models.

**cost per 1000 impressions:** (CPM) The cost of an ad for each one thousand impressions. Advertisers using a CPM pricing model pay by impressions rather than by clicks.

**cost per acquisition:** (CPA) The cost of an ad divided by the number of conversions. Also called cost per transaction (CPT) or cost per order (CPO).

**cost per click:** (CPC) 1) The cost of an ad divided by the total number of clicks for the ad. For example, if you spend 100 USD for an ad impression and the ad generates 10 clicks, then the cost per click is 100 USD/10=10 USD per click. 2) A pricing model in which advertisers are charged for each ad click.

**cost per order:** (CPO) The cost of an ad divided by the number of orders. Also called cost per acquisition (CPA) or cost per transaction (CPT).

**cost per transaction:** (CPT) The cost of an ad divided by the number of transactions. Also called cost per acquisition (CPA).

**CPA:** See "cost per acquisition."

**CPC:** See "cost per click."

**CPM:** See "cost per 1000 impressions."

**CPO:** See "cost per order."

**CPT:** See "cost per transaction."

**CSV:** A file format consisting of comma-separated values (CSV).

**CTR:** See "click-through rate."

## E-F {#e-f}

**eCPM:** The effective CPM, or the average cost paid per 1000 impressions during a specified date range. eCPM values can be calculated for either CPM or CPC campaigns.

## G-H {#g-h}

**half-life:** The time required for a quantity to decrease to half of its initial value. For each portfolio, you can specify half-lives to indicate how long data is relevant for cost models and revenue models. 
See "cost model half-life" and "revenue model half-life."

## I-J {#i-j}

**impression:** A single display of an ad on a webpage, mobile app, or other delivery medium. A user doesn't have to view or click the ad for it to count as an impression.

**impression lookback window:** (Display and social campaigns only) An advertiser-level setting that specifies the number of days after an ad impression occurs that the impression can be attributed to a conversion.

**impression override weight:** A specified percentage of a conversion value to attribute to impressions that occur within the client’s impression lookback window when the conversion is preceded by both paid clicks and impressions. When a conversion is preceded only by impressions, the advertiser's view-through weight, rather than the impression override weight, is applied to the impressions.

## K-L {#k-l}

**keyword:** A word or phrase associated with an ad.

**keyword constraint:** See "constraint."

**label classification:** A way to group your account components into meaningful sets. A label classification can contain multiple label values, which denote attributes. For example, a "Geo" label classification could include values for different geographical regions. 

**label value:** An element of a label classification. It can be assigned as a tag to ad campaigns and campaign entities so you can filter performance data and reports by label or configure optional constraints on bid units associated with the label.

**landing page URL:** The URL of the advertiser's webpage that opens when the end user clicks an ad.

## M-N {#m-n}

**marginal cost:** The change in total cost when the quantity changes by one unit.

**marginal cost-to-objective value:** The change in cost needed to raise the objective value by one (1). This has the same value as the legacy column "Marginal Cost-to-Revenue."

**match type:** An option that specifies how search terms are matched to ads. The options vary by ad network.

**minimum bid:** 1) The minimum amount to pay per impression or per 1000 impressions. 2) For search keywords, the minimum bid required for a given keyword based on its quality score. The minimum bid is usually the least amount you can pay per click in order for your keyword to show ads.

**model accuracy:** (Advertisers with portfolios) The percentage of accuracy of the cost models and revenue models that are used for optimizing bids, campaign budgets, and bid strategy targets for a portfolio. See "cost model," "cost accuracy," "revenue model," and "revenue accuracy."  [Model accuracy reports](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indicate the accuracy of the cost and revenue models.

## O-P {#o-p}

**objective:** (Advertisers with portfolios) A goal which a client sets to meet its business objective for a specific portfolio or a display campaign, such as to maximize profits or to meet a specific sales target. An objective consists of the conversion metrics to be tracked and optimized for the portfolio, and the relative weights of those metrics. The total weighted conversions for the portfolio are calculated are referred to as the "objective value."

**objective value:** (Advertisers with portfolios) The total weighted conversions as calculated according to the portfolio's current objective, including:

* all conversions, taking into account a) the weights assigned to each conversion in the portfolio's objective and, when applicable, b) the view-through weight for display view-throughs.

* all clicks, which the optimization capability considers a single conversion and is weighted according to the click value for the objective.

This has the same value as the legacy column "Weighted Revenue."

**optimization capability:** (Advertisers with portfolios) Search, Social, & Commerce keyword bidding technology, which determines the optimal bidding and budget management strategy for a portfolio based on its business objective.

**orphan transaction:** A transaction event that can't be associated with a specific keyword or ad.

**pixel:** A transparent, one pixel by one pixel image embedded on a webpage for tracking purposes. Adobe Advertising conversion-tracking tags include either an HTML image pixel or JavaScript to track clicks and their resulting transactions.

**placement:** A location on a display network in which your ads can appear. It can be an entire website, a subset of a website, or an ad position on a specific page.

**portfolio:** A set of ad campaigns, and their associated bid units, that are optimized to a single business objective and a performance target.

**POS:** percentage of spend

**PPC:** See "pay per click."

**property:** See "conversion metric."

**property time:** The time at which an individual conversion event occurs. When an event includes related follow-on events (such as a customer first registering for a free trial and later subscribing to a paid service), each event has its own property time.

## Q-R {#q-r}

**quality score:** A score that an ad network assigns to one of your keywords to determine its bid price and ad position. It's calculated according to the relevancy of the keyword to its associated ad and to the user's search query, the keyword's click-through rate, and other factors.

**redirect URL:** Part of a destination URL that sends the user to another server before, or instead of, the advertiser's landing page.

**return on investment:** (ROI) Revenue minus costs.

**revenue accuracy:** (Advertisers with portfolios) The actual revenue for a portfolio divided by the forecasted revenue. [Model accuracy reports](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indicate the accuracy of the revenue models that are used for optimization.

**revenue model:** (Advertisers with portfolios) Search, Social, & Commerce technology that predicts the conversion rate and estimated return for each bid unit, based on the click data (search and social) or impression data (display) and the advertiser's conversion data.

**revenue model coverage:** (Advertisers with portfolios) The number and/or percentage of bid units in a portfolio with revenue models. Bid units can have revenue models even if they haven't received revenue but have received impressions.

**revenue model half-life:** (Advertisers with portfolios) The number of days before the current date for which the revenue data is considered more recent and therefore more relevant for revenue models.

**ROI:** See "return on investment."

## S-T {#s-t}

**simulation:** (Advertisers with portfolios) Portfolio modeling that estimates the number of clicks and conversions that a portfolio can expect for different levels of spending and corresponding daily budgets, using historical data.

**spend strategy:** (Advertisers with portfolios) The strategy selected to optimize keyword/ad bidding for a portfolio.

**`s_kwcid`:** See "AMO ID."

**tracking URL:** A tracking template or a destination URL with extra parameters added to track information about clicks on the ad. It may include a redirect URL to first send users to a tracking server before redirecting them to the advertiser's landing page.

**transaction:** Any trackable event that occurs online or offline. Multiple transaction events may be tracked together as part of the same transaction or conversion; for example, an online request for information plus a resulting order by telephone might be considered components of a purchase. The terms "transaction" and "conversion" are often used interchangeably. A transaction is represented by a transaction ID, and it has one or more properties associated with it.

**transaction ID:** An advertiser-specified ID that identifies a transaction. When a transaction includes multiple events, they all have the same transaction ID.

**transaction property:** See "conversion."

**transaction time:** The time at which a click or impression is converted to a transaction. When a transaction consists of multiple transaction events (such as when a customer first registers for a free trial and later subscribes to a paid service), the transaction time comes from the first event in the chain (registering for the free trial).

**TSV:** A file format consisting of tab-separated values (CSV).

## U-V {#u-v}

**view-through:** (Display and social ads) An ad impression (or string of impressions) that results in a conversion without the user clicking an ad.

**view-through weight:** (Display and social campaigns only) An advertiser-level setting that specifies the weight to attribute to a view-through conversion relative to the weight attributed to a click-based conversion, as a percentage.

## W-X {#w-x}

**weighted objective:** See "objective."

**weighted revenue:** See "objective value."

**XLS** or **XLSX**: A binary file format for [!DNL Microsoft Office Excel] workbooks.

## Y-Z {#y-z}
