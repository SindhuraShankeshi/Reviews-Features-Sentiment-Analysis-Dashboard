# Zoom Features vs. Reviews Sentiment Dashboard

This repository provides a traceability visualization between Zoom feature releases and user app reviews from 2022 to 2024. It helps Product Managers and data teams quickly understand the emotional impact of releases without manually reading thousands of reviews.

## Project Overview

- Problem solved: Manually reading reviews to assess the impact of a release is slow and error-prone. This dashboard automatically connects feature rollouts to shifts in user sentiment.
- Timeframe: 2022–2024 (configurable based on available data).

## Technical Highlights

- NLP Analysis: Uses a RoBERTa-based model augmented with custom polarity logic to extract sentiment from review text and emojis.
- Traceability: Maps specific versions (e.g., 5.9.6) to sentiment spikes or drops, enabling fast root-cause analysis.
- Visualization: Interactive charts highlight sentiment trends alongside release dates and feature flags.

## Stack

- Python
- Streamlit (dashboard)
- Plotly (interactive visualizations)
- Pandas (data processing)
- Hugging Face / Transformers (RoBERTa)

## Key Results

- Quick Issue Detection: Identifies sudden drops in satisfaction caused by bugs or poor UX.
- Feature Validation: Visualizes which rollouts (e.g., Language Interpretation, Gesture Recognition) resulted in the most positive feedback.

## Installation

1. Clone the repo:

   ```bash
   git clone https://github.com/SindhuraShankeshi/Reviews-Features-Sentiment-Analysis-Dashboard.git
   cd Reviews-Features-Sentiment-Analysis-Dashboard
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv .venv
   source .venv/bin/activate  # macOS / Linux
   .venv\Scripts\activate     # Windows
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Usage

- Run the Streamlit dashboard:

  ```bash
  streamlit run app.py
  ```

- Upload or point the app at your reviews dataset and releases/versions file. The dashboard will compute sentiment and show traceability visualizations.

## Data

- Typical inputs:
  - Reviews CSV/JSON with columns: review_id, text, rating, date, version
  - Releases CSV/JSON with columns: version, release_date, features
- Preprocessing steps include cleaning text, normalizing emojis, and mapping reviews to released versions by date.

## Contributing

Contributions are welcome. Please open issues for bugs or feature requests and submit PRs with clear descriptions and tests where applicable.

## License

This project is released under the MIT License. See LICENSE for details.

## Contact

Maintainer: SindhuraShankeshi
