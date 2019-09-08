# Restricted Boltzmann Machine(RBM) 

```
대표적 Unsupervised Learning Model 

NN을 학습시킬때 Pretrain으로 활용됨 - 미리 이미지만 가지고 Network의 길을 터놓고 
초기값으로해서 NN 학습시키면 성능이 잘나옴 

```


- Energy-based models
```
the probability of a certain state is inversely proportional to its energy 

A restricted Boltzmann machine restricts connections between visible and hidden nodes 
```

```
RBM을 학습하는 건 결국 Energy를 학습하는 것. 
어떠한 Visible이 주어졌을때 그 Visible을 최대화하는 parameter를 찾는 것 
parameter는 Energy를 정의하는 W,b,a
```

## Contrastive Divergence
```
수식 아직 이해 잘 못함
```
