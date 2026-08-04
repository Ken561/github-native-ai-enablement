# Funds and Accelerators as GitHub-Native Enablement Mechanisms

`06-open-source-community-adoption.md` in `copilot-enterprise-playbook`
argues that funding maintainers is itself a GTM mechanism, not a separate
grant program bolted onto adoption. This doc is the operational companion:
how a fund or accelerator model actually works as an enablement channel,
using structures GitHub itself runs as the reference point.

## The mechanism, generally

A fund or accelerator model works because it solves the actual bottleneck
in open source adoption identified in the playbook doc: unpaid maintainer
time. Rather than marketing a tool at maintainers and hoping for organic
adoption, the program directly funds a maintainer's time to integrate,
document, and report back on using the tool against their own project. This
produces three things a marketing budget spent elsewhere can't:

1. **Genuine, project-specific proof points**, written by the maintainer in
   their own words, in their own project's actual context, which carries
   far more credibility with other maintainers than vendor-produced content
2. **Compensation for the real bottleneck**, maintainer time, rather than
   compensation for something that was never actually scarce (awareness)
3. **A structured cohort for feedback**, funded participants have a natural
   reason to report back on friction, gaps, and what actually worked, which
   functions as a distributed, credible version of the Phase 1 pilot
   feedback loop described in `01-rollout-strategy.md`

## Security-focused funds as a specific pattern

A fund explicitly focused on securing critical open source infrastructure
(rather than a general innovation or feature-adoption fund) targets a
different, and in some ways higher-leverage, adoption angle: it funds
maintainers to do security-hardening work that's chronically underfunded
across the ecosystem, and AI tooling that materially helps with that work
(vulnerability triage, dependency updates, code review assistance) earns
adoption through solving a problem maintainers already have, rather than
through being pitched as a new capability they need to learn to want.

## Accelerator models for AI-specific adoption

Where a fund typically supports ongoing maintenance work, an accelerator
model is usually structured as a defined cohort and timeframe, projects
selected to work intensively with a tool or capability (in this case, AI
integration specifically) over a set period, often with direct support,
mentorship, or technical assistance beyond just funding. This maps closely
onto the Phase 1 pilot structure in the enterprise playbook, deliberately
recruited, well-supported, short-timeframe, but built for an open source
population instead of an internal one, with visible outputs (what did this
project build, what did they learn) as the mechanism for spreading adoption
to projects that weren't part of the cohort.

## Why this belongs in an enablement program's toolkit, not just a grants team's

The natural organizational instinct is to treat funding/accelerator
programs as adjacent to enablement, run by a different team with a
different mandate. The case against that: the fund or accelerator cohort
is, functionally, the open source equivalent of the pilot champions
network described throughout this repo set. An enablement program that
doesn't coordinate with, or actively use, these mechanisms is leaving its
highest-credibility distribution channel for open source adoption
unmanaged, run by people who may not be thinking about it as an adoption
lever at all.

## A note on measuring this well

Standard adoption metrics (`ai-adoption-metrics`) don't capture a fund or
accelerator's real impact, the direct participant count is usually small.
The metric that matters is downstream: did funded/accelerated projects
produce content, documentation, or visible integration work that measurably
influenced adoption in projects *outside* the cohort. That's a harder
metric to capture cleanly, but it's the one that reflects whether the
program is actually functioning as a distribution mechanism rather than
just a grants line item.
