# Logistic Regression

Cost fuc이 줄어든다해서 목적을 전부 이룬건 아님
내가 풀고하자는 문제의 costfuc을 디자인하고 그것을 이용해 최적화 하는 것이 중요.

## Cross entropy(CE) 

- 어떤 확률분포 2개가 있을때 두 확률분포간 거리

## CE in NN

- target(정답)에 대한 확률분포가 있고 NN이 뱉어주는 어떤 estimation 분포가 있는 것
- Softmax 연산을 통해 어떤 estimate한 것과 target과 비교해서 Cross entropy를 통해 거리를 줄이는 것
- 분류 상황에서 해당 index의 숫자만 높이고 나머지 숫자는 신경쓰지 않겠다는 것
- 정답에 해당하는 index의 숫자 값만 높이고 나머지는 0이니까(One-hot으로 처리되니) 신경쓰지 않겠다는 것


## Cross entropy vs Squared loss

- focuses on correct classification vs  focusses on fitting values(모든 값을 다 맞추는데 목적을 두고 있음) 

- 분류에서 Cross entropy가 더 잘 작동(정답만 신경쓰면되니)


## Tips
- Softmax 취하기 전에 나온 값을 logit이라 부름
