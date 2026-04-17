Synthetic UBA dataset.

Contents:
- synthetic_normal_events_14days.csv: 14 days of normal event-level behaviour
- synthetic_abnormal_events.csv: anomaly scenarios for later testing
- synthetic_training_windows.csv: model-ready windows for your current Isolation Forest pipeline
- synthetic_abnormal_windows.csv: model-ready abnormal windows for testing
- dcarter_normal_events.csv / sahmed_normal_events.csv / jwalker_normal_events.csv
- dcarter_training_windows.csv / sahmed_training_windows.csv / jwalker_training_windows.csv
- uba_synthetic.db: SQLite database with all tables

Quick use in your current project:
1. Copy synthetic_training_windows.csv into your project's data folder and rename to training_windows.csv
2. Train:
   python train_model.py --training-csv data/training_windows.csv --model-out models/isolation_forest.joblib
