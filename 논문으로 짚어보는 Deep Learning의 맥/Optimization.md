# Optimization 방법론 
training 할때 사용하는 Opt 무엇이 있는지

## Gradient descent_경사하강법 

- Batch gradient descent 
```
데이터 전체를 한번에 고려해서 한번 gradient를 계산하는 것
오래걸림
```

- Stochastic gradient descent
```
한번에 한개씩만 보는 것 
55,000개를 모두 최소로하는 어떤 한 점을 찾고 싶은데 SGD는 한번에 한개씩만 보는 것
그러다보니 하나가 나머지 49,999에게 안좋을수도 있어 그래프 진동이 큼
```
 
- Mini-batch gradient decent
```
64 - 256개 데이터를 써서 (중간만큼) 번갈아가면서 골라가며 학습을 시키는 것
```

## Challenges
- learning rate 맞추기 어려움
- Local minima에 빠질 수 밖에 없음

## momentum 
- 이전에 있던 gradient 정보 활용해서 지금 gradient update하는 것

## Adagrad
- learning rate 스케줄링 하는 것인데 모든 파라미터마다 learning rate을 바꾸는 것
- larger updates for infrequent and smaller updates for frequent parameters 
- 많이 변했던 것은 조금 변하게하고 조금 변하게 한 것은 많이 변하게
```
learning rate가 계속 줄어드는 단점이 있음
```

## Adadelta
- learning rate가 계속 줄어드는 것을 막음
- exp moving average를 가지고 learning rate을 스케쥴링 해준다.
- 최근에 gradient가 많이 변한 parameter는 조금 쓰고 최근에 조금 변한 것은 많이
- no learning rate

## Adam
- learning rate와 momentum을 합친 것
- 왠만하면 Adam을 쓰면 좋다....
 

## Which optimizer to use?

- Use adaptive learning rate methods(Adagrad, Adadelta, Adam)


## Curriculum Learning
- 학습 데이터를 처음부터 다 써서 학습하는 것이 아닌 조금 쉬운 것부터 학습하는 것 

