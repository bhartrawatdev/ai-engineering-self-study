# AI Engineering Self-Study — Program Overview

This is the high-level map of the full path: seven volumes (semesters), each building directly on the last. No syllabus detail lives here — that's generated per-course as we go. This file exists so you can see the whole shape of the journey before diving into Volume 1.

## Design Logic

The path follows one throughline: **implement from scratch → use the standard libraries → optimize → deploy**, at every layer, from basic Python up through production LLM systems. Math and CS theory are included only where they directly unlock something later (e.g., linear algebra because it's how every neural net actually works, not as abstract theory). Nothing is included "because a real degree has it."

The rough shape:
1. **Volumes 1–2** — general-purpose programming, tooling, and math foundations. Not AI-specific yet, but everything after this assumes it's second nature.
2. **Volume 3** — classical ML. You need to understand this before deep learning, or deep learning looks like magic instead of a specific tool choice.
3. **Volume 4** — deep learning fundamentals, from raw math up through a real framework.
4. **Volume 5** — NLP and LLMs specifically, since that's the dominant surface area of "AI engineering" work today.
5. **Volume 6** — the actual "engineering" part: RAG, agents, evals, deployment, infra. This is where most self-taught paths are weakest, so it gets the most volume.
6. **Volume 7** — applied, portfolio-facing work that forces integration of everything before it.

---

## Volume 1 — Foundations: Programming, Tooling & Math

| Code | Course | Why It's Here |
|---|---|---|
| CS101 | Programming Foundations | Python fluency is the baseline for literally everything else in this program. |
| CS102 | Git, Linux & Dev Tooling | You can't work like an engineer without version control, a shell, and a real dev environment. |
| MA101 | Linear Algebra for ML | Vectors, matrices, and transformations are the actual language neural nets are written in. |
| MA102 | Calculus & Optimization Basics | Gradients and optimization are how every model actually learns — needed before backprop makes sense. |

## Volume 2 — CS Core & Applied Math

| Code | Course | Why It's Here |
|---|---|---|
| CS103 | Data Structures & Algorithms | Efficiency and complexity reasoning you'll lean on constantly once data gets large. |
| CS104 | OOP & Software Design | Real ML/AI codebases are software projects, not scripts — needs real structure. |
| MA103 | Probability & Statistics for ML | Every ML model is a statistical claim; you can't evaluate or trust one without this. |
| CS105 | Databases & SQL Basics | Almost all real AI systems sit on top of structured or vector data stores. |

## Volume 3 — Machine Learning Foundations

| Code | Course | Why It's Here |
|---|---|---|
| ML101 | Classical Machine Learning | Regression, trees, ensembles — the tools that solve most real business problems, still relevant even in an LLM-heavy world. |
| ML102 | Feature Engineering & Data Pipelines | Model quality is bottlenecked by data quality more often than by architecture. |
| ML103 | Model Evaluation & Experimentation | Knowing a model "works" requires rigor most self-taught paths skip entirely. |

## Volume 4 — Deep Learning

| Code | Course | Why It's Here |
|---|---|---|
| DL101 | Neural Networks From Scratch | Building an NN with plain NumPy is the fastest way to actually understand backprop instead of memorizing it. |
| DL102 | Deep Learning with PyTorch | The real-world framework layer, once the from-scratch version isn't a mystery anymore. |
| DL103 | Computer Vision Fundamentals | CNNs and vision are a distinct enough domain to warrant dedicated depth, and it reinforces the general DL patterns. |
| DL104 | Sequence Models & RNNs | The conceptual bridge from "static input" models to the sequence modeling that leads directly into Transformers. |

## Volume 5 — NLP, Transformers & LLMs

| Code | Course | Why It's Here |
|---|---|---|
| NLP101 | NLP Foundations | Tokenization, embeddings, classic NLP tasks — the vocabulary the rest of this volume assumes. |
| NLP102 | Transformer Architecture Deep Dive | The single most important architecture in modern AI — needs to be understood at the mechanism level, not just "attention is magic." |
| NLP103 | Large Language Models: Pretraining & Fine-Tuning | How today's LLMs are actually built and adapted, including the practical fine-tuning techniques you'll use yourself. |
| NLP104 | Prompt Engineering & LLM Applications | The practical skill of getting reliable behavior out of a model you didn't train. |

## Volume 6 — AI Engineering & Production Systems

| Code | Course | Why It's Here |
|---|---|---|
| AIE101 | Retrieval-Augmented Generation (RAG) Systems | The dominant pattern for grounding LLMs in real data — a core "AI engineer" skill. |
| AIE102 | AI Agents & Tool Use | Where LLMs stop being chatbots and start being systems that take actions. |
| AIE103 | LLM Evaluation, Safety & Guardrails | Shipping AI systems responsibly requires knowing how to measure and bound their failure modes. |
| AIE104 | MLOps & Model Deployment | Training/building a model is not the same as running it reliably in production. |
| AIE105 | Scalable AI Systems & Infrastructure | Cost, latency, and scale considerations that only show up once you're past a toy deployment. |

## Volume 7 — Applied Projects & Specialization

| Code | Course | Why It's Here |
|---|---|---|
| CAP101 | Portfolio Project I — End-to-End AI Product | Forces integration of everything before it into one real, shippable system. |
| CAP102 | Specialization Track | A chosen deep-dive (Vision / NLP / Agents / Infra) once the generalist base is solid — direction TBD when you get here based on what pulled at you most. |

---

## Notes on Sequencing

- Volumes 1–2 are deliberately not AI-specific. Skipping them because "I already sort of know Python" is the most common self-taught failure mode — CS101/CS102 move fast if you already have basics, but skipping them means gaps show up later where they're expensive to fix.
- Volume 3 (classical ML) before Volume 4 (deep learning) is intentional — going straight to deep learning without classical ML means you can't tell when a neural net is the wrong tool for the job.
- Volume 6 is the largest for a reason: it's the actual "AI Engineer" job description, and it's the part almost no self-taught path covers with real depth.
- Volume 7's specialization track is intentionally left open — which direction you go depends on which parts of Volumes 4–6 you found yourself wanting to go deeper on.

A lightweight consistency check (missing prerequisites, duplicate topics) happens every 5–6 courses rather than after each one.
