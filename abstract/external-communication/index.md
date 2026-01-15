# 外部通信

## 概要
プロセス外やネットワーク越しにデータを送受信する操作。

## 振る舞い
タイムアウト・再試行・エラー時の扱いを決め、通信部分は抽象化してテストで差し替えられるようにする。

## 例
function call_endpoint(request):
  response = send(request, timeout=3000)
  if not response.ok:
    raise Error("remote failure")
  return parse(response.body)


## 注意点
冪等でない操作の再送には注意し、機密情報をログに残さない。
