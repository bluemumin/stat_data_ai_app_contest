# stat_data_ai_app_contest
SDC 통계데이터 인공지능 활용대회(자연어 기반 인공지능 산업분류 자동화)의 데이터를 제외한 코드입니다.

## 1. Competition - SDC 통계데이터 인공지능 활용대회

  - Member : 김경록

  - Status : Complete
  
  - Tag : Competition

  - 사용언어 : Python(3.9)
  
  - 핵심 라이브러리 : Konlpy(komoran), keras(Sequential 기반 LSTM)

## 2. Why

통계청에서의 대/중/소 산업분류를 

NLP 기반, 자동화 할 수 있는 예측 모델 생성

## 3. Data

[대회 데이터 제공] 산업분류 구분 및 예시 문장 / 세부 분류 코드 구분 항목 

[대회 사이트](https://data.kostat.go.kr/sbchome/contents/cntPage.do?cntntsId=CNTS_000000000000575&amp;amp;curMenuNo=OPT_09_03_00_0)

(데이터 외부 유출 금지 -> 미 업로드, 관련 결과 삭제)

## 4. 분석 방법

 (a). Data Preprocessing
 
	- EDA : train 데이터 간 중복 여부 확인 완료, 사용 문장 현황 확인 완료
	
	- Data Reduction : 특수 문자, 불용어 제거
	
	- 명사 추출 : Konlpy 패키지 중 koroman 사용 (비교대상 : kkma) 
	
	- 사용 시도 : 맞춤법 교정, 띄어쓰기 교정 등 사용 (--> 시간 대비 개선 사항 없어서 미 사용)
	
 (b). Model & Algorithms
 
	- LSTM 기반 대/중/소 분류 각각 모델 사용 (비교 대상 : bi-lstm, bn & cnn-lstm)
	
	- 사용 시도1 : 소분류 oversampling, 이전 분류와 동일할 경우 선택(RuleBase 추가), 
	
	추가 데이터 사용(한국표준산업분류), 중복 데이터 제거, class_weight 부여
		 
	- 사용 시도2 : Bert 모델 사용
	
 (c). Report & Review
 
	- 최종 등수 : (58등/395팀) / accuracy : 88.57% / F1-score : 0.765
	
	- 긍정적 사항 : Bert 모델 사용 시도 및 NLP 모델 생성을 위한 다양한 시도 수행
	
	        자연어 전처리를 위한 패키지 사용 및 비교 과정을 통한 과정 수행 기록
	
	- 피드백 : label이 많을 경우에 대한 예측 방식 search 필요, 
	
	    	 Sequential 모델 제외한 다른 모델 습득 기회 필요, 
			  
		  Bert 모델 기본 사용 가능 → 응용 방법 습득 필요
		  
[팀 수 확인 출처](https://www.boannews.com/media/view.asp?idx=106557)

![](https://github.com/bluemumin/stat_data_ai_app_contest/blob/main/%EB%93%B1%EC%88%98.PNG)
