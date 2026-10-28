---
title: Create a reusable audience
description: Learn how to create reusable audiences to use as placement targets or exclusions. Create reusable audiences in Adobe Advertising DSP manually or with generative AI in AI Assistant or the All Audiences view.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
TQID: 'https://experienceleague.adobe.com/KhAxVTvMx4yBz3tfDtng3nOur2IodZAFFHMUQM1lKhQ'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: b4dc2b3d-fdb5-55cd-9190-f1076d8563e4
    internal-label: DSP Audiences
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Create a reusable audience

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

You can save and manage reusable audiences, which are groups of audience segments that you can use as targets or exclusions for multiple placements. Reusable audiences can include any first-party and third-party segments that are available to you, and even other saved audiences.

Create audiences using the AI-assisted audience agent in either the unified [AI Assistant](/help/dsp/ai-assistant/ai-assistant-about.md) or in the [!UICONTROL Audiences] > [!UICONTROL All Audiences] view, or create audiences manually.

>[!NOTE]
>
>(Advertisers for whom DSP converts hashed email IDs to LiveRamp RampID segments) First-party RampID segments that aren't attached to an active, scheduled, or paused placement are paused. The segment is noted in the segment list as "Auto paused."

## Generate a reusable audience using generative AI

### Create a reusable audience using AI Assistant

*Beta feature*

*Support for English only*

Give AI Assistant an audience brief or describe the audience characteristics you want to include or exclude in natural-language prompts. In the audience definition, you can refine the optimization criteria, ID types to include, and first-party segments to exclude. Once AI Assistant assembles a list of the matching audience segments, you can refine the segment list before you save the audience.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>This feature is in beta mode and is subject to change. Make sure that the generated audience expression represents the audience you want before saving the audience and using it for your placements.

1. Open AI Assistant:

   * In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**. Above the data table, click **[!UICONTROL Create] > [!UICONTROL Create with AI]**.

   * In the upper right of any page, click ![Agentic Chat](/help/dsp/assets/agent-chat.png "Agentic chat").

1. Define the audience:

   1. Create an initial prompt to define your audience in either of the following ways:

      * Enter your own target audience brief or some of the audience characteristics you want to include and exclude.

      * To see examples of target audience briefs and optionally copy one to use:
   
        1. Click **[!UICONTROL Build]** to expand the section.
     
        1. (Optional) To copy the text of an example audience brief into the prompt box:
     
           1. Click the example.
        
           1. (Optional) Edit the text to suit your needs. 
      
      See "[Write prompts and respond to the audience agent](#writing-prompts)" and "[Best practices for creating an audience brief](#audience-brief-best-practices)."

   1. To submit the prompt, click ![Submit prompt](/help/dsp/assets/submit-prompt.png "Submit prompt").

      You can ask multiple questions in one prompt, but only one prompt at a time. Wait for a response before you can send another prompt.

      A panel opens to the side, with the audience definition in the [!UICONTROL Step 1: Audience Definition] tab. The definition includes all defined audience filters, optimization criteria (including device ID types and universal ID types to include), and any of your first-party segments to exclude. If you didn't specify limitations, then segments are based on optimizing for the highest volume, including all device type ID types and universal IDs, and including all of your first-party audiences.
   
      When applicable, AI Assistant suggests additional audience filters to help you create a more effective audience brief. You can accept or reject the suggestions.
   
   1. (Optional) Refine the audience definition:
   
      * To change the optimization criteria between the *[!UICONTROL Highest volume]* to *[!UICONTROL Lowest cost]*, prompt AI Assistant to do it or click ![Edit](/help/dsp/assets/edit-ai.png "Edit") next to **[!UICONTROL Criteria]**, select the criteria, and then click **[!UICONTROL Apply]**.

      * To change between including all ID types (including all device type ID types and universal IDs) and only specific ID types, prompt AI Assistant to do it or click ![Edit](/help/dsp/assets/edit-ai.png "Edit") next to **[!UICONTROL ID type]**, select the ID types to include, and then click **[!UICONTROL Apply]**.

      * To exclude any of your first-party segments, prompt AI Assistant to do it or click ![Edit](/help/dsp/assets/edit-ai.png "Edit") in the **[!UICONTROL First-party segments to exclude]** section, select any segments you want to exclude for the audience, and then click **[!UICONTROL Apply]**.

      * Submit additional prompts as needed to describe the audience characteristics you want to include and exclude. To submit each prompt, click ![Submit prompt](/help/dsp/assets/submit-prompt.png "Submit prompt").

1. When the audience definition meets your criteria, specify the segments to include:

   1. Prompt AI Assistant to search for matching segments. You can say "ok," "go," "continue," "search," or any relevant term or phrase.

      The [!UICONTROL Step 2: Audience Segments] tab shows the proposed audience name, the audience size and distribution, the Boolean audience expression, and a list of the included audience segments grouped by characteristic.

   1. (Optional) In the [!UICONTROL Audience segments] section at the bottom, do any of the following:

      * To expand each group of audience segments, click **[!UICONTROL >]** next to the count.
      
      * To copy the segment IDs of the included audience segments to your clipboard, click **[!UICONTROL Copy rule]**.

      * To remove segments from the audience, prompt AI Assistant to do it or click ![Edit](/help/dsp/assets/edit-ai.png "Edit"), deselect any segments you want to remove from the audience, and then click **[!UICONTROL Apply]**.

1. When you're satisfied with the assembled audience, click **[!UICONTROL Save Audience]** to create the specified audience.

   >[!NOTE]
   >
   >To edit the audience later, [edit the audience expression manually](/help/dsp/audiences/reusable-audience-edit.md).

### Create a reusable audience using the audience agent from the [!UICONTROL Audiences] > [!UICONTROL All audiences] view

*Beta feature*

*Support for English only*

Give the audience agent an audience brief or natural-language prompts describing the audience characteristics you want to include and exclude.

>[!NOTE]
>
>This feature is in beta mode and is subject to change. Make sure that the generated audience expression represents the audience you want before saving the audience and using it for your placements.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Above the data table, click **[!UICONTROL Create]**.

1. In the [!UICONTROL New Audience] settings:

   1. Enter a unique **[!UICONTROL Audience Name]**.

   1. (Optional) Deselect the option to **[!UICONTROL Share with all advertisers in my account]**.

      When you share an audience, the audience becomes available as a target or exclusion to all advertisers within the account. However, the individual segments in the audience are available only to users to which the segments are shared. For example, if you share an audience containing Adobe Analytics segments with an advertiser who isn't mapped to the same [!DNL Analytics] account, then the segment isn't previewed in that audience for that advertiser. Only the segments available to that advertiser are previewed in the audience.

   1. Click **[!UICONTROL Save]**.

1. Build the audience:

   1. Enter one or more prompts to describe the audience characteristics you want to include and exclude. To submit each prompt, click ![Submit prompt](/help/dsp/assets/submit-prompt.png "Submit prompt").

      For more information, see "[Write prompts and respond to the audience agent](#writing-prompts)" and "[Best practices for creating an audience brief](#audience-brief-best-practices)."

      When applicable, the agent suggests additional segment filters to help you create a more effective audience brief. You can accept or reject the suggestions.

      As the audience agent finds relevant segments, it creates a Boolean audience expression based on your criteria. It also asks for your approval before looking for matching segments to assemble the audience. You can optionally ignore the request and continue to specify additional audience criteria instead.

   1. When the audience agent presents an audience expression that adequately describes your audience, tell the audience agent to proceed with assembling the audience.

      You can enter "proceed," "okay," "ok," "yes," or another similar word. The agent lists all suggested segments for each trait (such as "Parents"). To see details about the individual segments suggested for a trait, expand the trait.

   1. (If necessary) Specify additional criteria. When the audience agent presents an audience expression that meets all of your criteria, tell the audience agent to proceed with assembling the audience.

      To assemble the audience, enter "proceed," "okay," "ok," "yes," or another similar word. The agent lists all suggested segments for each trait (such as "Parents"). To see details about the individual segments suggested for a trait, expand any trait.

1. When you're satisfied with the assembled audience, click **[!UICONTROL Create]** to create the specified audience.

   >[!NOTE]
   >
   >To edit the audience later, [edit the audience expression manually](/help/dsp/audiences/reusable-audience-edit.md).

### Write prompts and respond to the audience agent {#writing-prompts}

<!-- Change heading level for this whole section to fit under AI procedure -->

#### Guidelines for writing audience prompts

* Use clear, descriptive language to describe the target audience.

  * You can enter complete sentences or a string of characteristics. Punctuation isn't required except when necessary for clarity.

  * In general, prompts are case-insensitive.
  
  * The audience agent recognizes most common synonyms.

* Be specific:

  * Provide details about all audience characteristics that you want to include and any characteristics that you specifically want to exclude. Providing more details increases the likelihood of obtaining results that meet your needs.

  * Identify locations, device types, and data providers to include or to exclude.

  You always have a chance to edit the audience filters, optimization criteria, first-party segments to exclude, and the final segment list before you save the audience. Proving full details to start shortens the process.

* Iteratively provide details to refine your criteria and the generated audience expression before you save the audience.
  
* The audience agent won't automatically save a generated audience expression as an audience. You can only save an audience by clicking the [!UICONTROL Save Audience] or [!UICONTROL Create] button, which are outside of the prompt area, so you can undo any changes that you don't want to keep.

See "[Best practices for creating an audience brief](#audience-brief-best-practices)" for further ways to optimize prompts for audiences.

<!--
Consider starting by asking for what you should include.

you can give thumbs up or down to [what exactly?].

Verify what info is carried over from session to session and what starts from scratch.

-->

#### Prompt limitations

* References to existing audiences.

* Text in languages besides English.

#### How to respond to the audience agent

When the audience agent needs a response from you, you can reply using keywords in the request or using common synonyms.

##### Confirm whether to proceed

`If you are okay with the proposed expression, I can start searching segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

Your affirmative replies:  "proceed," "okay," "ok," "yes," or another similar word

You can also ignore the request and continue to specify additional audience criteria instead.

##### Choose from suggested options

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

Your reply:  `1`, `proceed`, `2`, `maximum reach`, and so on.

You can also ignore the request and continue to specify additional audience criteria instead.

### Best practices for creating an audience brief {#audience-brief-best-practices}

An audience brief is a strategic writeup that defines the target audience for a campaign. A well-crafted brief helps the DSP audience agent identify the most relevant segments to assemble your targetable audience.

#### Components of an effective audience brief

Include as many audience attribute types as possible from the following list in your brief. Be specific about attributes you want to exclude.

<!--
 What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **Demographics**

  Includes attributes like age range, gender identity, marital status, household composition (family size, presence of children, multi-generational households).

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

#### Example of a well-structured audience brief for a prospecting campaign

The following is an example of a strong audience brief for a campaign to drive awareness and trial for a premium meal kit subscription service:

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

## Manually create a reusable audience

1. In the main menu, click **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Above the data table, click **[!UICONTROL Create] > [!UICONTROL Create manually]**.

1. In the [!UICONTROL New Audience] settings:

   1. Enter a unique **[!UICONTROL Audience Name]**.

   1. (Optional) Deselect the option to **[!UICONTROL Share with all advertisers in my account]**.

      When you share an audience, the audience becomes available as a target or exclusion to all advertisers within the account. However, the individual segments in the audience are available only to users to which the segments are shared. For example, if you share an audience containing Adobe Analytics segments with an advertiser who isn't mapped to the same [!DNL Analytics] account, then the segment isn't previewed in that audience for that advertiser. Only the segments available to that advertiser are previewed in the audience.

   1. Click **[!UICONTROL Save]**.

1. Click the **[!UICONTROL Switch to manual mode]** button in the right panel.

   The AI option is the default.

1. Build the audience:

   >[!NOTE]
   >
   >As you build the audience, detailed [audience size data](audience-about.md) is updated in the right panel

   * To create the segment logic manually, using segments available on the [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments], and [!UICONTROL Saved Audiences] tabs](audience-settings.md), do the following.

     * (Optional) Search for a segment name, description, or path.

       Search results include segments based on the exact terms you use. When you enter multiple terms, all of the terms must be found for a segment.

     * To add the first segment, locate the segment in the left panel, and select the check box next to the segment name.

     * To add a segment to an existing segment group:

        1. Click the segment group in the right panel.

        1. (Optional) Change the group logic to *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, or *[!UICONTROL Exclude All]*, as needed.

           *[!UICONTROL Exclude All]* isn't available to the first segment group. For an audience that includes only exclusions, build this audience as *[!UICONTROL Include Any]* and then, within a placement, select that audience from the Excluded Audiences menu.

        1. Locate the new segment in the left panel, and select the check box next to the segment name.

           The segment group is automatically updated with the new segment.

     * To add a new segment group:

       1. Click **[!UICONTROL + New Group]** in the right panel.
       
          1. (Optional) Change the logic between the previous group and the new group to *[!UICONTROL And]* or *[!UICONTROL Or]*, as needed.
          
          1. Locate the segments for the new group in the left panel, and select the check boxes next to the segment names.
          
          1. (Optional) Change the group logic to *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, or *[!UICONTROL Exclude All]*, as needed.

   * To use segment logic from an existing audience:

     1. Copy the segment logic from the existing audience in any of the following ways:

        * In the All Audiences view, hold the cursor over the audience row, and then click **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

        * In the settings for the existing audience, at the top of the segment logic panel, click **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

        * In a text editor, manually create the segment logic using alphanumeric segment IDs and [Boolean syntax](audience-segment-logic-syntax.md), and copy it to your clipboard.

     1. Click **[!UICONTROL paste in an audience rule to begin building]**, paste the existing segment logic into the input field, and then click **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >If the audience already includes any segment logic, pasting in new segment logic overwrites the existing logic.

1. Click **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [About audience management](audience-about.md)
>* [Audience settings](audience-settings.md)
>* [Syntax for audience segment logic](audience-segment-logic-syntax.md)
>* [Available third-party data providers](third-party-data-providers.md)
>* [Create and implement a custom segment](custom-segment-create.md)
>* [Create and implement a [!UICONTROL CCPA Opt-Out-of-Sale] segment](ccpa-opt-out-segment-create.md)
>* [Placement settings](/help/dsp/campaign-management/placements/placement-settings.md)
