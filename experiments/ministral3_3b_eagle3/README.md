# Ministral3 EAGLE3 Reproduction

This directory tracks the DeepSpec-side reproduction attempt for
`mistralai/Ministral-3-3B-Instruct-2512`.

The smoke scripts are intentionally tiny:

- `prepare_cache_smoke.sbatch` builds a four-sample target cache.
- `train_smoke.sbatch` trains the EAGLE3 draft for two optimizer steps against
  that cache.

They validate model loading, target hidden-state extraction, tokenizer/loss-mask
parsing, and the EAGLE3 training loop before launching a full Open-PerfectBlend
run.
