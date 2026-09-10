# Gamification Winner Selection & Reward Allocation

A Python prototype for designing a **controlled, data-driven promotional mechanic**: segment eligible users, select winners with weighted probabilities, and allocate rewards under configurable business rules.

## Product question

How can a promotional mechanic reward users in a way that is random enough to remain engaging, but still controlled by player behavior, value, fairness constraints, and a fixed reward budget?

## What the notebook does

- Builds player-level features from behavioral and financial metrics such as GGR, Net Cash and VIP level.
- Detects and handles extreme observations before winner selection.
- Classifies users into business-defined groups.
- Uses weighted random sampling rather than purely deterministic ranking.
- Limits repeated consecutive wins.
- Calculates rewards using configurable transformations and group weights.
- Includes a separate notebook for analysis and visualization of the mechanic.

## Analytical approach

The implementation combines **segmentation, outlier handling, weighted sampling, business rules and reward scoring**.

The core logic is wrapped in a `LuckyWinner` class so that thresholds, winner counts, group weights, reward weights and probability limits can be adjusted without rewriting the full workflow.

## Tech

`Python` · `pandas` · `NumPy` · `Matplotlib` · `Seaborn`

## Repository structure

- [`LuckyWInner.ipynb`](./LuckyWInner.ipynb) — winner-selection and reward-allocation logic.
- [`LuckyWinner_Charts.ipynb`](./LuckyWinner_Charts.ipynb) — analytical review and visualization.

## Data note

The raw source dataset is **not included** in this repository.

The IDs and example player-level values shown in the notebook are **synthetic / anonymized test data** and do not represent real customer identifiers.

This repository is retained as a historical portfolio example of product analytics, segmentation, probabilistic selection and configurable reward logic.
