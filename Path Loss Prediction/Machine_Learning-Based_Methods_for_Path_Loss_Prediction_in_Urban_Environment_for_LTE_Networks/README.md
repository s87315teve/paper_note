# Machine Learning-Based Methods for Path Loss Prediction in Urban Environment for LTE Networks

## 研究背景與目的

- 機器學習方法被認為是預測路徑損耗的一種有前景的替代方案,可以取代傳統的經驗和確定性模型
- 本研究旨在評估不同機器學習方法在城市環境中LTE網絡的路徑損耗預測性能

## 使用的機器學習方法

1. 支持向量回歸 (Support Vector Regression, SVR)
2. 隨機森林 (Random Forest, RF)  
3. K近鄰 (K-Nearest Neighbor, KNN)
   
*補充: 本研究的Baseline model為 COST231 Walfisch-Ikegami empirical model*

## 資料集

- 使用 WinProp 軟體進行光線追蹤 (Ray-tracing) 模擬，為了節省模擬時間使用了光追的 Dominant path model 來生成城市環境中的 Path loss 資料
- 考慮了視線 (Line-of-Sight, LOS) 和非視線 (Non-Line-of-Sight, NLOS) 兩種傳播條件
- 總共收集了5150個路徑損耗樣本，其中LOS 2644個，NLOS 2506個
### 模擬參數
| 參數                | 內容                         |
|---------------------|------------------------------|
| Frequency           | 2120 / 2140 / 2160 MHz       |
| BS EIRP             | 40 dBm                       |
| BS Height   | 75 / 95 / 115 m              |
| Bandwidth           | 20 MHz                       |
| BS Antenna type     | Omnidirectional              |
| MS Height           | 1.5 m                        |
| MS Antenna type     | Omnidirectional              |
| MS Antenna Gain     | 0 dBi                        |
| Transmitted signal  | OFDMA/QPSK                   |

*BS: base station*<br>
*MS: mobile station, 可以當作地面用戶*

## 訓練過程與驗證

- 使用7個參數作為機器學習算法的輸入變數:
  1. BS和MS之間的距離
  2. BS高度
  3. MS高度
  4. 載波頻率
  5. 接收器位置的X坐標 
  6. 接收器位置的Y坐標
  7. 視線狀態 (LOS或NLOS)


- 性能評估指標
  1. 平均誤差 (Mean error, ME) 
  2. 均方根誤差 (Root mean square error, RMSE)
  3. 平均絕對百分比誤差 (Mean aabsolute percentage error, MAPE)
  4. 皮爾森積動差相關(Pearson product-moment correlation)
  *=>* $\rho$ *數值範圍-1\~1，完全負相關\~完全正相關*

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

*補充:各模型最佳參數*<br>
SVR: $\gamma = 1$ (i.e. $\sigma = 0.707$)<br>
KNN: K=20*
### LOS 條件下的模型性能比較表

|                    | KNN| SVR RBF | Random Forest | COST231 WI  |
|-------------------------|-----------|---------------|---------------------|------------------|
| **ME [dB]**             | 0.2       | 0.4           | -0.4                | 7.9              |
| **MAPE [%]**            | 1.2       | 1.2           | 1.6                 | 7.9              |
| **RMSE [dB]**           | 2.1       | 2.2           | 2.1                 | 8.4              |
| $\rho$          | 0.93      | 0.92          | 0.93                | 0.68             |
| **Ttrain [s]**          | 2         | 304           | 36                  | -                |

### NLOS 條件下的模型性能比較表

|                    | KNN | SVR RBF | Random Forest | COST231 WI |
|-------------------------|------------|----------------|----------------------|-------------------|
| **ME [dB]**             | -0.2       | 0.3            | 0.4                  | 18.3              |
| **MAPE [%]**            | 2.2        | 2.6            | 2.3                  | 15.5              |
| **RMSE [dB]**           | 3.4        | 4.1            | 3.6                  | 19.1              |
| $\rho$              | 0.89       | 0.83           | 0.89                 | 0.61              |
| **Ttrain [s]**          | 2         | 304              | 36                    | -                 |


## 結論

- 所有評估的機器學習算法都優於傳統經驗模型
- KNN 算法在性能和訓練時間上表現最佳，較適合用來預測都市環境的 Path loss


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
