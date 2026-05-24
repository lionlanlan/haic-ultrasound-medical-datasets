# Public Ultrasound Medical Datasets for HAIC Research

A curated, public dataset guide for ultrasound medical imaging and human-AI collaboration (HAIC) research.

This repository focuses on datasets that can help researchers in the ultrasound community quickly understand what public data exists, what each dataset can be used for, and what is still missing for collaborative ultrasound AI.

## Scope

This list prioritizes:

- public or request-access ultrasound datasets;
- datasets with official download pages, challenge pages, or stable repositories;
- datasets with a paper, data descriptor, or representative high-impact usage paper;
- resources that can support HAIC topics such as AI-assisted diagnosis, report generation, quality assessment, skill augmentation, measurement support, active learning, and human-in-the-loop evaluation.

General radiology, pathology, and surgery datasets are useful for HAIC methodology, but they are not the main focus of this repository. The main table is ultrasound-first.

## Main Dataset Table

The structured source of truth is [`data/datasets.csv`](data/datasets.csv). It includes:

- official dataset or source links;
- paper or representative usage links;
- access status and license notes;
- beginner-friendly use cases;
- HAIC relevance;
- limitations for ultrasound human-AI collaboration.

## Starter View

| Dataset | Ultrasound area | Public source | Paper/source | Beginner use | HAIC relevance |
|---|---|---|---|---|---|
| EchoNet-Dynamic | Echocardiography video | [Project](https://echonet.github.io/dynamic/) | [Nature 2020](https://www.nature.com/articles/s41586-020-2145-8) | Ejection fraction and measurement assistance | Video-based interpretation and measurement workflow |
| CAMUS | Echocardiography | [Challenge](https://www.creatis.insa-lyon.fr/Challenge/camus/) | [arXiv](https://arxiv.org/abs/1908.06948) | Cardiac chamber segmentation | Human-AI measurement and contour correction |
| Fetal Planes DB | Fetal ultrasound | [Zenodo](https://zenodo.org/record/3904280) | [Scientific Reports 2020](https://www.nature.com/articles/s41598-020-67076-5) | Standard-plane classification | Skill support for view acquisition |
| HC18 | Fetal ultrasound | [Grand Challenge](https://hc18.grand-challenge.org/) | [Zenodo](https://zenodo.org/records/1322001) | Head circumference measurement | Measurement assistance and quality control |
| BUSI | Breast ultrasound | [Dataset page](https://scholar.cu.edu.eg/?q=afahmy/pages/dataset) | [Data in Brief 2019](https://doi.org/10.1016/j.dib.2019.104863) | Lesion classification and segmentation | AI-assisted lesion localization |
| OASBUD | Breast ultrasound | [Zenodo](https://zenodo.org/record/545928) | [Medical Physics](https://doi.org/10.1002/mp.12538) | Lesion analysis with RF data | Reader support and uncertainty studies |
| BUS-UCLM | Breast ultrasound | [GitHub](https://github.com/noeliavallez/BUS-UCLM-Dataset) | [Scientific Data 2025](https://doi.org/10.1038/s41597-025-04562-3) | Lesion segmentation | Interactive boundary correction |
| COVID-19 POCUS | Point-of-care ultrasound | [GitHub](https://github.com/jannisborn/covid19_pocus_ultrasound) | [NPJ Digital Medicine 2021](https://www.nature.com/articles/s41746-021-00475-z) | Video classification and triage | POCUS training and triage support |
| DDTI | Thyroid ultrasound | [Dataset page](https://service.tib.eu/ldmservice/dataset/ddti-dataset) | [JMI 2015](https://doi.org/10.1117/1.JMI.2.1.014505) | Thyroid nodule classification and segmentation | Ultrasound reporting and localization baseline |
| TN3K | Thyroid ultrasound | [Repository](https://github.com/haifangong/TRFE-Net-for-thyroid-nodule-segmentation) | [arXiv](https://arxiv.org/abs/2101.12386) | Thyroid nodule segmentation | Interactive segmentation and correction baseline |
| U2-BENCH | Ultrasound VLM benchmark | Candidate to verify | Candidate to verify | LVLM evaluation | Ultrasound assistant evaluation |

## How New Researchers Can Use This List

1. Choose a clinical ultrasound area: cardiac, fetal, breast, thyroid, abdominal, vascular, or POCUS.
2. Start with datasets that have stable public links and clear papers.
3. Match the dataset to a HAIC question:
   - Can AI help a clinician measure more consistently?
   - Can AI help a trainee acquire a better standard plane?
   - Can AI explain where a lesion or anatomy is located?
   - Can AI reduce disagreement or uncertainty?
   - Can a human correct AI outputs efficiently?
4. Check what human signal is available: labels, masks, measurements, reports, view quality, videos, multi-reader annotations, or workflow traces.
5. Document what is missing before designing a new data collection protocol.

## Why This Matters for Ultrasound HAIC

Most public ultrasound datasets are useful for model development but incomplete for HAIC. They often provide images, videos, labels, and masks, but rarely include:

- probe trajectory and contact force;
- operator gaze, speech, or intention;
- trainee/expert skill labels;
- view-search process before the final saved frame;
- AI suggestion logs and human correction behavior;
- multi-clinician disagreement and confidence;
- workflow context linking acquisition, diagnosis, reporting, and intervention.

This gap motivates future ultrasound HAIC datasets that record both the medical images and the human-AI collaboration process.

## Contributing

Please open an issue or pull request using `.github/ISSUE_TEMPLATE/add_dataset.md`.

Useful contributions include:

- adding a public ultrasound dataset;
- adding an official download link;
- adding a paper or highly cited usage paper;
- correcting license or access notes;
- adding a HAIC use case;
- explaining a limitation that new users should know.

## License

This dataset guide is released under [CC BY 4.0](LICENSE).
