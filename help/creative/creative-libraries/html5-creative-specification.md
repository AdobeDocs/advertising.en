---
title: HTML5 creative specification
description: Reference the HTML5 creative specification for Advertising Creative.
feature: Creative Standard Creatives
---
# HTML5 creative specification for Advertising Creative

This document outlines the requirements and API support for HTML5 creatives within [!DNL Creative]. The API allows the development of HTML5 creatives whose attributes can be configured at the time of creative delivery.

## Scope

[!DNL Creative] supports HTML5 banners with non-rich media creatives that appear within set borders on a page. You may use the following types of HTML5 creatives:

<!--Remove to simplify:

* **Simple HTML5:** Supports a single landing page URL that can be configured during creative creation and trafficking.

* **Static HTML5:** Supports up to 5 landing page URLs that can be configured during creative creation and trafficking.

-->

* **HTML5:** Supports up to 5 landing page URLs that can be configured during creative creation and trafficking.

* **Flexible HTML5:** Supports up to 5 landing page URLs that can be configured during creative creation and trafficking, and also allows creative attributes to be modified during creative creation and trafficking.

## Requirements

### Folder and compression requirements

* The creative must be packaged in a ZIP file (.ZIP format). Nested ZIP files aren't supported, so don't include a compressed folder inside the outer compressed folder.

* The ZIP file must contain at least one HTML file &mdash; the main HTML display file &mdash; which includes a reference to the [!DNL Creative] JavaScript library. The main HTML file can be either in the root folder or in a subfolder.

* The main HTML file can be named anything, as long as it doesn't include special characters, although `index.html` is recommended.

* All supporting assets that are needed to render the final creative must be either in the same folder as the HTML display file or in subfolders in the main folder.

* Don't include any files in the creative that aren’t referenced for that creative.

### Inclusion of the Advertising Creative JavaScript file

The main HTML file &mdash; and no other files &mdash; must contain a reference to the JavaScript file `AMOLibrary.js`. Call the file in the first line of the `<head>` section using the following address:

`https://ads.everesttech.net/ads/static/local/AMOLibrary.js`

This file contains functions to ensure that local testing of exit events occurs with no issues.

<!-- Remove to simplify:

### Simple HTML5 creative requirements

#### Support for click-through URLS in simple HTML5

The `<head>` section of the main HTML file must include a JavaScript variable name `clickTag` or `clickTAG`. The value of the variable should be the landing page URL. See the following example.

```
<script type=”text/javascript”>
var clickTag = “http://www.example.com”;
</script>
```

>[!NOTE]
>
>The static URL you include in the HTML5 creative is used for local testing purposes only and will be overwritten. When you upload an HTML5 creative, you'll define the default landing page for the `clickTag` variable. When you assign an uploaded HTML5 creative to an ad experience, you can optionally override the default landing page for the `clickTag` variable, and [!DNL Creative] adds click tracking to the URL when you save the experience.

-->

<!-- Renamed to simplify:
### Static HTML5 creative requirements
-->

### HTML5 creative requirements

#### Support for click-through URLS in static HTML5

##### `amo.registerClick(clkVar, clkUrl)`

Registers the click-through URLs and the associated parameter used to reference each URL (known as the `clickTag`). This informs the [!DNL Creative] ad server where to add click tracking. You can use this API to register up to five click tag variables, each with a corresponding landing page URL.

>[!NOTE]
>
>The static URLs you include in the HTML5 creative are used for local testing purposes only and will be overwritten. When you upload an HTML5 creative, you'll define the default landing page for each `clickTag` variable. When you assign an uploaded HTML5 creative to an ad experience, you can optionally override the default landing page for each `clickTag` variable, and [!DNL Creative] adds click tracking to the URLs when you save the experience.

###### Parameters

* `clkVar` &mdash; The name of the click variable (usually "clickTag"), enclosed in double quotes.

* `clkUrl` &mdash; The landing page URL for this click variable, enclosed in double quotes.

###### Usage

Call `amo.registerClick()` in the `<head>` section of the main HTML file.

###### Example

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

Triggers the exit event, which redirects the user to the landing page configured for the `clickTag`. During local testing, this function alerts developers whether the URL being passed to the function was registered.

###### Parameters

* `clkTag` &mdash; The name of the click variable you use to assign the landing page URL using the `amo.registerClick()` function, enclosed in single quotes.

* `event` &mdash; (Optional) The JavaScript "click" event object. This records the coordinates of clicks, which can be further used to analyze creative performance.

###### Usage

Call `amo.onAdClick()` in the `<body>` section of the main HTML file.

###### Examples

`amo.onAdClick('clickTag')` OR `amo.onAdClick('clickTag',clickEvt)`

### Flexible HTML5 creative requirements

#### Support for click-through URLS in flexible HTML5

##### `amo.registerClick(clkVar, clkUrl)`

Registers the click-through URLs and the associated parameter used to reference each URL (known as the `clickTag`). This informs the [!DNL Creative] ad server where to add click tracking. You can use this API to register up to five click tag variables, each with a corresponding landing page URL.

>[!NOTE]
>
>The static URLs you include in the HTML5 creative are used for local testing purposes only and will be overwritten. When you upload an HTML5 creative, you'll define the default landing page for each `clickTag` variable. When you assign an uploaded HTML5 creative to an ad experience, you can optionally override the default landing page for each `clickTag` variable, and [!DNL Creative] adds click tracking to the URLs when you save the experience.

###### Parameters

* `clkVar` &mdash; The name of the click variable (usually "clickTag"), enclosed in double quotes.

* `clkUrl` &mdash; The landing page URL for this click variable, enclosed in double quotes.

###### Usage

Call `amo.registerClick()` in the `<head>` section of the main HTML file.

###### Example

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

Triggers the exit event, which redirects the user to the landing page configured for the `clickTag`. During local testing, this function alerts developers whether the URL being passed to the function was registered.

###### Parameters

* `clkTag` &mdash; The name of the click variable you use to assign the landing page URL using the `amo.registerClick()` function, enclosed in single quotes.

* `event` &mdash; (Optional) The JavaScript "click" event object. This records the coordinates of clicks, which can be further used to analyze creative performance.

###### Usage

Call `amo.onAdClick()` in the `<body>` section of the main HTML file.

###### Examples

`amo.onAdClick('clickTag')` OR `amo.onAdClick('clickTag',clickEvt)`

#### Support for creative attributes in flexible HTML5

##### `amo.registerAttribute(key, type, value)`

Defines attributes of the creatives that can be changed at the time of creative or experience creation. You can define up to 20 creative attributes that can be configured at the time of creative or experience creation.

>[!NOTE]
>
>The values defined in this method are used for local development only and are not used in live ad serving.

###### Parameters

* `key` &mdash; The alphanumeric name of the attribute. It must begin with an alphabetic character.

* `type` &mdash; The type of attribute (`TEXT` or `IMAGE`).

* `value` &mdash; The value of the attribute for testing. For attributes of type `IMAGE`, the value must be the relative path to the image file.

###### Usage

Call `amo.registerAttribute()` to register one creative attribute, type, and value during testing in local mode. Any image files used as sample values should be packaged in the ZIP file along with the uploaded package.

##### `amo.attributes`

A JSON object to query the creative attribute variable names and values. The object keys will be the attribute names, and the values will be the values of those attributes.

In local testing mode, the key-value pairs are the pairs registered by the `amo.registerAttribute` API. For production, the creative attribute variable names and values must be configured at the time of creative creation and trafficking.

### Creative Content Requirements

Most of the display exchanges available in Advertising DSP have the following creative requirements:

* A solid border must surround all ad images.

* Expanding ads are not allowed.

* The landing page must open in a new window.

* The landing page domain and its subdomains may be no longer than 35 characters. **Note:** The final landing page URLs are defined in the DSP and not in the HTML5 assets themselves.

* Any disclaimers to an ad's offering must be included in the ad itself, and not just on the landing page.

<!-- * (Dynamic HTML5 creatives) Do not use `window.open` to handle clicks in your code. Always use `amo.onDynAdClick` to handle click-throughs. -->

## Example content as a JSON object and array

### Example content as a JSON object

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
}
```

### Example content as a JSON array

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
[{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
},

{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-mobile-720x520.png",
"product_url": "http://adobe.com/"
}

]
```

## Example HTML5 creative

### Example folder structure (after decompression)

* index.html

* /assets (folder)

  * bg.jpg (JPG, PNG, SVG, or GIF image)

### Example HTML file (index.html) for simple HTML5 creatives

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

### Example HTML File (index.html) for static HTML5 creatives

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  amo.registerClick("clickTag2","http://www.example2.com");
  amo.registerClick("clickTag3","http://www.example3.com");
  amo.registerClick("clickTag4","http://www.example4.com");
  amo.registerClick("clickTag5","http://www.example5.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

>[!MORELIKETHIS]
>
>* [Add standard creatives to a creative library](/help/creative/creative-libraries/creative-add-standard.md)
