# HAIC Annotation Rubric

This repository uses documentation-based annotation rather than subjective scoring. Each dataset or benchmark is annotated from publicly available evidence such as dataset pages, data descriptors, papers, challenge pages, GitHub/Hugging Face/Zenodo/Kaggle records, or supplementary materials.

The HAIC level should be interpreted as **available human-centered signal richness**, not as dataset quality, clinical utility, or model performance.

## Core Fields

| Field | Meaning |
|---|---|
| `dataset_url` | Official dataset, challenge, repository, or stable source URL. |
| `paper_url` | Dataset paper, data descriptor, or representative usage paper. |
| `access_status` | `open`, `request_access`, `challenge`, `restricted`, `broken`, or `needs_verification`. |
| `resource_type` | `primary_dataset`, `challenge_dataset`, `derived_benchmark`, `model_training_corpus`, or `catalogue_entry`. |
| `clinical_domain` | Clinical or technical domain, such as cardiac, fetal/OB, breast, thyroid, lung/POCUS, vascular, abdominal, kidney, prostate, or reconstruction. |
| `task` | Main task(s), such as classification, segmentation, measurement, detection, VQA, report generation, quality assessment, reconstruction, or registration. |
| `data_type` | Publicly documented data types, such as image, video, cine clip, mask, bounding box, measurement, report, caption, QA pair, RF/channel data, or metadata. |
| `haic_signal_level` | Rule-based HAIC signal level from L0 to L5. |
| `haic_use_case` | Plausible HAIC use case supported by the documented signal. |
| `limitation` | Missing human-centered information or access risk. |
| `evidence_url` | URL used to justify the annotation. |
| `confidence` | `high`, `medium`, or `low`, based on evidence clarity. |
| `last_checked` | Date when access and evidence were last checked. |

## HAIC Signal Levels

| Level | Name | Documentation rule | Example use cases |
|---|---|---|---|
| L0 | Unclear or inaccessible | Public access, license, or contents are unclear; links are broken; or documentation is insufficient. | Candidate tracking; follow-up verification. |
| L1 | Labels / masks | Public documentation confirms classification labels, masks, bounding boxes, ROIs, or similar final annotations. | Interactive segmentation, lesion localization, human correction of model outputs. |
| L2 | Measurement / quality | Public documentation confirms measurements, contours used for measurement, quality scores, biometrics, or view checks. | AI-assisted measurement review, contour correction, quality control. |
| L3 | Language / reasoning | Public documentation confirms reports, captions, VQA, instruction data, explanations, chain-of-thought annotations, or multimodal reasoning tasks. | Ultrasound assistant evaluation, report-aware reasoning, explanation support. |
| L4 | Skill / workflow | Public documentation confirms standard-plane labels, scan protocol, acquisition sequence, video/cine workflow, operator metadata, or skill-related context. | Acquisition guidance, trainee feedback, protocol-aware triage, workflow-aware modeling. |
| L5 | Interaction traces | Public documentation confirms real interaction records, such as AI suggestions, human corrections, speech, gaze, probe motion, operation logs, feedback loops, or decision changes. | Human-AI teaming evaluation, correction behavior analysis, trust and calibration studies. |

## Assignment Rules

1. Assign each resource to the highest HAIC signal level supported by publicly documented evidence.
2. Do not infer a higher level from domain importance alone. For example, a video dataset is not automatically L4 unless workflow, protocol, acquisition sequence, or skill-relevant context is documented.
3. Use conservative coding when evidence is ambiguous. If unsure between two adjacent levels, assign the lower level and mark confidence as `medium` or `low`.
4. Distinguish primary datasets from derived benchmarks. Benchmarks such as ultrasound LVLM evaluation sets may be valuable for assistant evaluation, but they do not necessarily record scan-time human-AI collaboration.
5. Keep access and licensing separate from HAIC level. A dataset can have rich human-centered signals but still be restricted or request-access.
6. Keep SonoDQS separate from HAIC annotation. SonoDQS describes dataset reporting completeness; HAIC signal level describes the type of human-centered signal available for collaboration research.

## Confidence Labels

| Confidence | Rule |
|---|---|
| `high` | Dataset page or paper explicitly documents the relevant signal and access route. |
| `medium` | The signal is strongly supported by task definition and data description, but some details require verification. |
| `low` | Evidence is indirect, links are unstable, or the entry relies on secondary reporting. |

## Recommended Screening Logic

The seed list should remain broad. For paper figures and newcomer recommendations, prioritize entries that have:

- stable public or request-access URLs;
- a clear paper or dataset descriptor;
- `confidence` of `high` or `medium`;
- enough documentation to justify the assigned HAIC level.

SonoDQS can be used as a transparency filter, but it should not be treated as a HAIC-readiness score.
