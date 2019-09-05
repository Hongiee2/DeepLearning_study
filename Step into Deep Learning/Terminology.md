# Terminology - 기계 학습 용어 정리
---
## Neural Network
> 연결이 되어 있는 어떤 구조. 따라서 입력과 출력이 있다. 

## Training 
> 최적화(SGD, Adagrad...)를 통해 NN의 Weight를 찾아가는 과정 

## Training Data
> gradient 계산하는 과정에 사용되는 train data 

## Validation Data(Cross-validation)
> NN의 size. depth, width, batch size, learning rate 등 이런 hyper parameter 조절할때 사용하는 data 

>즉, NN을 직접 학습시키는데 사용되는 것이 아니라 NN의 구조와 hyper parameter 잡는데 사용 

## Cross-validation
> 예를 들어 5개 data 중 4개는 학습 1개는 validation함 계속. 그때 최적이되는 hyper parameter와 network 모양이 정해질 것.
그럼 그 세팅을 가지고와서 전체 데이터로 다시 한번 학습을 시킴.

## Test Data
> Test Data는 앞에 2개 Data(Train, Validation data)와 철처히 무관한 Data여야 함.

## Activation Func(ReLU, sigmoid, thanh...) 
> 주요 목적은 non-linearity를 주기 위함 

> NN에서 비선형성을 주고 다음 Layer에서 그걸 입력으로 받아 반복해서 layer를 많이 쌓으면 NN가 복잡한 함수도 표현할 수 있게 됨 

## Epoch
> 내가 전체 데이터를 한번 다 학습(updata)했을때까지 단위 

> One epoch : one forward and backward pass of all training data 

> 일반적으로 위와 같이 돌리는 것이 버거워서 Batch size만큼 mini batch learning을 함


## Batch size : the number of training examples in one forward and backward pass 

> One iteration : number of passes 

> if we have 55,000 training data, and the batch size is 1,000. Then, we need 55 iterations to complete 1 epoch.

## Cost function 
> function that we want to minimize. Cost func를 바꿔가며 최소로 Cost가 나오는 것을 찾아야하며 무엇보다 미분이 가능해야함 그래야 gradient bp가 됨 

> (미분이 안되면 강화학습쓰면 학습이 된다네..?)
