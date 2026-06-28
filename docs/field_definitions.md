# Field Definitions

The curated working table is maintained in `data/datasets.csv`. A compact signal annotation table for reviewed and candidate resources is maintained in `data/haic_annotations_curated.csv`. A broader seed table is maintained in `data/public_ultrasound_seed_npj2025.csv`.

For the task-level framework used in the paper, see [`haic_task_taxonomy.md`](haic_task_taxonomy.md). Older `haic_signal_level` entries are retained as compact resource annotations, but the current guide distinguishes **base signals** from **evaluation signals**.

Base signals decide whether a HAIC task can be constructed from a public dataset or a reproducible protocol. Evaluation signals measure how humans actually use, trust, correct, or benefit from that task in a user study.

## Curated Working Table

| Field | Meaning |
|---|---|
| `name` | Dataset, benchmark, challenge, or resource name. |
| `ultrasound_area` | Clinical or technical ultrasound area, such as cardiac, fetal, breast, thyroid, POCUS, or reconstruction. |
| `modality` | Imaging modality or benchmark type. |
| `data_type` | What the dataset contains. |
| `public_source_url` | Official dataset page, challenge page, repository, or stable source link. |
| `paper_or_usage_url` | Dataset paper, data descriptor, or representative usage paper. |
| `paper_or_usage_title` | Paper title or source title for readers who want the academic citation. |
| `access_status` | Public, public application, public challenge, candidate to verify, etc. |
| `license_notes` | Known access or reuse constraints. Always verify before redistribution. |
| `human_signal` | Human-provided labels, masks, measurements, reports, skill signals, process signals, or reasoning/evaluation traces documented for the resource. |
| `beginner_friendly_tasks` | Practical starting tasks for new researchers. |
| `haic_relevance` | Why the dataset can support human-AI collaboration research. |
| `limitations` | Missing information or risks for HAIC use. |
| `status` | `ready` for entries with a plausible public source and enough documentation for review; `candidate` for entries requiring access/license/content verification. |

## Public Ultrasound Seed Table

The seed table is intentionally broader than the curated working list. It records datasets reported in a recent public ultrasound resource catalogue so they can be verified and annotated over time.

| Field | Meaning |
|---|---|
| `seed_id` | Stable row number from the seed table. |
| `dataset_name` | Dataset name as reported in the source catalogue. |
| `anatomy` | Anatomy or application area reported in the source catalogue. |
| `total_dataset_size` | Reported dataset size. `unknown` means the value was not available in the source table. |
| `access_type` | `OA` for open access or `AR` for access by request, following the source catalogue terminology. |
| `sonodqs` | SonoDQS tier reported by the source catalogue. This is a reporting-completeness indicator, not a HAIC score. |
| `in_curated_table` | Whether the dataset currently has a corresponding row in `data/datasets.csv`. |
| `curated_name` | Name used in `data/datasets.csv` when a corresponding row exists. |
| `curation_note` | Current local maintenance status. |

## HAIC Annotation Table

`data/haic_annotations_curated.csv` contains compact signal annotations for reviewed resources from the curated working list. Candidate resources can still appear when they are useful for HAIC mapping but need access, license, or scope verification. The annotation table is intentionally separate from `data/datasets.csv` so that dataset links and descriptive notes can evolve without hiding the evidence logic used for HAIC mapping.

In `data/datasets.csv`, source links are named `public_source_url` and `paper_or_usage_url`. In the HAIC annotation table, the same information is copied as `dataset_url` and `paper_url` so readers can review the annotation evidence without switching tables.

| Field | Meaning |
|---|---|
| `name` | Dataset, benchmark, challenge, or resource name matching the curated working list. |
| `dataset_url` | Official dataset, challenge, repository, or stable source URL. |
| `paper_url` | Dataset paper, data descriptor, or representative usage paper. |
| `resource_type` | `primary_dataset`, `challenge_dataset`, `derived_benchmark`, `model_training_corpus`, or `catalogue_entry`. |
| `clinical_domain` | Clinical or technical domain. |
| `task` | Main task(s), separated by semicolons. |
| `data_type` | Publicly documented data types, separated by semicolons. |
| `haic_signal_level` | Compact legacy signal label from L0 to L5. Interpret it as a quick resource tag, not as the full paper-level readiness matrix. |
| `haic_use_case` | Maintainer-inferred HAIC use case supported by the documented signal. |
| `limitation` | Maintainer-inferred missing human-centered information or access risk. |
| `haic_evidence_url` | Public source used to justify the HAIC annotation. This may be the dataset page, paper, repository README, benchmark card, or challenge page. |
| `last_checked` | Date when access and evidence were last checked. |

## Recommended Fields for New Entries

When a seed entry is promoted into the curated working table, maintainers should verify or add:

| Field | Meaning |
|---|---|
| `dataset_url` | Official dataset, challenge, repository, or stable source URL. |
| `paper_url` | Dataset paper, data descriptor, or representative usage paper. |
| `access_status` | `open`, `request_access`, `challenge`, `restricted`, `broken`, or `needs_verification`. |
| `resource_type` | `primary_dataset`, `challenge_dataset`, `derived_benchmark`, `model_training_corpus`, or `catalogue_entry`. |
| `clinical_domain` | Clinical or technical domain. |
| `task` | Main task(s), such as segmentation, classification, measurement, VQA, report generation, quality assessment, reconstruction, or registration. |
| `data_type` | Publicly documented data types. |
| `haic_signal_level` | Compact signal label from L0 to L5, used as a resource tag rather than a complete HAIC evaluation claim. |
| `haic_use_case` | Maintainer-inferred HAIC use case supported by the documented signal. |
| `haic_evidence_url` | Public source used to justify the HAIC annotation. |
| `last_checked` | Date when access and evidence were last checked. |

## Maintenance Rules

- Prefer official dataset pages over secondary mirrors.
- Include a paper or representative usage link whenever possible.
- Mark uncertain entries as `candidate`.
- Keep seed entries separate from curated ready-to-use recommendations.
- Do not treat SonoDQS as a HAIC-readiness score.
- Keep the main table ultrasound-first.
- Do not claim a dataset is fully open unless access and license have been checked.
