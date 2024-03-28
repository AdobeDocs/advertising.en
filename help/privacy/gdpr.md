---
title: Adobe Advertising Support for the General Data Protection Regulation
description: Learn about the supported data request types, required setup and field values, and examples of API access requests using legacy product IDs and returned data fields
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
---
# Adobe Advertising Support for the General Data Protection Regulation

*For [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; and Adobe Advertising DCO*

>[!IMPORTANT]
>
>The contents of this document are not legal advice and are not meant to substitute for legal advice. Consult with your legal counsel for advice concerning the General Data Protection Regulation.

The General Data Protection Regulation (GDPR), a law in effect May 25, 2018, gives all individuals (data subjects) within the borders of the European Union (EU) control of their personal data and simplifies the regulatory environment for international business. This law applies to all businesses (data controllers) that offer goods or services to, monitor the behavior of, or collect personal data from individuals within the borders of the EU at the time their personal data is processed, regardless of the data controller's business location.

Adobe Experience Cloud acts as a data processor for any personal data it receives and stores on behalf of its customers. As a data controller, you determine the personal data that Adobe Experience Cloud processes and stores on your behalf.

This document describes how [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; Advertising DSP (Demand Side Platform); and [!DNL Advertising DCO] support your data subjects' GDPR data access and deletion rights using the Adobe Experience Platform Privacy Service API and Privacy Service UI.

For more information about what GDPR means for your business, see [GDPR and Your Business](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Supported Data Request Types for Adobe Advertising

Adobe Experience Platform provides the ability for businesses to complete the following tasks:

* Access a data subject's cookie-level data within [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], or [!DNL DCO]; device ID-level data for ads in mobile apps within [!DNL DSP]; or email-level data associated with a Unified ID 2.0 ID within [!DNL DSP].

* Delete cookie-level data stored within [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], or [!DNL DCO] for data subjects using a browser; delete ID-level data stored within [!DNL DSP] for data subjects using apps on mobile devices; or delete hashed email-level data associated with a Unified ID 2.0 ID stored within [!DNL DSP].<!-- stored within DSP? I thought we don't store the email addresses but dump them as soon as they're translated to a universal ID? -->

* Check the status of one or all existing requests.

## Required Setup to Send Requests for Adobe Advertising

To make requests to access and delete data for Adobe Advertising, you'll need to:

1. Deploy a JavaScript library to retrieve and remove your data subject cookies. The same library, `AdobePrivacy.js`, is used for all Adobe Experience Cloud solutions.

   >[!IMPORTANT]
   >
   >Requests to some Experience Cloud solutions don't require the JavaScript library, but requests to Adobe Advertising require it.

   You should deploy the library on the webpage from which your data subjects can submit access and delete requests, such as your company's privacy portal. The library helps you retrieve [!DNL Adobe] cookies (namespace ID: `gsurferID`) so that you can submit these identities as part of access and delete requests via the Adobe Experience Platform Privacy Service API.

   When the data subject asks to delete personal data, the library also deletes the data subject's cookie from the data subject's browser.

   >[!NOTE]
   >
   >Deleting personal data is different than Opt-Out, which stops the targeting of an end user with audience segments. However, when a data subject asks to delete personal data from [!DNL Creative], [!DNL DSP], or [!DNL DCO], the library also sends a request to Adobe Advertising to opt out the data subject from segment targeting. For advertisers with [!DNL Search, Social, & Commerce], we recommend that you provide the data subjects a link to [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), which explains how to opt out of audience segment targeting.

1. Identify your Experience Cloud organization ID and make sure it's linked to your Adobe Advertising accounts.

   An Experience Cloud organization ID is a 24-character alphanumeric string appended with "@AdobeOrg." Most Experience Cloud customers have been assigned an organization ID. If your marketing team or internal [!DNL Adobe] system administrator doesn't know your organization ID, or isn't sure if it's been provisioned, then contact Adobe Customer Care at gdprsupport@adobe.com. You'll need the organization ID to submit requests to the Privacy API using the `imsOrgID` namespace.

   >[!IMPORTANT]
   >
   >Contact your company’s Adobe Advertising representative to confirm that all of your organization's Adobe Advertising accounts &mdash; including [!DNL DSP] accounts or advertisers, [!DNL Search, Social, & Commerce] accounts, and [!DNL Creative] or [!DNL DCO] accounts &mdash; are linked to your Experience Cloud organization ID.

1. Use either the [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (for automated requests) or the [Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (for ad-hoc requests) to submit access and delete requests to Adobe Advertising on behalf of the data subjects, and to check the status of existing requests.

   For advertisers who have a mobile app to interact with data subjects and launch campaigns with DSP, you'll need to download the Privacy-ready Mobile SDKs for Experience Cloud. The Mobile SDKs allow data controllers to set opt-out status flags, retrieve the data subject's device ID (namespace ID: `deviceID`), and submit requests to the Privacy Service API. Your mobile app will require an SDK Version 4.15.0 or greater.

   When you submit a data subject's access request, the Privacy Service API returns a data subject's information based on the specified cookie or device ID, which you then must return to the data subject.

   When you submit a data subject's delete request, the cookie ID or device ID is deleted from the server. For requests to [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], and [!DNL DCO], all cost, click, and revenue data associated with the cookie ID are also deleted from the server.

   >[!NOTE]
   >
   >If your company has multiple Experience Cloud organization IDs, then you must send separate API requests for each. You can, however make one API request to multiple Adobe Advertising sub-solutions ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], and [!DNL DCO]), with one account per sub-solution.

All of these steps are necessary for Adobe Advertising. For more information about these and other related tasks you need to perform using the Adobe Experience Platform Privacy Service, and where to find the items you'll need, see "[Privacy Service overview](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)."

## Required Field Values in Adobe Advertising JSON Requests

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` <*your Experience Cloud organization ID*>
`"users":`  where you replace this with the [cookie-based requests](#gdpr-request-fields-cookie) or the [email-based requests](#gdpr-request-fields-email)<!-- wording? -->.

<!-- Complete this section -->

### Cookie-based Requests {#gdpr-request-fields-cookie}<!-- Header? -->

`"users":`

* `"key":` <*usually the name of the data subject*> 

* `"action":` either `**access**` or `**delete**`

* `"user IDs":`

    * `"namespace": **411**` (which indicates the [!DNL adCloud] cookie space)<!-- The numeric value is actually "namespaceId," not "namespace," per https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix>

    * `"value":` <*the actual data subject’s cookie ID value as retrieved from `AdobePrivacy.js`*>

* `"include": **adCloud**` (which is the [!DNL Adobe] product that applies to the request)

* `"regulation": **gdpr**` (which is the privacy regulation that applies to the request)

## Hashed email-based requests {#gdpr-request-fields-email}<!-- Header? -->

`"users":`

* `"key":` <*usually the name of the data subject*> 

* `"action":` either `**access**` or `**delete**`

* `"user IDs":`

    * `"namespace": **Email_LC_SHA256**` (which indicates the hashed email space)

    * `"type": **standard**`

    * `"value":` <*the actual hashed email value in SHA256*>
    
    * `"namespaceId": **411**` (which indicates the [!DNL adCloud] cookie space)<!-- The numeric value is actually "namespaceId," not "namespace," per https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix>

* `"include": **adCloud**` (which is the [!DNL Adobe] product that applies to the request)

* `"regulation": **gdpr**` (which is the privacy regulation that applies to the request)

## Example of Request Submitted by Data Subject Using an Adobe Advertising User ID Retrieved from `AdobePrivacy.js`

The following example shows one access request for both cookie-based information (with the namespace `411`) and hashed email-based information (with the namespace `Email_LC_SHA256`) for a single user.

```
...
`{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "5AB13068374019BC@AdobeOrg"
      }
    ],
    "users": [
      {
        "key": "John Doe",
        "action": ["access"],
        "userIDs": [
          {
            "namespace": "411",
            "value": "Wqersioejr-wdg",
            "type":"namespaceId",
            "deletedClientSide":false
          },
          {
            "namespace":"Email_LC_SHA256",
            "value":"d78a276e7bb11a62d3c13ea58b9368ba70523cf1d834ffd5c629a1e93def3495",
            "type":"standard",
            "deletedClientSide":false
          }
        ]
      },
    ],
    "include": ["adCloud"],
    "regulation": "gdpr"
}'
```

<!-- old format with just cookie-level data
```

{
    "companyContexts": [
      {
        
{
"companyContexts":[
    {
        "namespace":"imsOrgID",
        "value":"5AB13068374019BC@AdobeOrg"
    }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
 "userIDs":[
      { 
        "namespace":"411",
        "value":"Wqersioejr-wdg",
        "type":"namespaceId",
        "deletedClientSide":false
      },
      {
        "namespace":"Email_LC_SHA256",
        "value":"d78a276e7bb11a62d3c13ea58b9368ba70523cf1d834ffd5c629a1e93def3495",
        "type":"standard",
        "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"gdpr"
}
```
 -->

## Data Fields That Are Returned for Access Requests

The following is an example of an access response for Adobe Advertising.

```
{
    "jobId": "6fc09b53-c24f-4a6c-9ca2-c6076b0842b6",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace": "411",
                "userID":"Wqersioejr-wdg"
            },
            {
                "namespace": "Email_LC_SHA256",
                "type":"standard",
                "value":"d78a276e7bb11a62d3c13ea58b9368ba70523cf1d834ffd5c629a1e93def3495",
                "isDeletedClientSide":false
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```

<!-- old format with just cookie-level data
```
...
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
-->
