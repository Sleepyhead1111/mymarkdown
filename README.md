# Dataset Card for "ComMT"

## Table of Contents
- [Dataset Description](#dataset-description)
  - [Dataset Summary](#dataset-summary)
  - [Supported Tasks and Leaderboards](#supported-tasks-and-leaderboards)
  - [Languages](#languages)
- [Dataset Structure](#dataset-structure)
  - [Data Instances](#data-instances)
  - [Data Fields](#data-fields)
  - [Data Splits](#data-splits)
- [Dataset Creation](#dataset-creation)
  - [Curation Rationale](#curation-rationale)
  - [Source Data](#source-data)
  - [Annotations](#annotations)
  - [Personal and Sensitive Information](#personal-and-sensitive-information)
- [Considerations for Using the Data](#considerations-for-using-the-data)
  - [Social Impact of Dataset](#social-impact-of-dataset)
  - [Discussion of Biases](#discussion-of-biases)
  - [Other Known Limitations](#other-known-limitations)
- [Additional Information](#additional-information)
  - [Dataset Curators](#dataset-curators)
  - [Licensing Information](#licensing-information)
  - [Citation Information](#citation-information)
  - [Contributions](#contributions)

## Dataset Description

- **Homepage:** 
- **Repository:** https://github.com/
- **Paper:** https://arxiv.org/
- **Point of Contact:** [More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)
- **Size of downloaded dataset files:** 
- **Size of the generated dataset:** 
- **Total amount of disk used:** 

### Dataset Summary

### Supported Tasks and Leaderboards

[More Information Needed](https://github.com/)

### Languages

[More Information Needed](https://github.com/)

## Data Structure

### Data Instances 

##### General Translation

An example of 'test' looks as follows.
```
{
  "src_lang": "en",
  "tgt_lang": "zh",
  "translation": {
      "en": "I know that advertising is how they make their money, but all that garbage seems counterproductive if it drives people away.",
      "zh": "我知道广告是为他们创收的一种方式，而如果大量的广告让观众反感离开，似乎会适得其反。"
  },
  "data_name": "wmt23_news",
  "task_type": "general_trans"
}
```

##### Doc-level Translation

An example of 'test' looks as follows.
```
This example was too long and was cropped:

{
    
}
```

##### Domain Translation

An example of 'test' belongs to domain_medical looks as follows.
```
{
  "src_lang": "en",
  "tgt_lang": "zh",
  "translation":{
      "en": "The median age of the 30 patients was 56.5 (28-80) years old, among them, 25 patients were primary plasma cell leukemia, and 5 patients were secondary plasma cell leukemia.",
      "zh": "30例PCL患者中位年龄56.5（28-80）岁，25例为原发性浆细胞白血病，5例为继发性浆细胞白血病。"
  },
  "data_name": "wmt21_biomedical",
  "task_type": "domain_medical"
}
```

##### Terminology-constrained Translation

An example of 'test' looks as follows.
```
This example was too long and was cropped:

{
    
}
```

##### Automatic Post-edition

An example of 'test' looks as follows.
```
This example was too long and was cropped:

{
    
}
```

##### In-context Learning

An example of 'train' looks as follows.
```
This example was too long and was cropped:

{
    
}
```

### Data Fields

The data fields are the same among all splits.

#### General Translation
- `text`: a `string` feature.

#### Doc-level Translation
- `text`: a `string` feature.

#### Domain Translation
- `text`: a `string` feature.

#### Terminology-constrained Translation
- `text`: a `string` feature.

#### Automatic Post-edition
- `text`: a `string` feature.

#### In-context Learning
- `text`: a `string` feature.

### Data Splits

| name | train |validation|test|
|------|------:|---------:|---:|
|De-en |       |          |    |
|Ru-en |       |          |    |
|Zh-en |       |          |    |
|Cs-en |       |          |    |

## Dataset Creation

### Curation Rationale

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Source Data

#### Initial Data Collection and Normalization

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

#### Who are the source language producers?

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Annotations

#### Annotation process

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

#### Who are the annotators?

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Personal and Sensitive Information

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

## Considerations for Using the Data

### Social Impact of Dataset

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Discussion of Biases

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Other Known Limitations

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

## Additional Information

### Dataset Curators

[More Information Needed](https://github.com/huggingface/datasets/blob/master/CONTRIBUTING.md#how-to-contribute-to-the-dataset-cards)

### Licensing Information

The dataset is licensed under the MIT License.

### Citation Information

```

```


### Contributions

