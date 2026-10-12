# Data dictionary

Scores run from 0 (the task cannot be performed by current GenAI) to 1 (it could be performed entirely by GenAI). They measure technical potential, not expected job loss. See the working paper for the method.

## `POLAND_FINAL_6digit_scores.xlsx` (one row per task, 29,700 rows, 2,541 occupations)

| Variable | Meaning |
|---|---|
| `Kod`, `Nazwa` | Six-digit code and Polish name of the occupation (KZiS) |
| `Occupation Title` | English occupation title |
| `Filtr: zadania do aktualizacji` | Flag (1 or 0): 1 marks 414 tasks flagged for update in the review of Polish tasks, 0 all others |
| `Synteza` | Polish summary text of the task, from the KZiS occupation description |
| `Task_Index` | Task number within the occupation |
| `task_full_text_PL`, `task_full_text_ENG` | Task text in Polish and its English translation |
| `Weaviate Status1`, `Weaviate Status2` | Status (success or fail) of the two retrieval calls to the Weaviate vector database that supplies similar, already-scored tasks to the scoring assistant. Two tasks show "fail" in both (occupation 342304 task 8, occupation 342307 task 1) |
| `score25` | Final 2025 task score |
| `prediction_justification_gemni1.5` | The model's written reasoning for the score (the column name keeps its original spelling) |
| `isco08_1d`, `description_1d`, `label1d` | ISCO-08 major group the occupation maps to (code, name, "code - name"). Empty for 60 task rows whose national group has no ISCO-08 counterpart in the mapping |
| `label6d` | "code - Polish name" of the occupation |
| `potential25` | 2025 exposure category of the occupation (see below) |
| `tasks_per_kod` | Number of tasks listed for the occupation |
| `task_color` | Score band of the task (see below) |
| `mean6d_pl`, `SD6d_pl` | Mean and standard deviation of the occupation's task scores (same value on every task row of the occupation) |

## `Poland_6digit_tree_plot_EN.xlsx` (one row per task)

A reduced table used to draw the tree viewer: `isco08_1d` to `isco08_4d` give the ISCO-08 groups ("code - title", "NA - NA" where there is no mapping), `isco08_6d` the Polish occupation, `isco08_6d_task` the task written as "(2025 score) - task text", and `potential25` and `task_color` as below.

## `ISCO_mapping.csv`

Lookup of ISCO-08 four-digit occupations (`isco08_4d`, `description_4d`) to their three-, two- and one-digit parent groups.

## Score bands (`task_color`)

`task_color` bins the task score: Very Low (below 0.25), Low (0.25 to 0.49), Medium (0.50 to 0.74), High (0.75 and above). It is used to colour tasks in the tree viewer.

## Exposure categories (`potential25`)

`potential25` is the exposure category of the **occupation**, repeated on every task row of that occupation. It is not a task-level value. It is set from the occupation's mean (μ) and standard deviation (σ) of task scores:

| Category | Rule |
|---|---|
| Exposed: Gradient 4 | μ ≥ 0.6 and μ − σ ≥ 0.5 |
| Exposed: Gradient 3 | 0.5 ≤ μ < 0.6 and μ + σ ≥ 0.5 |
| Exposed: Gradient 2 | 0.4 ≤ μ < 0.5 and μ + σ ≥ 0.5 |
| Exposed: Gradient 1 | μ < 0.4 and μ + σ ≥ 0.5 |
| Minimal Exposure | μ < 0.5 and μ + σ > 0.4 |
| Not Exposed | everything else |

Because the category repeats on each task row, counting rows counts tasks, not occupations.
