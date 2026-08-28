# Awesome Prompt Sensitivity and LLM Conclusion Stability

A curated academic resource on **prompt sensitivity, prompt robustness, evaluation stability, and the reliability of LLM-generated research conclusions**.

This repository connects the earlier AI-assisted research paper and citation-integrity audit with verified scholarly literature, benchmarks/datasets, tools, implementations, and learning resources. It is designed as a reusable research starting point for students and researchers studying how meaning-preserving changes in prompts can alter LLM outputs, evaluations, or conclusions.

**Student:** Dhyan Shah  
**Roll Number:** MHM2026002  
**Programme / Department:** IT - HMIIT  
**Research Topic:** Prompt Sensitivity and Its Effect on the Stability of LLM-Generated Research Conclusions

## Contents

- [Overview](#overview)
- [AI-Assisted Research Paper](#ai-assisted-research-paper)
- [Citation Integrity Audit](#citation-integrity-audit)
- [Curated Research Papers](#curated-research-papers)
  - [Survey and Review](#survey-and-review)
  - [Foundational and Prompting](#foundational-and-prompting)
  - [Prompt Sensitivity and Robustness](#prompt-sensitivity-and-robustness)
  - [Evaluation, Consistency, and Bias](#evaluation-consistency-and-bias)
  - [Recent Research](#recent-research)
- [Datasets and Benchmarks](#datasets-and-benchmarks)
- [Tools and Libraries](#tools-and-libraries)
- [GitHub Implementations](#github-implementations)
- [Tutorials and Learning Resources](#tutorials-and-learning-resources)
- [Verification and Research Practice](#verification-and-research-practice)
- [License](#license)

## Overview

Prompt sensitivity is the tendency of a language model to change its behavior when the wording, formatting, ordering, framing, or other surface properties of a prompt change even when the intended task remains meaning-equivalent. This is important in research because an LLM may be used to summarize literature, compare methods, judge evidence, classify observations, extract claims, or draft conclusions. In those settings, a change in the generated wording is not necessarily important, but a change in the underlying research claim can be.

The central distinction is therefore **output stability versus conclusion stability**. Two answers may be linguistically different while supporting the same conclusion, while a small change in wording can introduce a different qualifier, direction of effect, or recommendation. Research on formatting, demonstration order, paraphrasing, evaluation position, decoding, and multi-prompt evaluation shows that prompt and evaluation choices can materially affect measured behavior. Recent work also questions how much observed prompt sensitivity is caused by models themselves versus the evaluation procedures used to score them.

For research practice, a defensible workflow should not treat one fluent answer as a stable observation. A stronger protocol is to use several meaning-preserving prompt variants, repeat at least one prompt as a control, define how conclusions will be extracted before looking at results, record the model/version and generation settings, and report agreement or disagreement across variants. This repository collects the literature and practical tools needed to apply that mindset.

## AI-Assisted Research Paper

### Prompt Sensitivity and Its Effect on the Stability of LLM-Generated Research Conclusions

The paper is the earlier AI-assisted research output used as the foundation for this repository. It discusses prompt sensitivity as a methodological issue for LLM-assisted research and proposes a conclusion-stability perspective.

- [Read the paper (PDF)](paper/AI_Assisted_Research_Paper.pdf)
- [Source document (DOCX)](paper/AI_Assisted_Research_Paper.docx)

## Citation Integrity Audit

The earlier lab included a systematic audit of a sample of the paper's references and claim-citation support. The reported audit selected 10 references from a 28-reference bibliography and recorded **10/10 authentic references** in the sample. The claim-support review recorded **9 fully supported claims, 1 partially supported claim, and 0 unsupported claims**, producing the reported 95/100 claim-support score.

The audit itself also states an important limitation: a perfect sampled-reference authenticity score does **not** prove that every reference or every generated claim in the full paper is reliable. The audit therefore should be treated as evidence about the sampled checks, not as a guarantee about the complete bibliography.

- [Read the citation-integrity audit](citation-audit/Citation_Integrity_Audit.pdf)

## Curated Research Papers

The collection below exceeds the required minimum of 20 scholarly papers. Each record includes the title, authors, year, venue, a scholarly link, and a one-line relevance note.

### Survey and Review

1. **Pre-train, Prompt, and Predict: A Systematic Survey of Prompting Methods in Natural Language Processing**  
   Pengfei Liu, Weizhe Yuan, Jinlan Fu, Zhengbao Jiang, Hiroaki Hayashi, Graham Neubig — 2023, *ACM Computing Surveys*.  
   [DOI / publisher](https://doi.org/10.1145/3560815)  
   A foundational survey that organizes prompt-based learning and provides terminology for prompt design research.

2. **A Systematic Survey of Prompt Engineering in Large Language Models: Techniques and Applications**  
   Pranab Sahoo, Ayush Kumar Singh, Sriparna Saha, Vinija Jain, Samrat Mondal, Aman Chadha — 2024, *arXiv*.  
   [arXiv](https://arxiv.org/abs/2402.07927)  
   Provides a structured taxonomy of prompt-engineering techniques, applications, models, and datasets.

3. **Survey of Hallucination in Natural Language Generation**  
   Ziwei Ji, Nayeon Lee, Rita Frieske, Tiezheng Yu, Dan Su, Yan Xu, Etsuko Ishii, Ye Jin Bang, Andrea Madotto, Pascale Fung — 2023, *ACM Computing Surveys*.  
   [DOI / publisher](https://doi.org/10.1145/3571730)  
   Relevant to factual reliability and the verification burden created by fluent generated text.

4. **Holistic Evaluation of Language Models**  
   Rishi Bommasani, Percy Liang, Tony Lee, et al. — 2023, *Annals of the New York Academy of Sciences*.  
   [DOI / publisher](https://doi.org/10.1111/nyas.15007)  
   Provides a broad evaluation framework emphasizing standardized scenarios, metrics, transparency, and comparability.

### Foundational and Prompting

5. **Language Models are Few-Shot Learners**  
   Tom B. Brown, Benjamin Mann, Nick Ryder, et al. — 2020, *NeurIPS 2020*.  
   [NeurIPS](https://proceedings.neurips.cc/paper_files/paper/2020/hash/1457c0d6bfcb4967418bfb8ac142f64a-Abstract.html)  
   Foundational demonstration of few-shot task specification through natural-language prompts.

6. **Prompt Programming for Large Language Models: Beyond the Few-Shot Paradigm**  
   Laria Reynolds, Kyle McDonell — 2021, *CHI Extended Abstracts*.  
   [DOI](https://doi.org/10.1145/3411763.3451760)  
   Frames prompt programming as an interaction paradigm and helps establish the methodological context for prompt design.

7. **Chain-of-Thought Prompting Elicits Reasoning in Large Language Models**  
   Jason Wei, Xuezhi Wang, Dale Schuurmans, Maarten Bosma, Brian Ichter, Fei Xia, Ed Chi, Quoc Le, Denny Zhou — 2022, *NeurIPS 2022*.  
   [arXiv](https://arxiv.org/abs/2201.11903)  
   Shows how explicit reasoning-oriented prompting can substantially change performance on reasoning tasks.

8. **Large Language Models are Zero-Shot Reasoners**  
   Takeshi Kojima, Shixiang Shane Gu, Machel Reid, Yutaka Matsuo, Yusuke Iwasawa — 2022, *NeurIPS 2022*.  
   [arXiv](https://arxiv.org/abs/2205.11916)  
   Demonstrates that a simple instruction can alter reasoning behavior without demonstrations.

9. **Self-Consistency Improves Chain of Thought Reasoning in Language Models**  
   Xuezhi Wang, Jason Wei, Dale Schuurmans, Quoc V. Le, Ed H. Chi, Sharan Narang, Aakanksha Chowdhery, Denny Zhou — 2023, *ICLR 2023*.  
   [Google Research](https://research.google/pubs/self-consistency-improves-chain-of-thought-reasoning-in-language-models/)  
   Shows how sampling multiple reasoning paths and aggregating them can reduce dependence on one sampled reasoning trajectory.

10. **Large Language Models Are Human-Level Prompt Engineers**  
    Yongchao Zhou, Andrei Ioan Muresanu, Ziwen Han, Keiran Paster, Silviu Pitis, Harris Chan, Jimmy Ba — 2023, *ICLR 2023*.  
    [ML Anthology](https://mlanthology.org/iclr/2023/zhou2023iclr-large/)  
    Introduces Automatic Prompt Engineer and shows that automatically generated instructions can materially affect task performance.

11. **Calibrate Before Use: Improving Few-shot Performance of Language Models**  
    Zihao Zhao, Eric Wallace, Shi Feng, Dan Klein, Sameer Singh — 2021, *ICML 2021*.  
    [PMLR](https://proceedings.mlr.press/v139/zhao21c.html)  
    Directly studies instability caused by prompt format, examples, and example order and proposes contextual calibration.

12. **Rethinking the Role of Demonstrations: What Makes In-Context Learning Work?**  
    Sewon Min, Xinxi Lyu, Ari Holtzman, Mikel Artetxe, Mike Lewis, Hannaneh Hajishirzi, Luke Zettlemoyer — 2022, *EMNLP 2022*.  
    [ACL Anthology](https://aclanthology.org/2022.emnlp-main.759/)  
    Shows that demonstration format and input distribution can matter even when the demonstration labels themselves are altered.

### Prompt Sensitivity and Robustness

13. **Do Prompt-Based Models Really Understand the Meaning of Their Prompts?**  
    Albert Webson, Ellie Pavlick — 2022, *NAACL 2022*.  
    [ACL Anthology](https://aclanthology.org/2022.naacl-main.167/)  
    Tests many alternative prompts and finds that models can perform well even with irrelevant or misleading instructions.

14. **Fantastically Ordered Prompts and Where to Find Them: Overcoming Few-Shot Prompt Order Sensitivity**  
    Yao Lu, Max Bartolo, Alastair Moore, Sebastian Riedel, Pontus Stenetorp — 2022, *ACL 2022*.  
    [ACL Anthology](https://aclanthology.org/2022.acl-long.556/)  
    Demonstrates that the order of few-shot examples can move performance from near state-of-the-art to near-random levels.

15. **Measuring and Improving Consistency in Pretrained Language Models**  
    Yanai Elazar, Nora Kassner, Shauli Ravfogel, Abhilasha Ravichander, Eduard Hovy, Hinrich Schütze, Yoav Goldberg — 2021, *TACL*.  
    [ACL Anthology](https://aclanthology.org/2021.tacl-1.60/)  
    Introduces ParaRel and studies invariance under meaning-preserving paraphrases.

16. **Quantifying Language Models' Sensitivity to Spurious Features in Prompt Design or: How I Learned to Start Worrying About Prompt Formatting**  
    Melanie Sclar, Yejin Choi, Yulia Tsvetkov, Alane Suhr — 2024, *ICLR 2024*.  
    [ML Anthology](https://mlanthology.org/iclr/2024/sclar2024iclr-quantifying/)  
    Direct evidence that subtle formatting choices can cause very large performance changes.

17. **The Butterfly Effect of Altering Prompts: How Small Changes and Jailbreaks Affect Large Language Model Performance**  
    Abel Salinas, Fred Morstatter — 2024, *Findings of ACL 2024*.  
    [ACL Anthology](https://aclanthology.org/2024.findings-acl.275/)  
    Finds that even very small prompt perturbations can change model decisions.

18. **State of What Art? A Call for Multi-Prompt LLM Evaluation**  
    Moran Mizrahi, Guy Kaplan, Dan Malkin, Rotem Dror, Dafna Shahaf, Gabriel Stanovsky — 2024, *TACL*.  
    [ACL Anthology](https://aclanthology.org/2024.tacl-1.52/)  
    Shows that single-template benchmarks can be brittle and motivates evaluation across multiple instruction paraphrases.

### Evaluation, Consistency, and Bias

19. **Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena**  
    Lianmin Zheng, Wei-Lin Chiang, Ying Sheng, Siyuan Zhuang, Zhanghao Wu, Yonghao Zhuang, Zi Lin, Zhuohan Li, Dacheng Li, Eric P. Xing, Hao Zhang, Joseph E. Gonzalez, Ion Stoica — 2023, *NeurIPS 2023*.  
    [arXiv](https://arxiv.org/abs/2306.05685)  
    Examines LLM-as-a-judge limitations including position, verbosity, and self-enhancement biases.

20. **Large Language Models are not Fair Evaluators**  
    Peiyi Wang, Lei Li, Liang Chen, Zefan Cai, Dawei Zhu, Binghuai Lin, Yunbo Cao, Lingpeng Kong, Qi Liu, Tianyu Liu, Zhifang Sui — 2024, *ACL 2024*.  
    [ACL Anthology](https://aclanthology.org/2024.acl-long.511/)  
    Demonstrates positional bias in LLM-based evaluation and shows that changing response order can alter rankings.

21. **What Did I Do Wrong? Quantifying LLMs' Sensitivity and Consistency to Prompt Engineering**  
    Federico Errica, Davide Sanvito, Giuseppe Siracusano, Roberto Bifulco — 2025, *NAACL 2025*.  
    [ACL Anthology](https://aclanthology.org/2025.naacl-long.73/)  
    Introduces sensitivity and consistency metrics for studying changes across prompt rephrasings.

22. **The Effect of Sampling Temperature on Problem Solving in Large Language Models**  
    Matthew Renze — 2024, *Findings of EMNLP 2024*.  
    [ACL Anthology](https://aclanthology.org/2024.findings-emnlp.432/)  
    Studies how decoding temperature interacts with LLM problem-solving and prompt-engineering settings.

### Recent Research

23. **Flaw or Artifact? Rethinking Prompt Sensitivity in Evaluating LLMs**  
    Andong Hua, Kenan Tang, Chenhe Gu, Jindong Gu, Eric Wong, Yao Qin — 2025, *EMNLP 2025*.  
    [ACL Anthology](https://aclanthology.org/2025.emnlp-main.1006/)  
    Re-examines whether reported prompt sensitivity is partly produced by heuristic evaluation procedures.

24. **Understanding the Prompt Sensitivity**  
    Yang Liu, Chenhui Chu — 2026, *ACL 2026*.  
    [ACL Anthology](https://aclanthology.org/2026.acl-long.2053/)  
    Provides a recent theoretical analysis of why meaning-preserving prompt variants can produce divergent model behavior.

25. **Language Models Don't Always Say What They Think: Unfaithful Explanations in Chain-of-Thought Prompting**  
    Mikhail Turpin, Julian Michael, Ethan Perez, Samuel R. Bowman — 2023, *NeurIPS 2023*.  
    [arXiv](https://arxiv.org/abs/2305.04388)  
    Important for conclusion reliability because a fluent reasoning explanation is not necessarily evidence that the stated reasoning caused the answer.

26. **Non-determinism of 'Deterministic' LLM Settings**  
    B. Atil, S. Aykent, A. Chittams, L. Fu, R. J. Passonneau, E. Radcliffe, G. R. Rajagopal, A. Sloan, T. Tudrej, F. Ture, Z. Wu, L. Xu, B. Baldwin — 2024, *arXiv*.  
    [arXiv](https://arxiv.org/abs/2408.04667)  
    Relevant because non-deterministic behavior can confound attempts to attribute output differences solely to prompt changes.

## Datasets and Benchmarks

The assignment asks for at least three datasets/benchmarks where applicable. These are applicable because controlled prompt variants require fixed tasks or benchmark instances against which outputs can be compared.

1. **ParaRel** — A collection of meaning-preserving paraphrase templates for factual knowledge queries; directly useful for prompt-consistency experiments.  
   [Project repository](https://github.com/yanaiela/pararel)

2. **LAMA (Language Model Analysis)** — A factual and commonsense knowledge probing benchmark; useful for testing whether alternative prompt formulations retrieve the same knowledge.  
   [Project repository](https://github.com/facebookresearch/LAMA)

3. **BIG-bench** — A large collaborative benchmark containing hundreds of diverse tasks; useful for evaluating prompt variants across multiple task types. The repository is archived as of April 2026 but remains a useful benchmark resource.  
   [Project repository](https://github.com/google/BIG-bench)

4. **MT-Bench** — A multi-turn question set used with LLM-as-a-judge evaluation; useful for studying judge variability and positional effects.  
   [FastChat evaluation implementation](https://github.com/lm-sys/FastChat/tree/main/fastchat/llm_judge)

5. **MMLU** — A 57-subject multiple-choice benchmark; useful for controlled comparisons of prompt templates and evaluation implementations.  
   [Original implementation](https://github.com/hendrycks/test)

## Tools and Libraries

1. **LM Evaluation Harness** — A unified framework for running standardized and custom LLM evaluations with explicit prompts and metrics.  
   [GitHub](https://github.com/EleutherAI/lm-evaluation-harness)

2. **HELM** — Stanford CRFM's framework for holistic, reproducible, transparent evaluation of language and multimodal models.  
   [GitHub](https://github.com/stanford-crfm/helm)

3. **PromptSource** — A toolkit for creating, sharing, and applying natural-language prompt templates.  
   [GitHub](https://github.com/bigscience-workshop/promptsource)

4. **promptfoo** — A testing and evaluation toolkit for comparing prompts/models and running systematic LLM evaluations.  
   [GitHub](https://github.com/promptfoo/promptfoo)

5. **OpenAI Evals** — A framework and registry for constructing and running LLM evaluations.  
   [GitHub](https://github.com/openai/evals)

6. **LangSmith Evaluation** — Dataset-based experiment comparison and evaluation workflows for LLM applications.  
   [Documentation](https://docs.langchain.com/langsmith/evaluation-quickstart)

## GitHub Implementations

The assignment asks for at least five existing implementations. These were selected because they have a direct connection to prompt sensitivity, consistency, evaluation bias, or reproducible LLM evaluation.

1. **Ordered-Prompt** — Code for the ACL 2022 study of few-shot prompt-order sensitivity.  
   [GitHub](https://github.com/yaolu/ordered-prompt)

2. **ParaRel** — Code and data for measuring and improving consistency under paraphrased prompts.  
   [GitHub](https://github.com/yanaiela/pararel)

3. **LPAQA** — Prompt/query resources associated with prompt-based factual knowledge extraction and LAMA-style evaluation.  
   [GitHub](https://github.com/jzbjyb/LPAQA)

4. **FairEval** — Implementation associated with studying positional bias in LLM evaluation.  
   [GitHub](https://github.com/i-Eval/FairEval)

5. **FastChat** — Open platform containing MT-Bench and LLM-as-a-judge evaluation workflows.  
   [GitHub](https://github.com/lm-sys/FastChat)

6. **LM Evaluation Harness** — General-purpose reproducible benchmark and prompt evaluation framework.  
   [GitHub](https://github.com/EleutherAI/lm-evaluation-harness)

7. **HELM** — Holistic, transparent evaluation infrastructure from Stanford CRFM.  
   [GitHub](https://github.com/stanford-crfm/helm)

## Tutorials and Learning Resources

1. **ACL Anthology** — Authoritative portal for computational-linguistics papers, metadata, and proceedings.  
   [ACL Anthology](https://aclanthology.org/)

2. **LM Evaluation Harness documentation** — Installation, task definitions, custom prompts, model backends, and evaluation workflows.  
   [GitHub documentation](https://github.com/EleutherAI/lm-evaluation-harness)

3. **HELM documentation** — Practical material for reproducible, multi-dimensional LLM evaluation.  
   [GitHub](https://github.com/stanford-crfm/helm)

4. **PromptSource documentation** — Prompt templating, prompt collections, and prompt experimentation workflows.  
   [GitHub](https://github.com/bigscience-workshop/promptsource)

5. **OpenAI Evals: Building an eval** — Step-by-step guidance for creating datasets, registering evaluations, and running evals.  
   [Guide](https://github.com/openai/evals/blob/main/docs/build-eval.md)

6. **LangSmith Evaluation Quickstart** — Practical guide to datasets, evaluators, experiments, and result comparison.  
   [Guide](https://docs.langchain.com/langsmith/evaluation-quickstart)

7. **promptfoo documentation** — Practical LLM testing, evaluation, and red-teaming workflows.  
   [Documentation](https://www.promptfoo.dev/docs/)

## Verification and Research Practice

### Verification policy

The course instruction sheet requires the student to verify each scholarly resource's title, authors, year, venue, DOI/link, existence, and link-to-paper correspondence. AI may assist with discovery, but the student is responsible for final verification.

This repository was prepared using authoritative publisher, ACL Anthology, PMLR, NeurIPS, arXiv, and official project/GitHub records where available. **Before submission, Dhyan should click through the paper/resource links and tick the final verification checklist.**

### Recommended conclusion-stability protocol

For an LLM-assisted research claim:

1. Write the research question and expected claim-extraction rule before generation.
2. Create around five meaning-preserving prompt variants.
3. Run every variant at least once.
4. Repeat one prompt several additional times as a same-prompt control.
5. Record model/version, date, temperature or other decoding settings, retrieval/browsing state, and the exact prompt text.
6. Extract the conclusion from each response using the same predefined rule.
7. Report the agreement rate and list materially different conclusions.
8. Investigate whether differences are caused by prompt wording, sampling/non-determinism, evaluation method, or model-version changes.

This protocol is consistent with the research gaps identified in the earlier paper: a same-prompt repetition control is needed to separate prompt variance from other variance, and long-form conclusion stability requires explicit claim extraction.

## Copyright and Ethical Use

Only the student's own paper and citation-audit document are included as PDFs. Third-party research papers are linked rather than redistributed. This follows the course rule not to upload copyrighted papers without permission.

## License

The repository's original documentation and curation text are released under the MIT License. Third-party papers, datasets, software, and websites remain under their respective licenses and copyrights.

See [LICENSE](LICENSE).
