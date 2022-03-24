# Parallel compression data

This archive contains parallel compression data used for the experiments reported in [(Ive and Yvon, 2016)](https://aclanthology.org/C16-1142/). For this study, a small set of parallel sentences extracted from the testset of the [WMT 2014 News translation shared task](https://statmt.org/wmt14/translation-task.html) has been simultaneously compressed in both languages. The result is a 4-way corpus, where the relationship between two sentences in the same language is that of compression /expansion; while the relationship between sentences in different languages is that of translation.

## Data 

The `sgm/` directory contains the original News articles. The traces of editing operation are in the `trace/` directory and contains two files structured  as follows:

Each document change starts withe a document ID line.  Then, each subsequent line starts with the number of the line in the original document, followed by a colon, and a list of  deleted characters in the original sentence, separated by a semicolon. This list is empty if no deletion was performed.

Thus,
```
 docid="1204-canoe"
 1:
 2:115;117;118;119;120;121;122;123;124;127;129
```

contains trace of editing operations that for the document  ID docid="1204-canoe". The first line was left unchanged. Characters at the positions 115,117,118 etc. were deleted from the second line.

The `aligned/` directory contains a pre-processed version, with just the four parallel versions of each sentence tokenized with basic rules. Each file contains exactly 1002 lines. 

## Reference
Please cite the following research article if you use any part of the corpus in your work: 

```
@inproceedings{ive—yvon-coling2016,
author = {Julia Ive and Fran\c{c}ois Yvon},
title = {Parallel Sentence Compression},
booktitle = {Proceedings of COLING 2016, the 26th International Conference on Computational Linguistics: Technical Papers},
  month     = {December},
  year      = {2016},
  address   = {Osaka, Japan},
  pages     = {1503–1513},
  url       = {https://aclanthology.org/C16-1142/}
} 
```
## Licence
This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/).
