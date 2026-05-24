# Field Definitions

The main table is maintained in `data/datasets.csv`.

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
| `human_signal` | Human-provided labels, masks, measurements, reports, skill signals, or reasoning/evaluation traces. |
| `beginner_friendly_tasks` | Practical starting tasks for new researchers. |
| `haic_relevance` | Why the dataset can support human-AI collaboration research. |
| `limitations` | Missing information or risks for HAIC use. |
| `status` | `ready` for entries with a plausible public source; `candidate` for entries requiring access/license verification. |

## Maintenance Rules

- Prefer official dataset pages over secondary mirrors.
- Include a paper or representative usage link whenever possible.
- Mark uncertain entries as `candidate`.
- Keep the main table ultrasound-first.
- Do not claim a dataset is fully open unless access and license have been checked.

