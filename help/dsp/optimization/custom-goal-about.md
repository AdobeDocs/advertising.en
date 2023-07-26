---
title: About Custom Goals
description: Learn about custom goals to define your success events in packages optimized for the lowest CPA or the highest ROAS.
feature: DSP Optimization
exl-id: 806450b9-ce32-4f5c-a2ac-ba8e435ce36d
---
# About Custom Goals

Custom goals define the success events that an advertiser requires to meet its business objectives. Each package that uses the optimization goals "[!UICONTROL Highest ROAS - Custom Goal]" or "[!UICONTROL Lowest CPA - Custom Goal]" must include a custom goal that will help achieve the overall optimization goal. You can create custom goals as *objectives* in [!DNL Advertising Search, Social, & Commerce].

![custom goals](/help/dsp/assets/objective-goals.png)

Each custom goal consists of one or more conversion metrics and the relative weights of those metrics. The available conversion metrics include all metrics tracked using the Adobe Advertising conversion pixel and through Adobe Analytics.

>[!NOTE]
>
>* [!DNL Analytics] dimensions and segments aren't available for Adobe Advertising optimization.
>* To use Analytics events in DSP, work with your Adobe Account Team to configure an advertiser-level integration.
>* [!DNL Analytics] custom events follow this naming convention: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Example: `custom_event_16_examplersid`

For example, suppose that three conversion metrics are relevant to a specific package in one of your campaigns: "PDF Download" valued at 20 USD, "Email Signup" valued at 30 USD, and "Order Confirmation" valued at 40 USD. If you want to give weight according to the one-time monetary value of the customer action, then the relative weights of the properties would be 1, 2, and 1.5.

See the [best practices for creating custom goals](custom-goal-best-practices.md) for tips on how to configure your custom goals.

Once you [create a custom goal](custom-goal-create.md), you can [assign it to a package](/help/dsp/campaign-management/packages/package-settings.md) for reporting and algorithmic optimization using Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Create a Custom Goal](custom-goal-create.md)
>* [Best Practices for Building a Custom Goal](custom-goal-best-practices.md)
>* [Optimization Goals and How to Use Them](optimization-goals.md)
>* [Package Settings](/help/dsp/campaign-management/packages/package-settings.md)
> * [How DSP Optimizes Your Campaigns](optimization-how-dsp-optimizes-campaigns.md)
