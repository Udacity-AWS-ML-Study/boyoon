
## Machine Learning with AWS



### AI Services 예시

* Amazon Transcribe Medical: Health AI, medical 스피치를 텍스트로 변환, 음성 인식(ASR 서비스)

타겟층: 의사 - 텍스트로 증상 적는 데 드는 시간에 환자들에게 더 많이 신경 쓸 수 있음.

* Amazon Monitron: industrial AI
* Amazon Lookout for metrics: anomaly detection
* Amazon Lex: chatbot, public voice or text bots
* Amazon Personalize: highly customized recommendation
* Amazon Forecast: 예측 모델
* Amazon Fraud Detector: 사기, 횡령 등 검출
* Amazon Codeguru & Develops guru : 코드 퀄리티 개선, 가장 비경제적인 코드를 찾아줌.

* Amazon Rekognition: Vision
* Amazon Polly: 음성합성
* Amazon Translate & Amazon Textract: OCR 후 번역
* Contact Lens: 고객 문의 사항 듣고 감정 분석, 문제 분류
* Amazon Kendra: 비정형 데이터에서 검색 가능



## Amazon Sagemaker

1. Amazon Sagemaker Studio: 모델 생성, 훈련, 배포까지 가능. scalable
2. Amazon Sagemaker Distributed Training: 분산 훈련도 지원. 자동으로 모델과 데이터를 파이션해줌.
3. Amazon Sagemaker Clarify: ML workflow의 bias를 검출해주고 모델 설명해줌



---

## Computer Vision 

1. Computer Vision : 기계가 이미지와 비디오에서 패턴을 인식하고 고수준에서의 이해를 할 수 있게 하는 분야
2. 기대효과: 생산성 향상, 창의적 문제 해결

딥러닝 이전의 CV: use case에 한정되어 있었음. 일일이 그림의 피처를 annotate했어야 했음

인공신경망 구조

input layer

hidden layer: 숨어있는 중요 피처들을 찾음. 각 레이어별로 다른 특성들을 찾음.

초기 레이어: Edge detection 등 베이직 패턴을 찾음. 그 후 깊어질 수록 텍스처 등의 특징 찾고 이렇게 찾은 고수준 특성은 output layer에 들어가서 분류됨

output layer



## Use cases

* Image Classification: text detection이나 OCR(Optical Character Recognition), content moderation
* Object detection: 다양한 오브젝트를 검출. 오브젝트가 여러 개 있으면 여러 개 검출
* Semantic segmentation: 픽셀 단위로 오브젝트 검출. 오브젝트의 위치를 알려줌
* Activity recognition : video



---



# AWS DeepLens

아쉽게도 DeepLens device가 있어야 이 서비스를 제대로 이용할 수 있다!

그래서 이번 단원에서는 AWS를 이용한 분석에 도움되는 정보들만 적어봐야겠다.

* 데이터 수집: 데이터를 수집해서 AWS S3에 적재한다
* 모델 훈련: Amazon sagemaker 안의 주피터 노트북을 이용해서 모델을 훈련한다.
* 모델 배포: AWS Lambda를 이용해서 기기에 배포한다.
* 모델 결과 확인 : Amazon IoT Greenrass를 이용해 배포된 모델의 결과를 확인한다.

!!! 모델 훈련 후 모델 저장하고 세션 clear해야 함. 버켓도 지워야하고, sagemaker 노트북도 지워야함. 그래야 돈이 안나감.



Lambda : function을 만들어서 모델 inference 가능하게 해줌.



---



# AWS DeepRacer

* 요소: Agent, Environment, State, Action, Reward, Episode

* Agent: 우리가 훈련시키는 소프트웨어. 환경 속에서 목표 달성하기 위해 행동함
* Environment: 에이전트가 상호작용하는 환경. Deepracer에서는 트랙이 환경
* State: The state is defined by the current position within the environment that is visible, or known, to an agent. DeepRacer에서는 카메라로 찍은 이미지. initial state는 트랙의 스타팅 라인, terminal state는 랩이 끝나고 장애물
* Action : 에이전트가 취할 수 있는 행동. 직진, 우향, 좌향 등
* Feedback: 주어진 환경에서 에이전트의 행동에 따른 피드백이 주어짐. 수치의 reward의 형태로 주어짐. 
* Episode: a period of trial and error 



Training algorithm: learning objective를 정의함 ― maximize total cumulative reward.



AWS DeepRacer reward 그래프

![]()



---

# Generative AI



* discriminative model : 분류하는 모델
* generative model : 생성하는 모델



**유명 모델**

GANs

AR-CNN: Autoregressive models : data evolves over time 

Transformer-based models : data with sequential structure



## Deep Composer

GANs: add accompaniments

AR-CNN : enhance melody

Transformer: extend melody







----


