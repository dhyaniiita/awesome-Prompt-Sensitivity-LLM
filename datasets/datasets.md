# Datasets and Benchmarks

The course requires at least three datasets/benchmarks where applicable. The five below are relevant to controlled prompt-variation or evaluation-stability experiments.

1. **ParaRel** — Meaning-preserving paraphrase templates for factual knowledge queries; directly suited to prompt-consistency experiments. [Project](https://github.com/yanaiela/pararel)
2. **LAMA** — Factual and commonsense knowledge probing benchmark; useful for comparing answers under alternative prompt formulations. [Project](https://github.com/facebookresearch/LAMA)
3. **BIG-bench** — Large multi-task benchmark for probing language-model capabilities. The official repository is archived as of April 2026, but the benchmark remains usable as a reference resource. [Project](https://github.com/google/BIG-bench)
4. **MT-Bench** — Multi-turn evaluation set used in LLM-as-a-judge research; useful for position and judge-stability experiments. [FastChat evaluation](https://github.com/lm-sys/FastChat/tree/main/fastchat/llm_judge)
5. **MMLU** — 57-subject multiple-choice benchmark useful for controlled prompt-template comparisons. [Original implementation](https://github.com/hendrycks/test)

## Selection rationale

ParaRel is the closest direct match because it explicitly provides meaning-preserving paraphrases. LAMA and MMLU provide fixed tasks for prompt comparisons, while BIG-bench and MT-Bench support broader evaluation and judge-stability studies.
