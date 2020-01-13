## Overfitting

MLE는 숙명적으로 Overfitting을 따르게 됨

실제 우리가 알고 싶은 Decision boundary가 아닌주어진 데이터에 대해 과도하게 fitting되는 것.

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


## Overfitting 최소화

Training / Validation / Test Set으로 나눠 학습  

Training Loss는 내려가는데 Validation Loss가 증가하면 Overfitting이 일어나고 있다는 증거
