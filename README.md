# ML-ScikitLearn-LinearRegression
Machine Learning  Scikit-learn - LinearRegression (線性迴歸) -房價預測


## 數據分成Train Set & Test Set
~~~
from sklearn.model_selection import train_test_split

X_train, X_test, Y_train, Y_test = train_test_split(X_data,Y_target,test_size=0.4, random_state=0)
~~~
* train_data：所要劃分的樣本特徵集
* train_target：所要劃分的樣本結果
* test_size：樣本占比，如果是整數的話就是樣本的數量
* random_state：是亂數種子。
- 亂數種子：其實就是該組亂數的編號，在需要重複試驗的時候，保證得到一組一樣的亂數。比如你每次都填1，其他參數一樣的情況下你得到的亂數組是一樣的。但填0或不   填，每次都會不一樣。亂數的產生取決於種子，亂數和種子之間的關係遵從以下兩個規則：種子不同，產生不同的亂數；種子相同，即使實例不同也產生相同的亂數。

## Model 優化
* 將數據集一致化處理
- 加快算法收斂速度,優化算法訓練的效率,但無法提升算法準確性
~~~
model = LinearRegression(normalize=True)
~~~
* 欠擬合現象
- 優化欠擬合模型
(A) 挖掘更多輸入特徵
(B) 增加多項式特徵 => 增加模型複雜度
~~~
from sklearn.preprocessing import PolynomialFeatures
from sklearn.pipeline import Pipeline
~~~

