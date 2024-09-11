# Artificial Neural Network Modeling for Path Loss Prediction in Urban Environments
---
*提醒: 本筆記為claude生成*
## 摘要

- 提出使用人工神經網路(Artificial Neural Network, ANN)進行多維度迴歸,以建立3-6 GHz頻段下城市環境的路徑損耗模型
- ANN學習測量的路徑損耗數據,這些數據是距離和頻率的函數
- 分析網路架構參數(激活函數、隱藏層數量、節點數量)對預測準確度的影響
- 觀察到提出的模型比傳統線性模型更準確和靈活

## 主要內容

1. **模型輸入**:
   - 距離 (meter)
   - 頻率 (MHz)

2. **模型輸出**:
   - 路徑損耗值 (dB)

3. **使用的機器學習模型**:
   - 多層感知器神經網路 (Multilayer Perceptron Neural Network, MLP-NN)

4. **網路架構**:
   - 輸入層
   - 隱藏層 (數量可變)
   - 輸出層

5. **激活函數**:
   - 整流線性單元 (Rectified Linear Unit, ReLU)
   - 邏輯S形函數 (Logistic Sigmoid)
   - 雙曲正切函數 (Hyperbolic Tangent)

6. **優化算法**:
   - 有限記憶BFGS (L-BFGS)算法

7. **實驗結果**:
   - ANN模型在兩個測試區域都優於現有模型
   - 區域A: 性能提升約7.74% - 9.49%
   - 區域B: 性能提升約21.70% - 24.18%
   - 雙曲正切激活函數的ANN模型在兩個區域都表現最佳

8. **結論**:
   - ANN學習模型在兩個區域分別平均提升了8.89%和23.26%的性能
   - 對於高樓公寓建築環境(區域B),ANN學習模型能提供更準確的估計

## 未來工作

- 考慮更多環境特徵的多維空間分析
- 基於不同場景的大型數據集分析
- 使用更複雜的ANN架構

---
### Citation

**Plain Text:**
C. Park, D. K. Tettey, and H.-S. Jo, "Artificial neural network modeling for path loss prediction in urban environments," arXiv preprint arXiv:1904.02383, 2019.


**BibTeX:**
```bibtex
@article{park2019artificial,
  title={Artificial neural network modeling for path loss prediction in urban environments},
  author={Park, Chanshin and Tettey, Daniel K and Jo, Han-Shin},
  journal={arXiv preprint arXiv:1904.02383},
  year={2019}
}
```