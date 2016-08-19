# Matchmaker Dataset 
# Difficulties with the Data 
# Basic Linear Classification
각 분류값의 평균점을 구한다. 신규 데이터가 주어지면 평균점과 신규 데이터간의 벡터 내적을 구한 후 큰 값으로 분류시킨다.  
![1](http://d.pr/i/16RcX+)
# Categorical Features
## yes, no data 
1 또는 -1 로 변환한다. 
## 남자, 여자의 관심목록 
공통된 관심사의 개수만 센다. 

# Scaling the Data
데이터간의 척도가 다르면 큰 척도의 feature 들이 결과값을 좌우할 수 있다. 따라서 0과 1사이의 동일한 값들로 변형해야 한다. 

# Understanding Kernel Methods
데이터 그룹들을 선형으로 나눌 수 없을 때 kernel trick 을 사용해서 dimension 을 높여서 분류할 수 있다. 
![2](http://d.pr/i/1exfD+)
# Support-Vector Machines
주어진 데이터에 최적화시키면 새로운 데이터에 대해서 이런 일이 발생한다.  
이 때 SVM 은 분류와 데이터 사이에 일정한 margin 을 만들어서 데이터를 분류시키켜 준다.
![3](http://d.pr/i/ilc4+)

# Using LIBSVM
# Matching on Facebook
