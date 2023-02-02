# NEREL

A Russian dataset with nested named entities, relations, events and linked entities.

![alt text](https://github.com/nerel-ds/NEREL/blob/master/resources/el_example_1.jpg?raw=true)

### Version history

#### 1.1
Added: Linked entities

#### 1.0
First version:
* Nested named entities 
* Events
* Relations 

### List of entity types

|No. | Entity type | No. | Entity type | No. | Entity type
|---|---|---|---|---|---
|1. | AGE | 11. | FAMILY | 21. | PENALTY
|2. | AWARD | 12. | IDEOLOGY | 22. | PERCENT
|3. | CITY | 13. | LANGUAGE | 23. | PERSON
|4. | COUNTRY | 14. | LAW | 24. | PRODUCT
|5. | CRIME | 15. | LOCATION | 25. | PROFESSION
|6. | DATE | 16. | MONEY | 26. | RELIGION
|7. | DISEASE | 17. | NATIONALITY | 27. | STATE_OR_PROV
|8. | DISTRICT | 18. | NUMBER | 28. | TIME
|9. | EVENT | 19. | ORDINAL | 29. | WORK_OF_ART
|10. | FACILITY | 20. | ORGANIZATION |  | 

### Baselines for nested NER

 - [Biaffine model](https://arxiv.org/pdf/2005.07150.pdf)
 - [Pyramid model](https://www.aclweb.org/anthology/2020.acl-main.525.pdf)
 - [SpERT](https://arxiv.org/pdf/1909.07755.pdf)
 - [MRC model](https://arxiv.org/pdf/1910.11476.pdf) (Machine Reading Comprehension)

Word representations used with all models are [fastText](https://dl.fbaipublicfiles.com/fasttext/vectors-crawl/cc.ru.300.vec.gz) (fT) and pre-trained [RuBERT-cased](http://files.deeppavlov.ai/deeppavlov_data/bert/rubert_cased_L-12_H-768_A-12_v2.tar.gz) embeddings.

For more details, please see [here](https://github.com/nerel-ds/nested-ner-benchmarks). 

### Results of nested NER for NEREL

|Method | P | R | F1 
|---|---|---|---
|Biaffine, fT | 81.64 | 77.69 | 79.62
|Biaffine, RuBERT, ft | 80.71 | 77.84 | 79.25
|Pyramid, fT | 75.87 | 72.40 | 74.09
|Pyramid, RuBERT, ft | 79.54 | 79.91 | 79.73
|SpERT, RuBERT | 82.90 | 82.14 | 82.52
|MRC | **85.04** | **84.95** | **84.99**


### List of relation types

|No. | Relation type | No. | Relation type | No. | Relation type
|---|---|---|---|---|---
|1. | ABBREVIATION | 18. | HEADQUARTERED_IN | 35. | PLACE_RESIDES_IN
|2. | AGE_DIED_AT | 19. | IDEOLOGY_OF | 36. | POINT_IN_TIME
|3. | AGE_IS | 20. | INANIMATE_INVOLVED | 37. | PRICE_OF
|4. | AGENT | 21. | INCOME | 38. | PRODUCES
|5. | ALTERNATIVE_NAME | 22. | KNOWS | 39. | RELATIVE
|6. | AWARDED_WITH | 23. | LOCATED_IN | 40. | RELIGION_OF
|7. | CAUSE_OF_DEATH | 24. | MEDICAL_CONDITION | 41. | SCHOOLS_ATTENDED
|8. | CONVICTED_OF | 25. | MEMBER_OF | 42. | SIBLING
|9. | DATE_DEFUNCT_IN | 26. | ORGANIZES | 43. | SPOUSE
|10. | DATE_FOUNDED_IN | 27. | ORIGINS_FROM | 44. | START_TIME
|11. | DATE_OF_BIRTH | 28. | OWNER_OF | 45. | SUBEVENT_OF
|12. | DATE_OF_CREATION | 29. | PARENT_OF | 46. | SUBORDINATE_OF
|13. | DATE_OF_DEATH | 30. | PART_OF | 47. | TAKES_PLACE_IN
|14. | END_TIME | 31. | PARTICIPANT_IN | 48. | WORKPLACE
|15. | EXPENDITURE | 32. | PENALIZED_AS | 49. | WORKS_AS
|16. | FOUNDED_BY | 33. | PLACE_OF_BIRTH |  | 
|17. | HAS_CAUSE | 34. | PLACE_OF_DEATH |  | 


### Baselines for In-sentence relation extraction

 - [OpenNRE model](https://arxiv.org/pdf/1909.13078.pdf)
 - [SpanBERT model](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00300/43539/SpanBERT-Improving-Pre-training-by-Representing) 
 - [TRE model](https://arxiv.org/pdf/1906.03088.pdf) 

### Baselines for nested relation extraction

 - [OpenNRE model](https://arxiv.org/pdf/1909.13078.pdf)
 - IntModel

### Baseline for Document-level relation extraction

 - [OpenNRE model](https://arxiv.org/pdf/1909.13078.pdf)

The encoders used with SpanBERT and OpenNRE are multilingual BERT and RuBERT.

### Results of relation extraction for NEREL

|Method | P | R | F1 
|---|---|---|---
|**In-sentence relations**|
|OpenNRE, mBERT | 81.7 | 81.6 | 81.7
|OpenNRE, RuBERT | **85.3** | **84.6** | **84.9**
|SpanBERT, mBERT | 76.8 | 75.4 | 76.1
|SpanBERT, RuBERT | 77.4 | 78.6 | 78.0
|TRE | 66.4 | 68.1 | 67.2
|**In-sentence nested relations**|
|OpenNRE, mBERT | 74.3 | 77.7 | 76.0
|OpenNRE, RuBERT | **77.8** | **79.6** | **78.7**
|IntModel | 76.3 | 72.4 | 74.3
|**Document-level relations**|
|OpenNRE, mBERT | 35.7 | 51.2 | 42.1
|OpenNRE, RuBERT | **52.1** | **51.3** | **51.7**

### NEREL-BIO
[NEREL-BIO](https://github.com/nerel-ds/NEREL-BIO) is an extension of the NEREL dataset, introducing biomedical entity types in addition to the general-domain entities. 

### Citing & Authors

If you find this repository helpful, feel free to cite our papers:

[1] Loukachevitch N., Artemova E., Batura T., Braslavski P., Denisov I., Ivanov V., Manandhar S., Pugachev A., Tutubalina E. [NEREL: A Russian Dataset with Nested Named Entities, Relations and Events](https://acl-bg.org/proceedings/2021/RANLP%202021/pdf/2021.ranlp-1.100.pdf). Proceedings of RANLP. 2021. pp. 880–889.

    @inproceedings{loukachevitch2021nerel,
      title={{NEREL: A Russian} Dataset with Nested Named Entities, Relations and Events},
      author={Loukachevitch, Natalia and Artemova, Ekaterina and Batura, Tatiana and Braslavski, Pavel and Denisov, Ilia and Ivanov, Vladimir and Manandhar, Suresh and Pugachev, Alexander and Tutubalina, Elena},
      booktitle={Proceedings of RANLP},
      pages={876--885},
      year={2021}
    }

[2] Loukachevitch N., Braslavski P., Ivanov V., Batura T., Manandhar S., Shelmanov A., Tutubalina E. Entity Linking over Nested Named Entities for Russian. Proceedings of LREC. 2022.

    @inproceedings{nerel-el-nne, 
      title={{Entity Linking over Nested Named Entities for Russian}},
      author={Loukachevitch, Natalia and Braslavski, Pavel and Ivanov, Vladimir and Batura, Tatiana and Manandhar, Suresh and Shelmanov, Artem and Tutubalina, Elena},
      booktitle={Proceedings of LREC},
      year={2022},
    }
