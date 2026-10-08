# Repository Standard

Every repository on this account follows the same rules, so any project can be read, run, and reviewed in the same way.

<sub>VERSION 1.0 · OCTOBER 2026</sub>

## 1. Layout

Each repository uses only the folders it needs, always with these names and purposes.

| Path | Purpose |
|---|---|
| `README.md` | What the project is, what it contains, and how to run it |
| `src/` | Final, reusable code |
| `experiments/` | Exploratory scripts and earlier attempts, kept in order |
| `notebooks/` | Jupyter notebooks that are not part of an experiment sequence |
| `docs/` | Notes, proposals, reading lists, and reports |
| `outputs/` | Generated files such as logs and figures |
| `data/` | Local data only; raw data is never committed |
| `requirements.txt` | Python dependencies used by the code |

## 2. Naming

- File and folder names are lowercase `snake_case`.
- Every file carries the extension that matches its content.
- Attempts are numbered in the order they were made: `01_baseline.py`, `02_edge_detection.py`.
- The final version has a descriptive name and no number, so it is clear which file to use.
- Arduino sketches follow the Arduino convention: `src/<sketch_name>/<sketch_name>.ino`.

## 3. README

Every README has the same sections, in the same order:

1. Title and a one-sentence summary
2. A metadata line: category, year, and stack
3. **Overview**: the problem, the approach, and what the files contain
4. **Contents**: every top-level file and folder except the README itself, with one line each
5. **Usage**: how to install and run, when the code is runnable
6. **Notes**: status and known limitations

Categories: `RESEARCH`, `RESEARCH NOTES`, `APPLIED PROJECT`, `HARDWARE PROJECT`, `ARCHIVED COURSEWORK`, `ARCHIVED EXPERIMENT`, `WORKING NOTES`.

## 4. Data and privacy

- Credentials, tokens, and access codes are never committed; configuration comes from a local `.env`, with only `.env.example` in the repository.
- Personal, patient, and institutional data never appear in a public repository.
- Unpublished research stays private until publication; public pages describe it at topic level only.

## 5. Reproducibility

- Dependencies are listed in `requirements.txt` or the project's own manifest.
- Any result stated in a README is produced by code in the same repository.
- Paths to local data are documented in the README rather than hidden in code.

## 6. Change history

- Work happens on branches; `main` holds a reviewed state.
- Files are renamed and moved with `git mv`, never deleted and re-added, so their history stays traceable.
- Older code is kept as written; it is reorganized and documented, not silently rewritten.

## 7. Description and topics

- The About description follows one pattern: **what it is, then how**, in under 100 characters, with no trailing period.
  Example: `Billboard detection in street images using classical edge detection and OpenCV`
- Topics come from a fixed vocabulary, two to six per repository, never padded, with exactly one status topic, so related work groups together:

| Group | Topics |
|---|---|
| Field | `explainable-ai`, `medical-imaging`, `computer-vision`, `robotics`, `embedded-systems`, `data-analysis`, `machine-learning` |
| Method | `deep-learning`, `image-processing`, `object-detection`, `classification`, `decision-trees`, `llm-agents` |
| Stack | `python`, `pytorch`, `tensorflow`, `opencv`, `scikit-learn`, `arduino`, `web-application` |
| Status | `research`, `applied-project`, `coursework`, `archived` |

## 8. Status

- **Active**: under development; structure may change.
- **Archived**: finished or superseded; kept as a read-only reference.

Repositories created before this standard (2023 to 2025) were reorganized to follow it in October 2026. Their code is unchanged; only file names, locations, and documentation were updated.
