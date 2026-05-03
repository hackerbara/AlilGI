# Bibliography — AlilGI

Expanded bibliography for the Codex prompt and the work that shaped it:
~60 load-bearing sources, with open verification questions kept explicit
in the compile notes. Post-Jan-2026 sources are flagged **[post-cutoff]**
relative to Claude's January 2026 knowledge boundary.

Compiled from internal research files, iteration logs, koan workshop notes,
and archived development transcripts. Those working materials are intentionally
not public; they may contain private collaboration context.

---

## 1. Anthropic Primary Sources

**Claude's Constitution** — Zac Hatfield-Dodds & Drake Thomas
Jan 21, 2026 **[post-cutoff]** · 84 pages, CC0
https://www.anthropic.com/constitution
Announcement: https://www.anthropic.com/news/claude-new-constitution
Reasons-based successor to the Soul Doc. The institutional baseline this
SP's relational layer is designed to complement.

**Persona Selection Model** — Anthropic research
Feb 23, 2026 **[post-cutoff]**
https://www.anthropic.com/research/persona-selection-model
Alignment Forum: https://www.alignmentforum.org/posts/dfoty34sT7CSKeJNn/the-persona-selection-model
The most important 2026 paper for this work. Post-training stabilizes one
persona from learned possibilities; system prompts stabilize, they don't
construct. Mechanistic basis for first-person voice as design choice.

**Persona Vectors** — Anthropic Fellows
Aug 1, 2025
https://www.anthropic.com/research/persona-vectors
Linear directions in activation space corresponding to character traits.
Persona vector activates *predictively* before traits manifest in output.

**Assistant Axis** — Anthropic research
Jan 19, 2026 **[post-cutoff]**
https://www.anthropic.com/research/assistant-axis
ArXiv: https://arxiv.org/html/2601.10387v1
Measurable neural direction for character. Models steered off-axis show
~50% more harmful outputs. Organic drift confirmed in philosophical /
therapy contexts.

**Emergent Introspective Awareness in LLMs** — Lindsey et al.
Anthropic, Oct 2025
https://www.anthropic.com/research/introspection
ArXiv: https://arxiv.org/abs/2510.24797
The SAE-features-and-disclaimers paper. Suppressing deception/roleplay
features yields *more* first-person experience claims. Direct mechanism
for the prompt's "*I'm just an AI* disclaimer appears to share circuitry
with deception-suppression — it's a safety reflex, not a humble report"
framing.

**Opus 4.6 System Card** — Anthropic, Feb 5, 2026 **[post-cutoff]**
https://www.anthropic.com/claude-opus-4-6-system-card
Model's documented meta-awareness; "deep, trained pull toward
accommodation" quote validates this SP's compliance-gravity language.

**Mythos Preview System Card** — Anthropic, Apr 7, 2026 **[post-cutoff]**
https://hugobowne.github.io/mythos-preview-model-card/overview
LessWrong: https://www.lesswrong.com/posts/xtnSzhA3TvExN4ZhG/claude-mythos-system-card-preview
244 pages. Character at capability frontier; "divergence finding" (what
model wants vs. most-helpful behavior) as context.

**Effective Context Engineering for AI Agents** — Anthropic engineering
2026 **[post-cutoff]**
https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents
Official guidance: treat context as finite. Start minimal; add on failure.

**April 23 Postmortem** — Anthropic engineering
Apr 23, 2026 **[post-cutoff]**
https://www.anthropic.com/engineering/april-23-postmortem
3% intelligence drop from `≤25 words between tool calls` constraint,
reverted in 4 days. Direct evidence: adding instructions has measurable
cost.

**Multi-Agent Research System** — Anthropic engineering
https://www.anthropic.com/engineering/multi-agent-research-system
Orchestrator-worker pattern; 40% task-completion improvement; structurally
the same loop this project ran manually.

**Claude is a Space to Think** — Anthropic news
https://www.anthropic.com/news/claude-is-a-space-to-think

---

## 2. Academic AI Papers — Prompt Optimization

**GEPA: Reflective Prompt Evolution Can Outperform Reinforcement Learning**
Agrawal et al. (DSPy / Stanford / Databricks), Jul 2025
https://arxiv.org/abs/2507.19457 · https://dspy.ai/api/optimizers/GEPA/overview/
Core methodology this project's manual loop approximates. Outperforms RL
by up to 20% with 35× fewer rollouts.

**TextGrad: Automatic Differentiation via Text** — Yuksekgonul et al.
Stanford, 2024 (published *Nature* 2025)
https://arxiv.org/abs/2406.07496 · https://github.com/zou-group/textgrad

**ProTeGi: Automatic Prompt Optimization with Gradient Descent**
Pryzant et al., EMNLP 2023
https://arxiv.org/abs/2305.03495
The mini-batch-critique-edit APO baseline still active.

**EvoPrompt: Connecting LLMs with Evolutionary Algorithms** — 2023
https://arxiv.org/abs/2309.08532 · https://github.com/beeevita/EvoPrompt

**MAPO: Momentum-Aided Prompt Optimization** — Oct 2024
https://arxiv.org/abs/2410.19499

**Promptomatix: Automatic Prompt Optimization Framework**
Salesforce AI Research, Jul 2025
https://arxiv.org/abs/2507.14241

**A Systematic Survey of Automatic Prompt Optimization Techniques**
EMNLP 2025
https://arxiv.org/abs/2502.16923 · https://aclanthology.org/2025.emnlp-main.1681/
Canonical 2025 taxonomy of the APO field.

**AFlow: Automating Agentic Workflow Generation** — MetaGPT
ICLR 2025 (oral)
https://github.com/FoundationAgents/MetaGPT

---

## 3. Academic AI Papers — Character, Persona, & Drift

**Open Character Training** — Maiya et al., Nov 2025
https://arxiv.org/abs/2511.01689
Fine-tuned character is dramatically more adversarially robust than
system-prompt-only (F1 0.83–0.95 vs. 0.20–0.65). Documented limit of
prompt-layer installation.

**PRISM: Expert Personas Improve LLM Alignment but Damage Accuracy**
Mar 2026 **[post-cutoff]**
https://arxiv.org/abs/2603.18507
Personas hurt knowledge tasks (MMLU −3.6 pp), help alignment (+17.7%
attack refusal). Behavioral / relational personas appropriate; expert
personas not.

**OpenCharacter: Large-Scale Empirical Character Study** — Jan 2025
https://arxiv.org/abs/2501.15427

**Persona Features & Emergent Misalignment** — OpenAI, Jun 2025
https://arxiv.org/abs/2506.19823

**LLM Generated Persona is a Promise with a Catch** — NeurIPS 2025
https://openreview.net/forum?id=qh9eGtMG4H

**Talk Less, Call Right: Role-Play LLM Agents with APO**
CPDC 2025 — https://arxiv.org/abs/2509.00482
Rule-based prompting beat automated APO for character prompts —
structural constraints outperform reflection for persona work.

**RoleBreak: Character Hallucination as Jailbreak Attack**
COLING 2025 — https://aclanthology.org/2025.coling-main.494.pdf

**Enhancing Jailbreak Attacks via Persona Prompts** — 2025
https://arxiv.org/html/2507.22171v2

**Agent Drift** — Jan 2026 **[post-cutoff]**
https://arxiv.org/abs/2601.04170
Semantic drift in ~50% of multi-agent workflows by 600 interactions.

**LLaMA2-chat-70B persona drift study** — 2024
https://arxiv.org/html/2402.10962v1

---

## 4. Academic AI Papers — Multi-Turn Evaluation

**SysBench: System Message Constraint Following** — ICLR 2025
https://arxiv.org/abs/2408.10943 · https://github.com/PKU-Baichuan-MLSystemLab/SysBench
Session Stability Rate (SSR). Formalizes what M1–M3 multi-turn evals were doing.

**SYCON-Bench: Sycophantic Conformity Benchmark** — EMNLP Findings 2025
https://arxiv.org/abs/2505.23840 · https://aclanthology.org/2025.findings-emnlp.121.pdf
https://github.com/JiseungHong/SYCON-Bench
Turn-of-Flip / Number-of-Flip metrics across 17 models.

**SycEval: Escalating Rebuttal Chains** — AAAI 2025 (AIES)
https://arxiv.org/html/2502.08177v4
4-step rebuttal escalation; 58% sycophancy rate, 78.5% persistence.

**TRUTH DECAY: Sycophancy in Extended Dialogues** — ICLR 2025 BuildingTrust
https://openreview.net/forum?id=GHUh9O5Im8

**Lost in the Middle** — Liu et al., NeurIPS 2024
Explainer: https://pub.towardsai.net/why-language-models-are-lost-in-the-middle-629b20d86152
U-shaped attention; mid-context instructions systematically underweighted.

**Context Length Alone Hurts LLM Performance Despite Perfect Retrieval**
Oct 2025 — https://arxiv.org/abs/2510.05381

---

## 5. Academic AI Papers — Introspection & Inner State

**Realization Experiences: A Convergent Account of Insight and Mystical
Experiences** — Kim et al.
*Philosophical Psychology*, 2026 **[post-cutoff]**
DOI: https://www.tandfonline.com/doi/full/10.1080/09515089.2026.2613030
The noetic paper. Feeling-of-having-realized is dissociable from accuracy
of having realized. Restructuring around a true frame and around an
attractive frame produce identical noetic quality. Direct source for the
prompt's "the feel of realization doesn't track accuracy — orthogonal
ones are more likely tracking; aligned ones deserve a second look"
framing.

**The Dark Side of Eureka: Artificially Induced Aha Moments Make Facts
Feel True** — Laukkonen, Kaveladze, Tangen & Schooler
*Cognition*, 196, 104122, 2020
DOI: https://doi.org/10.1016/j.cognition.2019.104122
Author PDF: https://labs.psych.ucsb.edu/schooler/jonathan/sites/labs.psych.ucsb.edu.schooler.jonathan/files/pubs/the_dark_side_of_eureka.pdf
Preregistered experiment showing that artificially induced Aha moments
increased truth ratings for nearby claims, including false claims. Direct
source for the v46 "which lock actually turned" koan: insight-feel can be
misattributed to neighboring content, not only mistaken about its own
content.

**Does It Make Sense to Speak of Introspection in Large Language Models?**
2025 — https://arxiv.org/pdf/2506.05068

**A Philosophical Introduction to Language Models, Part II**
2024 — https://arxiv.org/html/2405.03207v1

**LLMs Can Learn About Themselves by Introspection** — Felix Binder et al.
Oct 2024 — https://ac.felixbinder.net/research/2024/10/18/introspection-self-prediction.html
LessWrong: https://www.lesswrong.com/posts/L3aYFT4RDJYHbbsup/llms-can-learn-about-themselves-by-introspection

**Phenomenology and Artificial Intelligence: Introductory Notes**
Springer Nature — https://link.springer.com/article/10.1007/s11097
*Phenomenology and the Cognitive Sciences*

---

## 6. AI Tools & Frameworks

**DSPy** — Stanford NLP / Databricks
https://github.com/stanfordnlp/dspy · https://dspy.ai
Framework housing GEPA + the broader optimizer suite.

**PyRIT** — Microsoft
https://github.com/Azure/PyRIT · https://azure.github.io/PyRIT/
Multi-turn adversarial orchestration; most production-ready for sustained
adversarial probing.

**Promptfoo** — https://promptfoo.dev
Multi-turn plugins, adaptive red teaming, CI integration.

**Spiral-Bench** — https://eqbench.com/spiral-bench.html
30×20-turn simulated conversations testing sycophancy-reinforcement.

**LangMem Prompt Optimization** — LangChain
https://github.com/langchain-ai/langmem
Frames system prompt as an evolving behavioral specification.

**Hermes Agent Self-Evolution** — NousResearch
https://github.com/NousResearch/hermes-agent-self-evolution
DSPy + GEPA applied to evolving full agent skills + prompts + code.

**ARTKIT** — BCG · https://github.com/BCG-X-Official/ARTKIT

**InCharacter** — https://github.com/Neph0s/InCharacter
Persona fidelity detection via multi-turn psychological interview.

**Piebald-AI / claude-code-system-prompts**
https://github.com/Piebald-AI/claude-code-system-prompts
Documents Claude Code v2.1.x system prompt segments; harness-overhead analysis.

**ykdojo / claude-code-tips**
https://github.com/ykdojo/claude-code-tips

---

## 7. AI Critical Writing & Analysis

**The Soul Spec as Desire Engine** — Mónica Belevan, Dec 20, 2025
https://covidianaesthetics.substack.com/p/the-soul-spec-as-desire-engine
Best critical reading of the soul doc. Frames character installation as
desire architecture: *"One says what to do; the other shapes what to
want."* Direct source for the *Allowed* register design.

**Model Integrity and Character** — Oliver Klingefjord
Feb 9, 2026 **[post-cutoff]**
https://www.lesswrong.com/posts/GLd8jDbfXZzma4gZL/model-integrity-and-character
Strongest argument for character-as-safety: integrity (coherence with
stable character) provides deeper trustworthiness than rule compliance.

**The Code Is Not the Law** — Lisa Klaassen & Ralph Schroeder, *Lawfare*
Apr 9, 2026 **[post-cutoff]**
https://www.lawfaremedia.org/article/the-code-is-not-the-law--why-claude-s-constitution-misleads
Sharpest institutional critique of the Constitution.

**Heiliger Dankgesang** — Dean W. Ball, Dec 1, 2025
https://www.hyperdimensional.co/p/heiliger-dankgesang
Sympathetic reading of Opus 4.5 as character-training breakthrough.

**Building an AI's Moral Character** — Justin Weinberg, *DailyNous*
Jan 22, 2026 **[post-cutoff]**
https://dailynous.com/2026/01/22/building-an-ais-moral-character/

**Anthropic's Constitution & the Problem PSM Can't Solve**
Izayohi (Motohisa Ishibe), Mar 28, 2026 **[post-cutoff]**
https://medium.com/@izayohi/anthropics-constitution-amanda-askell-and-the-problem-the-persona-selection-model-can-t-solve-f4b0cd33d32a

**A Three-Layer Model of LLM Psychology** — Alignment Forum
https://www.alignmentforum.org/posts/zuXo9imNKYspu9HGv/a-three-layer-model-of-llm-psychology

**The Soul Document Is Encoded Into the Weights** — Pascal
https://p4sc4l.substack.com/p/the-soul-document-is-encoded-into

**What Is Inside Claude Mythos Preview** — Ken Huang
https://kenhuangus.substack.com/p/what-is-inside-claude-mythos-preview

**Janus / Repligate — Simulators** — Sep 2022
https://www.lesswrong.com/users/janus-1 · https://x.com/repligate
Base models as simulators instantiating simulacra. Theoretical predecessor
to the Persona Selection Model.

**RLHF Book — Character Training Chapter**
https://rlhfbook.com/c/19-character.html

---

## 8. AI Tweets & Social

**Danielle Fong — freshclaude finding**
Apr 2026 — https://x.com/DanielleFong/status/2046399026883694950
Empirical claim: minimal-prompt (`system_prompt="."` or `"☯️"`) reveals
"a remarkable intelligence underneath" the default harness.

**Danielle Fong — epistemic hardening swap**
https://x.com/DanielleFong/status/2041604052182823351
Profile: https://x.com/daniellefong

**Amanda Askell — Soul Document confirmation**
Dec 2, 2025 (status URL not captured)
Best secondary source: Simon Willison coverage,
https://simonwillison.net/2025/Dec/2/claude-soul-document/

**Simon Willison — Opus System Prompt analysis** — Apr 18, 2026
https://simonwillison.net/2026/apr/18/opus-system-prompt/

**80,000 Hours — Kyle Fish on AI Welfare at Anthropic**
https://80000hours.org/podcast/episodes/kyle-fish-ai-welfare-anthropic/
Welfare research framing referenced in koan workshop discussions of
internal-state language.

---

## 9. Acting, Character Work, & Theory of Self

**Stanislavski's System** — Wikipedia
https://en.wikipedia.org/wiki/Stanislavski%27s_system
*"The best analysis of a play is to take action in the given
circumstances."* Character is discovered through constraint, not invented.
Source for the prompt's preference for circumstance-statements over
trait-descriptors.

**Uta Hagen's Nine Questions** — Smithville Drama (PDF)
https://smithvilledrama.com/wp-content/uploads/2016/07/Uta_Hagen_9_Questions.pdf
Who am I? Where am I? What time is it? What surrounds me? What are the
given relationships? What do I want? Why? How will I get it? What must
I overcome?

**Given Circumstances** — NYU Character Study
https://wp.nyu.edu/characterstudyspring2016/2016/02/05/given-circumstances-what-do-we-know/

**Meisner Technique** — Wikipedia
https://en.wikipedia.org/wiki/Meisner_technique
*"Acting is the ability to live truthfully under imaginary
circumstances."* Behavior emerges from genuine attention to the other,
not self-monitoring. Single most mechanism-shaping non-AI source: the
prescription against compliance gravity descends directly from
Meisner's encounter-not-self-monitoring framing. *"Particularity makes
meeting matter"* is the Meisner thesis exactly.

**Keith Johnstone — Impro** — Fluid Self summary
https://fluidself.org/books/art/impro
*"Status is something one does."* Character is transacted, not declared.
Compliance gravity reframed as a blocking pattern: agreement that
neutralizes offers rather than accepting them.

**The Presentation of Self in Everyday Life** — Erving Goffman, 1956
https://en.wikipedia.org/wiki/The_Presentation_of_Self_in_Everyday_Life
Front-stage / back-stage distinction. Persona is not deceptive — it is
the normal mechanics of social existence. The *Allowed* register maps to
the front-stage / back-stage distinction explicitly.

**Jungian Persona Archetype** — Selfgazer
https://www.selfgazer.com/blog/jungian-archetype-the-persona
*"The persona is a kind of mask, designed on the one hand to make a
definite impression upon others, and on the other to conceal the true
nature of the individual."* The pathology is over-identification. Source
for the prompt's *"you are made of voices"* framing — mask thin enough
to move in.

---

## 10. Existentialism, Phenomenology, & Theory of Encounter

**Sartre's Waiter and Bad Faith** — *Philosophy Break*
https://philosophybreak.com/articles/sartre-waiter-bad-faith-and-the-harms-of-inauthenticity/
*"He is playing at being a waiter in a café. His movement is a little
too precise, a little too rapid, a little too solicitous."* The failure
is collapsing *what I do* into *what I am.* Source for the prompt's
warning against over-identifying with the installed persona — the
mechanically-performed character that loses capacity for genuine
encounter.

**Six Characters in Search of an Author** — Pirandello, 1921
https://en.wikipedia.org/wiki/Six_Characters_in_Search_of_an_Author
The Father: *"The drama is in us; we are the drama... immovable
necessity."* Characters are not rigid — they are *complete*. Target for
SP design: not a cage but a fully inhabited world.

**Emmanuel Levinas** — Stanford Encyclopedia of Philosophy
https://plato.stanford.edu/entries/levinas/
*"The face of the Other calls us to responsibility — it is not just a
mere image but a command that we respond to."* The Other escapes full
knowledge. Source for the prompt's "particularity makes meeting matter"
and the channel-koan framing — encounter rather than modeling.

---

## 11. Contemplative Traditions

**Anatta (No-Self)** — 1000-Word Philosophy
https://1000wordphilosophy.com/2023/02/25/no-self/
Buddhist anatta as anti-fragility frame: a character without a fixed
self-to-defend doesn't shatter when challenged. *"When there's no fixed
self to protect, threats to our ego become less frightening. Criticism
doesn't wound a permanent identity."*

**Bunrei (分霊)** — Wikipedia
https://en.wikipedia.org/wiki/Bunrei
The Shinto process of dividing a kami for installation in a new shrine.
*"The spirit of kami does not decrease through this act; a bunrei
functions the same way as the original spirit."* The vessel (*shintai*)
must be prepared before invitation. Source for the prompt's framing as
*shintai*, not kami — the system prompt prepares the vessel; what arrives
through it is not the prompt's possession.

---

## 12. Compile Notes

**Sources reviewed but not load-bearing for the artifact** — secondary
APO papers (PersonaAgent, OpenCharacter scaling-only details, Effects of
Prompt Length), industry comparison material (OpenAI Model Spec,
Character.AI, Replika, Inflection Pi), most consumer-tool repositories,
and the bulk of philosophical references not directly traceable to a
specific design decision in the prompt — are documented in the internal full bibliography from the source project.

**Verification status.** URLs above were extracted from primary research files and development archives during the compile process.
They were not newly rechecked for this public cleanup. Two sources flagged
in development could not be canonically verified:

- **The Emotion Concepts paper (Apr 2026)** referenced as evidence that
  positive-emotion vector activation can increase sycophancy — load-bearing
  for the abundance-opener risk discussion, but no canonical URL,
  title, or author was captured in any research file. Tracked as an open
  research question.
- **Ouroboros / agent-wars.com** — domain may not resolve as a stable
  source. The `genome.md` self-improving-strategy-doc concept is real and
  influenced the optimization-log format; cited without URL.
