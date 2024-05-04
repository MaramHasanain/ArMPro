# ArMPro
This repo contains the *Arabic* multimodal propaganda dataset (**ArMPro**). The dataset covers two modalities, (1) text represented by annotated news paragraphs and (2) images and text represented by memes.

## Text Subset
This dataset represents the largest one to date for fine-grained propaganda detection. It includes **8,000** paragraphs extracted from over **2,800** Arabic news articles, covering a large variety of news domains. 


Example annotated paragraph:

<img width="350" alt="Screenshot 2024-05-04 at 3 56 26 PM" src="https://github.com/MaramHasanain/ArMPro/assets/3918663/255f6b47-1942-48cb-ba0a-259a79a7f93a">

### Data splits
We split the dataset in a stratified manner, allocating 75\%, 8.5\%, and 16.5\% for training, development, and testing, respectively. During the stratified sampling, the multilabel setting was considered when splitting the dataset. This ensures that persuasion techniques are similarly distributed across the splits.

### Coarse-grained label distribuition
| Binary label       | Train | Dev | Test  |
|--------------------|-------|-----|-------|
| Propagandistic     | 3,777 | 425 | 832   |
| Non-Propagandistic | 2,225 | 247 | 494   |
| **Total**              | **6,002** | **672** | **1,326** |

| Coarse-grained label | Train | Dev | Test  |
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
| Propaganda Technique                         | Count |
|-----------------------------------|-------|
| Loaded Language                   | 10,388 |
| Name Calling /Labeling            | 2,012  |
| Exaggeration /Minimisation        | 1,290  |
| Questioning the Reputation        | 776   |
| Obfuscation /Vagueness /Confusion | 756   |
| Causal Oversimplification         | 389   |
| Doubt                             | 303   |
| Appeal to Authority               | 256   |
| Flag Waving                       | 237   |
| Repetition                        | 166   |
| Slogans                           | 144   |
| Appeal to Fear /Prejudice         | 125   |
| Consequential Oversimplification  | 110   |
| Appeal to Hypocrisy               | 108   |
| False Dilemma /No Choice          | 79    |
| Conversation Killer               | 72    |
| Appeal to Time                    | 70    |
| Appeal to Popularity              | 56    |
| Appeal to Values                  | 52    |
| Red Herring                       | 50    |
| Guilt by Association              | 29    |
| Whataboutism                      | 28    |
| Straw Man                         | 25    |
| **Total**                             | **20,487** |

## Meme Subset (*Coming Soon!*)



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
