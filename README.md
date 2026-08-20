# Student Habits and Exam Performance

This project uses SQL and Tableau to examine relationships between student habits, personal circumstances, and exam scores in a 1,000-record dataset. The workflow moves from CSV ingestion and relational querying to a recruiter-friendly interactive dashboard.

## Objective

Compare exam outcomes across study time, attendance, sleep, media use, employment, and other student characteristics without treating observational relationships as causal effects.

## Tools and Technologies

- SQL and SQLite
- Python, pandas, and SQLAlchemy
- Jupyter Notebook and `ipython-sql`
- Excel and `openpyxl`
- Tableau Public

## Workflow and Analysis

1. Load the source CSV into a SQLite database.
2. Create a structured analysis table with a generated primary key.
3. Use grouped SQL queries to compare average exam scores across behavioral and demographic variables.
4. Create a separate table for students with scores of 90 or higher.
5. Export the 126 high-scoring records to Excel for additional review.
6. Present the analysis in an interactive Tableau story.

## Key Results and What This Demonstrates

- Average exam scores rose across the dataset's attendance bands: 67.94 for 50–74%, 69.20 for 75–89%, and 71.39 for 90–100% attendance.
- The notebook compares outcomes across study time, social-media use, streaming time, sleep, internet quality, employment, and extracurricular participation.
- The project demonstrates SQL aggregation, table creation, filtered data exports, and the translation of query results into an interactive visualization.

These results describe associations within this dataset and should not be interpreted as causal findings.

## Visualization

[View the interactive Tableau story](https://public.tableau.com/app/profile/david.salgado4874/viz/HabitsEffectsonExamScore/Story1)

## Repository Contents

| Path | Description |
| --- | --- |
| [`SQLPrac.ipynb`](SQLPrac.ipynb) | SQL queries, outputs, and supporting Python workflow |
| [`student_habits_performance.csv`](student_habits_performance.csv) | Source dataset with 1,000 student records |
| [`top_scorers.xlsx`](top_scorers.xlsx) | Export of records with exam scores of 90 or higher |

## Viewing and Reproducibility Notes

[View the notebook in nbviewer](https://nbviewer.org/github/Salgadod123/Habits-Effects-on-Exam-Score-Project/blob/main/SQLPrac.ipynb) if GitHub does not render every query output.

The notebook currently references local file paths and a local `Process` helper module. The included dataset and saved outputs allow the analysis to be reviewed, but those dependencies must be replaced or provided before the notebook can run unchanged on another computer.
