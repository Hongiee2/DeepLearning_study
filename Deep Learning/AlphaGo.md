# Nature 논문으로 살펴보는 AlphaGo 알고리즘
```
DL이 제일 중요 했다고 보기 애매한 논문이라 하심 

MCTS에 특화된 논문이고 DL은 MCTS를 정의하기 위한 구성으로 쓰임 

이분은 기존의 있는 방법론 (MCTS가 됐던 강화학습이 됐던) 그런 것과 상관 없어 보이는
방법론에 DL이 가지는 진짜 중요한 특징(정말 많은 data set을 고려할 수 있다)가 합쳐지마
기존에 못하던 문제를 풀었다는 것에 의의를 두심(

즉, DL 자체로서 알고리즘도 중요하지만 DL에 들어가있는 네트워크 구조와 학습망을 가지고
기존에 있는 문제에 적용해서 좋은 성능을 내는 것도 중요한 문제라 하심!
```

## Complexity of Go

- 바둑은 엄청난 복잡도를 가진다. 

## Monte-Carlo Tree Search

- Monte-Carlo (제일 합리적으로 둘 것 같은 곳에서부터) Tree Search를 해야 빨리 찾아냄
- 나와 상대방이 번갈아가며 수를 두는 것이 tree처럼 확장
- Selection (SL Policy Net)> Expansion (SL Policy Net)> Simulation(Rollout net,value net) > Backpropagation(Rollout net,value net)의 반복

## MCTS in AlphaGo
- Rollout policy (사람의 기보만 가지고 학습) : 빨리빨리 Simulation을 봐야할때
- SL policy network (사람의 기보만 가지고 학습) : 한수한수 착수를 해봐야할때
- RL policy network : 사람+알파고끼리 두었을때 
- Value network : 판세를 평가하는 

## Training
- Rollout policy, SL policy network : 사람의 기보를 가지고 한수한수 둔 것을 입력, 출력으로 classification(19x19 중 하나를 고르는) 문제를 푼 것.

- RL policy network : 알파고끼리 둔 기보도 활용을 해야. 이긴판 reward +1 진판 reward -1

