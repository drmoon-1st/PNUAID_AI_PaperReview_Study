아래 문서는 아직 완전히 정리되지않은 초기본입니다!!

# Resnet
> Deep Residual Learning for Image Recognition

## 사전에 알아야 할 논문
- VGG-Net 2014 (Very Deep 뭐시기)
	- 초기 모델(Alexnet 등) 얇은 모델들이 나왔었음
		- Alexnet은 딥러닝을 이용하여 성능이 잘 나오게 된 첫 모델
	- 모델이 깊어지면 성능이 좋아진다는 것에 착안하여 구성

## Abstract
- 깊게 만들었다.
- Residual function을 만들었다.
	- 최적화 하기에 쉽다.
	- 정확도를 얻었다.

## Introduction
- VGG-Net은 deep models로서성능이 좋았다. 그럼, 더 많은 레이어를 쌓으면 쌓을 수록 성능이 올라갈까?
	- vanishing/exploding  gradient 발생
		- normalized initialization 등으로 해결되고 있음
		- intermediate normalization layers
	- 56-layer 모델이 20-layer 모델보다 Error가 증가한 경우가 발생
- 위 문제를 타개하기 위해 `deep residual learning framework` 도입
	- F(x) = H(x) - x -> F(x) + x= H(x)
	- Dense 레이어에 대해 shortcut connections 적용

## Deep Residual Learning
### Residual Learning
`H(x)` : an underlying mapping to be fit by a few stacked layers <- 최소화하게 학습해야 함

![[Resnet-01.png]]
`F(x) = H(x) - x -> F(x) + x = H(x)`
해당 reformulation은  degradation problems에서 착안

`identity mappings`: CNN 레이어에서 다음 레이어와 이전 레이어의 size가 같은 연속된 레이어 매핑

레이어가 진행되면서 x(identity)를 더해주면서 잃어가던 초기 값을 다시 증강해주게 됨

### Identity 
x가 F(x)와 크기가 같아야 덧셈이 가능하므로 임의의 matrix Ws를 곱해서 연산하자
layer 두 개 이상 중첩 후 더하여야 효과가 나옴

### Network Architectures
**Plain network**
- VGG에 영감을 받아 34-layer plain 모델을 만들었음
- 해당 34-layer plain과 plain에 residual 연산을 더한 34-layer residual을 비교해보자

### Implementaion
어떻게 코드를 짰는가에 대한 파트

## Experiments
### ImageNet Classification
1000개 클래스 분류 문제에서 ResNet 모델은 18층 모델에 비해 34층이 에러가 더 낮게 나옴. Plain 모델은 더 높게 나옴

**building block**
64-d
3x3, 64
relu
3x3, 64
relu + x

**Bottleneck Architectures**
256-d
1x1, 64
relu
3x3, 64 (padding 이용)
relu
1x1, 256
relu + x
