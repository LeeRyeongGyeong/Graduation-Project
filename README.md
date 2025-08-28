# 인공지능을 활용한 표준 의료 빅데이터 기반 맞춤형 정밀 치료 지원 시스템 개발
1. 배경 : 병원 간 의료 데이터의 비표준화와 그 형식의 차이로 인한 질병 진단의 불편함이 존재
2. 목적 : 당뇨병 맞춤형 정밀 치료 지원 시스템 개발
3. 사용한 기술(언어) : Python, 머신러닝 알고리즘(XGboost), HTML, CSS, JavaScript
4. 결과 : 당뇨 진단에 가장 빈번하게 사용되는 검사 수치와 약물 정보를 활용, 환자 상태 예측 결과를 출력

# 목표
1. 특정 질환에 대한 예후 예측을 위해, 병원 내 환자 빅데이터를 수집하고, 빅데이터 전처리, 통계적 분석, 인공지능 알고리즘 등을 적용하여, 정밀진단 및 치료를 구현하고자 함.
2. 가지고 있는 데이터를 통해 학습된 모델로 웹사이트 구축하여 사용자가 직접 자신의 의료 정보를 통해 예후를 예측할 수 있도록 하고자 함.
3. 이후, 당뇨병뿐만 아니라 다른 질환에 대한 데이터를 추가하여 다른 질환의 예후 또한 예측할 수 있도록 다양성을 늘리고자 함.
4. 본 프로젝트에서는 당뇨병콩팥병증에 대해 인공지능과 접목하여 합병증을 예측하는 웹 사이트를 구축하는 것을 목표로 함.

# 프로젝트 요약
 당뇨병 환자의 기본 정보, 검사 정보, 복용 약물 정보 등의 데이터를 수집하여 검증, 품질 파악 후 전처리 과정을 거쳐 데이터베이스에 적재함. 적재된 데이터를 통해 머신러닝 알고리즘으로 환자의 상태를 예측하기 위해 지도 학습 중에서  Decision tree, Random forest, GBM, SVM, XGBoost와 같은 5가지 알고리즘을 사용하여 최상의 성능을 보여주는 모델로 결정하기로 함. 적용한 결과로 XGBoost의 성능이 가장 높았으므로, 해당 모델에서 Feature imfortance 5개를 추출하여 최종 모델에서는 5가지 특징으로 구성된 모델을 사용함. 

 최종 모델을 사용하여 사용자의 검사 & 약물 데이터를 입력받아 그에 해당하는 환자의 상태를 예측하여 결과로 출력해주기 위한 시각화 도구로 웹 사이트(Medical Data Analysis system)를 구축함. 해당 웹 사이트에서는 ACR(Albumin Creatinine Ratio), Insulin Glargine, Insulin Lispro, Pioglitazone, Repaglinide와 같은 검사 수치나 약물 복용 여부(0 또는 1)와 같은 값을 입력하면 학습한 모델의 분류 알고리즘을 통해 해당 정보를 가진 환자가 당뇨병콩팥병증에 걸릴 확률을 출력해 줌. 환자가 1명이 아니라 2명 이상일 경우, 웹 페이지의 Tutorial 페이지에 제시된 형식에 맞게 파일을 제작하여 업로드 하면 그에 맞는 결과를 웹 페이지에서 표로 결과를 볼 수 있으며 또한, csv 파일로 다운로드 받을 수 있음.

# 프로젝트를 통해 얻어지는 최종 결과물 
1. 당뇨병 환자의 의료 정보를 활용하여 당뇨병콩팥병증을 예측하는 인공지능 모델
2. 모델을 통해 예측된 결과를 시각적으로 사용자에게 알려주는 웹 사이트


# 작품 실행 장면
<img width="434" height="353" alt="image" src="https://github.com/user-attachments/assets/66596730-a1e9-43d0-aa30-9f9203c5fb83" />
Medical Data Analysis system(MIDAS) 메인 화면 
<img width="426" height="205" alt="image" src="https://github.com/user-attachments/assets/8d2cbc92-b6c1-488a-a823-ceb0aad6b956" />
메인 화면의 상단바에서 About → Information 클릭 시
머신러닝 알고리즘에 사용되는 데이터와 XGBoost 모델의 성능 정보를 알려주는 페이지
<img width="407" height="323" alt="image" src="https://github.com/user-attachments/assets/d944f740-f2ab-4fdf-b4e4-f2c6b7f42657" />
메인 화면의 상단바에서 About → Tutorial 클릭 시
MIDAS 웹 페이지의 사용법을 알려주는 페이지 
<img width="422" height="277" alt="image" src="https://github.com/user-attachments/assets/05d3a40b-5b4c-4a79-a35f-f1907ee7376f" />
메인 화면의 상단바에서 Members
: 프로젝트에 참여한 팀원 소개 페이지
<img width="392" height="389" alt="image" src="https://github.com/user-attachments/assets/909208cf-fda1-4e44-a9d4-8de91b916748" />
메인 화면의 상단바에서 About -> Predict :
머신러닝 알고리즘을 통해 만들어진 질환 예측 시스템이 구현된 시스템
<img width="340" height="536" alt="image" src="https://github.com/user-attachments/assets/0c648679-67c2-48e3-b08e-5a6be31e5786" />
메인 화면의 상단바에서 About -> Predict :
한 명의 대한 검사 정보와 약물 복용 여부를 입력 후 Predict 버튼을 눌러 예측한 페이지
<img width="426" height="633" alt="image" src="https://github.com/user-attachments/assets/792beb3b-5197-4c44-a5e0-0a71a78b41fe" />
메인 화면의 상단바에서 About -> Predict :
두 명 이상에 대한 파일 정보를 업로드 한 후 Predict 버튼 클릭하여 예측된 화면을 띄워주는 페이지



