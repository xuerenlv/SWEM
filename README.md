# SWEM (Simple Word-Embedding-based Models)

This repository contains source code necessary to reproduce the results presented in the paper [Baseline Needs More Love: On Simple Word-Embedding-Based Models and Associated Pooling Mechanisms] (ACL 2018):

## Prerequisite: 
* CUDA, cudnn
* Tensorflow (version >1.0). We used tensorflow 1.5.
Run: `pip install -r requirements.txt` to install requirements


## Run 
* Run: `python eval_dbpedia_emb.py` for ontology classification on the DBpedia dataset
* Run: `python eval_snli_emb.py` for natural language inference on the SNLI dataset
* Run: `python eval_yahoo_emb.py` for topic categorization on the Yahoo! Answer dataset
* Options: options can be made by changing `option` class in any of the above three files: 

- `opt.emb_size`: number of word embedding dimensions.
- `opt.drop_rate`: the keep rate of dropout layer.
- `opt.lr`: learning rate.
- `opt.batch_size`: number of batch size.
- `opt.H_dis': the dimension of last hidden layer.

* On a K80 GPU machine, training roughly takes about 3min each epoch and 5 epochs for Debpedia to converge, takes 50s each epoch and 20 epochs for SNLI, and 4min each epoch and 5 epochs for the Yahoo dataset.

## Data: 
* Download from the links below and put them into a `data' folder:
	* Ontology classification: [DBpedia (591MB)](https://drive.google.com/open?id=1EBmMise0LQu0QpO7T4a32WMFuTxAb6T0)
	* Natural language inference: [SNLI (101MB)](https://drive.google.com/open?id=1M13UswHThZYt-ARrHg6sN7Dlel-d6BB3)
	* Topic categorization: [Yahoo (1.7GB)](https://drive.google.com/open?id=1Dorz_CWZkHHpojVS4K4YUEhhczVLQgRc)


## Citation 
Please cite our paper if it helps with your research:

```latex
@inproceedings{Shen2018Baseline, 
title={Baseline Needs More Love: On Simple Word-Embedding-Based Models and Associated Pooling Mechanisms}, 
author={Shen, Dinghan and Wang, Guoyin and Wang, Wenlin and Renqiang Min, Martin and Su, Qinliang and Zhang, Yizhe and Li, Chunyuan and Henao, Ricardo and Carin, Lawrence}, 
booktitle={ACL}, 
year={2018} 
}
```
For any question or suggestions, feel free to contact dinghan.shen@duke.edu