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
- `dataset_url` is preferred for dataset/project access. `paper_or_evidence_url` may be a paper, DOI, arXiv page, or benchmark evidence link when a direct dataset URL is not yet verified.
- `needs_url_verification` means the item can be included in coverage statistics, but should not yet be presented as a ready-to-use dataset recommendation.
- `candidate_needs_recheck` means a URL exists in the curated guide, but the resource is still marked as candidate or unstable and should be rechecked before recommendation.
- `SonoDQS` comes from the Guo/Alsharid seed catalogue and describes documentation/reporting quality, not HAIC readiness.

CSV file: [../data/statistical_dataset_master.csv](../data/statistical_dataset_master.csv).

## Preview

| Dataset | Source | Anatomy | Task/scenario | Dataset link status |
|---|---|---|---|---|
| FETAL PLANES DB | guo72+u2bench | Fetus, fetal abdomen, fetal brain, fetal femur, fetal thorax, maternal cervix | Fetal standard plane identification | verified_or_from_u2bench_source |
| RESECT | guo72 | Brain |  | needs_url_verification |
| DDTI | guo72+u2bench | Thyroid | Thyroid nodule identification; thyroid nodule localisation | evidence_link_only |
| Ultrasound nerve segmentation | guo72 | Brachial plexus |  | verified_or_curated |
| Ultrasound image enhancement | guo72 | Thyroid, liver, breast, kidney, and carotid artery |  | needs_url_verification |
| Tufts medical echocardiogram dataset (TMED) | guo72 | Aortic stenosis, heart |  | needs_url_verification |
| COVIDx-US | guo72 | Lung |  | verified_or_curated |
| The open kidney ultrasound data set | guo72+u2bench | Kidney | Kidney detection; kidney diagnostic view identification | verified_or_from_u2bench_source |
| FPUS23 | guo72+u2bench | Ultrasound fetus phantom | Fetal diagnostic plane identification; fetal ultrasound report generation | evidence_link_only |
| Thyroid ultrasound cine-clip | guo72 | Thyroid |  | needs_url_verification |
| Reconstructing of 2D ultrasound (US) images into a 3D volume | guo72 | Forearms |  | needs_url_verification |
| Fetal abdominal structures segmentation dataset using ultrasonic images | guo72+u2bench | Fetal abdomen, fetal liver, fetal stomach, fetal aorta artery, fetal spine, intrahepatic portion of the umbilical vein | Fetal abdominal organ detection | verified_or_from_u2bench_source |
| Echocardiogram videos (EchoNet-Dynamic) | guo72 | Heart |  | verified_or_curated |
| FALLMUD | guo72+u2bench | Fascia lata | Muscle detection | verified_or_from_u2bench_source |
| Micro-ultrasound prostate segmentation dataset | guo72+u2bench | Prostate | Prostate localisation; prostate diagnostic view identification | verified_or_from_u2bench_source |
| CAMUS | guo72+u2bench | Heart | Ejection fraction estimation; atrium and ventricle localisation | verified_or_from_u2bench_source |
| Echocardiography (EchoNet-LVH) | guo72 | Heart |  | needs_url_verification |
| Regensburg Pediatric Appendicitis Dataset | guo72 | Appendix |  | needs_url_verification |
| Gallbladder ultrasound video | guo72 | Gallbladder |  | needs_url_verification |
| Gallbladder cancer ultrasound | guo72 | Gallbladder |  | needs_url_verification |
| Breast lesion detection in ultrasound videos (BUSV) | guo72+u2bench | Breast | Breast lesion classification | needs_url_verification |
| Muscle-tendon junction tracking in ultrasound images | guo72 | Muscle-tendon junction |  | needs_url_verification |
| Breast ultrasound images dataset | guo72+u2bench | Breast | Breast cancer classification; tumour localisation; diagnostic view identifica... | verified_or_from_u2bench_source |
| BITE | guo72 | Liver, gallbladder, breast, gastrointestinal, genitourinary |  | needs_url_verification |
| Dermatologic ultrasound images for classification | guo72+u2bench | Skin, hair, nail | Skin tumor classification | evidence_link_only |
