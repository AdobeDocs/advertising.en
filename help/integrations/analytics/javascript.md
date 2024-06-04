---
title: JavaScript Code for [!DNL Analytics for Advertising]
description: JavaScript Code for [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
---
# JavaScript Code for [!DNL Analytics for Advertising]

*Advertisers with Advertising DSP only*

For Advertising DSP, the [!DNL Analytics for Advertising] integration tracks view-through and click-through site interactions. Click-through visits are tracked by the standard Adobe Analytics code on your webpages; the [!DNL Analytics] code captures the AMO ID and EF ID parameters in the landing page URL and tracks them in their respective reserved [!DNL eVars]. You can track view-through visits by deploying a JavaScript snippet in your webpages.

On the first page view of a visit to the site, the Adobe Advertising JavaScript code checks to see if the visitor has previously seen or clicked on an ad. If the user has previously entered the site via a click-through or hasn't seen an ad, then the visitor is ignored. If the visitor has seen an ad and hasn't entered the site via a click-through during the [click lookback window](/help/integrations/analytics/prerequisites.md#lookback-a4adc) set within Adobe Advertising, then the Adobe Advertising JavaScript code either a) uses the [Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) to generate a supplemental ID (`SDID`) or b) uses the Adobe Experience Platform [!DNL Web SDK] `generateRandomID` method to generate a `[!DNL StitchID]`. Either ID is used to stitch data from Adobe Advertising to the visitor’s Adobe Analytics hit. Adobe Analytics then queries Adobe Advertising for the AMO ID and EF ID associated with the ad exposure. The AMO ID and EF IDs are then populated in their respective [!DNL eVars]. These values persist for a designated period (by default, 60 days).

[!DNL Analytics] sends site traffic metrics (such as page views, visits, and time spent) and any [!DNL Analytics] custom or standard events to Adobe Advertising hourly, using the EF ID as the key. These [!DNL Analytics] metrics then run through the Adobe Advertising attribution system to connect the conversions to the click and exposure history.

>[!NOTE]
>
>The Adobe Advertising JavaScript tracking logic occurs on the Adobe side and thus has virtually no impact to the page load time.
>
>In contrast, the logic for the [!DNL DCM] data connector to [!DNL Analytics] (using [!DNL Google Campaign Manager 360]) for Advertising DSP occurs on the client side. Client-side stitching slows down the page load and increases the risk of data loss. This occurs because the [!DNL Analytics] JavaScript must ping [!DNL DoubleClick] and wait for [!DNL DoubleClick] to pass back the last click/impression data to [!DNL Analytics]. When your [!DNL DSP] team sets up the [!DNL DCM] data connector, you must specify how long you're willing to delay the page.

<!--
## Deploying the JavaScript Code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The Standard Code

The standard JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

### Additional Code to Import First-Party Segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5’s technical team will provide a unique tag for your organization to implement on your webpages.
-->

## Deploying the JavaScript Code

The JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

### The Code

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### Where to Place the Code

The [!DNL Analytics for Advertising] JavaScript function must come after the Experience Cloud ID Service but before your Analytics App Measurement code. This ensures that the supplemental ID (`SDID`) or `[!DNL StitchID]` is included in your Analytics call.

![Code placement](/help/integrations/assets/a4adc-code-placement.png)

### Validating Code Deployment

You can perform validation using any packet sniffer type of tool (such as [!DNL Charles], [!DNL Fiddler], or [!DNL Chrome Developer Tools]) by comparing the values of the four IDs between the request going to Adobe Advertising and the request going to [!DNL Analytics], as outlined below.

#### How to Confirm the Code with [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Open [!DNL Chrome Developer Tools] and click the **Network** tab.

1. Load a website page that contains the [!DNL Analytics for Advertising] JavaScript.

1. Filter the [!UICONTROL Network] tab by `last` and review two rows:

    ![Filtering on last](/help/integrations/assets/a4adc-code-validation-filter-last.png)

    * The first row is the call to the JavaScript library and is titled `last-event-tag-latest.min.js`.
    * The second row is the call sending the request to Adobe Advertising. It begins as follows: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

       If you don't see the call to Adobe Advertising, then it might not be the first page view of your visit. For testing purposes, you can remove the cookie so that the next call is the first page view for the corresponding visit:

    1. On the Application tab, find the `adcloud` cookie, and verify that the cookie contains `_les_v` (last visit) with a value of `y` and a UTC epoch timestamp that expires in 30 minutes.
        1. Delete the `adcloud` cookie and refresh the page.

1. (Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code) Filter on `/b/ss` to see the Analytics hit.

    ![Filtering on `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code) Filter on `/interact` to verify that the request payload to the Edge Network contains `advertisingStitchID`.

    ![Filtering on `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Compare the ID values between the two hits. All of the values should be in query string parameters except for the report suite ID in the Analytics hit, which is the URL path immediately after `/b/ss/`.

    | ID | Analytics Parameter | Edge Network | Adobe Advertising Parameter |
    | --- | --- | --- | --- |
    | Experience Cloud IMS Org | `mcorgid` |  | `_les_imsOrgid` |
    | Supplemental Data ID | sdid |  | `_les_sdid` |
    | Stitch ID | stitchId | `advertisingStitchID` under the `_adcloud` property  |  |
    | Analytics Report Suite | The value after `/b/ss/` | | `_les_rsid` |
    | Experience Cloud Visitor ID | mid |  | `_les_mid` |

    If the ID values match, then the JavaScript implementation is confirmed. Adobe Advertising sends the [!DNL Analytics] server any click-through or view-through tracking details if they exist.

#### How to Confirm the Code with [!DNL Adobe Experience Cloud Debugger]

1. Open the [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) on your homepage.
1. Go to the [!UICONTROL Network] tab.
1. In the [!UICONTROL Solutions Filter] toolbar, click [!UICONTROL Adobe Advertising] and [!UICONTROL Analytics].
1. In the [!UICONTROL Request URL - Hostname] parameter row, locate `lasteventf-tm.everesttech.net`.
1. In the [!UICONTROL Request - Parameters] row, audit the signals generated, similar to Step 3 in "[How to Confirm the Code with [!DNL Chrome Developer Tools]](#validate-js-chrome)."
    * (Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code) Make sure the `Sdid` parameter matches the `Supplemental Data ID` in the Adobe Analytics filter.
    * (Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code) Make sure the value of the `advertisingStitchID` parameter matches the `Sdid` sent to the Experience Platform Edge Network.
    * If the code isn't generating, then check to make sure the Adobe Advertising cookie has been removed in the [!UICONTROL Application] tab. Once it's removed, refresh the page and repeat the process.

    ![Auditing [!DNL Analytics for Advertising] JavaScript code in [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising]](overview.md)
>* [Prerequisites and Key Information for Implementing [!DNL Analytics for Advertising]](prerequisites.md)
