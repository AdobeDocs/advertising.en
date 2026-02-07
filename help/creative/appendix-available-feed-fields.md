---
title: Available fields for dynamic ad feed files
description: Learn about the fields you can include in the feed files you use to create dynamic ads.
feature: Creative Dynamic Creatives
exl-id: 9cd3fa29-d4db-4e9f-9ffd-87b44b62a3e2
---
# Appendix: Available fields for dynamic ad feed files

The following feed fields are available on the Advertising Creative backend. You can upload a [feed file](/help/creative/feeds/asset-manage.md) that uses your organization-specific field names. However, before you can create a [catalog](/help/creative/feeds/catalog-manage.md) from your feed file, you must map each field in the feed file to one of the following fields in the [feed template](/help/creative/feeds/feed-template-manage.md) that'll you use to create the catalog.

The only field that must have an equivalent in your feed file is `PART_NUM`.

<!-- Questions:

What are these?
Rank
PROFILE_FILTER fields



Do geo fields need be populated as follows:
Country: 2 Letter country code (example: US)
State: state code_2 letter country code (example: CA_US)
City: City name_State code_2 letter country code (example: San Jose_CA_US)
DMA: DMA _2 letter country code (example: 201_US)
Zipcode: Zip code_2 letter country code (example: 94086_US)


TRUE?   GEO fields(Country/State/City/DMA/Zip), UT fields (UT1/UT2/UT3/UT4/UT5) [do we have an equivalent now?], Filtering fields(F1/F2/F3/F4/F5) can have comma separated values. We can have upto 2K characters.

TRUE FOR CSV AND TSV? character encoding on text format files should be UTF-8 -- If yes, then add that with feed file requirements.

-->

| Field Name | Data Type | Required? |
|------------|-----------|-----------|
| PART_NUM | varchar(64) | YES |
| PRODUCT_NAME | text | NO |
| PRODUCT_URL | text | NO |
| PRICE | decimal(10,2) | NO |
| DISCOUNT_PRICE | decimal(10,2) | NO |
| IMAGE | varchar(1024) | NO |
| IMAGE_HEIGHT | int | NO |
| IMAGE_WIDTH | int | NO |
| IMAGE_1 | varchar(1024) | NO |
| IMAGE_2 | varchar(1024) | NO |
| IMAGE_3 | varchar(1024) | NO |
| IMAGE_4 | varchar(1024) | NO |
| IMAGE_5 | varchar(1024) | NO |
| IMAGE_6 | varchar(1024) | NO |
| IMAGE_7 | varchar(1024) | NO |
| IMAGE_8 | varchar(1024) | NO |
| IMAGE_9 | varchar(1024) | NO |
| IMAGE_10 | varchar(1024) | NO |
| TEXT_1 | text | NO |
| TEXT_2 | text | NO |
| TEXT_3 | text | NO |
| TEXT_4 | text | NO |
| TEXT_5 | text | NO |
| TEXT_6 | text | NO |
| TEXT_7 | text | NO |
| TEXT_8 | text | NO |
| TEXT_9 | text | NO |
| TEXT_10 | text | NO |
| TEXT_11 | text | NO |
| TEXT_12 | text | NO |
| TEXT_13 | text | NO |
| TEXT_14 | text | NO |
| TEXT_15 | text | NO |
| ADDITIONAL_PRICE_1 | decimal(10,2) | NO |
| ADDITIONAL_PRICE_2 | decimal(10,2) | NO |
| ADDITIONAL_PRICE_3 | decimal(10,2) | NO |
| AD_SIZE | varchar(32) | NO |
| RANK | int | NO |
| COUNTRY | text | NO |
| STATE | text | NO |
| CITY | text | NO |
| ZIP | text | NO |
| DMA | text | NO |
| PROFILE_FILTER_1 | text | NO |
| PROFILE_FILTER_2 | text | NO |
| PROFILE_FILTER_3 | text | NO |
| PROFILE_FILTER_4 | text | NO |
| PROFILE_FILTER_5 | text | NO |
| DATAPASS_FILTER_1 | text | NO |
| DATAPASS_FILTER_2 | text | NO |
| DATAPASS_FILTER_3 | text | NO |
| DATAPASS_FILTER_4 | text | NO |
| DATAPASS_FILTER_5 | text | NO |
| AUDIENCE_SEGMENT | text | NO |
| LANGUAGE | text | NO |
| CREATIVE_ATTRIBUTE_1 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_2 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_3 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_4 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_5 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_6 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_7 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_8 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_9 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_10 | varchar(256) | NO |
| IS_DEFAULT | enum | NO |

>[!MORELIKETHIS]
>
>* [Workflows for dynamic ads](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Manage asset files](/help/creative/feeds/asset-manage.md)
>* [Manage feed templates](/help/creative/feeds/feed-template-manage.md)
>* [Manage catalogs](/help/creative/feeds/catalog-manage.md)
