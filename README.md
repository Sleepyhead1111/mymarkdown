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
  "src_lang": "en",
  "tgt_lang": "zh",
  "translation": {
      "en": "The outliers tend to be those who die young, so that typical (median) life expectancy is higher than average life expectancy. This means that raising  the average HLE can be achieved by raising the HLE of those at the bottom of the health distribution to that of the typical (median) person. This not only makes targeting inequality more attractive, but does not require path-breaking medical innovations to achieve longer lifespans – just the achievement of typical outcomes for more people. With this in mind, it is urgent to close the sizeable rich-poor life-expectancy gap – around 15 years – in the United States. As a metric for economic and social progress, targeting HLE implicitly acknowledges that aging is malleable (if it wasn’t, it wouldn’t be a viable target). It turns out that a range of behaviors and policies, as well as the environment we inhabit, influence how we age and how long we live. It is estimated that our genetics account for only one-quarter of the factors contributing to how we age. Given this malleability, it is crucial that governments focus on HLE for the maximum number of people. Such a focus would also help governments confront one of the biggest challenges of the future: societal aging. Given that every country in the world is expected to experience societal aging, focusing on how well we age becomes paramount. This age malleability requires drawing a distinction between chronological and biological measures of age and focusing on the latter.",
      "zh": "反常之处便是那些年纪轻轻便死去的人，他们让典型（中位）寿命预期长于平均寿命预期。 这意味着提高平均健康寿命预期可以通过将位于健康分布底层的人变成典型（中位）健康寿命预期的人来实现。 这不仅让针对不平等性问题变得更有吸引力，也不必一定需要突破性的医学创新才能实现生命周期的延长 — — 而只需要让更多人实现典型结果。 基于此，现在迫切需要缩小美国庞大的贫富寿命预期差距 — — 大约在15年左右。 作为一个经济和社会进步的指标，健康寿命预期间接承认衰老具有可塑性（若非如此的话，这就不是一个可行的目标 ） 。 一系列行为和政策，以及我们所居住的环境，都影响着我们如何变老和如何延长我们的寿命。 据估计，我们的器官大约占我们衰老的四分之一因素。 考虑到这一可塑性，政府必须关注最大数量人口的见刊寿命预期。 关注这一点也有助于政府面对未来最巨大的挑战之一：社会老龄化。 世界上每一个国家都会经历社会老龄化，关注我们以多么优秀的方式衰老变得至关重要。 这一年龄可塑性需要区分年龄的时间和生物指标，专注于后者。"
  },
  "task_type": "doc_trans",
  "data_name": "news-commentary_v18.1"
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

