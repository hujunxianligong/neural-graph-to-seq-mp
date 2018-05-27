# Neural Graph to Sequence Model

This repository contains the code for our paper [A Graph-to-Sequence Model for AMR-to-Text Generation](https://arxiv.org/pdf/1805.02473.pdf) in ACL 2018

## Data precrocessing
Our current data loading [code](./src_g2s/G2S_data_stream.py) requires simplified AMR graphs where variable tags, sense tags and quotes are removed. For example, the simplification result of
```
(d / describe-01 :ARG0 (p / person :name (n / name :op1 "Ryan")) :ARG1 p :ARG2 genius)
```
is simpled as
```
describe :arg0 ( person :name ( name :op1 ryan )  )  :arg1 person :arg2 genius
```
Our simplifier can be downloaded via [here](https://www.cs.rochester.edu/~lsong10/downloads/amr_simplifier.tgz). It is generated by modifying [NeuralAMR code](https://github.com/sinantie/NeuralAmr).

## Training

## Decoding with a pretained model

## Cite
If you like our paper, please cite
```
@InProceedings{song-EtAl:acl2018,
  author    = {Song, Linfeng  and  Zhang, Yue  and  Wang, Zhiguo  and  Gildea, Daniel},
  title     = {A Graph-to-Sequence Model for {AMR}-to-Text Generation},
  booktitle = {Proceedings of the 56th Annual Meeting of the Association for Computational Linguistics (ACL-18)},
  year      = {2018},
  address   = {Melbourne, Australia},
}
```
