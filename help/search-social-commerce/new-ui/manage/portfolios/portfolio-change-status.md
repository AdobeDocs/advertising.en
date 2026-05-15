---
title: (New UI) Change the status of a portfolio
description: Learn how to change the status of a portfolio or delete an inactive portfolio.
feature: Search Portfolios, Search Optimization
hide: true
---
# (New UI) Change the status of a portfolio

*Beta feature*

A portfolio's status can be one of the following:

* **Inactive:** The optimization capability is gathering cost/click/impression data for the relevant campaigns for reporting purposes, but it isn't modeling the data nor optimizing campaign budgets and bids.

* **Active:** The optimization capability is gathering cost/click/impression data and revenue data for the relevant campaigns and is modeling the data, but it isn't optimizing campaign budgets or bids. Activate an inactive portfolio to begin modeling data or downgrade an optimized portfolio to the active state to stop optimization.

* **Optimized:** The optimization capability is gathering cost/click/impression data and revenue data for the relevant campaigns, modeling the data, and optimizing campaign budgets and bids (when relevant) on the designated portfolio start date. Changing the status to optimized is also called launching the portfolio.

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
     >* You can launch a portfolio only if it is already active and contains at least one active campaign with at least one active ad and keyword/placement.
     >* Before you launch a portfolio, you must implement conversion tracking tags in the advertiser's webpages.
     >* Before you launch a portfolio, the best practice is to perform a baseline analysis.
     >* If you're launching a new portfolio, the make sure that the start date is today or later.>* Avoid changing the portfolio in the first week after launch, even though performance is volatile.
     >* Once Search, Social, & Commerce begins optimizing a portfolio, you should let it manage all future bid changes (when applicable). Search, Social, & Commerce will overwrite any changes you make from within the ad network.
     >* After you launch a portfolio, you can temporarily set manual bids for any CPC campaign in the portfolio by creating and posting campaign bulksheets. Any bid changes resulting from the posted data are applicable for one day. After that, Search, Social, & Commerce resumes setting bids according to its own optimization strategy.

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
