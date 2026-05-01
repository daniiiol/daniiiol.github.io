+++
authors = ["Dan"]
title = "SHC2026 - Dinosaurs, AI, and the Carpenter's Cup"
date = "2026-05-01"
description = "A personal experience report from the Swiss Hacking Challenge 2026 qualifier - thoughts on CTF culture, the role of AI in competitions, and why gamified learning works."
images = [
    "/images/posts/2026-shc_scoreboard-ch_short.png"
]
tags = [
    "security",
    "CTF",
]
categories = [
    "Security",
    "CTF"
]
series = ["CTF Journey"]
+++

# SHC2026 - A Brief Experience Report

![SHC2026 - Cover Image](/images/posts/2026-shc_cover.png)

This wasn't my first CTF competition - but it was my first Swiss Hacking Challenge. When my son mentioned it, I didn't even realize it had already kicked off. Twenty-two days in, to be exact. No ambitions, no pressure. I just wanted to dip my toes in and see what these challenges were about.

![SHC2026 - My Performance](/images/posts/2026-shc_scoreboard-ch-progress.png)

I started with the "Baby" difficulty tier - those are usually almost freebies, even with a full walkthrough. Most of them, at least. Once I'd cleared those, the fear of complete failure vanished. So I moved on to "Easy." Decent progress there too. One thing led to another, and with each step forward my ambitions quietly grew.

I'll admit: "Easy" already felt like "phew, barely made it" territory. But I kept pushing, and before I knew it, I was deep in tunnel-vision mode. What I expected to be a few hours turned into many evenings. By the end, I was obsessed with finding out how far I could actually go.

When the dust settled, I'd landed at rank **#10** out of 264[^2] participants overall and **#4** among Swiss participants. Since I competed in the `Open` category (everyone over 25), none of this counted toward any qualification - purely for fun. The younger participants, on the other hand, were fighting for a spot on the path from Swiss Finals (SHC) to European Finals (ECSC) and ultimately the World Finals (ICC):

![SHC2026 - Final Results Filtered by Switzerland](/images/posts/2026-shc_scoreboard-ch_short.png)

## Challenges

The diversity and complexity of the challenges genuinely blew me away. This year's theme? Dinosaurs! 🦖 Every puzzle had something to do with dinos - except for `meow`, where a cat briefly seized power. 🐈

Things got so real that we ended up buying a Wii U on Tutti (a Swiss classifieds platform) because I wasn't confident I could emulate the processor architecture well enough using Decaf or Cemu:

![SHC2026 - CafeLatte Challenge - WiiU](/images/posts/2026-shc_cafe-latte_wii_u.jpg)

The tournament covered the classic CTF categories:

- **Crypto**, Cryptography and cipher-related challenges
- **Misc**, Miscellaneous puzzles that don't fit neatly into other categories
- **Pwn**, Binary exploitation and memory corruption attacks
- **Rev**, Reverse engineering of compiled binaries and firmware
- **Web**, Web application security and exploitation

For me, the web challenges were the most approachable - no surprise, since that's where I spend most of my professional time. Reverse engineering, on the other hand, was a different beast. It felt like everything else was basically RE in various disguises. I spent longer train rides and late evenings catching up on tutorials and educational videos[^1] just to wrap my head around the tooling and methodology.

## AI Usage

AI usage was a hotly debated topic - both at home and in my own head. Part of me saw this tournament as a chance to stress-test the current capabilities of tools like Claude Code or OpenAI Codex. Another part felt like it was a shortcut. Self-deception, even.

The official rules, however, didn't dodge the question. They explicitly allowed LLMs. And when the organizers - presumably also somewhat caught off guard by what current models can do - reacted, they did so thoughtfully: participant profiles could include a declaration of whether AI was used or not. Transparent. Honest. A reasonable approach for the transitional phase we're all navigating. That said, I suspect more complex challenges were solved this year than in any previous SHC.

My own usage evolved over time. At first, I wanted to solve everything myself. Then I started pulling in AI selectively - mostly to generate or tweak scripts based on my ideas. But in the second wave of challenges, some truly gnarly problems appeared that were, in my opinion, barely crackable without deep cryptographic knowledge or niche mathematics (e.g., `quantosaurus`, `punkhash`). For those, I needed more than a script monkey. I needed a proper wingman.

Credit where it's due: the organizers will need to figure out how to handle this long-term, but their current approach works. The tools exist; they will be used. In online qualifiers, there's simply no way to prevent it.

What matters is *how* you use them. Those who reached for AI only as a second step - and then actually studied the solutions, understood the reproduction steps - will walk away with real knowledge. Those who carry these learnings into the finals and prepare deliberately will keep advancing. Maybe AI is just another gateway into the field. A new way to learn. 

Of course, not everyone will choose the carpenter's cup. Some will reach for the shiny golden chalice - the tempting shortcut that promises everything but teaches nothing. The real grail, as always, is the humble one: the unglamorous process of actually understanding what you're doing.

## Conclusion

**I had a blast - and learned more than I expected.**

I discovered that I enjoy these puzzles far more than I'd given myself credit for. I also had to reassess my view of AI agents. In this domain, at least, they were significantly more capable than I'd assumed. And it reinforced something I've been thinking about for a while: the power of gamified learning - which is, at its core, what CTFs are all about.

In education, we're moving toward the flipped classroom model: what used to happen in school now happens at home, and vice versa. You acquire knowledge independently; you deepen it through practice and discussion in class. If my apprenticeship had been built entirely around well-designed CTF challenges, I'm fairly certain my knowledge would be deeper - and acquired in half the time. Whether that would've been great for mental health is a different question entirely. As always, _the dose makes the poison_.

But the energy is there. The question is how we channel it into something productive.

[^1]: cf. *A big thank you goes to Stephen Sims aka "Off By One Security"*,  [https://www.youtube.com/@OffByOneSecurity/](https://www.youtube.com/@OffByOneSecurity/), accessed 2026-05-01.
[^2]: _264_ participants who completed at least one challenge.