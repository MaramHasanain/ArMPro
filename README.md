# ArMPro
This repo contains the *Arabic* multimodal propaganda dataset (**ArMPro**). The dataset covers two modalities, (1) text represented by annotated news paragraphs and (2) images and text represented by memes.

**Table of contents:**
  * [Text Subset](#text-subset)
    + [Data splits](#data-splits)
    + [Coarse-grained label distribuition](#coarse-grained-label-distribuition)
    + [Fine-grained label distribuition](#fine-grained-label-distribuition)
  * [Meme Subset (*Coming Soon!*)](#meme-subset-coming-soon)
  * [Licensing](#licensing)
  * [Citation](#citation)


## Text Subset
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

## Meme Subset (*Coming Soon!*)



## Licensing

This dataset is licensed under CC BY-NC-SA 4.0. To view a copy of this license, visit https://creativecommons.org/licenses/by-nc-sa/4.0/

## Citation
If you use our dataset in a scientific publication, we would appreciate using the following citations:

```
@article{hasanain2024can,
  title={Can GPT-4 Identify Propaganda? Annotation and Detection of Propaganda Spans in News Articles},
  author={Hasanain, Maram and Ahmed, Fatema and Alam, Firoj},
  journal={arXiv preprint arXiv:2402.17478},
  year={2024}
}
```
