# 文字列の置換

## 概要
文字列中の一部を別の内容に差し替える基本操作。テンプレート展開やマスキングで頻用される。

## 振る舞い
単一置換か全置換かを事前に決める。見つからない場合の扱い（無変更/例外）も呼び出し側で統一する。大文字小文字の区別やエンコード境界に注意。

## 例
function replace(text, needle, replacement):
  pos = find(text, needle)
  if pos < 0:
    raise Error("needle not found")
  return slice(text, 0, pos) + replacement + slice(text, pos + length(needle))


## 注意点
巨大文字列の全置換はメモリ再確保が増えるため、バッファを共有するかストリーミングで処理する。
