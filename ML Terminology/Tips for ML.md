# Tips

## overfitting

MLE는 숙명적으로 Overfitting을 따르게 됨

실제 우리가 알고 싶은 Decision boundary가 아닌주어진 데이터에 대해 과도하게 fitting되는 것.



## Overfitting 최소화

Training / Validation / Test Set으로 나눠 학습  

Training Loss는 내려가는데 Validation Loss가 증가하면 Overfitting이 일어나고 있다는 증거



## Overfitting
High accuracy on the training dataset  
Poor accuracy on the test dataset

- 데이터를 많이 모을수록 해결할 수 있음
- Less Features를 사용하면 Overfitting을 막을 수 있음
- **Regularization**으로 overfitting 방지 가능
> Early Stopping : Validation Loss가 더이상 낮아지지 않을 때
> Reducing Network Size
> Weight Decay
> Dropout
> Batch Normalization



## Data Processing

Standardization : 정규분포화
> 우리가 가진 데이터가 정규 분포를 따른다고 가정하고  평균과, 분산을 구해 정규분포의 값으로 만듬



## 용어
Epoch : training set 전체가 한번 사용되면 1 Epoch가 돈 것  

batch size : 전체를 나눠 트레이닝 함

iterations : batch를 몇번 사용했냐



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



## Internal Covariate Shift
Internal Covariate Shift가 Gradient Vanishing이나 Exploding 같은 문제를 만든다
> Training 분포와 Test 분포의 차이가 위와 같은 문제를 일으킨다

Sol
- 각 layer마다 normalization하는 Batch Norm 실행

> Batch norm으로 계속 normalization하면 activation func의 non linearity를 잃게 되는데 이를 완화시켜주기 위해 사용하는게 베타와, 감마
