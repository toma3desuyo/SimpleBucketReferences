# 剰余演算子

## 概要
割り算の余りを求める演算。

## 振る舞い
負数を含む場合の結果符号は言語で異なるため、仕様を確認する。

## 例
function mod(a, b):
  if b == 0: raise Error("division by zero")
  return a - floor(a / b) * b


## 注意点
周期計算やハッシュに使うときは負数入力の扱いを統一する。
