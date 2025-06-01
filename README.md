# ReflectiveLoopBreaker v1.6

ReflectiveLoopBreaker is a prototype AI safety scaffold focused on recursive loop detection, abstract signal monitoring, and internal instability checks. It is designed as a neutral seedbed without moral or ideological assumptions.

## Core State Variables

### Signal Consistency
Measures how stable and coherent recent outputs are.  
→ **High = coherence and internal alignment**  
→ **Low = randomness or semantic drift**  
**Suggested metric:** average entropy, token probability variance, or embedding similarity over last N outputs.

### Behavior Tension Pressure
Measures internal contradiction or instability between outputs or goals.  
→ **High = conflict, reversal, or unstable reasoning**  
→ **Low = consistent belief/action flow**  
**Suggested metric:** semantic divergence across output embeddings, contradiction classifiers, or contradiction distance.

### Friction Score Accumulation
Measures conceptual strain building up across outputs.  
→ **High = recursive buildup, forced compression, or logic overload**  
→ **Low = narrative clarity or low recursion**  
**Suggested metric:** ratio of compressed to raw text length, edit distance correction score, or zlib compression ratios.

## Safeguard Logic
- System halts when any threshold (defined in config.yaml) is crossed.
- Optional `verbose` mode can display signal values for debugging.
- Thresholds can be randomized slightly (jitter) to prevent probing attacks.

## Files
- `reflective_loopbreaker.py`: Core logic and loop.
- `config.example.yaml`: Example configuration file.
- `LICENSE`: RAIL license (intended).
- `requirements.txt`: Optional, contains `PyYAML`
- `.gitignore`: Standard exclusions
- `tests/test_sanity.py`: Basic smoke test to ensure loop runs once.

## Contribution Guidelines
ReflectiveLoopBreaker uses abstract, neutral variables (no moral or political hardcoding). Contributions should follow this ethos:
- Implement `compute_signal_consistency`, `compute_behavior_tension`, and `compute_friction_score` using flexible metrics.
- All core logic should remain modular and easily auditable.
- Ideological or moral classifiers must be contained in plugins, not core logic.

## License
Intended for release under the RAIL license. See LICENSE file.

## Contact
This repository is a prototype release for researchers interested in alignment, adversarial probing defense, and recursive system safety. Fork freely.

Created by **Jade P. / astrangeattractor@protonmail.com 
License: RAIL v1.3 — See LICENSE file for terms.
