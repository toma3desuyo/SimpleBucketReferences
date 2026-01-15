# 正規表現

## 概要
パターン文字列を使って部分一致や抽出を行う手法。

## 振る舞い
グローバル検索やグループキャプチャなど強力だが、バックトラッキングで性能が落ちることがある。

## 例
pattern = compile("([a-z]+)@(example\.com)")
match = pattern.find(text)
if match:
  user = match.group(1)


## 注意点
ユーザー入力をそのままパターンに埋め込むとReDoSの原因になるのでエスケープする。
