# Raw EEG CSV dataset

This repository contains the CSV exports for nine pseudonymized participants (`sub-001` to `sub-009`). The directory layout from acquisition is preserved:

```text
data/sub-XXX/ses-001/run-YYYYMMDD_HHMMSS/
```

Each run contains:

- `eeg.csv`: sample-level EEG signals, timing, experimental condition, phase, and quality fields.
- `events.csv`: experiment event log.
- `block_ratings.csv`: block-level subjective ratings and task responses.
- `probes.csv`: probe responses recorded during the experiment.
- `quiz_responses.csv`: quiz answers and response metadata.
- `acquisition_qc.csv`: acquisition quality-control measurements.

`sub-007` was exported with a different file set: it has `qc.csv` in place of
`acquisition_qc.csv`, plus `probe_epochs.csv` and `windows.csv`. These files are
kept under the same subject/session/run layout.

Only CSV files needed for algorithm development are included. Raw device binaries, MAT files, JSON metadata/reports, and checksum files are intentionally excluded.

## Download

The large `eeg.csv` files are stored with Git LFS. Install [Git LFS](https://git-lfs.com/) before cloning, then run:

```bash
git lfs install
git clone https://github.com/yuuuhhhh/raw_eeg.git
```

After cloning, verify that all large files are present with:

```bash
git lfs pull
```
