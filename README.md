# GitHub-Native AI Enablement

The other repos in this set (`copilot-enterprise-playbook`,
`ai-adoption-metrics`, `ai-tools-integration-patterns`,
`change-management-frameworks`, `skills-readiness-assessment`) are written to
be platform-agnostic: the change management theory and metrics framework
apply whether the tool is GitHub Copilot, Claude Code, or something else
entirely. This repo is the opposite. It's specifically about the parts of an
AI enablement program that only make sense once you're fluent in GitHub's
actual platform surface, not just AI tooling in the abstract.

## Why this repo exists

A program manager can run a technically correct rollout using generic
change-management theory and never once touch the features that make GitHub
specifically, rather than any Git host, the right place to run it. That gap
shows up fast in conversation with anyone who lives inside the platform:
questions about Copilot Enterprise policy controls, how code scanning
interacts with AI-suggested code, or how an accelerator/fund model extends
enablement into the open source ecosystem, don't have generic answers. This
repo is the platform-fluency layer underneath the rest of the set.

## What's in here

```
docs/copilot-enterprise-admin.md         Enterprise policy controls, seat management, exclusions, audit logs
docs/security-and-code-scanning.md       CodeQL, secret scanning, Dependabot, and how they interact with AI-assisted code
docs/actions-for-enablement.md           Using GitHub Actions as the automation backbone of an enablement program
docs/open-source-fund-and-accelerator.md How funding and accelerator models extend enablement into the open source ecosystem
docs/github-education-tie-in.md          How GitHub Education's mission and resources connect to enablement for learners
```

## How this connects to the rest of the set

- The GitHub Actions workflows in `ai-tools-integration-patterns` assume
  familiarity with Actions as a platform; `docs/actions-for-enablement.md`
  here is the "why Actions is the right automation layer" companion piece.
- `06-open-source-community-adoption.md` in `copilot-enterprise-playbook`
  covers the GTM theory for open source populations; this repo's
  `docs/open-source-fund-and-accelerator.md` covers the specific
  GitHub-native mechanisms (funds, accelerators) that operationalize it.
- `07-non-engineer-and-mixed-audience-enablement.md` in the playbook covers
  the change-management theory for learners; this repo's
  `docs/github-education-tie-in.md` covers what that looks like as an
  actual GitHub-native program.

## License

MIT — see LICENSE.
