# An Ubiquitous 2.6 GHz Radio Propagation Model for Wireless Networks Using Self-Supervised Learning From Satellite Images

---

## 1. 論文背景
- 移動無線網絡（Mobile Wireless Networks, MWN）的性能取決於適當的無線電覆蓋範圍，其中路徑損耗（Path Loss, PL）模型是評估其性能的重要工具。
- 隨著機器學習（Machine Learning, ML）和深度神經網絡（Deep Neural Networks, DNNs）的進步，基於數據驅動的PL模型得到了開發，並開始考慮使用衛星影像作為非傳統輸入數據。
- 然而，這些模型通常假設訓練數據與測試數據具有相似的分佈，這在現實情況中是一個薄弱的假設，因此模型的泛化能力成為關鍵問題。

## 2. 研究目的
- 本文提出了一種新的數據驅動PL模型，稱為**USARP（Ubiquitous Satellite Aided Radio Propagation）模型**，目的是通過使用衛星影像提高現有PL模型的地理泛化能力。
- USARP模型使用了自我監督學習技術來從衛星影像中提取無線電環境的通用數據表示，並將其與3GPP的PL模型進行比較，結果顯示誤差減少約9 dB。

## 3. 主要貢獻
- 分析了經驗PL模型和ML/DNN基於不同數據分佈的地理泛化能力。
- 提出了兩階段開發過程：1）使用自我監督學習從衛星影像中學習無線電環境的表示；2）將這些表示與實際測量數據結合，用於PL預測。
- 開發了一個新的數據驅動PL預測模型——**USARP模型**，並對其架構進行了優化，以提高其在多種無線電環境中的泛化能力。

## 4. USARP模型架構
- USARP模型的輸入包括衛星影像、基站（BS）和用戶設備（UE）的位置，以及描述BS和UE之間無線電連接的變量（例如3D距離和有效高度）。
- 模型利用CNN（ResNet50）來處理衛星影像，並結合了多層感知器（MLP）來進行最終的PL預測。

## 5. 結果與討論
- 在驗證和泛化數據集上，USARP模型的性能顯著優於基線模型（包括3GPP和各種ML回歸模型）。
- 特別是在泛化數據集上，USARP模型的RMSE減少了約1 dB，這顯示了其在不同無線電環境下的優越性能。

## 6. 結論
- 本研究提出的USARP模型利用衛星影像進行自我監督學習，大幅提高了PL預測的精度和地理泛化能力，對未來的無線網絡規劃具有重要意義。



