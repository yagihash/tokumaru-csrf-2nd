# 問題：間違ったCSRF対策〜中級編～
https://blog.tokumaru.org/2018/11/csrf_67.html

## Run
```
$: make up
$: open http://poc.local.xss.moe
```

## 解説
`strcmp()`を見た時点でarrayを食わせるパターンなので`token`ではなく`token[]`を送るようにしてあげる。

## 修正案
`strcmp()`を使わない。
