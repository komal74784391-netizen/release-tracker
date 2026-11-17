# Length-gate process

1. Pick the finished candidate run with the lowest `mean_answer_tokens`.
2. Audit the run's per-step `token_entropy`, `truncation_ratio` and `mean_answer_tokens`.
3. Evaluate the run's final logged checkpoint against `gate-policy.yaml`.
4. Record the outcome: open a gate issue and commit `results/<run>.json`.
