# 文字列の探索

## 概要
文字列中から部分文字列を見つける操作。最初の一致位置や真偽で返す。

## 振る舞い
単純探索は O(n*m)。長いパターンや繰り返し検索では効率的なアルゴリズムを使う。見つからない場合の返り値を統一する。

## 例
function index_of(text, needle):
  i = 0
  while i <= length(text) - length(needle):
    if substring(text, i, length(needle)) == needle:
      return i
    i += 1
  return -1


## 注意点
大文字小文字の扱い、正規化、マルチバイト境界をそろえる。
