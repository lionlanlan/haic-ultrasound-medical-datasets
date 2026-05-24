# Awesome HAIC Medical Datasets

A living list of public dataset resources for human-AI collaboration (HAIC) research in medical imaging, procedure analysis, and clinical skill augmentation.

This repository is designed as a companion resource for workshop-style papers and early-stage HAIC projects. The goal is not to list every medical dataset, but to identify datasets that can support questions about human judgment, AI assistance, disagreement, workflow, explanation, skill, and interaction.

## What Counts as HAIC-Relevant?

We tag a dataset as HAIC-relevant when it contains, or can reasonably support the study of, at least one of the following signals:

- **Human judgment**: multi-reader labels, disagreement, confidence, reports, diagnoses, or clinical measurements.
- **Human attention**: gaze, bounding boxes, region references, localization, or explanation traces.
- **Workflow context**: procedure phase, action, tool use, temporal sequence, or clinical process state.
- **Skill signal**: operator expertise, gesture quality, scanning quality, or training feedback.
- **Human-in-the-loop potential**: annotation refinement, active learning, AI-assisted reporting, triage, or collaborative decision-making.
- **Embodied interaction**: robot action, probe motion, control trajectory, or language-to-action planning.

## Dataset Taxonomy

| Category | HAIC value | Representative resources |
|---|---|---|
| Multi-reader diagnostic datasets | Model human disagreement and complementarity | LIDC-IDRI, VinDr-CXR |
| Image-report datasets | Study AI-assisted reporting and VLM grounding | MIMIC-CXR, PadChest |
| Gaze and attention datasets | Align AI explanations with human visual search | REFLACX |
| Ultrasound image/video datasets | Build ultrasound HAIC baselines and identify missing interaction signals | EchoNet-Dynamic, CAMUS, BUSI, Fetal Planes DB |
| Procedure and skill datasets | Study clinical skill augmentation and workflow support | JIGSAWS, Cholec80, CholecT45, EndoVis |
| VQA and instruction datasets | Evaluate multimodal assistants and reasoning | VQA-RAD, SLAKE, PathVQA |
| Survey-derived ultrasound VLM benchmarks | Track emerging ultrasound-specific HAIC resources | U2-BENCH, FETAL-GAUGE, ReMUD, PRS-Med |

## Starter Table

The structured source of truth is [`data/datasets.csv`](data/datasets.csv). A compact starter view is below.

| Dataset | Modality | HAIC signal | Example HAIC use case | Status |
|---|---|---|---|---|
| MIMIC-CXR | Chest X-ray | Images and free-text reports | AI-assisted reporting, report-grounded explanation | Public, credentialed |
| REFLACX | Chest X-ray | Eye gaze, reports, localization | Human attention modeling, gaze-aware explanation | Public, credentialed |
| VinDr-CXR | Chest X-ray | Multi-radiologist annotations | Disagreement-aware diagnosis, complementarity | Public, credentialed |
| LIDC-IDRI | Chest CT | Multi-reader contours and nodule ratings | Human disagreement, uncertainty-aware AI | Public |
| EchoNet-Dynamic | Echocardiography video | Expert measurements and tracings | Measurement assistance, video-based echo support | Public application |
| CAMUS | Echocardiography | Segmentation and cardiac measurements | Human-AI measurement workflow baseline | Public |
| Fetal Planes DB | Fetal ultrasound | Standard-plane labels | Skill support for fetal view acquisition | Public |
| HC18 | Fetal ultrasound | Head circumference annotation | Measurement assistance and quality control | Public challenge |
| BUSI | Breast ultrasound | Lesion labels and masks | AI-assisted lesion localization baseline | Public |
| OASBUD | Breast ultrasound | Lesion labels and outlines | Reader support and uncertainty studies | Public |
| COVID-19 POCUS | Point-of-care ultrasound | Video clips and diagnostic labels | Triage support and operator training baseline | Public |
| JIGSAWS | Surgical robotics | Gesture labels, kinematics, skill | Skill assessment, human-AI coaching | Public application |
| Cholec80 | Laparoscopic video | Surgical phase labels | Workflow-aware AI assistance | Public request |
| CholecT45 | Laparoscopic video | Tool-action-target triplets | Procedure understanding and action assistance | Public request |
| EndoVis challenges | Endoscopic/surgical video | Tools, actions, anatomy | Intraoperative AI assistance | Public challenge |
| VQA-RAD | Radiology VQA | Human question-answer pairs | Medical VLM reasoning and collaboration | Public |
| SLAKE | Medical VQA | Questions, answers, knowledge | Knowledge-grounded VLM support | Public |
| PathVQA | Pathology VQA | Image-question-answer pairs | Multimodal assistant evaluation | Public |
| U2-BENCH | Ultrasound VLM benchmark | Ultrasound reasoning tasks | Ultrasound LVLM evaluation | Candidate, verify access |
| FETAL-GAUGE | Fetal ultrasound benchmark | Fetal reasoning/evaluation | Fetal ultrasound assistant evaluation | Candidate, verify access |
| ReMUD / HAIBU-ReMUD | Ultrasound reasoning dataset | Reasoning-oriented multimodal data | Ultrasound instruction tuning and reasoning | Candidate, verify access |
| PRS-Med | Medical segmentation/reasoning | Position reasoning prompts | Human-style spatial reasoning for segmentation | Candidate, verify access |

## How to Use This List

1. Start with the HAIC signal, not the modality.
2. Choose datasets with explicit human traces when possible.
3. Use conventional labels-only datasets as baselines, then explain what interaction information is missing.
4. For ultrasound projects, separate diagnostic labels from acquisition skill, probe motion, view quality, and operator feedback.
5. Record access constraints and licenses before designing a benchmark.

## Ultrasound Gap Map

Public ultrasound datasets are useful for quick starts, but most are not complete HAIC datasets. Common missing signals include:

- probe trajectory and contact force;
- operator gaze, speech, and scanning intention;
- view-search process rather than only final selected frames;
- trainee/expert skill labels;
- AI suggestion logs and human correction behavior;
- uncertainty, disagreement, and confidence from multiple clinicians;
- workflow context linking acquisition, diagnosis, reporting, and intervention.

These gaps motivate prospective ultrasound HAIC data collection focused on collaborative scanning, skill augmentation, and human-AI decision-making.

## Contributing

Please open an issue or pull request using the template in `.github/ISSUE_TEMPLATE/add_dataset.md`. New entries should include an official URL, access status, license notes, and at least one HAIC use case.

