# mental-burnout-disambiguation

## Dataset Description

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
@inproceedings{sabri2024inferring,
title={Inferring Mental Burnout Discourse Across Reddit Communities},
author={Sabri, Nazanin and Pham, Anh C. and Kakkar, Ishita and ElSherief, Mai},
booktitle={Third Workshop on NLP for Positive Impact (Direct Submission)},
year={2024},
url={https://openreview.net/forum?id=EL5HZ4eU1Y}
}
```
