---
title: Troubleshooting Adobe Advertising data in Customer Journey Analytics
description: Learn how to troubleshoot and resolve issues with Adobe Advertising data in Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
---
# Troubleshooting Adobe Advertising data in Customer Journey Analytics

The following are potential issues, their possible causes, and solutions.

## List of all potential symptoms

| Symptom | More information |
| ------- | ---------------- |
| No alloy() calls are visible in the browser network tab | See the section "[Installation and setup issues](#issues-installation-setup)" > "[WebSDK extension doesn't initialize](#websdk-extension-doesn't-initialize)" |
| Console error: alloy isn't defined | See "[Installation and setup issues](#issues-installation-setup)" > "[WebSDK extension doesn't initialize](#websdk-extension-doesn't-initialize)" |
| No interact or collect requests to edge.adobedc.net | See "[Installation and setup issues](#issues-installation-setup)" > "[WebSDK extension doesn't initialize](#websdk-extension-doesn't-initialize)" |
| Requests reach the edge but return 400 or 500 errors | See the section "[Installation and setup issues](#issues-installation-setup)" > "[Datastream not configured or misconfigured](#datastream-not-configured-or-misconfigured)" |
| No data appears in Adobe Analytics or Adobe Advertising reports | See the section "[Installation and setup issues](#issues-installation-setup)" > "[Datastream not configured or misconfigured](#datastream-not-configured-or-misconfigured)" |
| Error in network response: "datastream not found" | See the section "[Installation and setup issues](#issues-installation-setup)" > "[Datastream not configured or misconfigured](#datastream-not-configured-or-misconfigured)" |
| The visitor ID changes between pages | See the section "[Installation and setup issues](#issues-installation-setup)" > "[Identity and ECID issues](#identity-and-ecid-issues)" |
| Advertising audience segments don't match | See the section "[Installation and setup issues](#issues-installation-setup)" > "[Identity and ECID issues](#identity-and-ecid-issues)" |
| The debugger shows that rule conditions aren't met | See the section "[Installation and setup issues](#issues-installation-setup)" > "[Rules or events aren't firing](#rules-or-events-aren't-firing)" |
| The [!UICONTROL Send Event] action never executes | See the section "[Installation and setup issues](#issues-installation-setup)" > "[Rules or events aren't firing](#rules-or-events-aren't-firing)" |
| Changes made in [!DNL Tags] aren't reflected on the live site | See the section "[Installation and setup issues](#issues-installation-setup)" > "[Library build and publishing issues](#library-build-and-publishing-issues)" |
| An extension update was applied, but the old behavior persists | See the section "[Installation and setup issues](#issues-installation-setup)" > "[Library build and publishing issues](#library-build-and-publishing-issues)" |
| The `alloy()` send event call succeeds (with a 200 response), but Adobe Advertising conversion data is missing from reports | See the section "[Installation and setup issues](#issues-installation-setup)" > "[Schema validation issues for Advertising fields](#schema-validation-for-advertising-fields)" |
| The XDM payload in the debugger shows no `_experience.adcloud` object | See the section "[Installation and setup issues](#issues-installation-setup)" > "[Schema validation issues for Advertising fields](#schema-validation-for-advertising-fields)" |
| No view-through or click-through conversions are recorded for the webpage | See the section "[Advertising extension setup issues](#advertising-extension-setup-issues)" |
| `_experience.adcloud` is missing from the Experience Data Model (XDM) payload for click-throughs | See the section "[Advertising extension setup issues](#advertising-extension-setup-issues)" |
| Conversions are confirmed in a debugger tool but don't appear in Adobe Advertising reports | See the section "[Advertising extension setup issues](#advertising-extension-setup-issues)" |

## Installation and setup issues {#issues-installation-setup}

### WebSDK extension doesn't initialize {#websdk-extension-doesn't-initialize}

Symptoms:

* No alloy() calls are visible in the browser network tab
* Console error: alloy isn't defined
* No interact or collect requests to edge.adobedc.net

| Cause | Fix |
| ----- | --- |
| Library not published or in draft state | Go to [Publishing Flow](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) and make sure the library that contains the WebSDK extension is in the approved/published state. |
| Embed code missing or wrong environment | Verify that the [!DNL Tags] embed code on the webpage references the correct environment (Dev/Stage/Prod). Look for the environment in the `<head>` tag for the `//assets.adobedtm.com/...` script tag. |
| Async vs. synchronous load conflict | Make sure that only one [!DNL Tags] embed code is present per webpage. Duplicate embed codes cause race conditions. |
| Content security policy (CSP) blocking | Add `edge.adobedc.net` `and assets.adobedtm.com` to your CSP `connect-src` and `script-src` directives. |

### Datastream not configured or misconfigured {#datastream-not-configured-or-misconfigured}

Symptoms:

* Requests reach the edge but return 400 or 500 errors
* No data appears in Adobe Analytics or Adobe Advertising reports<!-- It's not useful to organize this info by cause, not symptom -->
* Error in network response: "datastream not found"

| Cause | Fix |
| ----- | --- |
| The datastream ID for the tag property is missing or incorrect. | <ol><li>In [!DNL Tags], open the [datastream configuration settings](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) for your tag property.</li><li>Confirm that the [!UICONTROL Datastream] field points to the correct datastream for each environment (development, staging, and production), as well as to the correct scema and dataset.<br><br>Each environment should have its own datastream unless you explicitly share one datastream across all three environments.</li></ol> |
| Datastream services aren't enabled for the tag property. | [Open the datastream settings](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) and make sure that the following services are enabled:<ul><li>Adobe Advertising (for conversion/audience sync)</li><li>Adobe Experience Platform (for profile ingestion)</li></ul> |
| Sandbox mismatch |  Make sure the datastream belongs to the same Adobe Experience Platform sandbox as your schema and dataset. A common mistake is creating a datastream in the production sandbox but pointing schemas to the development sandbox. |

### Identity and ECID issues {#identity-and-ecid-issues}

Symptoms:

* The visitor ID changes between pages
* Advertising audience segments don't match

| Cause | Fix |
| ----- | --- |
| Third-party cookies are blocked | Migrate to first-party CNAME data collection by configuring a first-party domain in the datastream's edge configuration. |
| `idMigrationEnabled` is set to `false` while a legacy `s_ecid` cookie is present | Set `idMigrationEnabled: true` in the WebSDK base configuration to migrate the existing ECID from the `s_ecid` or `AMCV_` cookies. |

### Rules or events aren't firing {#rules-or-events-aren't-firing}

Symptoms:

* The debugger shows that rule conditions aren't met
* The [!UICONTROL Send Event] action never executes

Verify the following:

* The rule is saved and included in the active library build.
* The event type matches the actual page behavior (such as [!UICONTROL Library Loaded] vs. [!UICONTROL DOM Ready] vs. [!UICONTROL Window Loaded]).
* The rule's conditions aren't too restrictive. Test by temporarily removing conditions to isolate the issue.
* The rule order is correct. If multiple rules share the same event, check the rule ordering.
* No JavaScript errors earlier on the page are halting execution. Check the browser console for uncaught exceptions.

### Library build and publishing issues {#library-build-and-publishing-issues}

Symptoms:

* Changes made in [!DNL Tags] aren't reflected on the live site
* An extension update was applied, but the old behavior persists

| Cause | Fix |
| ----- | --- |
| Changes weren't added to a library | In [!UICONTROL Publishing Flow], confirm that your changes were added to a library in the development environment. Go to [!UICONTROL Libraries], open the working library, select **Add All Changed Resources**, then select **Save & Build**. |
| The browser is caching an old library | Do a hard refresh (Ctrl+Shift+R or Cmd+Shift+R), or open the page in an incognito/private window. Clear the browser cache entirely if the issue persists. |
| The embed code is for the wrong environment | Confirm that the embed code on the page is the production embed code if you're testing production behavior. |
| The library build failed silently | Go to [!UICONTROL Publishing Flow] and check whether the library shows a [!UICONTROL Build Failed] state. Open the library and review the build log &mdash; common causes are invalid rule configurations or extension version conflicts. |

### Schema validation issues for Advertising fields {#schema-validation-for-advertising-fields}

Symptoms:

* The `alloy()` send event call succeeds (with a 200 response), but Adobe Advertising conversion data is missing from reports
* The XDM payload in the debugger shows no `_experience.adcloud` object

#### Step 1: Confirm that the [!UICONTROL Advertising] field group is added to the schema

1. Go to Adobe Experience Platform > [!UICONTROL Data Management] > [!UICONTROL Schemas].
1. Open the schema used by your datastream.
1. In the [!UICONTROL Field Groups] panel, confirm that **Adobe Advertising Cloud ExperienceEvent Full Extension** is listed.
1. If it's missing, select **Add**, search for **Adobe Advertising Cloud**, select **Adobe Advertising Cloud ExperienceEvent Full Extension**, then select **Save**.

>[!NOTE]
>Republishing your [!DNL Tags] library isn't required for schema changes alone, but you must re-map the XDM data element in [!DNL Tags] if new fields were added.

#### Step 2: Verify that the required Adobe Advertising fields are present in the schema under `_experience.adcloud.conversionDetails`

| Field path | Type | Description |
| ----- | --- | --- |
| `_experience.adcloud.conversionDetails.trackingCode` | String | Maps the conversion to the originating ad click. Populated from the `s_kwcid` query parameter on the landing page URL. |
| `_experience.adcloud.conversionDetails.trackingIdentity` | String | Stores the unique identity and other details for the tracked view-through or click-through conversion event. Populated from the `ef_id` query parameter on the landing page URL. |

If either field is missing, confirm that the **Adobe Advertising Cloud ExperienceEvent Full Extension** field group was saved to the schema, then refresh the schema editor.

#### Step 3: Confirm that the landing page URL includes query parameters

On an ad click-through, the landing page URL must contain both query parameters, for example:

`https://www.example.com/landing-page?s_kwcid=AL!12345!3!abc123&ef_id=abc123xyz:G:s`

| Missing parameter | Likely cause |
| ----- | --- |
| `s_kwcid` | Auto-tagging isn't enabled in the Adobe Advertising Search or DSP campaign settings. |
| `ef_id` | The landing page URL isn't using an Adobe Advertising tracked redirect, or EF ID appending isn't enabled in the campaign settings. |

#### Step 4: Validate the outbound XDM payload

Open the AEP Debugger or the browser [!UICONTROL Network] tab, filter for `edge.adobedc.net`, and inspect the interact request body. A valid click-through payload looks similar to the following:

```json
{
  "events": [{
    "xdm": {
      "eventType": "advertising.clicks",
      "_experience": {
        "adcloud": {
          "conversionDetails": {
            "trackingCode": "AL!12345!3!abc123",
            "trackingIdentity": "abc123xyz:G:s"
          }
        }
      }
    }
  }]
}
```

If `trackingCode` or `trackingIdentity` are empty or missing:

* The query parameter wasn't present on the page when the rule fired. Check the URL and the rule's event timing.
* The field group is missing from the schema. Revisit the schema steps above.

## [!UICONTROL Advertising] extension setup issues {#advertising-extension-setup-issues}

Symptoms:

* No view-through or click-through conversions are recorded for the webpage.

  To verify if conversions are recorded:

  1. Open the webpage with `ef_id=test&s_kwcid=test` appended to the URL.
  1. Open your browser's code inspection tool (often called [!DNL Inspect]), open the [!DNL Network] tab, and look for an interact call for event_type="advertising.enrichment_ct" from Adobe Experience Platform.
  1. In the Data Collection interface, [open the schema definition](https://experienceleague.adobe.com/en/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas) for the website data you want to collect and confirm that `xdm->_experience->adcloud->conversionDetails->trackingCode` and `trackingIdentities` contain `ef_id` and `s_kwcid`.

* `_experience.adcloud` is missing from the Experience Data Model (XDM) payload for click-throughs.

* Conversions are confirmed in a debugger tool but don't appear in Adobe Advertising reports

| Cause | Fix |
| ----- | --- |
| The `Adobe Advertising` service isn't enabled for the datastream | <ol><li>In [!DNL Tags], open the [datastream configuration settings](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) for your tag property.</li><li>Enable the following services, and save the settings:<ul><li>Adobe Advertising (for conversion/audience sync)</li><li>Adobe Experience Platform (for profile ingestion)</li></ul></ol> |
| The `Adobe Advertising` component isn't enabled for the [!UICONTROL WebSDK] extension | The `Adobe Advertising` component within the WebSDK extension is disabled by default and must be explicitly enabled before any tracking for Adobe Advertising click-throughs or view-throughs is functional, regardless of how the XDM schema or rules are configured.<ol><li>In [!DNL Tags], open the [build options for the property in the Adobe Experience Platform Web SDK configuration settings](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/custom-build-components).</li><li>Enable the **Advertising** component, and save the settings.</li><li>Rebuild and republish the library.</li></ol> |
| Only click-through conversions are recorded; view-through conversions never appear | This is expected default behavior. Once the `Adobe Advertising` component is enabled, click-through tracking is active automatically using the `s_kwcid` and `ef_id` URL query parameters. View-through tracking is disabled by default and requires additional configuration &mdash; see the next row. |
| View-through tracking isn't enabled or configured | <ol><li>Enable the Adobe Advertising service for the datastream</li><ol><li>Go to [!UICONTROL Data Collection] > [!UICONTROL Datastreams] in Adobe Experience Platform and open the datastream used by your [!DNL Tags] property.</li><li>Select **Add Service**, select **Adobe Advertising** and **Adobe Experience Platform**, then select **Save**.</li></ol><li>Configure advertisers in Adobe Advertising DSP</li><ol><li>In [!DNL Tags], go to [!UICONTROL Extensions] > [!UICONTROL Installed] > **Adobe Experience Platform Web SDK** > [!UICONTROL Configure].</li><li>Under the [!UICONTROL Advertiser] section, select an advertiser from the dropdown and enable it. To configure multiple advertisers, select **Add Advertiser**.</li></ol><li>Verify that view-through conversion pixels are firing</li><ol><li>In the AEP Debugger, confirm that the interact call includes `stitchId` under the `xdm.query` field.</li><li>Confirm on the browser [!UICONTROL Network] tab that an event with type `advertising.enrichment` is fired and includes `stitchId` under `xdm.query`.</li></ol></ol> View-through conversions fire only every 30 minutes, regardless of the number of visits. If you don't see an interact call, clear your browser cache and try again. |
| (If no view-through events in Experience Platform after the Viewthrough interact call fires) The advertiser was typed in manually instead of selected from the dropdown | Reselect the advertiser from the [!UICONTROL Advertiser] dropdown instead of entering it manually. |
| (If no view-through events in Experience Platform after the Viewthrough interact call fires) No advertiser ID is sent with the view-through interact call | Confirm that an advertiser is configured and enabled under the [!UICONTROL Advertiser] section of the WebSDK extension configuration, then rebuild and republish the library. |

Before opening a support ticket for [!UICONTROL Advertising] extension setup issues, verify the following:

* The **Adobe Advertising** and **Adobe Experience Platform** services are added to the datastream.
* The **Adobe Advertising** component is enabled in the WebSDK extension configuration.
* The library was rebuilt and republished after enabling the component.
* For click-through tracking, the landing page URL contains `s_kwcid` and `ef_id` on ad click.
* For view-through tracking, an advertiser is configured in Adobe Advertising DSP with the correct advertiser ID.
* The WebSDK extension is version 2.36.0 or later.

## Reporting issues

### Summary reporting

| Symptom | Verification and resolution |
| ----- | --- |
| No summary reporting data is available in Customer Journey Analytics for Advertising DSP or Advertising Search, Social, & Commerce. | <ol><li>Confirm that Customer Journey Analytics Workspace is referencing the correct data view.</li><li>Confirm that the feed from Adobe Advertising to Customer Journey Analytics is enabled. Check with your Adobe Account Team.</li><li>Confirm that your Adobe Advertising dimension/classification/lookup dataset and your summary dataset are included in your Customer Journey Analytics connection.</li><li>Confirm that your Adobe Advertising dimensions and summary metrics are included in your Customer Journey Analytics data view.</li></ol>If you verify all of the above settings but you still don't see summary data, then open a [support ticket](https://experienceleague.adobe.com/home?support-tab=home#support) for your organization. |
| Summary reporting data is available in Customer Journey Analytics for Advertiser 1 but not Advertiser 2. | <ol><li>Confirm that the feed from Adobe Advertising to Customer Journey Analytics is enabled for Advertiser 2. Check with your Adobe Account Team.</li><li>Confirm that the setting "[!UICONTROL Backfill all existing data]" is enabled for your three datasets (dimension/classification/lookup, summary, and event metrics) in your Customer Journey Analytics connection.</li></ol>If you verify all of the above conditions but you still don't see summary data, then open a [support ticket](https://experienceleague.adobe.com/home?support-tab=home#support) for your organization. |
| (Search, Social, & Commerce users) Summary reporting data is available in Customer Journey Analytics for one [!DNL Google Ads], [!DNL Meta Ads], or [!DNL Microsoft Advertising] account but not for another account. | Verify that the feed from Adobe Advertising to Customer Journey Analytics is enabled for the specific ad network account. Check with your Adobe Account Team.<br><br>If the feed is enabled for an account but you still don't see summary data, then open a [support ticket](https://experienceleague.adobe.com/home?support-tab=home#support) for your organization. Include the [!UICONTROL Account ID] for the ad network account. |
| Summary reporting data in Customer Journey Analytics Workspace is different than the data in Advertising DSP or Advertising Search, Social, & Commerce, or summary data is missing for some campaigns and campaign entities. | <ol><li>Confirm that you're using the same date ranges in both [!DNL Workspace] and the Adobe Advertising report.</li><li>Confirm that any filters and segments that are applied in [!DNL Workspace] and the Adobe Advertising report aren't causing differences in data.</li><li>Confirm that the [!UICONTROL Time Zone] for your Customer Journey Analytics data view matches the [!UICONTROL Default Timezone] for your [Advertising DSP account](/help/dsp/admin/user-own-profile-edit.md).</li><li>Confirm that the setting "[!UICONTROL Backfill all existing data]" is enabled for your three datasets (dimension/classification/lookup, summary, and event metrics) in your Customer Journey Analytics connection.</li></ol>If you're sure of a data discrepancy, then open a [support ticket](https://experienceleague.adobe.com/home?support-tab=home#support) for your organization. Include the [!UICONTROL Account ID] for the ad network account. To show evidence of the discrepancy, include screenshots and spreadsheets. Your Adobe Account Team can retroactively fix the data feed to resolve the discrepancy if needed. |

### Event-level reporting

| Symptom | Verification and resolution |
| ----- | --- |
| Conversion data (such as `Page Views`) isn't available for a reporting dimension (such as `Campaign`) in Customer Journey Analytics Workspace. | Verify the following, starting with the items with the fewest verification barriers:<ul><li>Confirm that you're using the correct data view.</li><li>Confirm that the applicable conversion metrics are web/online events, which Adobe Advertising can attribute to dimensions.</li><li>Confirm that Adobe Advertising is tracking click-throughs and view-throughs on the applicable site.</li><li>In the Customer Journey Analytics connection for the classifications dataset, confirm that the values for the [!DNL Key] and [!DNL Matching Key] settings are correct: [!DNL Key]: `Tracking Code` (_customername.adLens2.trackingCode), [!DNL Matching Key]: `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode).</li><li>Confirm that the [!DNL Adobe Advertising] service is added to the Adobe Experience Platform datastream, that the mapped schema for the datastream is `XDM ExperienceEvent Schema`, and that the field group `Adobe Advertising Cloud ExperienceEvent Full Extension` is added to the `XDM ExperienceEvent` schema.</li><li>Confirm that the Adobe Advertising settings are configured correctly in the WebSDK extension and published.</li></ul>If you verify all of the above settings but you still don't see conversion data, then open a [support ticket](https://experienceleague.adobe.com/home?support-tab=home#support) for your organization. Include the [!UICONTROL Account ID] for the ad network account. |

<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

## Validation and debugging tools

### Adobe Experience Platform Debugger

Install the [!DNL Adobe Experience Platform Debugger] extension for [!DNL Chrome]. It provides:

* A real-time view of all WebSDK `alloy()` calls
* Datastream ID and environment validation
* XDM payload inspection
* Edge Network request and response details

Key checks in the debugger:

| Tab | What to check |
| ----- | --- |
| [!UICONTROL Summary] | Confirms that the WebSDK is detected and shows the installed version. |
| [!UICONTROL AEP Web SDK] | Shows each event fired, the full XDM payload, and the edge response. |
| [!UICONTROL Adobe Advertising] | Confirms AMO ID capture and the XDM interact call with the `advertising.enrichment` event type. |

### Browser Network tab

Filter by `edge.adobedc.net` to inspect raw edge requests:

* Request URL: `https://[org-id].data.adobedc.net/ee/v2/interact`
* Method: `POST`
* Status: `200` (healthy), `400` (bad payload), or `500` (server or datastream error)

Check the request payload for:

* The correct `dataStreamId`
* The presence of an `xdm` object with the expected fields
* An `identityMap` with the ECID populated

### Console validation

Check the installed WebSDK version:

```js
window.alloy.version
```

Manually trigger a test event:

```js
alloy("sendEvent", {
  xdm: {
    eventType: "web.webpagedetails.pageViews",
    web: {
      webPageDetails: { name: "Test Page", URL: window.location.href }
    }
  }
}).then(result => console.log("Edge response:", result))
  .catch(err => console.error("Send event error:", err));
```

## Quick reference checklist

Verify the following before opening a support ticket:

* The WebSDK extension is on the latest version.
* The library is published, and the embed code is correct for the environment.
* The datastream ID is set correctly for development, staging, and production.
* All required datastream services are enabled.
* The [!UICONTROL Advertising] component is enabled in the WebSDK extension configuration, and a DSP advertiser ID is configured.
* The XDM schema includes the [!UICONTROL Advertising] field group.
* The [!UICONTROL Send Event] rule includes an identity map and fires on the correct event.
* No CSP or browser privacy settings are blocking edge requests.
* The AEP Debugger confirms that events are reaching the edge.
* No JavaScript errors in the browser console are halting execution.
* The **Adobe Advertising Cloud ExperienceEvent Full Extension** field group is added to the schema.
* `_experience.adcloud.conversionDetails.trackingCode` is present in the schema.
* `_experience.adcloud.conversionDetails.trackingIdentity` is present in the schema.
* The landing page URL contains both `s_kwcid` and `ef_id` on click-through.
* The AEP Debugger confirms that `conversionDetails` is populated in the outbound payload.

## When to escalate

Escalate to your Adobe Account Team or your engineering team if:

* Edge requests return persistent `500` errors after datastream validation.
* [!UICONTROL Advertising] conversions are confirmed in the debugger but don't appear in reports after 24-48 hours.
* A WebSDK version update introduces a regression that wasn't present in the previous version. Include the specific version numbers in the support ticket.

>[!MORELIKETHIS]
>
>* [Overview](overview.md)
>* [Adobe Advertising IDs used by [!DNL Customer Journey Analytics]](ids.md)
>* [Prerequisites](prerequisites.md)
>* [Set up data collection, data transfer, and reporting](set-up.md)
>* [Adobe Advertising metrics and dimensions in Customer Journey Analytics](advertising-data-in-cja.md)
>* (Adobe Analytics users) [Collect historical data for AMO IDs and EF IDs for use in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
