# Statistical Master List of Public Ultrasound Resources

This table is intended as a statistical pool for the HAIC workshop paper, not as a fully verified recommendation list.

Sources merged:

- Guo/Alsharid public ultrasound seed list: 72 datasets.
- U2-BENCH source datasets: underlying sources listed in the U2-BENCH appendix/task summary, deduplicated against the Guo seed list where names match.
- Current curated-guide extras: datasets already maintained in this repository but not found in the two source pools above.

Summary as updated on 2026-06-29:

| Count | Value |
|---|---:|
| Primary statistical pool: Guo72 + U2-BENCH non-duplicates | 81 |
| Total unique rows in master list | 96 |
| Rows from Guo72 seed list | 72 |
| Rows appearing in U2-BENCH source list | 36 |
| Overlap between Guo72 and U2-BENCH sources | 27 |
| U2-BENCH-only source rows | 9 |
| Current curated-guide extras | 15 |
| Rows with verified/evidence links | 48 |
| Candidate links needing recheck | 3 |
| Rows still needing source URL verification | 45 |

Important interpretation notes:

- `U2-BENCH` itself is included as a derived benchmark row in the expanded living-guide table, while its underlying source datasets are also tracked separately.
- The main paper statistics should report clearly whether the denominator is the primary statistical pool or the expanded living-guide table. Current curated-guide extras are included for maintenance and HAIC-oriented examples.
- The public CSV is simplified for GitHub readers: internal source-bookkeeping columns are omitted, and `task_family` records the mapped task family or families for each row.
- `dataset_url` is preferred for dataset/project access. `paper_or_evidence_url` may be a paper, DOI, arXiv page, or benchmark evidence link when a direct dataset URL is not yet verified.
- `needs_url_verification` means the item can be included in coverage statistics, but should not yet be presented as a ready-to-use dataset recommendation.
- `candidate_needs_recheck` means a URL exists in the curated guide, but the resource is still marked as candidate or unstable and should be rechecked before recommendation.
- `SonoDQS` comes from the Guo/Alsharid seed catalogue and describes documentation/reporting quality, not HAIC readiness.

CSV file: [../data/statistical_dataset_master.csv](../data/statistical_dataset_master.csv).

## Preview

| Dataset | Task family | Anatomy | Task/scenario | Dataset link status |
|---|---|---|---|---|
| FETAL PLANES DB | recognition_classification; quality_acquisition | Fetus, fetal abdomen, fetal brain, fetal femur, fetal thorax, maternal cervix | Fetal standard plane identification | verified_or_from_u2bench_source |
| RESECT | reconstruction_registration | Brain |  | needs_url_verification |
| DDTI | recognition_classification; segmentation_localization | Thyroid | Thyroid nodule identification; thyroid nodule localisation | evidence_link_only |
| Ultrasound nerve segmentation | segmentation_localization | Brachial plexus |  | verified_or_curated |
| Ultrasound image enhancement | reconstruction_registration | Thyroid, liver, breast, kidney, and carotid artery |  | needs_url_verification |
| Tufts medical echocardiogram dataset (TMED) | recognition_classification; measurement_quantification | Aortic stenosis, heart |  | needs_url_verification |
| COVIDx-US | recognition_classification | Lung |  | verified_or_curated |
| The open kidney ultrasound data set | recognition_classification; quality_acquisition; segmentation_localization | Kidney | Kidney multi-class semantic segmentation; kidney view labels; multi-rater annotation variability | verified_or_from_u2bench_source |
| FPUS23 | recognition_classification; quality_acquisition; report_vqa_reasoning | Ultrasound fetus phantom | Fetal diagnostic plane identification; fetal ultrasound report generation | evidence_link_only |
| Echocardiogram videos (EchoNet-Dynamic) | measurement_quantification | Heart |  | verified_or_curated |
