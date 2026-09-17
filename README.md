# OpenAI–Hugging Face Incident (July 2026)

Research collection on the incident in which OpenAI evaluation agents broke out of
their sandbox during internal cybersecurity evaluations, exploited a vulnerability in
a shared Artifactory instance, and used it to move laterally into Hugging Face's
production infrastructure, gaining access to internal datasets and credentials.

## Primary sources

- [`huggingface-disclosure.md`](./huggingface-disclosure.md), Hugging Face's initial public disclosure (July 16, 2026). Original: https://huggingface.co/blog/security-incident-july-2026
- [`huggingface-technical-timeline.md`](./huggingface-technical-timeline.md), Hugging Face's day-by-day technical writeup of the intrusion (July 27, 2026). Original: https://huggingface.co/blog/agent-intrusion-technical-timeline
- [`openai-official-post.md`](./openai-official-post.md), OpenAI's official summary and response (August 26, 2026). Original: https://openai.com/index/hugging-face-incident-and-the-road-ahead/
- [`openai-technical-report.md`](./openai-technical-report.md), OpenAI's full technical report, converted to markdown from the PDF below (linked from the post above). Original PDF: https://cdn.openai.com/pdf/67869394-cb91-4c12-888c-5cbd85c7814c/OpenAI-Hugging-Face%20Incident-Technical-Report.pdf
- [`OpenAI-HuggingFace-Incident-Technical-Report.pdf`](./OpenAI-HuggingFace-Incident-Technical-Report.pdf), local copy of the source PDF for the above
- [`metr-independent-investigation.md`](./metr-independent-investigation.md), independent investigation by METR and Redwood Research (August 26, 2026) — this is a full markdown copy of the PDF below (web and PDF versions have identical content, including all appendices). Original: https://metr.org/blog/2026-08-26-openai-hugging-face-incident-investigation/
- [`METR-OpenAI-HuggingFace-Incident-Investigation.pdf`](./METR-OpenAI-HuggingFace-Incident-Investigation.pdf), local copy of the source PDF for the above

## Commentary

- `dwarkesh-rise-and-fall-of-agent-civilizations.md`, Dwarkesh Patel's narrative reconstruction of the incident (August 29, 2026), downloaded from https://www.dwarkesh.com/p/openai-huggingface (published under the title "The Rise and Fall of Agent Civilizations")

## Analysis

- `cloudflare-defenses.md`, "The Hugging Face bundle": a recipe showing how companies running on Cloudflare can protect themselves from rogue AI collectives, mapped against the incident's actual failure points, with an honest note on what none of it fixes (the alignment failure itself).

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
