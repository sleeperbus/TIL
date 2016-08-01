# Predicting Signups
trial 서비스를 사용하는 유저가 정식 서비스로 전환할지 판단할 때 여러 가지 지표들이 사용될 수 있다. 
* 유입경로 
* FAQ 를 읽었는가?
* 사이트에서 읽어들인 페이지
* 기타 등등 

# Introducing Decision Trees
linear regression 이나 NN 은 결과가 왜 그런 결과가 나왔는지 알기 어렵다. Decision Tree 는 중간 과정을 알 수 있기 때문에 이런 면에서 좋다.

# Training the Tree
이 챕터에서는 CART(Classification and Regression Tree) 알고리즘을 사용한다.

# Choosing the Best Split
데이터를 binary tree 형식으로 계속 나눠간다. 매 split 이 일어날 때부터 cost 가 줄어야 하는데 이 cost 를 측정하는 여러 방법이 있다.
## Gini Impurity
[지니불순도](https://ko.wikipedia.org/wiki/%EA%B2%B0%EC%A0%95_%ED%8A%B8%EB%A6%AC_%ED%95%99%EC%8A%B5%EB%B2%95#.EC.A7.80.EB.8B.88_.EB.B6.88.EC.88.9C.EB.8F.84)는 한 집합에서 임의로 추출한 값에 집합의 distinct 한 값 중 하나를 할당했을 때 오류일 확률을 말한다. 
## Entropy
엔트로피는 정보이론에서 무질서도를 뜻한다. 공식은 다음과 같다. 
* p(i) = 특정분류가 나올 확률 
* Entropy = sum(p(i) * log(p(i))) for all outcomes

# Recursive Tree Building
entropy 가 가장 낮아지는 feature 의 value 로 집합을 두 개로 나눈다. 두 집합을 각각의 root 로 삼는 트리를 recursive 하게 만든다. 
# Displaying the Tree

# Classifying New Observations

# Pruning the Tree
mingain 값을 사용해서 두 개의 leaf node 를 하나로 합칠 수 있다. 
# Dealing with Missing Data 
observation set 을 분류하는 중, 기준이 되는 feature 의 value 가 누락됐을 수도 있다. 이 때는 수정된 classify 함수가 필요하다. 틀리의 왼쪽, 오른쪽 결과를 모두 가져온 후 결과값을 가중평균한다. 
# Dealing with Numerical Outcomes
예측하려는 결과값이 숫자일 때 평가함수에 variance 를 사용할 수 있다. 분산값을 사용해서 데이터가 퍼져있는 정도를 줄일 수 있다.
# Modeing Homes Prices

# When to Use Decision Trees
