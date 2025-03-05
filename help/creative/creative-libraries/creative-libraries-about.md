---
title: About your creative libraries
description: Learn about managing the creatives for your ad experiences.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
---
# About your creative libraries

*Closed beta feature*

Your creative libraries allow you to manage the creatives that you'll use in your ad experiences. You can create multiple libraries, each with a set of creatives and *creative bundles*, which are groups of creatives that you can add to an experience as one unit.

Your libraries can include:

* **Individual creatives:** You can include individual creatives directly within ad experiences that don't have defined user targets. You can also use your creatives to create bundles, which you can include in targeted [ad experiences](/help/creative/experiences/experience-about.md).

  * **Standard creatives:** You can upload and manage creatives in [various formats](#creative-creative-formats). For each creative, you specify the default language for each ad with which you associate the creative, the default landing page that opens when a user clicks an ad that includes the creative, and optional labels to use as filters within various views within [!DNL Creative].

  * **Dynamic creatives:** (Existing Adobe Advertising DCO customers only) Administrator users can create dynamically generated creatives by mapping dynamic variables in an ad template to values in a feed file. All users can preview, duplicate, and delete existing dynamic ads.

* **Creatives bundles:** Group creatives into bundles to use across multiple experiences with defined user targets. You can create *standard bundles* that consist of standard ads and *dynamic bundles* that consist of dynamically generated ads. 

## Supported Creative Formats {#creative-creative-formats}

### Formats for Standard Creatives

You can add and manage the following creative types in the [supported creative sizes](creative-sizes.md).

>[!IMPORTANT]
>
>Even if you intend to use HTML5, Flexible HTML5, or third-party creatives for your ad experiences, you must also add image creatives for each creative size you use.
>
>Each experience requires a default image creative for each creative size assigned to the experience. The default image creatives are used when a browser isn't JavaScript-enabled or when the ad server can't personalize the ad because of delays.

#### Flexible HTML5

Flexible HTML5 creatives are HTML5 creatives with all of their images and other attributes as standard HTML tags, which you can edit directly within [!DNL Creative], either within a creative library or within an individual experience (which creates a variation of the original creative). Flexible HTML5 creatives use the Interactive Advertising Bureau (IAB) Technology Laboratory's standard for an [ad portfolio](https://flexibleads.iabtechlab.com/), for which ad format sizes are flexible (rather than fixed) and are based on the ad’s aspect ratio and size range, and for which ads maintain their resolution across devices and publisher sites.

You can<!-- either --> upload flexible HTML5 creatives as ZIP files<!-- or use one of the [provided templates](flexible-html5-templates.md) as a starting point -->. See the [specifications for flexible HTML5 creatives](html5-creative-specification.md).

<!-- Will flattening the view be possible later?
The card view, by default, includes a card for each base flexible HTML5 creative you've uploaded, with the number of creative variations [Delete old description? : an indicator of how many variations of the creative exist]. You can optionally flatten the card view to include separate cards for each base creative and each derivation. The table view is always flattened.


[Example default card view for a flexible creative with variations]()[]add image]
  
[Example card for a flexible creative with one variation]() [add image]

 -->

You can optionally change the default values of the attributes specified in a flexible HTML5 creative. Later, you can specify custom values for the attributes within a specific experience, which creates a variation of the parent creative.

#### HTML5 creatives

You can upload simple or static HTML5 creatives, with all attributes and images specified, as ZIP files. You can't edit any attributes or add images; instead, upload a new ZIP file to add a new creative. See the [specifications for simple and static HTML5 creatives](html5-creative-specification.md).

#### Image creatives

You can include image creatives in GIF, JPEG, JPG, or PNG format. You can upload<!--LATER:   images from your Adobe Experience Manager accounts or --> images from your device or network.

Each ad experience requires a default image creative for each creative size assigned to the experience.

#### Third-party creatives

Enter JavaScript tracking tags for creatives hosted on third-party ad servers. The script varies by ad server; the following is an example:

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

### Format for Dynamic Ads

Administrator users can dynamically generate creatives in static HTML5 and dynamic HTML5 format by mapping dynamic variables in an ad template to values in a feed file. Dynamic creatives may include creatives from your legacy Adobe Advertising Dynamic Creative Optimization (DCO) experiences.

## The [!UICONTROL Creative Libraries] views

See "[Customize your data views](/help/creative/introduction/customize-data-views.md)" for more information about customizing each view.

### The [!UICONTROL Creative Libraries] main view

The [!UICONTROL Creative Libraries] main view shows all of your creative libraries. Data for each library includes the number of experiences to which the library's bundles are assigned, the number of bundles, the number of creatives, the number of creative sizes, the number of default language targets, the creation date, and the last modification date to any element of the library. The table mode also includes a column for the advertiser.

#### Available actions

* Create new libraries

* For each creative library:

  * Edit the library name

  * Open the library to view the creatives and bundles assigned to the library

  * Delete the library

### The [!UICONTROL Creative Libraries] > [!UICONTROL Creatives] views

#### [!UICONTROL Standard Ads]

The [!UICONTROL Standard Ads] tab shows all standard creatives that you've created. Data for each creative includes the creative size, the creative type, and the creation date. The table mode also includes columns for the default language and the default landing page.

##### Available actions

* [Add standard creatives to a library](creative-add-standard.md)

* [Edit a standard creative](creative-edit-standard.md)

* [Preview a standard creative](creative-preview.md)

* [Add standard creatives to standard bundles, and remove standard creatives from a standard bundle](creative-attach-detach-bundles.md)

* [Duplicate standard creatives](creative-duplicate.md)

* [Download standard creatives](creative-download.md)

* [Delete standard creatives](creative-delete.md)

<!-- Add in as separate actions?

add or remove labels, regenerate thumbnails for your creatives. When a creative has child creative variations, you can view the variations within the Card view.

-->

#### [!UICONTROL Dynamic Ads]

The [!UICONTROL Dynamic Ads] tab shows all dynamic creatives that were created dynamically for your creative catalogs, except for any dynamic creatives that you [manually deleted](creative-delete.md) from the [!UICONTROL Dynamic Ads] tab. If you [manually duplicated](creative-duplicate.md) any dynamic creatives since a catalog was last processed, then the list of creatives for that catalog also includes the duplicate creatives.

Data for each creative includes the creative type, the creative size, the number of catalogs to which the creative belongs, and the creation date. The table mode also includes columns for the template through which the creative was generated and the offer count.

>[!NOTE]
>
>Each time a catalog is processed, data is refreshed for the existing dynamic creatives for that catalog.

##### Available actions

The ability to create and edit dynamic creatives is currently available only the Adobe Account Team. However, all users can:

* [Preview dynamic creatives](creative-preview.md)

* [Add dynamic creatives to dynamic bundles, and remove dynamic creatives from a dynamic bundle](creative-attach-detach-bundles.md)

* [Duplicate dynamic creatives](creative-duplicate.md)

* [Delete dynamic creatives](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### The [!UICONTROL Creative Libraries] > [!UICONTROL Bundles] view

The [!UICONTROL Bundles] view shows all of your standard and dynamic bundle containers. You can see the creative names, creative sizes, and languages for the creatives included in each bundle.

#### Available actions

* Add standard and dynamic bundles to a library

* List and preview the creatives in a bundle

* Edit a bundle name

* Add standard creatives to standard bundles, and remove standard creatives from a standard bundle

* Duplicate bundles

* Delete bundles

>[!MORELIKETHIS]
>
>* [Manage creative libraries](/help/creative/creative-libraries/creative-library-manage.md)
>* [Add standard creatives to a creative library](creative-add-standard.md)
>* [Manage creative bundles](bundle-manage.md)
>* [Customize your data views](/help/creative/introduction/customize-data-views.md)
