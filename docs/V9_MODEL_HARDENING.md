# V9 Model Hardening

This branch documents the V9 upgrade path for the network threat intelligence project.

## Implemented in the local V9 package
- Analyst risk scoring and risk bands
- Runtime feature-schema validation
- Systematic Destination Port / TCP-window ablation
- Reproducible analysis notebook
- Model card and promotion gates
- Genuine multiclass training pipeline, gated until labeled attack-family data is supplied

## Evidence policy
The bundled artifact remains BENIGN vs DDoS. Internal benchmark metrics must not be presented as production or cross-dataset performance. Multiclass metrics are not reported until a real labeled multiclass training/evaluation run completes.

## Promotion gates
1. Train/validation/final-test separation
2. External/unseen traffic evaluation
3. Shortcut-feature ablation
4. Per-class metrics and macro-F1 for multiclass
5. OOD + schema mismatch tests
6. Shadow deployment and analyst feedback
