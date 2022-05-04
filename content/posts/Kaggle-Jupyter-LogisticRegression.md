---
title: "KaggleのJupyter NotebookでLogisticRegressionをすると吐くエラーの対策"
date: 2022-02-14T21:15:34+09:00
draft: false
categories: ["programming","kaggle"]
---

# エラーの概要
多くのサイトで乗っているような手順に従って
```python
from sklearn.linear_model import LogisticRegression
model=LogisticRegression()
```
として、KaggleのJupyter Notebookでロジスティック回帰すると
```shell
AttributeError: 'str' object has no attribute 'decode'
```
エラーを吐きます
# 対策
```python
from sklearn.linear_model import LogisticRegression
model=LogisticRegression(solver='liblinear')
```
こうすればエラーが出なくなります

# 参考
[Kaggleのディスカッションページ](https://www.kaggle.com/general/269699)
