# NEREL

A Russian dataset with nested named entities, relations and events.

The dataset is available as a [release](https://github.com/nerel-ds/NEREL/releases/download/1.0/NEREL-v1.0.zip).

**Baselines for Nested NER**

 - [Biaffine model](https://arxiv.org/pdf/2005.07150.pdf)

 - [Pyramid model](https://www.aclweb.org/anthology/2020.acl-main.525.pdf)

 - [MRC model](https://arxiv.org/pdf/1910.11476.pdf) (Machine Reading Comprehension)

Word representations used with all models are [fastText](https://dl.fbaipublicfiles.com/fasttext/vectors-crawl/cc.ru.300.vec.gz) and pre-trained [RuBERT-cased](http://files.deeppavlov.ai/deeppavlov_data/bert/rubert_cased_L-12_H-768_A-12_v2.tar.gz) embeddings. 

**Baselines for In-sentence RE**

 - [OpenNRE model](https://arxiv.org/pdf/1909.13078.pdf)
 
 - [SpanBERT model](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00300/43539/SpanBERT-Improving-Pre-training-by-Representing) 
 
 - [TRE model](https://arxiv.org/pdf/1906.03088.pdf) 

**Baselines for Nested RE**

 - [OpenNRE model](https://arxiv.org/pdf/1909.13078.pdf)
 - IntModel

**Baseline for Document-level RE**

 - [OpenNRE model](https://arxiv.org/pdf/1909.13078.pdf)

The encoders used with SpanBERT and OpenNRE are multilingual BERT and RuBERT.
