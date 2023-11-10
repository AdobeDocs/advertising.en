---
title: Using the [!DNL Last Event Service] JavaScript Library with [!DNL Web SDK]
description: Learn the steps to switch from using the [!DNL Analytics] [!DNL visitorAPI] library to the [!DNL Experience Platform] [!DNL Web SDK] library for your [!DNL Analytics for Advertising] implementation.
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
---
# Using the [!DNL Last Event Service] JavaScript Library with Adobe Experience Platform [!DNL Web SDK]

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

If your organization uses the legacy Adobe Analytics `visitorAPI.js` library for data collection, you can optionally switch to using the [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) library (`alloy.js`), which allows you to interact with the various Experience Cloud services through the [!DNL Edge Network].

The [!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript library, as-is, records view-through and click-through events and stitches them to the associated conversions using a supplemental ID (`SDID`). The [!DNL Web SDK] library, however, doesn't supply a [!DNL stitch ID]. To use the [!DNL Web SDK] for [!DNL Analytics for Advertising], you'll need to modify 1) the [!DNL Last Event Service] tag you use on your webpages and 2) your [!DNL Web SDK] `sendEvent` commands accordingly.

## Step 1:  Edit Your [!DNL Last Event Service] Tag to Generate a `[!DNL StitchID]`

In the [!DNL Analytics for Advertising] [!DNL Last Event Service] tag you use on your webpages, add code to generate the `[!DNL StitchID]` using the random ID generator that's bundled in the library.

**Legacy tag:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

**New tag:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id''rsid').generateRandomId();
</script>
```

## Step 2: Use [!DNL Web SDK] to Send the [!DNL StitchID] as XDM Data for [!DNL Analytics]

Insert the following property within your [!DNL Web SDK] `sendEvent` command to send the [!DNL StitchID] to [!DNL Experience Edge] as [!DNL Experience Data Model] (XDM) data for [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] will use the value as an `SDID`.

**Property to add:**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**Example:**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript Code for [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
