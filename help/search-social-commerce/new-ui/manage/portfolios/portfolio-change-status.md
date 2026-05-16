---
title: (New UI) Change the status of a portfolio
description: Learn how to change the status of a portfolio or delete an inactive portfolio without opening the portfolio settings.
feature: Search Portfolios, Search Optimization
hide: true
---
# (New UI) Change the status of a portfolio

*Beta feature*

You can quickly change a [portfolio's status](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#portfolio-statuses) without opening the full portfolio settings.

To stop gathering cost/click/impression data and revenue data for the relevant campaigns, delete the portfolio. Deleting a portfolio makes it unavailable within Search, Social, & Commerce.

All changes to the portfolio status are logged in the portfolio's change history.

## Optimize, activate, or deactivate a portfolio

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Portfolios]**.

1. Hold the cursor over the portfolio row and click ![Edit](/help/search-social-commerce/assets/edit.png "Edit") next to the [!UICONTROL Portfolio Status].
   
1. Change the status:

   * To activate an inactive or optimized portfolio, select **[!UICONTROL Active]**.

   * To deactivate an active portfolio, select **[!UICONTROL Inactive]**.

   * To optimize (launch) an active portfolio, select **[!UICONTROL Optimized]**.
   
     >[!NOTE]
     >
     >* You can change the status to optimized only if the portfolio is already active and contains at least one active campaign with at least one active ad and keyword/placement.
     >* Before you change the status to optimized, you must implement conversion tracking tags in the advertiser's webpages. In addition, the best practice is to perform a baseline analysis.
     >* When you launch a new portfolio, make sure that the start date is today or later.
     >* Avoid changing the portfolio in the first week after optimization, even though performance is volatile.
     >* Once Search, Social, & Commerce begins optimizing a portfolio, let it manage all future campaign budget and (when applicable) bid change (when applicable). Search, Social, & Commerce will overwrite any changes you make from within the ad network.
     >* You can temporarily set manual bids for any optimized CPC campaign in the portfolio by creating and posting campaign bulksheets. Any bid changes resulting from the posted data are applicable for one day. After that, Search, Social, & Commerce resumes setting bids according to its own optimization strategy.

## Delete an inactive portfolio

You can delete only inactive portfolios. If the portfolio is optimized or active, then you must first change its status to inactive before you have the option to delete it.

1. In the main menu, click **[!UICONTROL Manage] > [!UICONTROL Portfolios]**.

1. Do either of the following:

   * Hold the cursor over the portfolio row and click **[!UICONTROL ...] > [!UICONTROL Delete]**.
   
   * Select the check box next to the portfolio. In the bulk actions toolbar, click ![Delete](/help/search-social-commerce/assets/delete-new.png "Delete").

1. In the confirmation message, click **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [Create a portfolio](portfolio-create.md)
>* [(New UI) Edit a portfolio](portfolio-edit.md)
>* [About portfolios](portfolio-about.md)
