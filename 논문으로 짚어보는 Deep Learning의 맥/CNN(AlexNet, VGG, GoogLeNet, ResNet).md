## AlexNet
가장 기본이고 초석이 되는 구조
layers가 2개로 나눠져 있는 이유 > GPU 메모리가 부족해서. 지금은 타이탄 하나만으로도 가능하다함

Regularization in AlexNet
- Data augmentation
> 주의 숫자같이 좌우 반전시 전혀 다른 의미가 되는 경우 Filp(좌우 대칭) augmentation을 쓰면 안됨
> Color variation 각각의 RGB 채널에 어떤 특정 값을 더하는데. 학습 데이터에서 해당 RGB가 얼마나 많이 변했는지
정보를 학습으로 뽑아내고 그것에 비례해서 RGB값을 더 함.
- Dropout
일반적으로 어떤 layer가 나오면 일정 %만큼 random하게 어떤 Node를 0으로 만드는게 Dropout인데
여기서만 output을 0.5만큼 곱했는데 나중에는 이렇게 안쓴다함.




## ReLU

> 

## LRN(Local Response Normalization)
> 정규화 테크닉
> implements a form of lateral inhibition inspired by real neurons




## VGG
stride 1 3x3 필터를 사용.



## GoogLeNet
22단 Inception Module을 잘 활용

Inception Module
1x1, 3x3, 5x5, 각 Conv가 
여러 갈림길이 생겨 

One by one convlution을 해서 채널을 중간에 한번 줄였을때 이 네트워크를 정의하는 파라미터 수가 줄어든다.
레이어를 오히려 하나 더 쓰였는데 파라미터 수가 줄어든다.
1x1로 채널을 줄이고 줄어든 채널로 전체적인 파라미터를 줄임


## ResNet
1등 엄청 많이함 > 범용적으로 많이 사용될 수 있다

Is deeper network always better?
> no! 레이어가 딥해지면 BP로 얻어지는 gradient들이 너무 커지거나 작아지게 됨
근데 초기화 방법, batch normalization, ReLu의 발달로 덜 중요해지고

Overfitting : train acuuracy는 계속 좋아지는데 test acuuracy가 계속 떨어지는 것을 보고 알 수 잇ㅇ므
train 데이터를 너무 잘 맞추려고 한 나머지 test data를 못맞추는 것
그래서 train accuracy와 test accuracy가 상반된 결과를 낳으면 overfitting되서 멈추게됨

Degradation problem : layer deep하게 쌓고 train도 test도 잘되는데 성능이 잘 안나오는 것

> Residual learning building block : 어떤 타겟과 현재 입력사이의 차이만을 학습하겠다
단점은 입력단과 출력단 차원이 같아야함

 residual이 왜 좋냐?
> 가정해서 해봤더니 실제로 잘됐더라
