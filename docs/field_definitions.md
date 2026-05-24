# Field Definitions

The dataset table is maintained in `data/datasets.csv`.

| Field | Meaning |
|---|---|
| `name` | Dataset or benchmark name. |
| `domain` | Clinical or research area. |
| `modality` | Imaging or procedural modality. |
| `data_type` | What the dataset contains. |
| `human_signal` | Human annotations, reports, gaze, skill labels, disagreement, or workflow information. |
| `haic_use_case` | Concrete human-AI collaboration research tasks enabled by the dataset. |
| `access_status` | Public, public with credentialing, public request, challenge access, candidate to verify, etc. |
| `official_url` | Official dataset page or primary repository. |
| `ultrasound_relevance` | Why the dataset matters for ultrasound HAIC. |
| `limitations` | Known limits for HAIC research. |
| `status` | `ready` for entries with a known public source; `candidate` for survey-derived entries that need access/license verification. |

