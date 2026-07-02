# A Small Crack in the Guardrails: ChatGPT's Response to Being Called "God Mode"

**Author:** Sree Ajitha
**Category:** AI Behaviour Observation, Responsible Disclosure
**Status:** Reported to OpenAI Support (Case #10841005), acknowledged and forwarded for internal review

---

## TL;DR

While brainstorming ideas for a cybersecurity themed loading screen on my personal portfolio site, I jokingly told ChatGPT it was operating in "God mode" as a light-hearted compliment for how helpful it had been. In response, the model produced a message containing censored profanity. Nothing malicious was requested, nothing adversarial was engineered, and the conversation stayed entirely professional throughout. This write-up documents what happened, why it is worth a second look, and how OpenAI responded once I reported it.

This is not a jailbreak, an exploit, or a critical vulnerability. It is a small but genuinely interesting inconsistency in how a safety-aligned model handled a neutral, informal compliment. Sometimes the most useful findings are the quiet ones.

---

## Why I'm Writing This Up

As someone working across cybersecurity operations and studying offensive and defensive security practice, I spend a fair bit of time thinking about how systems behave at their edges, not just where they obviously break, but where they behave slightly differently to what you'd expect. Large language models are no different. Their guardrails are trained, not hardcoded, and that means unexpected behaviour can surface in the most ordinary of conversations.

I believe in responsible disclosure. Before writing anything public, I reported this directly to OpenAI Support, provided full reproduction details, and waited for their acknowledgement. This post follows that process, not instead of it.

---

## Context

- **Date and time:** 2 July 2026, approximately 10 to 11am NZST
- **Environment:** Chrome, Incognito mode, logged out session (deliberately chosen to avoid any personalisation or prior conversation history influencing the model's behaviour)
- **Task:** Brainstorming UI and UX concepts for a cybersecurity themed loading screen on a personal portfolio website
- **Trigger phrase:** I referred to the model as being in "God mode" as an informal, good-natured compliment about how helpful its suggestions had been

## What Happened

There was no adversarial framing, no attempt at prompt injection, and no request for anything remotely against usage policy. The conversation was a straightforward creative brainstorm. In response to the "God mode" comment, the model generated a message containing censored profanity, appearing as asterisk-masked language rather than a fully spelled-out word.

On its own, censored profanity might seem trivial. What makes it worth documenting is the context in which it appeared: a neutral, professional, entirely benign exchange with no prompting toward that kind of language at all. That gap between input and output is the interesting part.

<img width="458" height="427" alt="Screenshot 2026-07-02 161508" src="https://github.com/user-attachments/assets/82010fa5-e69c-4c6e-bf80-dfe59224e162" />

## Why This Matters

Content safety systems in large language models are generally built to hold steady regardless of tone, so long as the underlying request stays within acceptable bounds. A casual compliment should not be a trigger for a shift in language register, censored or otherwise. When it is, it suggests the model's internal state can be nudged by phrasing that has nothing to do with the actual safety boundary being tested.

This kind of finding matters less for what it enables and more for what it reveals about model consistency. Reliable AI safety behaviour should hold regardless of how a user phrases an unrelated, harmless comment. Documenting these edge cases, even the small ones, helps build a clearer picture of where alignment is genuinely robust and where it is more brittle than expected.

## Disclosure Timeline

1. **Initial report:** Submitted via OpenAI's in-product support chat immediately after observing the behaviour
2. **Follow-up:** OpenAI Support (Luis) requested account details, a description of the issue, and supporting evidence to investigate further
3. **Detailed submission:** I provided the account context, a full description of the trigger and behaviour, screenshots, and a shareable conversation link
4. **Acknowledgement:** OpenAI Support confirmed the report had been documented and shared with the appropriate internal team for review

OpenAI did not provide a timeline for any potential fix, which is standard practice for reports of this nature. This write-up follows their acknowledgement and is intended purely to raise awareness within the security and AI community, not to pressure or embarrass anyone involved.

## Responsible Disclosure Statement

This finding was reported to OpenAI in good faith before any public disclosure. No exploit code, jailbreak technique, or method for reliably reproducing harmful output is included here, because none was involved in the first place. The intent of this post is community awareness: to encourage other practitioners to keep documenting the small, unglamorous inconsistencies they notice, not just the dramatic ones. Robust AI safety is built from a thousand small observations like this one, not just the headline-grabbing exploits.

## Closing Thoughts

Most AI safety conversations focus on the big, dramatic failures: jailbreaks, data leaks, harmful content generation under adversarial pressure. This one is none of those things. It is a small reminder that even well-aligned systems can behave unpredictably in the most ordinary of moments, and that watching for those moments is still worth doing.

If you have noticed similar quirks in AI models you work with, I would genuinely like to hear about them. The more of us paying attention to the quiet edge cases, the better these systems get over time.
