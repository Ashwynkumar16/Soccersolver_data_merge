# Soccersolver_data_merge

## Repository Structure:

```text
.
├── .gitignore
├── README.md
├── requirements.txt
├── mainNB.ipynb                 # Master ETL and Matching Pipeline Notebook
└── data/                        # Local data directory (Not tracked by Git)
    ├── soccersolver-player-data/  # Time-series historical data
    │   ├── leagues/
    │   │   └── season_files/    # Raw JSON files
    │   ├── players/
    │   │   └── season_files/
    │   ├── teams/
    │   │   └── season_files/
    │   └── unified/             # Flattened intermediate CSVs
    ├── sofifa/                  # FIFA Ratings dataset
    ├── wyscout_data/            # Static metadata snapshot
    │   ├── cleaned/             # Normalized CSVs ready for matching
    │   └── raw/                 # Original Wyscout exports
    └── unified_tables/          # Final Pipeline Outputs
        ├── leagues/
        │   ├── matched/         # 1-to-1 gold standard files
        │   ├── no match/        # Mathematical orphans (Zero data loss)
        │   └── partial match/   # Human-in-the-loop review files
        ├── players/
        │   ├── matched/
        │   ├── no match/
        │   └── partial match/
        └── teams/
            ├── matched/
            ├── no match/
            └── partial match/
```