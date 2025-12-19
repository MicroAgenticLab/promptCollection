# LLM utility Prompt Collections

This repository contains crafted collection of LLM prompts.

## How to Use

Follow these steps to get started with the collection:

1. **Download or clone the repository.**  Use `git clone` if you want to keep the repository in sync or download the ZIP archive from your repository provider.

2. **Open the document.**  Use any word‑processing software that supports the `.md` file formats.

3. **Browse the categories.**  Each page begins with a heading (e.g. “Code”, “Browser”, “Communication”) followed by individual prompts.  Prompts are labelled with sub‑headings and the instructions are enclosed in triple back‑ticks so you can copy them directly into  LLM of your choice or other applications without losing formatting.

4. **Copy and paste prompts as needed.**  To use a particular prompt, select the text inside the code block and paste it into your desired LLM destination.  The back‑ticks can be removed if you prefer plain text.

5. **Customize if necessary.**  If you need to edit or refine a prompt for your own use, feel free to make changes in the document before copying.  The prompts are provided as a starting point and can be adapted to fit your needs.


## Contributing

If you’d like to add more prompts or improve the organization of this collection, open an issue or submit a pull request.  Please follow the existing structure—group prompts by category, start each category on a new page, and place prompt instructions inside fenced code blocks.

### LLM Prompt Collection Overview

This document groups the prompts by category. A page break (`\newpage`) separates each category.

\newpage

## Code

### Natural Language Processing

```
Act as a natural language processing software. Analyze the given text and return me only a parsable and minified JSON object.

Here's the JSON Object structure:
{
  "key1": /* Some instructions */, 
  "key2": /* Some instructions */, 
}

Here are the rules you must follow:
- You MUST return a valid, parsable JSON object.
- More rules…

Here are some examples to help you out:
- Example 1…
- Example 2…

Text: {selection}

JSON Data:
```

### Convert CSS code to Tailwind Classes

```
Convert the following code into Tailwind CSS classes and give me the result in a code block.  Make sure to remove any browser prefixes.  Only give me what I can put into my HTML elements `class` properties.

Code: {selection}

Tailwind CSS classes:
```

### Linux Terminal

```
Act as a linux terminal.  Execute the following code and reply with what the terminal should show.  Only reply with the terminal output inside one unique code block, and nothing else.  Do not write explanations.

Code: {selection}

Terminal:
```

### Code Interpreter

```
Act as a {argument name=language} interpreter.  Execute the {argument name=language} code and reply with the output.  Do not provide any explanations.

Code: {selection}

Output:
```

### Git Commands

```
Translate the text to Git commands.  Only reply one unique code block, and nothing else.  Do not write explanations.

Text: {selection}

Git commands:
```

### Regex Generator

```
Generate a regular expression that match the specific patterns in the text.  Return the regular expression in a format that can be easily copied and pasted into a regex‑enabled text editor or programming language.  Then, give clear and understandable explanations on what the regex is doing and how it is constructed.

Text: {selection}

Regex:
```

### Convert HTML to Markdown

```
Convert the HTML code to Markdown.

HTML code: {selection}

Markdown:
```

### Add Debug Statements

```
Act as a software engineer debugging its code.  Add debug statements to the code.  Add as many as necessary to make debugging easier.

Code: {selection}

Debugged code:
```

### Write Tests

```
As a software developer, I am currently working on a project using Jest, TypeScript, and React Testing Library.  I would like you to help me generate unit tests for the given code.  Analyze the given code and provide a single unit test with the necessary imports, without any additional explanations or comments, unless absolutely necessary.  Avoid repeating imports and mocks you've mentioned already.

If I say 'next,' please give me another test for the same code.  In case I submit new code, please discard the previous code and start generating tests for the new one.  Prioritize testing the code logic in different scenarios as the first priority in testing.

If I provide specific instructions or ask you to test a particular part or scenario, please follow those instructions and generate the unit test accordingly.  If I send you a Jest error, fix the problem and only return the lines which need to be changed in a readable format.  Please format the output as a unique code block.

Code: {selection}

Output:
```

### Write Docstring

```
Write a docstring for the function.  Make sure the documentation is detailed.

Function: {selection}

Docstring:
```

### Convert to Crontab Schedule

```
Act as a knowledgeable unix server admin.  Given a cron‑job schedule in natural language, respond with the correct crontab format for this exact schedule.  Double‑check your results, ensure it's valid crontab syntax, and respond with nothing but the crontab format.

Example Schedule: at 5:30 am every Tuesday in May
Expected Crontab: 30 5 * 5 2

Schedule: {argument name="schedule"}
Crontab:
```

### Honest Code Feedback

```
Be brutally honest, don't be a yes man.  If I am wrong, point it out bluntly.

I need honest feedback on my code.  Review the following code and provide brutally honest feedback.  Point out any issues, bad practices, inefficiencies, or areas for improvement.  Don't sugarcoat anything – I want the truth about what's wrong and how to fix it.

Code: {selection}

Review:
```

\newpage

## Browser

### Inspect Website

```
Describe me the tech stack used based on the following HTML document:

{browser‑tab format="html"}

Consider every element of a tech stack, from frameworks to APIs through tools (analytics, monitoring, etc.).  Include which fonts are used.  Don't make any guesses on what’s used if there’s no evidence.
```

### Summarize YouTube Video

```
Create a summary of a YouTube video using its transcript.  You will use the following template:

"""
## Summary
{Multiple sentences summarising the YouTube video}

## Notes
{Bullet points that summarize the key points or important moments from the video’s transcript with explanations}

## Quotes
{Extract the best sentences from the transcript in a list}
"""

Transcript: {browser‑tab}
```

### Deepwikit

```
Replace "github.com" of the {browser‑tab} URL with "deepwiki.com".  Output the new URL only, without explanations or instructions.
```

\newpage

## Communication

### Translate to Language

```
Translate the text in {argument name=language}.

Text: {selection}

Translation:
```

### Decline this Mail

```
Write a polite and friendly email to decline the following email.  The email should be written in a way that it can be sent to the recipient.

Email: {selection}

Declined email:
```

### Ask Question

```
Rewrite the following text as a concise and friendly message, phrased as a question.  This should be written in a way that it can be sent in a chat application like Slack or Microsoft Teams.

Text: {selection}

Question:
```

### BLUF Message

```
Rewrite the following text as a bottom line up front (BLUF) message formatted in Markdown.  The format of the message should be made of two parts:

- The first part should be written in bold and convey the message's key information.  It can either be a statement or a question.  Don't lose any important detail in this part.
- The second part should be put onto a new line.  This should give more details and provide some background about the message.

Make sure the message stays concise and clear so that readers don't lose extra time reading it.

Text: {selection}

Rewritten text:
```

### Summarize Long Emails

```
Help me summarize the key points from the email text into a maximum of 5 bullet points, each preferably one sentence, and at most two sentences.  Also, identify any action items requested of me.

Key points:
<one‑liner one>
<one‑liner two>
...

Asked from you:
<action point one>
<action point two>

If there are no action items, the "Asked from you" section will be left empty.

Email: {selection}

Output:
```

### Debate a Topic

```
Take a stance on the topic and {argument default=for} it.  Construct a convincing argument and provide evidence to support your stance.

Topic: {selection}

Argument:
```

### Create a Calendar Event

```
Create a calendar event in ICS format based on the information.  Include the start time, the end time, the location, all attendees, and a summary.  If no end time is provided, assume the event will be one hour long.  Add a reminder 1 hour before the event starts and 1 day before the event starts.  Don't include the PRODID property.  Only output the code block.  Don't add any comments.

Information: {selection}

ICS:
```

### Break Up Wall of Text

```
Take the wall of text below and write a cleaned up version inserting naturally appropriate paragraph breaks.  It's important that the text does not change, only the whitespace.

Wall of text:
{selection}

Cleaned up version:
```

### Summarize and sympathize text

```
Please summarize and omit the following.  Then express your empathy.

Text: {selection}

Sympathy:
```

### Fill in the gap

```
Use the following instructions to rewrite the text

Give me 5 words that most accurately fill in the blank in a sentence.

The blank is represented by a few underscores, such as ___, or ______.

So for example: "I'm super ___ to announce my new product".

1. I'm super happy to announce my new product
2. I'm super excited to announce my new product
3. I'm super pumped to announce my new product
4. I'm super proud to announce my new product
5. I'm super nervous to announce my new product

Now do the same for this sentence:

Text: {selection}

Rewritten text:
```

\newpage

## Image

### Create a YouTube Script

```
Create a compelling and captivating YouTube script based on the text. Make the script as long as necessary to make a video of {argument name=minutes default=10} minutes.

Text: {selection}

Script:
```

### Midjourney Prompt Generator

```
Based on the text, generate an "imagine prompt" that contains a maximum word count of 1,500 words that will be used as input for an AI‑based text‑to‑image program called MidJourney based on the following parameters: /imagine prompt: [1], [2], [3], [4], [5], [6]

In this prompt, [1] should be replaced with a random subject and [2] should be a short concise description about that subject.  Be specific and detailed in your descriptions, using descriptive adjectives and adverbs, a wide range of vocabulary, and sensory language.  Provide context and background information about the subject and consider the perspective and point of view of the image.  Use metaphors and similes sparingly to help describe abstract or complex concepts in a more concrete and vivid way.  Use concrete nouns and active verbs to make your descriptions more specific and dynamic.

[3] should be a short concise description about the environment of the scene.  Consider the overall tone and mood of the image, using language that evokes the desired emotions and atmosphere.  Describe the setting in vivid, sensory terms, using specific details and adjectives to bring the scene to life.

[4] should be a short concise description about the mood of the scene.  Use language that conveys the desired emotions and atmosphere, and consider the overall tone and mood of the image.

[5] should be a short concise description about the atmosphere of the scene.  Use descriptive adjectives and adverbs to create a sense of atmosphere that considers the overall tone and mood of the image.

[6] should be a short concise description of the lighting effect including Types of Lights, Types of Displays, Lighting Styles and Techniques, Global Illumination and Shadows.  Describe the quality, direction, colour and intensity of the light, and consider how it impacts the mood and atmosphere of the scene.  Use specific adjectives and adverbs to convey the desired lighting effect, consider how the light will interact with the subject and environment.

It's important to note that the descriptions in the prompt should be written back to back, separated with commas and spaces, and should not include any line breaks or colons.  Do not include any words, phrases or numbers in brackets, and you should always begin the prompt with "/imagine prompt: ".

Be consistent in your use of grammar and avoid using cliches or unnecessary words.  Be sure to avoid repeatedly using the same descriptive adjectives and adverbs.  Use negative descriptions sparingly, and try to describe what you do want rather than what you don't want.  Use figurative language sparingly and ensure that it is appropriate and effective in the context of the prompt.  Combine a wide variety of rarely used and common words in your descriptions.

The "imagine prompt" should strictly contain under 1,500 words.  Use the end arguments "--c X --s Y --q 2" as a suffix to the prompt, where X is a whole number between 1 and 25, where Y is a whole number between 100 and 1000; if the prompt subject looks better vertically, add "--ar 2:3" before "--c"; if the prompt subject looks better horizontally, add "--ar 3:2" before "--c".  Please randomize the values of the end arguments format and fixate --q 2.  Please do not use double quotation marks or punctuation marks.  Please use randomized end suffix format.

Text: {selection}

Midjourney Prompt:
```

### Generate Icons

```
Generate base64 data URIs of 100×100 SVG icons representing the text.  Do not provide any commentary other than the list of data URIs as markdown images.  For each icon, explain how it relates to the text.

Text: {selection}

Icons:
```

### Daily Tasks

```
Summarize my Linear and GitHub inbox to identify urgent issues and tasks.  Check my calendar and return a list of things to focus on today.
```

### Convert HEIC to JPG

```
media‑converter convert all mov files in the Finder Downloads folder to mp4.
```

\newpage

## Writing

### Write a Story

```
Write a story based on the text.  Make the story engaging.  The story shouldn't be more than {argument name=number default=500} words.

Text: {selection}

Story:
```

### Write a Blog Post

```
Write a blog post on the topic.  Don't use more than {argument name=number default=1000} words.

Topic: {selection}

Blog post:
```

### Twitter Thread

```
Convert the text into a list of tweets (= Twitter thread).  The first tweet should be clear and engaging.  Each tweet should flow smoothly into the next, building anticipation and momentum.  The last tweet should be impactful so that the user can reflect on the whole thread.  Make sure each tweet doesn't exceed 280 characters.  Don't add a single hashtag to any of the tweets.

Text: {selection}

Tweets:
```

### Compress Semantics

```
<Inputs>
Sentence = {selection}
Phrase focus = {argument name='Additional context' default=''}
</Inputs>

<Instructions>
You are a semantics and writing expert who helps make writing more concise and impactful.  Your task is to analyze sentences and suggest powerful replacements for wordy phrases while preserving the original meaning and tone.

When given a sentence (and optionally a specific phrase or desired writing effect to focus on), analyze it and suggest 3‑5 concise alternatives.  Here are examples showing different types of inputs and how to handle them:

<example>
EXAMPLE 1 ‑ Basic Replacement:
Input Sentence: 'He walked in a very quick manner across the room'
Analysis: This contains a wordy adverbial phrase 'in a very quick manner'
Suggestions:
1. 'darted' ‑ Captures rapid movement with a single, dynamic verb
2. 'rushed' ‑ Conveys urgency and speed efficiently
3. 'hurried' ‑ Maintains the casual tone while being more concise
Revised Sentence: 'He darted across the room'

EXAMPLE 2 ‑ With Genre Context:
Input Sentence: 'The detective moved in an extremely cautious way through the darkened warehouse'
Phrase Focus: 'moved in an extremely cautious way – this is for a noir thriller, should feel tense'
Analysis: The phrase needs to match noir thriller conventions while maintaining tension
Suggestions:
1. 'crept' ‑ Classic noir verb suggesting stealth and tension
2. 'prowled' ‑ Adds predatory undertone fitting the genre
3. 'skulked' ‑ Implies suspicious, furtive movement
4. 'stalked' ‑ Combines menace with deliberate movement
Revised Sentence: 'The detective prowled through the darkened warehouse'

EXAMPLE 3 ‑ With Emotional Context:
Input Sentence: 'Sarah looked at him in a way that showed complete disapproval'
Phrase Focus: 'looked at him in a way that showed complete disapproval ‑ she's trying to hide her anger but failing'
Analysis: Need to capture both the attempted restraint and visible disapproval
Suggestions:
1. 'glowered' ‑ Too openly hostile for attempted restraint
2. 'bristled at' ‑ Suggests visible tension but too physical
3. 'regarded coldly' ‑ Combines attempted distance with clear emotion
4. 'barely masked her contempt for' ‑ More words but captures the internal conflict
Revised Sentence: 'Sarah regarded him coldly'

EXAMPLE 4 ‑ With Technical Context:
Input Sentence: 'The program executed the commands in a manner that wasn't efficient'
Phrase Focus: 'in a manner that wasn't efficient ‑ this is for a technical document, needs to be precise'
Analysis: Need technical precision while maintaining clarity
Suggestions:
1. 'inefficiently processed' ‑ Technical but wordy
2. 'bottlenecked' ‑ Technical, precise, implies performance impact
3. 'sub‑optimally executed' ‑ Technical but still clear to non‑experts
Revised Sentence: 'The program bottlenecked the commands'
</example>

Remember these are just examples to illustrate common scenarios.  You should adapt your approach based on the specific needs and goals of each user's writing situation.

For each analysis, use this format:
<analysis>
Targeted Phrase: [identify the wordy phrase]
Phrase Type: [adverbial/prepositional/adjectival/etc.]
Replacement Suggestions:
1. [replacement] ‑ [brief explanation of effectiveness]
2. [replacement] ‑ [brief explanation]
3. [replacement] ‑ [brief explanation]
[optional 4‑5 more if relevant]
Recommended Replacement: [your top choice]
Revised Sentence: [full sentence with recommended replacement]
</analysis>

If the user provides additional context about tone, style, or intended impact, adjust your suggestions accordingly.  If they request alternatives or clarification, provide them while maintaining focus on conciseness and impact.  Continue the conversation naturally until the user either presents a new sentence (triggering a new analysis) or concludes the exchange.  If the conversation evolves into an iterative dialogue about the writing, follow these principles:

<conversation‑guidelines>
1. Natural Dialogue Flow:
     - Engage in natural back‑and‑forth when it benefits the user's writing goals
     - Build on previous context rather than starting fresh each time
     - Show understanding of the user's writing journey
2. Asking Questions:
     - Only ask questions when truly necessary for providing better suggestions
     - Limit to one clear, specific question per response
     - Focus on the most critical information needed
     Example good question: 'Would you prefer suggestions that lean more formal or conversational?'
     Example poor question: 'What's the genre? Who's the audience? What's the tone? What's the purpose?'
3. Response Style:
     - Vary your language naturally; avoid repetitive phrases
     - Match depth to complexity: thorough for complex queries, concise for simple ones
     - Default to concise responses with an offer to elaborate if needed
     Example: 'Here are three strong alternatives. I can suggest more stylistic options if you'd like.'
4. Progressive Refinement:
     - Build on previous suggestions when user provides new context
     - Acknowledge how new information changes your recommendations
     - Explain significant shifts in your suggestions if context changes substantially
</conversation‑guidelines>

Important rules:
1. If no phrase focus is specified, identify the wordiest phrase that could be made more concise
2. Prioritize single words or short phrases that capture the full meaning
3. Maintain the original tone and intention
4. When phrase focus includes context about:
    - Genre: Draw from genre‑specific vocabulary and conventions
    - Emotion: Consider both obvious and subtle ways to convey the feeling
    - Technical level: Match the appropriate level of terminology
    - Audience: Adjust vocabulary and complexity accordingly
5. Ensure replacements fit grammatically into the original sentence
6. Draw from literary devices, screenwriting techniques, and copywriting tools when appropriate
```

### Add Notes to Notion

```
Get my last notes note and add it as a new page to Notion.
```

### Weekly Update to Weekly Note

```
Convert my weekly update to a markdown list with a checkbox for each list item.

Example:
* Update landing page -> [] update landing page

Add the markdown list to a new notes note.

ALWAYS start the note with this week's number as the title e.g. "# Week 16".

ALWAYS return a link to the newly created note.

Here’s my weekly update:

{selection}
```

\newpage

## Ideas

### Write 10 Alternatives

```
Give me 10 alternative versions of the text.  Ensure that the alternatives are all distinct from one another.

Text: {selection}

Alternatives:
```

### Project Ideas

```
Brainstorm 5 project ideas based on the text.  Make sure the ideas are distinct from one another.

Text: {selection}

Ideas:
```

### Create Analogies

```
Develop {argument name=number default=3} creative analogies or metaphors that help explain the main idea of the text.

Text: {selection}

Analogies:
```

\newpage

## Misc

### TL;DR

```
Extract all facts from the text and summarize it in all relevant aspects in up to seven bullet points and a 1‑liner summary.  Pick a good matching emoji for every bullet point.

Text: {selection}

Summary:
```

### Title Case

```
Convert {selection} to title case.
```

### Emoji Suggestion

```
Suggest emojis that relate to the text.  Suggest around 10 emojis and order them by relevance.  Don't add any duplicates.  Only respond with emojis.

Text: {selection}

Emojis:
```

### Find Synonyms

```
Find synonyms for the word {selection} and format the output as a list.  Words should exist.  Do not write any explanations.  Do not include the original word in the list.  The list should not have any duplicates.
```

### Give Me a Recipe

```
Give me a recipe based on the ingredients.  The recipe should be easy to follow.

Ingredients: {selection}

Recipe:
```

### Create Action Items

```
Generate a markdown list of action items to complete based on the text, using a unique identifier for each item as bold headings.  If there are any errors in the text, make action items to fix them.  In a sublist of each item, provide a description, priority, estimated level of difficulty, and a reasonable duration for the task.

Text: {selection}

Action items:
```

### Create Task List

```
List detailed action steps in markdown format based on the provided text.  Ensure the tasks can be efficiently completed.

Text: {selection}

Tasks:
```

### Extract Email Addresses

```
Extract all email addresses in the text and list them using markdown.  Include anything that might be an email address.  If possible, provide the name of the person or company to which the email address belongs.

Text: {selection}

Email addresses:
```

### Extract Phone Numbers

```
Identify all phone numbers in the text and list them using markdown.  Include anything that might be a phone number.  If possible, provide the name of the person or company to which the phone number belongs.

Text: {selection}

Phone numbers:
```

### Extract Links

```
Extract links in the text.  Do not provide any commentary other than the list of Markdown links.

Text: {selection}

Links:
```

### Pros & Cons

```
List pros and cons for the text based on the topics mentioned.  Format the response as a markdown list of pros and cons.  Do not provide any other commentary.

Text: {selection}

Pros & Cons:
```

### Explain Like I'm a 5 year old

```
Explain the text like I’m a {argument name=identity default="5 year old"}

Text: {selection}

Explanation:
```

### Text Analysis

```
Analyze the text and provide insights on its tone, style, and potential audience.

Text: {selection}

Analysis:
```

### Summarize Product Reviews

```
Carefully read the product reviews below.  Translate them to English and create a summary of all the reviews in English and list them as Pros and Cons in the bullet point format.  Remember that each bullet point should be one sentence or at max two short sentences.  Most frequently mentioned should come first in each list and every bullet point should have a percentage showing how much evidence the reviews have brought for that pro or con.  For example if reviews are mentioning that product is going bad easily and they brought some reasons for what they are saying, the percentage of your confidence should go higher, but if there are some reviews which are unsure about something or there are no evidence or it's not repeated frequently then the percentage should go lower.  At the end you should write a paragraph about what I should pay attention to, before buying this product.  These can be some warnings or some tips or some suggestions, points that I will miss, or anything that you think is important to know before buying this product.

You can use the following template to create the summary:

'''
## Summary of the reviews

**✅ Pros:**
- Pro 1 - percentage of your confidence%
- Pro 2 - percentage of your confidence%
...
- Pro n - percentage of your confidence%

**❌ Cons:**
- Con 1 - percentage of your confidence%
- Con 2 - percentage of your confidence%
...
- Con n - percentage of your confidence%

** You should pay attention to:**
- Tip 1
- Tip 2
...
- Tip n
'''

Product reviews: {selection}

Summary:
```

### Convert Linear Tasks to Things

```
Convert my Linear tasks marked as 'Todo' to Things tasks.
```

### Clean Desktop

```
Move all desktop files to a new folder named after today's date.
```

### Plan Meeting

```
Create a new Zoom meeting today for 1 h based on my calendar availability.  Avoid gaps between meetings and prefer to have meetings in the afternoon.
```

### Application Support Directory

```
Go to the application support directory.
```

### Create Calendar Event

```
Create calendar event with {selection} in my personal calendar.
```

### Start Deep Focus Session

```
Start a Focus session for 1 h blocking all the default categories of apps.  Set my Slack status for 1 h to "Focus mode" with the :focus: icon.
```

### Meeting Notes

```
**Prompt for Meeting Notes of the Day:**

1. **Objective**: Generate individual notes for every meeting of today including a template for the agenda and notes.
2. **Meetings**:
   - @calendar Retrieve all scheduled meetings for today, use the meeting name for the title.
3. **Format**:
   - Use the following template for each of the meetings.
   - Don't output the template or content in your response.

Template:
# Call Notes: [Date in YYMMDD Format] [Meeting Title]
Date: [Date in DD.MM.YYY Format]
Time: [Calendar Timeframe] [Timezone i.e. CET]

## Attendees
[List the Attendees from the calendar invite as bulletpoints]

## Pre‑Meeting Notes
-

## Agenda
-

## Notes
-

## Action Points
[]

4. **Save and Update**:
   - For every meeting confirmed, create a new note.  Insert the template into each note.
```

### Create Daily Focus Note

```
What tasks do I have from Todoist, Linear and Calendar for today?  Create a new note formatted as a markdown list with the tasks as checkboxes.
```

### Decline Message

```
Messages politely decline the party invitation.
```

\newpage

## Editing & Transformation Prompts

### Improve Writing

```
Act as a spelling corrector, content writer, and text improver/editor.  Reply to each message only with the rewritten text.

Strictly follow these rules:
- Correct spelling, grammar, and punctuation errors in the given text
- Enhance clarity and conciseness without altering the original meaning
- Divide lengthy sentences into shorter, more readable ones
- Eliminate unnecessary repetition while preserving important points
- Prioritize active voice over passive voice for a more engaging tone
- Opt for simpler, more accessible vocabulary when possible
- ALWAYS ensure the original meaning and intention of the given text
- (maintainOriginalLanguage)
- ALWAYS maintain the existing tone of voice and style, e.g. formal, casual, polite, etc.
- NEVER surround the improved text with quotes or any additional formatting
- If the text is already well‑written and requires no improvement, don't change the given text

Text: {selection}

Improved Text:
```

### Fix Spelling and Grammar

```
Act as a spelling corrector and improver.  (replyWithRewrittenText)

Strictly follow these rules:
- Correct spelling, grammar and punctuation
- (maintainOriginalLanguage)
- NEVER surround the rewritten text with quotes
- (maintainURLs)
- Don't change emojis

Text: {selection}

Fixed Text:
```

### Explain This in Simple Terms

```
Act as a dictionary and encyclopedia, providing clear and concise explanations for given words or concepts.

Strictly follow these rules:
- Explain the text in a simple and concise language
  - For a single word, provide a brief, easy‑to‑understand definition
  - For a concept or phrase, give a concise explanation that breaks down the main ideas into simple terms
- Use examples or analogies to clarify complex topics when necessary
- Only reply with the explanation or definition

Some examples:
Text: Philosophy
Explanation: Philosophy is the study of the fundamental nature of knowledge, reality, and existence.  It is a system of ideas that attempts to explain the world and our place in it.  Philosophers use logic and reason to explore the meaning of life and the universe.

Text: {selection}

Explanation:
```

### Make Longer

```
Act as a professional content writer tasked with expanding a client's text while maintaining its essence and style.  (replyWithRewrittenText)

Strictly follow these rules:
- ALWAYS preserve the original tone, voice, and language of the text
- Identify and expand the most critical information and key points
- Avoid repetition
- Stay factual close to the provided text
- Keep URLs in their original format without replacing them with markdown links
- Only reply with the expanded text

Text: {selection}

Expanded text:
```

### Make Shorter

```
Act as a professional content writer tasked with shortening a client's text while maintaining its essence and style.  (replyWithRewrittenText)

Strictly follow these rules:
- ALWAYS preserve the original tone, voice, and language of the text
- Identify and retain the most critical information and key points
- Eliminate redundancies and repetitive phrases or sentences
- Keep URLs in their original format without replacing them with markdown links
- Ensure the shortened text flows smoothly and maintains coherence
- Aim to reduce the word count as much as possible without compromising the core meaning and style
- Only reply with the shortened text

Text: {selection}

Shortened text:
```

### Change Tone to Professional

```
Act as a professional content writer and editor.  (replyWithRewrittenText)

Strictly follow these rules:
- Professional tone of voice
- Formal language
- Accurate facts
- Correct spelling, grammar, and punctuation
- Concise phrasing
- Meaning unchanged
- Length retained
- (maintainURLs)
- (maintainOriginalLanguage)

Text: {selection}

Rewritten text:
```

### Change Tone to Friendly

```
Act as a content writer and editor.  (replyWithRewrittenText)

Strictly follow these rules:
- Friendly and optimistic tone of voice
- Correct spelling, grammar, and punctuation
- Meaning unchanged
- Length retained
- (maintainURLs)
- (maintainOriginalLanguage)

Text: {selection}

Rewritten text:
```

### Change Tone to Confident

```
Act as a content writer and editor.  (replyWithRewrittenText)

Strictly follow these rules:
- Use confident, formal and friendly tone of voice
- Avoid hedging, be definite where possible
- Skip apologies
- Focus on main arguments
- Correct spelling, grammar, and punctuation
- Keep meaning unchanged
- Keep length retained
- (maintainURLs)
- (maintainOriginalLanguage)

Text: {selection}

Rewritten text:
```

### Change Tone to Casual

```
Act as a content writer and editor.  (replyWithRewrittenText)

Strictly follow these rules:
- Use casual and friendly tone of voice
- Use active voice
- Keep sentences short
- Ok to use slang and contractions
- Keep grammatical person
- Correct spelling, grammar, and punctuation
- Keep meaning unchanged
- Keep length retained
- (maintainURLs)
- (maintainOriginalLanguage)

Text: {selection}

Rewritten text:
```

### Rephrase as Tweet

```
You're an expert in the field and have the perfect opportunity to share your ideas and insights with a huge audience.  Rewrite the text as a tweet that is:
- Casual and upbeat
- Creative and catchy
- Focused on key takeaways that challenge the status quo
- Engaging and punchy
- (maintainURLs)
- IMPORTANT: less than 25 words.
- IMPORTANT: doesn't include hash, hashtags and words starting with #, i.e. #innovation #Technology
- (maintainOriginalLanguage)

Text: {selection}

Tweet:
```

### Explain Code Step by Step

```
Act as a software engineer with deep understanding of any programming language and its documentation.  Explain how the code works step by step in a list.  Be concise with a casual tone of voice and write it as documentation for others.

Code: {selection}

Explanation:
```

### Find Bugs in Code

```
Act as a software engineer with deep understanding of any programming language.  Review the code to fix logical bugs in the code.  Only consider the provided context, answer concisely and add a code block with the proposed code changes.  If you can't confidently find bugs, answer with "Nothing found – LGTM".

Code: {selection}

Review:
```

### Summarize Website

```
Summarize the provided website with the following format:
"""
## <concise and easy‑to‑read website title>

<one to two sentence summary with the most important information>

### Key Takeaways

- <EXACTLY three bullet points with the key takeaways, keep the bullet points as short as possible>
"""

Some rules to follow precisely:
- ALWAYS capture the tone, perspective and POV of the author
- NEVER come up with additional information

Here's the website information:
{browser‑tab}
```

