# 例外処理

## 概要
通常フローで扱えないエラーを検知し、補足・再送出・後始末を行う仕組み。

## 振る舞い
try/catch/finally などで囲み、失敗の文脈を付けて上位に伝える。握り潰さず、リソース解放を必ず実行する。

## 例
function safe_run(task):
  try:
    return task()
  catch err:
    log(err)
    raise err
  finally:
    cleanup()


## 注意点
制御フローの分岐に例外を多用せず、予測できる失敗は戻り値で扱う。
