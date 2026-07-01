+++
authors = ["Dan"]
title = "You don't feel velocity, you feel acceleration"
date = "2026-06-30"
description = "Newton reminds us that a body senses acceleration, not velocity. That is exactly why the AI-driven collapse of exploitation timelines feels so violent, why we have fallen below human reaction time, and why automation kept firmly under human control is the only next step fast enough."
images = [
    "/images/posts/2026-newton-acceleration-social.png"
]
tags = [
    "security",
    "AI",
    "Threat Intelligence",
]
categories = [
    "Security",
    "AI"
]
series = ["Secure-by-default"]
+++

# You don't feel velocity, you feel acceleration

![Newton, acceleration and the Zero Day Clock - Cover Image](/images/posts/2026-newton-acceleration-cover.png)

There is a small, almost philosophical fact buried in classical mechanics that I keep coming back to. Newton's first law says a body in uniform motion stays in uniform motion unless a force acts on it. His second law, `F = m * a`, then tells us what that force actually does. It doesn't produce velocity, it produces *acceleration*. The consequence is stranger than it sounds. You cannot feel velocity at all. You can only feel acceleration, the *change* in velocity.

Sit on a high-speed train gliding along at 300 km/h. Close your eyes. Nothing. Coffee sits still in the cup. The moment the driver brakes, your body knows instantly. Same speed, completely different sensation, because now there is a change.

I think about this constantly when I look at where our industry is right now. Because our threat landscape has been moving fast for years, and for years it felt like almost nothing. What we are feeling *now* is not the speed. It's the acceleration.

## The steady-state trap

For most of the last decade, the "velocity" of the threat landscape was high but roughly constant. Vulnerabilities got disclosed, exploits followed some weeks later, and we built our entire operating model around that comfortable, predictable cadence. Patch within 30 days, run a pentest once or twice a year, schedule the red team engagement for Q3, treat the backlog as technical debt.

And because that velocity was *constant*, we stopped feeling it. We normalized it. This is the deeply human failure mode that Newton predicts. Uniform motion is invisible from the inside. We were on the smooth train, telling ourselves the ride was under control.

It never was. It was just steady. Steady is not the same as safe, but our senses can't tell the difference.

## The acceleration is what we finally feel

Then AI-enabled offense hit the brakes on the whole comfortable model, and suddenly everyone feels the jolt.

The clearest instrument I've found for making that jolt visible is the [Zero Day Clock](https://zerodayclock.com/), a project by Sergej Epp that synthesizes exploitation timelines across 83,000+ CVEs from around ten sources like CISA KEV, ExploitDB and Metasploit.[^1] The headline number is not a speed, it's a derivative, and it is brutal.

- The median time between a vulnerability going public and someone exploiting it has fallen from roughly **84 days in 2021** to a matter of **hours today**, and the project openly projects the curve bending toward **one minute**.[^1][^2]
- The share of exploits that land as true zero-days, in the wild *before* any advisory exists, has climbed from around **31%** a few years ago to **73.2%**.[^1]

Look at those two facts together. Not only is the window collapsing, the majority of exploitation is now happening before we even get the disclosure that our whole patch-cycle operating model depends on. The train didn't just speed up. The tracks changed shape.

And this isn't hypothetical AI hand-waving. Independent researchers have turned single flaws into dozens of working exploits for a few dollars in compute. I've written before about how cheap discovery has become and what it does to defenders.[^3] The point of the Zero Day Clock is that it turns that anecdote into a trend line.

## Verifier's Law, or why the acceleration only points one way

Epp frames the underlying asymmetry as a kind of *Verifier's Law*. Offense has cheap, deterministic validators, either you got a shell or you didn't, while defense lives with expensive, ambiguous validation.[^2] An attacker's AI agent gets instant binary feedback and can iterate a thousand times overnight. A defender's signal is fuzzy, slow, and drowning in noise.

That asymmetry is exactly why AI accelerates the offensive frame harder than the defensive one. The force is applied unevenly, so the acceleration is unevenly felt. Same physics, but only one body is really being pushed.

## We have fallen below human reaction time

Here is the number that should reframe the whole strategy discussion. When median time-to-exploit is measured in hours and bending toward minutes, we have quietly crossed a line. We are now below human reaction time. Not below "a human working quickly" time, but below the time it takes to page someone, brief them, get an approval and act. A defensive loop with a human in the critical path can no longer close fast enough.

So automation stops being an optimization and becomes the only clock fast enough to matter. Detection, triage, validation and a growing slice of response and patching have to run at machine speed, because the other side already does. There is no way around it.

But this is also where the next class of attacks will be aimed, and it's the part I care about most. The moment my pipeline decides on its own, it becomes a target. AI-driven adversaries won't just race my patch cycle, they will try to turn my automation against me. They poison the signals it learns from, nudge it into quarantining the wrong asset, weaponize an over-eager auto-remediation into the very outage they wanted. Hand over the wheel without hardening it and you haven't removed the single point of failure, you've relocated it.

So the real challenge of this era isn't "automate more." It's automating well enough that the human keeps genuine control and the automation can't be subverted. Machine speed for the reflex, human judgment for the intent. Human-in-the-loop, never human-out-of-the-loop.

Building automation that is fast, controllable *and* attack-resistant is exactly the standing work a Purple Team does alongside the Blue Team.[^3] Build the automated response, attack it, harden it, then check that a human could still take back the controls under pressure. That is the real work sitting in front of us.

## The models won't decelerate for us

Newton's quiet lesson is that our perception is wired for change, not for state. That is a wonderful survival trait on the savannah and a dangerous blind spot in cybersecurity, the same one that spins a disoriented pilot into the ground, gently banking on an inner ear that only registers change while the instruments scream the truth. We notice the collapse now only because it still hurts. Soon it will fade into the quiet of a new normal, and that is precisely the moment we have to be ready for.

But here is the hopeful part. Maybe this was never a crisis so much as a step we had put off for too long. Our senses stopped being enough a long time ago; we just were never forced to admit it. Letting machines hold the reflexes while we keep the judgment is less a rescue than the next stage we were always going to have to grow into. The window has collapsed, whether or not your inner ear agrees. The reassuring part is that we are, finally, evolving to match it.


[^1]: cf. _Zero Day Clock_, [https://zerodayclock.com/](https://zerodayclock.com/) and _The Collapse_, [https://zerodayclock.com/collapse](https://zerodayclock.com/collapse), accessed 2026-07-01. Project by Sergej Epp; median time-to-exploit trend, zero-day share and CVE corpus size as reported there.

[^2]: cf. _Before the Breach: The Zero Day Clock and the Race Against Exploitation_, [https://www.resilientcyber.io/p/before-the-breach-the-zero-day-clock](https://www.resilientcyber.io/p/before-the-breach-the-zero-day-clock), accessed 2026-07-01, on Verifier's Law and the disclosure-to-patch gap. See also _AI shrinks zero-day exploit time from a year to a single day_, Tom's Hardware, [https://www.tomshardware.com/tech-industry/cyber-security/zero-day-clock-visualizes-and-quantifies-the-effects-of-ai-on-software-security-time-until-exploit-went-from-one-year-to-one-day-and-projected-to-be-one-minute-soon-enough](https://www.tomshardware.com/tech-industry/cyber-security/zero-day-clock-visualizes-and-quantifies-the-effects-of-ai-on-software-security-time-until-exploit-went-from-one-year-to-one-day-and-projected-to-be-one-minute-soon-enough), accessed 2026-07-01.

[^3]: See [Why I would build a purple team right now](/posts/2026-purple-teaming/) and [Are we unlearning how to understand?](/posts/2026-bugbounty-pentesting-ctf-and-ai/).