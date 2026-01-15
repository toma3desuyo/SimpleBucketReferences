# カプセル化

## 概要
内部状態を隠し、公開APIを通じてのみ操作させる設計。状態の一貫性と変更容易性を高める。

## 振る舞い
フィールドを直接公開せず、検証を行うアクセサ越しに更新する。外部からは契約通りの操作だけが実行される。

## 例
class SecretBox:
  private content
  function set(value):
    content = clone(value)
  function get():
    return clone(content)


## 注意点
デバッグ目的であっても内部表現を直接晒すと後で差し替えにくくなる。
