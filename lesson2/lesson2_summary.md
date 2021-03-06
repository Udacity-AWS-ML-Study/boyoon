



## What is Machine Learning



## Supervised Learning vs. Unsupervised Learning vs. Reinforcement Learning

신기한게 강화학습을 따로 떼서 설명한다. reward를 키우는 방향으로 학습하니까 확실히 unsupervised learning 도 아닌 것 같다.



강아지를 훈련시키는 것과 비슷하다. 잘 하면 간식을 주고, 잘못하면 혼내는 식으로 학습한다. 



## Traditional Problem Solving vs. Machine Learning



## Machine Learning의 모델

* Machine Learning Model
* Model Training Algorithm
* Model Inference Algorithm



Machine Learning Model: generic program, made specific by data

Model Training Algorithm: make small changes to the model to fit your problem

Model Inference Algorithm: Using a trained model to predict data



이렇게 세 단계로 생각해 본 적은 없는데, 진짜 training algorithm도 엄청 중요할 것 같다. 

<br>

## Steps of machine learning

![steps_of_ml]() #nlp 폴더 안에 있음


<br>

## Step 1: Define the Problem

* 자세하게 정의하기
* 어떤 ML Task인지 생각해보기 : Supervised vs. Unsupervised


<br>

## Step 2: Build a Dataset

데이터 분석의 80%는 데이터셋을 준비하는 과정

* 데이터셋 구축의 단계들: Data Collection, Data Inspection, Summary Statistics, Data Visualization

* Data Inspection: outliers, Missing or incomplete data, Transform your dataset

* Summary Statistics을 통해 Trends in the data, Scale of the data, Shape of the data를 알 수 있다.

  <br>

## Step 3: Model Training

* Splitting Dataset: 훈련 전에 train dataset, test dataset으로 데이터셋을 나눠야 함

* Model training algorithm이 하는 일: Iteratively update **model parameters** to minimize loss function

* model parameters: 모델이 어떻게 작동하는지를 정의함

* Loss Function: 모델이 목표와 얼마나 가깝게 예측하는지를 측정

* 그 외...: hyperparameters 설정, Be prepared to iterate(model training은 정확한 과학이라기 보다는 시행착오를 통해 답을 찾아가는 과정)

<br>

## Step 4: Model Evaluation

* 평가지표를 통해서 모델이 제대로 만들어졌는지를 평가하는 단계.
* 모델이 제대로 만들어지지 않았다면 다시 그 전단계들로 돌아가서 수정한다.

* 대표적인 평가지표: Accuracy, F1 score, Log Loss, Precision, Mean Absolute Error


<br>

## Step 5: Model Inference

한번도 못 봇 데이터를 예측할 때 사용

결과를 계속 모니터하기

<br>

---

## Case study

### 1. House price prediction

1) Define the Problem

2) Building a Dataset: Data collection, Data exploration, Data cleaning, Data visualization

3) Model Training 

A linear model across a single input variable can be represented as a line. It becomes a plane for two variables, and then a hyperplane for more than two variables. The intuition, as a line with a constant slope, doesn't change.

4) Evaluation

RMSE

5) Inference

---
 
