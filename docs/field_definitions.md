# Data Dictionary

This repository exposes two public CSV tables. The goal is to keep the guide readable for HAIC researchers while preserving enough source information to audit each entry.

## `data/living_guide.csv`

Main one-row-per-resource table.

- `resource_name`: dataset, benchmark, challenge, or resource name.
- `task_family`: one or more task-family codes separated by semicolons.
- `anatomy_or_domain`: anatomy, clinical domain, or technical domain.
- `task_or_scenario`: short description of the original task or use scenario.
- `base_signal_type`: what kind of base signal the resource provides or can support, such as labels, masks, measurements, quality cues, language data, or reconstruction targets.
- `source_url`: public source used to justify the row and task-family annotation. This may be a dataset page, paper, benchmark source list, or secondary catalogue.
- `source_type`: type of source used for `source_url`, such as `direct_resource`, `paper_or_evidence`, `benchmark_source_list`, `secondary_catalogue`, or `paper_only_not_public`.
- `dataset_url`: direct dataset, repository, challenge, or project link when confirmed.
- `evidence_url`: paper, DOI, arXiv page, benchmark page, or other evidence link when available.
- `status`: current source status. Rows marked `secondary_catalogue_only`, `benchmark_source_only`, `evidence_source_only`, or `paper_only_not_public` should not be read as confirmed direct dataset-release links.

## `data/task_family_summary.csv`

Compact task-family table used to explain the matrix and paper-level analysis.

- `task_family`: readable task-family name.
- `paper_matrix_count`: approximate multi-label count used in the paper matrix.
- `typical_base_signals`: common base signals for this task family.
- `public_data_reuse`: how public datasets in this family can usually be upgraded toward HAIC tasks.
- `needs_new_data_for`: which higher-level HAIC questions typically require new process, interaction, or longitudinal data.

## Task-Family Codes

- `recognition_classification`: disease, anatomy, view, or video labels.
- `segmentation_localization`: masks, boxes, landmarks, or regions of interest.
- `measurement_quantification`: biometrics, functional indices, volumes, or severity scores.
- `quality_acquisition`: view quality, standard-plane status, protocol state, or probe guidance.
- `report_vqa_reasoning`: reports, captions, question answering, or assistant-style outputs.
- `reconstruction_registration`: beamforming, enhancement, alignment, or spatial transformation.

## Signal Terminology

The guide separates two concepts.

- **Base signals** determine whether a HAIC task can be constructed from a public dataset or a reproducible protocol.
- **Evaluation signals** measure how humans actually use, trust, correct, or benefit from that task in a user study.

The public tables describe base-signal availability and reuse potential. They do not claim that user-study evaluation is unnecessary.
