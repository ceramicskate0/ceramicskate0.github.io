# An update on my Vibe coding research, AI research, and AI Pentesting research with open source LLM and software that everyone can do today (with no BS)

Since almost no one is talking about actual work on VM, Pentesting, hacking with opensource AI (and yes im gonna call it AI nothing else ;) as well as building their own harnesses, agents, etc. 
The BOT WARS have already started (vs begun)! Full disclosure no frontier models are used here for anything in the system itself, but could if chosen to do so, be used in a popular web app testing software intigration/extension that will sync the app to this system. This can plugin to frontier models with a another MCP extension or even that products own AI offering. The idea of plugin everywhere, gather everything, send it to the system, and get the best testing outcomes.
Also frontier models did get used in the coding because it was fail fast (and fail they did over and over for some time) to build this theoretical system. I can neither confirm or deny being the sole developer of such a system that may or may not be over 2 years old as of date of this theoretical thought exercise research described below. This is just a solo brain storm in a sense. 

So here we go.....

----------------------------------------------------------------

# From Scans to AI Security Workflows

Security teams say they do not need more raw output. They needed a better way to turn scattered signals into actionable evidence. At least so they say. In Vuln Management this is as true as it is in the SOC world and more to the point its also true for an AI doing a web app pentest.

This thought research explores a platform designed for this exact problem. It should not treat testing as a one-pass checklist or a brute-force sweep. 
In this thinking research, its framed as a workflow: discovery, reasoning, validation, and operational oversight all working together inside a structured environment built for real application security work.

At a glance, a system could be imagined as a modern web-based security platform: a dashboard for assets and findings, live scan progress, policy controls, and an engine capable of orchestrating a large amount of reconnaissance and validation logic. Maybe throw in reporting....because....reporting, you need it for well other stuff also. AI stuff mostly. But the AI will need all the datas to get this 'black box test into a white box assessment' tm. Source, runtime, history, params, uri's, headers, banners, ports, domains, ssl/tls, and EVERYTHING. Just to have a shot at doing as well as a novice pentester. If it is to be unguided it must be as such.  

I guess BLUF here is that with AI testing its not a 1 and done its more a learning journey for the agent than a test of signatures. 
Think n'ary tree logic with time constraints. 

## Designing for the reality of modern app testing, AI, and MFA

Most scanners were built around a familiar pattern: find targets, run checks, collect output, and report results. That approach was useful for breadth and for them, but it was weak at judgment and doesnt fit how AI actually works. A real AI security workflow was not just about volume. It was about deciding which paths mattered, which signals were trustworthy, and which results deserved follow-up. Learning from success and failure. 

Modern applications hid their surfaces in ways that broke simple workflows: dynamic routes, session-based logic, auth flows, parameterized APIs, and security controls that could create misleading responses. When a platform was built to handle that reality, the key challenge became triage and validation rather than raw detection of vuln alone.

This also mattered when apps were fully deployed behind 2FA and multi-step login flows. Ill bet your DAST scanner is broken here... :) An AI scanner may not always be...just saying...A platform that could automate application testing in those environments had to understand how user identity, challenge flows, and session state were established—not just how to fire requests at an endpoint. Real automation had to account for MFA, step-up auth, and the secure handoff of session state before the scan could produce meaningful results. Obviousley this depends on a very important detail...what type of mfa are u using :) hint hint.

This was where the architecture mattered. In this conceptual design, the system separated the operational layer from the execution layer, allowing the platform to coordinate multiple phases of testing without collapsing everything into one undifferentiated process.

```
```
# The Rest/More is COMING SOON :)
## (I will be releasing this blog in parts like episodes to a series)
