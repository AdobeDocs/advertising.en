---
title: Advertising DSP Macros
description: Reference the available macros for general tracking and to track clicks on third-party display ads.
feature: DSP Ads
exl-id: 7058c988-c544-4a61-84dd-eec4ce88ceba
---
# Advertising DSP Macros

A macro is a short command or shorthand for an instruction and usually follows the format `${MACRO_NAME}`. Macros included in creative code or click-through URLs expand into a longer code string that the ad server can understand. The DSP ad server executes macros when the ad is served or clicked.

Ad server macros are useful for passing important information to DSP or to third-party ad servers. Macros are most commonly used during trafficking of third-party and custom creative code or metadata (such as third-party pixels).

You can manually insert a macro anywhere, such as in a VAST tag, in any URL, or in a DSP or third-party event pixel. However, each DSP client and partner has a different ad tag format, and the macros should be inserted in different spots in the tag accordingly. Each time you work with a new client or partner, ask them for documentation on where to insert the macros in their ad tags that DSP traffics.

## General Tracking Macros

Use general tracking macros across all ad and tag types to pass back specific data, as required.

| Macro | Replacement Description | Type |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | The account ID. | integer |
| `${TM_AD_ID}` | The ad key (adKey). | string |
| `${TM_AD_ID_NUM}` | The ad ID. | integer |
| `${TM_ADVERTISER_ID}` | The advertiser ID. | integer |
| `${TM_CAMPAIGN_ID}` | The campaign key. | string |
| `${TM_CAMPAIGN_ID_NUM}` | The campaign ID. | integer |
|` ${TM_CLICK_URL}` | The redirect URL, which enables ad servers to track and count ad clicks. When the ad is served, if the user clicks it, the macro is activated and the click is recorded and counted for reporting purposes. | string |
|` ${TM_CLICK_URL_URLENC}` | The encoded redirect URL, which enables ad servers to track and count ad clicks. When the ad is served, if the user clicks it, the macro is activated and the click is recorded and counted for reporting purposes. Don't use this macro unless you are creating third-party ads and your vendor requires URL encoding. | string |
| `${TM_FEED_ID}` | The key for the media placement (feedKey). | string |
| `${TM_FEED_ID_NUM}` | The ID for the media placement. | integer |
|` ${TM_MACRO_PLACEMENT_SITE_KEY` | The site key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads.<!-- should map to placement_site_key column of placement_site table --> | string |
| `${TM_PLACEMENT_ID}` | The placement key (cpKey). | string |
| `${TM_PLACEMENT_ID_NUM}` | The placement ID. | integer |
| `${TM_RANDOM}` | Cachebuster: a random number between 1 and 1000000. | long |
| `${TM_SESSION_ID}` | The ID of the session, which corresponds to a single retrieval of the ad tag. | string |
| `${TM_SITE_DOMAIN_URLENC}` | The page subdomain parsed from the URL in the bid request; URL-encoded. Not supported for in-banner, click-to-play ads. | string |
|` ${TM_SITE_NAME}` | The site name for the placement. | string|
| `${TM_SITE_URL_URLENC}` | The URL passed in the bid request; URL-encoded. Not supported for in-banner, click-to-play ads. | string |
| `${TM_SITE_ID_NUM}` | The site ID for the placement. | integer |
| `${TM_TIMESTAMP}` | The Unix timestamp indicating the number of seconds elapsed since midnight (00:00 UTC) on 1 January 1970. | long  |
|` ${TM_VIDEO_DURATION}` | The duration of the ad video in seconds. | integer |

{style="table-layout:auto"}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## Mobile-Specific Macros

| Macro | Replacement Description | Type |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) The platform ID, which corresponds to the device's operating system:<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` when the platform is none of the above</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]) The device model name, URL-encoded. | string |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) The environment in which the ad was served:<ul><li>`a` = mobile application</li><li>`b` = mobile website</li></ul> | string (`a` or `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) The platform ID, which corresponds to the device's operating system:<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` when the platform is none of the above</li></ul> | string |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) The  the device type on which the ad was viewer:<ul><li>`TAB` = tablet</li><li>`PHN` = mobile</li><li>`computer` = computer</li></ul> | string |
| `${UOO}` | ([!DNL Nielsen]) Whether or not the user has opted out of ad tracking:<ul><li>`1` (DNT flag = 1) = the user has opted out of ad tracking</li><li>`0` (DNT flag = 0) = the user has opted in to ad tracking</li></ul> | integer (`0` or `1`) |
| `${TM_BUNDLE}` | The [!DNL iOS] or [!DNL Android] app store bundle ID. Examples: com.zynga.wwf2.free or id804379658 | string |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` indicates if the bidder determines that the bid request comes from the European Union origin and requires GDPR enforcement:<ul><li>`1` = GDPR should be enforced</li><li>`0` = GDPR should not be enforced</li></ul>`gdpr_consent=${GDPR_CONSENT}` is the consent value passed from the supply partner in the inbound bid request:<ul><li>In most cases, this is a base64url-encoded consent string, or daisybit (example: BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA)</li><li>`0` = no consent</li><li>`1` = consent</li></ul> | daisybit or integer |

{style="table-layout:auto"}

## Click Macros for Third-Party Display Ads

To accurately track clicks for ads using third-party display tags, DSP requires a display click macro. Only one version of the macro is required; the relevant macro depends on the type of tag.

| Macro | Replacement Description | Type |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | The redirect URL that enables ad servers to track and count ad clicks in the platform. | string |
| `${TM_CLICK_URL_URLENC}` | The redirect URL that enables ad servers that require URL encoding to track and count ad clicks in the platform. | string |

{style="table-layout:auto"}

DSP automatically inserts display click macros in a third-party display tag when you:

* Export ad tags from an ad server partner <!-- [Needs PM confirmation.] -->
* Bulk upload [!DNL Flashtalking] or [!DNL Google DoubleClick for Advertisers] ad tags directly in DSP

If a click macro is missing when you build a display ad, DSP displays a warning message, which prompts you to manually insert the appropriate display click macro in the correct area of the tag.

## [!DNL Analytics for Advertising] Macros

For additional macros available specifically for [ [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) customers, see "[Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md)" and "[Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md)."

## Troubleshooting Macro Errors

When you add macros to your code, make sure you use the exact syntax of the macro. When validating the macros, DSP checks that the macro exactly matches one of the valid macros.

Errors are generated if characters are missing from the beginning or end of the macro name. For example, you will see an error message if:

* You forget one or more of the characters at the beginning of the macro name, such as `${`. If you don’t include the full syntax, the entry isn’t recognized as a valid macro.
* The macro doesn’t end with a valid set of characters, such as `}`.

>[!MORELIKETHIS]
>
>* [Audio Ad Settings](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Connected TV Ad Settings](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Display Ad Settings](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Mobile Ad Settings](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Native Ad Settings](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Pre-roll Ad Settings](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Universal Video Ad Settings](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
