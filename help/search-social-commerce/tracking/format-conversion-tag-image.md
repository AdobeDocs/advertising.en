---
title: Format of image conversion tracking tags
description: Reference the format of image conversion tracking tags.
exl-id: e23107e1-b719-4572-a471-13e51387465d
feature: Search Tracking
---
# Format of image conversion tracking tags

>[!NOTE] 
>
>For information about when to use image tags versus JavaScript tags, see the [FAQs on tracking tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Non-secure tags for sites with HTTP:

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* Secure tags for sites with HTTPS:

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

where:

* `<ef-userid>` is a unique, numeric user ID that Search, Social, & Commerce assigns to the advertiser.

* `<propertyname>` is the conversion to track. For example, if you're tracking a conversion called "registration," then the tag would include the parameter `ev_registration=<registration>`, and you would need to pass the actual revenue for each transaction (such as `ev_registration=1`). When multiple properties are tracked, they're joined by an ampersand (`&`), such as `ev_registration=<registration>&ev_sale=<sale>` (for example, `ev_registration=1&ev_sale=12.99`). **Note:**  The property name may not include special characters.

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
