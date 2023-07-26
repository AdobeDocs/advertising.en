---
title: FAQs About Custom Reports
description: Learn answers to common questions about performance reports, including troubleshooting data issues.
exl-id: 85707666-7c0f-4aa3-8c91-fb73ef6a5061
---
# FAQs About Custom Reports

## General questions

+++What if the date range for the report begins before report data is available?
The report is generated, but it only includes data for the dates for which data is available. For more information about when data is available for each report type, see "[The Data Used for Reports](data-used-for-reports.md)."
+++

+++What's the difference between click date- and transaction date-based reports?
When you report conversions by transaction date, the data includes transactions whose transaction date occurred during the specified time period. This option is the default setting in basic reports and advanced reports, and it shows you how much revenue was earned within the specified time period.

When you report conversions by click date, the data includes transactions that resulted from a click that occurred during the specified time period. When a portfolio has significant delays between clicks and transactions, this type of reporting shows the historical revenue per click for the portfolio, which gives you an idea of what revenue behaviors to expect over time.

![Report by click date versus report by transaction date](/help/search-social-commerce/assets/click-date-vs-txn-date.png "Report by click date versus report by transaction date")
+++

+++What happens if I change the click lookback window or impression lookback window?
(Advertisers with Advertising pixel-based conversion tracking service only) Data for events resulting from the initial click is collected for a longer or shorter period.

An advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j) determine the number of days after a paid click or a display impression (respectively) occurs in which the event can be attributed to a conversion. Changing a value to a longer or shorter period may be important for advertisers with especially short or long click-to-revenue or display impression-to-revenue periods.

**Best practice:** Make sure that the lookback windows are longer than the click-to-revenue and display impression-to-revenue times for most of your keywords or ads. When they're shorter, some conversions aren't associated with the initial click or impression.
+++

+++How do I know which conversions resulted from a [!DNL Google Ads] ad extension or product listing?
You can see which conversions resulted from a click on a [!DNL Google Ads] ad extension (rather than on the ad itself) or on a product listing by generating a [!UICONTROL Transaction Report]. The [!UICONTROL Link Type] column value shows the type and title of a link that was clicked:

* Product listings are listed as `pla:<product ID>`, such as `pla:8525822`.

* Sitelinks are listed as `sl:<Sitelink text>`, such as `sl:See Current Offers`.
 
  You can also identify a sitelink if you include the [!UICONTROL Tracking URL] column in the report. The [!UICONTROL Tracking URL] for a sitelink includes the attribute `&ev_ltx=sl:<link-name>`.

>[!NOTE]
>
>Conversions from [!DNL Google Ads] locations and phone extensions are included in the data for the ads that they accompany. They aren't reported separately.

+++

+++The "[!UICONTROL Keyword]" column in my report includes a value "(adgroup content) <*ad group name*>."
When the row includes data for content-enabled search campaigns, display campaigns, or social campaigns &mdash; which don't include keywords &mdash; the [!UICONTROL Keyword] column shows the applicable ad group name instead.
+++

+++Because of seasonal or market changes, my reports show atypical data. Will this affect bids once the conditions change?
The optimization capability builds its revenue models for each bid unit daily to ensure that it identifies and immediately responds to trends, and the models incorporate long-term historical data to help predict seasonal performance. The portfolio's revenue model half-life setting<!-- add link to glossary? --> also determines how heavily recent revenue data is weighted. The best practice is to lower the half-life during a period of atypical performance but increase it after the revenue model is adjusted. If you have questions about whether adjusting the half-life is necessary, contact your Adobe Account Team.

If you don't want the data for the period to affect future bids at all, then you can choose to exclude those dates from the model. Contact your Adobe Account Team to exclude the dates.
+++

+++Can I create a report on a specific account property metric, such as [!UICONTROL Device] or [!UICONTROL Objective Name]?
For campaign entity reports ([!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], and [!UICONTROL Product Group Report]), metrics data is dynamically aggregated by the property columns you include in the report. You can optionally remove the key column for the report and include only the property columns for which you want to aggregate data.

For example, if you generate a [!UICONTROL Keyword Report] that includes the [!UICONTROL Ad Group] and [!UICONTROL] Device columns, then, by default, the report aggregates metrics for each keyword by ad group and device type. However, if you remove the [!UICONTROL Keyword] column before you generate the report, then the report dynamically generates metrics for the specified ad groups by device type.

>[!NOTE]
>
>You can't use this feature to aggregate data by label classifications. Any label classification columns in the report are omitted. Instead, use the [Label Classification Report](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## General data issues

+++Reports generated using different attribution rules show different totals.
If you generate a report multiple times using the same report parameters but with different attribution rules, then the data may differ for either of the following reasons:

* Click date-based data may fall outside of the specified date range.
  
  If you use the report parameter "[!UICONTROL Conversions based on click date]," then the specified date range applies to the date of the click instead of the date of the transaction. If the report also uses the attribution rule "First Event" or "Last Event," then the first or last event that led to the conversion may be outside of the specified date range. For example, assume that a user clicked Keyword_1 on April 30, clicked Keyword_2 on May 20, and converted on May 21. If the report uses the "[!UICONTROL First Event]" attribution rule and a date range of May 1-21, then the first event (a click on Keyword_1 on April 30) isn't included in the report. If you run the report with the same date range but using the "[!UICONTROL Last Event]" attribution rule, then the conversion is included in the report because the last click occurred within the specified date range.

* The portfolio filter selection excludes some of the events leading to the conversion.
  
  If you report on a subset of portfolios, then you may not be including the campaigns that included the event to which the conversion was attributed under one of the attribution rules. For example, assume a user clicks Keyword_1 from Portfolio_1, clicks Keyword_2 from Portfolio_2, and then converts. If the report uses the "[!UICONTROL First Event]" attribution rule, then Portfolio_1 must be included for the conversion to be included in the report. However, if the report uses the "Last Event" attribution rule, then Portfolio_2 must be included.

>[!TIP]
>
>If you want to compare conversion totals under different attribution rules, then run reports using the report parameter "[!UICONTROL Conversions based on transaction date]" and select all ad networks or all portfolios. If you set no other filters, the conversion totals should match.

+++

+++Individual data fields are incorrect, although the totals are correct.
This situation can occur when the metric formats use integers:

* If you create a [custom metric](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) with the format *Number w/out Decimal Points* (which shows data as integers) and include it in a view or a report that uses a weighted conversion attribution rule ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], or [!UICONTROL Even Distribution]), then the output is shown in integers, not decimals. In this case, individual data fields may be incorrect, although the totals are correct. For example, if an order is divided evenly between three events, then one order (rather than 0.33 order) is attributed to each of the three events. To resolve the issue, [change the metric format](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) to *Number to 2 Decimal Points*.

* Similarly, if you have a revenue metric that is sent as in integer, then the same issue occurs. (The revenue format is controlled by the conversion tag that submits the data.) To resolve the issue, [create a custom metric](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) consisting solely of the revenue metric and with the format *Number to 2 Decimal Points*, and include it in views and reports rather than the original metric.
+++

+++When click or revenue data is missing, how I prevent it from affecting future bids?
Click data issues occur when Search, Social, & Commerce is out of sync with the ad network. Contact your Adobe Account Team to manually sync the account. If click data is missing for an entire day, then ask your Adobe Account Team to exclude that day from the cost models.

Revenue data issues can occur because of a tracking or feed file issue. Contact your Adobe Account Team to investigate the issue. If revenue data is missing for an entire day, then ask your Adobe Account Team to exclude that day from the revenue models.
+++
  
+++Monetary data is shown in the wrong format.
By default, all monetary data in reports is shown in the format for US dollars (such as 1,000.00). To display the value in the correct currency format (but without any currency symbols in CSV and TSV formats), add the "[!UICONTROL Currency]" column to the report. If the report includes data for accounts with different currencies, then any "[!UICONTROL Total]" monetary values are simply the sum of all numbers in the column, regardless of currency.
+++
  
+++Why do I see decimal values for a conversion metric that should be a natural number (1, 2, and so on)?
You may see decimal values in the following cases:

* If you ran the report using any conversion attribution rule parameter other than [!UICONTROL Last Event] or [!UICONTROL First Event], then the revenue may be split between multiple events in the conversion path.

* In the [!UICONTROL Transaction Report], if multiple [bid units](/help/search-social-commerce/glossary.md#a-b) with different match types have the same transaction ID, then the revenue for the tracking ID is split according to the number of clicks on the specified click date.
+++

## Standard performance metrics

+++Click data is missing from reports.
The following are common reasons for a lack of click data. 
  
| Cause | Detection/Analysis | Resolution |
|---|---|---|
| The process that retrieves click data from the ad account failed. | There is no systematic way to detect this issue, but you may notice that a campaign shows no cost or click information even though the ad account spent money. | Contact Customer Support at &lt;*your Search, Social, & Commerce user account*&gt;@support\.efrontier\.com.<!-- Escaped periods and using HTML code for angle brackets --><br><br>If the data is missing for more than 24 hours, then exclude those dates from the cost forecasts until the data is retrieved. Your Adobe Account Team can exclude the dates. |
| A billing issue between the advertiser and ad network prevents the ad account from spending. | There is no systematic way to detect this issue, but you may notice that a campaign shows no cost or click information. | If you know that an ad account wasn't able to spend because of a billing issue, then exclude those dates from the cost forecasts. Your Adobe Account Team can exclude the dates. |  
+++
  
+++Performance data is different from data in the ad network editor.
When the ad network sends updates to previous data (often because they've attributed click fraud to some clicks), Search, Social, & Commerce doesn't update the data unless there is more than a 5% discrepancy and the Adobe Account Team files a request.

Also, when you compare impression share data aggregated across a date range, the data that Search, Social, & Commerce reports may differ from the data that the ad network reports. This difference is because of how the data is reported by the ad network's API, which Search, Social, & Commerce uses to pull in data. For example, for [!DNL Google Ads] data:

* For most impression share metrics, [!DNL Google Ads] caps either the low or high end of the values reported for values either less than 10% or greater than 90%. Data is reported as 0.0999 for <10% and 0.9001 for >90%

* When there is a mix of capped and uncapped data within the date range, Search, Social, & Commerce aggregates impression share data using the values sent in the API as-is, using 0.0999 for rows with <10% and 0.9001 for rows with >90%. This aggregation could result in a variance from the [!DNL Google Ads] pre-aggregated data because [!DNL Google Ads] can use actual percentage values, like 7% or 97%.
+++

+++Performance data in reports is different from data in [!DNL Google Analytics].
The two systems measure different data, so you should expect to see different data. For example:

* Search, Social, & Commerce (and Google Ads) track clicks, whereas [!DNL Google Analytics] tracks visits per 30-minute browser session. For example, if a user clicks your ad once, clicks the Back button, and then clicks the ad again, then Search, Social, & Commerce records two clicks but [!DNL Google Analytics] records one visit.

* [!DNL Google Analytics] shows all traffic data, whereas Search, Social, & Commerce (and [!DNL Google Ads]) filters invalid clicks (such as excessive, repeated clicks).

* [!DNL Google Analytics] includes click and revenue data for all clicks. Search, Social, & Commerce can't track click and revenue data for ads and keywords with incorrect or missing tracking URLs.
+++

## Conversion metrics

+++My report shows no conversion data.
The report may not include conversion metrics for which conversions occurred.
+++

+++Revenue is missing from reports.

**Advertisers using Adobe Advertising conversion tags**
  
*Possible causes:*
  
* Keywords or ads were added without prefixing the Search, Social, & Commerce click tracking prefix to the tracking templates or destination URLs, or the tracking prefix is incorrect.

* The conversion tracking tag isn't implemented correctly on all applicable webpages or was edited.

* The conversion metrics that Search, Social, & Commerce is tracking are excluded from reports and therefore not visible.

* The revenue parser for the client wasn't implemented.

*Possible solution or work-around:*

1. Verify that the correct columns are included in the reports or data views. If the correct columns aren't available to add, then you or your Adobe Account Team must [make the conversion metrics available to reports](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Verify that the correct conversion tracking tags are implemented on all applicable webpages. If necessary, ask your Adobe Account Team to create a test transaction for each applicable conversion tracking tag and to capture the details of the transaction, such as the `transactionid` and details from the cookie (such as the `trackingid`, `clickid`, and so on).

1. If the [!UICONTROL Auto Upload] option is disabled for the campaign and you've added keywords or ads, then make sure you've generated a tracking template or destination URL that includes Search, Social, & Commerce click redirect tracking for each. Your Adobe Account Team can run an internal report to see if any click-tracking URLs (tracking templates or destination URLs) are missing or malformed.
   
   If necessary, generate tracking by creating a bulksheet file with the correct URLs, and post the file to the appropriate account using the **Generate Tracking URLs** option.

   The destination URL should begin with "http://pixel.everesttech.net" or "https://pixel.everesttech.net."

1. If none of these steps resolves the issue, then [contact Customer Care](/help/search-social-commerce/get-help.md).
   
   If the client hasn't been launched or is newly launched, then Customer Care verifies if a revenue parser has been set up. If the parser is set up, then they verify if Search, Social, & Commerce is receiving any pixel conversions and troubleshoot the issue.

**Advertisers sending conversion data feeds**

*Possible causes:*

* The feed file wasn't delivered, it wasn't completely parsed, or the feed contained orphan transactions.

* The relevant conversion metrics are excluded from reports and therefore not visible.

>[!NOTE]
>
>Data generally doesn't appear in the user interface until 2-4 hours after the feed is received.

*Possible solution or work-around:*

1. Verify that the correct columns are included in the reports or data views. If the correct columns aren't available to add, then you or your Adobe Account Team must [make the conversion metrics available to reports](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Run the [!UICONTROL Portfolio Report]. If it's empty, then run the [!UICONTROL Campaign Report] and [!UICONTROL Search Engine Report] to see if the revenue appears in those reports. If it does, then the campaigns may not be assigned to the appropriate portfolio.

1. Verify that the file was sent to the revenue server, and that the file followed the same format and file-naming convention as previous files.
   
   If the format or file-naming convention changed, then correct the file and resend it.

1. If the file was sent, then [contact Customer Care](/help/search-social-commerce/get-help.md).
   
   Customer Care will check if the file was received and parsed. If the file was processed without errors, then they will check for orphan transactions.
+++
  
+++Some advanced reports don't include conversion data provided by an advertiser feed. 
The [!UICONTROL Geo Distribution Report] and [!UICONTROL Domain Referral Report] use data captured through the Adobe Advertising conversion tracking service and can be generated only for advertisers with the service. The reports don't include conversion data that is tracked outside of the Adobe Advertising conversion tracking system.
+++
  
+++Revenue data is different from the advertiser's own revenue data.

**Advertisers using Adobe Advertising conversion tags**

*Possible causes:*
  
* Search, Social, & Commerce disregards revenue when the cookie is expired or deleted, but the advertiser may consider it valid revenue.

* The traffic to the advertiser’s page came from a bookmark or organic search instead of from an ad.

* The conversion tracking tag isn't implemented correctly on all applicable webpages or was edited.

*Possible solution or work-around:*

1. Go to **[!UICONTROL Insights & Reports] > [!UICONTROL Reports]** and generate a [!UICONTROL Transaction Report]. Compare the transactions that Search, Social, & Commerce received with the advertiser’s data.

1. If some transactions are incorrect or are missing, then make sure that the relevant conversion tracking tag is implemented on all applicable webpages and wasn't edited unless your Adobe Account Team advised you to do so. A tag might be missing or changed if the website was recently updated.
   
   Search, Social, & Commerce expects well-formed URLs (with parameters in name-value pairs) within the `ef_transaction_properties` variable and within the `src` element of the `img` tag.

1. If you can't determine and resolve the issue, then [contact Customer Care](/help/search-social-commerce/get-help.md).

   Customer care will try to identify the missing transactions and to then check for orphan transactions and transactions that didn't come from an ad ("uncorrelated conversions").

**Advertisers with conversion data feeds using `ef_id` values**

See the possible causes and solutions for pixel implementations above.

**Advertisers with conversion data feeds using transaction IDs**

*Possible causes:*

* Search, Social, & Commerce disregards revenue when the cookie expires or is deleted, but the advertiser may consider it valid revenue.

* The traffic to the advertiser’s page came from a bookmark or organic search instead of from an ad.

* An offline conversion was reported before an online transaction occurred with the same transaction ID. The online transaction must occur first.

*Possible solution or work-around:*

1. Go to **[!UICONTROL Insights & Reports] > [!UICONTROL Reports]** and generate a [!UICONTROL Transaction Report]. Compare the transactions that Search, Social, & Commerce received with the advertiser’s feed data.

1. If a transaction in the feed file is missing from the report, then check if an online transaction with the same transaction ID (tracked via the pixel) occurred before the offline conversion.

1. If you can't determine and resolve the issue, then [contact Customer Care](/help/search-social-commerce/get-help.md).

   Customer care will check for data parsing errors and [orphan transactions](/help/search-social-commerce/glossary.md#o-p).

**Advertisers with other types of conversion data feeds**

*Possible causes:*

* Search, Social, & Commerce disregards revenue when the cookie is expired or deleted, but the advertiser may consider it valid revenue.

* The traffic to the advertiser’s page came from a bookmark or organic search instead of from an ad.

* There are [orphan transactions](/help/search-social-commerce/glossary.md#o-p), so Search, Social, & Commerce isn't counting all of the revenue that it should.

* The advertiser validated a Search, Social, & Commerce report against a different set of data than they sent in the feed.

* The transaction IDs (`ev_transid` values) weren't sent, aren't unique, or are incorrect.

* The feed file contains duplicate tracking IDs.

* Errors occurred when the file was parsed.

* The advertiser's de-duping logic differs from the Search, Social, & Commerce logic.

*Possible solution or work-around:*

1. Go to **[!UICONTROL Insights] & [!UICONTROL Reports > Reports]** and generate a [!UICONTROL Transaction Report]. Compare the transactions that Search, Social, & Commerce received with the advertiser’s data.

1. If some transactions are incorrect or are missing, then make sure that a) the feed file contains all required transaction IDs and no duplicate tracking IDs and b) the transaction IDs are unique and correct.

1. If you can't determine and resolve the issue, then [contact Customer Care](/help/search-social-commerce/get-help.md).

   Customer care will check for data parsing errors and orphan transactions.
+++

+++Revenue data is different from data in Adobe Analytics
See [https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html).<!-- change link URL to relative link -->
+++

## Specific reports

+++Should the [!UICONTROL Portfolio Report] show the same figures as the [!UICONTROL Portfolios] view?
The [!UICONTROL Portfolio Report] and the [!UICONTROL Portfolios] view show the same data when all filters for the view, the report parameters, and the data columns for the view and report are the same. For example, if the [!UICONTROL Portfolios] view shows portfolios that are "[!UICONTROL All but inactive]" for the date range "[!UICONTROL Last 7 days]" and with only the default data columns shown, then a [!UICONTROL Portfolio Report] using the default parameters shows identical data. If you change any of the report parameters or use different filters in the [!UICONTROL Portfolios] view, then the data values may be different.
+++

+++The data in my [!UICONTROL Portfolio Report] doesn't match the data in my [!UICONTROL Search Engine Report] or [!UICONTROL Search Engine Account Report].
The [!UICONTROL Portfolio Report] shows data for only the campaigns assigned to the specified portfolios, but the [!UICONTROL Search Engine Report] and [!UICONTROL Search Engine Account Report] may also include data for campaigns that aren't assigned to a portfolio.
+++
  
+++How is the [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] different from the portfolio-level [!UICONTROL Model Accuracy Report]?
(Agency account manager, Adobe account manager, and administrator users only) The [!UICONTROL Forecast Accuracy Report] available from [!UICONTROL Reports] > [!UICONTROL Model Accuracy] provides the same data as the portfolio-level [!UICONTROL Model Accuracy Report] except that you can run it across multiple portfolios and you can change the attribution rule. You also can run and schedule the report using custom parameters, and you can use it to create spreadsheet feeds. In addition, the [!UICONTROL Forecast Accuracy Report] is more accurate than the legacy portfolio-level report because it evaluates revenue accuracy using the historical objectives for the portfolio rather than the current objective, and it more accurately represents data for the applicable time zone.
+++
  
+++Ad-level data isn't available for [!DNL Google Ads] dynamic search ad (DSA), performance max, smart shopping, and [!DNL YouTube] campaigns.
The ad networks don't provide the identifier necessary to attribute revenue to an individual ad for those campaigns. Consequently, ad-level performance data isn’t available for those campaign types in the [!UICONTROL Ads] view or in the [!UICONTROL Ad Variation Report]. Expect discrepancies between the total ad-level data for a campaign and the total data for the campaign.
+++
  
+++In the [!UICONTROL Transaction Report], how do I know which conversion metric is from a data feed or is tracked by the Adobe Advertising tracking pixel?
In a transaction report, you can tell if an included conversion metric was tracked by the Adobe Advertising tracking pixel if you include the custom column "[!UICONTROL Tracking URL]." Tracking URLs with the Adobe Advertising tracking pixel begin with "`http://pixel.everesttech.net`."
+++
  
+++The data in my [!UICONTROL Transaction Report] doesn't match the data in my [!UICONTROL Keyword Report].
When you generate both reports by portfolio, the data is different if you generate the [!UICONTROL Keyword Report] using historical data (that is, based on the portfolio configuration during the specified dates) rather than using data for the current campaigns. When you generate the [!UICONTROL Transaction Report] by portfolio, it includes data for the current campaigns in the portfolio.
+++
  
## Spreadsheet feeds

+++Report output includes a mix of date ranges.
You may see different date ranges if the feed aggregates data using any data aggregation level other than "[!UICONTROL Daily]."

To resolve the issue, update the spreadsheet feed to include data aggregated daily. This task includes updating the report template, generating a report using the template, creating a custom [!DNL Microsoft® Excel] template using the report, and then updating the feed settings to include the new Excel template. For more information, see "[Edit spreadsheet report feed settings](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)."
+++
  
+++A spreadsheet feed results in an Internal Error.
This error may happen if you change the columns in the report template but don't update the [!DNL Microsoft® Excel] template accordingly.

To resolve the issue, update the spreadsheet feed to include the new columns. This task includes updating the report template, generating a report using the template, creating a custom [!DNL Excel] template using the report, and then updating the feed settings to include the new Excel template. For more information, see "[Edit spreadsheet report feed settings](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)."
+++
  
+++When I try to open a spreadsheet feed in [!DNL Excel], [!DNL Excel] reports an "unreadable content" error, and data is removed from the recovered content.
When the [!DNL Microsoft® Excel] template doesn't sort data by start date in ascending order, the spreadsheet feed may include blank rows. In particular, [!DNL Excel] reports the error "Excel found unreadable content in '<*report name*>.xlsx.' Do you want to recover the contents of the workbook? If you trust the source of this workbook, click yes." If you click "Yes," you get the following message: "Removed Records: Cell information from /xl/worksheets/sheet1.xml part," and the spreadsheet feed includes blank rows.

To resolve the issue, edit the [!DNL Excel] template associated with the feed to sort data by [!DNL Start date in Ascending (Oldest to Newest) order], and then upload the updated template via the spreadsheet feed settings. For more information, see "[Edit spreadsheet report feeds](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)."
+++
