
![main](/image/main.PNG)
# agricultural_products_price_forecast

> 기간

2020/09 ~ 2020/12

> 프로젝트 간략 소개 한 문장

LSTM을 이용한 농산물 가격 예측

> 실행 환경

Jupyter Notebook

## 문제 인식
농산물의 가격은 비농산물의 가격과 비교해 높은 변동성을 가지고 있습니다. 
농산물의 생산지는 기상환경때문에 재배지가 한곳에 집중 되어있는 상품이 많습니다. 
대규모 재배단지에 집중호우나 저온현상, 가뭄 등의 자연재해가 발생하면 농산물의 생산량에 타격을 받아 가격변동이 있을 수 있습니다.
이러한 점은 소비자 입장에서는 구매의 부담을, 생산자 입장에서는 수입의 불안정성을 유발합니다.
이러한 문제점을 해결하기 위해 농산물 물가 예측 프로젝트를 주제로 선정하여 진행했습니다.
## 분석 주제
- 농산물의 생산량과 날씨는 상관관계를 가지는가
- 농산물의 가격에 상관관계를 미치는 변수는 무엇인가
- 농산물의 가격 예측

## 프로젝트 구조
1. EDA를 통한 변수 선택
2. Prophet분석
3. LSTM분석(순환신경망 모델)

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

## 1. EDA를 통한 변수 선택

> 날씨와 생산량의 상관관계
<img src="https://github.com/sesame86/agricultural_products_price_forecast/blob/main/image/output_temp.PNG?raw=true" width="70%"/>

> 사과 🍎

![apple_cor_plot](/image/apple_cor_plot.PNG)


> 양파 🧅

![onion_cor_plot](/image/onion_cor_plot.PNG)


> 대파 🥬

![greenonion_cor_plot](/image/greenonion_cor_plot.PNG)

## 이용할 변수

> 사과 🍎

- 최저기온
- 평균기온
- 최고기온
- 유통비용
- 생산량

> 양파 🧅

- 유통비용
- 수입(중량)
- 수입(금액)
- 생산량

> 대파 🥬

- 평균기온
- 최저기온
- 최고기온
- 생산량

##2. Prophet분석

> 사과 🍎

> 양파 🧅

> 대파 🥬

##3. LSTM분석

> 사과 🍎

![apple_lstm](/image/apple_lstm.PNG)
<img src="https://github.com/sesame86/agricultural_products_price_forecast/blob/main/image/apple_score.png?raw=true" width="30%"/>

시각화해서 확인해보면 예측이 뒷부분으로 갈수록 어긋나는 부분이 있지만 나머지 부분에서는 가격의 트렌드를 따라가는 것을 확인할 수 있습니다.

> 양파 🧅

![onion_lstm](/image/onion_lstm.PNG)
<img src="https://github.com/sesame86/agricultural_products_price_forecast/blob/main/image/onion_score.png?raw=true" width="30%"/>

시각화해서 확인해보면 예측이 뒷부분으로 갈수록 어긋나는 부분이 있지만 나머지 부분에서는 가격의 트렌드를 따라가는 것을 확인할 수 있습니다.

> 대파 🥬

![greenonion_lstm](/image/greenonion_lstm.PNG)
![greenonion_score](/image/greenonion_score.png)

## 핵심 기능
- 농산물은 통제 불가능한 기상 여건에 따라 생산량의 편차가 큰 수준이기 때문에 날씨와 생산량의 상관관계를 통해 농산물에 중요한 날씨 변수가 무엇인지 확인할 수 있습니다.

- 생산량, 공급량, 수출수입, 소비자 물가, 유통비용 데이터들과 가격의 상관관계를 통해 농산물 가격에 영향을 미치는 변수를 선택할 수 있습니다.
