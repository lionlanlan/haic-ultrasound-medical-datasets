# HAIC Task-Level Taxonomy for Ultrasound Resources

This document explains the task-readiness matrix used in the paper and repository. It is not a dataset-quality score. It asks a narrower question: which recordable signals can a public ultrasound dataset provide, derive, or still fail to provide for HAIC task design?

![HAIC task-readiness matrix](../figures/haic_task_readiness_matrix.png)

## Base Signals and Evaluation Signals

We separate two kinds of information.

- **Base signals** decide whether a HAIC task can be constructed from a dataset. They include labels, masks, measurements, reports, scan states, model predictions, prediction-ground-truth differences, uncertainty scores, deferral rules, intermediate edits, and interaction logs.
- **Evaluation signals** measure what happens when people actually use the task. They include preference, time cost, workload, accept/override behavior, trust calibration, reliance, skill retention, and clinical usefulness.

The matrix classifies base-signal availability. It does not claim that user studies are unnecessary. A complete HAIC study can collect evaluation signals at any level.

## Basic Task Families

| Task family | Meaning | Typical examples |
|---|---|---|
| Recognition / classification | Predict image, video, view, disease, or anatomy class. | Disease classification, view recognition, standard-plane labels. |
| Segmentation / localization | Locate anatomy, lesions, instruments, or regions. | Masks, boxes, landmarks, ROIs. |
| Measurement / quantification | Estimate clinical quantities from images/videos. | Ejection fraction, head circumference, chamber volume, severity score. |
| Quality / acquisition | Assess image quality, protocol state, or acquisition quality. | View quality, standard-plane feedback, probe guidance. |
| Report / VQA / reasoning | Connect ultrasound data to language or reasoning. | Reports, captions, question answering, assistant outputs. |
| Reconstruction / registration | Improve, reconstruct, align, or transform ultrasound data. | Beamforming, enhancement, 3D reconstruction, registration. |

## HAIC Levels

| Level | Interaction form | Required HAIC signals |
|---|---|---|
| L1 | AI one-way output | AI prediction and reference target. |
| L2 | Human review/correction | Accept, reject, or edit action; override decision; correction cost. |
| L3 | Selective collaboration | AI confidence or uncertainty; deferral rule; coverage; selective accuracy. |
| L4 | Multi-turn interaction | Intermediate states; user action sequence; per-turn AI update; turn-level cost; convergence trajectory. |
| L5 | Longitudinal co-adaptation | Trust calibration; reliance pattern; skill retention; strategy drift; repeated-use outcomes. |

## Support Codes

| Code | Meaning |
|---|---|
| ✓ | The original dataset already contains the base target needed for this task family and level. |
| ↻ | Proxy base signals can be derived by an explicit, reproducible protocol, usually by adding model outputs, prediction-ground-truth differences, confidence scores, or deferral rules. |
| ! | Support depends on dataset-specific temporal or process signals, such as scan sequences, probe states, intermediate edits, or interaction traces. |
| - | The core base signals require new prospective human-AI interaction logs. |

The main boundary is L4. L2 and L3 are mostly outcome-level simulations: a model output can be compared with existing annotations to estimate correction burden or deferral behavior. L4 is process-level: it requires states and actions across turns. Quality/acquisition datasets are the exception because their native targets may already describe scan quality, standard-plane status, or probe guidance, which can serve as intermediate feedback during acquisition. L5 remains prospective because repeated-use adaptation cannot be recovered from static images or labels.

## Task-Family Upgrade Patterns

- Final-output tasks such as classification, measurement, and report/VQA can often move from L1 to L3 by adding predictions, confidence scores, and deferral rules.
- Spatial-output tasks such as segmentation, localization, reconstruction, and registration naturally support L2 correction protocols through clicks, scribbles, regions, contours, or transform adjustments.
- Quality/acquisition tasks are closest to L4 when they include scan sequences, probe states, standard-plane status, or action consequences.
- L5 requires longitudinal user records regardless of task family.
