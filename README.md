# mental-burnout-disambiguation

Dataset of 2,330 Reddit posts labeled for discussion of mental burnout and context of burnout. You can read more about the dataset in our paper. 

Link to paper: https://aclanthology.org/2024.nlp4pi-1.21

## Annotation Description

### Task 1: Burnout Disambiguation 

* `burnout = 1`: Use of one of the burnout keywords in a manner related to mental health. The described experience is in the past or present. Hypothetical scenarios are not considered.
* `burnout = 0`: Burnout keyword is used in contexts unrelated to mental health (i.e. without reference to psychological burnout), for example mechanical failure.


### Task 2: Context of Burnout 

Context is only labeled for posts with `burnout = 1` otherwise the value is set to `None`. 

* `context = professional`: Mention of burnout occurring in the context of paid work or education. 
* `context = personal`: Mention of burnout in life outside of work, such as hobbies, relationships, and belief.
* `context = non-traditional`: Mention of burnout occurring in the context of work not traditionally recognized by society. This includes unpaid work such as homemaker, and parenting, or paid work such as sex work.

## Reading the data

```python
import pandas as pd

df = pd.read_csv('dataset.csv')
```

The columns in the dataset are `id`, `burnout` and `context`. 

## How do I cite this work?

```
@inproceedings{sabri-etal-2024-inferring,
    title = "Inferring Mental Burnout Discourse Across {R}eddit Communities",
    author = "Sabri, Nazanin  and
      Pham, Anh C.  and
      Kakkar, Ishita  and
      ElSherief, Mai",
    editor = "Dementieva, Daryna  and
      Ignat, Oana  and
      Jin, Zhijing  and
      Mihalcea, Rada  and
      Piatti, Giorgio  and
      Tetreault, Joel  and
      Wilson, Steven  and
      Zhao, Jieyu",
    booktitle = "Proceedings of the Third Workshop on NLP for Positive Impact",
    month = nov,
    year = "2024",
    address = "Miami, Florida, USA",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2024.nlp4pi-1.21",
    pages = "224--231",
    abstract = "Mental burnout refers to a psychological syndrome induced by chronic stress that negatively impacts the emotional and physical well-being of individuals. From the occupational context to personal hobbies, burnout is pervasive across domains and therefore affects the morale and productivity of society as a whole. Currently, no linguistic resources are available for the analysis or detection of burnout language. We address this gap by introducing a dataset annotated for burnout language. Given that social media is a platform for sharing life experiences and mental health struggles, our work examines the manifestation of burnout language in Reddit posts. We introduce a contextual word sense disambiguation approach to identify the specific meaning or context in which the word {``}burnout{''} is used, distinguishing between its application in mental health (e.g., job-related stress leading to burnout) and non-mental health contexts (e.g., engine burnout in a mechanical context). We create a dataset of 2,330 manually labeled Reddit posts for this task, as well as annotating the reason the poster associates with their burnout (e.g., professional, personal, non-traditional). We train machine learning models on this dataset achieving a minimum F1 score of 0.84 on the different tasks. We make our dataset of annotated Reddit post IDs publicly available to help advance future research in this field.",
}

```
