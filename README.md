# agricultural_products_price_forecast

> 기간

2020/09 ~ 2020/12

> 프로젝트 간략 소개 한 문장

LSTM을 이용한 농산물 가격 예측

> 실행 환경

Jupyter Notebook

> 사용한 데이터

![use_data](/image/use_data.PNG)

- kamis(open api)
  - 가격 데이터 : 일별 가격데이터
  - 유통비용 데이터 : 연도별 가격 데이터

- 농식품수출정보(csv)
  - 수입수출 데이터(kg, $): 월별 데이터

- 기상청 기상자료개방포털(csv)
  - 날씨 데이터 : 일별 날씨 데이터

- 농업관측 통계정보시스템(OASIS)(csv)
  - 공급량 데이터(kg) : 일별 데이터

- 국가통계포털(csv)
  - 생산량 데이터(t) : 연도별 데이터
  - 소비자 물가지수 : 월별 데이터

## EDA

> 날씨와 생산량의 상관관계

![cor_plot](/image/output_temp.PNG)

> 사과

![cor_plot](/image/apple_cor_plot.PNG)


> 양파

![cor_plot](/image/onion_cor_plot.PNG)


> 대파

![cor_plot](/image/greenonion_cor_plot.PNG)

## 분석 이용 데이터

> 사과
- 최저기온
- 평균기온
- 최고기온
- 유통비용
- 생산량

> 양파
- 유통비용
- 수입(중량)
- 수입(금액)
- 생산량

> 대파
- 평균기온
- 최저기온
- 최고기온
- 생산량


## 핵심 기능
- 사용자 기반 협업 필터링은 사용자가 평가한 영화 평점과 다른 사용자의 영화평점간의 유사도를 비교하여 유사도가 높은 사용자가 높게 평가한 영화를 사용자에게 추천해주는 알고리즘 입니다.

