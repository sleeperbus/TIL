# A Corpus of News
여러 뉴스사이트에서 rss 를 통해 기사들을 긁어온다. 이렇게 긁어온 기사들은 세 개의 자료형으로 저장된다.
* all words: {단어: 등장회수} dictionary 
* article words: 각 기사의 {단어, 등장회수} list 
* article titles: 각 기사의 제목 list  

위 자료들을 사용해서 wordmatrix 를 만든다.  
## word matrix 
등장회수와 출현 비율 조건을 만족하는 단어로 중첩 list 를 만든다. 단어목록이 love, world, hello 이고 기사가 3가지라면 다음과 같이 표현된다. 
```
[[0, 1, 1], [1, 2, 1], [2, 1, 0]]
```
# Previous Approaches
앞 챕터들에서 다루었던 방법들을 적용해본다. 
## Bayesian Classification
각 단어에 가중치를 주는 방법을 사용한다. 이 방법은 사전에 label 이 된 데이터로 train 이 필요하다. label 개수가 많다면 적합하지 않을 수 있다. 
## Clustering 
wordmatrix 에서 각 vector 간 거리를 구해서 hclust 를 시켜본다. 

# Non-Negative Matrix Factorization 
A * B = word matrix 가 되는 A, B 를 구하는 것이 목적이다. 수학적인 과정이 들어가기 때문에 자세한 내용은 생략 
# Displaying the Results
# Using Stock Market Data
