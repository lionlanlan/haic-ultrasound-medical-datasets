# Workshop Position Outline

## Working Title

Public Ultrasound Medical Dataset Resources for Human-AI Collaboration: A Starting Point Toward Collaborative Ultrasound AI

## Core Claim

Public ultrasound datasets are usually organized by organ, modality, and model task, but HAIC research needs a different view: whether a dataset contains human judgment, measurements, annotations, workflow, skill, or interaction signals that make human-AI collaboration measurable.

## Link to the Ultrasound VLM Survey

The ultrasound VLM survey shows rapid progress in:

- ultrasound vision-language models for perception and diagnosis;
- ultrasound benchmarks and instruction-tuned assistants;
- agentic and robotic ultrasound systems;
- VLA-style planning for scanning and intervention.

However, most public ultrasound resources still lack the signals needed for HAIC research: probe motion, operator intent, gaze, spoken reasoning, skill level, AI suggestion logs, human correction, and collaborative decision traces.

## Proposed Contributions for a 4-Page HAIC Paper

1. A HAIC-oriented taxonomy of public ultrasound datasets.
2. A curated, maintainable resource list with public source links, paper links, access status, and HAIC use cases.
3. A starter guide connecting ultrasound dataset types to beginner-friendly research tasks.
4. An ultrasound gap analysis motivating future collaborative ultrasound data collection.

## Suggested 4-Page Structure

### Page 1: Motivation

- HAIC asks different questions from conventional medical AI.
- Many researchers know individual ultrasound datasets such as EchoNet-Dynamic, CAMUS, BUSI, and fetal plane datasets, but there is no practical map showing which ones support HAIC.
- Dataset suitability should be judged by human signals and workflow context, not only by modality and labels.

### Page 2: Taxonomy

Include a figure mapping datasets by HAIC signal:

- human judgment and disagreement;
- human attention and explanation;
- reports and language grounding;
- procedure workflow and skill;
- ultrasound acquisition and measurement;
- embodied action and robotics.

### Page 3: Resource Table

Use a compact representative table from `data/datasets.csv`, with columns:

- dataset;
- public source link;
- paper or representative usage paper;
- ultrasound area;
- human signal;
- beginner-friendly task;
- HAIC use case;
- access/license note;
- limitation.

### Page 4: Ultrasound Case Study and Roadmap

- Show how current ultrasound datasets support only partial HAIC.
- Identify missing signals for collaborative ultrasound AI.
- Propose a future collection protocol for ultrasound HAIC:
  - image/video stream;
  - probe motion;
  - operator gaze and speech;
  - trainee/expert labels;
  - AI suggestions;
  - human corrections;
  - outcome and report.

## Candidate Figure

Figure 1: "From Medical AI Datasets to HAIC Datasets"

Left: conventional dataset labels.

Middle: HAIC signals.

Right: research tasks such as complementarity, skill augmentation, interactive reporting, active learning, and robotic assistance.
