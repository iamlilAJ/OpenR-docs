---
title: Quick Start
parent: Getting Started
nav_order: 3
---

# Quick Start
{: .no_toc }

This following starts the language model (LM) and reward model (RM) services required for running inference. Then it prepares and runs inference using different techniques.
{: .fs-6 .fw-300 }


Start LM & RM Services

```bash
sh reason/llm_service/create_service_math_shepherd.sh
```

Run inference
```bash
export PYTHONPATH=$(pwd)
sh scripts/eval/cot_greedy.sh
sh scripts/eval/cot_rerank.sh
sh scripts/eval/beam_search.sh
```

Before training, please modify the `$dataset_path`, `$model_name_or_path` and `$prm_name_or_path` in `train/mat/scripts/train_llm.sh`.
```bash
cd train/mat/scripts
bash train_llm.sh
```