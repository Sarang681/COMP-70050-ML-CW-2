# 70050 Coursework 2: Predicting housing values in 2020

Group: _TODO: names / usernames_

## Setup

**Lab machines (what TAs use):**
```bash
source /vol/lab/ml/mlvenv/bin/activate
jupyter lab
```

**Locally with uv:**
```bash
uv sync
uv run jupyter lab   # or select .venv as the kernel in VS Code / PyCharm
```

## Data
Put the provided files in `data/`:
`housing_1990.csv`, `housing_2020_train.csv`, `housing_2020_test.csv`, `mlp_1990.pt`, `mlp_1990.json`.

## Layout
```
task1.ipynb   Task 1A (MLP from scratch) + 1B (moment matching, fine-tuning)
task2.ipynb   Task 2A–2D (cross-attention, LoRA, transfer, variations, ablation)
data/         provided data and the 1990 MLP
figures/      plots saved by the notebooks, used in the report
```

## Reproducing results
Run each notebook top to bottom (Kernel → Restart & Run All). Every figure and table in the report is produced by a cell in one of them.

## Conventions
- Fixed random seeds for every run.
- Standardisation statistics come from the training subset only (the 4 training folds, or all 500 rows for the final model).
- Full-batch training: 1 epoch = 1 gradient step.
- The test set is used only for the final evaluations (1A-A5 and 2D).
