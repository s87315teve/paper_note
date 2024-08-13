以下是這篇論文的重點摘要,使用markdown格式整理:

# 基於機器學習方法預測城市環境中LTE網絡的路徑損耗

## 研究背景與目的

- 機器學習方法被認為是預測路徑損耗的一種有前景的替代方案,可以取代傳統的經驗和確定性模型
- 本研究旨在評估不同機器學習方法在城市環境中LTE網絡的路徑損耗預測性能

## 使用的機器學習方法

1. 支持向量回歸 (Support Vector Regression, SVR)
2. 隨機森林 (Random Forest, RF)  
3. K近鄰 (K-Nearest Neighbor, KNN)

## 數據集與模擬

- 使用WinProp軟件進行模擬,生成城市環境中的路徑損耗數據
- 考慮了視線(Line-of-Sight, LOS)和非視線(Non-Line-of-Sight, NLOS)兩種傳播條件
- 總共收集了5150個路徑損耗樣本,其中LOS 2644個,NLOS 2506個

## 訓練過程與驗證

- 使用7個參數作為機器學習算法的輸入變量:
  1. 基站和移動站之間的距離
  2. 基站高度
  3. 移動站高度
  4. 載波頻率
  5. 接收器位置的X坐標
  6. 接收器位置的Y坐標
  7. 路徑可見性(LOS或NLOS)

- 採用10折交叉驗證方法
- 使用均方根誤差(Root Mean Square Error, RMSE)、平均絕對百分比誤差(Mean Absolute Percentage Error, MAPE)等指標評估性能

## 結果與討論

1. 所有機器學習算法的表現都優於經驗模型COST231 Walfisch-Ikegami
2. 在LOS條件下:
   - RMSE: 2.1-2.2 dB
   - MAPE: 1.2-1.6%
3. 在NLOS條件下:
   - RMSE: 3.4-4.1 dB
   - MAPE: 2.2-2.6%
4. KNN算法整體表現最佳:
   - LOS條件下RMSE: 2.1 dB
   - NLOS條件下RMSE: 3.4 dB
   - 訓練時間最短(2秒)

## 結論

- 所有評估的機器學習算法都優於傳統經驗模型
- KNN算法在性能和訓練時間上表現最佳,是城市環境路徑損耗預測的理想選擇


---
### Citation

**Plain Text:**
N. Moraitis, L. Tsipi and D. Vouyioukas, "Machine Learning-Based Methods for Path Loss Prediction in Urban Environment for LTE Networks," 2020 16th International Conference on Wireless and Mobile Computing, Networking and Communications (WiMob), Thessaloniki, Greece, 2020, pp. 1-6, doi: 10.1109/WiMob50308.2020.9253369. 



**BibTeX:**
```bibtex
@INPROCEEDINGS{9253369,
  author={Moraitis, Nektarios and Tsipi, Lefteris and Vouyioukas, Demosthenes},
  booktitle={2020 16th International Conference on Wireless and Mobile Computing, Networking and Communications (WiMob)}, 
  title={Machine Learning-Based Methods for Path Loss Prediction in Urban Environment for LTE Networks}, 
  year={2020},
  volume={},
  number={},
  pages={1-6},
  keywords={Urban areas;Machine learning algorithms;Predictive models;Training;Long Term Evolution;Machine learning;Computational modeling;3D simulation;Long Term Evolution (LTE);machine learning;path loss prediction;urban environment},
  doi={10.1109/WiMob50308.2020.9253369}}

```
