# Greybox @ SemEval2024 Task 4: Progressive Fine-tuning (for Multilingual Detection of Propaganda Techniques) 

**Task Page:** https://propaganda.math.unipd.it/semeval2024task4/index.html

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Nathan-Roll1/GreyBox/blob/main/Submission_GreyBox_SemEval_2024_Task_4.ipynb) 
[![arXiv](https://img.shields.io/badge/arXiv-TBA-orange.svg)](https://arxiv.org/abs/2406.xxxxx) 

**Authors:**

* Nathan Roll (nroll@ucsb.edu)
* Calbert Graham (crg29@cam.ac.uk) 

**Performance**
| Language     | Rank | Fh    | Prh    | ReCh   |
|--------------|------|-------|--------|--------|
| English      | 5/32 | 0.670 | 0.652  | 0.688  |
| Bulgarian    | 7/19 | 0.476 | 0.438  | 0.521  |
| N. Macedonian | 8/19 | 0.434 | 0.440  | 0.430  |

**Illustrative Code Snippet**

```python
import openai 

# Example of progressive fine-tuning (replace with your actual models & datasets)
base_model = "text-davinci-003"
technique_datasets = ["loaded_appeal_to_fear_data", ...] 
main_dataset = "multi_lingual_propaganda_corpus"

for dataset in technique_datasets:
    openai.FineTune.create(training_file=dataset, model=base_model)

openai.FineTune.create(training_file=main_dataset, model=base_model)
```

**The following information is *not* final:**

```bibtex
@inproceedings{GreyBoxSemeval2024task4, 
	title={GreyBox at SemEval-2024 Task 4: Progressive Fine-tuning (for Multilingual Detection of Propaganda Techniques)},
	author={Roll, Nathan and Graham, Calbert},
	booktitle = {Proceedings of the 18th International Workshop on Semantic Evaluation},
	series = {SemEval 2024},
	year = {2024},
	address = {Mexico City, Mexico},
	month = {June},
	pages = {},   
	doi= {}   
