+++
authors = ["Dan"]
title = "Purple. The third color your organisation needs right now"
date = "2026-05-09"
description = "Why AI-accelerated discovery is outpacing defence, and how a standing Purple Team bridges the gap between Red and Blue."
images = [
    "/images/posts/2026-purple-teaming-social.png"
]
tags = [
    "security",
    "Chaos Engineering",
    "PurpleTeaming",
]
categories = [
    "Security",
    "Chaos Engineering"
]
series = ["Secure-by-default"]
+++

# Why I would build a <span style="color:#8b5cf6">purple</span> team right now

![Purple Teaming - Cover Image](/images/posts/2026-purple-teaming-cover.png)

I've been banging the "Purple Teaming" drum for years. It's a niche term, even inside cybersecurity circles, and most people I talk to either haven't heard of it or shrug it off as just another buzzword. I get it. But I genuinely believe it's one of the most underestimated capabilities an organisation can have. And recent developments have only made that conviction stronger.

## The current challenge

The wind has shifted. Finding vulnerabilities isn't the bottleneck anymore. Fixing them fast enough is.

OpenAI's official cyber evaluation describes GPT-5.5 as a model with high cyber capability.[^4] The UK AI Security Institute rated it as the strongest performer they've ever seen on their cyber tasks.[^2] Anthropic documents Claude Mythos Preview finding zero-days in major operating systems and browsers.[^5] Let that sink in for a moment.

The conclusion? Discovery got cheaper. A lot cheaper. And if I don't speed up my defence now, I'm going to lose the economic race against AI-augmented offence.

This isn't just marketing talk. I've written about these dynamics in previous posts[^1] and tested them extensively myself. Frontier models are already very good at systematically uncovering patterns, weak code paths and misconfigurations. Even where fully automated exploits are still unreliable, the sheer speed-up in analysis is enough to pile serious pressure on defenders. 

Meanwhile, the inbound volume just keeps growing. NIST had to adjust its NVD workflows in 2026 because a massive backlog had piled up since early 2024.[^3] On 9 May 2026, the NVD dashboard showed 349,324 CVEs total, with 1,506 still «Awaiting Enrichment» and a staggering 66,726 «Not Scheduled». HackerOne[^6] reports an incredible surge in valid AI-assisted vulnerability findings and a lot valid reports from autonomous agents alone.

So what happens with all these reports? They pile up. Coordination bodies and vendors simply can't process them fast enough. But the models keep finding vulnerabilities regardless. When one researcher finds something, a second and third will land on the same result for the same target. Zero-day discovery is no longer "unique within a processable timeframe" for a vendor. I have to assume zero-days are now being found by many people simultaneously. The pressure on patch suppliers is going to increase massively. And here's the uncomfortable part: before a zero-day is officially recognised, my systems may already be under attack, even though I haven't received any indication that a patch is missing.

But the risk isn't just about the spectacular zero-day. It's also about the poorly handled one-day. When current models can translate CVE texts, advisories, patch diffs and PoCs into exploitable knowledge faster than ever, my window between disclosure and abuse shrinks. We need to start treating unpatched, publicly described vulnerabilities like operational incidents, not technical debt. The friction for attackers keeps dropping. My backlogs can quickly become attack paths.

### So why isn't a traditional Red Team (pentesters, bug bounty, etc.) and a traditional Blue Team (e.g. SOC) enough? Why the third color?

Red Teams are great at finding paths and proving control failures. Blue Teams are great at telemetry, detection and response. What's missing in the AI era is the *standing function* in between. A Purple Team isn't just a coordination meeting. It's a continuous, internal Red Team with a delivery obligation. It actively hunts for weaknesses, accepts external inputs from VDPs, bug bounties, advisories and threat intelligence, and it doesn't stop at the PoC. It supports Blue with detection checklists, hardening measures, reproduction steps and when needed, concrete code fixes or patch recommendations. That's where Purple is uniquely positioned. 

### What does this team actually need? 

Offensive thinking, solid debugging, code literacy, cloud and platform knowledge, and above all: **empathy**. The kind of empathy it takes to sit down with a dev team that's already under pressure, explain a finding without finger-pointing, and translate it into a task they can actually act on. Without that, even the best findings die in a backlog. 

What I care about most is using the same AI tools defensively to close the gap a little. I have models pinpoint code paths, explain root causes, sketch patch options, review diffs, prepare regression tests and draft detection rules. Official programmes from OpenAI[^4], Microsoft[^7] and Anthropic[^5] now explicitly describe exactly these kinds of defensive workflows.

Models help speed things up, but never without human review, a clear scope and a controlled environment. The gap can't be closed entirely.

### Making it real

I'll admit: I personally dislike KPIs 🦦. But since one or two managers are bound to read this, let me not dodge the topic. I'd measure a Purple Team not by report count but by the speed of risk reduction. My core KPIs: 

- Time to Acknowledge
- Time to Validate Exploitability
- MTTR for validated internet-exposed findings 
- Percentage of KEV-adjacent risks mitigated within SLA
- Percentage of prioritised ATT&CK techniques with productive detection 
- Regression rate after fix 

The build-up has to stay pragmatic. Size the team according to risk and complexity, but honestly, you can start with 1-2 FTEs. The organisation will notice quickly what these people deliver, uncover and implement. They won't just flag missing patches the way a traditional SOC would. They'll hand over mitigation measures and concrete recommendations on the spot. **But:** There is no US versus THEM. Just one team in the same boat. Exactly what you'd expect from a true enabling team.

## Team comparison
The table below is my operational distillation from MITRE's ATT&CK-oriented Purple Teaming and the validation headaches HackerOne[^6] describes around AI-generated vulnerability reports.

| Team | Primary Responsibility | Typical Deliverables | Weakness in the AI Era |
|---|---|---|---|
| Red Team | Find attack paths, prove control failures, surface real weaknesses | Campaign reports, PoCs, attack chains, prioritisation recommendations | Often episodic; strong at proving issues, weaker at sustained fix throughput |
| Blue Team | Detect, respond, monitor, harden | Alerts, playbooks, dashboards, detection use cases, telemetry | Sees a lot but struggles to cleanly prioritise AI-generated noise and new findings without validation |
| Purple Team | Validate as an internal Red Team, ingest external inputs, support Blue, accelerate fixes | Validated findings, detection & hardening checklists, ATT&CK mappings, patch/code-fix proposals, retest reports, vendor communication | Primarily fails when an official mandate is missing or silo thinking persists in the organisation |

## The models won't wait. Neither should your defence.

Discovery is getting cheaper by the month. The backlog is growing. The window between disclosure and exploitation is shrinking. None of this is going to slow down. A Purple Team won't magically fix all of that, but it's the closest thing I've seen to a function that can actually keep up: validate fast, fix fast, learn fast. 

Start small. Two people, a clear mandate, and a shared inbox. You'll be surprised how quickly the rest of the organisation starts pulling in the same direction.


[^1]: See [Are we unlearning how to understand?](/posts/2026-bugbounty-pentesting-ctf-and-ai/) on how AI is reshaping pentesting and bug bounty, [SHC2026 - Dinosaurs, AI, and the Carpenter's Cup](/posts/2026-swisshackingchallenge2026-qualifier-journey/) for first-hand experience with AI agent capabilities in CTF challenges, and [Back on the Other Side](/posts/2025-bug-bounty-journey/) for context on the manual effort AI is now augmenting.

[^2]: cf. _External Evaluations for Cyber Capabilities - UK AISI_, [https://deploymentsafety.openai.com/gpt-5-5/external-evaluations-for-cyber-capabilities---uk-aisi](https://deploymentsafety.openai.com/gpt-5-5/external-evaluations-for-cyber-capabilities---uk-aisi), accessed 2026-05-09.

[^3]: cf. _NIST Updates NVD Operations to Address Record CVE Growth_, [https://www.nist.gov/news-events/news/2026/04/nist-updates-nvd-operations-address-record-cve-growth](https://www.nist.gov/news-events/news/2026/04/nist-updates-nvd-operations-address-record-cve-growth), accessed 2026-05-09.

[^4]: cf. _OpenAI GPT-5.5 Trusted Access for Cyber_, [https://openai.com/index/gpt-5-5-with-trusted-access-for-cyber/](https://openai.com/index/gpt-5-5-with-trusted-access-for-cyber/), accessed 2026-05-09.

[^5]: cf. _Anthropic Red Team - Claude Mythos Preview_, [https://red.anthropic.com/2026/mythos-preview/](https://red.anthropic.com/2026/mythos-preview/), accessed 2026-05-09.

[^6]: cf. _HackerOne - Hacker-Powered Security Report_, [https://www.hackerone.com/report/hacker-powered-security](https://www.hackerone.com/report/hacker-powered-security), accessed 2026-05-09.

[^7]: cf. _Microsoft - Analyzing Open Source Bootloaders: Finding Vulnerabilities Faster with AI_, [https://www.microsoft.com/en-us/security/blog/2025/03/31/analyzing-open-source-bootloaders-finding-vulnerabilities-faster-with-ai/](https://www.microsoft.com/en-us/security/blog/2025/03/31/analyzing-open-source-bootloaders-finding-vulnerabilities-faster-with-ai/), accessed 2026-05-09.