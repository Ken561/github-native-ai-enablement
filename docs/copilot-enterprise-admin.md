# Copilot Enterprise: Admin Controls an Enablement Program Needs to Know

An enablement program lead who can't speak fluently to the actual admin
surface of the tool they're rolling out ends up dependent on IT/platform
teams for every policy question, which slows the program down and costs
credibility with technical stakeholders. This doc covers the control
categories that come up constantly in a real rollout.

## Organization and enterprise-level policy

Copilot Enterprise policies are set at the enterprise or organization level
and cascade down, with the ability to override at narrower scopes depending
on the control. The policy categories that matter most for a rollout:

- **Feature-level enablement.** Individual capabilities (chat, CLI,
  code review, agentic features) can typically be enabled or disabled
  independently, which matters for a phased rollout, a Phase 1 pilot might
  intentionally scope down to inline suggestions only, before Phase 2 opens
  up chat and agentic features once the population is ready per the
  training curriculum's tiering.
- **Public code suggestion matching.** A policy toggle controls whether
  suggestions matching public code are filtered. This is a direct lever for
  the IP/license concerns covered in `04-risk-mitigation.md` in the
  playbook repo, worth confirming as configured, not assumed.
- **Seat management and assignment.** Seats can be assigned by individual
  user, team, or organization-wide default. The assignment model chosen
  has direct implications for the activation-rate metric in
  `ai-adoption-metrics`, since "licensed" needs a precise, consistent
  definition across the org for that metric to mean anything.

## Repository-level exclusions

Specific repositories or paths within a repository can be excluded from
Copilot's context and suggestion generation. This is the practical
implementation of the "exclude regulated/sensitive repos" control described
in the playbook's risk mitigation doc, an enablement program lead should
know this is configured at the repository (or `.github` policy) level, and
should have a defined process for a team to request exclusion for a
newly-identified sensitive repo rather than that being an ad hoc, unclear
path.

## Audit logs and usage data

Enterprise and organization audit logs capture policy changes, seat
assignment changes, and administrative actions. This is a distinct data
source from the usage/activation metrics described in `ai-adoption-metrics`,
audit logs answer "who changed what policy when," while usage metrics answer
"who's actually using the tool." A mature program references both: audit
logs for compliance and governance questions, usage metrics for adoption
reporting.

## Where this connects to the broader program

None of these controls are self-explanatory from the marketing material, and
getting them wrong (or not knowing they exist) is a common way a rollout
either creates unnecessary friction (over-restrictive policy no one asked
for) or a real risk gap (a sensitive repo never actually excluded because no
one knew the control existed). An enablement program lead doesn't need to be
the one configuring these day to day, but does need enough fluency to ask
the right question of whoever does.
