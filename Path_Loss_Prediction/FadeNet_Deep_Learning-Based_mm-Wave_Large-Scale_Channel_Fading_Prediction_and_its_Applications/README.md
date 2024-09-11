# FadeNet: Deep learning-based mm-wave large-scale channel fading prediction and its applications
---
*提醒: 本筆記為claude生成*
## 背景
- 5G 毫米波(mm-Wave)網路的規劃和優化需要準確預測大規模衰落(Large-Scale Fading, LSF)
- 現有方法計算成本高或不準確,不適合城市規模的小區規劃

## 提出方法: FadeNet
- 使用卷積神經網絡(Convolutional Neural Network)預測從基站到覆蓋區域的 LSF
- 輸入:
  - 地形高度(Terrain Height)
  - 建築物高度(Building Height)
  - 植被高度(Foliage Height)
  - 視線(Line-of-Sight, LoS)資訊(選用)
- 輸出:
  - 256x256 像素的 LSF 預測圖
- 網絡架構:
  - 28 層卷積網絡,基於 U-Net 改進
  - 使用跳躍連接(Skip Connections)
- 訓練數據:
  - 使用射線追蹤(Ray-Tracing)生成的 LSF 值作為地面真值(Ground Truth)

## 結果
- FadeNet 預測準確度優於統計方法
- 計算速度比射線追蹤快 40-1000 倍
- 加入 LoS 特徵可將預測 RMSE 降低 1.3 dB
- 在不同城市間的泛化性能良好

## 應用:最佳小區選址
- 可快速預測候選站點的覆蓋情況,大幅縮短網路規劃時間

## 局限性與未來工作
- 反射預測不夠準確
- 未考慮天線方向圖
- 可探索其他網絡架構

總的來說,FadeNet 提供了一種快速準確的 LSF 預測方法,可顯著提高毫米波網路規劃的效率。

---
### Citation

**Plain Text:**
V. V. Ratnam et al., "FadeNet: Deep Learning-Based mm-Wave Large-Scale Channel Fading Prediction and its Applications," in IEEE Access, vol. 9, pp. 3278-3290, 2021, doi: 10.1109/ACCESS.2020.3048583.



**BibTeX:**
```bibtex
@article{ratnam2020fadenet,
  title={FadeNet: Deep learning-based mm-wave large-scale channel fading prediction and its applications},
  author={Ratnam, Vishnu V and Chen, Hao and Pawar, Sameer and Zhang, Bingwen and Zhang, Charlie Jianzhong and Kim, Young-Jin and Lee, Soonyoung and Cho, Minsung and Yoon, Sung-Rok},
  journal={IEEE Access},
  volume={9},
  pages={3278--3290},
  year={2020},
  publisher={IEEE}
}

```