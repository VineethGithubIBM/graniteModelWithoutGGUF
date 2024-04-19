---
license: apache-2.0
---

**Model Name**: Granite-7b-base

**License**: Apache-2.0

**Languages**: Primarily English

**Architecture**: The model architecture is a replica of Meta’s Llama2-7B base variant with MHA, trained with 1M batch size on 2T tokens.

**Context Length**: 4k tokens

**Tokenizer**: Llama2

**Model Developers**: IBM Research

Representing IBM’s commitment to open source innovation IBM has released granite-7b-base, a base pre-trained LLM from IBM’s Granite model series, under an apache-2.0 license for community and commercial use. Granite-7b-base was pre-trained from scratch on IBM-curated data as an open reference implementation of Meta’s Llama-2-7B. In a commitment to data transparency and fostering open innovation, the data sources, sampling proportions, and URLs for access are provided below.

**Pre-Training Data**

The model was trained on 2T tokens, with sampling proportions designed to match the sampling distributions released in the Llama1 paper as closely as possible.

| Dataset | Description | Sampling Proportion | URL |
|---|---|---|---|
|Common Crawl |Open repository of web crawl data with snapshots ranging from 2021 to 2023.| 77% | https://data.commoncrawl.org/ |
|Github_Clean | Code data from CodeParrot covering a variety of coding languages. | 5.50% | https://huggingface.co/datasets/codeparrot/github-code-clean |
|Wikipedia and Wikimedia| Eight Wikimedia projects (enwiki, enwikibooks, enwikinews, enwikiquote, enwikisource, enwikiversity, enwikivoyage, enwiktionary). containing extracted plain text from pages and articles.| 2% |	https://dumps.wikimedia.org |
|USPTO |	US patents granted from 1975 to May 2023, excluding design patents.|	5%	| https://bulkdata.uspto.gov/ |
|PubMed Central|	Biomedical and life sciences papers.|	1.75%	|https://ftp.ncbi.nlm.nih.gov/pub/pmc/oa_package/|
|arXiv|	Over 1.8 million scientific paper pre-prints posted to arXiv. |	2.50%	| https://huggingface.co/datasets/togethercomputer/RedPajama-Data-1T |
|StackExchange|	Anonymized set of all user-contributed content on the Stack Exchange network, a popular collection of websites centered around user-contributed questions and answers.|	1%	| https://archive.org/details/stackexchange_20221206|
|PG19|	A repository of free e-books with focus on older works for which U.S. copyright has expired.|	0.25% |	https://github.com/google-deepmind/pg19|
|Webhose |	Unstructured web content converted into machine-readable data feeds purchased by IBM.|	5% |	N/A |

**Evaluation Results**

LM-eval Harness Scores

|Evaluation metric|	Llama2-7B (baseline) |	Granite-7b-base|
|---|---|---|
|MMLU (zero shot)| 0.41 |	0.43|
|MMLU (5-shot weighted avg)|	0.47 |	0.50|
|Arc challenge|	0.46 |	0.44|
|Arc easy|	0.74|	0.71|
|Boolq|	0.78 |	0.76 |
|Copa |	0.87 |	0.83 |
|Hellaswag|	0.76 |	0.74|
|Openbookqa|	0.44|	0.42|
|Piqa|	0.79|	0.79|
|Sciq|	0.91|	0.91|
|Winogrande|	0.69|	0.67|
|Truthfulqa|	0.39|	0.39|
|GSM8k (8-shot)|	0.13|	0.11|

**Bias, Risks, and Limitations**

Granite-7b-base is a base model and has not undergone any safety alignment, there it may produce problematic outputs. In the absence of adequate safeguards and RLHF, there exists a risk of malicious utilization of these models for generating disinformation or harmful content. Caution is urged against complete reliance on a specific language model for crucial decisions or impactful information, as preventing these models from fabricating content is not straightforward. Additionally, it remains uncertain whether smaller models might exhibit increased susceptibility to hallucination in ungrounded generation scenarios due to their reduced sizes and memorization capacities. This aspect is currently an active area of research, and we anticipate more rigorous exploration, comprehension, and mitigations in this domain.