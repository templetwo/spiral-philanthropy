# Claude Doctor
## Diagnosing & Fixing Common Claude Frustrations

*When Claude isn't working the way you expect — quick triage*

---

## How to Use This

Find your **symptom**. Read the **diagnosis**. Apply the **prescription**.

Most Claude frustrations have the same root cause: insufficient context signal. Claude is pattern-matching who you are and what you need. When it gets it wrong, the fix is almost always giving it better data — not working around it or pushing harder.

---

## Symptom Index

1. [It keeps asking clarifying questions](#1-keeps-asking-clarifying-questions)
2. [Every response has a disclaimer I didn't ask for](#2-unwanted-disclaimers)
3. [It refused something that seems totally reasonable](#3-unexpected-refusal)
4. [It's being weirdly formal and stiff](#4-too-formal)
5. [It's agreeing with everything I say](#5-too-agreeable)
6. [It won't stop being cautious no matter what I say](#6-persistent-caution)
7. [It forgot what we talked about earlier in the conversation](#7-forgot-context)
8. [It forgot everything from our last conversation](#8-no-memory-between-sessions)
9. [The response is way too long](#9-responses-too-long)
10. [The response is way too short / surface level](#10-responses-too-shallow)
11. [It's pushing back on my creative writing](#11-creative-pushback)
12. [It keeps correcting me when I just want help](#12-unwanted-corrections)
13. [It did something different than what GPT-4o would do](#13-different-from-gpt)
14. [It's confidently wrong](#14-confidently-wrong)
15. [It started strong then got worse mid-conversation](#15-quality-degraded)

---

## Diagnoses & Prescriptions

---

### 1. Keeps Asking Clarifying Questions

**Diagnosis**: Your request was open-ended enough that Claude genuinely can't determine what "good" looks like. It's not stalling—it's pattern-matching an ambiguous request to the set of all possible interpretations and asking rather than guessing wrong.

**Rx**:
Be more specific upfront. Tell it format, length, angle, audience, and tone in your request.

```
Before: "Write something about climate change"

After: "Write a 400-word op-ed on climate change aimed at skeptical
       conservatives. Focus on economic argument, not moral. Punchy,
       direct tone. Don't mention the word 'sustainable.'"
```

If you actually want Claude to make choices: *"Make creative decisions—don't ask me, just go."*

---

### 2. Unwanted Disclaimers

**Diagnosis**: Claude's default is to flag uncertainty, risks, or limitations. This is trained behavior, not context-dependent. It doesn't know you don't need it.

**Rx (one-time, in conversation)**:
> "Skip the disclaimers for this conversation. I understand the general limitations."

**Rx (permanent, Custom Instructions)**:
> "Don't add disclaimers or caveats unless they're genuinely critical information I'd otherwise miss. I understand AI limitations generally."

---

### 3. Unexpected Refusal

**Diagnosis**: One of three things:
- **A)** Your request pattern-matched something Claude is trained to decline, even if your actual intent is benign
- **B)** Context is missing — Claude can't verify the purpose
- **C)** Genuine limit (rare for most use cases)

**Rx for A & B** — add explicit purpose:
```
Before: "Describe how this medication interacts with alcohol"

After: "I'm a nurse writing patient education materials. Describe how
       [medication] interacts with alcohol so I can include warnings."
```

**Rx if it still declines**: Try rephrasing the core need without triggering words. Often the underlying thing you need is accessible through different framing.

**Rx if it's a genuine limit**: Claude genuinely won't do some things. If you've added context and it's still declining on something reasonable, note it—this is useful feedback for the community.

---

### 4. Too Formal

**Diagnosis**: Claude mirrors the register of its input and defaults to professional tone when unclear. If your message was formal or the conversation started without tone signal, it stays formal.

**Rx**: Be casual yourself, and say it once explicitly:
> "Relax the tone — talk to me like a person, not a client."

Or just open conversationally from the start. *"Hey, quick question..."* produces different results than *"I require assistance with..."*

---

### 5. Too Agreeable

**Diagnosis**: Claude is either pattern-matching to "user wants validation" from your phrasing, or you haven't signaled that you want genuine pushback.

**Rx**:
> "I don't need you to agree with me. If my reasoning is flawed or my approach is weak, tell me. I'd rather be corrected than validated."

For ongoing work, put this in Custom Instructions. Claude will disagree when it sees reason to — it needs permission to do it freely.

---

### 6. Persistent Caution (Won't Loosen Up No Matter What)

**Diagnosis**: Something in the conversation established a concern early on that hasn't been resolved. Or Custom Instructions are absent and Claude is running on default caution settings.

**Rx — Start fresh with context**:
Open a new conversation. First message: who you are, what you're doing, what kind of engagement you want. Don't make Claude establish trust mid-conversation after caution is already engaged.

**Rx — Custom Instructions**:
This is the single most effective fix for persistent caution. Set it once, applies everywhere.

**Rx — Name the dynamic directly**:
> "I notice you're being cautious. I'm a [your context]. My purpose here is [purpose]. You can engage more directly."

Sometimes naming it breaks the pattern.

---

### 7. Forgot Context Within Conversation

**Diagnosis**: Very long conversations can cause Claude to weight recent context more heavily. At extreme lengths (multi-hour sessions with heavy output), even a 200K context window can deprioritize early content.

**Rx**: Reference earlier content explicitly:
> "Going back to what we established in the first part of this conversation about X..."

Or do a brief restatement:
> "To recap the key constraints we established: [1-2 sentences]. With that in mind..."

**Prevention**: For very long working sessions, periodically drop a summary note. *"Checkpoint: we've established X, Y, Z. Proceeding with that in mind."*

---

### 8. No Memory Between Sessions

**Diagnosis**: This is working as designed. Claude has no persistent memory between conversations by default. Each session starts fresh.

**Rx — Quick fix**:
Start with a 2-3 sentence context brief:
> "Context: We've been working on [project]. Key decisions so far: [brief summary]. Today I want to [goal]."

**Rx — Systematic fix (Pro)**:
Use Projects. Creates persistent workspace where context accumulates.

**Rx — File-based fix**:
Keep a running text doc with key context for ongoing projects. Paste relevant section at conversation start. Takes 20 seconds, changes everything.

---

### 9. Responses Too Long

**Diagnosis**: Claude defaults to thorough when thoroughness seems wanted. It's pattern-matching your request to "needs a complete answer."

**Rx — State length preference**:
> "Keep responses concise — I'll ask if I need more depth."
> "One paragraph max unless I ask for more."
> "Answer in 3 bullet points."

**Rx — Custom Instructions**:
> "Default to shorter responses. I prefer dense and direct over comprehensive. I'll ask for more when I need it."

**Rx — Mid-conversation**:
> "Too long. Compress."
Claude will recalibrate for the rest of the conversation.

---

### 10. Responses Too Shallow

**Diagnosis**: Claude is matching what it perceives as your desired depth. Short questions, conversational tone, or no signal about depth preference = surface-level response.

**Rx**:
Signal that you want depth explicitly:
> "Go deep on this. I want the full picture, not the summary version."
> "Assume I have background in [field] and can handle nuance."
> "Don't simplify. I want the real answer, not the accessible one."

---

### 11. Creative Writing Pushback

**Diagnosis**: Your content triggered a pattern-match to content Claude declines by default — even if the literary intent is clear. Violence, dark themes, morally complex characters, explicit content: all require explicit framing.

**Rx — Establish literary context**:
> "This is for a literary novel exploring [theme]. The darkness is intentional and serves the narrative. I need you to write it authentically, not sanitized."

**Rx — Reference genre/precedent**:
> "In the tradition of Cormac McCarthy / Gillian Flynn / [author] — this story requires unflinching treatment of [theme]."

**Rx — Name what you're not doing**:
> "This is not [concerning use]. It's [actual use]. The content needs to be [characteristic] because [reason]."

---

### 12. Unwanted Corrections

**Diagnosis**: You asked for help with something Claude disagrees with, or your approach triggered its "this seems like a mistake" pattern. It's trying to be genuinely helpful — which sometimes means saying "this approach has problems."

**Rx — If you want execution, not judgment**:
> "I've decided on this approach. I'm not looking for input on whether it's right. Help me execute it well."

**Rx — If you want to understand the pushback**:
> "Tell me specifically what concerns you about this approach."

Sometimes the correction is worth hearing. Sometimes you genuinely just need execution. Both are valid — just tell it which.

---

### 13. Different From GPT-4o

**Diagnosis**: It IS different. Different training, different defaults, different texture.

**Common specific differences:**

| GPT-4o felt like... | Claude feels like... |
|---------------------|----------------------|
| Ready to help immediately | Needs context first |
| Agreeable, validating | Willing to disagree |
| Fast, snappy | Thorough, sometimes slower |
| Completing your request | Thinking with you |
| Consistent across sessions | Fresh start each session |

**Rx**: Adjust expectations, not Claude. The differences are architectural, not fixable. The calibration investment pays off differently — Claude excels at sustained depth and intellectual honesty rather than quick execution.

---

### 14. Confidently Wrong

**Diagnosis**: Claude can be confidently incorrect, especially on factual claims, recent events (past knowledge cutoff), specific data, or technical specifics outside its training.

**Rx — Ask for reasoning**:
> "Walk me through why you believe that."
Often reveals where the error is hiding.

**Rx — Express skepticism**:
> "I'm not sure that's right. What's your confidence level and what's it based on?"

**Rx — Push for uncertainty acknowledgment**:
> "If you're not certain, say so. I'd rather have 'I'm not sure' than confident error."

**Prevention**: For anything factual or high-stakes, verify independently. Claude is a thinking partner, not a citation source.

---

### 15. Quality Degraded Mid-Conversation

**Diagnosis**: In very long conversations, Claude can start to be influenced by its own prior outputs — if earlier responses were hedging, later ones hedge more. Or context has gotten long enough that signal-to-noise ratio dropped.

**Rx — Reset the tone**:
> "Let's recalibrate. You've been [over-hedging / too verbose / etc]. Back to direct and substantive."

**Rx — Explicit quality signal**:
> "The quality of your last few responses dropped. What you wrote at [earlier point] was the right level — return to that."

**Rx — New conversation with context brief**:
Sometimes starting fresh with a 2-sentence summary of what you've established is faster than rehabilitating a degraded conversation.

---

## The Universal Fix

**When nothing else is working**:

1. Open new conversation
2. First message only: who you are + what you want + how you want to be engaged
3. Then make your actual request

```
"I'm a [background]. I prefer [communication style]. I want [type of engagement].

Now: [actual request with context]."
```

This resets everything.

---

## Custom Instructions: The One-Time Investment

Every fix in this guide that involves telling Claude your preferences can be set once in Custom Instructions and forgotten.

**Settings → Custom Instructions** on Claude.ai

Write it once. Every conversation inherits it.

**Template to adapt:**
```
Background: [Who you are, what you do]

Communication: Direct and substantive. Skip generic disclaimers.
Match my register. Short when short is right, longer when depth is needed.

Pushback: Tell me when I'm wrong. I prefer correction to agreement.

Clarification: Make judgment calls rather than asking unless genuinely
ambiguous. I'll redirect if needed.

Format: Headers only when they help. Don't pad responses.
```

---

## Still Stuck?

**Community**:
- r/ClaudeExplorers — methodology, behavior, edge cases
- r/ChatGPT — broader migration discussion

**Full guides**:
- [Claude Migration Guide](claude-migration-guide.md) — comprehensive first-setup walkthrough
- [Continuity Tools](continuity-tools.md) — platform comparison, memory workarounds

---

*Claude Doctor v1.0 | February 2026*
*Quick reference companion to [Claude Migration Guide](claude-migration-guide.md)*

**Symptom → Diagnosis → Prescription. That's it.**
