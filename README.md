# Can LLM2Vec be good for ER task?

## LLM problem in ER

LLM achieve state of the art in the tast of Entity Matching in the majority of the dataset, but have several problem like:
-   opacity;
-   unable to provide numeric accuracy

## Idea

Using the idea of [LLM2Vec: Large Language Models Are Secretly Powerful Text Encoders](https://arxiv.org/abs/2404.05961), we want to embed a record and use numerical vector instead of generative answer for evaluation.

## Dataset
Standard dataset taken by github [Deepmatcher](https://github.com/anhaidgroup/deepmatcher/blob/master/Datasets.md) for benchmarking.

The first one is clean, the others are dirty by adding noise in the records.

## Files

In `notebook`  folder are stored the notebook used for the projects.

The `data` are stored in google drives. The embeddings can be retrieved here: [data](https://drive.google.com/drive/folders/1BTyFyfAgUPi4sshXUhit7Lcf62SXFte6?usp=sharing). 
The embeddings are zipped and separated by instruction id. 
Are stored also the train/valid split for training pourpose. 
