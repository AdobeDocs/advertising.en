---
title: Adobe Advertising support for the California Consumer Privacy Act &#58; Consumer Opt-Out-of-Sale Support
description: Learn about support for capturing consumer opt-out-of-sale requests.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
---
# Adobe Advertising Support for the California Consumer Privacy Act: Consumer Opt-Out of Sale Support

*For Adobe Advertising Demand Side Platform (DSP)*

>[!IMPORTANT]
>
>The contents of this document are not legal advice and are not meant to substitute for legal advice. Consult with your legal counsel for advice concerning the California Consumer Privacy Act.

The California Consumer Privacy Act (CCPA) is California’s new privacy law, which is effective January 1, 2020. CCPA provides California residents new rights regarding their personal information and imposes data protection responsibilities on certain entities who conduct business in California. CCPA provides consumers with the right to access and delete their data as well as the right to opt out of certain activities that qualify as “selling” personal information to a third party.

As a business, you will determine the personal data that Adobe Experience Cloud processes and stores on your behalf.

As your service provider, Adobe Advertising provides support for your business to fulfill its obligations under CCPA that are applicable to the use of Adobe Advertising products and services, including managing consumer requests to access and delete personal information and managing consumer requests to opt out of the sale of personal information.

This document describes how Adobe Advertising Demand Side Platform (DSP), as a service provider, supports the consumer right to opt out of the "sale" of "personal information," as each term is defined by the CCPA. It includes information on how to communicate opt-out-of-sale requests to Adobe Advertising and how to retrieve reports of your organization's opt-out-of-sale requests.

For information about how [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; and [!DNL Advertising DCO] support consumers' personal information access and deletion rights, see [Adobe Advertising Support for the California Consumer Privacy Act: Consumer Data Access and Delete Support](/help/privacy/ccpa/ccpa-access-delete.md).

For more information about the Adobe Privacy services for CCPA, see the [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Communicating Consumer Opt-Out-of-Sale Requests to Adobe Advertising

You can communicate consumer opt-out-of-sale requests by using either:

* a CCPA opt-out-of-sale segment created in Advertising DSP
* the Adobe Experience Platform Privacy Service API

### Method 1: Communicate CCPA Opt-Out-of-Sale Requests Using a [!UICONTROL CCPA Opt-Out-of-Sale] Segment in Advertising DSP

>[!NOTE]
>
>Users remain in CCPA opt-out-of-sale segments indefinitely.

1. Log in to the advertiser's account in Advertising DSP at [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Create a CCPA opt-out-of-sale segment, and implement the segment pixel to capture the opt-out requests](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Method 2: Communicate CCPA Opt-Out-of-Sale Requests Using the Adobe Experience Platform Privacy Service API

*Advertisers assigned an Adobe Experience Cloud organization ID only*

1. Deploy a JavaScript library to retrieve your customer's cookies. The same library, `AdobePrivacy.js`, is used for all Adobe Experience Cloud solutions.

   >[!IMPORTANT]
   >
   >Requests to some Adobe Experience Cloud solutions don't require the JavaScript library, but requests to Adobe Advertising require it.

   You should deploy the library on the webpage from which your customers can submit opt-out-of-sale requests, such as your company's privacy portal. The library helps you retrieve Adobe cookies (namespace ID: `gsurferID`) so that you can submit these identities as part of opt-out-of-sale requests via the Adobe Experience Platform Privacy Service API.

1. Identify your Experience Cloud organization ID and make sure that it's linked to your Adobe Advertising accounts.

   An Experience Cloud organization ID is a 24-character alphanumeric string appended with "@AdobeOrg." Most Experience Cloud customers have been assigned an organization ID. If your marketing team or internal Adobe system administrator doesn't know your organization ID, or isn't sure if it's been provisioned, then contact your Adobe Account Team. You'll need the organization ID to submit requests to the Privacy API using the `imsOrgID` namespace.

   >[!IMPORTANT]
   >
   >Contact your company’s Adobe Advertising representative to confirm that all of your organization's Adobe Advertising accounts &mdash; including [!DNL DSP] accounts or advertisers, [!DNL Search, Social, & Commerce] accounts, and [!DNL Creative] or [!DNL DCO] accounts &mdash; are linked to your Experience Cloud organization ID.

1. Use the Adobe Experience Platform Privacy Service API to [submit opt-out-of-sale requests](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) to Adobe Advertising on behalf of consumers, and to check the status of existing requests.

   See the Appendix below for an example of an opt-out-of-sale request.

   >[!NOTE]
   >
   >If your business has multiple Experience Cloud organization IDs, then you must send separate API requests for each. You can, however make one API request to multiple Adobe Advertising sub-solutions ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], and [!DNL DCO]), with one account per sub-solution.

All of these steps are necessary to receive support from Adobe Advertising. For more information about these and other related tasks you need to perform using the Adobe Experience Platform Privacy Service, and where to find the necessary items, see [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Retrieving Reports of Consumers Who Submitted Opt-Out-of-Sale Requests

Adobe Advertising generates monthly reports of IDs that customers have submitted for opt-out-of-sale requests for the account. Each report is available as a tab-separated text file compressed into GZIP format. The data consolidates requests captured using CCPA opt-out-of-sale segments that were created in Advertising DSP and any submissions made via the Privacy Service API. User IDs captured in CCPA opt-out-of-sale segments are identified by segment and by advertiser. Reports are generated on the first of each month for the previous month. For example, the monthly user list for June is available on July 1.

You can retrieve links to the monthly reports that were created in the previous three months, either from within Advertising DSP or by using the Advertising DSP [!DNL Trafficking API]. Each link is valid for seven days but refreshes each time a customer attempts to retrieve one.

### Method 1: Retrieve Consumer Opt-Out-of-Sale Reports Within Advertising DSP

1. Log in to the advertiser's account in Advertising DSP at [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Retrieve the reports](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Method 2: Retrieve Consumer Opt-Out-of-Sale Reports Using the Advertising DSP [!DNL Trafficking API]

This feature is available to organizations that use the [!DNL Trafficking API]. See the documentation for the [!DNL Trafficking API] for more information.<!-- Add link to API doc once it's published. -->

If your organization doesn't use the [!DNL Trafficking API] but is interested in more information, contact your Adobe Account Team.

## Appendix: Example [!UICONTROL CCPA Opt-Out-of-Sale] Request for Privacy Service API Users

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "adCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["adCloud"],
    "regulation": "ccpa"
}'
```

where:

* `"namespace": "adCloud"` indicates the `adCloud` cookie space, and the corresponding value is the customer’s cookie ID as retrieved from `AdobePrivacy.js`
* `"include": ["adCloud"]` indicates that the request applies to Adobe Advertising
