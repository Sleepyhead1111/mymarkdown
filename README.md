# Dataset Card for "ComMT"

## Dataset Description

- **Homepage:** 
- **Repository:** https://github.com/NiuTrans/LaMaTE/
- **Paper:** https://arxiv.org/

### Dataset Summary

ComMT(Comprehensive Machine Translation benchmark) is a diverse translation-related dataset, aiming to assess how well the machine translation system generalizes across various tasks that evaluate different aspects of a translation model.

While there have been datasets developed for fine-tuning LLMs for multiple translation tasks, our focus is on a broader range of application scenarios. We hope that such a benchmark can be adopted to provide a systematic  evaluation of machine translation systems, and that this, in turn, will encourage practitioners to pay more attention to the issue of generalization when developing these systems.

### Supported Tasks and Languages

ComMT includes 6 tasks in total, and supports four languages: German, Czech, Russian, and Chinese, as shown in the figure below：

<img src="https://github.com/Sleepyhead1111/mymarkdown/blob/main/commt.png"  width="600" height = “600”/>

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
  "task_type": "general_trans",
  "data_name": "wmt23_news"
}
```

##### Doc-level Translation

An example of 'test' looks as follows.
```
{
  "src_lang": "en",
  "tgt_lang": "zh",
  "translation": {
      "en": "The outliers tend to be those who die young, so that typical (median) life expectancy is higher than average life expectancy. This means that raising the average HLE can be achieved by raising the HLE of those at the bottom of the health distribution to that of the typical (median) person. This not only makes targeting inequality more attractive, but does not require path-breaking medical innovations to achieve longer lifespans – just the achievement of typical outcomes for more people. With this in mind, it is urgent to close the sizeable rich-poor life-expectancy gap – around 15 years – in the United States. As a metric for economic and social progress, targeting HLE implicitly acknowledges that aging is malleable (if it wasn’t, it wouldn’t be a viable target). It turns out that a range of behaviors and policies, as well as the environment we inhabit, influence how we age and how long we live. It is estimated that our genetics account for only one-quarter of the factors contributing to how we age. Given this malleability, it is crucial that governments focus on HLE for the maximum number of people. Such a focus would also help governments confront one of the biggest challenges of the future: societal aging. Given that every country in the world is expected to experience societal aging, focusing on how well we age becomes paramount. This age malleability requires drawing a distinction between chronological and biological measures of age and focusing on the latter.",
      "zh": "反常之处便是那些年纪轻轻便死去的人，他们让典型（中位）寿命预期长于平均寿命预期。这意味着提高平均健康寿命预期可以通过将位于健康分布底层的人变成典型（中位）健康寿命预期的人来实现。这不仅让针对不平等性问题变得更有吸引力，也不必一定需要突破性的医学创新才能实现生命周期的延长——而只需要让更多人实现典型结果。基于此，现在迫切需要缩小美国庞大的贫富寿命预期差距——大约在15年左右。作为一个经济和社会进步的指标，健康寿命预期间接承认衰老具有可塑性（若非如此的话，这就不是一个可行的目标）。一系列行为和政策，以及我们所居住的环境，都影响着我们如何变老和如何延长我们的寿命。据估计，我们的器官大约占我们衰老的四分之一因素。考虑到这一可塑性，政府必须关注最大数量人口的见刊寿命预期。关注这一点也有助于政府面对未来最巨大的挑战之一：社会老龄化。世界上每一个国家都会经历社会老龄化，关注我们以多么优秀的方式衰老变得至关重要。这一年龄可塑性需要区分年龄的时间和生物指标，专注于后者。"
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
  "task_type": "domain_medical",
  "data_name": "wmt21_biomedical"
}
```

##### Terminology-constrained Translation

An example of 'test' looks as follows.
```
{
  "src_lang": "en",
  "tgt_lang": "zh",
  "translation": {
      "en": "Tim's younger brother, Tod Leiweke, is currently the chief operating officer of the National Football League since 2015.",
      "zh": "蒂姆的弟弟托德·莱维克自 2015 年以来担任国家橄榄球联盟的首席运营官。"
  },
  "hints": [{"en": "National Football League", "zh": "国家橄榄球联盟"}],
  "task_type": "term_con_trans",
  "data_name": "PAWS-X"
}
```

##### Automatic Post-edition

An example of 'test' looks as follows.
```
{
  "src_lang": "en",
  "tgt_lang": "zh",
  "translation": {
      "en": "unfazed, Matteo hires an assassin to bomb the resort to create chaos and mayhem.",
      "zh": "马特奥不慌不忙地雇用了一名刺客来轰炸度假村，从而引起混乱。"
  },
  "mt_gen": "马特奥不慌不忙地雇用了一名刺客来轰炸制造混乱和混乱的手段.",
  "task_type": "ape",
  "data_name": "wmt21_APE"
}
```

##### In-context Learning

An example of 'train' looks as follows.
```
{
  "src_lang": "zh",
  "tgt_lang": "en",
  "translation": {"zh": "如何永久关闭Facebook帐户", "en": "How to close Facebook account permanently"},
  "task_type": "context_learning_trans",
  "data_name": "TowerBlocks",
  "meta_task": "general_trans",
  "shots": [
  {"src_lang": "en", "tgt_lang": "zh", "translation": {"en": "Since then, more knowledge was accumulated through extensive studies on HCoV-229E and HCoV-OC43, both of which cause self-limiting symptoms.", "zh": "此后，通过对两种均可引起自限性症状的 HCoV-229E 和 HCoV-OC43 病毒的广泛研究，人类积累了更多相关知识。"}, "data_name": "tico19", "task_type": "general_trans"},
  {"src_lang": "en", "tgt_lang": "zh", "translation": {"zh": "柴油汽车是一项很好的发明。", "en": "The diesel car was a wonderful invention."}, "data_name": "UM-corpus_education", "task_type": "general_trans"},
  {"src_lang": "en", "tgt_lang": "zh", "translation": {"en": "While much about COVID-19 is still unknown, preliminary data suggests that it is more virulent and contagious than the seasonal flu, and less virulent but more contagious than SARS and MERS.", "zh": "尽管关于 COVID-19 我们还有很多未知的地方，但初步数据表明，该病毒比季节性流感的毒性和传染性更强，毒性弱于 SARS 和 MERS 但传染性更强。"}, "data_name": "tico19", "task_type": "general_trans"}
  ]
}
```

### Data Fields

All tasks have 5 keys as described below:

- `src_lang` (`str`): source text language.
- `tgt_lang` (`str`): target text language.
- `translation`: a `dictionary` feature containing:
  - `src_lang`: a `string` feature.
  - `tgt_lang`: a `string` feature.
- `task_type`: a `string` feature.
- `data_name`(`str`): data source.

Some tasks have other keys as described below:

#### Terminology-constrained Translation
- `hints`: a `list` feature containing:
  - `src_lang` (`str`): source language terminology.
  - `tgt_lang` (`str`): trget language terminology.

#### Automatic Post-edition
- `mt_gen`(`str`): text generated by machine translation

#### In-context Learning
- `meta_task` (`str`): 
- `shots`: a `list` feature containing examples for `General Translation` task

### Data Splits

| name | train |validation| test|
|------|:-----:|---------:|:---:|
|De-en | 76912 |          |17968|
|Ru-en | 60690 |          |15923|
|Zh-en | 75619 |          |18122|
|Cs-en | 26440 |          |12965|



## Additional Information

### Licensing Information

The dataset is licensed under the MIT License.

### Citation Information

```
@article{article_id,
  author    = {Author List},
  title     = {Dataset Paper Title},
  journal   = {Publication Venue},
  year      = {2025}
}
```

