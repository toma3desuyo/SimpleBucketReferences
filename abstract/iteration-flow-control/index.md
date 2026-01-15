# 反復フロー制御

## 概要
ループの途中で処理をスキップしたり終了させたりする制御（continue / break / 早期 return など）。

## 振る舞い
多段の脱出は意図が読みにくくなるため、条件を早期にまとめるか関数分割でシンプルにする。

## 例
for each item in stream:
  if should_skip(item):
    continue
  if should_stop(item):
    break
  process(item)


## 注意点
リソース解放が必要な場合はループを抜ける経路すべてで後始末が行われるようにする。
