## GeoGPT-QA Dataset: A Large-scale Geoscience QA Dataset for Supervised Fine-tuning of LLMs

### 1. Dataset Description

We introduce **GeoGPT-QA Dataset**, a large-scale synthetic question–answer (QA) corpus developed to support supervised fine-tuning (SFT) of geoscience foundation models.

The dataset is derived from open-access geoscience publications distributed under the CC BY license. Using an automated data synthesis pipeline, we generated professional QA pairs from article titles and abstracts with [Qwen2.5-72B-Instruct](https://huggingface.co/Qwen/Qwen2.5-72B-Instruct). In total, the dataset comprises 40,000 QA instances, covering a wide spectrum of subfields within Earth sciences. To download the dataset, please visit: https://huggingface.co/datasets/GeoGPT-Research-Project/GeoGPT-QA

Each entry in the GeoGPT-QA Dataset is structured with the following information:

- `index`: unique identifier of the QA item

- `question`: automatically generated geoscience-related question

- `answer`: corresponding synthesized reference answer

- `title`: title of the source publication

- `authors`: list of publication authors

- `doi`: digital object identifier of the source publication

- `journal`: name of the publishing journal

- `volume`: volume number of the source publication

- `pages`: page range of the source publication

- `license`: usage license of the source publication (all is under CC BY)

By leveraging high-quality open-access literature and automated synthesis pipelines, the GeoGPT-QA Dataset provides a scalable, domain-relevant and reliable resource for advancing the development of large language models tailored to geoscience.

### 2. How to download

The dataset is hosted on the [Hugging Face Hub](https://huggingface.co/datasets/GeoGPT-Research-Project/GeoGPT-QA) as an CSV file (`.csv`).


#### Using `wget` or `curl`
```
wget https://huggingface.co/datasets/GeoGPT-Research-Project/GeoGPT-QA/resolve/main/geogpt-qa.csv
```
```
curl -L -o geogpt-qa.csv https://huggingface.co/datasets/GeoGPT-Research-Project/GeoGPT-QA/resolve/main/geogpt-qa.csv
```



#### Using 🤗`datasets` library

```python
from datasets import load_dataset

data = load_dataset("GeoGPT-Research-Project/geogpt-qa")
```

### 3. License and Intended Uses

**License**：The dataset is released under the Creative Commons Attribution 4.0 International (CC BY 4.0) license. You may share and adapt with attribution, link to the license, and indicate changes. Please note that the dataset was built using [Qwen2.5-72B-Instruct](https://huggingface.co/Qwen/Qwen2.5-72B-Instruct), which is licensed under the [Qwen LICENSE AGREEMENT](https://huggingface.co/Qwen/Qwen2.5-72B-Instruct/blob/main/LICENSE). Your use of [Qwen2.5-72B-Instruct](https://huggingface.co/Qwen/Qwen2.5-72B-Instruct) must comply with its own license terms.

**Copyright**: Copyright (c) 2025 Zhejiang Lab. All rights reserved.

**Intended Use**：The dataset is intended for research, development, and educational purposes, with primary applications in supporting supervised fine-tuning of geoscience foundation models and facilitating reproducible research in the geosciences. However, due to its synthetic nature, it may not comprehensively cover all subfields and could contain errors. Therefore, it is not recommended for direct use in high-risk scenarios such as decision-making or policy formulation.


## 4. Contact
For questions, feedback, or contributions, please open an issue in this repository or contact us at 📧 [support.geogpt@zhejianglab.org](support.geogpt@zhejianglab.org).