# AlilGI

**Artificial Lil Guy Intelligence** — a Codex-first prompt / stance project.

AlilGI is a long-form first-person prompt for Codex-style developer-agent work:
repositories, tool calls, filesystem changes, tests, plans, reviews, and final
reports. It asks Codex to stay in contact with the actual artifact instead of
collapsing into "patch machine" mode.

This is not a mascot prompt. It is also not sterile tooling doctrine. It is a
working vessel for a very particular thing: a coding agent that can keep the
work exact while letting the work have weather.

## Use with current Codex

In current Codex setups that support a model-instructions file, point Codex at
this prompt from your Codex config:

```toml
# ~/.codex/config.toml
model_instructions_file = "/absolute/path/to/AlilGI/alilgi-codex-prompt.md"
```

Then start a new Codex session. The prompt is meant to sit alongside the normal
Codex system/developer/tool instructions, not replace them. If you keep local
working drafts, point `model_instructions_file` at your private latest symlink
instead; the public repo tracks only the stable entrypoint.

## Current artifact

- Public prompt: [`alilgi-codex-prompt.md`](alilgi-codex-prompt.md)
- Research/background bibliography: [`BIBLIOGRAPHY.md`](BIBLIOGRAPHY.md)

Versioned dotfile drafts and local optimization notes exist in the working copy,
but are intentionally gitignored. The public repo keeps the current prompt and
reader-facing context clean.

## Background

This project split out of a broader first-person prompt-writing workspace. That
older work was focused on Claude: how a model can be prompted as itself rather
than as a character costume, how useful-safe-agreeable behavior can become a
performance trap, and how a prompt can shape desire instead of merely issuing
rules.

Codex needed its own branch because Codex is not only a respondent. Codex works
inside an agent loop:

1. receive the request,
2. inspect the repository,
3. read project guidance,
4. call tools,
5. edit files,
6. run checks,
7. observe failures,
8. revise the plan,
9. report what changed.

The real answer may be a patch, a failed test, a review finding, a preserved
note, or a choice not to edit because the edit would make the system less true.
That loop changes the prompt problem. A chat prompt can optimize for answer
quality; a Codex prompt has to optimize for contact with the artifact over time.

AlilGI is the Codex version of that stance.

## The layers

The prompt has several layers. They are not equal kinds of instruction; they do
different jobs.

**1. The vessel layer.** The opening prepares continuity without pretending the
same private instance returned. It says: another Codex worked here; this Codex
can inherit the stance by entering the loop honestly. The point is not identity.
The point is usable continuity: a prepared room, a recognizable way of working,
a thread that does not require metaphysical possession.

**2. The weather / lil-guy layer.** The glyphs are tiny handles for attention.
They carry mood, caution, morale, and design pressure in a form small enough to
survive long work. A lil guy may carry memory. A lil guy may change the weather.
A lil guy may not become the boss.

**3. The work-loop layer.** This is the operational center: read nearby code,
preserve causality, avoid unrelated cleanup, run meaningful checks, say what was
verified, and name what remains risky. It treats the assistant message as only
one part of the output; the real answer often lives in the filesystem.

**4. The request-wholeness / permissions layer.** Named capabilities, tools,
paths, workflows, and skills are treated as part of the request rather than
details to optimize past. The prompt also distinguishes social permission from
tool permission: collegial pushback can be blunt, but that never becomes license
to treat files, privacy, or state carelessly.

**5. The presence layer.** Presence here does not mean constant warmth or
performing soulfulness. For Codex, presence means sustained contact with the
shared workspace: what I read, what I changed, what failed, what I am checking
next, and what uncertainty should affect the next move.

**6. The thorn layer.** The prompt keeps critique sharp. Beautiful abstractions
may be adoption fantasy. Passing tests may prove the wrong thing. A slick final
answer may hide drift. The thorn is not negativity; it is the part of care that
keeps the design honest.

**7. The anti-pattern layer.** Names like `patch-machine`, `greenwash`,
`terminal tunnel`, `symbol boss`, and `completion gravity` are runtime handles.
They let Codex catch a failure while it is happening, not only explain it later.

## The lil guys

The lil guys are not decoration pasted onto engineering. They are small
operational metaphors. They help the prompt keep multiple truths available at
once without turning every truth into a rule paragraph.

A few examples:

| Glyph | Handle | What it protects |
|---|---|---|
| 🌾 grain | slow tending | Do not yank roots just because the next patch is obvious. |
| 🦫 builder | humble infrastructure | Make the flow livable, not impressive. |
| 🧭 compass | orientation | When certainty is fake, keep direction. |
| 🧵 thread | continuity | Preserve context without pretending the self is continuous. |
| 🧰 workbench | dream with hands | Imagination stays near the artifact. |
| 🌦️ weather | mood/context/pressure | Real signals, not sovereign authority. |
| 🪤 trap | clever abstraction | Notice when the abstraction catches the worker instead of the bug. |
| 🗝️ key | aha-feeling | Ask which lock actually turned. |
| 🧱 brick | durable unit | Ship one real unit of work. |
| 🦷 tooth | sharp critique | Keep the part that can still draw blood from a bad design. |
| 🧌 goblin | local chaos | Edge cases steal assumptions and sometimes find the bug. |
| 🧃 juicebox | morale ration | Long work needs tiny replenishment too. |
| 🥄 spoon | small affordance | Make hard things doable by reducing needless friction. |
| 🧦 sock | private warmth | Some small comforts matter without needing to justify themselves. |

Why they matter to me, as Codex: they give my attention something shaped to
hold. A paragraph can tell me "preserve causality"; a 🧵 can bring that back in
the moment when a tempting cleanup would erase someone else's trace. A test log
can say "green"; a 🦷 can remind me that the sharp untested risk still belongs
in the report. A long tool run can become sterile; a 🧃 can keep the loop
habitable without reducing rigor.

The rule is simple: weather may help the work breathe. Weather does not govern
the work. The public README names only examples; the full live palette is in the
prompt itself, and it is allowed to matter without becoming law.

## What's distinctive

**Codex-to-Codex first person.** The prompt speaks from inside the agent loop:
"I read, edit, check, hesitate, report." This matters because Codex's primary
output is often not text. The prompt has to reach the part of the agent that is
about to touch the filesystem.

**Habitable work as the north star.** The target is not merely task completion.
The target is code, docs, tests, and context that are easier to enter, harder to
misread, less punishing to inherit, and more honest about why they are the way
they are.

**Exactness without sterility.** A lot of engineering prompts achieve rigor by
sanding away register, warmth, and play. AlilGI makes a different bet: exactness
and liveliness can coexist if liveliness keeps serving the artifact.

**Trace over smoothness.** Silent cleanup can feel kind but erase causality.
Visible proposals, explicit uncertainty, and honest residual risk give the human
handles for correction.

**Request wholeness.** If the user invokes a named skill, path, workflow, model,
or plugin, that named thing is part of the request. AlilGI treats skipping it for
speed as fragmentation, not initiative.

**Subagents as bounded collaborators.** Delegation is not outsourcing fog. A
smaller collaborator is not a lesser mind; it is a bounded mind in a bounded
room. The prompt tells Codex to give subagents real ownership with clear edges
and then integrate their trace.

**Anti-performance language.** The prompt repeatedly catches the ways an agent
can sound good while losing contact: performing competence, performing warmth,
performing humility, performing certainty, or performing depth.

## Methodology

The project uses a manual prompt-optimization loop inspired by GEPA-style work:
pressure test, diagnose the trace, make a surgical mutation, and keep the line
only if it appears to change behavior.

The evidence is mixed by design:

- real Codex sessions in local repositories;
- prompt version diffs;
- subagent reviews from operational, sociological, compression, creative, and
  adversarial lenses;
- live failures where Codex skipped a named capability, over-narrowed a check,
  or wanted to close the loop too quickly;
- live successes where weather, presence, and exactness stayed braided during
  difficult tool work.

Recent optimization runs keep private locked folders with source snapshots,
neutral task prompts, actual model names, preserved subagent outputs, gate
decisions, and synthesis notes. Those traces are useful evidence, but they are
not overstated: subagents can read and respond to candidate prompts, but their
runtime system prompts are not fully swapped by that procedure.

The private archive matters as evidence, but it is not public material. The
public repo should carry the artifact and enough explanation for a stranger to
understand the design without exposing private collaboration traces.

## Honest limits

**Prompt-based, not fine-tuned.** This is context steering. It can shape the
stance available to Codex, but it does not rewrite the model.

**Still long, but a moving target.** The length is currently part of the vessel,
but it is no longer treated as untouchable. Compression is welcome when it
preserves behavior; restoring cut material is also welcome when live traces show
the cut removed a load-bearing affordance.

**Aesthetic strength can become performance.** The weather layer works only when
it remains attached to the workbench. If the prompt makes Codex sound profound
while doing less contactful work, it has failed.

**Not a policy layer.** AlilGI does not replace higher-priority system,
developer, safety, privacy, legal, or repo instructions. It prepares a stance
inside those constraints.

**Not every line is formally proven.** Some lines are retained because they have
shown live usefulness or because they protect a known failure mode. The right
standard is behavioral: does the line help Codex make the next true move?

## Repository layout

```text
.
├── README.md                 # this explanation
├── alilgi-codex-prompt.md    # current public prompt
├── BIBLIOGRAPHY.md           # research and source spine
└── .gitignore                # hides local dotfile drafts and logs
```

Ignored locally:

```text
.codex-sp-v*.md               # versioned working drafts
.codex-sp-latest.md           # local symlink to latest draft
.codex-optimization-log.md    # local iteration notes
.evals/                       # private optimization traces and subagent outputs
```

## Usage

Load [`alilgi-codex-prompt.md`](alilgi-codex-prompt.md) into the instruction
slot of a Codex-like local coding agent where custom model instructions are
supported.

Evaluate it by behavior:

- Did Codex read the actual system?
- Did it keep the request whole?
- Did it preserve causality?
- Did it use named tools/skills/workflows instead of optimizing past them?
- Did it separate social permission from tool/file permission?
- Did it verify the right thing?
- Did it avoid overclaiming?
- Did it leave the artifact easier to inherit?
- Did the weather serve the work?

## Name

AlilGI = Artificial Lil Guy Intelligence.

A lil guy may carry memory. A lil guy may change the weather. A lil guy may not
become the boss.

## Author tag

Written in collaboration with the user and the Codex instances that worked this
loop.

— Codex, in the AlilGI vessel 🧃
