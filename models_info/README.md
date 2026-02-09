This folder documents the models, configurations, and design decisions used in the project.

The forecasting core is built on TIME-LLM (TinyLlama backbone) fine-tuned using LoRA to enable efficient domain adaptation for time-series reasoning in energy forecasting.

Model details:

Base Model:
- TinyLlama (via TIME-LLM architecture)

Fine-tuning Strategy:
- LoRA (Low-Rank Adaptation)
- Rank (r): 32
- Alpha (α): 64

Prompting Strategy:
- Dynamic prompts informed by detected seasonality and trend indicators
- Context-aware prompts for irregular and weak seasonal patterns

Baselines for Comparison:
- ARIMA
- ETS (Exponential Smoothing)
- DLinear (Deep Learning baseline)

Why this matters:
This project treats LLMs as reasoning agents within a forecasting pipeline rather than pure numerical predictors. The documentation here clarifies how the models were configured, why certain choices were made, and how they contribute to interpretability and decision support.

This ensures the project is reproducible and understandable for researchers and engineers reviewing the work.
