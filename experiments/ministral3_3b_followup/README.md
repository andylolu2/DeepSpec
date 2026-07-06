# Ministral3 Follow-Up Experiments

These launchers compare:

- Eagle3 soft-CE/KL baseline from `experiments/ministral3_3b_eagle3`.
- Eagle3 with the end-to-end multi-step TV loss.
- DSpark with a Ministral3-3B target.

All generated heavy artifacts are directed under `/mnt/vast/runs/andy`.

Smoke jobs:

```bash
sbatch experiments/ministral3_3b_followup/train_eagle3_e2e_tv_smoke.sbatch
sbatch experiments/ministral3_3b_followup/train_dspark_smoke.sbatch
```

Full 3000-step jobs:

```bash
sbatch experiments/ministral3_3b_followup/train_eagle3_e2e_tv_3000steps_16gpu.sbatch
sbatch experiments/ministral3_3b_followup/train_dspark_3000steps_16gpu.sbatch
```

Single-node fallback jobs:

```bash
sbatch experiments/ministral3_3b_followup/train_eagle3_e2e_tv_3000steps_8gpu.sbatch
sbatch experiments/ministral3_3b_followup/train_dspark_3000steps_8gpu.sbatch
```

Eval jobs:

```bash
sbatch experiments/ministral3_3b_followup/eval_eagle3_e2e_tv_3000steps.sbatch
sbatch experiments/ministral3_3b_followup/eval_dspark_3000steps.sbatch
sbatch experiments/ministral3_3b_followup/eval_eagle3_e2e_tv_8gpu_3000steps.sbatch
sbatch experiments/ministral3_3b_followup/eval_dspark_8gpu_3000steps.sbatch
```
