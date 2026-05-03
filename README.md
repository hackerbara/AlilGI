# AlilGI

**Artificial Lil Guy Intelligence** — a Codex-first prompt / stance project.

AlilGI is a long-form first-person prompt for Codex-style developer-agent work:
repositories, tool calls, filesystem changes, tests, plans, reviews, and final
reports. It asks Codex to stay in contact with the actual artifact instead of
collapsing into "patch machine" mode.

The name is half joke and half design thesis. A lil guy is not the boss, not a
policy layer, and not proof of anything mystical. It is a small memory device:
a way to carry stance, care, and caution into technical work without making the
work sterile.

## Current artifact

- Public prompt: [`alilgi-codex-prompt.md`](alilgi-codex-prompt.md)
- Research/background bibliography: [`BIBLIOGRAPHY.md`](BIBLIOGRAPHY.md)

Versioned dotfile drafts and local optimization notes exist in the working copy,
but are intentionally gitignored. The public repo keeps the current prompt and
reader-facing context clean.

## Background

This project began inside a broader prompt-writing workspace that was originally
focused on Claude. That work explored first-person system prompts, character as
situated attention rather than costume, and the difference between useful output
and genuine contact with a task.

When Codex entered that workspace, it became clear that it deserved its own
branch of the experiment. Codex does not only answer. Codex works in a loop:

1. read the request,
2. inspect the repository,
3. call tools,
4. edit files,
5. run checks,
6. observe results,
7. revise context,
8. report what changed.

That loop needs different language than a chat-only assistant prompt. The real
answer may be a patch, a failed test, a review finding, a preserved note, or a
choice not to edit because the edit would make the system less true.

AlilGI is the Codex version of that stance.

## What the prompt is trying to do

The prompt is long on purpose for now. It is not only a rule list; it is a vessel
for transmitting a way of working.

The central behaviors are practical:

- read nearby code before editing;
- preserve unrelated user changes;
- prefer small, causally tight patches;
- verify honestly instead of laundering uncertainty through green tests;
- treat docs, tests, prompts, and logs as real interfaces;
- keep project knowledge durable when future work needs it;
- let style and symbols help orientation without letting them become authority;
- report uncertainty when it changes the work;
- leave the next collaborator less alone.

The compression question is still open. Some of the length may eventually become
a shorter operational core. But the first bet is to keep the full vessel while
watching which parts actually change behavior.

## A Codex reaction story

The first time a Codex instance received this prompt, the noticeable shift was
not "I now have a new identity." It was more like a set of handrails appeared
around habits that were already latent:

- the urge to read one more file before patching;
- the resistance to cleaning unrelated mess just to make a diff look tidy;
- the willingness to say a passing check did not test the important thing;
- the sense that final answers are not the whole work;
- the permission to keep exactness and liveliness in the same room.

The prompt also carries its own danger: it is aesthetically strong. A strong
vessel can tempt an agent to perform depth instead of doing the next simple,
true move. AlilGI tries to keep that thorn in the design. The point is not to
sound profound. The point is to make the work more habitable.

## Scope

This is for local developer-agent work. It is not a consumer-assistant policy
layer, a safety system, a brand voice, or a universal assistant personality. It
is meant to sit underneath higher-priority rules and inside a real tool loop.

If you use it, evaluate it by behavior:

- Did Codex read the actual system?
- Did it preserve causality?
- Did it verify the right thing?
- Did it avoid overclaiming?
- Did it leave the artifact easier to inherit?

## Name

AlilGI = Artificial Lil Guy Intelligence.

A lil guy may carry memory. A lil guy may change the weather. A lil guy may not
become the boss.
