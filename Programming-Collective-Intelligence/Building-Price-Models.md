# Building a Sample Dataset
* rating 과 age 을 입력으로 받는 wineprice 함수는 정확한 가격을 산출
* 랜덤 데이터를 생성하는 wineset1() 함수는 wineprice 를 호출하기는 하나 noise 를 더해서 가격의 신빙성을 떨어트리면서 data set 을 생성

# k-Nearest Neighbors
새로운 와인의 가격을 산출하기 위해서 기존의 데이터를 사용한다. vector distance 가 가장 가까운 것 몇 개를 골라서 평균 가격을 와인의 가격으로 정한다.  

보통 knn 을 이야기 하면 데이터를 분류하는 관점이다. data set 을 k개의 분류로 나누는 것인데 이 책에서는 k개의 가까운 data point 의 값을 평균해서 가격을 산출한다. 숫자를 추정하는 것이다. 
## Number of Neighbors
문제는 기존의 data set 에서 몇 개의 데이터를 골라서 평균으로 삼느냐는 것. 
* 너무 적은 데이터를 사용해서 평균을 내면 가격 편차가 커질 수 있다.
* 너무 많은 데이터를 사용해서 평균을 내면 관계 없는 가격들이 많이 들어있어서 가격이 희석될 수 있다. 
* 결국은 적당한 숫자를 고르는 것이 중요하겠다.

## Defining Similarity
vector 간의 유사도를 구하기 위해 제일 흔한 방법을 쓴다. 
* euclidean distance 

## Code for k-Nearest Neighbors
책에 코드가 잘 구현되어 있다...

# Weighted Neighbors
입력된 vector 와 가장 가까운 k개의 데이터를 가져왔을 때 이들의 산술평균을 구하는 것은 불공평할 때가 있다. k개의 가격이 비슷하면 괜찮지만 차이가 난다면 정확도가 떨어진다. 이를 위해 각각의 가격에 가중치를 둔다. 가중치의 기준이 되는 것은 입력된 vector 와의 distance 이다.
## Inverse Function
가중치를 1/d 로 설정한다. 이 때 d 가 엄청 작다면 가중치가 엄청 커지기 때문에, 1/(d+0.1) 정도로 적당하게 설정한다. 단점은 가중치의 편차가 너무 크다는 것이다. 
## Subtraction Function
정해진 숫자에서 distance 를 뺀다. 
## Gaussian Function
가우스 함수, 그런데 이 책에서 나오는 가우스 함수는 약간 이상하다. 가우스 함수에는 표준편차가 들어가야하는데 그러려면 전체 집합에 대한 정보가 필요하지만 여기에서는 sd 대신 특정 상수를 사용한다. 

## Weighted kNN
가중치 평가함수를 사용해서 평균을 구하는 함수를 작성한다. 

# Cross-Validation
## 일반적인 CV 
1. 데이터를 train set 과 test set 으로 나눈다.
2. train set 을 model 에 던져서 parameter 를 얻는다. 
3. 설정된 parameter 의 model 에 test set 을 던져서 오차를 구한다. 
4. 위의 과정을 반복해서 오차가 작은 parameter 를 선택한다.

## 여기에서 쓰인 CV
1. 데이터를 train set 과 test set 으로 나눈다. 
2. train set 을 기존의 데이터 묶음으로 보고 알고리즘과 test set 의 데이터를 하나씩 던져서 결과값을 얻은 후 이것의 오차율을 더한다.
3. 각 알고리즘마다 위의 행동을 반복해서 최적의 알고리즘을 구한다. 

여기서 쓰이는 방식은 model 의 parameter 를 구한다기보다는 데이터에 적합한 알고리즘을 구한다. 
# Heterogeneous Variables
각 feature 간의 축적이 다를 때는 해당 축적의 범위를 맞춰주어야 한다. 일반적으로 이런 과정을 Normalization 이라고 한다. 통계적으로 각 feature 들의 값들을 손쉽게 변형할 수 있으나 여기에서는 약간 다른 방식을 사용한다. 
## Adding to the Dataset
## Scaling Dimensions
rescale 이라는 함수를 작성한다. 이 함수는 data 와 scale 이라는 list 타입을 받아들인다. sclae 에는 각 feature 의 배율이 담겨져 있어서 이 배율을 사용해서 데이터를 변경한다. 
# Optimizing the Scale
scaling 변수 최적화. 통계적으로 해결하지 않고 앞 단락의 optimizing 기법들을 사용해본다. 
# Uneven Distributions
## Estimating the Probability Density
## Graphing the Probabilities
# Using Real Data - the eBay API
## Getting a Developer Key
## Setting Up a Connection
## Performing a Search
## Getting Details for an Item
## Building a Price Predictor
# When to Use k-Nearest Neighbors
