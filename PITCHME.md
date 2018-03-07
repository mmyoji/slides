#### 言語処理のための機械学習入門 第3回

2018-03-08 @mmyoji

---

## 1.5 パラメータ推定法

データからパラメータを推定する

1. 最尤推定
2. MAP 推定

---

## パラメータ

> パラメータとは、分布曲線を生成するために確率分布関数（PDF）の入力に使用できる母集団全体の記述的測度

[参考](https://support.minitab.com/ja-jp/minitab/18/help-and-how-to/statistics/basic-statistics/supporting-topics/data-concepts/what-are-parameters-parameter-estimates-and-sampling-distributions/)

---

## i.i.d.

independently, identically distributed

独立に同一の確率分布に従うデータ

* $P(D)$ 尤度 (likelihood) 積の形を取る

* $\log P(D)$ 対数尤度 和の形を取る

[参考](http://tkengo.github.io/blog/2016/06/16/yaruo-machine-learning6/)

(1.41) がわからない

---

## 最尤推定

maximum likelihood estimation

$\log P(D)$ が最大となるようなパラメータを求める

---

## seq. 最尤推定

P さんの例

$$ \log P(D) = \sum n\_{w} \log P\_{w} $$

をそのまま計算してもおかしな値になる

前提条件を考慮して、ラグランジュ関数を作る

(参考 P.14 1.2.3)

例題1.21 がわかりやすい

---

## MAP 推定

最大事後確率推定 maximum a posteriori estimation

* 事前確率分布 $P(\theta)$

* 事後確率分布 $P(\theta|D)$

事後確率分布を最大化するパラメータを求める

---

## seq. MAP 推定

P さんの例

1. ラグランジュ関数つくる
2. $p_{w}$ について偏微分
3. 連立方程式解く

---

## seq. MAP 推定

seq. P さんの例

* $n_{w}$ ... 各単語の出現回数
* $N$ ... $\sum n_{w}$
* $|V|$ ... 扱う単語の数

---

## References

* [パラメータ、パラメータ推定値、およびサンプル分布とは - Minitab](https://support.minitab.com/ja-jp/minitab/18/help-and-how-to/statistics/basic-statistics/supporting-topics/data-concepts/what-are-parameters-parameter-estimates-and-sampling-distributions/)
* [やる夫で学ぶ機械学習 - 対数尤度関数 - けんごのお屋敷](http://tkengo.github.io/blog/2016/06/16/yaruo-machine-learning6/)

---

おわり

