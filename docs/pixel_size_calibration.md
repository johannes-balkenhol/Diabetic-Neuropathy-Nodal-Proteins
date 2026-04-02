# Pixel size calibration note

## Estimated value
**20.4 nm/px** — used throughout the analysis pipeline.

## Source
Estimated from acquisition parameters of the dSTORM setup.
The original raw acquisition files (`.lif` / `.czi` / acquisition log)
are not available in this project folder.

## Consequence for results
- All **distance measurements** (stripe spacing in µm, ACF peak in nm)
  are approximate and depend on this estimate.
- All **ratio-based features** (signal kurtosis, Shannon FFT entropy,
  peak/valley ratio, amplitude CV, stripe CV) are dimensionless and
  **independent of pixel size** — these are the primary outcomes.
- The ACF reports peaks at ~122 nm (6 px) which is below the reliable
  detection limit (~10 px per period). The nm value is therefore not used
  as a primary outcome; only the profile stripe spacing (2–7 µm) is reported.

## To verify
Contact the microscopy facility for the original acquisition log or
check the `.lif` / `.czi` metadata of the original raw dSTORM files.
Expected pixel size for this setup: 15–25 nm/px (consistent with 20.4).
