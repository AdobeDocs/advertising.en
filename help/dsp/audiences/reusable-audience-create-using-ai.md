---
title: Create a Reusable Audience Using Generative AI
description: Learn how to create reusable audiences in Adobe Advertising DSP using the AI-assisted audience agent. Describe your target audience in natural-language prompts; the agent suggests third-party segments and builds audience expressions for use as targets or exclusions.
feature: DSP Audiences
hidefromtoc: yes
hide: yes
---
# Create a Reusable Audience Using Generative AI

*Beta feature*

*Prompts in the English language only*

<!-- I thought it was all segment types? -->

<!-- Redo the legacy file to include the new info. It's probably cleanest to keep it as two separate procedures (gen AI and manually) rather than one big, long procedure. -->

Use the AI-assisted audience agent to generate new reusable audiences using all third-party segments that are available to you, according to your stated requirements. You can use your audiences as targets or exclusions for multiple placements.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>This feature is in beta mode and is subject to change. Make sure that the generated audience expression represents the audience you want before creating the audience and using it for your placements.

## Create a Reusable Audience Using Generative AI

1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Above the data table, click **[!UICONTROL Create]**.

1. Enter a unique **[!UICONTROL Audience Name]**.

1. (Optional) Deselect the option to **[!UICONTROL Share with all advertisers in my account]**.

   When you share an audience, the audience becomes available as a target or exclusion to all advertisers within the account. However, the individual segments in the audience are available only to users to which the segments are shared.

1. Click **[!UICONTROL Save]**.

1. Build the audience:

   For users with beta permissions, the AI option is the default. To [assemble the audience yourself](/help/dsp/audiences/reusable-audience-create.md), click the "Switch to manual mode" button at the bottom.

   1. Enter one or more prompts to describe the audience characteristics you want to include and exclude. To submit each prompt, click ![Submit prompt](/help/dsp/assets/submit-prompt.png "Submit prompt").

      For more information, see "[Writing Prompts](#writing-prompts)" and "[Best Practices for Creating an Audience Brief](#audience-brief-best-practices)."

      As the AI agent finds relevent segments, it creates an audience expression based on your criteria. It also asks for your approval before looking for matching segments to assemble the audience.

      You can optionally ignore the request and continue to specify additional audience criteria instead.

   1. When the AI agent presents an audience expression that adequately describes your audience, tell the AI agent to proceed with assembling the audience.

      You can enter "proceed," "okay," "ok," "yes", or another similar word. 

   1. (If necessary) Specify additional criteria. When the AI agent presents an audience expression that meets all of your criteria, tell the AI agent to proceed with assembling the audience.

1. When you're satified with the assembled audience, click **[!UICONTROL Create]** to create the specified audience.

   >[!NOTE]
   >
   >You can't later edit the audience using the AI agent. Instead, [edit the audience expression manually](/help/dsp/audiences/reusable-audience-edit.md).

## Writing Prompts {#writing-prompts}

### What should a prompt include?

* Use clear, descriptive language to describe the target audience.

  In general, prompts are case-insensitive, and punctuation isn't required except to provide clarity.

* Be specific and provide details about all audience characteristics that you want to include and any characteristics that you specifically want to exclude. The more details that you provide, the greater the chance that you'll get the results that meet your needs.

* Identify locations, device types, and data providers to include or to exclude.

* Iteratively provide details to refine your criteria and the generated audience expression before you save the audience.

* Learn about prompting through experimentation.

  The audience agent won't automatically save a generated audience expression as an audience. You can only save an audience by clicking the [!UICONTROL Create] button, which is outside of the prompt area, so you can undo any changes that you don't want to keep.

See "[Best Practices for Creating an Audience Brief](#audience-brief-best-practices)" for further ways to optimize prompts for audiences.

<!-- I think these are happening later:

DSP uses "smart" defaults based on the user's previous audiences (all user-created audiences or only ones created via AI prompting?)

you can use a predefined prompt (fill in the blanks, and some fields might have selectors where you can choose values)

Over time, DSP XXXX defaults [clarify this]

 onsider starting by asking for a general template, which contains placeholder values that you can replace with your desired values. The default template is something like "Create a xxx with NNN xxx."

you can give thumbs up or down to [what exactly?]. Verify what info is carried over from session to session and what starts from scratch.

-->

### What can't you include in a prompt?

* References to existing audience expressions.

* Text in languages besides English.

### Examples of AI agent responses and how to reply

When the AI agent needs a response from you, you can reply using keywords in the request or using common terms that are equivalent.

#### AI agent response asking you a question

`If you are okay with the proposed expression, I can start searching third party segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

Your affirmative replies:  "proceed," "okay," "ok," "yes", or another similar word

You can also ignore the request and continue to specify additional audience criteria instead.

#### AI agent response asking you to choose from multiple options

```
Would you like to:
1) Proceed with this expression,
2) Get maximum reach alternatives, or
3) Modify the expression manually?
```

Your reply:  `1`, `proceed`, `2`, `maximum reach`, and so on.

You can also ignore the request and continue to specify additional audience criteria instead.

## Best Practices for Creating an Audience Brief {#audience-brief-best-practices}

An audience brief is a strategic writeup that defines the target audience for a campaign. A well-crafted brief helps the DSP audience agent identify the most relevant segments to assemble your targetable audience.

### Essential Components of an Effective Audience Brief

#### Audience attributes

Include as many attribute types as possible from the following list in your brief. Be specific about attributes you want to exclude.

<!-- What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **Demographics**

  Includes attributes like age range, gender, marital status, household composition (family size, presence of children, multi-generational households).

* **Socioeconomic Indicators**

  Establishes financial capacity through household income (HHI) bands, education level, occupation/job titles, employment status, and home ownership status.

* **Geographic Parameters**

  Defines location scope including country/countries, region (EMEA, APAC, NA), population density (urban/suburban/rural).

* **Interests & Affinities**

  Identifies passions and preferences such as hobbies (sports, arts, outdoor activities), media consumption patterns, brand affinities, and lifestyle activities (travel, dining, entertainment).

* **Psychographics**

  Captures mindset and values including aspirations (status-seeking, self-improvement), core values (sustainability, innovation, tradition), personality traits (risk-takers, early adopters), and purchase motivations.

* **Behavioral Signals**

  Observable actions including purchase behavior (shopping frequency, channel preferences, brand loyalty), online behavior (website visits, content engagement, social media activity), and offline behavior (store visits, event attendance, memberships).

* **In-Market Intent**

  Identifies purchase readiness through product/service categories being researched, purchase timeline (immediate, near-term, long-term), and relevant life events triggering purchase decisions.

* **Life Stage**

  Current phase understanding including career stage (student, entry-level, mid-career, executive, retired), family stage (newlyweds, new parents, empty nesters), and major life transitions.

### Example of a Well-Structured Audience Brief for a Prospecting Campaign

The following is an example of a strong audience brief for a campaign to drive awareness and trial for a premium meal kit subscription service:

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [Duplicate a Reusable Audience](/help/dsp/audiences/reusable-audience-duplicate.md)
>* [Edit a Reusable Audience](/help/dsp/audiences/reusable-audience-edit.md)
>* [View Details About a Reusable Audience](/help/dsp/audiences/reusable-audience-view-details.md)
>* [Share a Reusable Audience](/help/dsp/audiences/reusable-audience-share.md)
>* [Export a Reusable Audience](/help/dsp/audiences/reusable-audience-export.md)
>* [Copy the Segment Key for a Reusable Audience to the Clipboard](/help/dsp/audiences/reusable-audience-clipboard.md)
>* [Delete a Reusable Audience](/help/dsp/audiences/reusable-audience-delete.md)
