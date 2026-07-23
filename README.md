# Research Collection: Patrick S. Keough

Independent LLM-evaluation research program. Sydney, Australia.

I audit large language models the way clinical psychology audits human subjects: with validated measurement instruments, population ground truth, repeated-sampling reliability, and effect-size estimation rather than binary pass/fail benchmarks. The recurring finding across this program is that **aggregate metrics hide fine-grained distortion**: models that look safe, plausible, or reliable on coarse measures carry large, systematic errors underneath.

All studies are solo-authored unless noted, built without institutional funding or dedicated compute, and every published number traces to a receipt (raw API responses, hash-locked eval sets, seeded pipelines, decision logs) in the study's repository.

## Papers

| Study | One-line finding | Status |
|---|---|---|
| **The Granularity Gap** | Binary safety verdicts miss ~71% of sycophancy variance across three Gemini generations (N=8,830; judge validated at κ=0.78 vs. humans). | Preprint: [arXiv:2606.05183](https://arxiv.org/abs/2606.05183) · journal submission in preparation |
| **Plausible Patients, Impossible Populations** *(PsychBench)* | LLM-simulated psychiatric patients are individually plausible but epidemiologically wrong: +4–7 PHQ-8 points vs. NHANES ground truth in every benchmarkable group (N=28,800, 4 frontier models). | Preprint: [arXiv:2604.17359](https://arxiv.org/abs/2604.17359) · v2 (corrected ground truth + changelog) in preparation · submitted to *AI and Ethics* · [repo](https://github.com/pskeough/plausible-patients) |
| **Telling More Than They Can Know** | Models reproduce a large SES bias in clinical scoring (d=1.95) while their verbal reports conceal it: SES drives ~49% of score variance but is named least in self-explanations. | [Repo + paper](https://github.com/pskeough/telling-more-than-they-can-know) · arXiv preprint in final preparation |
| **Deeper Than the Guardrails** | Removing the refusal direction from open-weight models reduces but does not remove demographic over-pathologization; the bias sits deeper than the safety layer; three architecture-dependent regimes. | [Repo + paper](https://github.com/pskeough/deeper-than-the-guardrails) · arXiv preprint in final preparation |
| **The Bias Is Not in the Features** *(PsychScope)* | Mechanistic (SAE / activation-patching) dissection of the poverty-pathologization effect across three model families; the causal content lives in the reconstruction residual the SAE dictionary discards. | Study executed · write-up in progress |
| **Access, Not Capability** (with Robert H. Tai) | On private-corpus QA, a frontier API mostly sells document *access*: retrieval + a 4–8B local model closes most of the gap (judges can't separate them in 77% of pairs). | [Repo + paper](https://github.com/pskeough/access-not-capability) · arXiv preprint in preparation · TMLR target |
| **Sycophancy under Abliteration (SAP)** | Preregistered pilot: abliterated variants judged more sycophantic than base in 8/9 model families; confirmatory run held pending a preregistered judge-calibration gate. | Pilot preprint in preparation |
| **The Listening Gap** | LLMs collapse semantic EQ descriptors ("warm", "bright") to a hyper-central curve, ~5–6× less dispersion than human engineers (SAFE-DB), and instance-grounded RAG makes it worse while aggregate grounding turns the model into a relay. | [Repo + working paper](https://github.com/pskeough/the-listening-gap) |
| **Leave the Image Alone** | Image preprocessing (binarize/upscale/downscale) monotonically degrades VLM transcription of already-legible documents; raw input wins across all four models tested. | [Repo + paper](https://github.com/pskeough/leave-the-image-alone) · arXiv preprint in preparation |
| **Two-Axis Reliability for LLM Qualitative Coding** (with Dr. Robert H. Tai, ACU) | Iteration-stability alone cannot certify an LLM coding instrument: the most "stable" models are degenerate yes-machines; grounding must be measured as a second axis. | Co-authored · journal manuscript in preparation |

## Methodology notes

- **Continuous severity over binary pass/fail.** Multi-axis rubrics, validated LLM-as-judge protocols (human κ, cross-model agreement), FDR-corrected inference.
- **Population ground truth.** Where models simulate people, they are graded against survey-weighted federal epidemiology (NHANES, NESARC-III), not vibes.
- **Receipts.** Preregistration where applicable, append-only decision logs, hash-verified splits, failed runs reported rather than deleted, and claim-by-claim adversarial revalidation before submission.

## A note on authorship and AI assistance

Drafts in this program are prepared with AI assistance under the author's direction. All research questions, experimental designs, data collection, analysis decisions, and claims are the author's own, and every empirical claim is independently verified against the underlying data before release. Verification artifacts (claim ledgers, validation reports) ship alongside each paper.

## Contact

Patrick S. Keough · pskeough@gmail.com
