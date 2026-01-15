# 条件分岐

## 概要
条件に応じて処理を切り替える制御。

## 振る舞い
相互排他的な条件は順序を決め、重複を避ける。デフォルト分岐を用意して未定義ケースをなくす。

## 例
function classify(score):
  if score >= 80: return "high"
  else if score >= 50: return "mid"
  else: return "low"


## 注意点
条件が増えたら表駆動やポリモーフィズムへの置き換えを検討する。
