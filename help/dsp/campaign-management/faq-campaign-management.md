---
title: FAQs about campaign management
description: Learn more about campaign management, including the latency period for changes and what happens when you make budget changes during a flight.
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
TQID: https://experienceleague.adobe.com/PgO4aktP20KQzNe6SG6Vw7ahvYqHTSISQ10FCum-vQg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
    internal-label: DSP placements
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
    internal-label: DSP Packages
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# FAQs about campaign management

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latency of setting changes

* When you change a placement or package setting, when does the change take effect?

    Settings changes usually take effect immediately but may take up to 12 hours.

    If it's the final day of delivery, make changes early in the day so DSP has plenty of time to recalibrate the package based on the changes. For example, if you change from even pacing to frontload pacing, DSP needs to reassess how to distribute spend throughout the remainder of the flight. Don't make that kind of change if you only have one hour left to deliver on the final day of the flight.

## Budget updates mid-flight

* When you make a change to a placement, how long does DSP take to reallocate the package budget?

    Budget allocation is based on placement performance, which is evaluated using a 14-day average. Changes to a placement result in changes to the budget allocation only when they cause changes in performance during the 14-day average.

    When performance changes occur, DSP reallocates the package budget among the placements accordingly during the next budget optimization cycle, which occurs at about midnight (00:00) in the campaign's time zone.

* How is budget reallocated when a placement is removed from a package and added to another package?

    A placement's entire spend history is attached to the placement and moves with it from package to package.

    When you remove a placement from a package, the package no longer has any history of the placement's spend. The package budget becomes (package budget - removed placement budget) / time interval remaining in flight. The package budget is then allocated to the placements remaining in the package.

    Similarly, if you add the same placement to a different package, DSP considers the placement's spend history when it allocates budget for all placements in the new package.

* How does package pacing change on the last day of a flight?

    On the last day of a flight, the day is shortened from 24 hours to 23 hours so that the package budget isn't exceeded. Also, the package's pacing fill strategy automatically changes to "[!UICONTROL Frontload]," even if it's set to "[!UICONTROL even]." This means 65% of the daily budget should deliver by 11:30 a.m. EST.

>[!MORELIKETHIS]
>
>* [Package settings](/help/dsp/campaign-management/packages/package-settings.md)
>* [Placement settings](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Best practices for setting up performance campaigns](/help/dsp/optimization/campaign-best-practices-performance.md)
