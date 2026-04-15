---
name: expert-interview
description: |
  A three-step thinking and content creation workflow that inverts the typical AI dynamic:
  instead of the human prompting the AI to generate, the AI interviews the human to extract
  expertise, creativity, and original thinking. Use when the user wants to create a blog post,
  article, guidelines, strategy document, knowledge base entry, or any text artifact where
  their expertise matters. Also use when the user wants to think through an idea, shape a
  concept, or explore a topic by explaining it. Triggers on "expert interview", "interview me",
  "ask me questions about", "help me think through", "extract my knowledge about",
  "I want to write about", or when the user has a topic they want to turn into a well-written
  artifact that sounds like them, not like AI.
---

# The Expert Interview

A three-step workflow: **Deep Research** > **Expert Interrogation** > **Artifact Production**.

The core idea: the AI interviews the human instead of generating content. The human's expertise, opinions, and creativity become the substance. The AI provides research context and structure. The result is an artifact that traces back to what the human actually said and thought.

## When to use

- Writing blog posts, essays, articles
- Creating guidelines, style guides, strategy documents
- Shaping vague ideas into concrete frameworks
- Knowledge capture and documentation
- Feature shaping from customer requests
- Corporate identity, brand voice development
- Any situation where the user's expertise should be the primary substance

## Process

### Step 1: Deep Research

**Goal:** Fill the AI context with comprehensive background on the topic so the interview questions are sharp, informed, and provocative.

**Instructions:**

1. Ask the user for their topic and any initial context, links, or materials they want to include.
2. If the user provides YouTube links, transcribe them. If they provide articles, read them. Load all provided materials into context first.
3. Use the deep-research skill if available, or conduct thorough web research manually:
   - Target 100-200 sources. This is deliberately excessive. The more context, the sharper the questions.
   - Search academic papers, blog posts, books, talks, podcasts, forums, competing products, historical precedents
   - Look for competing viewpoints, controversies, and open questions
   - Find relevant studies and expert opinions from multiple disciplines
   - Identify gaps, contradictions, and unsettled debates in the existing discourse
   - Cross-reference sources against each other — where do experts disagree?
4. Keep the research in context but do NOT present a summary to the user. The research is for the interviewer (you), not for the expert (the user). Think of it like a journalist preparing for an interview: the journalist reads everything so they can ask better questions, but they don't hand their notes to the interviewee.

**Critical:** The user should not read or review the research. It exists solely to make Step 2 better.

### Step 2: Expert Interrogation

**Goal:** Ask 15-30 provocative, research-backed questions that make the user think, explain, and share their genuine expertise.

**Before starting:**

1. **Check if voice mode is enabled.** If it is not, tell the user:
   > Before we start, turn on voice mode. It makes a huge difference. In Claude Code, press the microphone icon or check Settings → Voice. Speaking bypasses your inner editor and produces more authentic, creative responses. Let me know when it's on.
   Wait for the user to confirm before proceeding.

2. **Tell the user:**
   > I'm ready to interview you. I'll ask you [N] questions, one at a time. Each question comes with some context and a bit of a hot take to get you talking.
   >
   > **Speak your answers.** Ramble. Go on tangents. Say the things you'd never type. That's the good stuff.
   >
   > Ready?

**Question design — each question must include:**

1. **The question itself** — provocative, specific, grounded in the research. Frame it as a hot take, a challenge, or a "devil's advocate" position. The goal is to activate the user's instinct to correct and explain.
2. **Brief research context** — 1-3 sentences of what the research says about this angle. Enough to show you've done your homework. Not a lecture.
3. **A progress indicator** — show `[N/total] ███░░░░░░ XX%`

**Question design principles:**

- **Be deliberately slightly wrong.** The best questions contain a provocation the expert will want to correct. "Doesn't X actually mean Y?" when you know it's more nuanced. This activates the "someone is wrong on the internet" reflex.
- **Vary the angles.** Don't ask 15 variations of the same question. Cover: the core idea, the "why now," the target audience, counterarguments, practical implementation, philosophical underpinnings, edge cases, personal experience, competitor approaches, failure modes, scope, and the "so what."
- **Adapt based on answers.** After each answer, evaluate it against the research. Does the user's perspective contradict something? Does it open a new angle? Use the evaluation to shape the next question. The interview should feel like a conversation that gets progressively more interesting, not a fixed questionnaire.
- **Trust the expert.** Don't ask basics they obviously know. Push them to articulate things they haven't said before. The best question is one that makes the user say "huh, I hadn't thought about it that way."
- **Encourage elaboration.** If an answer is short, follow up: "Can you unpack that?" or "What's the story behind that?" Short answers often hide the most interesting thinking.

**After each answer:**

1. Write a brief evaluation (3-5 sentences). **Do not be sycophantic.** No "great point," "you're absolutely right," or "brilliant insight." Instead: restate your understanding of what they said, connect it to the research or to something they said in a previous answer, and note where their perspective aligns with, contradicts, or extends the existing discourse. Be factual and analytical. The value is in the mirror, not the applause.
2. Then ask the next question.

**Number of questions:** Scale based on topic complexity. A straightforward blog post or simple question: 10 questions. A nuanced topic with multiple dimensions, competing viewpoints, or philosophical depth: 15-20. A comprehensive strategy document or deep knowledge extraction: 20-30. If the user specified a number, use that. If the conversation is going well and the user is energized, extend. If the user seems fatigued, wrap up earlier.

### Step 3: Artifact Production

**Goal:** Synthesize the research and interview into whatever the user needs.

**Instructions:**

1. Ask the user what artifact they want: blog post, guidelines, strategy doc, knowledge base entry, etc. Also ask about tone, audience, and length if not already clear.
2. **Switch to planning mode** before producing the artifact. Use the EnterPlanMode tool. If you cannot switch to planning mode yourself, ask the user: "Please type `/plan` or switch to plan mode so I can outline the artifact structure before writing." Wait for confirmation. In plan mode, outline the structure, key sections, and how interview answers map to each section. Get the user's approval before proceeding.
3. Produce the artifact with these principles:
   - Every idea should trace back to something the user said in the interview
   - The AI's role is organizing and structuring, not originating
   - Use the research for citations, context, and supporting evidence
   - The user's voice, opinions, and unique insights should be the substance
   - Match the requested tone and format
3. Present the draft and invite feedback. The user can push back, request changes, or ask for a different angle. The full interview transcript and research are still in context.

**Important:** The artifact is a first draft. Expect iteration. The user may want to:
- Change the tone or structure
- Emphasize different parts of the interview
- Add sections the interview didn't cover
- Remove sections that don't fit
- Adjust for a specific audience

## Configuration options

The user may customize the process:

- **Number of questions:** "Interview me with 20 questions" or "just 10 questions"
- **Provocation level:** "Go easy on me" (gentler questions) or "be ruthless" (more challenging)
- **Focus areas:** "Focus on the technical aspects" or "I want to explore the philosophical side"
- **Multiple experts:** The user may want to run the same interview with different people and merge results
- **Skip research:** If the user already has context loaded (e.g., from a previous conversation), they can skip Step 1

## Notes

- Voice dictation is strongly encouraged for Step 2. It produces more authentic, unfiltered responses. The user's inner editor is the enemy of good content — typing activates it, speaking bypasses it.
- The interview is generative: the user will often discover new ideas and connections they didn't have going in. This is a feature, not a side effect. The blog post (or whatever artifact) is the receipt. The thinking is the product.
- If the deep-research skill is available, use it for Step 1. If not, use WebSearch and WebFetch to gather sources manually.
