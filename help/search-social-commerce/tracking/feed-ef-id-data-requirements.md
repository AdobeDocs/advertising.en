---
title: Data requirements for data feeds using EF IDs
description: Reference the data requirements for data feeds using EF IDs.
exl-id: 15e76f3a-c376-4e7b-b3c8-ca76fd427002
---
# Data requirements for data feeds using EF IDs

Following are the header fields and corresponding data fields required for each type of feed file.

>[!NOTE]
>* The headers can be in any order as long as the data in the subsequent rows follows the same order. If you don't include a header, then the order of the data rows must be consistent with each feed file.
>* Each line of the feed file must contain data for one transaction, and the transaction must be identified by an Adobe Advertising-generated ef_id (token).

| Header Field/Column Name | Type | Description |
| ---- | ---- | ---- |
| EF ID | Case-sensitive string | The ef_id (token) that you captured upon the click for the transaction, which consists of the surfer ID, the click time, and the network type. Don't alter the value. |
| Transaction ID | Case-sensitive string | (Optional but recommended) The advertiser-generated transaction ID. The best practice is to include this for each transaction even though the ef_id is used to track the transaction at the time of redirect. |
| Transaction Date | DateTime | The date of the transaction. The format must be consistent for each transaction. |
| Client-specific Conversion | String | A conversion that is being tracked (such as the transaction type or amount). Discuss the conversions to be included with the Adobe Advertising implementation team before starting the feed. |

## Example

The following example file includes data for two conversion metrics (Product and Revenue).

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [File requirements for conversion feed files](feed-file-requirements.md)
>* [Conversion tracking using an EF ID feed](/help/search-social-commerce/tracking/feed-efid.md)
