# stewie.byun 의 AI 학습용 저장소

아무거나 끄적임

## Day3

Benchmarks
- 어뷰징의 가능성이 있음
- MMLU: Multiple-chice questions in 57 subjects
  - 80% 후반 모델을 선택 
- 'Golden Dataset 으로 테스트' 하는 것이 좋음


## Day2

RAG(Retrieval Augmented Generation)

> 기술은 왜 쓰고 언제 쓰는지 아는 것이 중요

- RAG는 검색을 통해 정보를 가져와서 생성하는 모델
- 민감한 개인정보를 다루는 경우, RAG를 통해 검색을 통해 정보를 가져오는 것이 좋음
- 임베딩도 파인튜닝이 필요함 (유사도 계산을 위해, ex 윤석렬 과 계엄)

LangChain
- 웹페이지를 긁어오는 등등의 로더들을 제공
  - WebBasedLoader
  - PDFLoader

RAG Splitter
- 한 문단이 이상적으로 판단될 경우, 두 세 문단으로 테스트 해보고,
- 조금씩 줄여나가면서 테스트 해보는 것이 좋음

Vector Store
- 검색을 위한 벡터 저장소
- KNN: K-Nearest Neighbors
  - 유사도를 계산하여 가장 가까운 벡터를 찾아냄
- ANN: Approximate Nearest Neighbors
  - 유사도를 계산하여 가장 가까운 벡터를 찾아냄
  - ANN은 KNN보다 빠르지만, 정확도가 떨어짐
  - 1등(=최고) 을 찾아줄 필요가 없을 때 사용
- 시멘틱
  - 반대는 '키워드' 서치 (대부분 BM25 를 사용) 
  - cf SQL
  - 하이브리드 형태로 사용 (pgVector)

프롬프트 작성 방법
- Edge 케이스의 테스트 케이스를 준비
- 프롬프트를 작성하고, 테스트 케이스를 통과하는지 확인

HyDE
- Q 에 대한 LLM 의 A 를 생성
- 위 A 를 임베딩해서 그 근처 데이터를 Retrie 하는 것
- 잘 되지만 비싸다

> '정의' 와 '쓰임'과 '특징'을 알려줘

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


