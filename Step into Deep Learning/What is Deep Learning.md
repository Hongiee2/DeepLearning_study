# 수정중

Deep learning?
- Machine Learning
- High-level abstraction
- Network

ML과 Deep Learning의 차이
ML : data가 주어졌을때 이 data로부터 유용한 정보를 뽑아내는 것
DL : ML안에 조그만한 분야. 어떤 data가 주어졌을때 그 데이터를 통해서	유용한 정보를
뽑아낼 수 있는 좋은 알고리즘 중 하나. DL 안에 multi level perceptron(MLP),
CNN, RNN 등의 구조가 있음.

DL 오래된 연구 분야 바탕이 되는 연구들 오랫동안 진행되어 왔음.
최근들어 기술의 발전으로 실생활에 적용 가능해진 것

DL이 잘 동작하는 건 단순히 인간의 뇌를 잘 모방하기때문이 아니라
그 구조가 많은 데이터를 처리하기 적합하기 때문임.

NN의 어떤 엄청 유명한 한 논문에 의하면 MLP구조가 임의의 어떤 함수를 모두 모방할 수 있다함
(헉 엄청난 것)

```
MLP는 Fully Connected Layer, Dense Layer 등의 여러 이름으로 불리며 기존의 CNN에 많이 활용되는 구조
```

DL은 만능인가?
- 학습시키기위해 많은 테크닉들이 필요하고 그를 위해서 데이터도 많이 필요

Black Box : 기존에 있는 많은 모듈들을 그냥 활용해서 데이터를 활용하긴 쉽지만
새로운 것을 만들긴 힘든(tensorflow)

white Box : 밑바닥부터 모든 것을 바꿔서 입맛대로 변형시킬 수 있는(Pytorch)

---

Course Contents

Regularization 기계 학습 전반의 아주 중요한 토픽
Main purpose is to avoid "OverFitting(과적합)"

Optimization Methods : 학습 최적화 방법론(SGD,Adagrad...)

Restricted Boltzmann Machine(RBM) : 비지도학습방법론

Denoising Auto-Encoder : 중간과정에서 노이즈가 있는 어떤 이미지가 들어오면
노이즈가 없는 image로 reconstruction

Semantic Segmentation : 이미지를 각 픽셀별로 뜻하는게 무엇인지 맞추는 알고리즘. 이 픽셀은 강아지or고양이에 속한다를 알려줌 

Weakly-Supervised Localization : 이미지에서 각 픽셀들이 어떤 class에 속하는지 알수있게됨

Semantic Segmentation과의 차이점은 Semantic Segmentation은 ground-truth가 필요 각 픽셀이 무엇인지 라벨링이 필요
근데 Weakly-Supervised Localization은 이미지와 이미지에 해당하는 class 정보만 있으면 됨
(이 이미지가 금붕어다라는 사실만 알면 되는거지 금붕어가 여기있다라는 정보는 필요X)
그럼에도 출력값으로 금붕어가 어디있는지 잘나옴

Detection Methods : R-CNN, SPP net, Fast R-CNN, Faster R-CNN.
Detection은 이미지가 주어지면 이미지안에 물체들의 위치를 찾는 것(Semantic Segmentation과 비슷하지만 Detection은 강아지에 Bounding box를 처줌)

Visual Q&A : 이미지와 단어들로 구성된 문장이 같이 들어감.

Super Resolution : 저해상도 이미지가 들어왔을때 고해상도 이미지를 찾는 알고리즘

Deep Reinforcement Learning 

Sequence Generation : 지금까지는 주어진 것을 어떻게 잘 해석할까인데 이건 새로운 것을 만들어 보는 것

Word Embedding : 단어들을 어떻게 컴퓨터가 이해하기 쉬운 숫자들로 옮길 수 있는지 

Image Captioning : 이미지가 주어지면 이미지를 설명하는 문장을 만드는 알고리즘

Hangul-RNN : 구운몽을 가지고 학습한 네트워크가 그와 비슷한 것을 만들어볼 것

ResNet 알아볼 것

Neural Style : Texture Synthesis Using Convolutional Neural Networks 논문과 
Understanding Deep Image Representations by Inverting Them을 잘 섞은게 Neural Style
이 둘을 각각 알아보고 코드도 볼 것

Mixture Density Network : 일반적으로 NN입력고정되면 고정된 output이 나오는데
어떤 입력에 대해 출력을 가우시안 Mixture Model로 Modeling할 수 있다...

Domain Adversarial Network : 시뮬레이터 소스공간 input과 output 둘다 잘 구할 수 있는 공간에서 학습을 시키고
실제 적용 target 공간에서는 이미지만 주어짐. 그때 그 공간에서 해당 이미지가 무엇인지 찾는 것. 그것을 딥러닝으로 찾는

One-Shot Learning : NN의 가장 큰 단점은 새로운 데이터를 처리하기 힘들다는 것인데
(ex 어떤 분류기에 새로운 class를 추가해야할 때) 그 해당하는 데이터를 다시 학습데이터로 집어넣어서
처음부터 다시 학습시켜야하는데 비효율적. 그래서 주어진 새로운 dataset을 빨리 학습시킬 수 있는지

Metric Learning : 두개 이미지 주어졌을때 두 이미지 사이 거리를 나타내는 것

Memory Network : 컴퓨터구조(메모리)를 NN으로 만든 것

Uncertainty in NN : NN이 이미지를 잘 분류할때도, 잘 분류못할때도 있는데 그때 NN이 확실하지 않다는 정보를 구할 수 있으면 좋겠는데
이에 관해 연구하는 논문


