# リストの結合(文字列化)

## 概要
リスト要素を区切り文字で連結し、単一の文字列にする。

## 振る舞い
各要素の文字列化規則を決め、null や未定義要素をどう扱うかを統一する。空リストは空文字を返すのが一般的。

## 例
function join(list, delimiter):
  buffer = ""
  for i, item in enumerate(list):
    if i > 0: buffer += delimiter
    buffer += to_text(item)
  return buffer


## 注意点
大量要素ではバッファビルダーを使って余分な再確保を避ける。
