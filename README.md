# CNNwithRSE

## これは何?

[Towards Robust Neural Networks via Random Self-ensemble](https://arxiv.org/abs/1712.00673)をFGSMについて簡単に実装したもの。

学習に用いたデータはCIHAR-10で,適当につくったCNNへの非標的型攻撃について検証した。

## 結果

![output](https://user-images.githubusercontent.com/46624038/206204959-d2cf2e84-9959-4a83-8971-270ca383ac0c.png)

横軸がFGSMでどれだけ入力を変化させるかを制御するパラメタepsilonで縦軸がFGSMにより生成された敵対的サンプルに対する精度。
modelは無対策のモデル、rsemodel:ensemble{n}はNoise Layerの影響でぶれるn個の出力をアンサンブルしたときのRSEを導入したモデルについてのepsilonと精度との関係を表している。

以下にFGSMで生成された画像の例を示す。

- 無対策モデル(FGSM　epsilon=0.05)

![be00e8eb-0e77-4538-a251-5c8c34242caa](https://user-images.githubusercontent.com/46624038/206206639-03dbe6a1-0cbf-421d-b4c1-9b176029a752.png)


- RSEを導入したモデル(n=10)(FGSM epsilon=0.010)


![cd780a83-7355-4da8-a778-75be5c07cf6d](https://user-images.githubusercontent.com/46624038/206206442-b5e2714b-1b0c-465a-9c88-c16b8e8fea55.png)






## 学習済み重み

- model3.pth 無対策モデル
- rsemodel3.pth RSEを導入したモデル
