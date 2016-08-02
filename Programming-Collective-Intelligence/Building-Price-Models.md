# Building a Sample Dataset
* rating 과 age 을 입력으로 받는 wineprice 함수는 정확한 가격을 산출
* 랜덤 데이터를 생성하는 wineset1() 함수는 wineprice 를 호출하기는 하나 noise 를 더해서 가격의 신빙성을 떨어트리면서 data set 을 생성

# k-Nearest Neighbors
새로운 와인의 가격을 산출하기 위해서 기존의 데이터를 사용한다. vector distance 가 가장 가까운 것 몇 개를 골라서 평균 가격을 와인의 가격으로 정한다. 
## Number of Neighbors
문제는 기존의 data set 에서 몇 개의 데이터를 골라서 평균으로 삼느냐는 것. 
## Defining Similarity
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
