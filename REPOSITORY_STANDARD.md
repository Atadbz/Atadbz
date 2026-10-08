# Repository Standard

The rules my project repositories follow, so any project can be read and reviewed in the same way.

<sub>VERSION 1.1 · OCTOBER 2026</sub>

## 1. Scope

- **Archived** repositories follow every rule below, including the layout.
- **Active** repositories follow the README, data, and metadata rules at once. They keep their working layout until they are archived, so ongoing work never breaks.

## 2. Layout

Each archived repository uses only the folders it needs, always with these names and purposes.

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

## 3. Naming

- File and folder names are lowercase `snake_case`. Conventional files keep their usual names: `README.md`, `LICENSE`, `.env.example`, and this document.
- Every file carries the extension that matches its content.
- Attempts are numbered in the order they were made: `01_baseline.py`, `02_edge_detection.py`.
- The final version has a descriptive name and no number, so it is clear which file to use.
- Arduino sketches follow the Arduino convention, `<sketch_name>/<sketch_name>.ino`, inside `src/` or `experiments/`.

## 4. README

Every README uses these parts, in this order:

1. Title and a one-sentence summary
2. A metadata line: category, year, and stack
3. **Overview**: the problem, the approach, and what the files contain
4. **Contents**: one short entry for every top-level file and folder, except the README itself and dotfiles
5. **Usage**: how to install and run; left out when there is nothing to run
6. **Notes**: status and known limitations
7. A closing line that links to this standard

Categories: `RESEARCH`, `RESEARCH NOTES`, `APPLIED PROJECT`, `HARDWARE PROJECT`, `ARCHIVED COURSEWORK`, `ARCHIVED EXPERIMENT`, `WORKING NOTES`.

## 5. Data and privacy

- New code reads credentials, tokens, and access codes from a local `.env`; only `.env.example` is committed.
- Personal, patient, and institutional data never appear in a public repository.
- Unpublished research stays private until publication; public pages describe it at topic level only.

## 6. Reproducibility

- Dependencies are listed in `requirements.txt` or the project's own manifest.
- Any result stated in a README is produced by code in the same repository.
- Paths to local data are documented in the README rather than left for the reader to discover.

## 7. Change history

- Work happens on branches; `main` holds a reviewed state.
- Files are renamed and moved with `git mv`, never deleted and re-added, so their history stays traceable.
- Archived code is kept as written. Where it predates sections 5 and 6, for example hardcoded paths or placeholder codes, its README Notes say so.

## 8. Description and topics

- The About description follows one pattern: **what it is, then how**, in under 100 characters, with no trailing period.
  Example: `Green signboard detection and alignment in photos using OpenCV color masking and contours`
- Topics come from a fixed vocabulary, two to six per repository, never padded, so related work groups together:

| Group | Topics |
|---|---|
| Field | `explainable-ai`, `medical-imaging`, `computer-vision`, `robotics`, `embedded-systems`, `data-analysis`, `machine-learning` |
| Method | `deep-learning`, `image-processing`, `object-detection`, `classification`, `decision-trees`, `llm-agents` |
| Stack | `python`, `pytorch`, `tensorflow`, `opencv`, `scikit-learn`, `arduino`, `web-application` |
| Status | `research`, `applied-project`, `coursework`, `archived` |

- Every repository carries exactly one status topic. An archived repository always uses `archived`, whatever its category.

## 9. Status

- **Active**: under development; layout may change.
- **Archived**: finished or superseded; kept as a read-only reference.

Repositories that existed before this standard were brought in line with it in October 2026. Their code is unchanged: file names, locations, and documentation were updated, and a `requirements.txt` was added where one was missing.
