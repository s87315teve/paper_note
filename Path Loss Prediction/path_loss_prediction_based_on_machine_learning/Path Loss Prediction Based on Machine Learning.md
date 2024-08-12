# Path Loss Prediction Based on Machine Learning Techniques: Principal Component Analysis, Artificial Neural Network, and Gaussian Process

---
## 1. 研究目的

- 開發基於機器學習技術的路徑損耗預測新方法
- 結合PCA、ANN-MLP和Gaussian Process等技術

## 2. 主要方法

- 使用PCA進行特徵選擇和降維
- 採用ANN-MLP建立非線性路徑損耗模型  
- 使用Gaussian Process建立陰影效應模型
- 將ANN-MLP和Gaussian Process結合,形成完整的路徑損耗和陰影效應預測模型

## 3. 數據收集

- 在韓國農村地區進行實地測量
- 頻率:450MHz、1450MHz、2300MHz
- 發射天線高度15m,接收天線高度2m
- 測量距離範圍約3.5km

## 4. 結果分析

- PCA降維後模型性能與原始4特徵模型相當,但訓練時間大幅縮短
- ANN-MLP模型在路徑損耗預測上優於線性回歸和Gaussian Process模型
- 結合ANN-MLP和Gaussian Process的模型在預測覆蓋率上優於傳統的線性對數距離模型

## 5. 結論

- 提出的機器學習方法可以更準確地預測特定場地的路徑損耗
- 新方法在預測覆蓋率誤差小於1.6%,而傳統模型誤差可達12%
- 該方法有利於高可靠性無線傳感器網絡的設計

## 6. 未來研究方向

- 探索不同ANN結構的影響
- 開發只預測參考距離以外額外路徑損耗的ANN模型
- 將該方法應用於考慮天線高度、建築物高度等其他變量的預測模型開發

---
### Cite

**Plain Text:**
H.-S. Jo, C. Park, E. Lee, H. K. Choi, and J. Park, "Path loss prediction based on machine learning techniques: Principal component analysis, artificial neural network, and Gaussian process", Sensors, vol. 20, no. 7, p. 1927, 2020.


**BibTeX:**
```bibtex
@article{jo2020path,
  title={Path loss prediction based on machine learning techniques: Principal component analysis, artificial neural network, and Gaussian process},
  author={Jo, Han-Shin and Park, Chanshin and Lee, Eunhyoung and Choi, Haing Kun and Park, Jaedon},
  journal={Sensors},
  volume={20},
  number={7},
  pages={1927},
  year={2020},
  publisher={MDPI}
}
```
