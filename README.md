# Paper學習筆記
看paper+作筆記

---
## 分類
- Path loss + Machine learning
- Neural network architecture
- Sensor fusion 
- Dynamic transmission
- Survey
- Tools

---
### Path loss + Machine learning
 1. [將PCA, MLP, GP用於Path loss預測](/Path_Loss_Prediction/Path_Loss_Prediction_Based_on_Machine_Learning_Techniques_Principal_Component_Analysis_Artificial_Neural_Network_and_Gaussian_Process/README.md)
    * 關鍵字: PCA (Principal Component Analysis), ANN (Artificial Neural Network), MLP (Multilayer Perceptron), GP (Gaussian Process), Feature selection 
    * 簡介: 結合PCA、MLP和GP技術，提出一種高精度的路徑損耗預測方法，顯著提升了預測準確度並有利於高可靠性無線感測器網路設計
 2. [都市環境LTE網路的機器學習+Path loss預測](/Path_Loss_Prediction/Machine_Learning-Based_Methods_for_Path_Loss_Prediction_in_Urban_Environment_for_LTE_Networks/README.md)
    * 關鍵字: SVR (Support Vector Regression), RF (Random Forest), KNN (K-Nearest Neighbors), LTE (Long-Term Evolution), Ray-tracing
    * 簡介: 驗證了SVR、RF和KNN等機器學習方法在都市LTE網路 Path loss 預測任務中均優於傳統的經驗模型 COST231 Walfisch-Ikegami，特別是 KNN 在性能和訓練時間上表現最佳
 3. [使用Scalable Transformer來預測地圖兩點之間的Path loss](/Path_Loss_Prediction/Transformer-Based_Neural_Surrogate_for_Link-Level_Path_Loss_Prediction_from_Variable-Sized_Maps/README.md)
    * 關鍵字: Scalable Transformer, Resnet (Residual neural network), MLP (Multilayer perceptron), UNet, 3GPP TR38.901, Ray-tracing
    * 簡介: 提出了一個可擴展的Transformer架構，能夠從不同大小的地圖中預測Link-level path loss，並從稀疏資料中能夠有效學習與泛化，性能優於現有機器學習方法
 4. [使用深度學習預測室外毫米波的Path Loss Exponent](/Path_Loss_Presiction/Path_Loss_Exponent_Prediction_for_Outdoor_Millimeter_Wave_Channels_through_Deep_Learning/README.md)
    * 關鍵字: CNN (Convolutional Neural Network), VPL (Vertical Plane Launch), Ray-tracing, Millimeter wave, Path Loss Exponent (PLE), GIS (Geographic Information System)
    * 簡介: 提出了一種新的深度學習算法,使用CNN從3D地圖數據預測毫米波頻段的路徑損耗指數,結合了確定性模型的精確性和統計模型的快速推理時間,在各種環境中表現穩定,為5G毫米波頻段的快速路徑損耗預測提供了有效工具
 5. [使用RadioNet基於Transformer的模型進行密集城市環境無線電地圖預測](/Path_Loss_Prediction/radionet/README.md)
    * 關鍵字: RadioNet, Transformer, Grid Embedding, CNN (Convolutional Neural Network), UNet, Ray-tracing
    * 簡介: 提出了一個名為RadioNet的新型Transformer基礎模型，用於快速且可靠的無線電地圖預測。引入了網格嵌入技術來替代傳統的位置嵌入，更好地描述源、目標和環境障礙物之間的空間關係。在密集城市環境中，RadioNet顯著提高了預測準確性和可靠性，同時大幅提升了預測速度，相比光線追蹤方法快4個數量級。
 6. [使用衛星圖像的自監督學習來建立無處不在的2.6 GHz無線網路傳播模型](/Path_Loss_Prediction/2.6_GHz_Radio_Propagation_Model_for_Wireless_Networks_Using_Self-Supervised_Learning/README.md)
    * 關鍵字: Self-supervised learning, CNN (Convolutional Neural Network), ResNet50, MLP (Multilayer Perceptron), ROI (Region of Interest) Filter, Path loss prediction, Satellite images
    * 簡介: 提出了USARP (Ubiquitous Satellite Aided Radio Propagation) 模型，使用自監督學習從衛星圖像中提取無線環境特徵，結合CNN和MLP架構，顯著提升了路徑損耗預測的地理泛化能力，在多種無線傳播環境中表現優異
 7. [使用卷積神經網路FadeNet進行毫米波大規模信道衰落預測](/Path_Loss_Prediction/FadeNet_Deep_Learning-Based_mm-Wave_Large-Scale_Channel_Fading_Prediction_and_its_Applications/README.md)
    * 關鍵字: CNN (Convolutional Neural Network), U-Net, LSF (Large-Scale Fading), mm-Wave (Millimeter Wave), Ray-tracing
    * 簡介: 提出了FadeNet,一種基於改進U-Net架構的28層卷積神經網路,能夠從地形、建築和植被高度圖像預測毫米波大規模信道衰落,計算速度比傳統光線追蹤方法快40-1000倍,並在多個城市間展現了良好的泛化性能
 8. [使用人工神經網路建模預測都市環境的路徑損耗](/Path_Loss_Prediction/Artificial_Neural_Network_Modeling_for_Path_Loss/README.md)
    * 關鍵字: ANN (人工神經網路, Artificial Neural Network), MLP (多層感知器, Multilayer Perceptron), ReLU (修正線性單元, Rectified Linear Unit), L-BFGS (限制記憶體BFGS演算法, Limited-memory Broyden-Fletcher-Goldfarb-Shanno), 路徑損耗預測, 都市環境
    * 簡介: 提出了一種基於人工神經網路的多維度迴歸架構，用於3到6 GHz頻段都市環境的路徑損耗建模。透過對網路架構參數（如啟動函數、隱藏層數量和節點數）的分析，發現所提出的ANN模型比傳統線性模型更精確和靈活，特別是在高樓大廈環境中表現出色，為複雜都市環境的無線通訊網路規劃提供了更精確的工具。
### Neural network architecture
### Sensor fusion 
### Dynamic transmission
### Survey
### Tools
