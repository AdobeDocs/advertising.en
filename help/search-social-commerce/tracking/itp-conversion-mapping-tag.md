---
title: The Adobe Advertising conversion mapping tag
description: Learn about the JavaScript-based conversion mapping tag for ITP 2.2, which allows Adobe Advertising to track a conversion event that occurs on a page that's not the landing page.
exl-id: 6e2515da-2552-4f19-8344-1dee96cbf706
---
# The Adobe Advertising JavaScript conversion mapping tag

*Advertisers with Adobe Advertising conversion tracking only*

The Adobe Advertising JavaScript-based conversion mapping tag, when used in addition to the Adobe Advertising JavaScript v2 or v3 conversion tracking tag, allows Adobe Advertising to track a conversion event that occurs on a page that's not the landing page. The ITP 2.2 solution stores a user's cookie in local storage in an advertiser-owned iFrame. Local storage can then persist the cookie value from the click downstream to the conversion page.

Use the conversion mapping tag to ensure that Adobe Advertising can track all conversions that occur within Apple Safari and Mozilla Firefox browsers, which limit the persistence of first-party cookies. <!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

To use the conversion mapping tag:

1. [Deploy the conversion mapping tag](#deploy-conversion-mapping-tag).

1. If your organization uses multiple Adobe Experience Cloud Identity Service organization IDs (formerly called IMS Org IDs), then [update your conversion tags](#update-conversion-tags) to include the organization ID.

1. [Validate the tag deployment](#validate-conversion-mapping).

## Deploy the JavaScript conversion mapping tag for ITP 2.2 {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>If you're using the JavaScript conversion mapping tag for ITP 2.0, then replace the existing tag in all conversion pages with one of the following tags.<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* If your organization uses a single organization ID, which is used for your Search, Social, & Commerce account, then use the following tag:

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`
  
  where you replace `{AMO User ID}` with the unique user ID for your Search, Social, & Commerce account. 

* If your organization use multiple organization IDs, then use the following tag:

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`
  
  where:
  
  * you replace the value `{xxxxxx@AdobeOrg}` with the organization ID for which the page's conversions are tracked. Use the same organization ID for all of the conversion pages.
    
  * you replace `{AMO User ID}` with the unique user ID for your Search, Social, & Commerce account. 

* If you're using a tag management system that doesn't support adding the `imsorgid` variable to the script tag, then use the following code instead:

  *If your organization uses a single organization ID:

    ```
    <script>
    window.ad_cloud = window.ad_cloud || {};
    window.ad_cloud.userid = "{AMO User ID}"
    </script>
    <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
    ```
    
    where you replace `{AMO User ID}` with the unique user ID for your Search, Social, & Commerce account. 

  * If your organization use multiple organization IDs:

    ```
    <script>
    window.ad_cloud = window.ad_cloud || {};
    window.ad_cloud.imsorgid = "{xxxxxx@AdobeOrg}"
    window.ad_cloud.userid = "{AMO User ID}"
    </script>
    <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
    ```
    
    where:
  
    * you replace the value `{xxxxxx@AdobeOrg}` with the organization ID for which the page's conversions are tracked. Use the same organization ID for all of the conversion pages.
    
    * you replace `{AMO User ID}` with the unique user ID for your Search, Social, & Commerce account. 

If you don't know the value of your organization ID or your Search, Social, & Commerce user ID, then ask your Adobe Account Manager.

### Examples

```
<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="abc12345@AdobeOrg" userid="99999"></script>`
```

```
<script>
window.ad_cloud = window.ad_cloud || {};
window.ad_cloud.imsorgid = "abc12345@AdobeOrg"
window.ad_cloud.userid = "99999"
</script>
<script src="//www.everestjs.net/static/amo-conversion-mapper.js"></script>
```

### Where to add the tag

Add the tag in any page that could be a landing page from a search click (ideally, on all pages, since landing pages may change over time). It must be loaded before the Adobe Advertising JavaScript v3 conversion tracking tag.

If it's placed within an iframe or container tag, then:

* The iframe should be on same level as the top-level domain.

* The conversion mapping tag should be only one (1) level below the top-level domain.

## Update your JavaScript conversion tags {#update-conversion-tags}

If your organization uses multiple organization IDs, then add the organization ID for which a page's conversions are tracked to your existing JavaScript conversion tags.

If your organization uses one organization ID, this step isn't necessary.

### JavaScript V2 tags

Add the following string at the start of the conversion script tag:

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

where you replace the value `{xxxxxx@AdobeOrg}` with the organization ID for which the page's conversions are tracked.

Example:

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
ef_imsorgid = "abc12345@AdobeOrg";
var ef_event_type="transaction";
var ef_transaction_properties = "ev_property name=<property name>&ev_transid=<transid>";
/*
 * Do not modify below this line
 */
var ef_segment = "";
var ef_search_segment = "";
var ef_userid="ef-userid";
var ef_pixel_host="pixel.everesttech.net";
var ef_fb_is_app = 0;
var ef_allow_3rd_party_pixels = 1;
effp();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property name=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

### JavaScript V3 tags

After `window.EF` is defined, add the following string:

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

where you replace the value `{xxxxxx@AdobeOrg}` with the organization ID for which the page's conversions are tracked.

Example:

```
<script type='text/javascript'>
    (function() {
        var f = function() {
              EF.init({ eventType: "transaction",
                        transactionProperties : "ev_property=<property name>&ev_transid=<transid>",
                        segment : "",
                        searchSegment : "",
                        sku : "",
                        userid : "ef-userid",
                        pixelHost : "pixel.everesttech.net"
                        
                        , allow3rdPartyPixels: 1});
              EF.main();
        };
        window.EF = window.EF || {};
        window.EF.imsorgid ="abc12345@AdobeOrg";
        if (window.EF.main) {
            f();
            return;
        }
        window.EF.onloadCallbacks = window.EF.onloadCallbacks || [];
        window.EF.onloadCallbacks[window.EF.onloadCallbacks.length] = f;
        if (!window.EF.jsTagAdded) {
            var efjs = document.createElement('script'); efjs.type = 'text/javascript'; efjs.async = true;
            efjs.src = 'https://www.everestjs.net/static/st.v3.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(efjs, s);
            window.EF.jsTagAdded=1;
        }
    })();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

## Validate the tag deployment {#validate-conversion-mapping}

Ask your Adobe Account Team to help with validating the conversion mapping tag and the regular conversion tag (if you've updated it).
