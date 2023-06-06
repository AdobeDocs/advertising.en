---
title: Format of JavaScript conversion tracking tags version 2
description: Reference the format of JavaScript conversion tracking tags version 2. 
---
# Format of JavaScript conversion tracking tags version 2

The following format is for sites that use HTTPS. For sites that use HTTP, the URLs should begin with "http."

>[!NOTE] 
>
>For information about when to use Version 2 versus Version 3, see the [FAQs on tracking tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
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

where:

* `<ef-userid>` is a unique, numeric user ID that Search, Social, & Commerce assigns to the advertiser.

* `<propertyname>` is the conversion that will be tracked. For example, if you're tracking a conversion called "registration," then the tag would include the parameter `ev_registration=<registration>`, and you would need to pass the actual revenue for each transaction (such as `ev_registration=1`). When multiple properties are tracked, they're joined by an ampersand (`&`), such as `ev_registration=<registration>&ev_sale=<sale>` (for example, `ev_registration=1&ev_sale=12.99`). **Note:**  The property name may not include special characters.

* `<transid>` is a unique transaction ID (such as an actual order ID) that the advertiser generates and passes to identify a transaction. It's included only when the "[!UICONTROL Include unique transaction IDs]" option is selected.

  Search, Social, & Commerce uses the transaction ID to eliminate duplicate transactions with the same transaction ID and property value. The transaction ID is included in the [!UICONTROL Transaction Report], which you can use to validate data within Adobe Advertising with the advertiser's data. **Note:** If the advertiser's data doesn't include a unique ID per transaction, then Search, Social, & Commerce still generates one based on transaction time.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [About Adobe Advertising conversion-tracking tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generate an Adobe Advertising conversion tag](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [FAQs about conversion and page view tracking tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format of JavaScript conversion tracking tags version 2](format-conversion-tag-jsv2.md)
>* [Format of JavaScript conversion tracking tags version 3](format-conversion-tag-jsv3.md)
>* [Format of image conversion tracking tags](format-conversion-tag-image.md)
