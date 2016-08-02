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

# Weighted Neighbors

## Inverse Function
## Subtraction Function
## Gaussian Function
## Weighted Function
## Weighted kNN
# Cross-Validation
# Heterogeneous Variables
## Adding to the Dataset
## Scaling Dimensions
# Optimizing the Scale
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
