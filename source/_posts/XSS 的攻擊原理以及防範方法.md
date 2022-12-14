---
title: XSS 的攻擊原理以及防範方法
tags:
- 資安
- XSS
categories:
- 資安
---
### 攻擊原理
XSS 為 Cross-site Scriptinng 的縮寫，中文為「跨網站指令碼」。

利用網站漏洞將帶有程式的 `<script>` 標籤或其它腳本程式注入網站，讓攻擊者可以取得更高的權限，例如讓網站重新導向至惡意連結或取得 cookie 等。

### 防範方法：避免直接輸出
1. 跳脫
   若能將 `<script>` 經過編碼轉換，在 html 渲染時以純文字的方式印出，就能避免 XSS。
2. 過濾
   若需要將使用者輸入文字以 html 渲染出來，例如部落格文章中的 `<h1>`、`<h2>`、`<h3>` 等標籤，則可以採用過濾的方式，把 `script`、`iframe` 等標籤針對性的不直接印出。
