# インスタンスの初期化処理

## 概要
生成直後のオブジェクトに必須情報を設定し、不変条件を満たす状態にする。

## 振る舞い
必須パラメータが欠けていれば例外にする。外部リソース取得を伴う場合は失敗時に後始末を行う。

## 例
class Service:
  function init(config):
    require(config.endpoint)
    self.endpoint = config.endpoint


## 注意点
重い初期化は遅延実行に分け、並行実行環境では初期化の重複を防ぐ。
