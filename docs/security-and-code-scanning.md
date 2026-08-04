# Security and Code Scanning: How They Interact With AI-Assisted Code

`04-risk-mitigation.md` in the playbook repo covers security risk at the
policy level. This doc covers the specific GitHub-native security tooling
that operationalizes it, and how each interacts with AI-assisted code
specifically, since "run the same security tooling regardless of how code
was authored" is a stated principle in this repo set, but implementing it
well requires understanding what each tool actually catches.

## CodeQL / code scanning

Static analysis that runs against the codebase regardless of authorship.
For an enablement program, the relevant question isn't whether to run it
(it should run unconditionally, per `claude-code-ci.yml` in
`ai-tools-integration-patterns`), it's whether findings correlate with
AI-assistance signal over time. If AI-assisted PRs show a materially
different code-scanning finding rate than hand-written PRs, that's a signal
worth tracking (see `docs/policy-logging.md` in the integration-patterns
repo) and worth feeding back into the training curriculum, since it points
at a specific, addressable gap in developer judgment rather than a generic
"be more careful" message.

## Secret scanning

Catches credentials and secrets committed to a repository, including push
protection that can block a commit before it lands. This is directly
relevant to AI-assisted code for a specific reason: a coding assistant
trained partly on public code may surface patterns that look like
placeholder credentials or hardcoded configuration in a way a careful human
author might avoid by habit. Push protection is a meaningfully stronger
control than post-hoc scanning for this reason, it catches the issue before
merge rather than after, which matters more for AI-assisted commits where
the author may not have written the specific line being flagged.

## Dependabot

Flags known-vulnerable dependencies and can open automated update PRs. The
enablement-relevant angle: an AI coding assistant suggesting a new
dependency or library version is, in effect, making a dependency decision
on the developer's behalf. Dependabot's vulnerability database is the
check against a suggestion that pulls in something outdated or already
known to be problematic, worth explicitly covering in training as "the
tool that catches what the assistant might not know is already flagged."

## Branch protection and CODEOWNERS

Not a scanning tool, but the structural control that ensures none of the
above matters only in theory: branch protection rules requiring passing
status checks (including code/secret scanning) before merge, and CODEOWNERS
ensuring the right human reviews a change to a sensitive path, are what
make "AI-assisted code gets no exemption from review" (a principle stated
throughout this repo set) actually enforced rather than aspirational. An
enablement program that recommends security practices without confirming
branch protection actually requires them is recommending a policy with no
teeth.

## How this ties to a broader security program

Programs focused on open source security specifically (funding secure
maintenance work, running an AI-focused security accelerator for open
source projects) operate one level up from any single repository's
configuration: they're addressing whether the ecosystem a codebase depends
on is itself secure and well-maintained, which is a precondition Dependabot
and code scanning can flag violations of, but can't fix on their own. An
enablement program with visibility into both levels, per-repo security
configuration and ecosystem-level health, can make a stronger case for why
AI-assisted development needs both layers of scrutiny rather than treating
security as satisfied once local scanning is turned on.
