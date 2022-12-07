# CNNwithRSE

## これは何?

[Towards Robust Neural Networks via Random Self-ensemble](https://arxiv.org/abs/1712.00673)をFGSMについて簡単に実装したもの。

学習に用いたデータはCIHAR-10で,適当につくったCNNへの非標的型攻撃について検証した。

## 結果

![output](https://user-images.githubusercontent.com/46624038/206204959-d2cf2e84-9959-4a83-8971-270ca383ac0c.png)




## 学習済み重み

- model3.pth 無対策モデル
- rsemodel3.pth RSEを導入したモデル
