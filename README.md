# Market Research Lab

This repository hosts the **Market Research Lab**, a modular research system for exploring and analysing U.S. stock market data.

The goal is to build a reproducible pipeline that:

* Ingests market, sentiment and fundamentals data from external APIs.
* Engineers features suitable for machine learning models.
* Trains and evaluates models to generate **signals** indicating potential trade opportunities.
* Applies risk management and constructs hypotheses rather than executing trades automatically.

The lab is structured as a series of independent modules (under `src/`) that can be developed and tested in isolation. Each milestone in the project roadmap will extend this foundation.

For more details on the project plan and milestones, see the documentation in the `docs/` directory.

## Repository Layout

```
market-research-lab/
├── data/              # scratch space for local datasets (excluded from git)
├── docs/              # design documents, architecture diagrams and project plans
├── notebooks/         # exploratory notebooks and experiments
└── src/               # source code for the research pipeline
    ├── ingestion/     # downloading and caching raw data from external sources
    ├── features/      # feature engineering and preprocessing
    ├── models/        # model definitions and training routines
    ├── signals/       # signal generation logic
    ├── risk/          # risk management utilities
    └── utils/         # shared helper functions
```

## Getting Started

1. **Install Python 3.11+** and create a virtual environment:
   - https://www.python.org/downloads/release/python-3110/

   ```
   ✔️ CHECK THIS BOX:
   ☑ Add Python to PATH
   Then click:
   Customize Installation → Install
   ```

   ```
   py install 3.11
   py 3.11 -m venv .venv      
   .venv/bin/activate
   ```

2. **Install dependencies:**

   ```
   pip install --upgrade pip
   pip install -r requirements.txt
   ```

3. **Configure API keys:**

   Create a `.env` file in the repository root based on the template `.env.sample`. This file should provide your API credentials (e.g., `ALPACA_API_KEY`, `ALPACA_SECRET`, `FINNHUB_API_KEY`). Do not commit your `.env` file to version control.

4. **Explore the codebase:**

   Each subpackage under `src/` contains an `__init__.py` file and placeholder modules to get you started. Future milestones will flesh out these modules.

## License

 See the `LICENSE` file for details.
