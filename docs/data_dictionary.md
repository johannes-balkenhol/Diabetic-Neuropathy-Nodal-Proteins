# Data dictionary

## Clinical variables
| Variable | Type | Unit | Description |
|---|---|---|---|
| NIS_LL | float | score 0–88 | Neuropathy Impairment Score lower limb |
| NPSI | float | score 0–100 | Neuropathic Pain Symptom Inventory |
| SAS | float | score | Sheffield Assessment Scale |
| SNAP_sural | float | µV | Sural nerve SNAP amplitude |
| IENFD_per_mm | float | fibres/mm | Intraepidermal nerve fibre density |
| HbA1c_pct | float | % | Glycated haemoglobin |
| disease_duration_months | float | months | Time since diabetes diagnosis |

## ACF measures
| Variable | Unit | Description |
|---|---|---|
| acf_peak_mean_nm | nm | Mean ACF periodicity across ROIs per patient |
| acf_peak_sd_nm | nm | SD of ACF periodicity — marker of structural irregularity |

## Image metadata
| Parameter | Value | Note |
|---|---|---|
| Pixel size | ~20.4 nm/px | Estimated; original acquisition files not available |
| Image shape | (41, 599, 1721) | Angles × H × W |
| Angle range | −20° to +20°, 1° steps | 41 frames |
| Bit depth | 16-bit uint | |
