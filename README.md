# SDSC3002_Cityu

Coursework for **SDSC3002 Data Mining** at City University of Hong Kong. The notebooks implement frequent-pattern mining, k-core numbers on a graph, and an SVD recommender.

These are my assignment solutions, shared for reference — please do not copy them for your own submissions.

## Files

| Path | What it covers |
| --- | --- |
| [`Assignment1/Q4.ipynb`](Assignment1/Q4.ipynb) | **Apriori** frequent itemsets on [`Assignment1/trans.txt`](Assignment1/trans.txt) (one transaction per line). Reports the number of frequent patterns for minimum frequencies `0.0001`–`0.0005`. See [`Assignment1/Question4.txt`](Assignment1/Question4.txt) for the brief and [`Assignment1/README.txt`](Assignment1/README.txt) for how the class is structured. |
| [`Assignment2/Q4.ipynb`](Assignment2/Q4.ipynb) | **k-core** numbers for each node in a graph. Reads an edge list from `DBLP.txt` (skips a header line) and writes `node:core` lines to `result.txt`. |
| [`Assignment3/Q4.ipynb`](Assignment3/Q4.ipynb) | **SVD** recommender with [`scikit-surprise`](https://surpriselib.com/): 10-fold CV (RMSE) on `training.txt`, then predictions for `testing.txt` written to `prediction.txt` as `user,item,rating`. |
| `item_tag.txt` | Item-to-tag data at the repo root (`item:tag,tag,...`) |

Run each notebook from its own assignment folder so the relative data paths work.

## Requirements

- Python 3 and [Jupyter](https://jupyter.org/)
- Assignments 1–2: standard library only
- Assignment 3: `numpy`, `pandas`, `scikit-surprise`

```bash
python3 -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install jupyter numpy pandas scikit-surprise
jupyter notebook
```

## Data files that are not in this repo

- **Assignment 2:** `DBLP.txt` and `result.txt` in the repo are empty placeholders. Put the real edge list next to the notebook before running it.
- **Assignment 3:** `training.txt` and `testing.txt` are required by the notebook but are not committed here. Place them in `Assignment3/` (CSV with columns `user,item,rating`, no header).

## Licence

MIT — see [LICENSE](LICENSE).
