# [Deep Residual Learning for Image Recognition(문경환)](../pdfs/Deep_Residual_Learning_for_Image_Recognition.pdf)
* <strong>동훈</strong>: identity 값인 input `x`가 단순히 layer를 통과하면서 `gradient vanishing`을 방지하거나 사라진 초기의 기억을 계속 전파할 수 있게 하는 역할로 생각했어요. 논문을 다시 읽어보니 F(x)의 아웃풋을 H(x)가 아닌 `H(x)-x`로 제한을하면서 각 Residual block이 자신만의 작은 목표에 집중하도록 만드는 것 같네요! x를 미분하면 1이니까 연산도 쉬워지니까 일석이조인 것 같습니다!

* <strong>지현</strong>: 이번 세미나는 "Deep Residual Learning for Image Recognition" 논문을 중심으로 진행되었습니다. 이 논문은 기존의 신경망 모델들이 깊이를 증가시킬 때 발생하는 `degradation problem`을 해결하기 위해 `Residual Learning`을 도입한 연구입니다. 층이 깊어질수록 최적화가 어려워지고, 성능이 저하되는 문제를 해결하기 위해 저자들은 각 레이어가 `잔차 함수` (residual function)을 학습하도록 설계하고, 이로 인해 `identity mapping` 을 활용한 효율적인 학습을 가능하게 합니다. 해당 방식은 네트워크가 훨씬 깊어지더라도 안정적인 학습을 가능하게 하여, 점점 더 깊고 정밀한 구조로 발전하는 최근 딥러닝 모델들에 매우 유용하게 적용될 것 같습니다. 좋은 발표 감사합니다.

* <strong>민혜</strong>: - 합성곱 신경망부터 렐루함수까지, AI초보자인 저에게는 용어들이 낯설게 다가와 원활하게 이해하기에 어려움이 많았습니다. 발표자님의 좋은 설명 덕분에 논문의 전체적인 중심내용을 파악할 수 있었고, 간략하게라도 이해하는 것에 의의를 두게 되었습니다. 아주 전문적인 커멘트를 작성하진 못했지만, 관심이 있는 분야인 만큼 추후 더 깊은 공부를 한 뒤 이 논문을 다시 공부해 보고 싶습니다.

* <strong>지훈</strong>: resnet 논문 커멘트(틀린 내용이 있어도 양해부탁드리고 많은 피드백 부탁드림다)
Abstract 더 많은 층을 가진 신경망 알고리즘의 학습을 위해 Residual Learning을 사용한다. 이 모델은 기존보다 더 낮은 오류를 발생시키며, 더 효율적이다.
설명: 층과 층사이 relu 등의 활성화 함수를 통해 학습이 진행되는 기존 모델. 거기에 층을 뛰어넘는 원래값 identity를 추가, 원래함수는 f(x)지만, 이과정 거치면 아이덴티티 x를 더해 f(x) + x가 됨. (이를 이용하면 층별 독립성이 조금은 줄어들어 과대적합을 방지할 수 있을것)개인적생각. 
기존 모델에 비해 층이 적을때는 차이가 적지만, 층이 많아질수록 서로의 독립성이 사라져 오류확률이 줄어듬.
결론, resnet이 기존 모델보다 효율적이다!

* <strong>현석</strong>: resnet 논문 커멘트 neural networks 가 깊어 질수록 성능은 좋아지지만 train이 어렵다 따라서 잔차를 이용하여 잔차학습(residual learning)을 이용하여 깊은 신경망에서도 training이 쉽게 이뤄진다는 것이 정말 신기했다

# [Attention Is All You Need(문경환)](../pdfs/Attention_is_all_you_need.pdf)
> * hi

# [SupCon-MPL-DP: Supervised Contrastive Learning with Meta Pseudo Labels for Deepfake Image Detection(문경환)](../pdfs/supcon_mpl.pdf)
> * 스터디 발표회 추가 세미나
