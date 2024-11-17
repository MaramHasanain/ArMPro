# ArMPro
This repo contains the *Arabic* propaganda dataset (**ArMPro**).
<!-- The dataset covers two modalities, (1) text represented by annotated news paragraphs and (2) images and text represented by memes. -->

![License](https://img.shields.io/badge/license-CC--BY--NC--SA-blue) [![Paper](https://img.shields.io/badge/Paper-Download%20PDF-green)](https://aclanthology.org/2024.lrec-main.244.pdf)

**Table of contents:**
  * [Dataset](#dataset)
    + [Data splits](#data-splits)
    + [Coarse-grained label distribuition](#coarse-grained-label-distribuition)
    + [Fine-grained label distribuition](#fine-grained-label-distribuition)
  * [Meme Subset (*Coming Soon!*)](#meme-subset-coming-soon)
  * [Licensing](#licensing)
  * [Citation](#citation)


## Dataset
This dataset represents the largest one to date for fine-grained propaganda detection. It includes **8,000** paragraphs extracted from over **2,800** Arabic news articles, covering a large variety of news domains.


Example annotated paragraph:

<img width="350" alt="Screenshot 2024-05-04 at 3 56 26 PM" src="https://github.com/MaramHasanain/ArMPro/assets/3918663/255f6b47-1942-48cb-ba0a-259a79a7f93a">

### Data splits
We split the dataset in a stratified manner, allocating 75\%, 8.5\%, and 16.5\% for training, development, and testing, respectively. During the stratified sampling, the multilabel setting was considered when splitting the dataset. This ensures that persuasion techniques are similarly distributed across the splits.

### Coarse-grained label distribuition
| **Binary label**     | **Train** | **Dev** | **Test**  |
|--------------------|-------|-----|-------|
| Propagandistic     | 3,777 | 425 | 832   |
| Non-Propagandistic | 2,225 | 247 | 494   |
| **Total**              | **6,002** | **672** | **1,326** |

| **Coarse-grained label** | **Train** | **Dev** | **Test**  |
|----------------------|-------|-----|-------|
| Manipulative Wording | 3,460 | 387 | 757   |
| no technique         | 2,225 | 247 | 494   |
| Reputation           | 1,404 | 163 | 314   |
| Justification        | 471   | 48  | 102   |
| Simplification       | 384   | 42  | 82    |
| Call                 | 176   | 21  | 40    |
| Distraction          | 74    | 9   | 16    |
| **Total**                | **8,194** | **917** | **1,805** |

### Fine-grained label distribuition

| **Technique**                        | **Train**  | **Dev**   | **Test**  |
|----------------------------------|--------|-------|-------|
| Loaded Language                  | 7,862  | 856   | 1670  |
| no technique                     | 2,225  | 247   | 494   |
| Name Calling/Labeling            | 1,526  | 158   | 328   |
| Exaggeration/Minimisation        | 967    | 113   | 210   |
| Questioning the Reputation       | 587    | 58    | 131   |
| Obfuscation/Vagueness/Confusion  | 562    | 62    | 132   |
| Causal Oversimplification        | 289    | 33    | 67    |
| Doubt                            | 227    | 27    | 49    |
| Appeal to Authority              | 192    | 22    | 42    |
| Flag Waving                      | 174    | 22    | 41    |
| Repetition                       | 123    | 13    | 30    |
| Slogans                          | 101    | 19    | 24    |
| Appeal to Fear/Prejudice         | 93     | 11    | 21    |
| Appeal to Hypocrisy              | 82     | 9     | 17    |
| Consequential Oversimplification | 81     | 10    | 19    |
| False Dilemma/No Choice          | 60     | 6     | 13    |
| Conversation Killer              | 53     | 6     | 13    |
| Appeal to Time                   | 52     | 6     | 12    |
| Appeal to Popularity             | 44     | 4     | 8     |
| Appeal to Values                 | 38     | 5     | 9     |
| Red Herring                      | 38     | 4     | 8     |
| Guilt by Association             | 22     | 2     | 5     |
| Whataboutism                     | 20     | 4     | 4     |
| Straw Man                        | 19     | 2     | 4     |
| **Total**                            | **15,437** | **1,699** | **3,351** |

**Note**: "no technique" refers to paragraphs without any propagandistic techniques use.

<!-- ## Meme Subset (*Coming Soon!*) -->



## Licensing

This dataset is licensed under CC BY-NC-SA 4.0. To view a copy of this license, visit https://creativecommons.org/licenses/by-nc-sa/4.0/

## Citation
If you use our dataset in a scientific publication, we would appreciate using the following citations:

- Maram Hasanain, Fatema Ahmad, and Firoj Alam. 2024. Can GPT-4 Identify Propaganda? Annotation and Detection of Propaganda Spans in News Articles. In Proceedings of the 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation (LREC-COLING 2024), pages 2724–2744, Torino, Italia. ELRA and ICCL.

```
@inproceedings{hasanain-etal-2024-gpt,
    title = "Can {GPT}-4 Identify Propaganda? Annotation and Detection of Propaganda Spans in News Articles",
    author = "Hasanain, Maram  and
      Ahmad, Fatema  and
      Alam, Firoj",
    editor = "Calzolari, Nicoletta  and
      Kan, Min-Yen  and
      Hoste, Veronique  and
      Lenci, Alessandro  and
      Sakti, Sakriani  and
      Xue, Nianwen",
    booktitle = "Proceedings of the 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation (LREC-COLING 2024)",
    month = may,
    year = "2024",
    address = "Torino, Italia",
    publisher = "ELRA and ICCL",
    url = "https://aclanthology.org/2024.lrec-main.244",
    pages = "2724--2744",
    abstract = "The use of propaganda has spiked on mainstream and social media, aiming to manipulate or mislead users. While efforts to automatically detect propaganda techniques in textual, visual, or multimodal content have increased, most of them primarily focus on English content. The majority of the recent initiatives targeting medium to low-resource languages produced relatively small annotated datasets, with a skewed distribution, posing challenges for the development of sophisticated propaganda detection models. To address this challenge, we carefully develop the largest propaganda dataset to date, ArPro, comprised of 8K paragraphs from newspaper articles, labeled at the text span level following a taxonomy of 23 propagandistic techniques. Furthermore, our work offers the first attempt to understand the performance of large language models (LLMs), using GPT-4, for fine-grained propaganda detection from text. Results showed that GPT-4{'}s performance degrades as the task moves from simply classifying a paragraph as propagandistic or not, to the fine-grained task of detecting propaganda techniques and their manifestation in text. Compared to models fine-tuned on the dataset for propaganda detection at different classification granularities, GPT-4 is still far behind. Finally, we evaluate GPT-4 on a dataset consisting of six other languages for span detection, and results suggest that the model struggles with the task across languages. We made the dataset publicly available for the community.",
}
```
