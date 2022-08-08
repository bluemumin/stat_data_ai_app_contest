# stat_data_ai_app_contest
SDC 통계데이터 인공지능 활용대회(자연어 기반 인공지능 산업분류 자동화)의 데이터를 제외한 코드입니다.

[대회 사이트](https://data.kostat.go.kr/sbchome/contents/cntPage.do?cntntsId=CNTS_000000000000575&amp;amp;curMenuNo=OPT_09_03_00_0)

등수 : 58등/395팀 [팀 수 확인 출처](https://www.boannews.com/media/view.asp?idx=106557)

<img data-action="zoom" src='{{ "/등수.PNG" | relative_url }}' alt='absolute'> 

방식 : tokenizer 수행 -> 명사 추출

-> 대분류(19종류), 중분류(74종류), 소분류(225종류) 각각 모델 생성해서 학습

목적 : 

1.LSTM 모델 기반, 다양한 전처리를 통한 NLP 기법 공부

2.BERT 모델 코드 공부를 위한 기본 과정 학습용