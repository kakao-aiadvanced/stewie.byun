# stewie.byun 의 AI 학습용 저장소

아무거나 끄적임

## Day1
Deep Learning to LLM

치와와 vs 머핀

머신 러닝 vs 딥 러닝

머신 러닝 : 피쳐를 직접 선택해야 함

딥 러닝 : 피쳐를 자동으로 선택함
- 데이터로부터 Representation Learning을 함

Drop Out
- 뉴런을 랜덤하게 삭제하여 과적합을 방지함

Self-Attention

Incontext Learning
- 모델이 프롬프트를 통해 학습을 함

Learning(학습) vs Inference(추론)
- Inference는 모델이 학습을 하지 않고 예측을 함
- Learning은 모델이 학습을 함
- Inference 에서는 파라미터가 업데이트 되지 않음

Attention is all you need
- 모델이 프롬프트를 통해 학습을 함
- 프롬프트 없이 학습을 함

Reinforcement Learning(강화학습)
- 모델이 프롬프트를 통해 학습을 함
- 최종 상벌은 있지만, 중간 과정은 없는 경우 사용

어떤 모델을 써야 할까?
- 리더보드 1등 모델을 쓰자
- 큰 모델 부터 작은모델로 줄여나가자
  - 큰 모델도 나중에 점점 저렴해진다.

128k 토큰 = 약 책 1권

토큰이 길어질수록 attention 이 떨어짐
= 간결한 프롬프트를 작성하는 것이 중요

비용은 어느정도의 컨텍스트를 제공해야 하는지 고려해봐야함

Prompt Engineering

Least to Most Prompting(최소에서 최대로)
- 모델이 최소한의 정보로 최대한의 성능을 내도록 유도

모델이 커지면, 프롬프트 엔지니어링이 덜 중요함


