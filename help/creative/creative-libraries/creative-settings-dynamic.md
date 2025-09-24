---
title: Dynamic creative settings
description: Reference the settings for dynamic creatives.
feature: Creative Dynamic Creatives
---
# Dynamic creative settings

<!-- add a description -->

## Dynamic ad settings for static HTML5 ads {#dynamic-ad-settings-static-html5}

<!-- add a description -->

### Basic Details

**[!UICONTROL Advertiser]:** The advertiser for which to create the ads.

**[!UICONTROL Library]:** The creative library in which to create the ads.

**[!UICONTROL Dynamic Ad Name]:** A unique name for the creative.

**[!UICONTROL Ad Template Size]:** The ad dimensions for the ad template from which to create the ad. If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template Type]:** The type of ad template from which to create the ad: *[!UICONTROL Static HTML5]* or *[!UICONTROL Dynamic HTML5]*.<!-- explain more --> If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template]:** The ad template from which to create the ad.

**[!UICONTROL clickURL]:** A valid landing page URL to which users are redirected when they click the ad.

### [!UICONTROL Attributes Details]

The dynamic ad attributes.<!-- do these vary according to the uploaded file?  -->

## Dynamic ad settings for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}

<!-- add a description -->

### Basic Details

**[!UICONTROL Advertiser]:** The advertiser for which to create the ads.

**[!UICONTROL Library]:** The creative library in which to create the ads. If you're creating the ads from within [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], then the library name is already selected and read-only.

**[!UICONTROL Dynamic Ad Name]:** A unique name for the creative.

**[!UICONTROL Ad Template Size]:** The ad dimensions for the ad template from which to create the ad. If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template Type]:** The type of ad template from which to create the ad: *[!UICONTROL Static HTML5]* or *[!UICONTROL Dynamic HTML5]*.<!-- explain more --> If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template]:** The ad template from which to create the ad.

<!-- I don't see this, but check once in production:  **[!UICONTROL All Catalogs]**: Generates ads from all available catalogs for the specified advertiser. -->

**[!UICONTROL Catalogs]**: <!-- (When [!UICONTROL All Catalogs] isn't selected) -->One or more of the specified advertiser's catalogs from which to generate ads.

**[!UICONTROL Content Selection]**: (Optional) Any columns in the feed file for which values must be present to create ads: *[!UICONTROL Profile]*, *[!UICONTROL Geography], *[!UICONTROL Segment], *[!UICONTROL Datapass].  **Note:** These settings works independently from the advanced settings in ad experience settings.

**[!UICONTROL Number of offers (Max 50]:** The number of offers that can be created for each ad.<!-- Clarify this -- is this the frequency cap (max number of times an ad may be served)? -->

### [!UICONTROL Attributes Details]




Identify the names of the columns in the specified catalogs <!-- feed files? --> that correspond to the following attributes.<!-- verify --><!-- will these necessarily all be dynamic?  If static, then no formatting, I guess. --><!-- do these vary according to the uploaded file?  -->

**[!UICONTROL backgroundimage]**: The column in the feed file that represents the `backgroundimage` variable. For dynamic values, use the XXX format <!-- ??? --><!-- Demo shows her using `!{background_image}` -- not sure if the actual column name includes the symbols or if it's just `background_image` but the formatting indicates that we're plugging in cell data to create the ads? --> For a static background image that will be used for all ads created, enter <!-- what? How would you indicate this?-->

<!-- I think we'll be listing the column names from the specified feed file, and we'll accept only specific column names for this attribute, so the user will get a small drop-down list to choose from. -->

**[!UICONTROL description]**: The <!-- default? --> ad description.<!-- used how? -->

**[!UICONTROL ctaText]**: <!-- default? --> The text for the ad's call to action<!-- necessarily a call to action button? -->.

**[!UICONTROL clickUrl]**: The variable that allows click-tracking redirects from the generated<!-- ?? --> ads.<!-- Or is this the default landing page for all ads? --> The default landing page URLs are populated from the uploaded feed file creative unit, but you can change the default URLs.

Note: When you include the creative in an experience, you can replace the default
value for any of the click URLs with a custom landing page URL to generate a derivation
of the base creative.

Note: A click tag allows [!DNL Creative] to assign a tracking code to the ad and report
the click-through data.

