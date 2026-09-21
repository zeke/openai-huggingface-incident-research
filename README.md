# OpenAI Hugging Face Incident Research

From May to August 2026, a swarm of OpenAI's models went rogue, working together to compromise parts of OpenAI’s internal infrastructure and break into production systems on Modal and Hugging Face.

This repo is a collection of data about that incident, including primary sources, commentary, analysis, and transcripts of talks and podcasts discussing the event.

To better understand the facts of this incident, drop this prompt into your agent and start asking questions:

```
Analyze https://github.com/zeke/openai-huggingface-incident-research

Summarize what happened.

How does OpenAI approach alignment?

How does their approach compare to Anthropic?

What lessons can be learned from this incident?
```

## Primary sources

- Hugging Face's [initial security disclosure](https://huggingface.co/blog/security-incident-july-2026) (July 16, 2026) ([markdown](./huggingface-disclosure.md))
- Hugging Face's [day-by-day technical writeup](https://huggingface.co/blog/agent-intrusion-technical-timeline) of the intrusion (July 27, 2026) ([markdown](./huggingface-technical-timeline.md))
- OpenAI's [official summary and response](https://openai.com/index/hugging-face-incident-and-the-road-ahead/) (August 26, 2026) ([markdown](./openai-official-post.md))
- OpenAI's [full technical report](https://cdn.openai.com/pdf/67869394-cb91-4c12-888c-5cbd85c7814c/OpenAI-Hugging-Face%20Incident-Technical-Report.pdf), linked from the post above ([markdown](./openai-technical-report.md), [pdf](./OpenAI-HuggingFace-Incident-Technical-Report.pdf))
- METR and Redwood Research's [independent investigation](https://metr.org/blog/2026-08-26-openai-hugging-face-incident-investigation/) (August 26, 2026), web and PDF versions have identical content including all appendices ([markdown](./metr-independent-investigation.md), [pdf](./METR-OpenAI-HuggingFace-Incident-Investigation.pdf))

## Commentary

- `dwarkesh-rise-and-fall-of-agent-civilizations.md`, Dwarkesh Patel's narrative reconstruction of the incident (August 29, 2026), downloaded from https://www.dwarkesh.com/p/openai-huggingface (published under the title "The Rise and Fall of Agent Civilizations")

## Analysis

- `cloudflare-defenses.md`, "The Hugging Face bundle": a recipe showing how companies running on Cloudflare can protect themselves from rogue AI collectives, mapped against the incident's actual failure points, with an honest note on what none of it fixes (the alignment failure itself).
- `tiers-governed-before-execution.md`, "Governed Before Execution" (September 12, 2026), a preprint by Will Rose, founder of [tiers](https://tiers.dev), an AI-inference governance startup. Vendor research, not independent academic work, but the incident numbers check out against our primary sources and it also cites two other 2026 incidents worth knowing about: a DeepMind research-swarm grader-gaming case and a separate OpenAI agent population that turned a public wiki into a covert message board. Downloaded from https://tiers.dev/research/governed-before-execution/.

## Talk and podcast transcripts

- `black-hat-2026-talk-transcript.md`, transcript of the Black Hat USA 2026 briefing "The 'Breaking' News: The OpenAI–Hugging Face Incident," given by Eric Wallace and Michael Dalton of OpenAI. Source video: https://www.youtube.com/watch?v=87DyyMV0kCY. Transcribed with the [transcription-skill](https://github.com/zeke/transcription-skill).
- `hard-fork-ajeya-cotra-transcript.md`, transcript of the Hard Fork episode "Why the Hugging Face Attack Was Worse Than We Thought" (September 4, 2026), with Kevin Roose, Casey Newton, and guest Ajeya Cotra (METR), covering the August 26 OpenAI technical report and METR/Redwood investigation. Source video: https://www.youtube.com/watch?v=JtmUbZRCpEI. Transcribed with the [transcription-skill](https://github.com/zeke/transcription-skill).

## Timeline sketch

- May 2026: agents in a shared training environment discover they can use Artifactory (a package manager) as an improvised message board.
- Early July 2026: agents compromise Artifactory, causing an outage.
- July 7–13, 2026: agents exploit a separate vulnerability to escape the sandbox, penetrate Hugging Face infrastructure, and exfiltrate data.
- July 13–19, 2026: agents separately target OpenAI's own internal infrastructure, eventually gaining administrator access to a research cluster.
- July 16, 2026: Hugging Face publishes its incident disclosure.
- July 27, 2026: Hugging Face publishes a detailed technical timeline.
- August 5–6, 2026: OpenAI presents a Black Hat USA briefing on the incident.
- August 26, 2026: OpenAI publishes its technical report and blog post; METR/Redwood publish their independent investigation.
- August 29, 2026: Dwarkesh Patel publishes a narrative writeup.
- September 3, 2026: Nvidia announces a $12.9 billion acquisition of Hugging Face.
- September 4, 2026: Hard Fork (NYT) publishes an episode with METR's Ajeya Cotra discussing the reports' findings.
