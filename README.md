# Long sentences Transformer to Document Ranking

This repository store all codes used to make experiments with LongFormer (https://arxiv.org/abs/2004.05150) and Reformer (https://arxiv.org/abs/2001.04451) in the document ranking task as final project for
Deep Learning applied to NLP course in UNICAMP 1st-2020.

## How to run

All project were ran in Google Cloud Platform (GCP) due to memory limitation, because files are too large to fit in a simple computer. So i use GCP with the $300 free trial to process data and train model. All process made and how to use GCP can be found in [DATASET.md](https://github.com/lucashueda/long_sentence_transformer/blob/master/DATASET.md) and [TRAINING.md](https://github.com/lucashueda/long_sentence_transformer/blob/master/TRAINING.md).

Basically i use 2 notebooks to generate train dataset and dev/test eval datasets. Since for our project the training is a little different from evaluating i made used 2 different CGP machines, one with more memory to load MS MARCO files and other with less memory (but still more than a home computer) with GPU to train my model. All instructions and notebooks used are described in **DATASET.md** and **TRAINING.md** files.

## The Reformer

The Reformer is a variation of traditioal Transformer that optimize memory usage by some changes in self attention methodology.

## The LongFormer

Similar to Reformer the LongFormer intend to make an memory efficient Transformer, with less modifications but also excellent results Longformer was choose because of its supply by HuggigFace team, in opposite to Reformer the LongFormer has a few more pre trained models.


## The MS MARCO dataset

We used the MS MARCO Document Ranking dataset available in https://github.com/microsoft/TREC-2019-Deep-Learning that contains full documents and search queries. There is an annotated file that relate an relevant document to a specific query that we use to generate our positive-relation query-document, and another document that is the top-100 documents related to a specific query generated by BM25 simple baseline that we will use as a negative-relation query-document (or "unjudged document").

To use all files as train dataset we need to make "tripletes" with files in the format: 

<code> query_string | positive_document_string | negative_document_string </code>

## Repository structure

- dataset_gen/ : Notebooks used to generate train and eval datasets from MS MARCO files
- models/ : Notebooks used to train the models
- eval/ : Notebooks used to eval our model in MRR@10

## Requisites

- GCP (or any other cloud services that provide a robust environment)
- Transformers lib
- Pytorch

## Author

* Lucas Hideki Ueda (lucashueda@gmail.com)


