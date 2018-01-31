## Python Machine Learning 4th

2018-02-01 @mmyoji

---

## Content

第5章 次元削減でデータを圧縮する

* 5.1 主成分分析による教師なし次元削減

---

## 次元削減, What For?

* 計算効率の改善
* 「次元の呪い」を減らす
    * 次元が多すぎると、学習モデルの効率が下がる的な

---

## 主成分分析 PCA

* Principal Component Analysis
* 教師なし線形変換法
* 主に次元削減タスクに用いられる
* 特徴量どうしの相関関係に着目し、パターンを抽出
* 高次元データにおいて、分散が最大となる方向を見つけ、より低い次元へ射影
* 全特徴量に等しい重要度を割り当てたいなら、事前に標準化する必要

---

## seq. 主成分分析 PCA

1. d次元のデータセットを標準化
2. 標準化したデータセットの共分散行列を作成
3. 共分散行列から固有ベクトルと固有値を求める
4. 最大となる k 個の固有値に対応する k 個の固有ベクトルを選択 (`k <= d`)
5. 上記固有ベクトルから射影行列 W を作成
6. W を使って d 次元のデータセット X を変換し、新しい k 次元の特徴部分空間を取得

---

## まとめ

標準化したデータ作ったら

`sklearn.decomposition.PCA#fit_transform` に

ぶち込め

---

## References

* [次元の呪いについて - Qiita](https://qiita.com/tn1031/items/96e7131cd41df1aebe85)
* [次元の呪い (Curse of dimensionality) とは何なのか - Qiita](https://qiita.com/kibinag0/items/b1c0dac7df941ee42315)

---

おわり

