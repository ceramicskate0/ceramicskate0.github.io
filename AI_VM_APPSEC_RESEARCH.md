# An update on my Vibe coding research, AI research, and AI Pentesting research with open source LLM and software that everyone can do today (with no BS)

Since almost no one is talking about actual work on VM, Pentesting, hacking with opensource AI (and yes im gonna call it AI nothing else ;) as well as building their own harnesses, agents, etc. 
The BOT WARS have already started (vs begun)! Full disclosure no frontier models are used here for anything in the system itself, but could if chosen to do so, be used in a popular web app testing software intigration/extension that will sync the app to this system. This can plugin to frontier models with a another MCP extension or even that products own AI offering. The idea of plugin everywhere, gather everything, send it to the system, and get the best testing outcomes.
Also frontier models did get used in the coding because it was fail fast (and fail they did over and over for some time) to build this theoretical system. I can neither confirm or deny being the sole developer of such a system that may or may not be over 2 years old as of date of this theoretical thought exercise research described below. This is just a solo brain storm in a sense. 

So here we go.....

Oh also, from now on when I use AI or some simlar word it is safe to assume the phrase to mean open source AI.

----------------------------------------------------------------

# From Scans to AI Security Workflows

Security teams say they do not need more raw output. They needed a better way to turn scattered signals into actionable evidence. At least so they say. In Vuln Management this is as true as it is in the SOC world and more to the point its also true for an AI doing a web app pentest.

This thought research explores a platform designed for this exact problem. It should not treat testing as a one-pass checklist or a brute-force sweep. 
In this thinking research, its framed as a workflow: discovery, reasoning, validation, and operational oversight all working together inside a structured environment built for real application security work.

At a glance, a system could be imagined as a modern web-based security platform: a dashboard for assets and findings, live scan progress, policy controls, and an engine capable of orchestrating a large amount of reconnaissance and validation logic. Maybe throw in reporting....because....reporting, you need it for well other stuff also. AI stuff mostly. But the AI will need all the datas to get this 'black box test into a white box assessment' tm. Source, runtime, history, params, uri's, headers, banners, ports, domains, ssl/tls, and EVERYTHING. Just to have a shot at doing as well as a novice pentester. If it is to be unguided it must be as such.  

I guess BLUF here is that with AI testing its not a 1 and done its more a learning journey for the agent than a test of signatures. 
Think n'ary tree logic with time constraints. 

## Designing for the reality of modern app testing, AI, and MFA

Most scanners were built around a familiar pattern: find targets (or be given), run checks, collect output, and report results. That approach was useful for breadth and for them, but it was weak at judgment and doesnt fit how AI actually works. A real AI security workflow was not just about volume. It was about deciding which paths mattered, which signals were trustworthy, and which results deserved follow-up. Learning from success and failure. 

Modern applications hid their surfaces in ways that broke simple workflows: dynamic routes, session-based logic, auth flows, parameterized APIs, client side code, and security controls that could create misleading responses. When a platform was built to handle that reality, the key challenge became triage and validation rather than raw detection of vuln alone.

This also mattered when apps were fully deployed behind 2FA and multi-step login flows. Ill bet your DAST scanner is broken here... :) An AI scanner may not always be...just saying...A platform that could automate application testing in those environments had to understand how user identity, challenge flows, and session state were established—not just how to fire requests at an endpoint. Real automation had to account for MFA, step-up auth, and the secure handoff of session state before the scan could produce meaningful results. Obviousley this depends on a very important detail...what type of mfa are u using :) hint hint.

This was where the architecture mattered. In this conceptual design, the system separated the operational layer from the execution layer, allowing the platform to coordinate multiple phases of testing without collapsing everything into one undifferentiated process.

## Automated AI scans with 2FA/MFA

The strongest security testing platforms dont (or shouldnt) stop at “happy path” testing. Or im sorry if this is you...unauth testing. They also have to work when an application was protected by real-world authentication controls, especially 2FA/MFA. In the research, that meant the system would need to capture and maintain (only when it needed it) the right auth context, handle lockouts sensibly, and continue the scan without breaking the user experience or invalidating the target’s protections.

That was the difference between a older scanner's and this research's workflow. A true automation layer could be imagined as handling login-driven surfaces, challenge-based flows, and protected application states, then continuing with discovery and validation where the user had explicitly authorized the test. This was especially relevant when the application was fully deployed with 2FA enabled and the testing had to reflect the same conditions a legitimate pentester would encounter. 

The research's result should be a scan engine that could move from login to authenticated app testing and deep validation, all while respecting the target’s access controls and avoiding blind probes that created noise instead of signal (think, pray and spray FP's). Allowing for auth scans even on a schedule with MFA and maintain a authentication context in the scan for things like...dynamic priv esc testing etc (think isadmin=true or hijacking, or replays, or even lets say maybe the use of a headless browser etc)... Now there may be some other people research out there on this topic and specifically the use of a little known lib that allows for this but right now i simply cant recall...

## An execution model built for long-running analysis

A pentest was rarely a single action. It opften times begins with discovery, proceeded through targeted testing, and then entered a validation stage before any output was treated as a confident finding. Each step needed different evidence, different constraints, and different decision logic.

A good interface could make that lifecycle visible. A user could see scan state, target reachability, live progress, and the current testing phase in a way that supported operational awareness rather than blind execution. This was essential when a test might span several classes of findings, multiple attack surfaces, and iterative analysis loops.

A scan progress view would not just a status panel. It would be a visible expression of the platform’s design philosophy: security work was a sequence of decisions under uncertainty, and those decisions needed to be traceable.

## Discovery that adapted instead of repeating itself

A common failure mode in testing systems was stale discovery: the same paths were revisited, the same surface was re-scanned, and new areas remained invisible because the system was relying on a fixed sequence. This theoretical platform could avoid that problem by making discovery adaptive. ollama show qwen2.5-coder:8b


Instead of following a narrow static playbook, this system could evaluate the target environment and the signals it had already observed. It could ingest traffic patterns, inspect parameters, follow likely application paths, and decide which areas should be explored next. In practical terms, discovery became a form of reasoning rather than a hardcoded workflow.

That mattered because modern attack surfaces were rarely static. They shifted with auth state, API behavior, dynamic content, and infrastructure controls. The right system was one that could react to what it learned rather than repeating the same checks on the same routes.

## AI as an tester, not a wildcard

This research effort could use AI in a way that was much more grounded than the common “fully autonomous scanner” trope. It did not simply let a model run free across a target. Instead, it used model-driven reasoning inside a controlled testing system with guardrails for scope, validation, and evidence.

This was a critical distinction. AI was most valuable when it augmented the analyst’s judgment rather than replacing the boundaries of the system itself. The platform asked the model to reason about the current target context, identify likely vulnerability classes, and decide which signals deserved attention.

That reasoning was then structured around bug-class decomposition. Rather than asking the model to make broad, shallow conclusions across every type of issue at once, it narrowed the task to focused classes and then evaluated the results in context.

The AI pipeline was not just a feature; it was a disciplined workflow for decomposing complexity into manageable reasoning units.

```
```
# The Rest/More is COMING SOON :)
## (I will be releasing this blog in parts, at random, like episodes to a series)
[back](./)
