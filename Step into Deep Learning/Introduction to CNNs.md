# CNN
CNN are basically layers of convolutions followed by subsampling and fully connected layers

- convolution, sub sampling(max pooling같은)의 주된 역할
> Feature extraction

# FC
fully connected layers classifies which category current input belongs to using extracted features
> 최종적으로 분류를 위해 필요한 것


## CNN 왜 잘될까?
1. Local Invariance
> 동일한 Convolution Filter 모양이 전체 이미지를 '모두' 돌아다님 

2. Compositionality
> Conv -> Conv -> Conv 계층구조

# Convolution
> 결국, Conv 연산은 내가 Conv 하려는 Filter 모양과 내가 Conv하는 위치 픽셀이 얼마나 유사한지를 나타냄 

> 값이 클수록 원본의 것과 유사한 것

# Stride
> 몇칸씩 건너뛸 것인지

# channels
> 필터의 채널과 필터의 대상이 되는 채널이 같아야한다!!! 

> 필터 개수를 얼마큼 늘릴 것인지는 자유

# parameters
> DL에서 parameter의 개수는 적으면 적을수록 좋음. 뒷단 FC에서 parameter를 엄청 많이 먹는데 이것을 최대한 간소화하는게 성능향상에 중요.
