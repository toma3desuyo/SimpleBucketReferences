# べき乗演算子

## 概要
基数を指数回だけ乗じる演算。指数が大きいと急増する。

## 振る舞い
二乗法を使えば O(log n) で計算できる。オーバーフローや精度限界を監視する。

## 例
function power(base, exp):
  result = 1
  while exp > 0:
    if exp % 2 == 1:
      result *= base
    base *= base
    exp //= 2
  return result


## 注意点
負の指数や根を扱う場合は定義を追加する。
