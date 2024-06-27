# mmlu_redux

### Paper

Title: `Are We Done with MMLU?`

Abstract: `Maybe not. We identify and analyse errors in the popular Massive Multitask Language Understanding (MMLU) benchmark. Even though MMLU is widely adopted, our analysis demonstrates numerous ground truth errors that obscure the true capabilities of LLMs. For example, we find that 57% of the analysed questions in the Virology subset contain errors. To address this issue, we introduce a comprehensive framework for identifying dataset errors using a novel error taxonomy. Then, we create MMLU-Redux, which is a subset of 3,000 manually re-annotated questions across 30 MMLU subjects. Using MMLU-Redux, we demonstrate significant discrepancies with the model performance metrics that were originally reported. Our results strongly advocate for revising MMLU's error-ridden questions to enhance its future utility and reliability as a benchmark. Therefore, we open up MMLU-Redux for additional annotation https://huggingface.co/datasets/edinburgh-dawg/mmlu-redux.`

### Citation

```bibtex
@misc{gema2024mmlu,
      title={Are We Done with MMLU?}, 
      author={Aryo Pradipta Gema and Joshua Ong Jun Leang and Giwon Hong and Alessio Devoto and Alberto Carlo Maria Mancino and Rohit Saxena and Xuanli He and Yu Zhao and Xiaotang Du and Mohammad Reza Ghasemi Madani and Claire Barale and Robert McHardy and Joshua Harris and Jean Kaddour and Emile van Krieken and Pasquale Minervini},
      year={2024},
      eprint={2406.04127},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```

### Groups and Tasks

#### Groups

* `mmlu_pro`: 'All 14 subjects of the mmlu_pro dataset, evaluated following the methodology in mmlu's original implementation'
* `mmlu_pro_flan_cot_fewshot`: 'mmlu_pro_flan_cot_fewshot includes 5-shot of exemplars for chain-of-thought approach'
* `mmlu_pro_flan_cot_zeroshot`: 'mmlu_pro_flan_cot_zeroshot evaluates using zero-shot chain-of-thought approach'
* `mmlu_pro_generative`:  'mmlu_pro_generative solves questions of mmlu_pro using direct (generative) approach'
* `mmlu_pro_continuation`: 'mmlu_pro_continuation evaluates the ability to continue and complete a given text'

#### Tasks

The following tasks evaluate subjects in the mmlu_redux dataset
- `mmlu_redux_{subject_english}`
- `mmlu_redux_flan_cot_fewshot_{subject_english}`
- `mmlu_redux_flan_cot_zeroshot_{subject_english}`
- `mmlu_redux_generative_{subject_english}`
- `mmlu_redux_continuation_{subject_english}`

### Checklist

For adding novel benchmarks/datasets to the library:
* [x] Is the task an existing benchmark in the literature?
  * [x] Have you referenced the original paper that introduced the task?
  * [x] If yes, does the original paper provide a reference implementation? If so, have you checked against the reference implementation and documented how to run such a test?


If other tasks on this dataset are already supported:
* [ ] Is the "Main" variant of this task clearly denoted?
* [ ] Have you provided a short sentence in a README on what each new variant adds / evaluates?
* [ ] Have you noted which, if any, published evaluation setups are matched by this variant?