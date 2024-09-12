# An Ubiquitous 2.6 GHz Radio Propagation Model for Wireless Networks Using Self-Supervised Learning From Satellite Images

---
*提醒: 本筆記為claude生成*


## 研究背景
- 無線網路性能依賴於適當的無線覆蓋,路徑損失(Path Loss, PL)模型是評估覆蓋的重要工具
- 機器學習和深度神經網路近期被應用於無線傳播建模,允許使用非傳統輸入如衛星圖像
- 然而,數據驅動的PL模型通常假設訓練和測試數據分佈相似,這在實際場景中是不成立的
- 因此,泛化能力(模型在不同數據分佈上的表現)對移動網路運營商至關重要

## 提出方法:USARP模型
- 名稱:Ubiquitous Satellite Aided Radio Propagation (USARP) model
- 目標:增強經驗PL模型的地理泛化能力
- 創新點:使用自監督學習從衛星圖像中提取無線環境的一般表示

### 輸入:
1. 衛星圖像
2. 基站(BS)和用戶設備(UE)位置
3. 無線鏈路變量:
   - 3D距離的對數: log₁₀(d₃D)
   - 有效高度: h_eff

### 輸出:
- 預測的路徑損失(PL)值

### 模型架構:
1. ROI過濾層:突出衛星圖像中的關鍵區域
2. ResNet50 CNN:從衛星圖像提取特徵
3. 多層感知機(MLP):處理CNN特徵和無線鏈路變量
4. 最後一個線性層:結合所有特徵進行PL預測

### 使用的機器學習技術:
- 自監督學習(Self-Supervised Learning):用於預訓練ResNet50
- 卷積神經網絡(CNN):ResNet50用於處理衛星圖像
- 多層感知機(MLP):用於特徵處理和最終預測
- 正則化技術:Dropout和L2正則化

## 主要結果
- USARP模型在驗證和泛化數據集上都優於基準模型
- 在泛化數據集上,USARP的均方根誤差(RMSE)為12.34 dB,比線性回歸模型低1 dB
- 衛星圖像輸入改善了驗證集上的RMSE超過3 dB,泛化集上約1 dB
- USARP模型展示了在多種無線傳播環境中使用的潛力,甚至超過了針對特定環境優化的線性回歸模型

## 結論
USARP模型通過適當的架構設計、正則化方法和有效利用衛星圖像數據,增強了經驗PL模型的地理泛化能力。這為開發可在多種無線環境中使用的通用PL模型提供了新的方向。


---
### Citation

**Plain Text:**
M. Sousa, P. Vieira, M. P. Queluz and A. Rodrigues, "An Ubiquitous 2.6 GHz Radio Propagation Model for Wireless Networks Using Self-Supervised Learning From Satellite Images," in IEEE Access, vol. 10, pp. 78597-78615, 2022, doi: 10.1109/ACCESS.2022.3193486.





**BibTeX:**
```bibtex
@article{sousa2022ubiquitous,
  title={An ubiquitous 2.6 GHz radio propagation model for wireless networks using self-supervised learning from satellite images},
  author={Sousa, Marco and Vieira, Pedro and Queluz, Maria Paula and Rodrigues, Ant{\'o}nio},
  journal={IEEE Access},
  volume={10},
  pages={78597--78615},
  year={2022},
  publisher={IEEE}
}
```
