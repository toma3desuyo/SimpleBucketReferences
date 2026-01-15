# 加算演算子

## 概要
数値同士を足し合わせる二項演算。合計値の計算やカウンタ更新に利用する。

## 振る舞い
整数ではオーバーフロー、浮動小数では丸め誤差に注意。単位が異なる値を足さない。

## 例
function add(a, b):
  result = a + b
  if overflow(result):
    raise Error("overflow")
  return result


## 注意点
累積加算の誤差を抑えたいときは小さい値から足すか補正アルゴリズムを検討する。
