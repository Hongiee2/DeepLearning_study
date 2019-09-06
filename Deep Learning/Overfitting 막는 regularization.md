## Overfitting 막는 regularization

## Regularization?
- Main purpose is to avoid "OverFitting"

## OverFitting
- 학습 데이터를 너무 믿는 나머지 test data를 못 맞추는 것
- 학습 데이터를 이용하는 이유는 test data를 맞추기 위함인데(주객전도)
- data에 noise가 많을때도 문제가 됨
- training error는 줄어드는데 test error가 커질때
- NN을 더 복잡한 것을 사용하면 할수록 OverFitting의 확률이 더 커짐

## Preventing OverFitting?
- Get more data (data Augmentation도 해당)
- Use a model with the right capacity(적절한 능력을 가지는 모델 활용하기)
- Average many different models(Ensemble) 
```
ex) 데이터 셋 10,000개 있으면, 데이터 셋을 8000개씩 뽑아서 5개의 set을 만들어
각각의 모델을 8,000개씩 학습. 어떤 입력이 새로들어오면 모델이 5개 있으니
5개 결과가 나오고 5개 결과가 제일 많이 가르키고 있는 것을 쓰는 것
```
- Use DropOut, DropConnect, or BatchNorm


## Limiting the Capacity
- Architecture : Limit the number of hidden layers and units per layer
- Early stopping : Stop the learning before it overfits using validation sets
```
NN이 학습을 시키다가 너무 많이 학습이 되면 validation error가 줄어드다가 다시 커지게 시작되면
그때 학습을 멈추는 것
```
- Weight-decay : Penalize large weights using penalties or constraints on their squared values(L2 penalty) or absolute values(L1 penalty)
```
학습한 parameter를 너무 커지지 않게 하는 것
```

## DropOut
- DropOut increases the generalization performance of the neural network by restricting the model capacity
```
한 layer가 있을때 그 layer의 node들을 몇개 꺼버리는 것. 중요한 것을 학습할때만 몇개 0으로 만들고 나머지는 씀. 

test할땐 다 쓰고. 끄는 것도 random으로
```

## DropConnect
- DropOut은 Node를 끊는거였다만 DropConnect는 weight를 끊는 것. layer 값을 0으로 만드는게 아니라 weight를 끊어버리는 것

## Batch Normalization(중요)
Benefits of BN 

- Increase learning rate
- Remove Dropout(Dropout 안써도 된다)
- Reduce L2 weight decay
- Accelerate learning rate decay
- Remove Local Response Normalization

> 배치 짱이다

