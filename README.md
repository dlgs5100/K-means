# K-means and K-means++

## Introduction:
機器學習相較於傳統由程式設計師訂定方法，而是透過以往的規則或是資料，使機器自行找到其運行規則。而其演算法分為四類，監督式學習、非監督式學習、強化學習以及遷移學習。本篇採用是非監督式學習中的K-means分群法以及其改善方法，並以UCI中的Iris和Abalone為測試資料集。

## Method:
a) K-Means
1.	預設群數量。
2.	隨機初始化K個群中心。
3.	計算所有資料點分別到K個群中心距離，每個資料點依序從K個距離中選最短距離，代表該資料點屬於該群。
4.	透過該群所有資料成員，重新計算出重心，並以此為該群新的群中心。
5.	重複步驟3到5，直到所有資料點不再變動其所屬群，或達到初始設定最大次數上限。

b) K-Means++
1.	預設群數量，初始化N為1。
2.	隨機初始化1個群中心。
3.	計算所有資料點到所有群中心的距離，每個資料點從N個距離中選最短距離並給予機率權重。
4.	透過機率權重以及輪盤法，求得新的群中心，N加1。
5.	重複步驟3到5，直到N等於K。
6.	計算所有資料點分別到K個群中心距離，每個資料點依序從K個距離中選出其最小，代表該資料點屬於該群。
7.	透過該群所有資料成員，重新計算出重心，並以此為該群新的群中心。
8.	重複步驟6到8，直到所有資料點不再變動其所屬群，或達到初始設定最大次數上限。


## Specification:
### Input:
```
1. 選擇資料集
2. 選擇演算法
3. 運行次數
4. K範圍
```
### Output:
```
1. 當前K值
2. 收斂花費迭代
3. 花費時間
4. 輪廓係數，表樣本與同類別距離相近，不同類別距離遠離的程度，範圍[-1,1]
5. 平方誤差總和，表資料點和群中心的離散程度
```

## Manual:
- 資料集必須與程式相同資料夾

## Simulation Result:

### Environment:
- OS: Windows 10
- CPU: i7-6700HQ
- RAM: 8G
- Compiler: Python 3

### K-means(Iris)
**Time of  cluster** </br>
![](Image/time.png) </br>
**Silhouette_score of  cluster** </br>
![](Image/silhouette_score.png) </br>
**Sum_of_square_error** </br>
![](Image/sum_of_square_error.png) </br>

### K-means++(Abalone)

## Discussion


## Conclusion:

---
## License and copyright
© Jerry Cheng