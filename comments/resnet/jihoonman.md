resnet 논문 커멘트(틀린 내용이 있어도 양해부탁드리고 많은 피드백 부탁드림다)
Abstract 더 많은 층을 가진 신경망 알고리즘의 학습을 위해 Residual Learning을 사용한다. 이 모델은 기존보다 더 낮은 오류를 발생시키며, 더 효율적이다.
설명: 층과 층사이 relu 등의 활성화 함수를 통해 학습이 진행되는 기존 모델. 거기에 층을 뛰어넘는 원래값 identity를 추가, 원래함수는 f(x)지만, 이과정 거치면 아이덴티티 x를 더해 f(x) + x가 됨. (이를 이용하면 층별 독립성이 조금은 줄어들어 과대적합을 방지할 수 있을것)개인적생각. 
기존 모델에 비해 층이 적을때는 차이가 적지만, 층이 많아질수록 서로의 독립성이 사라져 오류확률이 줄어듬.
결론, resnet이 기존 모델보다 효율적이다!
