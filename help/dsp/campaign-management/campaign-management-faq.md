---
title: FAQs About Campaign Management
description: Learn more about campaign management, including the latency period for changes and what happens when you make budget changes during a flight.
feature: DSP Packages, DSP Placements
exl-id: 9034ab2c-b8b0-4759-bc87-5f73857bb062
---
# FAQs About Campaign Management

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latency of Setting Changes

* When you change a placement or package setting, when will the change take effect?

    Settings changes usually take effect immediately but may take up to 12 hours.
    
    If it's the final day of delivery, make changes early in the day so DSP has plenty of time to recalibrate the package based on the changes. For example, if you change from even pacing to frontload pacing, DSP needs to reassess how it will distribute spend throughout the remainder of the flight. Don't make that kind of change if you only have one hour left to deliver on the final day of the flight.

## Budget Updates Mid-Flight

* When you make a change to a placement, how long does DSP take to reallocate the package budget?

    Budget allocation is based on placement performance, which is evaluated using a 14-day average. Changes to a placement result in changes to the budget allocation only when they cause changes in performance during the 14-day average.

    When performance changes occur, DSP reallocates the package budget among the placements accordingly during the next budget optimization cycle, which occurs at about midnight (00:00) in the campaign's time zone.

* How is budget reallocated when a placement is removed from a package and added to another package?

    A placement's entire spend history is attached to the placement and moves with it from package to package.
    
    When you remove a placement from a package, the package no longer has any history of the placement's spend. The package budget will become (package budget - removed placement budget) / time interval remaining in flight. The package budget is then allocated to the placements remaining in the package.
    
    Similarly, if you add the same placement to a different package, DSP considers the placement's spend history when it allocates budget for all placements in the new package.

* How does package pacing change on the last day of a flight?

    On the last day of a flight, the day is shortened from 24 hours to 23 hours so that the package budget isn't exceeded. Also, the package's pacing fill strategy automatically changes to "[!UICONTROL Frontload]," even if it's set to "[!UICONTROL even]." This means 65% of the daily budget should deliver by 11:30 a.m. EST.

>[!MORELIKETHIS]
>
>* [Package Settings](/help/dsp/campaign-management/packages/package-settings.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Best Practices for Setting up Performance Campaigns](/help/dsp/optimization/campaign-best-practices-performance.md)
