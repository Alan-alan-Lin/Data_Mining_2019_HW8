# Data_Mining_2019_HW8
用python 對 Wine.csv 對目標 quality 進行 Ensemble learning 並與未使用的結果進行比較:  
1.先讀取csv檔，並且區分Feature和Target，存成x和y，引入 KFold 進行 cross validation 驗證，將 n_splits 設 10，以進行 10 Folds cross-validation  
![img](https://github.com/Alan-alan-Lin/Data_Mining_2019_HW8/blob/main/HW_8/Python_3.JPG)  
![img](https://github.com/Alan-alan-Lin/Data_Mining_2019_HW8/blob/main/HW_8/Python_4.JPG)  
2.以 10 Folds cross-validation 進行 DecisionTreeClassifier 分類，得到的準確率約為0.8947  
![img](https://github.com/Alan-alan-Lin/Data_Mining_2019_HW8/blob/main/HW_8/Python_13.JPG)  
3.以 10 Folds cross-validation 進行 BaggingClassifier，n_estimators= 10，得到的準確率為0.9395  
![img](https://github.com/Alan-alan-Lin/Data_Mining_2019_HW8/blob/main/HW_8/Python_14.JPG)  
![img](https://github.com/Alan-alan-Lin/Data_Mining_2019_HW8/blob/main/HW_8/Python_15.JPG)  
4.以 10 Folds cross-validation 進行 RandomForestClassifier 分類，得到的準確率約為0.9499  
![img](https://github.com/Alan-alan-Lin/Data_Mining_2019_HW8/blob/main/HW_8/Python_16.JPG)  
![img](https://github.com/Alan-alan-Lin/Data_Mining_2019_HW8/blob/main/HW_8/Python_17.JPG)  
5.以 10 Folds cross-validation 進行 AdaBoost , n_estimators =10，得到的準確率約為0.8859  
![img](https://github.com/Alan-alan-Lin/Data_Mining_2019_HW8/blob/main/HW_8/Python_18.JPG)  
![img](https://github.com/Alan-alan-Lin/Data_Mining_2019_HW8/blob/main/HW_8/Python_19.JPG)  
基本上使用進行 Ensemble learning 的分類器去進行資料分類得到的準確度都較高，除了 AdaBoost：0.8859 < Decision Tree：0.8947，剩下Bagging(0.9394)和 RandomForest(0.9499)準確率都超過 9 成  
