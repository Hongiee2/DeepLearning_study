## Regularization

---

## Parameter Norm Penalties
- NN학습시키는데 있어서 Weight를 너무 커지지 않게 하는 것이 중요
- 제곱이나 절대값 같은 파라미터에 패널티를 줌

## Dataset Augmentation
- The best way to make a ML modle generalize better is to train it on more data
- One way to get around this problem is to create fake data and add it to the training set
- GAN을 써서도 할 수 있다네

## Noise Robustness
- layer 여러개 있을때 layer 중간중간에 noise 집어넣는게 parameter 줄이는데 좋다

- Another way that noise has been used is by adding it to the weights

## Semi-Supervised Learning
- Un/Supervised 두개 합친 러닝
- semi-supervised learning usually refers to learning a representation.
```
the goal is to learn a representation so that examples from the same class have similar representataions. 

Unsupervised learning can provide useful cues for how to group examples in representation space.
```

## Multi-Task Learning

- 한번에 여러 문제를 푸는 것
- Among the factors that explain the variations observed in the data associated with the different tasks, some are shared across two or more tasks.

## Early Stoping
- traning error는 줄어드는데 validation error는 올라가는 것

## Parameter Typing and Parameter Sharing
- 어떤 파라미터들을 공유하는 것 > 파라미터 수를 줄이는 역할을 함

## Bagging and Other Ensemble Methods
- Variance가 높다 > 다양하게 나오는 것
- Bias가 높다 > 틀린 것. 정답에서 멀어진 것

```
high bias low Variance는 걍 안좋은 모델
```
- Bagging : High Variance를 low Variance로 만드는 것
- Boosting : weak learner을 sequential하게 두어 차이만큼 학습하고 넣고 붙이고 반복(ex. AdaBoost)

## Adversarial Training

- NN에 사람이 보고 관측할 수 없는 아주 미세한 noise를 섞게되어 test하면 완전 다른 class가 나옴
- 학습시킬때 입력단에 noise 넣고 data Augmentation하면 Adversarial examples 강해짐.
- 우리가 가지고 있는 모델의 기울기가 엄청나게 가파르다(노이즈 좀만 섞은데도 전혀 다른 결과가 나오니)
