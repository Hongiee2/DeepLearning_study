## Problem of Sigmoid
Vanishing Gradient
> 해결책 : ReLU, tanh, leaky_relu



## Restricted Boltzmann Machine
Initialize 방식 중 하나. 요즘에는 잘 사용 안됨
Pre-training, Fine-tuning

나중에는 Xavier / He initialization 초기화 방식이 더 많이 쓰임



## Dropout
학습을 진행하며 각 레이어에 존재하는 노드들을 무작위 특정 설정 비율에 따라 껏다 켰다를 반복
>  학습할 때만 Dropout사용 Test시에는 모든 노드를 켜야됨

## Gradient Vanishing / Exploding
Gradient Vanishing
Gradient Exploding : gradient 너무 크게 해서 발생하는 문제
> 값이 너무 큰값 혹은 NaN이 나올 때

Sol
- Change activation function
- Careful initialization
- Small learning rate
- **Batch Normalization**
