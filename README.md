# Public Ultrasound Datasets for HAIC Research

This repository is the online living guide accompanying our HAIC-oriented analysis of public ultrasound datasets. It is not a general ultrasound-AI catalogue and it does not rank dataset quality. It asks a narrower question:

> Given a public ultrasound dataset, what human-AI collaboration (HAIC) task can be constructed from its available base signals?

## Public Tables

The public guide is intentionally kept to two CSV tables.

- [`data/living_guide.csv`](data/living_guide.csv): the main one-row-per-resource guide. It lists the resource name, task family, anatomy/domain, task description, base-signal type, source URL, source type, direct dataset link when confirmed, evidence link, and verification status.
- [`data/task_family_summary.csv`](data/task_family_summary.csv): a compact task-family summary. It gives the paper-matrix counts, typical base signals, likely HAIC reuse path, and what new data are needed for higher-level studies.

## Background Sources

The guide builds on public searches, challenge pages, benchmark papers, repositories, and prior ultrasound-resource surveys. A recent *npj Digital Medicine* survey catalogued 72 public ultrasound datasets and 56 open-source ultrasound models. We use that survey as a resource-discovery starting point, then reorganize public datasets by HAIC task family and by the base signals they can support. [Survey link](https://pmc.ncbi.nlm.nih.gov/articles/PMC12722232/)

## Core Concepts

- **Base signals** decide whether a HAIC task can be constructed from a dataset or a reproducible protocol. Examples include labels, masks, measurements, reports, scan states, model predictions, prediction-ground-truth differences, uncertainty scores, deferral rules, intermediate edits, and interaction logs.
- **Evaluation signals** measure how people actually use the task in a user study. Examples include preference, time cost, workload, accept/override behavior, trust calibration, reliance, skill retention, and clinical usefulness.

Public datasets can often provide or derive base signals for lower-level HAIC tasks, but they do not replace user studies for evaluating real workload, trust, handoff behavior, or clinical benefit.

## Readiness Matrix

The matrix maps five HAIC levels to six ultrasound task families. The same task-family counts are listed in [`data/task_family_summary.csv`](data/task_family_summary.csv).

![HAIC task-readiness matrix](figures/haic_task_readiness_matrix.png)

Support codes:

- **Native**: the original dataset already contains the base target needed for this level.
- **Protocol-derived**: proxy base signals can be derived through a reproducible protocol, such as model predictions, prediction-ground-truth differences, confidence scores, or deferral rules.
- **Conditional**: support depends on dataset-specific temporal or process signals, such as scan sequences, probe states, intermediate edits, or interaction traces.
- **New logs required**: core base signals require prospective human-AI interaction logs.

The main boundary is L4. L2 and L3 are mostly outcome-level simulations: model outputs can be compared with existing annotations to estimate correction burden or deferral behavior. L4 is process-level and requires states and actions across turns. L5 remains prospective because repeated-use adaptation cannot be recovered from static images or labels.

## How to Use This Guide

1. Start from [`data/task_family_summary.csv`](data/task_family_summary.csv) to identify the task family and likely HAIC upgrade path.
2. Use [`data/living_guide.csv`](data/living_guide.csv) to find candidate public resources and trace each entry through `source_url`.
3. Decide which base signals are already available, which can be derived by protocol, and which require new data collection.
4. Design the user study separately to collect evaluation signals such as workload, correction time, trust, preference, reliance, and clinical usefulness.

## Notes

- Benchmark collections such as U2-BENCH are useful for HAIC-oriented model evaluation, but they are not treated as single primary datasets inside one task family.
- Every row includes `source_url`, the public source used to justify inclusion and task-family annotation. When a direct dataset page is not confirmed, `source_url` may point to a paper, benchmark source list, or secondary catalogue, with `status` marking the limitation.
- Multi-rater or rater-evaluation resources such as Open Kidney, MCE, and SonoRate are useful for studying expert variability and selective deferral, but they remain scarce in ultrasound.
- K2MUSE is included as an ultrasound-adjacent process-rich resource. It contains time-synchronized A-mode ultrasound and locomotion signals and should not be treated as a diagnostic B-mode ultrasound dataset.

## Contributing

Please open an issue or pull request using [`.github/ISSUE_TEMPLATE/add_dataset.md`](.github/ISSUE_TEMPLATE/add_dataset.md). Useful contributions include stable dataset links, papers, access notes, task-family corrections, base-signal annotations, and limitations relevant to user studies.

## License

This dataset guide is released under [CC BY 4.0](LICENSE).
