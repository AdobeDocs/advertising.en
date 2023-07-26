---
title: Data requirements for data feeds using a transaction ID
description: Reference the data requirements for data feeds using a transaction ID.
exl-id: 67e1cadd-b607-465c-9db6-ca76d8ca84c5
---
# Data requirements for data feeds using a transaction ID

Following are the header fields and corresponding data fields required for each type of feed file.

>[!NOTE]
>* The headers can be in any order as long as the data in the subsequent rows follows the same order. If you don't include a header, then the order of the data rows must be consistent with each feed file.
>* Each line of the feed file must contain data for one transaction, and the transaction must be identified by a transaction ID.

| Header Field/Column Name | Type | Description |
| ---- | ---- | ---- |
| Transaction ID (ev_transid) | Case-sensitive string | The advertiser-generated identifier associated with the transaction. Because the Adobe Advertising conversion-tracking tag is used for the online portions of the transaction, this must be the same as the transaction ID (ev_transid) that Adobe Advertising provided for the earlier part of the transaction. This means that the conversion tag for the online portion of the transaction must include a conversion metric for a unique transaction ID.<br><br>**Note:** Adobe Advertising uses the ID to locate the old transaction data and update it according to an agreed-upon insertion mode (for example, to replace the existing data or to augment it with the new data). |
| Transaction Date | DateTime | The date of the transaction. The format must be consistent for each transaction. |
| Client-specific Conversion | String | A conversion that is being tracked (such as the transaction type or amount). Discuss the conversions to be included with the Adobe Advertising implementation team before starting the feed. |

## Example

The following example file includes data for two conversion metrics (Product and Revenue).

```
Transaction ID,Transaction Date,Product,Revenue
12345,2010-02-17,Coffee,15.00
12346,2010-02-17,Tea,42.00
12347,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [File requirements for conversion feed files](feed-file-requirements.md)
>* [Conversion tracking using a transaction ID feed](/help/search-social-commerce/tracking/feed-transaction-id.md)
