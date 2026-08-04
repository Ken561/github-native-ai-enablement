# GitHub Education as an Enablement Channel

`07-non-engineer-and-mixed-audience-enablement.md` in the playbook repo
covers the change-management theory for teaching AI tool literacy to
learners and non-engineers. This doc covers the operational piece: how an
education-focused program, reaching students, self-taught developers, and
educators, functions as an enablement channel with a different shape than
an enterprise internal rollout or an open source fund.

## Why education is a distinct channel, not a smaller version of enterprise rollout

An enterprise rollout works with a bounded, known population and can lean
on manager sponsorship. An education-focused program works with an
unbounded, self-selecting population: students and self-taught developers
discover the tool through curricula, course materials, and instructor
recommendation, not through an org chart. The playbook's "slow down the
tiering" principle applies here more than anywhere else in this repo set,
this is the population furthest from the "already has professional coding
judgment" assumption most of the rest of this repo set is built on.

## Instructor and curriculum reach as the real distribution mechanism

The highest-leverage lever in an education channel isn't reaching students
directly, it's reaching the instructors and program leads who build
curricula, the same dynamic as the maintainer-credibility point in
`docs/open-source-fund-and-accelerator.md`, translated to an educational
context. An instructor who incorporates a tool thoughtfully into a course
(with the verification-first, "explain why" framing from the playbook's
non-engineer doc) reaches an entire cohort of students with an approach
that's already been vetted for pedagogical soundness, rather than students
encountering the tool ungoverned and forming habits nobody designed for.

## Free or discounted access as a structural enabler

Cost is a more binding constraint for students and self-taught learners
than for an enterprise population where licensing is a line item someone
else approves. A meaningful student/education access program isn't just
goodwill, it's the access-removal step that makes every other part of this
channel possible; a technically excellent curriculum aimed at a population
that can't get access to the tool doesn't produce adoption.

## Community and mentorship structures

Beyond curriculum and access, community programs (mentorship, peer
learning groups, hackathon-style events) serve the same function as the
internal champions network in `01-rollout-strategy.md`: a peer, not a
program team, answering the next question and modeling good practice. For
a self-selecting population without an org chart, this peer structure is
often the *only* reinforcement mechanism available, there's no manager to
protect training time or reinforce good habits, which makes community
structure not a nice-to-have but the primary Reinforcement-stage mechanism
(in ADKAR terms) for this population.

## Connecting this back to enterprise enablement

This isn't a purely external concern for an internal enablement program.
Interns and new graduates entering an organization arrive having already
formed habits, good or bad, from whatever exposure they had to AI coding
tools during their education. A program that understands the education
channel can calibrate onboarding for early-career hires more accurately: a
new hire from a program that taught verification-first practices needs a
different onboarding emphasis than one whose only exposure was unguided,
low-friction acceptance of suggestions with no habit of scrutiny built in.

## Measuring an education channel

Similar caution as the fund/accelerator doc: raw usage numbers in an
education context can be misleading in the other direction from an
enterprise rollout. High usage without the verification habits described in
the playbook's non-engineer doc isn't a success metric, it's a leading
indicator of exactly the over-trust risk that doc warns about. The more
meaningful signal is qualitative: are instructors reporting that students
can explain what a suggestion does and why it's right, not just that they
accepted it.
