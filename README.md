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

## Results

In the table I represent the final result of the hyperparameter tuning of the pipelines. For more details, see the presentation in the github files

|      | dataset_name         | threshold | mod        | with_labels | recall | precision |   f1 | instr |
|------|----------------------|----------:|------------|-------------|-------:|----------:|-----:|------:|
| DSM1 | abt_buy              |      0.83 | supervised | 1           |   0.71 |      0.48 | 0.57 |     0 |
| DSM2 | dirty_itunes_amazon  |      0.85 | supervised | 0           |   1.00 |      0.90 | 0.95 |     1 |
| DSM3 | dirty_dblp_acm       |      0.90 | supervised | 1           |   0.97 |      0.96 | 0.97 |     1 |
| DSM4 | dirty_dblp_scholar   |      0.83 | supervised | 1           |   0.94 |      0.87 | 0.90 |     0 |
| DSM5 | dirty_walmart_amazon |      0.90 | supervised | 0           |   0.56 |      0.50 | 0.53 |     0 |
